---
title: "Using Aspose.Drawing in Blazor WebAssembly App"
type: docs
url: /net/using-aspose-drawing-in-blazor-webassembly-app/
keywords: "Blazor, Blazor WebAssembly, C# Draw Graphics, Graphics C#"
description: "Learn how to use Aspose.Drawing in Blazor WebAssembly application with C#."
weight: 40
---

Blazor can run your client-side C# code directly in the browser, using WebAssembly. Blazor works in all modern web browsers, including mobile browsers.

You can use Aspose.Drawing in your Blazor WebAssembly app to draw vector graphics, text, and generate images as demonstrated in this tutorial.

## 1. Create a C# Blazor WebAssembly App project.

In Visual Studio, create a new C# **Blazor App** - **Blazor WebAssembly App** project, selecting **.NET 5.0** and **ASP.NET Core hosted** options:

![Blazor WebAssembly App project settings](blazor-webassembly-app-project-settings.png)

## 2. Add the Aspose.Drawing package to the BlazorApp1.Client project dependencies.

![Installing Aspose.Drawing from NuGet](../installation/installation_1.png)

## 3. Add image drawing code.

Replace the **Pages\Index.razor** file with the following code that draws a gradient and creates an image.

```csharp
@page "/"
@using System.Drawing;
@using System.Drawing.Drawing2D;
@using System.Drawing.Imaging;
@using System.IO;

<img src="@imageSrc" />

@code {
    private string imageSrc;

    public Index()
    {
        imageSrc = "data:image/png;base64, " + Convert.ToBase64String(Draw(ImageFormat.Png).ToArray());
    }

    static MemoryStream Draw(ImageFormat format)
    {
        Bitmap bitmap = new Bitmap(1000, 800, PixelFormat.Format32bppPArgb);
        Graphics graphics = Graphics.FromImage(bitmap);
        graphics.SmoothingMode = SmoothingMode.AntiAlias;

        Brush brush = new LinearGradientBrush(new Point(0, 0), new Point(1000, 800), Color.Red, Color.Blue);
        graphics.FillEllipse(brush, 100, 100, 800, 600);

        MemoryStream result = new MemoryStream();
        bitmap.Save(result, format);
        result.Seek(0, SeekOrigin.Begin);
        return result;
    }
}
```

## 4. Add an Aspose.Drawing license file.

Copy your **Aspose.Drawing.NET.lic** file with Aspose.Drawing licensing information to the client project directory, open this file properties from Solution Explorer and set **Build Action** to **Embedded resource**.

## 5. Add license initialization code.

In the **Program.cs** file, add the following code to the beginning on the **Main** method:

```csharp
Aspose.Drawing.License license = new Aspose.Drawing.License();
license.SetLicense("BlazorApp1.Client.Aspose.Drawing.NET.lic");
```

## 6. Run the application.

Start the project from Visual Studio, the browser will display the gradient image created with Aspose.Drawing:

<img src="linear-gradient-in-blazor.png" alt="Linear gradient drawn in Blazor" width="900" />