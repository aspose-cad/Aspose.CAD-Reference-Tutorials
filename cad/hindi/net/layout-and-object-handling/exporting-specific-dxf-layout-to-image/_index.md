---
title: छवि में विशिष्ट DXF लेआउट निर्यात करना - Aspose.CAD ट्यूटोरियल
linktitle: छवि में विशिष्ट DXF लेआउट निर्यात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: छवियों में विशिष्ट DXF लेआउट निर्यात करने के लिए .NET के लिए Aspose.CAD का उपयोग करने पर चरण-दर-चरण मार्गदर्शिका देखें। इस शक्तिशाली ट्यूटोरियल के साथ अपनी .NET विकास दक्षता को अधिकतम करें।
type: docs
weight: 10
url: /hi/net/layout-and-object-handling/exporting-specific-dxf-layout-to-image/
---
## परिचय

.NET विकास के क्षेत्र में, Aspose.CAD कंप्यूटर-एडेड डिज़ाइन (CAD) फ़ाइलों को संभालने के लिए एक शक्तिशाली उपकरण के रूप में सामने आता है। विशेष रूप से, यह छवियों में विशिष्ट DXF लेआउट निर्यात करने के लिए व्यापक कार्यक्षमता प्रदान करता है। यह ट्यूटोरियल आपको चरण दर चरण प्रक्रिया के माध्यम से मार्गदर्शन करेगा, जिससे आप आसानी से Aspose.CAD की क्षमताओं का उपयोग कर सकेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  Aspose.CAD लाइब्रेरी: Aspose.CAD लाइब्रेरी को डाउनलोड और इंस्टॉल करें[रिलीज पेज](https://releases.aspose.com/cad/net/).

- विकास परिवेश: सुनिश्चित करें कि आपकी मशीन पर .NET विकास परिवेश स्थापित है।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.CAD द्वारा प्रदान की गई कार्यक्षमताओं तक पहुँचने के लिए आवश्यक नामस्थान आयात करके प्रारंभ करें:

```csharp
using System;
```

## चरण 1: अपना प्रोजेक्ट सेट करें

एक नया .NET प्रोजेक्ट बनाएं या मौजूदा प्रोजेक्ट खोलें जहां आप Aspose.CAD कार्यक्षमता को लागू करने की योजना बना रहे हैं।

## चरण 2: CAD छवि लोड करें

अपने निर्दिष्ट फ़ाइल पथ से CAD छवि लोड करने के लिए निम्नलिखित कोड का उपयोग करें:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (var image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // आगे के चरणों के लिए आपका कोड यहां जाएगा।
}
```

## चरण 3: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

पृष्ठ की चौड़ाई और ऊंचाई निर्दिष्ट करते हुए रेखापुंज विकल्प सेट करें:

```csharp
var rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## चरण 4: परतों पर पुनरावृति करें

CAD छवि से परतें पुनर्प्राप्त करें और उनके माध्यम से पुनरावृत्त करें:

```csharp
var layersList = image.Layers;
foreach (var layerName in layersList.GetLayersNames())
{
    // आगे के चरणों के लिए आपका कोड यहां जाएगा।
}
```

## चरण 5: छवियों में परतें निर्यात करें

प्रत्येक परत के लिए, कॉन्फ़िगर विकल्पों का उपयोग करके इसे JPEG छवि में निर्यात करें:

```csharp
rasterizationOptions.Layers = new string[] { layerName };
var options = new Aspose.CAD.ImageOptions.JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
image.Save(layerName + "_out.jpg", options);
```

CAD छवि में प्रत्येक परत के लिए इन चरणों को दोहराएँ।

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि .NET वातावरण में Aspose.CAD का उपयोग करके विशिष्ट DXF लेआउट को छवियों में कैसे निर्यात किया जाए। इस ट्यूटोरियल ने आपको इस शक्तिशाली लाइब्रेरी से अधिकतम लाभ उठाने के लिए आवश्यक कदमों से सुसज्जित किया है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य .NET फ्रेमवर्क के साथ Aspose.CAD का उपयोग कर सकता हूँ?

A1: हां, Aspose.CAD विभिन्न .NET फ्रेमवर्क के साथ संगत है, जो आपकी विकास आवश्यकताओं के लिए लचीलापन प्रदान करता है।

### Q2: क्या Aspose.CAD के लिए अस्थायी लाइसेंस उपलब्ध हैं?

 उ2: हां, आप Aspose.CAD के लिए अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q3: मैं Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A3: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और सहायता प्राप्त करने के लिए।

### Q4: क्या Aspose.CAD के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

 उ4: हाँ, आप Aspose.CAD का निःशुल्क परीक्षण देख सकते हैं[यहाँ](https://releases.aspose.com/).

### Q5: मुझे Aspose.CAD के लिए विस्तृत दस्तावेज़ कहां मिल सकते हैं?

 A5: व्यापक का संदर्भ लें[Aspose.CAD दस्तावेज़ीकरण](https://reference.aspose.com/cad/net/) गहन जानकारी के लिए.