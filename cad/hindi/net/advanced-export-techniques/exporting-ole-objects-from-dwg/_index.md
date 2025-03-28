---
title: DWG फ़ाइलों से OLE ऑब्जेक्ट निर्यात करना - Aspose.CAD ट्यूटोरियल
linktitle: DWG फ़ाइलों से OLE ऑब्जेक्ट निर्यात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का उपयोग करके DWG फ़ाइलों से OLE ऑब्जेक्ट निर्यात करने पर चरण-दर-चरण मार्गदर्शिका देखें। अपने CAD फ़ाइल हेरफेर कौशल को सहजता से बढ़ाएं।
weight: 12
url: /hi/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG फ़ाइलों से OLE ऑब्जेक्ट निर्यात करना - Aspose.CAD ट्यूटोरियल

## परिचय

क्या आप DWG फ़ाइलों से OLE ऑब्जेक्ट आसानी से निकालना चाह रहे हैं? .NET के लिए Aspose.CAD आपके लिए प्रक्रिया को सुव्यवस्थित करने के लिए यहां है। इस ट्यूटोरियल में, हम चरण दर चरण OLE ऑब्जेक्ट निर्यात करने में आपका मार्गदर्शन करेंगे, यह सुनिश्चित करते हुए कि आप इस शक्तिशाली .NET लाइब्रेरी का अधिकतम लाभ उठा सकें। 

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET लाइब्रेरी के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास लाइब्रेरी स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[.NET डाउनलोड पेज के लिए Aspose.CAD](https://releases.aspose.com/cad/net/).

-  दस्तावेज़ निर्देशिका: एक निर्देशिका स्थापित करें जहाँ आपकी DWG फ़ाइलें संग्रहीत हैं। प्रतिस्थापित करें`"Your Document Directory"` वास्तविक पथ के साथ दिए गए कोड स्निपेट में।

## नामस्थान आयात करें

आपके .NET प्रोजेक्ट में, आपको Aspose.CAD कार्यक्षमताओं का लाभ उठाने के लिए आवश्यक नामस्थान आयात करने की आवश्यकता होगी। निम्नलिखित कोड स्निपेट का उपयोग करें:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

```csharp
string MyDir = "Your Document Directory";
```

 प्रतिस्थापित करें`"Your Document Directory"` उस पथ के साथ जहां आपकी DWG फ़ाइलें स्थित हैं।

## चरण 2: DWG फ़ाइलें निर्दिष्ट करें

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

उन DWG फ़ाइलों को सूचीबद्ध करें जिन्हें आप सरणी के भीतर संसाधित करना चाहते हैं।

## चरण 3: निर्यात विकल्प कॉन्फ़िगर करें

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

अपनी आवश्यकताओं के आधार पर निर्यात विकल्पों को अनुकूलित करें। इस उदाहरण में, हम पीएनजी निर्यात को एक निर्दिष्ट लेआउट के साथ कॉन्फ़िगर करते हैं।

## चरण 4: फ़ाइलों के माध्यम से पुनरावृति करें और निर्यात करें

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

निर्दिष्ट DWG फ़ाइलों के माध्यम से पुनरावृति करें, प्रत्येक को लोड करें, और निर्यातित PNG फ़ाइल को परिभाषित विकल्पों के साथ सहेजें।

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.CAD का उपयोग करके DWG फ़ाइलों से OLE ऑब्जेक्ट सफलतापूर्वक निर्यात कर लिया है। यह शक्तिशाली लाइब्रेरी जटिल कार्यों को सरल बनाती है, सीएडी फ़ाइल हेरफेर में दक्षता और लचीलापन प्रदान करती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या .NET के लिए Aspose.CAD जूनियर और सीनियर दोनों CAD फ़ाइलों के लिए उपयुक्त है?

A1: हाँ, .NET के लिए Aspose.CAD बहुमुखी है और कनिष्ठ और वरिष्ठ दोनों प्रकार सहित CAD फ़ाइलों की एक विस्तृत श्रृंखला को संभाल सकता है।

### Q2: क्या मैं विभिन्न लेआउट के लिए निर्यात विकल्पों को अनुकूलित कर सकता हूँ?

ए2: बिल्कुल! जैसा कि ट्यूटोरियल में दिखाया गया है, आप अपनी विशिष्ट आवश्यकताओं के अनुरूप लेआउट सहित निर्यात विकल्पों को तैयार कर सकते हैं।

### Q3: मुझे .NET के लिए Aspose.CAD के लिए विस्तृत दस्तावेज़ कहां मिल सकते हैं?

 ए3: अन्वेषण करें[.NET दस्तावेज़ीकरण के लिए Aspose.CAD](https://reference.aspose.com/cad/net/) गहन जानकारी और उदाहरणों के लिए।

### Q4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 A4: हाँ, आप निःशुल्क परीक्षण के साथ .NET के लिए Aspose.CAD की क्षमताओं का अनुभव कर सकते हैं। मिलने जाना[इस लिंक](https://releases.aspose.com/) प्रारंभ करना।

### Q5: मैं समुदाय से समर्थन कैसे प्राप्त कर सकता हूं या उससे कैसे जुड़ सकता हूं?

 A5: समर्थन और सामुदायिक सहभागिता के लिए, पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
