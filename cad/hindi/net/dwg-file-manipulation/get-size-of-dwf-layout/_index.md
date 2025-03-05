---
title: C# में DWG फ़ाइलों के साथ कार्य करना - DWF लेआउट का आकार प्राप्त करें
linktitle: C# में DWG फ़ाइलों के साथ कार्य करना - DWF लेआउट का आकार प्राप्त करें
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: DWG फ़ाइलों को संभालने में .NET के लिए Aspose.CAD की शक्ति का अन्वेषण करें। C# का उपयोग करके आसानी से DWF लेआउट आकार निकालना सीखें।
type: docs
weight: 10
url: /hi/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## परिचय

कंप्यूटर-एडेड डिज़ाइन (CAD) और .NET विकास के क्षेत्र में, Aspose.CAD DWG फ़ाइलों को संभालने के लिए एक शक्तिशाली उपकरण के रूप में खड़ा है। यह ट्यूटोरियल आपको C# में DWG फ़ाइलों के साथ काम करने और DWF लेआउट का आकार निकालने की प्रक्रिया में मार्गदर्शन करेगा। इससे पहले कि हम कोड में उतरें, आइए सुनिश्चित करें कि आपने इस यात्रा पर निकलने के लिए सब कुछ तैयार कर लिया है।

## आवश्यक शर्तें

इस ट्यूटोरियल का निर्बाध रूप से पालन करने के लिए, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास .NET के लिए Aspose.CAD स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[.NET डाउनलोड पेज के लिए Aspose.CAD](https://releases.aspose.com/cad/net/).

अब जब आपके पास आवश्यक उपकरण हैं, तो आइए कोडिंग क्षेत्र में कूदें।

## नामस्थान आयात करें

इससे पहले कि हम कोड के साथ काम करना शुरू करें, आइए आवश्यक नामस्थान आयात करें:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

ये नेमस्पेस आपके C# एप्लिकेशन में Aspose.CAD के साथ CAD फ़ाइलों को संभालने के लिए आवश्यक कक्षाएं और तरीके प्रदान करेंगे।

## चरण 1: अपना वातावरण स्थापित करें

यह सुनिश्चित करके शुरुआत करें कि आपके पास अपने प्रोजेक्ट के लिए सही वातावरण स्थापित है। अपने C# प्रोजेक्ट में Aspose.CAD लाइब्रेरी का संदर्भ लें।

## चरण 2: फ़ाइल पथ परिभाषित करें

अपनी DWG फ़ाइल के लिए पथ और जेनरेट की गई JPG फ़ाइलों के लिए आउटपुट निर्देशिका को परिभाषित करें:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## चरण 3: DWF छवि लोड करें

Aspose.CAD का उपयोग करके DWF छवि लोड करें:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // आगे के चरणों के लिए कोड यहां जाएगा
}
```

## चरण 4: पृष्ठों के माध्यम से पुनरावृति करें

DWF छवि के पृष्ठों के माध्यम से पुनरावृति करें:

```csharp
foreach (var page in image.Pages)
{
    // आगे के चरणों के लिए कोड यहां जाएगा
}
```

## चरण 5: लेआउट जानकारी प्राप्त करें

प्रत्येक पृष्ठ से लेआउट जानकारी प्राप्त करें:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## चरण 6: JPG विकल्प सेट करें

लेआउट को JPG फ़ाइल के रूप में सहेजने के लिए विकल्प सेट करें:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // आगे के चरणों के लिए कोड यहां जाएगा
}
```

## चरण 7: पृष्ठ का आकार निर्धारित करें

DWF लेआउट का आकार निर्धारित करें:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// आगे के चरणों के लिए कोड यहां जाएगा
```

## चरण 8: पृष्ठ आयाम सेट करें

इकाई प्रकार के आधार पर पृष्ठ आयाम सेट करें:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## चरण 9: JPG फ़ाइल सहेजें

निर्दिष्ट विकल्पों के साथ JPG फ़ाइल सहेजें:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

अब आपने C# में Aspose.CAD का उपयोग करके DWG फ़ाइल से DWF लेआउट का आकार सफलतापूर्वक निकाल लिया है। .NET विकास के लिए Aspose.CAD द्वारा प्रदान की जाने वाली अधिक सुविधाओं और कार्यात्मकताओं का पता लगाने के लिए स्वतंत्र महसूस करें।

## निष्कर्ष

इस ट्यूटोरियल में, हमने Aspose.CAD का उपयोग करके C# में DWG फ़ाइलों के साथ काम करने की प्रक्रिया के बारे में जाना है। इन चरणों का पालन करके, आप न केवल DWF लेआउट का आकार प्राप्त कर सकते हैं बल्कि अपने .NET प्रोजेक्ट्स में विभिन्न CAD-संबंधित कार्यों के लिए Aspose.CAD की क्षमताओं का लाभ भी उठा सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD नवीनतम DWG फ़ाइल स्वरूपों के साथ संगत है?

 A1: Aspose.CAD नवीनतम संस्करणों सहित विभिन्न DWG फ़ाइल स्वरूपों का समर्थन करता है। को देखें[प्रलेखन](https://reference.aspose.com/cad/net/) विशिष्ट संगतता विवरण के लिए।

### Q2: क्या मैं वाणिज्यिक और व्यक्तिगत दोनों परियोजनाओं के लिए Aspose.CAD का उपयोग कर सकता हूँ?

 A2: हाँ, Aspose.CAD व्यावसायिक और व्यक्तिगत उपयोग दोनों के लिए लचीले लाइसेंसिंग विकल्प प्रदान करता है। दौरा करना[खरीद पृष्ठ](https://purchase.aspose.com/buy) अधिक जानकारी के लिए।

### Q3: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A3: आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/) मूल्यांकन प्रयोजनों के लिए.

### Q4: मुझे Aspose.CAD के लिए समर्थन कहां मिल सकता है?

उ4: किसी भी प्रश्न या सहायता के लिए, पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19).

### Q5: क्या Aspose.CAD के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

 A5: हां, आप Aspose.CAD के निःशुल्क परीक्षण संस्करण तक पहुंच सकते हैं[यहाँ](https://releases.aspose.com/).