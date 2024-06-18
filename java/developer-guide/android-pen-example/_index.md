---
title: "Using Aspose.Drawing for Java in Android application"
type: docs
url: /java/android-pen-example/
keywords: Java API, Java Draw Graphics, Graphics Java, Drawing Java application, Android
description: "Learn how to use Aspose.Drawing graphic library for Android application."
weight: 9
---
You can use Aspose.Drawing for Java library in Android applications to draw vector graphics, and text, and generate images as demonstrated in this tutorial.

{{% alert color="primary" %}}

Aspose.Drawing is a versatile and user-friendly API. This article guides you, step by step, through the process of setting up and creating your first Java application with Aspose.Drawing. Although the steps are demonstrated using IntelliJ IDEA, the procedures for other IDEs are analogous. The article includes a code example that generates your first simple drawing.

{{% /alert %}}

Upon installation, all Aspose components operate in evaluation mode. This mode, which doesn't have a time constraint, incorporates watermarks into the generated drawings.

## Creating an Application that Uses Aspose.Drawing

To work with Aspose.Drawing in your applications:

- Download Aspose.Drawing for Java.
- Create a project.
- Add a reference to the Aspose.Drawing API.
- Write the code.

### Download Aspose.Drawing for Java

- Download <a href="https://downloads.aspose.com/drawing/java">Aspose.Drawing for Java</a>.
- Unzip the downloaded ZIP archive on your development computer, for example, `c:\Users\User\AndroidApp\lib`.

### Create Project

- Launch the IDE.
- In the main toolbar click "New Project".
- Enter the project name and location.
- Click "Create" button.


### Add Reference of Aspose.Drawing for Java API

The project uses the Aspose.Drawing API as the core library for performing drawing operations. So, you have to reference the Aspose.Drawing JAR in the project.

1. Select the "Project Structure" menu (in the File menu):

2. Add Aspose.Drawing JAR in to dependencies implementation(files("libs/aspose-drawing-24.4.jar"))


### Write **MainActivity**

The next step is to create a new class.

The code below uses the Aspose.Drawing API to run a simple Pen test. Replace the **MainActivity** file with the following code:

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "AndroidPenTest.java" >}}

{{% alert color="primary" %}}

All coding is done in the `main()` method of the class `Main`.

{{% /alert %}}

## Run Android application

Connect to your Android device and start the project from IDE by pressing the "Run" button on the toolbar. Simple test should be success.


