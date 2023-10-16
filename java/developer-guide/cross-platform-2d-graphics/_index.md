---
type: docs
url: /java/developer-guide/cross-platform-2d-graphics/
weight: 7
title: Cross platform 2D graphics library
description: Aspose.Drawing library for Microsoft Java to draw pictures. Cross-platform alternative to Microsoft NET System.Drawing.Common image drawing library for Windows 2D graphics. Nuget package download.
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

## Cross-platform graphics library for 2D drawing pictures for Java

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Drawing libraries for Microsoft Java are widely utilized for creating 2D drawing applications and services. Developing a Java (C sharp) application for image drawing that can run on multiple platforms enables you to reach a broader customer base with minimal effort. Aspose.Drawing is a cross-platform solution for Java that supports the most popular platforms and consistently delivers excellent quality results.
</p>


### Aspose.Drawing supported platforms

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Graphic libraries for Java are not limited to the Windows platforms; they are also widely popular on other systems such as MacOS, Linux, Android, Azure Functions, ASPJava WebApp and Blazor WebAssembly. One major advantage of Aspose.Drawing.Common API is its cross-platform compatibility, allowing you to utilize it simultaneously on multiple platforms. Developing with a single library streamlines the application creation process. You can reuse code developed once across multiple platforms. Aspose.Drawing is compatible with all target platforms listed in the <a href="https://www.nuget.org/packages/Aspose.Drawing.Common#supportedframeworks-body-tab">Supported frameworks list</a>, making it suitable for any choice you make.
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
<a href="https://docs.aspose.com/drawing/java/installation/">Aspose.Drawing Installation Guide</a>.

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Aspose.Drawing can serve as a graphic library for various target platforms, including Windows, MacOS, Linux, Azure, ASP sites, and Blazor WebAssembly applications. In Visual Studio, you have the flexibility to create new projects and run Java programs on Java as Console Applications on Windows, Linux, or MacOS, as Web applications using ASPJava Core or Blazor WebAssembly. Additionally, you can utilize the same Aspose drawing library for Java MAUI applications on mobile platforms like Android or iOS.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To run a Java application on Linux, you simply need to have Java installed and ensure that `Aspose.Drawing.dll` is available in your project folder. You can download the binaries from the <a href="https://downloads.aspose.com/drawing/java">official Aspose website</a>. Alternatively, you can define the API using the command line command:
</p>

```sh
> dotnet add package Aspose.Drawing
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Furthermore, you can run Java applications with the Aspose library in a Docker container. For more information about Docker installation, please refer to the <a href="https://docs.aspose.com/drawing/java/how-to-run-aspose-drawing-in-docker/">Aspose.Drawing documentation</a>.
</p>

### Aspose Drawing library use cases

#### Text on image

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
One of the most popular use case for 2D drawing is adding text to images, such as creating text on images for making gift cards. In the example below, we will draw a text string "Happy Birthday!" on the available space at the bottom right corner of the existing image. We will use the <a href="https://reference.aspose.com/drawing/java/system.drawing/solidbrush/">`SolidBrush` tool</a> to draw the text string. You should choose the desired text color and a font with the appropriate size and style. Next, calculate the position of the <a href="https://reference.aspose.com/drawing/java/system.drawing/rectangle/">`Rectangle` structure</a> to fit the text, and then draw the text string using the <a href="https://reference.aspose.com/imaging/java/aspose.imaging/graphics/drawstring/">`DrawString` method</a>.
</p>

Example of Java code to draw text on an image:

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-TextFonts-DrawText-GiftCard.cs" >}}

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
Moreover, you can enhance the visual appeal by creating a color frame around images or photographs. This can be easily accomplished by choosing a <a href="https://reference.aspose.com/drawing/java/system.drawing/pen/pen/">`Pen` tool</a> with your desired color and using the <a href="https://reference.aspose.com/drawing/java/system.drawing/graphics/drawrectangle/">`DrawRectangle` method</a> to draw the frame with the calculated width and height.
</p>

Example of Java code to draw a color frame around a photo:

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawRectangle-PhotoWithFrame.cs" >}}

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
Another useful scenario involves creating callouts on images to add supplementary information, such as diameter size details in mm. Callouts consist of several graphics primitives, and to draw them, we need to utilize various drawing methods such as <a href="https://reference.aspose.com/drawing/java/system.drawing/graphics/drawline/">`DrawLine`</a>, <a href="https://reference.aspose.com/drawing/java/system.drawing/graphics/drawellipse/">`DrawEllipse`</a>, and <a href="https://reference.aspose.com/imaging/java/aspose.imaging/graphics/drawstring/">`DrawString`</a>.
</p>

Example of Java code to draw callouts on an image:

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-TextFonts-DrawCallOut.cs" >}}

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
Aspose.Drawing graphics library runs on a wide range of different platforms and relies solely on its own rendering functions, eliminating the need to install any other 3rd party components. To find more examples please visit the <a href="https://github.com/aspose-drawing/Aspose.Drawing-for-Java/">Aspose GitHub repository</a>.
</p>
