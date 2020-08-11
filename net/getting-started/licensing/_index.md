---
title: "Licensing"
type: docs
url: /net/licensing/
keywords: "license, licensing, metered license"
description: "Learn more about licensing of Aspose.Drawing, types of licenses, apply the license."
weight: 60
---

## **Evaluation Version Limitations**
Customers can test the API thoroughly before making a final decision to buy it. However, the API has certain evaluation limitations if you will use it without a license. These limitations include:

- The limit of drawing operations is limited to 100 and an exception will be thrown after that
- A watermark is embedded in output image when user saves the image
## **Apply License using File or Stream Object**
The license can be loaded from a file or stream object. The easiest way to set a license is to put the license file in the same folder as the Aspose.Drawing.dll file and specify the file name, without a path, as shown in the example below.

{{% alert color="primary" %}} 

If you use are using any other Aspose for .NET component along with Aspose.Drawing for .NET, please specify the namespace for License like Aspose.Drawing.License.

{{% /alert %}} 
### **Loading a License from File**
The easiest way to apply a license is to put the license file in the same folder as the Aspose.Drawing.dll file and specify just the file name without a path.

{{% alert color="primary" %}} 

When you call the SetLicense method, the license name that you pass should be that of your license file. For example, if you change the license file name to "Aspose.Drawing.lic.xml" pass that file name to the Drawing.SetLicense(…) method.

{{% /alert %}} 




{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-Licensing-Licensing-LoadLicenseFromFile.cs" >}}
### **Loading a License from a Stream Object**
The following example shows how to load a license from a stream.

{{< gist "aspose-com-gists" "b8960f80422422251405395636eab772" "Examples-CSharp-Licensing-Licensing-LoadLicenseFromStream.cs" >}}
