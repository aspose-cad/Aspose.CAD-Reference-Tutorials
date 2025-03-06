---
title: आईएफसी फाइलों को पीएनजी में निर्यात करना - Aspose.CAD ट्यूटोरियल
linktitle: आईएफसी फाइलों को पीएनजी में निर्यात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का अन्वेषण करें, जो निर्बाध IFC से PNG रूपांतरण के लिए एक मजबूत समाधान है। कुशल CAD फ़ाइल प्रोसेसिंग के लिए अभी डाउनलोड करें।
weight: 10
url: /hi/net/exporting-to-image-formats/exporting-ifc-files-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# आईएफसी फाइलों को पीएनजी में निर्यात करना - Aspose.CAD ट्यूटोरियल

## परिचय

कंप्यूटर-एडेड डिज़ाइन (सीएडी) की गतिशील दुनिया में, कुशल फ़ाइल रूपांतरण महत्वपूर्ण है। .NET के लिए Aspose.CAD एक शक्तिशाली उपकरण के रूप में उभरता है, जो IFC (इंडस्ट्री फाउंडेशन क्लासेस) फ़ाइलों को PNG प्रारूप में निर्यात करने के लिए निर्बाध क्षमताएं प्रदान करता है। यह चरण-दर-चरण ट्यूटोरियल Aspose.CAD के साथ एक सहज अनुभव सुनिश्चित करते हुए, प्रक्रिया में आपका मार्गदर्शन करेगा।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

### 1. Aspose.CAD इंस्टालेशन

 सुनिश्चित करें कि आपके पास .NET के लिए Aspose.CAD स्थापित है। आप इसे रिलीज़ पेज से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

### 2. दस्तावेज़ निर्देशिका

 अपने दस्तावेज़ों के लिए एक निर्दिष्ट निर्देशिका बनाएँ। दिए गए उदाहरण में, वेरिएबल`MyDir` दस्तावेज़ निर्देशिका का प्रतिनिधित्व करता है।

## नामस्थान आयात करें

अब जब आपके पास पूर्वापेक्षाएँ सेट हो गई हैं, तो आइए Aspose.CAD कार्यात्मकताओं का उपयोग करने के लिए अपने .NET एप्लिकेशन में आवश्यक नेमस्पेस आयात करें।

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## चरण 1: IFC फ़ाइल लोड करें

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

 इस चरण में, हम Aspose.CAD को आरंभ करते हैं`IfcImage` ऑब्जेक्ट करें और उसमें IFC फ़ाइल लोड करें।

## चरण 2: रैस्टराइज़ेशन विकल्प सेट करें

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

पीएनजी आउटपुट के लिए पृष्ठ की चौड़ाई और ऊंचाई को कॉन्फ़िगर करने के लिए रेखापुंज विकल्पों को परिभाषित करें।

## चरण 3: पीएनजी विकल्प सेट करें

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

पीएनजी विकल्प बनाएं और पहले से परिभाषित रास्टराइज़ेशन विकल्पों को संबद्ध करें।

## चरण 4: आउटपुट पथ निर्दिष्ट करें

```csharp
    // आउटपुट पथ भी सेट करें
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

पीएनजी फ़ाइल के लिए आउटपुट पथ को परिभाषित करें, यह सुनिश्चित करते हुए कि इसका नाम ".png" एक्सटेंशन वाली स्रोत फ़ाइल के समान है। अंत में, परिवर्तित छवि को सहेजें।

## निष्कर्ष

इन सरल चरणों के साथ, आपने .NET के लिए Aspose.CAD का उपयोग करके एक IFC फ़ाइल को PNG में सफलतापूर्वक निर्यात कर लिया है। यह बहुमुखी उपकरण CAD रूपांतरण प्रक्रिया को सरल बनाता है, जिससे यह डेवलपर्स और इंजीनियरों के लिए सुलभ हो जाता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं macOS या Linux पर .NET के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: नहीं, .NET के लिए Aspose.CAD विशेष रूप से Windows वातावरण के लिए डिज़ाइन किया गया है।

### Q2: क्या परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस उपलब्ध है?

 उ2: हां, आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/) मूल्यांकन के लिए।

### Q3: मैं Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A3: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और चर्चा के लिए।

### Q4: मुझे व्यापक दस्तावेज कहां मिल सकते हैं?

 A4: का संदर्भ लें[Aspose.CAD दस्तावेज़ीकरण](https://reference.aspose.com/cad/net/) विस्तृत जानकारी और उदाहरणों के लिए.

### Q5: यदि इंस्टालेशन के दौरान मुझे समस्याएँ आती हैं तो क्या होगा?

 A5: दस्तावेज़ की जाँच करें या सहायता लें[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
