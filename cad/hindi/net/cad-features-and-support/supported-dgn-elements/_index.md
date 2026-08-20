---
date: 2026-03-29
description: Aspose.CAD for .NET का उपयोग करके DGN को PNG में कैसे बदलें, सीखें। यह
  गाइड CAD फ़ाइल फ़ॉर्मेट समर्थन और समर्थित DGN तत्वों के पूर्ण सेट को भी कवर करता
  है।
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET के साथ DGN को PNG में बदलें
url: /hi/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET के साथ DGN को PNG में बदलें

## परिचय

क्या आप एक .NET डेवलपर हैं जो **DGN को PNG में** सहजता से बदलना चाहते हैं? Aspose.CAD for .NET DGN फ़ाइलों को कुशलतापूर्वक संभालने के लिए एक मजबूत समाधान प्रदान करता है। इस ट्यूटोरियल में, हम समर्थित DGN तत्वों में गहराई से जाएंगे, आपको Aspose.CAD for .NET के साथ काम करने की प्रक्रिया के माध्यम से मार्गदर्शन करेंगे और दिखाएंगे कि इन तत्वों को PNG छवियों में कैसे निर्यात किया जाए।

## त्वरित उत्तर
- **Aspose.CAD क्या करता है?** यह CAD/BIM फ़ाइलों (जिसमें DGN शामिल है) को PNG जैसे रास्टर फ़ॉर्मेट में पढ़ता, संशोधित करता और परिवर्तित करता है।  
- **क्या मैं 2D और 3D DGN तत्वों को बदल सकता हूँ?** हाँ – दोनों 2‑D और 3‑D इकाइयों का समर्थन किया जाता है।  
- **कौन से .NET संस्करण आवश्यक हैं?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **क्या परीक्षण के लिए लाइसेंस चाहिए?** एक मुफ्त ट्रायल उपलब्ध है; उत्पादन के लिए लाइसेंस आवश्यक है।  
- **लाइब्रेरी कहाँ से प्राप्त करें?** इसे आधिकारिक Aspose साइट से डाउनलोड करें (नीचे लिंक)।

## “DGN को PNG में बदलना” क्या है?
DGN को PNG में बदलना का अर्थ है वेक्टर‑आधारित DGN ड्राइंग (2‑D या 3‑D) को रास्टर इमेज फ़ॉर्मेट (PNG) में रेंडर करना। यह तब उपयोगी होता है जब आपको वेब पर CAD ड्रॉइंग दिखानी हों, रिपोर्ट में एम्बेड करनी हों, या CAD व्यूअर की आवश्यकता के बिना थंबनेल बनाना हो।

## CAD फ़ाइल फ़ॉर्मेट समर्थन के लिए Aspose.CAD for .NET क्यों उपयोग करें?
- **पूर्ण CAD फ़ाइल फ़ॉर्मेट समर्थन** – DGN, DWG, DXF, DWF, और अधिक।  
- **कोई बाहरी निर्भरताएँ नहीं** – शुद्ध .NET लाइब्रेरी, कोई नेटिव CAD इंस्टॉलेशन नहीं।  
- **उच्च‑गुणवत्ता रेंडरिंग** – लाइन वेट, रंग, और 3‑D ज्योमेट्री को संरक्षित रखता है।  
- **बैच प्रोसेसिंग** – सर्वर‑साइड एप्लिकेशन में कई फ़ाइलों को आसानी से लूप किया जा सकता है।

## आवश्यकताएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- .NET प्रोग्रामिंग का बुनियादी ज्ञान।  
- आपके मशीन पर Visual Studio स्थापित हो।  
- Aspose.CAD for .NET लाइब्रेरी, जिसे आप [यहाँ](https://releases.aspose.com/cad/net/) डाउनलोड कर सकते हैं।

## नेमस्पेस आयात करें

अपने प्रोजेक्ट को शुरू करने के लिए, आवश्यक नेमस्पेस को अपने .NET एप्लिकेशन में आयात करें। यह चरण सुनिश्चित करता है कि आपको Aspose.CAD for .NET द्वारा प्रदान की गई कार्यक्षमताओं तक पहुंच प्राप्त हो।

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## DGN को PNG में कैसे बदलें

नीचे एक चरण‑दर‑चरण गाइड है जो आपको DGN फ़ाइल लोड करने, उसके तत्वों को इटररेट करने, 2‑D और 3‑D दोनों इकाइयों को संभालने, और अंत में परिणाम को PNG रास्टर इमेज में निर्यात करने की प्रक्रिया से गुजराता है।

### चरण 1: DGN फ़ाइल लोड करें

अपने .NET एप्लिकेशन में एक मौजूदा DGN फ़ाइल को `DgnImage` के रूप में लोड करके शुरू करें।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### चरण 2: DGN तत्वों के माध्यम से इटररेट करें

`foreach` लूप का उपयोग करके DGN तत्वों के माध्यम से इटररेट करें। Aspose.CAD for .NET विभिन्न प्रकार के DGN तत्व प्रदान करता है जिनके साथ आप काम कर सकते हैं।

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### चरण 3: पहले समर्थित 2‑D इकाइयों को संभालें

ये इकाइयाँ अब 3‑D रेंडरिंग के लिए भी समर्थित हैं। स्विच स्टेटमेंट आपको तत्व प्रकार के आधार पर लॉजिक को शाखाबद्ध करने की अनुमति देता है।

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### चरण 4: समर्थित 3‑D इकाइयों को संभालें

Aspose.CAD कई 3‑D DGN तत्वों के लिए पूर्ण समर्थन जोड़ता है। आवश्यकतानुसार उन्हें प्रोसेस करने के लिए स्विच को विस्तारित करें।

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### चरण 5: PNG के रूप में निर्यात करें और सहेजें

किसी भी आवश्यक परिवर्तन के बाद, DGN ड्रॉइंग को PNG रास्टर इमेज में निर्यात करें और निर्दिष्ट डायरेक्टरी में सहेजें।

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **प्रो टिप:** रिज़ॉल्यूशन, बैकग्राउंड रंग, और अन्य PNG‑विशिष्ट सेटिंग्स को नियंत्रित करने के लिए `Image.Save` को `new PngOptions()` के साथ उपयोग करें।

## CAD फ़ाइल फ़ॉर्मेट समर्थन अवलोकन

Aspose.CAD for .NET केवल DGN तक सीमित नहीं है। यह DWG, DXF, DWF, और कई अन्य CAD फ़ॉर्मेट का भी समर्थन करता है, जिससे आप एक ही API के साथ विभिन्न इंजीनियरिंग ड्रॉइंग को संभाल सकते हैं। यह कई मानकों में **CAD फ़ाइल फ़ॉर्मेट समर्थन** की आवश्यकता वाले प्रोजेक्ट्स के लिए आदर्श बनाता है।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|--------|-----|
| **छवि खाली दिखाई देती है** | शून्य DPI के साथ निर्यात किया गया | `PngOptions` में `ResolutionX` और `ResolutionY` निर्दिष्ट करें। |
| **3‑D ज्योमेट्री गायब है** | स्विच में तत्व प्रकार को संभाला नहीं गया | गायब `DgnElementType` केस जोड़ें और तदनुसार रेंडर करें। |
| **बड़ी फ़ाइलों पर मेमोरी समाप्त** | पूरी फ़ाइल को एक साथ लोड करना | तत्वों को बैच में प्रोसेस करें या जहाँ संभव हो स्ट्रीमिंग का उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: Aspose.CAD for .NET की दस्तावेज़ीकरण कहाँ मिल सकती है?
A1: आप दस्तावेज़ीकरण [यहाँ](https://reference.aspose.com/cad/net/) पा सकते हैं।

### Q2: Aspose.CAD for .NET कैसे डाउनलोड करें?
A2: आप लाइब्रेरी [यहाँ](https://releases.aspose.com/cad/net/) डाउनलोड कर सकते हैं।

### Q3: क्या Aspose.CAD for .NET के लिए मुफ्त ट्रायल उपलब्ध है?
A3: हाँ, आप मुफ्त ट्रायल [यहाँ](https://releases.aspose.com/) तक पहुँच सकते हैं।

### Q4: Aspose.CAD for .NET के लिए अस्थायी लाइसेंस कहाँ प्राप्त करें?
A4: अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) उपलब्ध हैं।

### Q5: सहायता चाहिए या कोई प्रश्न हैं?
A5: Aspose.CAD for .NET समुदाय [समर्थन फ़ोरम](https://forum.aspose.com/c/cad/19) पर जाएँ।

---

**अंतिम अद्यतन:** 2026-03-29  
**परीक्षण किया गया:** Aspose.CAD for .NET 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}