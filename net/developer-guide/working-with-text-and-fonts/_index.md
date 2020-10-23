---
title: "Working with Text and Fonts"
type: docs
url: /net/working-with-text-and-fonts/
keywords: "C# Draw Text, Draw Text on Photo C#, Add Text to photo C#"
description: "Add text to a photo using C#. Draw text on a photo using C# and VB.NET. Draw with different fonts using C#."
weight: 70
---

Working with text and fonts using C# is easy with Aspose.Drawing for .NET. You can format fonts and text styles to draw text during graphics drawing. This article shows how to:

- Format Text
- Draw Text
- Get Existing Fonts
- Use Text Styling
## **Draw Text**
In order to draw text using C#, the following steps can be used.

1. Instantiate a Bitmap object
1. Instantiate a Graphics object with the bitmap object
1. Initialize a brush
1. Use the DrawString method to draw text on the bitmap

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-TextFonts-DrawText-DrawText.cs" >}}
## **Format Text**
In order to format text using C#, the following steps can be used.

1. Instantiate a Bitmap object
1. Instantiate a Graphics object with the bitmap object
1. Define the necessary string alignment parameters such as string alignment and line alignment
1. Use the DrawString method to draw formatted text

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-TextFonts-FormatText-FormatText.cs" >}}
## **Text Hinting**
Text hinting mode can be specified using the API. The following C# code shows how to set the grid fitting mode.

1. Instantiate a Bitmap object
1. Instantiate a Graphics object with the bitmap object
1. Use the TextRenderingHint property of the Graphics object to specify the hinting mode
1. Use the DrawText method to draw text with the defined mode

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-TextFonts-Hinting-Hinting.cs" >}}

The following helper function is used for drawing text.

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-TextFonts-Hinting-HintingDrawText.cs" >}}
## **Installed Fonts**


{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-TextFonts-InstalledFonts-InstalledFonts.cs" >}}
