---
date: 2026-08-17
description: C# और Aspose.CAD for .NET का उपयोग करके dwg फ़ाइलों में इमेज जोड़ना सीखें।
  यह गाइड आपको इमेज इम्पोर्ट करने, इंसर्शन पॉइंट सेट करने, और PDF में एक्सपोर्ट करने
  की प्रक्रिया दिखाता है।
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: C# के साथ DWG फ़ाइलों में इमेज इम्पोर्ट करना
og_description: C# का उपयोग करके dwg फ़ाइलों में इमेज जोड़ना सीखें। यह ट्यूटोरियल
  इमेज इम्पोर्ट करने, इंसर्शन पॉइंट सेट करने, और Aspose.CAD के साथ dwg को PDF में
  कनवर्ट करने को कवर करता है।
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: C# और Aspose.CAD का उपयोग करके dwg फ़ाइलों में इमेज जोड़ने का तरीका
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: C# और Aspose.CAD का उपयोग करके dwg फ़ाइलों में इमेज जोड़ने का तरीका
url: /hi/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# का उपयोग करके Aspose.CAD के साथ dwg फ़ाइलों में छवि कैसे जोड़ें

## परिचय

जब आपको CAD ड्रॉइंग्स को लोगो, फ़ोटो या रास्टर ग्राफ़िक्स से समृद्ध करना हो, तो DWG फ़ाइल में छवि जोड़ना एक सामान्य आवश्यकता है। इस ट्यूटोरियल में आप सीखेंगे कि कैसे **add image to dwg** को प्रोग्रामेटिक रूप से C# और Aspose.CAD for .NET का उपयोग करके जोड़ें, और फिर वैकल्पिक रूप से परिणाम को PDF में बदलें। चरणों को इस तरह विभाजित किया गया है कि आप प्रत्येक भाग को अपनी परियोजना में कॉपी‑पेस्ट कर सकें।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी इस कार्य को संभालती है?** Aspose.CAD for .NET.
- **क्या मैं PNG फ़ाइलें एम्बेड कर सकता हूँ?** हाँ – PNG, JPEG, BMP और अन्य रास्टर फ़ॉर्मेट समर्थित हैं।
- **क्या विकास के लिए मुझे लाइसेंस चाहिए?** परीक्षण के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।
- **क्या PDF निर्यात समर्थित है?** बिल्कुल – आप अपडेटेड DWG को एक लाइन में PDF में बदल सकते हैं।
- **कौन से .NET संस्करण संगत हैं?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## DWG फ़ाइल क्या है?

DWG फ़ाइल Autodesk AutoCAD ड्रॉइंग्स के लिए मूल बाइनरी फ़ॉर्मेट है, जो वेक्टर ज्योमेट्री, लेयर्स और मेटाडेटा संग्रहीत करता है। यह वास्तुकला, इंजीनियरिंग और निर्माण में व्यापक रूप से उपयोग होता है, और Aspose.CAD इस फ़ॉर्मेट को बिना AutoCAD स्थापित किए पढ़ और लिख सकता है।

## Aspose.CAD के साथ dwg में छवि क्यों जोड़ें?

Aspose.CAD **50+ इनपुट और आउटपुट फ़ॉर्मेट** का समर्थन करता है, 500 MB से बड़े फ़ाइलों को पूरी डॉक्यूमेंट मेमोरी में लोड किए बिना प्रोसेस कर सकता है, और एक निर्धारक API प्रदान करता है जो हेडलेस सर्वर वातावरण में काम करता है। यह DWG ड्रॉइंग्स के बल्क‑प्रोसेसिंग को तेज़ और विश्वसनीय बनाता है।

## पूर्वापेक्षाएँ
- C# प्रोग्रामिंग का मूल ज्ञान।
- Aspose.CAD for .NET स्थापित। आप इसे [Aspose.CAD for .NET डाउनलोड पृष्ठ](https://releases.aspose.com/cad/net/) से डाउनलोड कर सकते हैं। आप अन्य Aspose उत्पादों को भी [Aspose रिलीज़ पृष्ठ](https://releases.aspose.com/) पर देख सकते हैं।
- Visual Studio 2022 या उसके बाद का विकास वातावरण।

## Aspose.CAD का उपयोग करके dwg में छवि कैसे जोड़ें?

लक्षित DWG लोड करें, एक रास्टर इमेज ऑब्जेक्ट बनाएं जो आप एम्बेड करना चाहते हैं, इंसर्शन पॉइंट और स्केलिंग वेक्टर सेट करें, फिर इमेज को ड्रॉइंग में जोड़ें। अंत में संशोधित DWG को सहेजें या सीधे PDF में निर्यात करें। पूरा वर्कफ़्लो केवल कुछ API कॉल्स में पूरा हो जाता है और सामान्य 2‑पेज ड्रॉइंग्स के लिए एक सेकंड से कम समय लेता है।

### नेमस्पेस आयात करें
उन नेमस्पेस को शामिल करें जो आपको आवश्यक CAD क्लासेज़ को एक्सपोज़ करते हैं।

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### चरण 1: अपने दस्तावेज़ डायरेक्टरी सेट करें
उस फ़ोल्डर को तैयार करें जिसमें स्रोत DWG और वह इमेज हो जिसे आप एम्बेड करना चाहते हैं।

```csharp
string MyDir = "Your Document Directory";
```

### चरण 2: dwg फ़ाइल लोड करें
`CadImage` क्लास एक DWG ड्रॉइंग का प्रतिनिधित्व करती है और इसकी एंटिटीज़, लेयर्स और मेटाडेटा तक पहुँच प्रदान करती है।

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### चरण 3: छवि गुण निर्धारित करें
एक `Image` ऑब्जेक्ट बनाएं जो रास्टर फ़ाइल (जैसे PNG) की ओर इशारा करता है और उसका फ़ॉर्मेट निर्दिष्ट करें।

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### चरण 4: insertion point dwg और वेक्टर सेट करें
निर्दिष्ट करें कि इमेज ड्रॉइंग के भीतर कहाँ दिखाई देगी और उसे कैसे स्केल किया जाएगा। इंसर्शन पॉइंट 2‑D निर्देशांक द्वारा परिभाषित होता है, जबकि वेक्टर चौड़ाई और ऊँचाई नियंत्रित करते हैं।

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### चरण 5: रास्टर इमेज बनाएं और कॉन्फ़िगर करें
एक `RasterImage` ऑब्जेक्ट इंस्टैंशिएट करें, इमेज डेटा असाइन करें, और कोई अतिरिक्त रेंडरिंग विकल्प सेट करें।

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### चरण 6: dwg फ़ाइल में छवि जोड़ें
कॉन्फ़िगर की गई रास्टर इमेज को DWG की एंटिटीज़ कलेक्शन में डालें ताकि वह ड्रॉइंग का हिस्सा बन जाए।

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### चरण 7: PDF के रूप में सहेजें (dwg को pdf में निर्यात करें)
इमेज एम्बेड करने के बाद आप **convert dwg to pdf** या **save dwg as pdf** को एक ही कॉल से कर सकते हैं। यह उन स्टेकहोल्डर्स के साथ ड्रॉइंग साझा करने में उपयोगी है जिनके पास CAD सॉफ़्टवेयर नहीं है।

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## छवि एम्बेड करने के बाद dwg को pdf में कैसे बदलें?

`CadImage` इंस्टेंस पर `Save` मेथड को `SaveFormat.Pdf` के साथ कॉल करें और वैकल्पिक रूप से एक `PdfOptions` ऑब्जेक्ट पास करें ताकि पेज साइज, रास्टराइज़ेशन और मेटाडेटा नियंत्रित हो सके। Aspose.CAD एम्बेडेड रास्टर इमेज, लेयर्स और लाइन वेट्स को संरक्षित रखता है, जिससे एक सटीक PDF प्रतिनिधित्व बनता है जिसे कोई भी व्यूअर खोल सकता है। यह परिवर्तन एक ही लाइन के कोड में किया जाता है।

## सामान्य समस्याएँ और समाधान
- **Image appears at the wrong location** – इंसर्शन पॉइंट निर्देशांक और दिशा वेक्टर को दोबारा जाँचें; वे ड्रॉइंग के मूल बिंदु के सापेक्ष होते हैं।
- **Large images cause memory spikes** – इंसर्शन से पहले रास्टर इमेज पर `Resize` विकल्प का उपयोग करें, या कम‑रिज़ॉल्यूशन कॉपी के साथ काम करें।
- **PDF export loses vector quality** – सुनिश्चित करें कि आप `PdfOptions` के साथ सहेज रहे हैं जो वेक्टर डेटा को बनाए रखता है; रास्टर इमेज हमेशा जैसा है वैसा एम्बेड रहती है।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.CAD for .NET को अन्य प्रोग्रामिंग भाषाओं के साथ उपयोग कर सकता हूँ?**  
A: कोर लाइब्रेरी .NET‑विशिष्ट है, लेकिन Aspose Java, Python और अन्य प्लेटफ़ॉर्म के लिए समकक्ष API प्रदान करता है।

**Q: क्या Aspose.CAD के लिए एक मुफ्त ट्रायल उपलब्ध है?**  
A: हाँ, आप एक मुफ्त ट्रायल को [Aspose मुफ्त ट्रायल पृष्ठ](https://releases.aspose.com/) पर देख सकते हैं।

**Q: Aspose.CAD के लिए विस्तृत दस्तावेज़ीकरण कहाँ मिल सकता है?**  
A: दस्तावेज़ीकरण [Aspose.CAD .NET API रेफ़रेंस](https://reference.aspose.com/cad/net/) में उपलब्ध है।

**Q: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त करूँ?**  
A: अस्थायी लाइसेंस पाने के लिए [temporary license page](https://purchase.aspose.com/temporary-license/) पर जाएँ।

**Q: क्या Aspose.CAD समर्थन के लिए समुदाय फ़ोरम हैं?**  
A: हाँ, आप [Aspose.CAD community forum](https://forum.aspose.com/c/cad/19) में समर्थन प्राप्त कर सकते हैं और समुदाय के साथ जुड़ सकते हैं।

---

**अंतिम अपडेट:** 2026-08-17  
**परीक्षण किया गया:** Aspose.CAD 24.11 for .NET  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [DWG को PDF या रास्टर इमेज में निर्यात करना - Aspose.CAD गाइड](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [C# में DWG को DXF फ़ॉर्मेट में निर्यात करना - Aspose.CAD ट्यूटोरियल](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [विशिष्ट लेआउट को PDF में निर्यात करना - Aspose.CAD गाइड](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}