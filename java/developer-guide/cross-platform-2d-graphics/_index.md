---
type: docs
url: /java/developer-guide/cross-platform-2d-graphics/
weight: 7
title: Cross Platform 2D Graphics Library
description: Aspose.Drawing library for Java to draw pictures. Cross-platform image drawing library for 2D graphics.
keywords: [
drawing pictures,
image drawing,
2d drawing,
cross platform,
Drawing library for Windows,
Drawing library for Linux,
Graphics library for Web application
]
---

## Cross-platform Graphics Library for 2D Drawing Pictures for Java

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Java drawing libraries play a pivotal role in crafting 2D drawing applications and services. Designing a Java application for image drawing with compatibility across various platforms not only broadens your audience reach but also demands minimal effort. Aspose.Drawing stands out as a cross-platform solution for Java, ensuring compatibility with any platform where Java is available and consistently delivering high-quality results.
</p>

### Aspose.Drawing Supported Platforms

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The Aspose graphic library for Java extends beyond Windows platforms and enjoys popularity on systems like MacOS, Linux, Android, and Web services. The Aspose.Drawing Java API boasts cross-platform compatibility, enabling simultaneous utilization on various platforms. This not only streamlines the development process but also allows you to reuse code across multiple platforms after developing it once.
</p>

### Installing Aspose.Drawing for Java from Maven Repository

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
If you are developing within the Maven, you can easily install Aspose.Drawing using the Maven Repository.
</p>

```xml
<repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://repository.aspose.com/repo/</url>
    </repository>
</repositories>
```

<p align='justify'>
Then define Aspose.Drawing for Java API dependency in your pom.xml as follows:
</p>

```xml
<dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-drawing</artifactId>
        <version>23.11</version>
        <classifier>jdk16</classifier>
   </dependency>

   <!-- if you need a documentation, please add the following dependency. For example it could be useful for IDE. -->
   <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-drawing</artifactId>
        <version>23.11</version>
        <classifier>javadoc</classifier>
   </dependency>
</dependencies>
```

<p align='justify'>
For more detailed installation instructions please visit the
<a href="https://docs.aspose.com/drawing/java/installation/">Aspose.Drawing Installation Guide</a>.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Aspose.Drawing for Java can function as a graphic library across diverse platforms, encompassing Windows, MacOS, Linux, and Android applications. In IDEs like Eclipse, you have the flexibility to create new projects and run Java programs as Console Applications on Windows, Linux, MacOS, or as Web applications.
</p>

### **Aspose.Drawing for Java Use Cases**

#### **Draw a Text on Image**

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
One of the most popular use case for 2D drawing is adding text to images, such as creating text on images for making gift cards. In the example below, we will draw a text string "Happy Birthday!" on the available space at the bottom right corner of the existing image. We will use the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/solidbrush/">`SolidBrush` tool</a> to draw the text string. You should choose the desired text color and a font with the appropriate size and style. Next, calculate the position of the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/rectangle/">`Rectangle` structure</a> to fit the text, and then draw the text string using the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawString-java.lang.String-com.aspose.drawing.Font-com.aspose.drawing.Brush-com.aspose.drawing.RectangleF-">`DrawString` method</a>.
</p>

Example of Java code to draw text on an image:

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-TextFonts-DrawText-GiftCard.java" >}}

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
        <img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/TextFonts/girl_giftCard.jpg" alt="Text drawing on image gift card" width="476" height="315"/>
    </div>
</div>
<figcaption>Drawing text on image</figcaption>
</figure>


#### **Draw a Photo Frame**

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Moreover, you can enhance the visual appeal by creating a color frame around images or photographs. This can be easily accomplished by choosing a <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/pen/">`Pen` tool</a> with your desired color and using the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawRectangle-com.aspose.drawing.Pen-int-int-int-int-">`DrawRectangle` method</a> to draw the frame with the calculated width and height.
</p>

Example of Java code to draw a color frame around a photo:

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-LinesCurvesShapes-DrawRectangle-PhotoWithFrame.java" >}}

<figure class="frame">
<div class="container"><div>Source image</div><div>Resulting image</div></div>
<div class="container">
    <div>
        <img src="cat.jpg" alt="Frame drawing on image" width="476" height="268"/>
    </div>
    <div>
       <img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/TextFonts/cat_with_honor_out.jpg" alt="Frame drawing on image" width="476" height="268"/>
    </div>
</div>
<figcaption>Frame drawing on image</figcaption>
</figure>


#### **Make Callouts**

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Another useful scenario involves creating callouts on images to add supplementary information, such as diameter size details in mm. Callouts consist of several graphics primitives, and to draw them, we need to utilize various drawing methods such as <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawLine-com.aspose.drawing.Pen-int-int-int-int-">`DrawLine`</a>, <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawEllipse-com.aspose.drawing.Pen-com.aspose.drawing.RectangleF-">`DrawEllipse`</a>, and <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawString-java.lang.String-com.aspose.drawing.Font-com.aspose.drawing.Brush-com.aspose.drawing.RectangleF-">`DrawString`</a>.
</p>

Example of Java code to draw callouts on an image:

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-TextFonts-DrawCallOut.java" >}}

<figure class="frame">
<div class="container"><div>Source image</div><div>Resulting image</div></div>
<div class="container">
    <div>
        <img src="gears.png" alt="Callouts drawing on image" width="176" height="183"/>
    </div>
    <div>
        <img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/TextFonts/gears_with_callout_out.png" alt="Callouts drawing on image" width="176" height="183"/>
    </div>
</div>
<figcaption>Callouts drawing on image</figcaption>

</figure>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The Aspose.Drawing Java graphics library operates seamlessly on various platforms, relying solely on its rendering functions, eliminating the need to install any additional third-party components. For more examples, please visit <a href="https://github.com/aspose-drawing/Aspose.Drawing-for-Java/">Aspose.Drawing for Java GitHub repository</a>.
</p>
