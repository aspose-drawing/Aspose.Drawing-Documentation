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
Using the Aspose.Drawing 2D graphic library for .NET (C#), you can effortlessly create fascinating drawings. This graphic library provides the capability to work with various font styles, sizes, and colors, enabling the transformation of ordinary fonts into graphic art. It empowers you to manipulate graphic objects and create colored outlines around font characters.
</p>

### C# code examples

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To demonstrate the capabilities of the graphic library, we will craft a text drawing in a lollipop-inspired style. Beginning with the word "Lollipop" as our base text string, we will enhance it with vibrant outlines. To make the font more intriguing, we'll decorate the font edges with circular white "nuts" measuring 35 pixels in diameter. To create a showcase video, we can gradually decrease the nut size by 1 pixel starting from every 20 frames.
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

<a href="https://reference.aspose.com/drawing/net/aspose.drawing.drawing2d/graphicspath/addstring/#addstring_2">GraphicsPath.AddString
</a>

### Resulting font drawing

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

### Source code:

<a href="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/blob/master/Examples/Showcases/Showcases/LollipopFont.cs">LollipopFont.cs</a>
