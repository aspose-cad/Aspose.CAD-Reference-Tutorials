---
title: .NET के लिए Aspose.CAD में कस्टम पेन विकल्पों के साथ CAD निर्यात बढ़ाएं
linktitle: निर्यात में पेन समर्थन
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: जानें कि .NET के लिए Aspose.CAD का उपयोग करके अपने CAD छवि निर्यात को कैसे बढ़ाया जाए। पीडीएफ, पीएनजी, बीएमपी और अन्य में आश्चर्यजनक दृश्यों के लिए पेन विकल्पों को अनुकूलित करें।
weight: 12
url: /hi/net/cad-features-and-support/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.CAD में कस्टम पेन विकल्पों के साथ CAD निर्यात बढ़ाएं

## परिचय

.NET के लिए Aspose.CAD कंप्यूटर-एडेड डिज़ाइन (CAD) फ़ाइलों के साथ काम करने के लिए टूल का एक शक्तिशाली सेट प्रदान करता है, जो डेवलपर्स को CAD छवियों में हेरफेर करने और निर्यात करने में सक्षम बनाता है। एक उल्लेखनीय विशेषता निर्यात के दौरान पेन समर्थन है, जो उपयोगकर्ताओं को पीडीएफ, पीएनजी, बीएमपी, जीआईएफ, जेपीईजी2000, जेपीईजी, पीएसडी, टीआईएफएफ और डब्लूएमएफ जैसे विभिन्न प्रारूपों में सीएडी छवियों को निर्यात करते समय पेन के लिए स्टार्ट और एंड कैप सेटिंग्स को अनुकूलित करने की अनुमति देता है।

इस ट्यूटोरियल में, हम .NET के लिए Aspose.CAD का उपयोग करके निर्यात में पेन समर्थन की बारीकियों के बारे में विस्तार से जानेंगे। हम प्रक्रिया में आपका मार्गदर्शन करने के लिए स्पष्ट स्पष्टीकरण और उदाहरण प्रदान करते हुए प्रत्येक चरण का विवरण देंगे।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- आपके विकास परिवेश में .NET के लिए Aspose.CAD स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[रिलीज पेज](https://releases.aspose.com/cad/net/).

- सीएडी फ़ाइल स्वरूपों, विशेष रूप से डीएक्सएफ (ड्राइंग एक्सचेंज फॉर्मेट) की बुनियादी समझ।

- C# प्रोग्रामिंग भाषा का कार्यसाधक ज्ञान।

## नामस्थान आयात करें

आरंभ करने के लिए, सुनिश्चित करें कि आप अपने C# प्रोजेक्ट में आवश्यक नामस्थान आयात करें:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## चरण 1: अपनी दस्तावेज़ निर्देशिका सेट करें

उस निर्देशिका को परिभाषित करें जहां आपका CAD दस्तावेज़ स्थित है:

```csharp
string MyDir = "Your Document Directory";
```

## चरण 2: सीएडी छवि लोड करें

Aspose.CAD का उपयोग करके CAD छवि लोड करें:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## चरण 3: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

निर्यात प्रक्रिया को अनुकूलित करने के लिए रेखापुंज और पीडीएफ विकल्प बनाएं:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## चरण 4: पेन विकल्पों को अनुकूलित करें

पेन के लिए प्रारंभ और समाप्ति कैप विकल्प सेट करें:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## चरण 5: वेक्टर रैस्टराइज़ेशन विकल्प लागू करें

पीडीएफ विकल्पों में रेखापुंज विकल्प लागू करें:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## चरण 6: निर्यात की गई पीडीएफ को सहेजें

अनुकूलित पेन विकल्पों के साथ सीएडी छवि को पीडीएफ फाइल के रूप में सहेजें:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने .NET के लिए Aspose.CAD की निर्यात सुविधा में पेन समर्थन का पता लगाया है। चरण-दर-चरण मार्गदर्शिका का पालन करके, आप अपने सीएडी छवि निर्यात के लचीलेपन को बढ़ाते हुए, पेन के लिए स्टार्ट और एंड कैप सेटिंग्स को आसानी से अनुकूलित कर सकते हैं।

अपनी निर्यात की गई छवियों में वांछित दृश्य प्रभाव प्राप्त करने के लिए विभिन्न पेन विकल्पों के साथ बेझिझक प्रयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं पीडीएफ के अलावा अन्य छवि प्रारूपों के लिए इन पेन विकल्पों का उपयोग कर सकता हूं?

A1: हां, पेन विकल्प विभिन्न छवि प्रारूपों जैसे पीएनजी, बीएमपी, जीआईएफ, जेपीईजी और अन्य पर लागू किया जा सकता है।

### Q2: मुझे .NET के लिए Aspose.CAD के लिए अतिरिक्त दस्तावेज़ कहां मिल सकते हैं?

 A2: देखें[प्रलेखन](https://reference.aspose.com/cad/net/) व्यापक जानकारी और उदाहरणों के लिए।

### Q3: क्या .NET के लिए Aspose.CAD का निःशुल्क परीक्षण उपलब्ध है?

 उ3: हाँ, आप निःशुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं .NET के लिए Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A4: पर जाएँ[अस्थायी लाइसेंस पृष्ठ](https://purchase.aspose.com/temporary-license/) अस्थायी लाइसेंसिंग विकल्पों के लिए।

### Q5: मैं .NET के लिए Aspose.CAD के लिए सामुदायिक समर्थन कहाँ से प्राप्त कर सकता हूँ?

 A5: समुदाय के साथ जुड़ें[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
