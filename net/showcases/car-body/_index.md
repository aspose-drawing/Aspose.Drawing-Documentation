---
title: "Creating Car Body Drawing"
type: docs
url: /net/showcases/car-body/
weight: 20
description: Creating Car Body drawing with Aspose.Drawing .NET (C#) 2d graphic library. The library allows to creation of drawings with color transparency levels, semi-transparent images and text rendering.
keywords: [2d graphic library, create drawings, drawing .NET, Bezier curves, mix bitmap, bitmap frames, alpha layer, skin designs, transparency level, text drawings, text rendering, text hinting, anti-aliasing, graphics smoothing, c# code example]
---

## Creating Car Body Drawing

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The Aspose.Drawing .NET (C#) 2d graphic library provides designers with a powerful tool for creating captivating drawings. You can combine various existing images and text strings, layering them semi-transparently to create new drawings. In the example below, we will use a car image and add a logo image with text to draw on the car's body.
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

<figure class="frame">
<div class="container">
    <div>
        <figcaption>Logo image</figcaption>
    </div>
    <div>
        <figcaption>Car body image</figcaption>
    </div>
</div>
<div class="container">
    <div>
        <img src="./brit-01.png" alt="Logo image" width="125" height="102"/>
    </div>
    <div>
        <img src="./carbody-sedan-04.png" alt="Car body image" width="640" height="274"/>
    </div>
</div>
<figcaption>Source images</figcaption>
</figure>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To showcase the drawing capabilities, let's create various skin designs for the car's body image. The `Skin` class comprises a background color, and within it, the `DesignElement` class further consists of a `Banner` class containing a text string and a `Logo` class with image attributes. Now you can assign different skins with background colors using the <a href="https://reference.aspose.com/drawing/net/aspose.drawing/color/fromargb/#fromargb_3">Color.FromArgb</a> method. The FromArgb() method creates a new skin color using four parameters: the first one sets the alpha layer to determine transparency levels, followed by R, G, B color palette parameters. So, skins number 1 and 2 in the code example below will use only a colored background, while skins 3 and 4 use additional `DesignElements` with a logo image, a position, and the banner text strings "KEWIN" and "ANCHOR," respectively. Define a font name, size, style and color per each `Banner` element:
</p>

```cs
Skin skin1 = new() { Background = Color.FromArgb(120, 0, 80, 80) };
skins.Add(skin1);

Skin skin2 = new() { Background = Color.FromArgb(80, 180, 80, 0) };
skins.Add(skin2);

Skin skin3 = new() { Background = Color.FromArgb(80, 80, 80, 180) };
skin3.Design.Add(new DesignElement(
    new Logo(Path.Combine(inputDirectory, "brit-01.png"), new PointF(333, h - 253))));
skin3.Design.Add(new DesignElement(
    new Banner("KEWIN", new Font("Arial", 140, FontStyle.Bold, GraphicsUnit.Pixel),
    Color.FromArgb(120, 0, 255, 255), new PointF(350, h - 277))));
skins.Add(skin3);

Skin skin4 = new() { Background = Color.FromArgb(120, 255, 255, 0) };
skin4.Design.Add(new DesignElement(
    new Logo(Path.Combine(inputDirectory, "anchor-01.png"), new PointF(275, h - 290))));
skin4.Design.Add(new DesignElement(
    new Banner("ANCHOR", new Font("Verdana", 120, FontStyle.Bold | FontStyle.Italic, GraphicsUnit.Pixel),
    Color.FromArgb(120, 255, 0, 0), new PointF(250, h - 285))));
skins.Add(skin4);
```

### Car body coloration

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Next, we create a `GraphicsPath` object named `carBody`, which outlines the car image using Bezier curves. We then incorporate a new Bitmap frame created from both the `carBody` and the skin using the `DrawFrame` function:
</p>

```cs
GraphicsPath carBody = MakeCarBody(h);

foreach (Skin skin in skins)
{
    frames.Add(DrawFrame(w, h, carBody, skin));
}
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The `DrawFrame` function creates new `Bitmap` graphics with dimensions `w x h` and a white background color. We enable graphics smoothing with high quality and text rendering hinting with anti-aliasing attributes. Following that, we load a source car body PNG image file and use the <a href="https://reference.aspose.com/drawing/net/aspose.drawing/graphics/drawimage/#drawimage_14">Graphics.DrawImage method</a> to render it onto the bitmap. Additionally, we fill the interior of the car body's `GraphicsPath` with the skin's background color using the <a href="https://reference.aspose.com/drawing/net/aspose.drawing/graphics/fillpath/">FillPath method</a>. So, the background color will applied only to the `carBody` outline region:
</p>

```cs
private static Bitmap DrawFrame(int w, int h, GraphicsPath carBody, Skin skin)
{
    Bitmap bitmap = new(w, h);
    Graphics g = Graphics.FromImage(bitmap);
    g.Clear(Color.White);
    g.SmoothingMode = SmoothingMode.HighQuality;
    g.TextRenderingHint = TextRenderingHint.AntiAlias;

    Bitmap rasterCar = new(Path.Combine(inputDirectory, "carbody-sedan-04.png"));
    g.DrawImage(rasterCar, new RectangleF(0, 0, w, h));

    Brush brush1 = new SolidBrush(skin.Background);
    g.FillPath(brush1, carBody);
//...
}
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
If our skin comprises a `Banner` text and a `Logo` image, we will also render them onto the graphics using the <a href="https://reference.aspose.com/drawing/net/aspose.drawing/graphics/drawstring/#drawstring_4">DrawString</a> and <a href="https://reference.aspose.com/drawing/net/aspose.drawing/graphics/drawimage/#drawimage_14">DrawImage</a> methods. We use <a href="https://reference.aspose.com/drawing/net/aspose.drawing/graphics/clip/">Graphics.Clip property</a> in order to cut drawn text string and image logo only to the clip region corresponding to the `carBody` outline:
</p>

```cs
Bitmap bitmap2 = new(w, h);
Graphics g2 = Graphics.FromImage(bitmap2);
g2.SmoothingMode = SmoothingMode.HighQuality;
g2.TextRenderingHint = TextRenderingHint.AntiAlias;

g2.Clip = new Region(carBody);

foreach (DesignElement de in skin.Design)
{
    if (de.Banner is not null)
    {
        Brush brush2 = new SolidBrush(de.Banner.Color);
        g2.DrawString(de.Banner.Text, de.Banner.Font, brush2, de.Banner.Place.X, de.Banner.Place.Y);
    }

    if (de.Logo is not null)
    {
        Bitmap logo = new(de.Logo.ImageFile);
        g2.DrawImage(logo, new RectangleF(de.Logo.Place.X, de.Logo.Place.Y, logo.Width, logo.Height));
    }
}
```

### Transparent bitmap blending

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;


<a href="https://reference.aspose.com/drawing/net/aspose.drawing.imaging/imageattributes/">ImageAttributes class</a>

<a href="https://reference.aspose.com/drawing/net/aspose.drawing.imaging/imageattributes/setcolormatrix/#setcolormatrix_2">ImageAttributes.SetColorMatrix</a>

<a href="https://reference.aspose.com/drawing/net/aspose.drawing.imaging/colormatrix/colormatrix/#constructor_1">ColorMatrix</a>

</p>

```cs
g.Clip = new Region(carBody);

ImageAttributes imageAttributes = new();
ColorMatrix colorMatrix = new(new float[][]
{
    new float[] { 1, 0, 0, 0, 0 },
    new float[] { 0, 1, 0, 0, 0 },
    new float[] { 0, 0, 1, 0, 0 },
    new float[] { 0, 0, 0, 0.7f, 0 },
    new float[] { 0, 0, 0, 0, 1 }
});

imageAttributes.SetColorMatrix(
    colorMatrix,
    ColorMatrixFlag.Default,
    ColorAdjustType.Bitmap);

PointF[] destParallelogram = new PointF[]
{
    new PointF( 0, 0 ),
    new PointF( w, 0 ),
    new PointF( 0, h ),
};

g.DrawImage(
    bitmap2,
    destParallelogram,
    new RectangleF(0, 0, w, h),
    GraphicsUnit.Pixel,
    imageAttributes);
```


### Mixing two bitmaps

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Furthermore, we can mix bitmap frames that feature various skins into a sequence of images, which can then be saved to files in the PNG format. This allows two skins to be simultaneously blended into the car body image, separated by an edge line. To create a mixed bitmap we assign two objects `frame1` and `frame2` with current and next bitmaps skins:
</p>

```cs
Bitmap frame = new(1920, 1080, PixelFormat.Format32bppPArgb);
Graphics g = Graphics.FromImage(frame);
g.SmoothingMode = SmoothingMode.HighQuality;

for (int f1 = 0; f1 < frames.Count; f1++)
{
    int f2 = (f1 + 1) % frames.Count;
    frame1 = frames[f1];
    frame2 = frames[f2];

    for (int i = 0; i < (makeVideo ? 200 : 1); i++)
    {
        ++frameNumber;
        percent = makeVideo ? i * step % 100 : 25;
        mixedFrame = Mix(w, h, frame1, frame2, percent);
        DrawEdge(w, h, carBody, mixedFrame, percent);

        for (int n = 0; n < 2; n++)
        {
            for (int m = 0; m < 3; m++)
            {
                g.DrawImage(mixedFrame, (1920 - 50) / 2 * n, (1080 - 50) / 3 * m - 40);
            }
        }

        string fileName = string.Format("{0}/{1:d5}.png", outputDirectory, frameNumber);
        frame.Save(fileName);
        Console.WriteLine(fileName);
    }
}
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
We will mix two bitmaps with different skins to create a new one, gradually changing the proportion from 0% to 100%. On this resulting bitmap, we will use the <a href="https://reference.aspose.com/drawing/net/aspose.drawing/graphics/drawimage/#drawimage_9">DrawImage</a> method to draw the left portion from 'frame1' and the right portion from 'frame2', divided by a vertical edge line whose position is determined by the 'percent' variable:
</p>

```cs
private static Bitmap Mix(int w, int h, Bitmap frame1, Bitmap frame2, float percent)
{
    Bitmap bitmap = new(w, h);
    Graphics g = Graphics.FromImage(bitmap);
    g.SmoothingMode = SmoothingMode.HighQuality;

    float edgePosition = w * percent / 100;

    RectangleF rect1 = new(edgePosition, 0, w - edgePosition, h);
    g.DrawImage(frame1, rect1, rect1, GraphicsUnit.Pixel);

    RectangleF rect2 = new(0, 0, edgePosition, h);
    g.DrawImage(frame2, rect2, rect2, GraphicsUnit.Pixel);

    return bitmap;
}
```

### Drawing laser edge line

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Additionally, we will draw a laser vertical line between the two bitmaps, which will be 5 pixels wide. To achieve this, we create a rectangle at a position that corresponds to the percentage of the skin bitmaps mixing proportion. We then obtain the region, which is an intersection of our rectangle and the `carBody` graphics path, using the <a href="https://reference.aspose.com/drawing/net/aspose.drawing/region/intersect/#intersect_1">Region.Intersect</a> method. Finally, we fill this region with a magenta-colored brush.
</p>

```cs
private static readonly Brush edgeBrush = Brushes.Magenta;

private static void DrawEdge(int w, int h, GraphicsPath carBody, Bitmap frame, float percent)
{
    float edgeSize = 5.0f;
    float edgePosition = w * percent / 100;

    Rectangle rect = new(
        (int)(edgePosition - edgeSize / 2), 0,
        (int)(edgeSize), h);

    Region edge = new(carBody);
    edge.Intersect(rect);

    Graphics g = Graphics.FromImage(frame);
    g.FillRegion(edgeBrush, edge);
}
```

### Resulting drawings

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Because of the transparency established by the alpha layer, the resulting car body images acquire a new color, as well as the logo image and text drawings. In the drawing example below two skins are shown on the car body at the same time:
</p>

<figure class="frame"><p>
    <img class="marginauto" src="./sample_CarBody.png" alt="Car body drawing" width="640" height="212"/>
<figcaption>Car body drawing</figcaption>
</p></figure>

### Showcase video

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Finally, you can convert the series of PNG images with mixed skins into MP4 video with 30 frames per second and H.264 codec using `ffmpeg` program:
</p>

```sh
ffmpeg -framerate 30 -i ./out/%%05d.png -vcodec libx264 -pix_fmt yuv420p ./out/CarBody.mp4
```

<script type="application/ld+json">
{
    "@context": "https://schema.org/",
    "@type": "VideoObject",
    "name": "Car Body drawing",
    "duration": "PT00M30S",
    "uploadDate": "2023-09-16",
    "embedUrl": "https://www.youtube.com/embed/xvEuQHaHWrk",
    "thumbnailUrl": "https://i9.ytimg.com/vi/xvEuQHaHWrk/mqdefault.jpg?sqp=CMi6oKgG-oaymwEmCMACELQB8quKqQMa8AEB-AH-CYAC0AWKAgwIABABGFUgVihlMA8=&rs=AOn4CLAAyl52MFXaz0bGBtDwjlO_vH9-5Q",
    "description": "Creating Car Body drawing with Aspose.Drawing .NET (C#) 2d graphic library",
}
</script>

<iframe width="1156" height="650" src="https://www.youtube.com/embed/xvEuQHaHWrk" title="CarBody" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Source code

Please see the full C# code example on the Aspose.Drawing Github: [CarBody.cs](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/blob/master/Examples/Showcases/Showcases/CarBody.cs)
