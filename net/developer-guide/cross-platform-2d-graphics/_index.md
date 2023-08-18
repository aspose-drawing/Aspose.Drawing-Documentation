---
type: docs
url: /net/developer-guide/cross-platform-2d-graphics/
weight: 7
title: Cross platform 2D graphics library
description: Aspose.Drawing library for Microsoft .NET to draw pictures. Cross-platform alternative to Microsoft NET System.Drawing.Common image drawing library for Windows 2D graphics. Nuget package download.
keywords: [
drawing pictures,
c sharp,
dot net,
asp net,
microsoft net,
nuget package,
image drawing,
2d drawing,
csharp net,
cross platform,
web assembly,
Drawing library for Windows,
Drawing library for Linux,
Drawing library for Azure,
Graphics library for ASP site,
Graphics library for Web application,
Drawing library for Blazor
]
---

## Cross-platform graphics library for 2D drawing pictures for .NET

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Drawing libraries for Microsoft .NET are widely utilized for creating 2D drawing applications and services. Developing a C# (C sharp) application for image drawing that can run on multiple platforms enables you to reach a broader customer base with minimal effort. Aspose.Drawing is a cross-platform solution for .NET that supports the most popular platforms and consistently delivers excellent quality results.
</p>


### Aspose.Drawing supported platforms

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Graphic libraries for .NET are not limited to the Windows platforms; they are also widely popular on other systems such as MacOS, Linux, Android, Azure Functions, ASP.NET WebApp and Blazor WebAssembly. One major advantage of Aspose.Drawing.Common API is its cross-platform compatibility, allowing you to utilize it simultaneously on multiple platforms. Developing with a single library streamlines the application creation process. You can reuse code developed once across multiple platforms. Aspose.Drawing is compatible with all target platforms listed in the <a href="https://www.nuget.org/packages/Aspose.Drawing.Common#supportedframeworks-body-tab">Supported frameworks list</a>, making it suitable for any choice you make.
</p>


### How to install Aspose.Drawing for different platforms

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
If you are developing within the Visual Studio development environment, you can easily install Aspose.Drawing using the integrated NuGet package manager. Simply search for `Aspose`, select `Aspose.Drawing` or `Aspose.Drawing.Common`, and click Install. Alternatively, you can install Aspose.Drawing from the NuGet package manager command line by typing the following command:
</p>

```sh
> Install-Package Aspose.Drawing
```

For more detailed installation instructions please visit the
<a href="https://docs.aspose.com/drawing/net/installation/">Aspose.Drawing Installation Guide</a>.

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Aspose.Drawing can serve as a graphic library for various target platforms, including Windows, MacOS, Linux, Azure, ASP sites, and Blazor WebAssembly applications. In Visual Studio, you have the flexibility to create new projects and run C# programs on .NET as Console Applications on Windows, Linux, or MacOS, as Web applications using ASP.NET Core or Blazor WebAssembly. Additionally, you can utilize the same Aspose drawing library for .NET MAUI applications on mobile platforms like Android or iOS.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run a .NET application on Linux, you simply need to have .NET installed and ensure that `Aspose.Drawing.dll` is available in your project folder. You can download the binaries from the <a href="https://downloads.aspose.com/drawing/net">official Aspose website</a>. Alternatively, you can define the API using the command line command:
</p>

```sh
> dotnet add package Aspose.Drawing
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Furthermore, you can run C# applications with the Aspose library in a Docker container. For more information about Docker installation, please refer to the <a href="https://docs.aspose.com/drawing/net/how-to-run-aspose-drawing-in-docker/">Aspose.Drawing documentation</a>.
</p>

### Aspose Drawing library use cases

#### Text on image

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
One of the most popular use case for 2D drawing is adding text to images, such as creating text on images for making gift cards. In the example below, we will draw a text string "Happy Birthday!" on the available space at the bottom right corner of the existing image. We will use the <a href="https://reference.aspose.com/drawing/net/system.drawing/solidbrush/">`SolidBrush` tool</a> to draw the text string. You should choose the desired text color and a font with the appropriate size and style. Next, calculate the position of the <a href="https://reference.aspose.com/drawing/net/system.drawing/rectangle/">`Rectangle` structure</a> to fit the text, and then draw the text string using the <a href="https://reference.aspose.com/imaging/net/aspose.imaging/graphics/drawstring/">`DrawString` method</a>.
</p>

Example of C# code to draw text on an image:

```cs
using (var image = Image.FromFile(Path.Combine(RunExamples.GetDataDir(), "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);

    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;

    SolidBrush brush = new SolidBrush(Color.Navy);
    Font font = new Font("Calibri", 20, FontStyle.Italic);

    int padding = 5;

    string text = "Happy Birthday!";
    var words = text.Split(' ');

    int extentWidth = 0;
    int extentHeight = 0;

    words.ToList().ForEach(word => { var stringSize = graphics.MeasureString(word, font);
                                        extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
                                        extentHeight += (int)stringSize.Height; });

    Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth,
                                        image.Height - padding - extentHeight,
                                        extentWidth,
                                        extentHeight);

    graphics.DrawString(text, font, brush, rectangle);

    image.Save(Path.Combine(RunExamples.GetDataDir(), "UseCases", "girl_card.jpg"));
}
```

<style>
   .frame {
    border: 2px solid darkgray;
    padding: 5px;
    margin: 0 auto;
    background: #f0f0f0;
    align-items: center;
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
<div class="container"><div>Source image</div><div>Resulting image</div></div>
<div class="container">
    <div>
        <img src="girl.jpg" alt="Text drawing on image gift card" width="476" height="315"/>
    </div>
    <div>
        <img src="girl_card.jpg" alt="Text drawing on image gift card" width="476" height="315"/>
    </div>
</div>
<figcaption>Frame drawing on image</figcaption>
</figure>


#### Photo frame

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Moreover, you can enhance the visual appeal by creating a color frame around images or photographs. This can be easily accomplished by choosing a <a href="https://reference.aspose.com/drawing/net/system.drawing/pen/pen/">`Pen` tool</a> with your desired color and using the <a href="https://reference.aspose.com/drawing/net/system.drawing/graphics/drawrectangle/">`DrawRectangle` method</a> to draw the frame with the calculated width and height.
</p>

Example of C# code to draw a color frame around a photo:

```cs
using (var image = Image.FromFile(Path.Combine(RunExamples.GetDataDir(), "UseCases", "cat.jpg")))
{
    var graphics = Graphics.FromImage(image);

    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;

    var pen = new Pen(Color.Magenta, 1);

    int gap = 2;

    graphics.DrawRectangle(pen, 0, 0, image.Width - 1, image.Height - 1);
    graphics.DrawRectangle(pen, gap, gap, image.Width - gap - 1, image.Height - gap - 1);

    image.Save(Path.Combine(RunExamples.GetDataDir(), "UseCases", "cat_with_honor.jpg"));
}
```

<figure class="frame">
<div class="container"><div>Source image</div><div>Resulting image</div></div>
<div class="container">
    <div>
        <img src="cat.jpg" alt="Frame drawing on image" width="476" height="268"/>
    </div>
    <div>
       <img src="cat_with_honor.jpg" alt="Frame drawing on image" width="476" height="268"/>
    </div>
</div>
<figcaption>Frame drawing on image</figcaption>
</figure>


#### Make callouts

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Another useful scenario involves creating callouts on images to add supplementary information, such as diameter size details in mm. Callouts consist of several graphics primitives, and to draw them, we need to utilize various drawing methods such as <a href="https://reference.aspose.com/drawing/net/system.drawing/graphics/drawline/">`DrawLine`</a>, <a href="https://reference.aspose.com/drawing/net/system.drawing/graphics/drawellipse/">`DrawEllipse`</a>, and <a href="https://reference.aspose.com/imaging/net/aspose.imaging/graphics/drawstring/">`DrawString`</a>.
</p>

Example of C# code to draw callouts on an image:

```cs
// callout with size
using (var image = Image.FromFile(Path.Combine(RunExamples.GetDataDir(), "UseCases", "gears.png")))
{
    var graphics = Graphics.FromImage(image);

    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;

    DrawCallOut(graphics, new PointF(107, 55), new PointF(179, 5), 74, "mm");

    DrawCallOut(graphics, new PointF(111, 146), new PointF(29, 180), 28, "mm");

    image.Save(Path.Combine(RunExamples.GetDataDir(), "UseCases", "gears_with_callout.jpg"));
}

void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
{
    Pen pen = new Pen(Color.LightGray, 1);

    Font font = new Font("Arial", 10, FontStyle.Bold);

    string outputValue = $"{value} {unit}";

    var textSize = graphic.MeasureString(outputValue, font);

    int diameterSymbolSize = 12;
    int spaceSize = 3;

    textSize.Width += diameterSymbolSize + spaceSize;

    float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
    float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;

    graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);

    float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
    float textAnchorY = callOutMiddleY;
    graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY,
                     textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX,
                     callOutMiddleY);

    graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize,
                                           (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));

    graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1,
                          (int)textAnchorX + diameterSymbolSize + 2,
                          (int)textAnchorY - diameterSymbolSize - 2);

    SolidBrush brush = new SolidBrush(Color.LightGray);

    graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize,
                                                 (int)(textAnchorY - textSize.Height));
}
```

<figure class="frame">
<div class="container"><div>Source image</div><div>Resulting image</div></div>
<div class="container">
    <div>
        <img src="gears.png" alt="Callouts drawing on image" width="176" height="183"/>
    </div>
    <div>
        <img src="gears_with_callout.jpg" alt="Callouts drawing on image" width="176" height="183"/>
    </div>
</div>
<figcaption>Callouts drawing on image</figcaption>

</figure>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Aspose.Drawing graphics library runs on a wide range of different platforms and relies solely on its own rendering functions, eliminating the need to install any other 3rd party components. To find more examples please visit the <a href="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/">Aspose GitHub repository</a>.
</p>
