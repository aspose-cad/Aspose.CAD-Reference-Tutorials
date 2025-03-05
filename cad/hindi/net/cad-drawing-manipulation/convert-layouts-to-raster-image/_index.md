---
title: .NET के लिए Aspose.CAD में लेआउट को रैस्टर इमेज में बदलें
linktitle: लेआउट को रेखापुंज छवि में बदलें
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का उपयोग करके आसानी से CAD लेआउट को रेखापुंज छवियों में परिवर्तित करें। शक्तिशाली सीएडी हेरफेर क्षमताओं के साथ अपने विकास को बढ़ाएं।
type: docs
weight: 12
url: /hi/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---
## परिचय

क्या आप अपने .NET अनुप्रयोगों में लेआउट को आसानी से रेखापुंज छवियों में परिवर्तित करना चाहते हैं? आगे कोई तलाश नहीं करें! यह चरण-दर-चरण मार्गदर्शिका आपको .NET के लिए Aspose.CAD का उपयोग करके प्रक्रिया के बारे में बताएगी, जो एक शक्तिशाली लाइब्रेरी है जो कंप्यूटर-एडेड डिज़ाइन (CAD) कार्यों को सरल बनाती है।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- .NET लाइब्रेरी के लिए Aspose.CAD: लाइब्रेरी को डाउनलोड और इंस्टॉल करें[.NET डाउनलोड पेज के लिए Aspose.CAD](https://releases.aspose.com/cad/net/).

- विकास परिवेश: सुनिश्चित करें कि आपकी मशीन पर एक कार्यशील .NET विकास परिवेश स्थापित है।

- कनवर्ट करने के लिए दस्तावेज़: एक CAD दस्तावेज़ तैयार करें जिसमें वे लेआउट शामिल हों जिन्हें आप रास्टर छवियों में कनवर्ट करना चाहते हैं।

- आपकी दस्तावेज़ निर्देशिका: कोड में प्लेसहोल्डर "आपकी दस्तावेज़ निर्देशिका" को अपनी दस्तावेज़ निर्देशिका के पथ से बदलें।

## नामस्थान आयात करें

सबसे पहले, आइए आपके कोड में Aspose.CAD कार्यक्षमताओं को सुलभ बनाने के लिए आवश्यक नामस्थान आयात करें।

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## चरण 1: सीएडी दस्तावेज़ लोड करें

Aspose.CAD लाइब्रेरी का उपयोग करके CAD दस्तावेज़ लोड करके प्रारंभ करें।

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //आगे के चरणों के लिए आपका कोड यहां जाएगा
}
```

## चरण 2: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

 का एक उदाहरण बनाएं`CadRasterizationOptions` पृष्ठ की चौड़ाई, ऊंचाई निर्धारित करने और उन लेआउट को निर्दिष्ट करने के लिए जिन्हें आप कनवर्ट करना चाहते हैं।

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## चरण 3: परिणामी छवि के लिए टिफ़ऑप्शंस सेट करें

 का एक उदाहरण बनाएं`TiffOptions`परिणामी छवि के प्रारूप को परिभाषित करने के लिए।

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## चरण 4: परिणामी छवि सहेजें

आउटपुट पथ निर्दिष्ट करें और परिवर्तित छवि को सहेजें।

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.CAD का उपयोग करके CAD लेआउट को रैस्टर छवि प्रारूप में सफलतापूर्वक परिवर्तित कर लिया है। संभावनाएं विशाल हैं, और यह मार्गदर्शिका आपके सीएडी-संबंधित प्रयासों के लिए शुरुआती बिंदु के रूप में कार्य करती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD सभी CAD प्रारूपों के साथ संगत है?

 A1: Aspose.CAD DWG, DXF, DWF, STL और अन्य सहित CAD प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है। जाँचें[प्रलेखन](https://reference.aspose.com/cad/net/) एक व्यापक सूची के लिए.

### Q2: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A2: पर जाएँ[अस्थायी लाइसेंस पृष्ठ](https://purchase.aspose.com/temporary-license/) परीक्षण और मूल्यांकन उद्देश्यों के लिए एक अस्थायी लाइसेंस प्राप्त करना।

### Q3: मुझे Aspose.CAD के लिए समर्थन कहां मिल सकता है?

 उ3: सहायता प्राप्त करने के लिए फ़ोरम एक बेहतरीन स्थान है। दौरा करना[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) समुदाय से जुड़ने और सहायता प्राप्त करने के लिए।

### Q4: क्या मैं Aspose.CAD को मुफ़्त में आज़मा सकता हूँ?

 उ4: बिल्कुल! अपना पकड़ो[मुफ्त परीक्षण](https://releases.aspose.com/) Aspose.CAD की विशेषताओं और क्षमताओं का पता लगाने के लिए।

### Q5: मैं Aspose.CAD के लिए लाइसेंस कहां से खरीद सकता हूं?

 A5: पर नेविगेट करें[खरीद पृष्ठ](https://purchase.aspose.com/buy) लाइसेंस खरीदने और Aspose.CAD की पूरी क्षमता को अनलॉक करने के लिए।