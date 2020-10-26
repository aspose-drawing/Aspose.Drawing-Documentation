---
title: "Working with Pens"
type: docs
url: /net/working-with-pens/
keywords: "C# Draw Graphics, Change Graphics Pen color C#, Pen Width Draw Graphics C#"
description: "Learn about how to draw with pen in C#. .NET code to set pen width and color in C# and VB.NET."
weight: 30
---

Aspose.Drawing for .NET API provides the capability to draw graphics elements. Pens are one of the key elements of working with graphics and are used to draw different line objects such as an ellipse, circle, etc with the specified color.
## **Set Pen Width to Draw Graphics**
To draw graphics with a certain pen width, the following steps can be used.

1. Create an object of the Bitmap class
1. Initialize the Graphics object from the created bitmap
1. Create a new Pen with the desired width
1. Use the DrawLine method to draw a line with the desired width
1. Save the output to any desired output image format

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-Pens-Width-Width.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/Pens/Width_out.png" alt="Pen width" width="500" />

## **Set Pen Color to Draw Graphics**
To draw graphics with a certain pen color, the following steps can be used.

1. Create an object of the Bitmap class
1. Initialize the Graphics object from the bitmap
1. Create a new Pen with the desired color
1. Use the DrawLine method to draw a line
1. Save the output to any desired output image format

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-Pens-Colors-Colors.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/Pens/Colors_out.png" alt="Pen color" width="500" />

## **Join Lines**
Multiple lines can be joined to create a path. To join lines using C#, the following steps can be used.

1. Create an object of the Bitmap class
1. Initialize the Graphics object from the bitmap
1. Create a GraphicsPath object to establish a path
1. Use the LineJoin to join lines

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-Pens-Join-Join.cs" >}}

The following method is called by above code sample to draw path using Pen.

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-Pens-Join-PenJoinDrawPath.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/Pens/Join_out.png" alt="Join lines" width="500" />