---
title: "Creating Car Body Drawing"
type: docs
url: /net/showcases/car-body/
weight: 20
description: Creating Car Body drawing with Aspose.Drawing .NET (C#) 2d graphic library
keywords: [2d drawing,]
---

## Creating Car Body Drawing

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The Aspose.Drawing .NET (C#) graphic library provides designers with a powerful tool for creating captivating drawings. You can combine various existing images and text strings, layering them semi-transparently to create new drawings. In the example below, we will use a car image and add a logo image with text to the car's body. To demonstrate this capability, let's create several skin designs for the car's body image.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The `Skin` class consists of a background color and the `DesignElement` class, which in turn consists of a `Banner` class with a text string and a `Logo` class with image attributes:
</p>

```cs
internal class Banner
{
    public string Text;
    public Font Font;
    public Color Color;
    public PointF Place;

    public Banner(string text, Font font, Color color, PointF place)
    {
        this.Text = text;
        this.Font = font;
        this.Color = color;
        this.Place = place;
    }
}

internal class Logo
{
    public string ImageFile;
    public PointF Place;

    public Logo(string imageFile, PointF place)
    {
        this.ImageFile = imageFile;
        this.Place = place;
    }
}

internal class DesignElement
{
    public Banner? Banner;
    public Logo? Logo;

    public DesignElement(Banner banner)
    {
        this.Banner = banner;
    }

    public DesignElement(Logo logo)
    {
        this.Logo = logo;
    }
}

internal class Skin
{
    public Color Background = new();
    public List<DesignElement> Design = new();
}
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Now you can assign different skins with background colors using the <a href="https://reference.aspose.com/drawing/net/system.drawing/color/fromargb/#fromargb_2">Color.FromArgb</a> method. The FromArgb() method creates a new skin color using four parameters: the first one sets the alpha layer to determine transparency levels, followed by R, G, B color palette parameters. So, skins number 1 and 2 in the code example below will use only a colored background, while skins 3 and 4 use additional `DesignElements` with a logo image, a position, and the text strings "KEWIN" and "ANCHOR," respectively:
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

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Then we create a `GraphicsPath` carBody variable with the car image outline drawing with Bezier curves.
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

<a href="https://reference.aspose.com/drawing/net/aspose.drawing/graphics/drawimage/#drawimage_8">Graphics.DrawImage method</a>

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
...
}
```



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


<figure class="frame"><p>
    <img class="marginauto" src="./sample_CarBody.png" alt="Car body drawing" width="640" height="212"/>
<figcaption>Car body drawing</figcaption>
</p></figure>

### Video

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


Full C# code example:
