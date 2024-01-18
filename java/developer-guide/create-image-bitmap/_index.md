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
    <img class="marginauto" src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/LinesCurvesShapes/DrawArc.png" alt="Draw arc in bitmap in Java" width="1000" height="800"/>
<figcaption>Draw arc graphics on bitmap in Java</figcaption>
</p></figure>

## **Load existing Image from File into Bitmap**

Loading an existing image from a file and saving it back to disk using the Java API can be accomplished, as presented in the following Java code sample:

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-Images-LoadSave-LoadSave.java" >}}

<figure class="frame"><p>
    <img class="marginauto" src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/LoadSave_out.png" alt="Load and save image bitmap in Java" width="195" height="55"/>
<figcaption>Load and save image bitmap in Java</figcaption>
</p></figure>
