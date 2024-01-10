---
title: "Working with Coordinate System Transformations"
type: docs
url: /java/working-with-coordinate-system-transformations/
description: "Change Coordinate System Transformations of image in Java."
keywords: Java Draw Graphics, coordinate system transformation, Global transformation, Local transformation, matrix transformation, page transformation, units of measure, World transformation
weight: 60
---

## **Global Transformation in Java**

To globally transform a scene in Java, follow these steps:

- Create an instance of the `Bitmap` class.
- Initialize a new object of the `Graphics` class with this bitmap object.
- Use the `rotateTransform()` method of the `Graphics` object to specify the rotation angle.
- Draw the shapes with global transformation.

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-CoordinateSystemsTransformations-GlobalTransformation-GlobalTransformation.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/CoordinateSystemsTransformations/GlobalTransformation_out.png" alt="Global Transformation" width="1000" />

## **Local Transformation of in Java**

To locally transform an object in Java, follow these steps:

- Create an instance of the `Bitmap` class.
- Initialize a new object of the `Graphics` class with this bitmap object.
- Create a shape such as `Ellipse`.
- Define a matrix with the desired transformation.
- Apply the matrix to the defined object.

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-CoordinateSystemsTransformations-LocalTransformation-LocalTransformation.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/CoordinateSystemsTransformations/LocalTransformation_out.png" alt="Local Transformation" width="1000" />

## **Matrix Transformation of a Path in Java**

To perform a matrix transformation on a path in Java, follow these steps:

- Create an instance of the `Bitmap` class.
- Initialize a new object of the `Graphics` class with this bitmap object.
- Create a shape such as a `Rectangle`.
- Define the Matrix Transformation using the `Matrix` class.
- Apply the transformation to a defined rectangle.

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-CoordinateSystemsTransformations-MatrixTransformations-MatrixTransformations.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/CoordinateSystemsTransformations/MatrixTransformations_out.png" alt="Matrix Transformation" width="1000" />

## **Page Transformation in Java**

To perform a page transformation of a scene in Java, follow these steps:

- Create an instance of the `Bitmap` class.
- Initialize a new object of the `Graphics` class with this bitmap object.
- Set the `GraphicsUnit` for the `Graphics` class object.
- Draw a shape such as a `Rectangle`.

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-CoordinateSystemsTransformations-PageTransformation-PageTransformation.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/CoordinateSystemsTransformations/PageTransformation_out.png" alt="Page Transformation" width="1000" />

## **Applying Different Units of Measurement in Java**

To apply different units of measurement to different objects in a scene in Java, follow these steps:

- Create an instance of the `Bitmap` class.
- Initialize a new object of the `Graphics` class with this bitmap object.
- Set the `pageUnit` for the `Graphics` class object.
- Draw shapes such as rectangles.

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-CoordinateSystemsTransformations-UnitsOfMeasure-UnitsOfMeasure.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/CoordinateSystemsTransformations/UnitsOfMeasure_out.png" alt="Units of Measure" width="1000" />

## **World Transformation in Java**

To apply world transformation in Java, follow these steps:

- Create an instance of the `Bitmap` class.
- Initialize a new object of the `Graphics` class with this bitmap object.
- Use the `translateTransform()` method to set the transformation.
- Draw a shape such as a rectangle.

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-CoordinateSystemsTransformations-WorldTransformation-WorldTransformation.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/CoordinateSystemsTransformations/WorldTransformation_out.png" alt="World Transformation" width="1000" />
