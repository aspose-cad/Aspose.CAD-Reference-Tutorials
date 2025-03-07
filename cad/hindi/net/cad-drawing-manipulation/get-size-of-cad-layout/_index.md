---
title: .NET के लिए Aspose.CAD में CAD लेआउट का आकार प्राप्त करें
linktitle: सीएडी लेआउट का आकार प्राप्त करें
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: जानें कि Aspose.CAD का उपयोग करके .NET में CAD लेआउट आकार कैसे प्राप्त करें। कुशल सीएडी फ़ाइल हेरफेर के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 14
url: /hi/net/cad-drawing-manipulation/get-size-of-cad-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.CAD में CAD लेआउट का आकार प्राप्त करें

## परिचय

.NET के लिए Aspose.CAD का उपयोग करके CAD लेआउट का आकार प्राप्त करने पर इस व्यापक मार्गदर्शिका में आपका स्वागत है। Aspose.CAD एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को CAD फ़ाइलों के साथ निर्बाध रूप से काम करने में सक्षम बनाती है। इस ट्यूटोरियल में, हम आपको व्यावहारिक उदाहरणों और चरण-दर-चरण निर्देशों का उपयोग करके सीएडी लेआउट के आकार को पुनर्प्राप्त करने की प्रक्रिया के बारे में बताएंगे।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास Aspose.CAD लाइब्रेरी स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[.NET डाउनलोड पेज के लिए Aspose.CAD](https://releases.aspose.com/cad/net/).

- दस्तावेज़ फ़ाइलें: वे CAD फ़ाइलें तैयार करें जिनके साथ आप काम करना चाहते हैं। यह ट्यूटोरियल उदाहरण के रूप में "conic_pyramid.dxf" और "Bottom_plate.dwg" का उपयोग करता है।

अब, चलिए शुरू करें!

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, आवश्यक नामस्थान आयात करके प्रारंभ करें:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

 अपनी दस्तावेज़ निर्देशिका के लिए पथ सेट करें. प्रतिस्थापित करें`"Your Document Directory"` वास्तविक पथ के साथ.

```csharp
string MyDir = "Your Document Directory";
```

## चरण 2: CAD फ़ाइल पथ निर्दिष्ट करें

CAD फ़ाइल पथों की एक सरणी परिभाषित करें जिसका आप विश्लेषण करना चाहते हैं। इस उदाहरण में, हम "conic_pyramid.dxf" और "Bottom_plate.dwg" का उपयोग करते हैं।

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## चरण 3: CAD फ़ाइलों के माध्यम से पुनरावृति करें

प्रत्येक सीएडी फ़ाइल के माध्यम से पुनरावृति करें और लेआउट जानकारी पुनः प्राप्त करें।

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (अगले कदम के लिए आगे बढ़ें)
    }
}
```

## चरण 4: गैर-रिक्त लेआउट प्राप्त करें

CAD फ़ाइल प्रकार के आधार पर गैर-रिक्त लेआउट प्राप्त करने के लिए एक सहायक विधि परिभाषित करें।

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (अगले कदम के लिए आगे बढ़ें)
}
```

## चरण 5: DWG फ़ाइलों के लिए लेआउट प्राप्त करें

DWG फ़ाइलों के लिए गैर-रिक्त लेआउट पुनर्प्राप्त करने के लिए तर्क लागू करें।

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (अगले कदम के लिए आगे बढ़ें)
}
```

## चरण 6: DXF फ़ाइलों के लिए लेआउट प्राप्त करें

DXF फ़ाइलों के लिए गैर-रिक्त लेआउट पुनर्प्राप्त करने के लिए तर्क लागू करें।

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (अगले कदम के लिए आगे बढ़ें)
}
```

## चरण 7: लेआउट आकार प्राप्त करें और छवि के रूप में सहेजें

लेआउट आकार प्राप्त करने और इसे एक छवि के रूप में सहेजने की प्रक्रिया पूरी करें।

```csharp
foreach (string layout in layouts)
{
    // ... (अगले कदम के लिए आगे बढ़ें)
}
```

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि .NET के लिए Aspose.CAD का उपयोग करके CAD लेआउट का आकार कैसे प्राप्त किया जाए। इस ट्यूटोरियल में आपके प्रोजेक्ट को सेट करने से लेकर लेआउट जानकारी प्राप्त करने और इसे एक छवि के रूप में सहेजने तक आवश्यक कदम शामिल हैं। अब आप कुशल CAD फ़ाइल हेरफेर के लिए इस ज्ञान को अपने .NET अनुप्रयोगों में शामिल कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD सभी CAD फ़ाइल स्वरूपों के साथ संगत है?

A1: हाँ, Aspose.CAD DWG और DXF सहित विभिन्न CAD फ़ाइल स्वरूपों का समर्थन करता है।

### Q2: क्या मैं छवि-बचत विकल्पों को अनुकूलित कर सकता हूँ?

ए2: बिल्कुल! आप अपनी विशिष्ट आवश्यकताओं को पूरा करने के लिए छवि विकल्पों, जैसे प्रारूप और रिज़ॉल्यूशन को समायोजित कर सकते हैं।

### Q3: मुझे अतिरिक्त दस्तावेज़ कहां मिल सकते हैं?

 A3: का संदर्भ लें[Aspose.CAD दस्तावेज़ीकरण](https://reference.aspose.com/cad/net/) विस्तृत जानकारी और उदाहरणों के लिए.

### Q4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 A4: हां, आप Aspose.CAD को a के साथ एक्सप्लोर कर सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/).

### Q5; मुझे तकनीकी सहायता कैसे मिल सकती है?

 A5: तकनीकी सहायता के लिए, पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
