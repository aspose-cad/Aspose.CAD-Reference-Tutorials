---
title: 3डी छवियों को पीडीएफ में निर्यात करना - Aspose.CAD ट्यूटोरियल
linktitle: पीडीएफ में 3डी छवियाँ निर्यात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD के साथ 3D CAD छवियों को आसानी से PDF में बदलें। निर्बाध पीडीएफ निर्यात के लिए हमारे चरण-दर-चरण ट्यूटोरियल का पालन करें।
weight: 10
url: /hi/net/3d-image-export/exporting-3d-images-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 3डी छवियों को पीडीएफ में निर्यात करना - Aspose.CAD ट्यूटोरियल

## परिचय

क्या आप .NET के लिए Aspose.CAD का उपयोग करके पीडीएफ में 3D छवियों को निर्बाध रूप से निर्यात करना चाहते हैं? यह चरण-दर-चरण ट्यूटोरियल आपको प्रक्रिया के माध्यम से मार्गदर्शन करेगा, यह सुनिश्चित करते हुए कि आप अपनी 3D छवियों को आसानी से पीडीएफ प्रारूप में परिवर्तित करने के लिए Aspose.CAD की शक्ति का उपयोग करते हैं।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास .NET के लिए Aspose.CAD लाइब्रेरी स्थापित है। यदि नहीं, तो आप इसे यहां से डाउनलोड कर सकते हैं[.NET डाउनलोड पेज के लिए Aspose.CAD](https://releases.aspose.com/cad/net/).

- दस्तावेज़ निर्देशिका: एक निर्देशिका स्थापित करें जहाँ आपकी CAD फ़ाइलें संग्रहीत हैं, और पथ नोट करें।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.CAD के साथ काम करने के लिए आवश्यक नेमस्पेस आयात करें। अपनी कोड फ़ाइल के शीर्ष पर निम्नलिखित पंक्तियाँ जोड़ें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## चरण 1: सीएडी छवि लोड करें

 उस सीएडी छवि को लोड करके शुरुआत करें जिसे आप पीडीएफ में निर्यात करना चाहते हैं। उपयोग`Load` Aspose.CAD लाइब्रेरी से विधि। प्रतिस्थापित करें`"conic_pyramid.dxf"` आपकी CAD फ़ाइल के पथ के साथ।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // CAD छवि लोड करने के लिए आपका कोड यहां दिया गया है
}
```

## चरण 2: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

 CAD छवि के लिए रेखापुंज विकल्प कॉन्फ़िगर करें। पेज की चौड़ाई, पेज की ऊंचाई और लेआउट जैसे पैरामीटर सेट करें। से संबंधित पंक्ति को अनटिप्पणी करें`TypeOfEntities` यदि आपकी इकाइयाँ 3D हैं।

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = typeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## चरण 3: पीडीएफ विकल्प सेट करें

पीडीएफ विकल्प बनाएं और उन्हें रैस्टराइज़ेशन विकल्पों के साथ संबद्ध करें।

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## चरण 4: पीडीएफ के रूप में सहेजें

कॉन्फ़िगर विकल्पों का उपयोग करके सीएडी छवि को पीडीएफ फ़ाइल के रूप में सहेजें। पीडीएफ फ़ाइल के लिए आउटपुट पथ निर्दिष्ट करें।

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.CAD का उपयोग करके पीडीएफ में 3डी छवियों को सफलतापूर्वक निर्यात किया है। यह सीधा ट्यूटोरियल यह सुनिश्चित करता है कि आप आसानी से अपनी CAD फ़ाइलों को अधिक सुलभ प्रारूप में परिवर्तित कर सकें।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD सभी CAD फ़ाइल स्वरूपों के साथ संगत है?

A1: हां, Aspose.CAD विभिन्न फ़ाइल प्रकारों को संभालने में लचीलापन सुनिश्चित करते हुए, CAD प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### Q2: क्या मैं पीडीएफ में निर्यात करते समय पृष्ठ आयामों को अनुकूलित कर सकता हूं?

ए2: बिल्कुल। ट्यूटोरियल दर्शाता है कि अपनी आवश्यकताओं के अनुसार पृष्ठ की चौड़ाई और ऊंचाई को कैसे कॉन्फ़िगर करें।

### Q3: क्या Aspose.CAD के लिए अस्थायी लाइसेंस उपलब्ध हैं?

 उ3: हाँ, आप Aspose.CAD पर जाकर अस्थायी लाइसेंस प्राप्त कर सकते हैं[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/).

### Q4: मुझे अतिरिक्त सहायता या सामुदायिक चर्चाएँ कहाँ मिल सकती हैं?

 A4: की ओर जाएं[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) समुदाय के समर्थन और उससे जुड़ने के लिए।

### Q5: क्या Aspose.CAD का कोई निःशुल्क परीक्षण संस्करण उपलब्ध है?

 A5: हां, आप Aspose.CAD पर पहुंच कर इसकी विशेषताओं का पता लगा सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
