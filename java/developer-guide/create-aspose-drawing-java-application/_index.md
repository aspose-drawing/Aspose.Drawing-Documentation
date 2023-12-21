---
title: "Creating Aspose.Drawing Java application"
type: docs
url: /java/create-aspose-drawing-java-application/
keywords: Java API, Java Draw Graphics, Graphics Java, Drawing Java application
description: "Learn how to use Aspose.Drawing graphic library for Java application."
weight: 9
---

You can use Aspose.Drawing library in a cross-platform Java applications to draw vector graphics, and text, and generate images as demonstrated in this tutorial.

{{% alert color="primary" %}}

Aspose.Drawing is a versatile and user-friendly API. This article guides you, step by step, through the process of setting up and creating your first Java application with Aspose.Drawing. Although the steps are demonstrated using MyEclipse, the procedures for other IDEs are analogous. The article includes a code example that generates your first simple drawing.

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
- Unzip the downloaded ZIP archive on your development computer, for example `D:\Java.Drawing-API`.

### Create Project

- Launch the MyEclipse IDE.
- In the main toolbar, click New Java Project, or, from the File menu, select New Java Project.
- Enter the project name.
- Click Finish.

### Add Reference of Aspose.Drawing for Java API

The project uses the Aspose.Drawing API as the core library for performing image operations. So, you have to reference the Aspose.Drawing JAR in the project.

1. Select the project’s properties menu (right-click on the project).

Right-clicking the project opens a menu. The Properties option can be found at the bottom.

2. Select the Java Build Path option.
3. Click **Add External Jar**.
4. Select the Aspose.Drawing file to add it to the project.

### Write MyClass.Java

The next step is to create a new class.

- Click on **New Java Class** in the main toolbar.
- If not already specified, select `HelloWorld/src` as the source folder.
- Type `MyClass` for the class name.
- Select the option to create the `main()` method.
- Click Finish.

The code below uses the Aspose.Drawing API to create a drawing from scratch.

Replace the **MyClasss.java** file with the following code that draws a gradient and saves an image:

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-NET6-Drawing.java" >}}

{{% alert color="primary" %}}

All coding is done in the main() method of the MyClass.java class.

{{% /alert %}}

## Run Java application

Start the project from IDE, in the project output directory the resulting **gradient.png** image file will be generated:

![Linear gradient drawn in Java](linear-gradient-in-java.png)
