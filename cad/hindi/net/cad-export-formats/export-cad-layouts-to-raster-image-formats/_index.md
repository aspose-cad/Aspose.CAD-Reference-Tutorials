---
date: 2026-03-21
description: Aspose.CAD for .NET का उपयोग करके dxf को png और अन्य रास्टर फ़ॉर्मैट
  में कैसे बदलें, सीखें। सहज CAD लेयर निर्यात के लिए हमारी चरण‑दर‑चरण गाइड का पालन
  करें।
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET के साथ DXF को PNG में बदलें
url: /hi/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET में CAD लेआउट को रास्टर इमेज फ़ॉर्मैट में निर्यात करें

## परिचय

क्या आप Aspose.CAD for .NET का उपयोग करके **convert dxf to png** और अन्य रास्टर इमेज फ़ॉर्मैट को प्रभावी ढंग से बदलना चाहते हैं? यह चरण‑दर‑चरण गाइड आपको प्रक्रिया के माध्यम से ले जाएगा, विस्तृत निर्देश और कोड स्निपेट प्रदान करेगा ताकि कार्य सहज हो सके। चाहे आप एक अनुभवी डेवलपर हों या Aspose.CAD में नए हों, यह ट्यूटोरियल सभी स्तरों के विशेषज्ञता को ध्यान में रखता है।

### त्वरित उत्तर
- **कौन सा लाइब्रेरी रूपांतरण को संभालता है?** Aspose.CAD for .NET  
- **डिफ़ॉल्ट रूप से समर्थित प्रमुख फ़ॉर्मैट?** JPEG, PNG, BMP, and TIFF raster images  
- **क्या मैं विशिष्ट CAD लेयर्स को निर्यात कर सकता हूँ?** Yes – use `CadRasterizationOptions.Layers` to target individual layers  
- **उत्पादन के लिए लाइसेंस आवश्यक है?** A valid Aspose.CAD license is required for non‑trial use  
- **समर्थित .NET संस्करण?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## **convert dxf to png** क्या है?

DXF (Drawing Exchange Format) फ़ाइल को PNG में बदलना मतलब वेक्टर‑आधारित CAD डेटा को पिक्सेल‑आधारित इमेज में रास्टराइज़ करना है। यह तब उपयोगी होता है जब आपको CAD ड्रॉइंग को वेब पेज, रिपोर्ट या किसी भी ऐसे वातावरण में एम्बेड करना हो जो केवल रास्टर ग्राफिक्स का समर्थन करता हो।

## CAD लेयर्स को अलग‑अलग निर्यात क्यों करें?

CAD लेयर्स को व्यक्तिगत रूप से निर्यात करने से आपको दृश्य आउटपुट पर सूक्ष्म नियंत्रण मिलता है, प्रत्येक इमेज का फ़ाइल आकार घटता है, और आप लेयर‑विशिष्ट स्टाइलिंग या पोस्ट‑प्रोसेसिंग लागू कर सकते हैं। यह विशेष रूप से बड़े इंजीनियरिंग ड्रॉइंग्स के लिए उपयोगी है जहाँ केवल कुछ लेयर्स किसी विशेष दर्शकों के लिए प्रासंगिक होती हैं।

## पूर्वापेक्षाएँ

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- **Aspose.CAD for .NET Library** – इसे [Aspose.CAD website](https://releases.aspose.com/cad/net/) से डाउनलोड करें।  
- **CAD Drawing File** – एक DXF फ़ाइल (उदा., `conic_pyramid.dxf`) जिसे आप रास्टर फ़ॉर्मैट में बदलना चाहते हैं।  

## Namespaces आयात करें

अपने .NET प्रोजेक्ट में, Aspose.CAD कार्यक्षमताओं का उपयोग करने के लिए आवश्यक namespaces आयात करें। अपने कोड की शुरुआत में निम्नलिखित namespaces शामिल करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## **convert dxf to png** कैसे करें – चरण‑दर‑चरण गाइड

### चरण 1: CAD ड्रॉइंग लोड करें

पहले, DXF फ़ाइल को `Image` ऑब्जेक्ट में लोड करें। यह ऑब्जेक्ट मेमोरी में पूरे CAD ड्रॉइंग को दर्शाता है।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### चरण 2: `CadRasterizationOptions` बनाएं

आउटपुट आयाम और रिज़ॉल्यूशन जैसे रास्टराइज़ेशन सेटिंग्स को कॉन्फ़िगर करें। ये विकल्प नियंत्रित करते हैं कि वेक्टर डेटा कैसे रास्टराइज़ किया जाता है।

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### चरण 3: लेयर्स निर्दिष्ट करें (CAD लेयर्स निर्यात)

यदि आपको केवल एक विशेष लेयर चाहिए, तो यहाँ उसका नाम सूचीबद्ध करें। यह **export cad layers** को व्यक्तिगत रूप से दर्शाता है।

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### चरण 4: इमेज फ़ॉर्मैट चुनें – CAD को PNG (या JPEG) के रूप में सहेजें

एक इमेज‑फ़ॉर्मैट‑विशिष्ट विकल्प ऑब्जेक्ट बनाएं। जब आप **save cad as png** करना चाहते हैं तो `JpegOptions` को `PngOptions` से बदलें।

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** PNG फ़ाइलें बनाने के लिए, बस `new PngOptions()` को इंस्टैंशिएट करें, `JpegOptions` के बजाय।

### चरण 5: JPEG (या PNG) फ़ॉर्मैट में निर्यात करें

अंत में, रास्टराइज़्ड इमेज को डिस्क पर सहेजें। फ़ाइल एक्सटेंशन आउटपुट फ़ॉर्मैट निर्धारित करता है।

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

जब आप `JpegOptions` को `PngOptions` से बदलते हैं, तो वही कोड **convert dxf to png** करेगा और एक `.png` फ़ाइल उत्पन्न करेगा।

### अतिरिक्त चरण: सभी लेयर्स को बदलें

यदि आपको ड्रॉइंग की प्रत्येक लेयर के लिए **convert cad to raster** करने की आवश्यकता है, तो नीचे दिया गया हेल्पर मेथड कॉल करें। यह सभी लेयर्स पर इटररेट करता है और प्रत्येक को अलग इमेज के रूप में सहेजता है।

```csharp
ConvertAllLayersToRasterImageFormats();
```

*Note:* `ConvertAllLayersToRasterImageFormats` का इम्प्लीमेंटेशन पूर्ण Aspose.CAD सैंपल सूट का हिस्सा है और लेयर्स की बैच प्रोसेसिंग को दर्शाता है।

## सामान्य समस्याएँ और ट्रबलशूटिंग

| लक्षण | संभावित कारण | समाधान |
|---------|--------------|-----|
| खाली या सफ़ेद इमेज | रास्टराइज़ेशन विकल्प सेट नहीं हैं (जैसे, `PageWidth`/`PageHeight` = 0) | `PageWidth` और `PageHeight` के मान सकारात्मक हों, यह सुनिश्चित करें |
| लेयर्स गायब | `Layers` एरे में लेयर नाम गलत है | CAD फ़ाइल में सटीक लेयर नाम (केस‑सेंसिटिव) की जाँच करें |
| कम गुणवत्ता वाला PNG | डिफ़ॉल्ट DPI कम है | उच्च गुणवत्ता के लिए `rasterizationOptions.Resolution = 300;` सेट करें |

## अक्सर पूछे जाने वाले प्रश्न (Original)

### Q1: क्या मैं निर्यात के लिए अन्य इमेज फ़ॉर्मैट का उपयोग कर सकता हूँ?
A1: हाँ, आप कर सकते हैं। बस `JpegOptions` को इच्छित फ़ॉर्मैट के विकल्पों से बदलें, जैसे `PngOptions` या `BmpOptions`।

### Q2: क्या कोई ट्रायल संस्करण उपलब्ध है?
A2: हाँ, आप Aspose.CAD की कार्यक्षमता को ट्रायल संस्करण डाउनलोड करके यहाँ [here](https://releases.aspose.com/) से देख सकते हैं।

### Q3: मैं Aspose.CAD के लिए सपोर्ट कैसे प्राप्त कर सकता हूँ?
A3: समुदाय समर्थन के लिए Aspose.CAD [forum](https://forum.aspose.com/c/cad/19) पर जाएँ या समर्पित समर्थन के लिए लाइसेंस खरीदने पर विचार करें।

### Q4: क्या टेम्पररी लाइसेंस उपलब्ध हैं?
A4: हाँ, आप टेम्पररी लाइसेंस यहाँ से प्राप्त कर सकते हैं [here](https://purchase.aspose.com/temporary-license/)।

### Q5: दस्तावेज़ीकरण कहाँ मिल सकता है?
A5: विस्तृत दस्तावेज़ीकरण के लिए यहाँ देखें [here](https://reference.aspose.com/cad/net/)।

## अतिरिक्त FAQ

**Q: क्या मैं सभी लेयर्स को एक कमांड में निर्यात कर सकता हूँ?**  
A: हाँ, ऊपर दिखाए गए `ConvertAllLayersToRasterImageFormats` मेथड का उपयोग करें।

**Q: क्या Aspose.CAD SVG जैसे वेक्टर फ़ॉर्मैट को सपोर्ट करता है?**  
A: यह मुख्यतः रास्टर फ़ॉर्मैट को लक्ष्य करता है, लेकिन आप PDF में निर्यात कर सकते हैं जो वेक्टर डेटा को बनाए रखता है।

**Q: निर्यात किए गए PNG की बैकग्राउंड रंग कैसे नियंत्रित करूँ?**  
A: सहेजने से पहले `rasterizationOptions.BackgroundColor` को इच्छित `Color` पर सेट करें।

**Q: क्या पूरे ड्रॉइंग के बजाय एकल लेआउट निर्यात करना संभव है?**  
A: हाँ, `rasterizationOptions.Layouts` को कॉन्फ़िगर करके आप वह लेआउट नाम(नाम) निर्दिष्ट कर सकते हैं जिसे आप रास्टराइज़ करना चाहते हैं।

## निष्कर्ष

अब आपने सीख लिया है कि Aspose.CAD for .NET का उपयोग करके **convert dxf to png**, **export cad layers**, और **save cad as png** या JPEG कैसे किया जाता है। `CadRasterizationOptions` को समायोजित करके और इमेज‑फ़ॉर्मैट विकल्पों को बदलकर, आप रूपांतरण को लगभग किसी भी रास्टर आउटपुट के अनुसार अनुकूलित कर सकते हैं। Aspose.CAD API में अन्य फ़ॉर्मैट विकल्पों का अन्वेषण करें ताकि आपका CAD‑to‑raster वर्कफ़्लो विस्तृत हो सके।

---

**अंतिम अपडेट:** 2026-03-21  
**परीक्षण किया गया:** Aspose.CAD for .NET 24.11 (लेखन समय पर नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}