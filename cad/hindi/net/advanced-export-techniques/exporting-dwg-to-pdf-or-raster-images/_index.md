---
title: DWG को PDF या Raster Images में निर्यात करना - Aspose.CAD गाइड
linktitle: DWG को PDF या Raster छवियों में निर्यात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का उपयोग करके DWG को PDF या रेखापुंज छवियों में निर्यात करने पर एक व्यापक मार्गदर्शिका देखें। चरणों, पूर्वापेक्षाओं को जानें और इस शक्तिशाली लाइब्रेरी से परिचित हों।
type: docs
weight: 11
url: /hi/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## परिचय

क्या आप अपने .NET एप्लिकेशन में DWG फ़ाइलों को पीडीएफ या रैस्टर छवियों में निर्बाध रूप से परिवर्तित करना चाहते हैं? आगे कोई तलाश नहीं करें! यह चरण-दर-चरण मार्गदर्शिका आपको .NET लाइब्रेरी के लिए शक्तिशाली Aspose.CAD का उपयोग करके प्रक्रिया के बारे में बताएगी। चाहे आप एक अनुभवी डेवलपर हों या अभी शुरुआत कर रहे हों, यह ट्यूटोरियल सभी कौशल स्तरों को पूरा करता है।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित स्थान हैं:

- .NET प्रोग्रामिंग की बुनियादी समझ।
-  .NET लाइब्रेरी के लिए Aspose.CAD स्थापित किया गया। यदि नहीं, तो इसे डाउनलोड करें[यहाँ](https://releases.aspose.com/cad/net/).
- .NET विकास के लिए आपका पसंदीदा एकीकृत विकास वातावरण (आईडीई) स्थापित किया गया।

## नामस्थान आयात करें

आइए आपके .NET प्रोजेक्ट में आवश्यक नेमस्पेस आयात करके शुरुआत करें। यह सुनिश्चित करता है कि आपके पास अपने कोड में Aspose.CAD कार्यक्षमता तक पहुंच है।

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

उस DWG फ़ाइल को लोड करके प्रारंभ करें जिसे आप कनवर्ट करना चाहते हैं। "आपकी दस्तावेज़ निर्देशिका" को अपनी DWG फ़ाइल के पथ से बदलें।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // DWG लोड करने के लिए आपका कोड यहां दिया गया है
}
```

## चरण 2: पीडीएफ निर्यात सेट करें

अब, पीडीएफ निर्यात सेटिंग्स को कॉन्फ़िगर करें। यह उदाहरण दर्शाता है कि लेआउट कैसे सेट करें और यूनिट रूपांतरणों को कैसे संभालें।

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// इकाई प्रणाली की जाँच करें और परिभाषित करें
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// पीडीएफ निर्यात स्थापित करने के लिए आपका कोड यहां दिया गया है
```

## चरण 3: पीडीएफ में निर्यात करें

कॉन्फ़िगर की गई सेटिंग्स का उपयोग करके पीडीएफ में निर्यात निष्पादित करें।

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## चरण 4: रेखापुंज छवियों को निर्यात करें

पीएनजी जैसी रेखापुंज छवियों को निर्यात करने की कार्यक्षमता बढ़ाएँ।

```csharp
// 300 डीपीआई पर ए4 आकार - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि DWG फ़ाइलों को PDF और रैस्टर छवियों दोनों में निर्यात करने के लिए .NET के लिए Aspose.CAD का उपयोग कैसे करें। यह शक्तिशाली लाइब्रेरी प्रक्रिया को सुव्यवस्थित करती है, जिससे यह कुशल और डेवलपर-अनुकूल बन जाती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अपने व्यावसायिक प्रोजेक्ट में .NET के लिए Aspose.CAD का उपयोग कर सकता हूँ?

 A1: हाँ, आप कर सकते हैं। मिलने जाना[buy.aspose.com/buy](https://purchase.aspose.com/buy) लाइसेंसिंग विवरण के लिए.

### Q2: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 ए2: निश्चित रूप से! अपना निःशुल्क परीक्षण प्राप्त करें[यहाँ](https://releases.aspose.com/).

### Q3: मैं .NET के लिए Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 ए3: की ओर जाएं[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन के लिए.

### Q4: क्या मैं परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस प्राप्त कर सकता हूँ?

 उ4: हाँ, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: मुझे विस्तृत दस्तावेज कहां मिल सकते हैं?

 A5: दस्तावेज़ यहां उपलब्ध है[Aspose.CAD](https://reference.aspose.com/cad/net/).