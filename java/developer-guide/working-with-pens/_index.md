---
title: "Working with Pens"
type: docs
url: /java/working-with-pens/
keywords: Java API, Java Draw Graphics, Change Graphics Pen color Java, Pen Width Draw Graphics Java, Join Lines in Java
description: "Learn about how to draw with pen in Java. Java code to set pen width and color using Java. Join Lines in Java."
weight: 30
---

Aspose.Drawing for Java API empowers you to create graphic elements. Pens play a crucial role in graphic operations, allowing you to draw various line objects like ellipses, circles, etc., with specified colors.

## **Set Pen Width to Draw Graphics in Java**

To draw graphics with a specific pen width, follow these steps:

1. Create an object of <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/bitmap/">`Bitmap` class</a>.
1. Initialize an object of <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/">`Graphics` class</a> from this bitmap
1. Define a <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/pen/">`Pen` object</a> with desired parameters
4. Utilize the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawLine-com.aspose.drawing.Pen-int-int-int-int-">`drawLine()` method</a> to draw a line with the specified width.
5. Save the output in any desired image format.

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-Pens-Width-Width.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/Pens/Width.png" alt="Pen width" width="1000" />

## **Set Pen Color to Draw Graphics in Java**

To draw graphics with a certain pen color, the following steps can be used.

1. Create an object of <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/bitmap/">`Bitmap` class</a>.
1. Initialize an object of <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/">`Graphics` class</a> from this bitmap
1. Define a <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/pen/">`Pen` object</a> with desired parameters
1. Use the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawLine-com.aspose.drawing.Pen-int-int-int-int-">`drawLine()` method</a> to draw a line
1. Save the output to any desired output image format

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-Pens-Colors-Colors.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/Pens/Colors.png" alt="Pen color" width="1000" />

## **Join Lines to Create Path in Java**

Multiple lines can be joined to create a path. To join lines using Java, the following steps can be used.

1. Create an object of <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/bitmap/">`Bitmap` class</a>.
1. Initialize an object of <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/">`Graphics` class</a> from this bitmap
1. Create a <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing.drawing2d/graphicspath/">`GraphicsPath` object</a> to establish a path
1. Use the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/pen/#setLineJoin-int-">`setLineJoin()` method</a> to join lines

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-Pens-Join-Join.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/Pens/Join.png" alt="Join lines" width="1000" />
