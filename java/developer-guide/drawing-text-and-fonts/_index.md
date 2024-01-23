---
title: "Drawing Text and Fonts with Java"
type: docs
url: /java/drawing-text-and-fonts/
keywords: Java Draw Text, Draw Text on image Java, Add Text to image Java, format text, text hinting, get installed fonts
description: "Add text to image using Aspose.Drawirng for Java. Draw text on image using Java API. Draw with different fonts using Java API."
weight: 70
---

Working with text and fonts using Java is simplified with Aspose.Drawing for Java. You can effortlessly combine fonts and text styles to draw text during graphics drawing. This article guides you on:

- Drawing Text
- Formatting Text
- Text Hinting
- Retrieving Existing Fonts

## **Draw Text in Java**

Below are the steps to draw text:

- Create an instance of the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/bitmap/">`Bitmap` class</a>.
- Initialize a new object of the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/">`Graphics` class</a> with the bitmap object.
- Set up a <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/brush/">`Brush` object</a> for text drawing.
- Employ the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawString-java.lang.String-com.aspose.drawing.Font-com.aspose.drawing.Brush-com.aspose.drawing.RectangleF-">`drawString()` method</a> to draw text on the bitmap.

These simple steps empower you to effortlessly integrate text into your graphics using Aspose.Drawing for Java.

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-TextFonts-DrawText-DrawText.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/TextFonts/DrawText.png" alt="Draw text" width="1000" />

## **Format Text in Java**

Formatting text adds a layer of sophistication to your Java graphics, and with Aspose.Drawing for Java, it's a straightforward process. Here's how you can format text:

- Begin by creating a <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/bitmap/">`Bitmap` object</a>.
- Initialize a new <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/">`Graphics` object</a> using the created bitmap object.
- Specify the necessary string format parameters, such as string alignment and line alignment, to achieve the desired formatting.
- Utilize the <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/#drawString-java.lang.String-com.aspose.drawing.Font-com.aspose.drawing.Brush-com.aspose.drawing.RectangleF-">`drawString()` method</a> to effortlessly draw formatted text on the bitmap.

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-TextFonts-FormatText-FormatText.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/TextFonts/FormatText.png" alt="Format text" width="1000" />

## **Text Hinting in Java**

Text hinting mode is a crucial aspect of text rendering, and with Aspose.Drawing for Java, you have the flexibility to control it. Steps to Set Text Hinting Mode:

- Start by creating a <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/bitmap/">`Bitmap` object</a>.
- Initialize a new <a href="https://reference.aspose.com/drawing/java/com.aspose.drawing/graphics/">`Graphics` object</a> using the created bitmap object.
- Utilize the `TextRenderingHint` property of the `Graphics` object to specify the desired hinting mode.
- Finally, employ the `drawText` function to draw text with the specified hinting mode.

By following these steps, you can precisely control the text hinting mode to achieve optimal text rendering using Aspose.Drawing for Java.

Text hinting mode can be specified using the API. The following Java code shows how to set the grid fitting mode.

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-TextFonts-Hinting-Hinting.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/TextFonts/Hinting.png" alt="Text hinting" width="1000"/>

## **Installed Fonts in Java**

Retrieving Existing Fonts in Java:

{{< gist "aspose-com-gists" "3562c2fe053aae0bda46f32abae6062a" "Examples-JAVA-TextFonts-InstalledFonts-InstalledFonts.java" >}}

<img src="https://raw.githubusercontent.com/aspose-drawing/Aspose.Drawing-for-Java/main/Examples/Data/TextFonts/InstalledFonts.png" alt="Installed fonts" width="1000" />
