---
title: "Hello World Example"
type: docs
url: /java/hello-world-example/
keywords: "Java API, Java create Arc, Java Vector Graphics, create bitmap, draw arc, Graphic library"
description: "Java Hello World example to draw an Arc. Java code sample to work with vector graphics in Java."
weight: 70
---

## **Hello World Example**

This "Hello World" example demonstrates the drawing capabilities of the Aspose.Drawing for Java API through a basic vector graphics creation.

The Aspose.Drawing Graphic Library for Java is a comprehensive tool for image manipulation and vector drawing. It facilitates the creation of vector graphics primitives like lines, curves, and figures by defining sets of points on a coordinate system. Additionally, it allows the display of text in various fonts, sizes, and styles, and provides the capability to save drawing results in popular graphics file formats. The subsequent example illustrates the process of drawing an arc in Java through the following steps.

1. Create an object of `Bitmap` class with the size of 1000x800 pixels.
1. Create an object of `Graphics` class from this bitmap.
1. Define a `Pen` object with parameters: color `Blue` and pen size of 2 pixels.
1. Use the `drawArc()` method of `Graphics` class object to Draw an Arc.

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-LinesCurvesShapes-DrawArc-DrawArc.java" >}}

The resulting Arc image is saved to the PNG file:

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
</style>

<figure class="frame"><p>
    <img class="marginauto" src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/LinesCurvesShapes/DrawArc.png" alt="Drawing Arc with Java" width="1000" height="800"/>
<figcaption>Example of drawing Arc with Java</figcaption>
</p></figure>
