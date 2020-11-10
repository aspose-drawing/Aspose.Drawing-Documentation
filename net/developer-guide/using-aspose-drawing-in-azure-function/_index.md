---
title: "Using Aspose.Drawing in Azure Function"
type: docs
url: /net/using-aspose-drawing-in-azure-function/
keywords: "Azure, Azure Function, C# Draw Graphics, Graphics C#"
description: "Learn how to use Aspose.Drawing in Azure Function with C#."
weight: 40
---

```csharp
using System.IO;
using System.Threading.Tasks;
using Microsoft.AspNetCore.Mvc;
using Microsoft.Azure.WebJobs;
using Microsoft.Azure.WebJobs.Extensions.Http;
using Microsoft.AspNetCore.Http;

using System.Drawing;
using System.Drawing.Drawing2D;
using System.Drawing.Imaging;

namespace AzureFunctionApp1
{
    public static class Function1
    {
        [FunctionName("Function1")]
        public static async Task<IActionResult> Run([HttpTrigger(AuthorizationLevel.Anonymous, "get", "post", Route = null)] HttpRequest req, ExecutionContext context)
        {
            Aspose.Drawing.License license = new Aspose.Drawing.License();
            license.SetLicense(Path.Combine(context.FunctionAppDirectory, "Aspose.Drawing.NET.lic"));

            return new FileStreamResult(Draw(ImageFormat.Png), "image/png");
        }

        static Stream Draw(ImageFormat format)
        {
            Bitmap bitmap = new Bitmap(1000, 800, PixelFormat.Format32bppPArgb);
            Graphics graphics = Graphics.FromImage(bitmap);

            Brush brush = new LinearGradientBrush(new Point(0, 0), new Point(1000, 800), Color.Red, Color.Blue);
            graphics.FillEllipse(brush, 100, 100, 800, 600);

            MemoryStream result = new MemoryStream();
            bitmap.Save(result, format);
            result.Seek(0, SeekOrigin.Begin);
            return result;
        }
    }
}
```

![Linear gradient drawn in Azure Function](linear-gradient-from-azure-function.png)