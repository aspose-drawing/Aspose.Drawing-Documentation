---
title: Create bitmap from scratch or load from file using Java
type: docs
url: /java/create-image-bitmap/
keywords: create image bitmap in Java, create graphics on bitmap using Java, draw graphics in Java, load existing image from file on bitmap using Java
description: Create image bitmap from scratch or load from file using Java API.
weight: 10
---

Whether you're creating a bitmap from scratch or loading one from an existing file, Aspose.Drawing for Java simplifies these common tasks, providing a seamless experience for bitmap creation and editing.

## **Create New Bitmap in Java**

Creating a new image from scratch is pretty straightforward with the Aspose.Drawing Java API. The ensuing Java code example demonstrates how to create a new bitmap and draw an Arc on it:

1. Create an instance of the `Bitmap` class.
2. Initialize an object of the `Graphics` class from this bitmap.
3. Define a `Pen` object with the desired parameters.
4. Utilize the `drawArc()` method of the `Graphics` class object to draw an Arc.

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-LinesCurvesShapes-DrawArc-DrawArc.java" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-Java/raw/master/Examples/Data/LinesCurvesShapes/DrawArc_out.png" alt="Draw Arc" width="500" />

## **Load existing Image from File into Bitmap**

Loading an existing image from a file and saving it back to disk using the Java API can be accomplished, as presented in the following Java code sample:

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-Images-LoadSave-LoadSave.java" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-Java/raw/master/Examples/Data/Images/LoadSave_out.png" alt="Load and save image" />
