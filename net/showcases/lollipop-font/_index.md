---
title: "Creating Lollipop Font drawing"
type: docs
url: /net/showcases/lollipop-font/
weight: 20
description: Creating Lollipop Font drawing with Aspose.Drawing .NET (C#) 2d graphic library
keywords: [2d graphic library, font drawing, text drawing, font styles]
---

## Creating Lollipop Font

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Using the Aspose.Drawing 2D graphic library for .NET (C#), you can effortlessly create fascinating drawings. This graphic library provides the capability to work with various font families, styles, sizes, and colors, enabling the transformation of ordinary fonts into graphic art. It empowers you to manipulate graphic objects and create colored outlines around font characters.
</p>

<style>
   .frame {
    border: 2px solid darkgray;
    padding: 5px;
    margin: 10px 0 5px 5px;
    background: #f0f0f0;
    align-items: center;
   }
   .marginauto {
    margin: 10px auto 20px;
    display: block;
   }
   .frame figcaption {
    margin: 0 auto;
    display: flex;
    flex-direction: row;
    justify-content: center;
   }
   .container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
   }
</style>

<figure class="frame"><p>
    <img class="marginauto" src="./sample_LollipopFont.png" alt="Lollipop Font drawing" width="640" height="360"/>
<figcaption>Lollipop Font drawing</figcaption>
</p></figure>

### C# code examples

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To demonstrate the capabilities of the graphic library, we will create a text drawing in a lollipop-inspired style. Beginning with the word "Lollipop" as our base text string, we will enhance it with vibrant outlines. To add intrigue to the font, we'll decorate the edges with circular white "nuts," each measuring 35 pixels in diameter. For a dynamic showcase video, we'll gradually reduce the nut size by 1 pixel every 20 frames. In each frame, we will render the word "Lollipop" on a black background, complete with a mirrored reflection to simulate a water reflection effect. Finally, we will save each resulting image frame as a separate PNG file.
</p>

```cs
private static readonly string word = "Lollipop";
private static readonly Size frameSize = new(1920, 1080);

for (int i = 0; i < (makeVideo ? frames : 1); ++i)
{
    nutDiameter = 35.0f - (i % 20);
    Bitmap image1 = DrawWord(word);
    Bitmap bitmap = DrawReflection(image1, frameSize.Width, frameSize.Height);

    string fileName = string.Format("{0}/{1:d4}.png", outputDirectory, i + 1);
    bitmap.Save(fileName);
    Console.WriteLine(fileName);
}
```

#### Drawing word

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Initially, generate a bitmap graphic with dimensions of `w x h`, where `w`` corresponds to the width of the word's characteristics, and `h` is three times the font size's height. Enable high-quality smoothing mode and set a black background color. We will use the "Arial" font family and center the string alignment.
</p>

```cs
private static Bitmap DrawWord(string word)
{
    int w = word.Length * fontSize;
    int h = fontSize * 3;
    int margin = 5;

    Bitmap bitmap = new(w, h, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
    Graphics graphics = Graphics.FromImage(bitmap);
    graphics.SmoothingMode = SmoothingMode.HighQuality;

    graphics.Clear(Color.Black);

    FontFamily fontFamily = new("Arial");
    StringFormat stringFormat = new()
    {
        Alignment = StringAlignment.Center,
        LineAlignment = StringAlignment.Center
    };
//...
}
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
We utilize the <a href="https://reference.aspose.com/drawing/net/aspose.drawing.drawing2d/graphicspath/addstring/#addstring_2">GraphicsPath.AddString</a> method to incorporate the word into a graphics path. Following that, in the `VisitPoints` procedure, we generate a list of points that align with this path. For every fifth point along the path, we introduce a circle of "nuts" using the <a href="https://reference.aspose.com/drawing/net/aspose.drawing.drawing2d/graphicspath/addellipse/#addellipse">GraphicsPath.AddEllipse</a> method, but only if the distance between two nut points exceeds 12 pixels.
</p>

```cs
Rectangle rectangle = new(0, fontSize, w, fontSize);

GraphicsPath path = new();
path.AddString(word, fontFamily, (int)FontStyle.Bold, fontSize, rectangle, stringFormat);

GraphicsPath path2 = new();
path2.AddString(word, fontFamily, (int)FontStyle.Bold, fontSize, rectangle, stringFormat);

VisitPoints(path, path2, graphics, AddEllipseToPath);

private static void VisitPoints(
    GraphicsPath path,
    GraphicsPath path2,
    Graphics graphics,
    Action<RectangleF, Graphics, GraphicsPath> handler)
{
    PointF[] points = path.PathPoints;
    PointF prev = new(0, 0);
    float diameter = nutDiameter;
    for (int i = 0; i < path.PointCount; ++i)
    {
        PointF point = points[i];
        if (i % 5 == 0 && Distance(point, prev) > 12)
        {
            RectangleF rectangle = new(
                point.X - diameter / 2,
                point.Y - diameter / 2,
                diameter,
                diameter);
            handler(rectangle, graphics, path2);
        }
        prev = point;
    }
}

private static void AddEllipseToPath(RectangleF rectangle, Graphics graphics, GraphicsPath path)
{
    path.AddEllipse(rectangle);
}
```

#### Selecting lollipop colors

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Next, we'll assemble a palette of 30 colors for our lollipop-style drawing. This entails creating two sets of colors: the first set is for background colors, and the second set comprises the basic palette colors. By blending these two sets, we'll obtain our lollipop colors.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
For the initial 30 background colors, we'll take a two-part approach. The first 15 colors will be randomly selected from the RGB color space, while the next 15 will be calculated as complementary colors to the first part. Subsequently, we'll select 30 palette colors for the second color set. These colors will be evenly distributed, with the starting point chosen randomly from a predefined palette image file "palette.png". The selection of each specific color will be accomplished using the <a href="https://reference.aspose.com/drawing/net/aspose.drawing/color/fromargb/#fromargb_2">Color.FromArgb</a> method.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To derive our final lollipop colors, we'll blend palette colors with background colors according to the following scheme. The 30 colors will be divided into intervals of 4, with palette colors mixed with background colors in proportions of 70%, 40%, 20%, and 10%, respectively. This pattern will repeat within each interval.
</p>

```cs
private static List<Color> GetColors(int half, Random r)
{
    int start = 0;
    int range = 255;
    List<Color> colors = new();

    int count = half * 2;
    for (int i = 0; i < count; ++i)
    {
        Color c;
        if (i < half)
        {
            c = Color.FromArgb(start + r.Next(range), start + r.Next(range), start + r.Next(range));
            colors.Add(c);
        }
        else
        {
            Color o = colors[i % half];
            c = Color.FromArgb(255 - o.R, 255 - o.G, 255 - o.B);
            colors.Add(c);
        }
    }

    List<Color> palette = new();
    Bitmap image1 = new(Path.Combine(inputDirectory, "palette.png"));
    int w = image1.Width;
    int index = r.Next(w);
    int step = w / count;

    for (int i = 0; i < count; ++i)
    {
        index += step;
        index %= w - 1;
        Color c = image1.GetPixel(index, 0);
        palette.Add(c);
    }

    List<Color> result = new();
    int interval = 4;
    for (int i = 0; i < count; ++i)
    {
        Color c;
        if (i % interval == 0)
        {
            c = Blend(palette[i], colors[i], 0.7);
        }
        else if (i % interval == 1)
        {
            c = Blend(palette[i], colors[i], 0.4);
        }
        else if (i % interval == 2)
        {
            c = Blend(palette[i], colors[i], 0.2);
        }
        else
        {
            c = Blend(palette[i], colors[i], 0.1);
        }
        result.Add(c);
    }

    return result;
}

private static Color Blend(Color color, Color backColor, double amount)
{
    byte r = (byte)(color.R * amount + backColor.R * (1 - amount));
    byte g = (byte)(color.G * amount + backColor.G * (1 - amount));
    byte b = (byte)(color.B * amount + backColor.B * (1 - amount));
    return Color.FromArgb(r, g, b);
}
```

The base rainbow palette image file used for color generation:

<figure class="frame"><p>
    <img class="marginauto" src="./palette640.png" alt="Color palette for drawing" width="640" height="33"/>
<figcaption>Color palette</figcaption>
</p></figure>

The resulting 30 lollipop colors are derived from the rainbow palette but are partially blended with random background colors at intervals of every 4 colors:

<figure class="frame"><p>
    <img class="marginauto" src="./Lollipop-colors.webp" alt="Lollipop colors drawing fragment" width="640" height="602"/>
<figcaption>Fragment of lollipop 30 colors drawing</figcaption>
</p></figure>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

</p>

```cs
Random r = new(seed);
int half = 15; // of pen amount
int doubleStroke = 3 * 2; // the double width of stroke is increment of real pen width
List<Color> colors = GetColors(half, r);
Pen widest = new(colors[0], half * 2 * doubleStroke);

for (int i = 0; i < half * 2; ++i)
{
    Color c = colors[i];
    Pen pen = new(c, (half * 2 - i) * doubleStroke)
    {
        LineJoin = LineJoin.Round
    };

    if (i == 0)
    {
        widest = pen;
    }

    graphics.DrawPath(pen, path2);
}

LinearGradientBrush brush = new(
    rectangle,
    Color.White,
    Color.Gray,
    LinearGradientMode.Vertical);
graphics.FillPath(brush, path);

VisitPoints(path, path, graphics, DrawAndFillEllipse);

path2.Widen(widest);
bitmap = Crop(bitmap, path2, margin);
```

#### Drawing reflection

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The reflection image effect enhances the visual attractiveness of the drawing. To simulate an image mirroring effect, we generate a new bitmap graphic with high-quality smoothing and interpolation modes enabled. Subsequently, we draw two lollipop word images using the <a href="https://reference.aspose.com/drawing/net/system.drawing/graphics/drawimage/#drawimage_20">Graphics.DrawImage</a> method. The first image is positioned above the horizon line, while the second one is positioned below it and is vertically inverted with its height reduced by half. The lower image is further shaded by applying the <a href="https://reference.aspose.com/drawing/net/system.drawing/graphics/fillrectangle/#fillrectangle_1">Graphics.FillRectangle</a> method, which applies a linear gradient transparency effect, transitioning vertically from a level of 150 to the maximum black level of 255.
</p>

```cs
public static Bitmap DrawReflection(Bitmap image1, int w, int h)
{
    Bitmap bitmap = new(w, h, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
    Graphics graphics = Graphics.FromImage(bitmap);
    graphics.SmoothingMode = SmoothingMode.HighQuality;
    graphics.InterpolationMode = InterpolationMode.HighQualityBicubic;
    graphics.Clear(Color.Black);

    float bw = image1.Width;
    float bh = image1.Height;

    graphics.DrawImage(image1, new RectangleF(
        w / 2 - bw / 2,
        horizon - bh,
        bw,
        bh));

    graphics.DrawImage(image1, new RectangleF(
        w / 2 - bw / 2,
        horizon + bh / 2,
        bw,
        -bh / 2));

    RectangleF rectangle = new(
        w / 2 - bw / 2,
        horizon,
        bw,
        bh / 2);

    LinearGradientBrush brush = new(
        rectangle,
        Color.FromArgb(150, 0, 0, 0),
        Color.FromArgb(255, 0, 0, 0),
        LinearGradientMode.Vertical);
    graphics.FillRectangle(brush, rectangle);

    return bitmap;
}
```

### Lollipop font showcase video

<script type="application/ld+json">
{
    "@context": "https://schema.org/",
    "@type": "VideoObject",
    "name": "Celtic Heart figure text",
    "duration": "PT00M20S",
    "uploadDate": "2023-09-16",
    "embedUrl": "https://www.youtube.com/embed/wLFASipfdRM",
    "thumbnailUrl": "https://i9.ytimg.com/vi/wLFASipfdRM/mqdefault.jpg?sqp=CMi6oKgG-oaymwEmCMACELQB8quKqQMa8AEB-AH-CYAC0AWKAgwIABABGCggVShyMA8=&rs=AOn4CLAZ-4ZL0q8d2h17Ju3AjoWaxoCn3w",
    "description": "Creating Lollipop Font drawing with Aspose.Drawing .NET (C#) 2d graphic library",
}
</script>

<iframe width="1156" height="650" src="https://www.youtube.com/embed/wLFASipfdRM" title="Lollipop Font" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Source code

<a href="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/blob/master/Examples/Showcases/Showcases/LollipopFont.cs">LollipopFont.cs</a>
