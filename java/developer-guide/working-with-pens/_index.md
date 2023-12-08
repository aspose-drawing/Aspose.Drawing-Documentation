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

1. Create a Bitmap class object.
2. Initialize the Graphics object from the created bitmap.
3. Create a new Pen with the desired width.
4. Utilize the DrawLine method to draw a line with the specified width.
5. Save the output in any desired image format.

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-Pens-Width-Width.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-Java/raw/master/Examples/Data/Pens/Width_out.png" alt="Pen width" width="500" />

## **Set Pen Color to Draw Graphics in Java**

To draw graphics with a certain pen color, the following steps can be used.

1. Create an object of the Bitmap class
1. Initialize the Graphics object from the bitmap
1. Create a new Pen with the desired color
1. Use the DrawLine method to draw a line
1. Save the output to any desired output image format

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-Pens-Colors-Colors.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-Java/raw/master/Examples/Data/Pens/Colors_out.png" alt="Pen color" width="500" />

## **Join lines to create Path in Java**

Multiple lines can be joined to create a path. To join lines using Java, the following steps can be used.

1. Create an object of the Bitmap class
1. Initialize the Graphics object from the bitmap
1. Create a GraphicsPath object to establish a path
1. Use the LineJoin to join lines

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-Pens-Join-Join.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-Java/raw/master/Examples/Data/Pens/Join_out.png" alt="Join lines" width="500" />
