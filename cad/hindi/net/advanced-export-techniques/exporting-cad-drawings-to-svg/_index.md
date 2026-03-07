---
date: 2026-03-07
description: Aspose.CAD for .NET का उपयोग करके CAD को SVG में निर्यात करना सीखें,
  SVG का रंग अनुकूलित करें, और DWG को प्रभावी ढंग से SVG में बदलें।
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD को SVG में निर्यात करें – CAD ड्रॉइंग्स को SVG फ़ॉर्मेट में निर्यात करना
  - Aspose.CAD गाइड
url: /hi/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD को SVG में निर्यात करें – CAD ड्रॉइंग्स को SVG फ़ॉर्मेट में निर्यात करना

## परिचय

वेब पेज, रिपोर्ट या इंटरैक्टिव विज़ुअलाइज़ेशन के लिए रिज़ॉल्यूशन‑इंडिपेंडेंट ग्राफ़िक्स की आवश्यकता होने पर CAD ड्रॉइंग्स को SVG में निर्यात करना एक सामान्य आवश्यकता है। इस ट्यूटोरियल में आप Aspose.CAD for .NET के साथ **how to export CAD to SVG** सीखेंगे, **customize SVG color** विकल्पों का अन्वेषण करेंगे, और केवल कुछ कोड लाइनों में **convert DWG to SVG** (या DXF to SVG) कैसे किया जाता है, देखेंगे। कदम तेज़ हैं, API सहज है, और उत्पन्न SVG फ़ाइलें किसी भी डिवाइस पर पूरी तरह से स्केल करती हैं।

## त्वरित उत्तर
- **What library handles the conversion?** Aspose.CAD for .NET.  
- **Can I change the color mode?** Yes – use `SvgColorMode` to set grayscale, black‑white, or full‑color.  
- **Which CAD formats are supported?** DWG, DXF, and many others (see Aspose.CAD docs).  
- **Do I need a license for development?** A temporary license is available for testing.  
- **How long does the conversion take?** Typically under a second for standard drawings.

## “export CAD to SVG” क्या है?
Export CAD to SVG का अर्थ है एक मूल CAD फ़ाइल (जैसे DWG या DXF) को लेकर उसे Scalable Vector Graphics फ़ॉर्मेट में रेंडर करना। SVG XML‑आधारित, हल्का, और CSS के साथ स्टाइल किया जा सकता है—जिससे यह आधुनिक वेब और मोबाइल एप्लिकेशन के लिए आदर्श बनता है।

## CAD को SVG में निर्यात करने के लिए Aspose.CAD क्यों उपयोग करें?
- **No external dependencies** – शुद्ध .NET API, AutoCAD इंस्टॉलेशन की आवश्यकता नहीं।  
- **Fine‑grained control** – आप **customize SVG color** कर सकते हैं, तय कर सकते हैं कि टेक्स्ट को शेप्स के रूप में रखा जाए, और रास्टराइज़ेशन विकल्प चुन सकते हैं।  
- **Broad format support** – वही कोड **convert DWG to SVG**, **convert DXF to SVG** और अन्य फ़ॉर्मेट्स के लिए काम करता है, जिससे आपका कोड बेस सरल हो जाता है।  
- **High performance** – गति और कम मेमोरी उपयोग के लिए अनुकूलित, बैच प्रोसेसिंग के लिए उपयुक्त।

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास है:

- **Aspose.CAD for .NET** स्थापित है। आप लाइब्रेरी [here](https://releases.aspose.com/cad/net/) से डाउनलोड कर सकते हैं।  
- एक .NET विकास वातावरण (Visual Studio, Rider, या .NET CLI)।  
- एक CAD फ़ाइल (DWG या DXF) जिसे आप परिवर्तित करना चाहते हैं।

## नेमस्पेस आयात करें

सबसे पहले, आवश्यक नेमस्पेस को अपने प्रोजेक्ट में लाएँ ताकि क्लासेज उपलब्ध हों।

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## स्टेप‑बाय‑स्टेप गाइड

### स्टेप 1: डॉक्यूमेंट डायरेक्टरी सेट करें  
उस फ़ोल्डर को परिभाषित करें जहाँ आपका स्रोत CAD फ़ाइल स्थित है और जहाँ SVG आउटपुट सहेजा जाएगा।

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### स्टेप 2: CAD ड्रॉइंग लोड करें  
`Image.Load` का उपयोग करके DWG (या DXF) फ़ाइल पढ़ें। यह **load DWG .NET** परिदृश्यों के लिए काम करता है।

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### स्टेप 3: SVG निर्यात विकल्प कॉन्फ़िगर करें  
निर्यात सेटिंग्स को अपनी आवश्यकताओं के अनुसार समायोजित करें। यहाँ हम रंग मोड को ग्रेस्केल सेट करते हैं और सभी टेक्स्ट को वेक्टर शेप्स के रूप में रेंडर करने के लिए मजबूर करते हैं।

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### स्टेप 4: SVG फ़ाइल सहेजें  
अंत में, SVG फ़ाइल को डिस्क पर लिखें। यह स्टेप **saves CAD as SVG** है और परिवर्तन को पूरा करता है।

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

इन चार संक्षिप्त चरणों का पालन करके, आप आउटपुट की उपस्थिति पर पूर्ण नियंत्रण के साथ **convert DWG to SVG** (या **convert DXF to SVG**) कर सकते हैं।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|-------|-----|
| **Blank SVG output** | स्रोत फ़ाइल पथ गलत है या फ़ाइल भ्रष्ट है। | `MyDir` को सत्यापित करें और सुनिश्चित करें कि CAD फ़ाइल बिना त्रुटियों के खुलती है। |
| **Colors look wrong** | `SvgColorMode` अनजाने में ग्रेस्केल पर सेट है। | मूल रंगों को बनाए रखने के लिए `options.ColorType` को `SvgColorMode.FullColor` में बदलें। |
| **Text missing** | `TextAsShapes` को `false` पर सेट किया गया है और व्यूअर एम्बेडेड फ़ॉन्ट्स को सपोर्ट नहीं करता। | `TextAsShapes = true` रखें या SVG में आवश्यक फ़ॉन्ट्स एम्बेड करें। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD सभी CAD फ़ॉर्मेट्स के साथ संगत है?
A1: Aspose.CAD विभिन्न CAD फ़ॉर्मेट्स का समर्थन करता है, जिसमें DWG और DXF शामिल हैं, जिससे व्यापक संगतता सुनिश्चित होती है।

### Q2: क्या मैं SVG में निर्यात करते समय रंग मोड को कस्टमाइज़ कर सकता हूँ?
A2: हाँ, Aspose.CAD आपको रंग मोड चुनने की अनुमति देता है, जिससे आउटपुट में लचीलापन मिलता है।

### Q3: क्या परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस उपलब्ध हैं?
A3: हाँ, आप मूल्यांकन के लिए एक अस्थायी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

### Q4: मैं Aspose.CAD के विस्तृत दस्तावेज़ कहाँ पा सकता हूँ?
A4: दस्तावेज़ [here](https://reference.aspose.com/cad/net/) पर उपलब्ध है।

### Q5: मैं Aspose.CAD से संबंधित समर्थन कैसे प्राप्त कर सकता हूँ या प्रश्न पूछ सकता हूँ?
A5: समर्थन और चर्चा के लिए समुदाय फ़ोरम [here](https://forum.aspose.com/c/cad/19) पर जाएँ।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं इस कोड को .NET Core या .NET 6 के साथ उपयोग कर सकता हूँ?**  
A: बिल्कुल। Aspose.CAD for .NET .NET Framework, .NET Core, और .NET 5/6+ के साथ संगत है।

**Q: क्या केवल एक विशिष्ट लेआउट या लेयर को निर्यात करना संभव है?**  
A: हाँ। सहेजने से पहले `SvgOptions` का उपयोग करके `PageIndex` सेट करें या लेयर्स को फ़िल्टर करें।

**Q: उत्पन्न SVG में कस्टम CSS स्टाइल्स कैसे एम्बेड करूँ?**  
A: सहेजने के बाद, आप SVG XML को पोस्ट‑प्रोसेस करके `<style>` एलिमेंट्स जोड़ सकते हैं, या नए संस्करणों में उपलब्ध होने पर `options.CustomCss` का उपयोग कर सकते हैं।

**Q: स्रोत CAD फ़ाइल के लिए आकार सीमाएँ क्या हैं?**  
A: लाइब्रेरी बड़े फ़ाइलों को संभालती है, लेकिन जटिलता के साथ मेमोरी उपयोग बढ़ता है। बहुत बड़े ड्रॉइंग्स के लिए, पृष्ठों को व्यक्तिगत रूप से प्रोसेस करने पर विचार करें।

**Q: क्या परिवर्तन लाइन वेट्स और लाइन टाइप्स को संरक्षित करता है?**  
A: डिफ़ॉल्ट रूप से, लाइन वेट्स संरक्षित रहते हैं। आप अधिक सूक्ष्म नियंत्रण के लिए `SvgOptions` में रेंडरिंग विकल्प समायोजित कर सकते हैं।

---

**अंतिम अपडेट:** 2026-03-07  
**परीक्षित संस्करण:** Aspose.CAD for .NET 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}