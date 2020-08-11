---
title: "Working with Coordinate System Transformations"
type: docs
url: /net/working-with-coordinate-system-transformations/
description: "Change Coordinate System Transformations of image in C#."
weight: 60
---

## **Global Transformation**
For global transformation of an image in C#, the following steps can be used.

1. Instantiate a new object of Bitmap class
1. Initialize a new object of Graphics class with this bitmap object
1. Use the RotateTransform method of Graphics object to specify the rotation angle
1. Draw the shapes to have global transformation

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-GlobalTransformation-GlobalTransformation.cs" >}}
## **Local Transformation**
` `For local transformation of an image in C#, the following steps can be used.

1. Instantiate a new object of Bitmap class
1. Initialize a new object of Graphics class with this bitmap object
1. Draw the shapes such as Ellipse
1. Define a matrix with desired transformation
1. Apply the matrix to defined object

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-LocalTransformation-LocalTransformation.cs" >}}
## **Matrix Transformation**
` `For Matrix transformation of an image in C#, the following steps can be used.

1. Instantiate a new object of Bitmap class
1. Initialize a new object of Graphics class with this bitmap object
1. Draw the shapes such as rectangle
1. Define the Matrix Transformation using the Matrix class
1. Apply the transformation to defined rectangle

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-MatrixTransformations-MatrixTransformations.cs" >}}

The following helping method is called by above code sample.

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-MatrixTransformations-MatrixTransformationsTransformPath.cs" >}}
## **Page Transformation**
For Page transformation of an image in C#, the following steps can be used.

1. Instantiate a new object of Bitmap class
1. Initialize a new object of Graphics class with this bitmap object
1. Set the GraphicsUnit for the Graphics class object
1. Draw the shapes such as Ellipse

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-PageTransformation-PageTransformation.cs" >}}
## **Units of Measure**
To apply different units of measurement to different objects of an image in C#, the following steps can be used.

1. Instantiate a new object of Bitmap class
1. Initialize a new object of Graphics class with this bitmap object
1. Set the GraphicsUnit for the Graphics class object
1. Draw the shapes such as Ellipse

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-UnitsOfMeasure-UnitsOfMeasure.cs" >}}
## **World Transformation**
For World Transformation, the following sample C# code can be used.

1. Instantiate a new object of Bitmap class
1. Initialize a new object of Graphics class with this bitmap object
1. Use the TranslateTransform method to set the transformation
1. Draw the shapes such as rectangle

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-CoordinateSystemsTransformations-WorldTransformation-WorldTransformation.cs" >}}
