---
title: "Working with Vector Graphics"
type: docs
url: /net/working-with-vector-graphics/
keywords: "C# Draw Bezier Curves, C# Cardinal Spline, Draw Arc C#, Vector Graphics C#"
description: "Draw Bezier Curves in C#. Draw Cardinal Spline using C#. Draw Arc, Ellipse, Path, Polygon in C# and VB.NET."
weight: 20
---

Aspose.Drawing for .NET makes it easy for you to draw vector graphics using C#. The API lets you work with a variety of different vector graphics such as arcs, Bezier spline, Cardinal Spline, closed curves, ellipses, lines and a  number of other types. This article contains C# examples for drawing different types of vector graphics using the API.
## **Draw Arc**
To drawn an arc using C#,

1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawArc method of Graphics class object to draw an arc

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawArc-DrawArc.cs" >}}

![Draw Arc result](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawArc_out.png)

## **Draw Bezier Spline**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawBezier method of Graphics class object to draw Bezier Spline

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawBezierSpline-DrawBezierSpline.cs" >}}

![Draw Bezier Spline result](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawBezierSpline_out.png)

## **Draw Cardinal Spline**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawCurve method of Graphics class object to draw Cardinal Spline

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawCardinalSpline-DrawCardinalSpline.cs" >}}

![Draw Cardinal Spline result](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawCardinalSpline_out.png)

## **Draw Closed Curve**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawClosedCurve method of Graphics class object to draw closed curve

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawClosedCurve-DrawClosedCurve.cs" >}}

![Draw Closed Curve result](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawClosedCurve_out.png)

## **Draw Ellipse**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawEllipse method of Graphics class object to draw Ellipse

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawEllipse-DrawEllipse.cs" >}}

![Draw Ellipse result](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawEllipse_out.png)

## **Draw Lines**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawLine method of Graphics class object to draw lines

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawLines-DrawLines.cs" >}}

![Draw Lines result](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawLines_out.png)

## **Draw Path**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Initialize a new object of GraphicsPath class and add Lines to its path collection



{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawPath-DrawPath.cs" >}}

![Draw Path result](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawPath_out.png)


## **Draw Polygon**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawPolygon method of Graphics class object to draw Polygon

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawPolygon-DrawPolygon.cs" >}}

![Draw Polygon result](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawPolygon_out.png)

## **Draw Rectangle**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawRectangle method of Graphics class object to draw Rectange

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawRectangle-DrawRectangle.cs" >}}

![Draw Rectangle result](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawRectangle_out.png)

## **Fill Region**
1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Instantiate a GraphicsPath class object
1. Add polygon to the Path collection of GraphicsPath class object
1. Use the FillRegion method of Graphics class to fill defined regions

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-FillRegion-FillRegion.cs" >}}

![Fill Region result](https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/FillRegion_out.png)
