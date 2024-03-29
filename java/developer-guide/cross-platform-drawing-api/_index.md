---
type: docs
url: /java/developer-guide/cross-platform-drawing-api/
weight: 8
title: Cross-Platform Drawing API
description: Aspose.Drawing library for Java for drawing pictures. Cross-platform support of Java Graphics API for 2D geometric drawings such as drawing lines, drawing shapes, drawing paths and drawing rectangles.
keywords: [drawing pictures,
lines drawing,
draw lines,
vector images,
vector file,
drawing shapes,
geometric drawings,
Java API,
cross-platform drawing,
Drawing API for Windows,
Drawing API for Linux]
---

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
    margin: 0 auto 5px;
	display: flex;
    flex-direction: row;
    justify-content: space-around;

   }
</style>

## Cross-Platform Drawing API for Java

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The Aspse.Drawing library offers a cross-platform Java API for crafting geometric drawings. With Aspose.Drawing, you can effortlessly sketch vector images like lines, shapes, rectangles, polygons, arcs, Bezier curves, and text with diverse fonts and styles. Moreover, you can implement various transformations to 2D objects and preserve the outcomes as raster or vector files. The same Aspose library serves as a drawing API for Windows, Linux or MacOS, ensuring consistent quality and performance across all targeted platforms where Java is available.
</p>

### How to Draw Lines and Shapes in Java

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
In this example, we demonstrate how to create a series of graphic primitives, including lines, rectangles, and ellipses, using the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawPath-com.aspose.drawing.Pen-com.aspose.drawing.drawing2d.GraphicsPath-">`DrawPath` method</a>. To start, we create a bitmap with a size of `1000x800` pixels and a color depth of 32 bits per pixel. Next, we define a Pen object with two properties: the color set to `Blue` and a width of 2 pixels, which will be used for drawing the images, along with a <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing.drawing2d/graphicspath/">`GraphicPath` object</a>. Following that, we sequentially add two lines to the Path, each defined by its starting and ending X, Y coordinates: one from (100, 100) to (1000, 400), and another line from (1000, 600) to (300, 600); a Rectangle with the following specifications: left upper corner at (500, 350), width of 200, and height of 400 pixels; and an Ellipse object fitted within a rectangle, positioned at the left upper corner (10, 250), with a width of 450 and a height of 300 pixels. Using the `DrawPath` method and the previously described Pen object, we draw the Path onto the created bitmap. Finally, we rasterize the image and save it as a PNG file.
</p>

Java code example to draw a path:

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-LinesCurvesShapes-DrawPath-DrawPath.java" >}}

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The Java code above will draw the following image with Lines, Rectangles and Ellipses:
</p>

<figure class="frame">
<img class="marginauto" src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/LinesCurvesShapes/DrawPath.png" alt="Draw Line Rectangle Ellipse Path " width="1000" height="800"/>
<figcaption>Example of drawing lines, rectangles and ellipses</figcaption>
</figure>


### How to Create Geometric Drawings with Arcs and Bezier Curves

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Similar to the previous example of 2D geometrics drawings, to draw an arc, we begin by creating a 1000x800 bitmap and then proceed to create a Pen object with the color `Blue` and a width of `2` px. Next, we create an arc object with <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawArc-com.aspose.drawing.Pen-float-float-float-float-float-float-">method `DrawArc`</a>. As method parameters, we pass the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/pen/">object `Pen`</a> followed by rectangle coordinates where our arc will be fitted: upper left point (0, 0) and bottom right point (700, 700). The last two parameters are begin and end angles to draw the arc: from 0 degrees to 180 degrees. Angle in degrees measured clockwise from the x-axis to the starting point of the arc.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The Java code example to draw an arc:
</p>

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-LinesCurvesShapes-DrawArc-DrawArc.java" >}}

<figure class="frame">
<img class="marginauto" src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/LinesCurvesShapes/DrawArc.png" alt="Draw Arc with Aspose.Drawing" width="1000" height="800"/>
<figcaption>Example of drawing arc</figcaption>
</figure>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
To draw a Bezier curve, you need to utilize the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawBezier-com.aspose.drawing.Pen-com.aspose.drawing.PointF-com.aspose.drawing.PointF-com.aspose.drawing.PointF-com.aspose.drawing.PointF-">`DrawBezier` method</a>. This method takes a Pen object and four sets of coordinates representing Point objects, which are used to define the curve. The first point represents the starting point for drawing, followed by the first control point, the second control point, and finally, the ending point of the curve. The Aspose.Drawing graphic library automatically calculates and draws the Bezier curve from the starting point to the endpoint, taking into account the curve direction based on the control points.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The Java code example to draw a Bezier curve:
</p>

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-LinesCurvesShapes-DrawBezierSpline-DrawBezierSpline.java" >}}

<figure class="frame">
<img class="marginauto" src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/LinesCurvesShapes/DrawBezierSpline.png" alt="Draw Bezier spline curve with Aspose.Drawing" width="1000" height="800"/>
<figcaption>Example of drawing Bezier spline curve</figcaption>
</figure>


### How to Render Text

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Let's try a more intricate example with text drawing. We will render a text with anti-aliasing and clip it within an elliptical area. To begin, we create a graphics object using a bitmap with dimensions 1000x800 px, and then set the `TextRenderingHint` graphics property to `AntiAliasGridFit`. Next, we create a `GraphicsPath` object representing an ellipse fitted to the rectangle with coordinates from (200, 200) to (600, 400). We then clip an ellipse area that fits within the rectangle. Afterward, we create a `StringFormat` object, a `Brush` object, set the alignment, and select an appropriate font with the desired size and style. Finally, we use the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawString-java.lang.String-com.aspose.drawing.Font-com.aspose.drawing.Brush-com.aspose.drawing.RectangleF-com.aspose.drawing.StringFormat-">`DrawString` method</a> to create a text string with the clipped ellipse area.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The Java code example to draw a text string:
</p>

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-Rendering-Clipping-Clipping.java" >}}

<figure class="frame">
<img class="marginauto" src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/Rendering/Clipping.png" alt="Draw text string and clipping with Aspose.Drawing" width="1000" height="800"/>
<figcaption>Example of drawing text string with clipping</figcaption>
</figure>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Utilizing the Java API of the Aspose.Drawing graphics library allows you to create geometric drawings of any level of complexity, providing the flexibility to develop cross-platform applications with consistently excellent results.
</p>

For more examples please visit Aspose's official GitHub repository: <a href="https://github.com/aspose-drawing/Aspose.Drawing-for-Java">Aspose.Drawing for Java</a>.
