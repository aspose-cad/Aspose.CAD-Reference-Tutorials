---
title: CAD ड्रॉइंग में वॉटरमार्क जोड़ना - Aspose.CAD गाइड
linktitle: CAD ड्रॉइंग में वॉटरमार्क जोड़ना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का उपयोग करके पेशेवर वॉटरमार्क के साथ अपने CAD चित्रों को बेहतर बनाएं। वैयक्तिकृत और आकर्षक डिज़ाइन के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 11
url: /hi/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## परिचय

क्या आप पेशेवर वॉटरमार्क जोड़कर अपने सीएडी चित्रों को बेहतर बनाना चाहते हैं? .NET के लिए Aspose.CAD आपकी CAD फ़ाइलों में वॉटरमार्क को निर्बाध रूप से एकीकृत करने के लिए एक मजबूत समाधान प्रदान करता है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको Aspose.CAD का उपयोग करके वॉटरमार्क जोड़ने की प्रक्रिया के बारे में बताएंगे, यह सुनिश्चित करते हुए कि आपके चित्र न केवल महत्वपूर्ण जानकारी देंगे बल्कि आपका अद्वितीय चिह्न भी रखेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:
-  .NET के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास Aspose.CAD लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).
- आपकी दस्तावेज़ निर्देशिका: अपने CAD चित्रों को संग्रहीत करने के लिए एक निर्देशिका सेट करें।
अब, आइए अपने CAD चित्रों में वॉटरमार्क जोड़ना शुरू करें!

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में आवश्यक नामस्थान आयात करके प्रारंभ करें:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## चरण 1: सीएडी ड्राइंग लोड करें

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## चरण 2: वॉटरमार्क को MTEXT के रूप में जोड़ें

```csharp
// नया MTEXT जोड़ें
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## चरण 3: या टेक्स्ट के रूप में वॉटरमार्क जोड़ें

```csharp
// वैकल्पिक रूप से, टेक्स्ट जैसी सरल इकाई जोड़ें
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## चरण 4: पीडीएफ में निर्यात करें

```csharp
// वॉटरमार्क के साथ सीएडी ड्राइंग को पीडीएफ में निर्यात करें
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

विभिन्न रेखाचित्रों के लिए इन चरणों को दोहराएँ, और आपके पास कुछ ही समय में पेशेवर दिखने वाली वॉटरमार्क वाली CAD फ़ाइलें होंगी!

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि .NET के लिए Aspose.CAD का उपयोग करके अपने CAD चित्रों में वॉटरमार्क कैसे जोड़ें। यह सरल लेकिन शक्तिशाली प्रक्रिया आपको अपने तकनीकी चित्रों की अखंडता को बनाए रखते हुए अपने डिजाइनों को निजीकृत करने की अनुमति देती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं वॉटरमार्क के स्वरूप को अनुकूलित कर सकता हूँ?

A1: हाँ, आप अपनी पसंद के अनुसार टेक्स्ट, फ़ॉन्ट, आकार और वॉटरमार्क की स्थिति को अनुकूलित कर सकते हैं।

### Q2: क्या Aspose.CAD विभिन्न CAD फ़ाइल स्वरूपों के साथ संगत है?

A2: Aspose.CAD व्यापक अनुकूलता सुनिश्चित करते हुए DWG और DXF सहित विभिन्न CAD फ़ाइल स्वरूपों का समर्थन करता है।

### Q3: क्या मैं एक ही CAD ड्राइंग में एकाधिक वॉटरमार्क जोड़ सकता हूँ?

उ3: बिल्कुल! आप विभिन्न उपयोग के मामलों के लिए लचीलापन प्रदान करते हुए, आवश्यकतानुसार उतने वॉटरमार्क जोड़ सकते हैं।

### Q4: क्या Aspose.CAD निःशुल्क परीक्षण की पेशकश करता है?

उ4: हां, आप नि:शुल्क परीक्षण के साथ Aspose.CAD की सुविधाओं का पता लगा सकते हैं। उसे ले लो[यहाँ](https://releases.aspose.com/).

### Q5: मुझे Aspose.CAD के लिए समर्थन कहां मिल सकता है?

 A5: किसी भी प्रश्न या सहायता के लिए, पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19).