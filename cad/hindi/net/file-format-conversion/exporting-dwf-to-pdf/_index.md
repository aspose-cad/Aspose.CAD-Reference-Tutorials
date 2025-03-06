---
title: DWF को PDF में निर्यात करना - Aspose.CAD गाइड
linktitle: DWF को पीडीएफ में निर्यात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का उपयोग करके DWF को PDF में निर्यात करने पर एक सहज मार्गदर्शिका देखें। अपनी CAD फ़ाइल प्रबंधन क्षमताओं को सहजता से बढ़ाएँ।
weight: 10
url: /hi/net/file-format-conversion/exporting-dwf-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWF को PDF में निर्यात करना - Aspose.CAD गाइड

## परिचय

.NET विकास की दुनिया में, Aspose.CAD कंप्यूटर-एडेड डिज़ाइन (CAD) फ़ाइलों को संभालने के लिए एक शक्तिशाली लाइब्रेरी के रूप में खड़ा है। इस ट्यूटोरियल में, हम एक विशिष्ट कार्य पर ध्यान केंद्रित करेंगे: .NET के लिए Aspose.CAD का उपयोग करके DWF (डिज़ाइन वेब प्रारूप) फ़ाइलों को पीडीएफ में निर्यात करना। चाहे आप एक अनुभवी डेवलपर हों या अभी शुरुआत कर रहे हों, इस कार्यक्षमता को अपने अनुप्रयोगों में निर्बाध रूप से एकीकृत करने के लिए आगे बढ़ें।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

-  .NET के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास .NET के लिए Aspose.CAD स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

- विकास पर्यावरण: विज़ुअल स्टूडियो या किसी अन्य पसंदीदा आईडीई सहित एक कार्यशील .NET विकास वातावरण स्थापित करें।

## नामस्थान आयात करें

अपने प्रोजेक्ट में आवश्यक नामस्थान आयात करके प्रारंभ करें। Aspose.CAD द्वारा प्रदान की गई कार्यक्षमताओं तक पहुँचने के लिए यह चरण महत्वपूर्ण है।

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## चरण 1: DWF फ़ाइल लोड करें

उस DWF फ़ाइल को लोड करके शुरुआत करें जिसे आप पीडीएफ में निर्यात करना चाहते हैं। फ़ाइल पथ को तदनुसार समायोजित करें।

```csharp
string MyDir = "Your Document Directory";
string fileName = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(fileName))
{
    // आपका कोड यहां...
}
```

## चरण 2: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

वांछित आउटपुट सुनिश्चित करने के लिए DWF के लिए रैस्टराइज़ेशन विकल्प सेट करें। इस उदाहरण में, हम पृष्ठ की ऊंचाई और चौड़ाई को परिभाषित करते हैं।

```csharp
CadRasterizationOptions dwfRasterizationOptions = new CadRasterizationOptions();
dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## चरण 3: पीडीएफ विकल्पों को परिभाषित करें

पीडीएफ विकल्प बनाएं और उन्हें पहले से कॉन्फ़िगर किए गए रैस्टराइज़ेशन विकल्पों के साथ संबद्ध करें।

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = dwfRasterizationOptions;
```

## चरण 4: पीडीएफ में निर्यात करें

परिणामी पीडीएफ फ़ाइल के लिए आउटपुट पथ निर्दिष्ट करते हुए, निर्यात प्रक्रिया निष्पादित करें।

```csharp
string outPath = MyDir + "18-12-11 9644 - site.pdf";
image.Save(outPath, pdfOptions);
```

## चरण 5: निर्यात सत्यापित करें

पीडीएफ में 3डी छवियों का सफल निर्यात सुनिश्चित करें। सहेजे गए फ़ाइल पथ के साथ एक पुष्टिकरण संदेश प्रदर्शित करें।

```csharp
Console.WriteLine("\n3D images exported successfully to PDF.\nFile saved at " + MyDir);
```

अब आपने Aspose.CAD का उपयोग करके अपने .NET एप्लिकेशन में DWF से PDF निर्यात कार्यक्षमता को सफलतापूर्वक लागू कर दिया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने .NET के लिए Aspose.CAD का उपयोग करके DWF फ़ाइलों को PDF में निर्यात करने की प्रक्रिया का पता लगाया। इन चरणों का पालन करके, आप अपनी CAD फ़ाइल प्रबंधन क्षमताओं को बढ़ाते हुए, इस कार्यक्षमता को अपनी परियोजनाओं में निर्बाध रूप से एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य CAD फ़ाइल स्वरूपों के साथ .NET के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: हाँ, Aspose.CAD DWG, DXF, DWF और अन्य सहित विभिन्न CAD फ़ाइल स्वरूपों का समर्थन करता है। विस्तृत सूची के लिए दस्तावेज़ की जाँच करें।

### Q2: मुझे Aspose.CAD के लिए अतिरिक्त सहायता कहां मिल सकती है?

 A2: अतिरिक्त सहायता के लिए, पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) जहां आप प्रश्न पूछ सकते हैं और समुदाय के साथ बातचीत कर सकते हैं।

### Q3: क्या Aspose.CAD के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

 उ3: हाँ, आप Aspose.CAD का निःशुल्क परीक्षण संस्करण देख सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त करूं?

 A4: आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं[इस लिंक](https://purchase.aspose.com/temporary-license/).

### Q5: मैं .NET के लिए Aspose.CAD का पूर्ण संस्करण कहां से खरीद सकता हूं?

 A5: आप .NET के लिए Aspose.CAD का पूर्ण संस्करण यहां से खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
