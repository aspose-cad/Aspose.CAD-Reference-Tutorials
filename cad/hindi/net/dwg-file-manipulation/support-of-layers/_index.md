---
title: C# के साथ DWG फ़ाइलों में परतों को संभालना - Aspose.CAD ट्यूटोरियल
linktitle: C# के साथ DWG फ़ाइलों में परतें संभालना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD के साथ C# का उपयोग करके DWG फ़ाइलों में परतों को संभालने का तरीका जानें। कुशल सीएडी फ़ाइल हेरफेर के लिए चरण-दर-चरण मार्गदर्शिका।
weight: 11
url: /hi/net/dwg-file-manipulation/support-of-layers/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# के साथ DWG फ़ाइलों में परतों को संभालना - Aspose.CAD ट्यूटोरियल

## परिचय

.NET के लिए Aspose.CAD के साथ C# का उपयोग करके DWG फ़ाइलों में परतों को संभालने पर हमारे गहन ट्यूटोरियल में आपका स्वागत है। Aspose.CAD एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को CAD फ़ाइल स्वरूपों के साथ निर्बाध रूप से काम करने में सक्षम बनाती है। इस ट्यूटोरियल में, हम आपको चरण दर चरण DWG फ़ाइलों में परतों को संभालने की प्रक्रिया के बारे में मार्गदर्शन देंगे।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- C# प्रोग्रामिंग भाषा का बुनियादी ज्ञान।
- आपकी मशीन पर विज़ुअल स्टूडियो स्थापित है।
-  .NET लाइब्रेरी के लिए Aspose.CAD, जिसे आप यहां से डाउनलोड कर सकते हैं[Aspose.CAD वेबसाइट](https://releases.aspose.com/cad/net/).

## नामस्थान आयात करें

आरंभ करने के लिए, अपने C# प्रोजेक्ट में आवश्यक नामस्थान आयात करें। ये नामस्थान CAD फ़ाइलों के साथ काम करने के लिए आवश्यक कार्यक्षमता प्रदान करते हैं।

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## चरण 1: DWG फ़ाइल लोड करें

Aspose.CAD लाइब्रेरी का उपयोग करके DWG फ़ाइल को अपने C# एप्लिकेशन में लोड करके प्रारंभ करें।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // अगले चरणों के लिए आपका कोड यहां दिया गया है
}
```

## चरण 2: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

 का एक उदाहरण बनाएं`CadRasterizationOptions` और यह परिभाषित करने के लिए इसके गुण सेट करें कि DWG फ़ाइल को कैसे व्यवस्थित किया जाना चाहिए।

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## चरण 3: परतें निर्दिष्ट करें

रैस्टराइज़ेशन विकल्पों में वांछित परतें जोड़ें। इस उदाहरण में, हमने "लेयरए" जोड़ा है।

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## चरण 4: छवि निर्यात विकल्प कॉन्फ़िगर करें

 आवश्यक छवि निर्यात विकल्प बनाएँ. यहाँ, हम उपयोग कर रहे हैं`JpegOptions` JPEG में निर्यात करने के लिए.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

## चरण 5: निर्यात की गई छवि को सहेजें

आउटपुट पथ निर्दिष्ट करें और रैस्टराइज़्ड DWG फ़ाइल को JPEG के रूप में सहेजें।

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

अब आपने .NET के लिए Aspose.CAD के साथ C# का उपयोग करके DWG फ़ाइल में परतों को सफलतापूर्वक संभाल लिया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने C# और Aspose.CAD लाइब्रेरी का उपयोग करके DWG फ़ाइलों में परतों को संभालने की प्रक्रिया के बारे में जाना। इन चरणों का पालन करके, आप अपने .NET अनुप्रयोगों में CAD फ़ाइलों के साथ कुशलतापूर्वक काम कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं एक साथ कई परतों को संभाल सकता हूँ?

 A1: हाँ, आप कर सकते हैं। बस इसमें परत नाम जोड़ें`rasterizationOptions.Layers` सरणी.

### Q2: क्या Aspose.CAD का परीक्षण संस्करण उपलब्ध है?

 उ2: हाँ, आप नि:शुल्क परीक्षण संस्करण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मुझे दस्तावेज़ कहां मिल सकते हैं?

 A3: दस्तावेज़ उपलब्ध है[यहाँ](https://reference.aspose.com/cad/net/).

### Q4: मुझे Aspose.CAD के लिए समर्थन कैसे मिलेगा?

 A4: आप पर समर्थन मांग सकते हैं[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19).

### Q5: Aspose.CAD के लिए लाइसेंसिंग विकल्प क्या हैं?

 A5: आप लाइसेंसिंग विकल्प और खरीदारी विवरण तलाश सकते हैं[यहाँ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
