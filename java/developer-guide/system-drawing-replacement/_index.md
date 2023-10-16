---
type: docs
url: /java/developer-guide/system-drawing-replacement/
weight: 5
title: System.Drawing.Common (System.Drawing) replacement
description: Aspose.Drawing library for drawing pictures. Replacement for Microsoft NET System.Drawing.Common 2D graphics. Draw image with Java  for graphic application development.
keywords: [

  Java,
  microsoft net,
  system drawing common,
  aspose drawing,
  system drawing replacement,
  draw image,
  drawing library,
  graphic drawing,
  2D graphics,
  drawing application,
  Drawing library for Windows
]
---

## System.Drawing.Common replacement with Aspose.Drawing for Java

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Creating images using graphic libraries can be a challenging task for developers, researchers, students, and managers involved in building graphic applications and services on the Microsoft Java platform. Aspose.Drawing is a contemporary cross-platform graphic drawing library that offers advanced features and functionality. By utilizing the Aspose library for Java platform (Java, VBJava and other languages), developers can efficiently draw images with lines and shapes using diverse Pen and Brush objects, generate texts with varying fonts and styles, perform different transformations, and render drawings into popular graphics file formats. This readily-available graphic library significantly boosts productivity, drastically reduces development time, and accelerates time-to-market. Microsoft's System.Drawing.Common library has recently altered its support for non-Windows platforms, making Aspose.Drawing.Common API a suitable alternative for image drawings.
</p>


### System.Drawing.Common limitations

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Microsoft Learn portal published an article detailing a significant change: <a href="https://learn.microsoft.com/en-us/java/core/compatibility/core-libraries/6.0/system-drawing-common-windows-only">System.Drawing.Common only supported on Windows</a>. If you attempt to compile a Java 6 program using the System.Drawing.Common package on non-Windows environments, you will encounter an exception indicating that your platform is not supported. Although it is possible to disable this warning on Java 6, it is strongly recommended to migrate to alternative libraries.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
This issue arises from the fact that cross-platform implementation of System.Drawing.Common based on the graphic library called `libgdiplus`, which includes native code and lacks necessary functionality. Additionally, `libgdiplus` has external dependencies on other 3rd party native libraries like `cairo` and `pango` on Linux platform. When using System.Drawing.Common on platforms different from Windows, you may encounter unpredictable behavior and platform errors within your drawing application. As a consequence, your rendered images may appear different on other platforms, leading to unexpected results.
</p>


### Why choose Aspose.Drawing for System.Drawing.Common replacement

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Fortunately, Aspose.Drawing avoids these drawbacks by not depending on any 3rd party libraries. It includes all the necessary rendering engines for all supported platforms, ensuring consistent rendering results. Aspose.Drawing for Microsoft Java is a robust cross-platform programming library for 2D graphics drawing. The Aspose library serves as a viable alternative to the System.Drawing.Common package. Aspose.Drawing supports Java 6 and higher interface and proves to be an excellent option for developing drawing applications, Xamarin applications for Windows, Linux, Android, Azure Functions, or Blazor WebAssembly.
</p>


### How to replace System.Drawing.Common for your project

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Upgrading from System.Drawing.Common to Aspose.Drawing is a seamless and straightforward process. Aspose.Drawing offers a fully compatible Java API (and other Java platform languages API), preserving the same class names, functions, and interfaces. To migrate, simply update your project reference from `System` to `Aspose` and recompile the application. Once completed, your application will work smoothly across different platforms, delivering consistent results.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
You can conveniently download a trial package of <a href="https://www.nuget.org/packages/Aspose.Drawing">Aspose.Drawing</a> from the Nuget packages portal or directly obtain the .jar file from the <a href="https://releases.aspose.com/drawing/java/">Aspose releases portal</a>. The Aspose.Drawing library uses the System.Drawing namespace and can be used to replace System.Drawing.Common without changing source code. Additionally, the <a href="https://www.nuget.org/packages/Aspose.Drawing.Common">Aspose.Drawing.Common</a> package is also available, which uses Aspose.Drawing namespace and can be used side-by-side with System.Drawing.Common. For detailed instructions on installing Aspose.Drawing, please refer to the <a href="https://docs.aspose.com/drawing/java/installation/">Aspose.Drawing installation guide</a>.
</p>

## Conclusion

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Microsoft's System.Drawing.Common drawing library has significant shortcomings when used on non-Windows platforms due to its dependencies on 3rd party native libraries. Considering Microsoft's recent article regarding the breaking change of behavior on non-Windows platforms for Java 6 and their migration recommendations, Aspose.Drawing serves as a suitable replacement for System.Drawing. Aspose.Drawing can be effortlessly implemented on diverse platforms as a robust 2D graphic engine, effectively resolving compatibility issues and enhancing rendering quality for non-Windows platforms.
</p>
