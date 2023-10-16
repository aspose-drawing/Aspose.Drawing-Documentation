---
title: "Working with Text and Fonts"
type: docs
url: /net/working-with-text-and-fonts/
keywords: "C# Draw Text, Draw Text on image C#, Add Text to image C#"
description: "Add text to an image using C#. Draw text on an image using C# and VB.NET. Draw with different fonts using C#."
weight: 70
---

Working with text and fonts using C# is easy with Aspose.Drawing for .NET. You can combine fonts and text styles to draw text during graphics drawing. This article shows how to:

- Format Text
- Draw Text
- Get Existing Fonts
- Use Text Hinting
## **Draw Text**
In order to draw text using C#, the following steps can be used.

1. Instantiate a Bitmap object
1. Instantiate a Graphics object with the bitmap object
1. Initialize a brush
1. Use the DrawString method to draw text on the bitmap

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-TextFonts-DrawText-DrawText.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/TextFonts/DrawText_out.png" alt="Draw text" width="500" />

## **Format Text**
In order to format text using C#, the following steps can be used.

1. Instantiate a Bitmap object
1. Instantiate a Graphics object with the bitmap object
1. Define the necessary string format parameters such as string alignment and line alignment
1. Use the DrawString method to draw formatted text

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-TextFonts-FormatText-FormatText.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/TextFonts/FormatText_out.png" alt="Format text" width="500" />

## **Text Hinting**
Text hinting mode can be specified using the API. The following C# code shows how to set the grid fitting mode.

1. Instantiate a Bitmap object
1. Instantiate a Graphics object with the bitmap object
1. Use the TextRenderingHint property of the Graphics object to specify the hinting mode
1. Use the DrawText method to draw text with the defined mode

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-TextFonts-Hinting-Hinting.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/TextFonts/Hinting_out.png" alt="Text hinting" />

## **Installed Fonts**


{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-TextFonts-InstalledFonts-InstalledFonts.cs" >}}

<img src="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/raw/master/Examples/Data/TextFonts/InstalledFonts_out.png" alt="Installed fonts" width="500" />