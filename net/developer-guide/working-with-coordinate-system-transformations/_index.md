---
title: "Working with Coordinate System Transformations"
type: docs
url: /net/working-with-coordinate-system-transformations/
description: "Change Coordinate System Transformations of image in C#."
weight: 60
---

## **Global Transformation**
For global transformation of a scene in C#, the following steps can be used.

1. Instantiate a new object of Bitmap class
1. Initialize a new object of Graphics class with this bitmap object
1. Use the RotateTransform method of Graphics object to specify the rotation angle
1. Draw the shapes with global transformation

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-GlobalTransformation-GlobalTransformation.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/CoordinateSystemsTransformations/GlobalTransformation_out.png" alt="Global Transformation" width="500" />

## **Local Transformation**
For local transformation of an object in C#, the following steps can be used.

1. Instantiate a new object of Bitmap class
1. Initialize a new object of Graphics class with this bitmap object
1. Create a shape such as Ellipse
1. Define a matrix with desired transformation
1. Apply the matrix to defined object

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-LocalTransformation-LocalTransformation.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/CoordinateSystemsTransformations/LocalTransformation_out.png" alt="Local Transformation" width="500" />

## **Matrix Transformation**
For Matrix transformation of a path in C#, the following steps can be used.

1. Instantiate a new object of Bitmap class
1. Initialize a new object of Graphics class with this bitmap object
1. Create a shape such as Rectangle
1. Define the Matrix Transformation using the Matrix class
1. Apply the transformation to defined rectangle

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-MatrixTransformations-MatrixTransformations.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/CoordinateSystemsTransformations/MatrixTransformations_out.png" alt="Matrix Transformation" width="500" />

## **Page Transformation**
For Page transformation of a scene in C#, the following steps can be used.

1. Instantiate a new object of Bitmap class
1. Initialize a new object of Graphics class with this bitmap object
1. Set the GraphicsUnit for the Graphics class object
1. Draw a shape such as Rectangle

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-PageTransformation-PageTransformation.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/CoordinateSystemsTransformations/PageTransformation_out.png" alt="Page Transformation" width="500" />

## **Units of Measure**
To apply different units of measurement to different objects of a scene in C#, the following steps can be used.

1. Instantiate a new object of Bitmap class
1. Initialize a new object of Graphics class with this bitmap object
1. Set the PageUnit for the Graphics class object
1. Draw the shapes such as Rectangles

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-UnitsOfMeasure-UnitsOfMeasure.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/CoordinateSystemsTransformations/UnitsOfMeasure_out.png" alt="Units of Measure" width="500" />

## **World Transformation**
For World Transformation, the following sample C# code can be used.

1. Instantiate a new object of Bitmap class
1. Initialize a new object of Graphics class with this bitmap object
1. Use the TranslateTransform method to set the transformation
1. Draw a shape such as Rectangle

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-WorldTransformation-WorldTransformation.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/CoordinateSystemsTransformations/WorldTransformation_out.png" alt="World Transformation" width="500" />
