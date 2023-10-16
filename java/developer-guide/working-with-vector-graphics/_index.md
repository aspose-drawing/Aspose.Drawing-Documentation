---
title: Working with Vector Graphics in C#
linktitle: "Working with Vector Graphics"
type: docs
url: /net/working-with-vector-graphics/
weight: 20
keywords: C# .Net Drawing, Draw Arc in C#, Draw Bezier Spline in C#, Draw Cardinal Spline in C#, Draw Closed Curve in C#, Draw Ellipse in C#, Draw Lines in C#, Draw Path in C#, Draw Polygon in C#, Draw Rectangle in C#, Fill Region in C#
description: Draw Arc, Bezier Spline, Cardinal Spline, Closed Curve, Ellipse, Lines, Path, Polygon, Rectangle and Fill Region in C# or .NET
---

Aspose.Drawing for .NET makes it easy for you to draw vector graphics using C#. The API lets you work with a variety of different vector graphics such as arcs, Bezier spline, Cardinal Spline, closed curves, ellipses, lines and a  number of other types. This article contains C# examples for drawing different types of vector graphics using the API.
## **Draw Arc in C#**
To drawn an arc using C#:

1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawArc method of Graphics class object to draw an arc

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawArc-DrawArc.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawArc_out.png" alt="Draw Arc" width="500"/>

## **Draw Bezier Spline in C#**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawBezier method of Graphics class object to draw Bezier Spline

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawBezierSpline-DrawBezierSpline.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawBezierSpline_out.png" alt="Draw Bezier Spline" width="500"/>

## **Draw Cardinal Spline in C#**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawCurve method of Graphics class object to draw Cardinal Spline

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawCardinalSpline-DrawCardinalSpline.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawCardinalSpline_out.png" alt="Draw Cardinal Spline" width="500"/>

## **Draw Closed Curve in C#**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawClosedCurve method of Graphics class object to draw closed curve

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawClosedCurve-DrawClosedCurve.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawClosedCurve_out.png" alt="Draw Closed Curve" width="500"/>

## **Draw Ellipse in C#**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawEllipse method of Graphics class object to draw Ellipse

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawEllipse-DrawEllipse.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawEllipse_out.png" alt="Draw Ellipse" width="500"/>

## **Draw Lines in C#**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawLine method of Graphics class object to draw lines

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawLines-DrawLines.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawLines_out.png" alt="Draw Lines" width="500"/>

## **Draw Path in C#**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Initialize a new object of GraphicsPath class and add Lines to its path collection



{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawPath-DrawPath.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawPath_out.png" alt="Draw Path" width="500"/>

## **Draw Polygon in C#**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawPolygon method of Graphics class object to draw Polygon

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawPolygon-DrawPolygon.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawPolygon_out.png" alt="Draw Polygon" width="500"/>

## **Draw Rectangle in C#**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawRectangle method of Graphics class object to draw Rectangle

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawRectangle-DrawRectangle.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawRectangle_out.png" alt="Draw Rectangle" width="500"/>

## **Fill Region in C#**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Instantiate a GraphicsPath class object
1. Add polygon to the Path collection of GraphicsPath class object
1. Use the FillRegion method of Graphics class to fill defined regions

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-FillRegion-FillRegion.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/FillRegion_out.png" alt="Fill Region" width="500"/>
