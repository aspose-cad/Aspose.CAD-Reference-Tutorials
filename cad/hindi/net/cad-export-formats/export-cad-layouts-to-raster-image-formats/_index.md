---
title: .NET के लिए Aspose.CAD में रैस्टर छवि प्रारूपों में CAD लेआउट निर्यात करें
linktitle: रास्टर छवि प्रारूपों में सीएडी लेआउट निर्यात करें
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: जानें कि .NET के लिए Aspose.CAD का उपयोग करके रास्टर छवियों में CAD लेआउट कैसे निर्यात करें। निर्बाध रूपांतरण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 10
url: /hi/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---
## परिचय

क्या आप .NET के लिए Aspose.CAD का उपयोग करके CAD लेआउट को रैस्टर छवि प्रारूपों में कुशलतापूर्वक परिवर्तित करना चाहते हैं? यह चरण-दर-चरण मार्गदर्शिका आपको प्रक्रिया के बारे में बताएगी, कार्य को सहज बनाने के लिए विस्तृत निर्देश और कोड स्निपेट प्रदान करेगी। चाहे आप एक अनुभवी डेवलपर हों या Aspose.CAD में नए हों, यह ट्यूटोरियल विशेषज्ञता के सभी स्तरों को पूरा करता है।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- .NET लाइब्रेरी के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास Aspose.CAD लाइब्रेरी स्थापित है। यदि नहीं, तो आप इसे यहां से डाउनलोड कर सकते हैं[Aspose.CAD वेबसाइट](https://releases.aspose.com/cad/net/).

- सीएडी ड्राइंग फ़ाइल: एक सीएडी ड्राइंग फ़ाइल तैयार करें (उदाहरण के लिए, conic_pyramid.dxf) जिसे आप रैस्टर छवि प्रारूपों में कनवर्ट करना चाहते हैं।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.CAD कार्यक्षमताओं का लाभ उठाने के लिए आवश्यक नामस्थान आयात करें। अपने कोड की शुरुआत में निम्नलिखित नामस्थान शामिल करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## चरण 1: सीएडी ड्राइंग लोड करें

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// छवि के एक उदाहरण में CAD ड्राइंग लोड करें
using (var image = Image.Load(sourceFilePath))
{
    // सीएडी ड्राइंग लोड करने के लिए आपका कोड यहां दिया गया है
}
```

## चरण 2: कैडरास्टराइज़ेशन विकल्प बनाएं

```csharp
// CadRasterizationOptions का एक उदाहरण बनाएं
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## चरण 3: परतें निर्दिष्ट करें

```csharp
// परत का नाम CadRasterizationOptions की परत सूची में जोड़ें
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## चरण 4: JpegOptions बनाएं

```csharp
// JpegOptions (या रेखापुंज प्रारूपों के लिए कोई ImageOptions) का एक उदाहरण बनाएं
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## चरण 5: जेपीईजी प्रारूप में निर्यात करें

```csharp
// प्रत्येक परत को Jpeg प्रारूप में निर्यात करें
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## अतिरिक्त चरण: सभी परतों को परिवर्तित करें

यदि आप सभी परतों को परिवर्तित करना चाहते हैं, तो निम्न विधि का उपयोग करें:

```csharp
ConvertAllLayersToRasterImageFormats();
```

यह विधि सीएडी ड्राइंग में सभी परतों पर पुनरावृत्ति करती है, प्रत्येक परत को एक अलग जेपीईजी फ़ाइल में निर्यात करती है।

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि .NET के लिए Aspose.CAD का उपयोग करके CAD लेआउट को रेखापुंज छवि प्रारूपों में कैसे निर्यात किया जाए। यह ट्यूटोरियल सीएडी रूपांतरण के लिए कुशल और विश्वसनीय समाधान चाहने वाले डेवलपर्स के लिए एक व्यापक मार्गदर्शिका प्रदान करता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं निर्यात के लिए अन्य छवि प्रारूपों का उपयोग कर सकता हूँ?

 A1: हाँ, आप कर सकते हैं। बस बदलें`JpegOptions` वांछित प्रारूप के विकल्पों के साथ, जैसे`PngOptions` या`BmpOptions`.

### Q2: क्या कोई परीक्षण संस्करण उपलब्ध है?

 उ2: हां, आप परीक्षण संस्करण डाउनलोड करके Aspose.CAD की कार्यक्षमता का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A3: Aspose.CAD पर जाएँ[मंच](https://forum.aspose.com/c/cad/19) सामुदायिक सहायता के लिए या समर्पित सहायता के लिए लाइसेंस खरीदने पर विचार करें।

### Q4: क्या अस्थायी लाइसेंस उपलब्ध हैं?

 उ4: हाँ, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: मुझे दस्तावेज़ कहां मिल सकते हैं?

 A5: विस्तृत दस्तावेज़ देखें[यहाँ](https://reference.aspose.com/cad/net/).