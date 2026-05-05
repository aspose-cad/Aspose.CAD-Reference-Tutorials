---
date: 2026-03-16
description: Aspose.CAD for .NET के साथ DWG को PDF या रास्टर इमेज में कैसे बदलें,
  सीखें। यह चरण‑दर‑चरण CAD‑to‑PDF ट्यूटोरियल DWG को PNG जैसे इमेज फ़ॉर्मेट में एक्सपोर्ट
  करने को कवर करता है और दिखाता है कि DWG को इमेज फ़ाइलों में कुशलतापूर्वक कैसे एक्सपोर्ट
  किया जाए।
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET का उपयोग करके DWG को PDF और रास्टर इमेजेज़ में कैसे बदलें
url: /hi/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG को PDF या रास्टर इमेजेज़ में निर्यात करना - Aspose.CAD गाइड

## परिचय

यदि आपको **DWG को PDF** में (या PNG जैसे रास्टर फ़ॉर्मेट में) सीधे .NET एप्लिकेशन से बदलने की आवश्यकता है, तो आप सही जगह पर हैं। इस ट्यूटोरियल में हम Aspose.CAD for .NET का उपयोग करके रूपांतरण करने के लिए आवश्यक सटीक चरणों को बताएँगे, समझाएँगे कि यह लाइब्रेरी क्यों एक मजबूत विकल्प है, और दिखाएँगे कि केवल कुछ कोड लाइनों से PDF और इमेज दोनों आउटपुट को कैसे संभालें।

## त्वरित उत्तर
- **DWG रूपांतरण को कौनसी लाइब्रेरी संभालती है?** Aspose.CAD for .NET  
- **क्या मैं DWG को PNG के साथ-साथ PDF में भी निर्यात कर सकता हूँ?** हाँ – दोनों फ़ॉर्मेट्स के लिए वही रास्टराइज़ेशन विकल्प काम करते हैं।  
- **क्या विकास के लिए लाइसेंस चाहिए?** टेस्टिंग के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **कौनसे .NET संस्करण समर्थित हैं?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **क्या इकाई रूपांतरण स्वचालित रूप से संभाला जाता है?** आप कोड में दिखाए अनुसार इकाई प्रणाली को मैन्युअली (मीट्रिक या इम्पीरियल) परिभाषित कर सकते हैं।

## “DWG को PDF में बदलना” क्या है?
DWG को PDF में बदलना का मतलब है CAD ड्राइंग (DWG) को एक पोर्टेबल, केवल‑देखने योग्य दस्तावेज़ (PDF) में रेंडर करना। यह उन हितधारकों के साथ डिज़ाइन साझा करने के लिए उपयोगी है जिनके पास CAD सॉफ़्टवेयर नहीं है, प्रिंट करने योग्य दस्तावेज़ बनाने के लिए, या ड्रॉइंग को एक सार्वभौमिक रूप से पढ़े जाने योग्य फ़ॉर्मेट में संग्रहित करने के लिए।

## इस रूपांतरण के लिए Aspose.CAD का उपयोग क्यों करें?
- **कोई बाहरी निर्भरताएँ नहीं** – लाइब्रेरी पूरी तरह से प्रबंधित कोड में काम करती है।  
- **उच्च सटीकता** – लेयर्स, लाइन वेट्स और लेआउट जानकारी को बनाए रखती है।  
- **इन‑बिल्ट रास्टर विकल्प** – एक ही कॉन्फ़िगरेशन ऑब्जेक्ट के साथ PNG, JPEG, BMP आदि में निर्यात करने देता है।  
- **क्रॉस‑प्लेटफ़ॉर्म** – .NET Core के साथ Windows, Linux, और macOS पर काम करता है।

## पूर्वापेक्षाएँ

ट्यूटोरियल में आगे बढ़ने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित उपलब्ध हैं:

- .NET प्रोग्रामिंग की बुनियादी समझ।  
- Aspose.CAD for .NET लाइब्रेरी स्थापित हो। यदि नहीं, तो इसे [here](https://releases.aspose.com/cad/net/) से डाउनलोड करें।  
- आपका पसंदीदा इंटीग्रेटेड डेवलपमेंट एनवायरनमेंट (IDE) .NET विकास के लिए सेट अप हो।

## नेमस्पेस आयात करें

आइए आपके .NET प्रोजेक्ट में आवश्यक नेमस्पेस आयात करके शुरू करें। यह सुनिश्चित करता है कि आपके कोड में आपको Aspose.CAD कार्यक्षमता तक पहुँच मिले।

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## चरण 1: DWG फ़ाइल लोड करें

जिस DWG फ़ाइल को आप बदलना चाहते हैं उसे लोड करके शुरू करें। `"Your Document Directory"` को अपनी DWG फ़ाइल के पथ से बदलें।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## चरण 2: PDF निर्यात सेट करें (DWG को PDF में निर्यात कैसे करें)

अब, PDF निर्यात सेटिंग्स को कॉन्फ़िगर करते हैं। यह उदाहरण लेआउट सेट करने और इकाई रूपांतरण को संभालने का तरीका दर्शाता है।

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## चरण 3: PDF में निर्यात करें

कॉन्फ़िगर किए गए सेटिंग्स का उपयोग करके PDF में निर्यात को निष्पादित करें।

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## चरण 4: रास्टर इमेजेज़ में निर्यात करें (dwg को इमेज में निर्यात)

फ़ंक्शनालिटी को विस्तारित करके PNG जैसी रास्टर इमेजेज़ में निर्यात करें।

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## सामान्य समस्याएँ और समाधान

| समस्या | क्यों होता है | समाधान |
|-------|----------------|------------|
| **PDF में खाली पृष्ठ** | लेआउट सही ढंग से निर्दिष्ट नहीं किया गया | सुनिश्चित करें कि `rasterizationOptions.Layouts` में सही लेआउट नाम (जैसे, `"Model"`) शामिल है। |
| **गलत आयाम** | DPI या पेज आकार का मेल नहीं | `CadRasterizationOptions` में `PageHeight`, `PageWidth`, और DPI मानों को समायोजित करें। |
| **इकाइयाँ गलत दिख रही हैं** | इकाई रूपांतरण परिभाषित नहीं है | `DefineUnitSystem` का उपयोग करके `cadImage.UnitType` के आधार पर `currentUnitIsMetric` और `currentUnitCoefficient` सेट करें। |
| **लाइसेंस अपवाद** | ट्रायल संस्करण की सीमाएँ | `Image.Load` कॉल करने से पहले एक अस्थायी या स्थायी लाइसेंस लागू करें। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अपने व्यावसायिक प्रोजेक्ट्स में Aspose.CAD for .NET का उपयोग कर सकता हूँ?
A1: हाँ, आप कर सकते हैं। लाइसेंसिंग विवरण के लिए [purchase.aspose.com/buy](https://purchase.aspose.com/buy) पर जाएँ।

### Q2: क्या कोई मुफ्त ट्रायल उपलब्ध है?
A2: बिल्कुल! अपना मुफ्त ट्रायल [here](https://releases.aspose.com/) से प्राप्त करें।

### Q3: मैं Aspose.CAD for .NET के लिए समर्थन कैसे प्राप्त कर सकता हूँ?
A3: समुदाय समर्थन के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

### Q4: क्या मैं परीक्षण उद्देश्यों के लिए एक अस्थायी लाइसेंस प्राप्त कर सकता हूँ?
A4: हाँ, आप एक अस्थायी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

### Q5: विस्तृत दस्तावेज़ीकरण कहाँ मिल सकता है?
A5: दस्तावेज़ीकरण [Aspose.CAD](https://reference.aspose.com/cad/net/) पर उपलब्ध है।

### Q6: मैं उच्च गुणवत्ता के साथ **CAD को PNG के रूप में सहेजूँ** कैसे?
A6: `CadRasterizationOptions` में `PageHeight` और `PageWidth` को इच्छित पिक्सेल आयाम पर सेट करें और DPI को 300 या उससे अधिक चुनें।

### Q7: जब स्रोत फ़ाइल में कई लेआउट हों तो **dwg को कैसे बदलें** का सबसे अच्छा तरीका क्या है?
A7: `rasterizationOptions.Layouts` को उन सभी लेआउट नामों से भरें जिन्हें आप निर्यात करना चाहते हैं, फिर प्रत्येक लेआउट पर लूप करें और प्रत्येक आउटपुट फ़ॉर्मेट के लिए `Save` कॉल करें।

**अंतिम अपडेट:** 2026-03-16  
**परीक्षित संस्करण:** Aspose.CAD 24.11 for .NET  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}