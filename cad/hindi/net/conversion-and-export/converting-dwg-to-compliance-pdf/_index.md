---
title: DWG को अनुपालन पीडीएफ में परिवर्तित करना - Aspose.CAD ट्यूटोरियल
linktitle: DWG को अनुपालन पीडीएफ में परिवर्तित करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD के साथ DWG को अनुपालन पीडीएफ में बदलें। चरण-दर-चरण मार्गदर्शन के लिए हमारे ट्यूटोरियल का अनुसरण करें।
weight: 13
url: /hi/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG को अनुपालन पीडीएफ में परिवर्तित करना - Aspose.CAD ट्यूटोरियल

## परिचय

.NET के लिए Aspose.CAD का उपयोग करके DWG फ़ाइलों को अनुपालन पीडीएफ में परिवर्तित करने पर हमारे चरण-दर-चरण ट्यूटोरियल में आपका स्वागत है। Aspose.CAD एक शक्तिशाली .NET API है जो डेवलपर्स को CAD फ़ाइल स्वरूपों के साथ सहजता से काम करने में सक्षम बनाता है। इस ट्यूटोरियल में, हम आपको विस्तृत उदाहरणों और स्पष्टीकरणों के साथ DWG फ़ाइल को अनुपालन पीडीएफ में परिवर्तित करने की प्रक्रिया के बारे में मार्गदर्शन करेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास Aspose.CAD लाइब्रेरी आपके .NET प्रोजेक्ट में एकीकृत है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

- विकास परिवेश: एक कार्यशील .NET विकास परिवेश स्थापित करें, और सुनिश्चित करें कि यह सही ढंग से कॉन्फ़िगर किया गया है।

- नमूना DWG फ़ाइल: एक नमूना DWG फ़ाइल डाउनलोड करें जिसे आप अनुपालन पीडीएफ में कनवर्ट करना चाहते हैं।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.CAD कार्यक्षमताओं का उपयोग करने के लिए आवश्यक नामस्थान आयात करें।

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

अब, आइए DWG फ़ाइल को अनुपालन पीडीएफ में परिवर्तित करने की प्रक्रिया को कई चरणों में विभाजित करें।

## चरण 1: DWG फ़ाइल लोड करें

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## चरण 2: रैस्टराइज़ेशन विकल्प सेट करें

 का एक उदाहरण बनाएं`CadRasterizationOptions` और इसके गुणों को कॉन्फ़िगर करें, जैसे पृष्ठभूमि रंग, पृष्ठ चौड़ाई और पृष्ठ ऊंचाई।

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## चरण 3: पीडीएफ विकल्प बनाएं

 का एक उदाहरण बनाएं`PdfOptions` और वेक्टर रेखापुंज विकल्प सेट करें।

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## चरण 4: पीडीएफ के रूप में सहेजें (ए1ए अनुपालन)

A1a अनुपालन के साथ CAD छवि को अनुपालन पीडीएफ के रूप में सहेजें।

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## चरण 5: पीडीएफ के रूप में सहेजें (ए1बी अनुपालन)

अनुपालन प्रकार को A1b में बदलें और CAD छवि को अनुपालन पीडीएफ के रूप में सहेजें।

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.CAD का उपयोग करके DWG फ़ाइल को अनुपालन पीडीएफ में सफलतापूर्वक परिवर्तित कर लिया है। यह ट्यूटोरियल उन डेवलपर्स के लिए एक व्यापक मार्गदर्शिका प्रदान करता है जो अपने अनुप्रयोगों में सीएडी रूपांतरण क्षमताओं को एकीकृत करना चाहते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.CAD का उपयोग करके अन्य CAD प्रारूपों को अनुपालन पीडीएफ में बदल सकता हूँ?

A1: हां, Aspose.CAD विभिन्न CAD प्रारूपों का समर्थन करता है, जो अनुपालन पीडीएफ में रूपांतरण को सक्षम बनाता है।

### Q2: क्या Aspose.CAD .NET कोर के साथ संगत है?

A2: हां, Aspose.CAD .NET फ्रेमवर्क और .NET कोर दोनों के साथ संगत है।

### Q3: क्या Aspose.CAD के लिए कोई लाइसेंसिंग विकल्प हैं?

 उ3: हां, आप लाइसेंसिंग विकल्प तलाश सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### Q4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ4: हाँ, आप निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q5: मुझे Aspose.CAD के लिए समर्थन कहाँ से मिल सकता है?

A5: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) किसी भी समर्थन-संबंधी प्रश्न के लिए।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
