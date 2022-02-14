---
title: Create bitmap from scratch or load from file using C#
type: docs
url: /net/create-image/
keywords: create image from scratch in csharp, create graphics on bitmap using csharp, draw graphics in C#, load existing image from file on bitmap using C#.
description: Create bitmap from scratch or load from file using C# .NET API.
weight: 10
---

Creating bitmap from scratch or loading from file using C# is a common requirement. Aspose.Drawing for .NET lets you create a bitmap from scratch or open from an existing file that can further be edited. 
## **Create New Bitmap in C#**
Creating a new image from scratch is easy using Aspose.Drawing for .NET API. The following C# example shows how to create a new drawing and draw an arc on it.

1. Instantiate an object of Bitmap class
1. Initialize an object of Graphics class from this bitmap
1. Define a Pen object with desired parameters
1. Use the DrawArc method of Graphics class object to draw an arc

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-LinesCurvesShapes-DrawArc-DrawArc.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/LinesCurvesShapes/DrawArc_out.png" alt="Draw Arc" width="500" />

## **Load existing Image from File into Bitmap**
You can also load an existing image from file and save it back to disc using the API as shown in the following C# code sample.

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-Images-LoadSave-LoadSave.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/Images/LoadSave_out.png" alt="Load and save image" />
