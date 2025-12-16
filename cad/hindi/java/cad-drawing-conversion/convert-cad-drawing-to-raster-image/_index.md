---
date: 2025-12-16
description: Aspose.CAD for Java के साथ CAD को PNG में कैसे बदलें, सीखें, जिसमें DWG
  को इमेज में निर्यात करना, CAD को PNG के रूप में सहेजना, और CAD को रास्टर इमेज विकल्प
  शामिल हैं।
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java का उपयोग करके CAD को PNG में कैसे परिवर्तित करें
url: /hi/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java का उपयोग करके CAD को PNG में कैसे बदलें

आधुनिक इंजीनियरिंग कार्यप्रवाहों में, आपको अक्सर **CAD को PNG में बदलने** की आवश्यकता होती है ताकि ड्रॉइंग्स को ब्राउज़र में दिखाया जा सके, दस्तावेज़ों में एम्बेड किया जा सके, या उन हितधारकों के साथ साझा किया जा सके जिनके पास CAD सॉफ़्टवेयर नहीं है। यह ट्यूटोरियल आपको पूरी प्रक्रिया के माध्यम से ले जाता है— CAD फ़ाइल को लोड करने से लेकर उच्च‑गुणवत्ता वाले PNG रास्टर इमेज को एक्सपोर्ट करने तक— Java के लिए शक्तिशाली Aspose.CAD लाइब्रेरी का उपयोग करके।

## त्वरित उत्तर
- **मुख्य उद्देश्य क्या है?** CAD ड्रॉइंग्स को PNG रास्टर इमेज में बदलना।  
- **कौन सी लाइब्रेरी उपयोग की जाती है?** Aspose.CAD for Java।  
- **क्या मुझे लाइसेंस चाहिए?** एक मुफ्त ट्रायल उपलब्ध है; उत्पादन उपयोग के लिए लाइसेंस आवश्यक है।  
- **क्या मैं इमेज आकार को कस्टमाइज़ कर सकता हूँ?** हाँ, `CadRasterizationOptions` का उपयोग करके चौड़ाई और ऊँचाई सेट करें।  
- **समर्थित CAD फ़ॉर्मैट्स?** DWG, DXF, DWF, और कई अन्य।

## CAD को PNG में बदलना क्या है?
CAD को PNG में बदलना का अर्थ है वेक्टर‑आधारित CAD सामग्री (DWG, DXF, आदि) को पिक्सेल‑आधारित इमेज फ़ॉर्मेट में रास्टराइज़ करना। PNG पारदर्शिता और लॉसलेस क्वालिटी को बनाए रखता है, जिससे यह वेब प्रीव्यू, दस्तावेज़ीकरण, और रिपोर्टिंग के लिए आदर्श है।

## CAD को PNG (CAD से रास्टर इमेज) में क्यों बदलें?
- **सर्वव्यापी दृश्यता:** PNG किसी भी डिवाइस पर विशेष CAD व्यूअर्स की आवश्यकता के बिना काम करता है।  
- **तेज़ लोडिंग:** रास्टर इमेज वेब पेजों में तुरंत लोड होते हैं।  
- **आसान एम्बेडिंग:** PNG को PDF, Word दस्तावेज़, या स्लाइड डेक में डालें।  
- **सुसंगत रूप:** लाइन वेट, रंग, और लेयर्स को बिल्कुल वैसा ही रखें जैसा डिज़ाइन किया गया है।

## पूर्वापेक्षाएँ
शुरू करने से पहले, सुनिश्चित करें कि आपके पास है:
1. **Java Development Environment** – JDK 8 या उससे नया स्थापित और कॉन्फ़िगर किया हुआ।  
2. **Aspose.CAD Library** – लाइब्रेरी डाउनलोड करके अपने प्रोजेक्ट में जोड़ें। आप लाइब्रेरी **[here](https://releases.aspose.com/cad/java/)** पर पा सकते हैं।

## नेमस्पेस इम्पोर्ट करें
अपनी Java क्लास में आवश्यक इम्पोर्ट जोड़ें ताकि आप Aspose.CAD ऑब्जेक्ट्स के साथ काम कर सकें।

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## CAD को PNG में बदलने के लिए चरण-दर-चरण गाइड

### चरण 1: CAD ड्रॉइंग लोड करें
सबसे पहले, `Image.load()` का उपयोग करके स्रोत CAD फ़ाइल (DXF, DWG, आदि) लोड करें।

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

> **प्रो टिप:** पाथ समस्याओं से बचने के लिए अपने CAD फ़ाइलों को एक समर्पित फ़ोल्डर (जैसे, `CADConversion`) में रखें।

### चरण 2: रास्टराइज़ेशन विकल्प सेट करें (dwg को इमेज में एक्सपोर्ट करें)
आउटपुट इमेज का आकार और अन्य रास्टर सेटिंग्स निर्धारित करें।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

यदि आवश्यक हो तो आप यहाँ बैकग्राउंड रंग, लाइन रेंडर मोड, और DPI को भी नियंत्रित कर सकते हैं।

### चरण 3: इमेज विकल्प बनाएं (cad को png के रूप में सहेजें)
`PngOptions` का एक इंस्टेंस बनाएं और रास्टराइज़ेशन सेटिंग्स संलग्न करें।

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### चरण 4: रास्टर इमेज सहेजें (cad फ़ाइल को png में) 
अंत में, PNG फ़ाइल को डिस्क पर लिखें।

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

परिणामी फ़ाइल `conic_pyramid_raster_image_out.png` आपके मूल CAD ड्रॉइंग का उच्च‑रिज़ॉल्यूशन PNG प्रतिनिधित्व है।

### अन्य फ़ाइलों के लिए दोहराएँ
`srcFile` को किसी अन्य CAD फ़ाइल की ओर इंगित करने के लिए बदलें और वही चरण चलाएँ। वही कोड DWG, DWF, और अन्य समर्थित फ़ॉर्मैट्स के लिए काम करता है।

## सामान्य समस्याएँ और समाधान
| Issue | Solution |
|-------|----------|
| **खाली PNG आउटपुट** | सुनिश्चित करें कि स्रोत CAD फ़ाइल सही ढंग से लोड हो (`Image.load()` को कोई अपवाद नहीं फेंकना चाहिए)। |
| **गलत आयाम** | `PageWidth` / `PageHeight` को समायोजित करें या DPI को `rasterizationOptions.setResolution(...)` के माध्यम से सेट करें। |
| **लेयर्स गायब** | सुनिश्चित करें कि CAD फ़ाइल की लेयर्स छिपी नहीं हैं; `CadRasterizationOptions.setDrawType(CadDrawTypeMode.Vector);` का उपयोग करें। |
| **लाइसेंस त्रुटियाँ** | एक वैध Aspose.CAD लाइसेंस फ़ाइल उपयोग करें (`License license = new License(); license.setLicense("Aspose.CAD.lic");`)। |

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या Aspose.CAD सभी CAD फ़ॉर्मैट्स के साथ संगत है?**  
A1: Aspose.CAD कई CAD फ़ॉर्मैट्स को सपोर्ट करता है, जिसमें DWG, DXF, DWF, और अधिक शामिल हैं। पूर्ण सूची के लिए **[documentation](https://reference.aspose.com/cad/java/)** देखें।

**Q2: क्या मैं अपनी विशिष्ट आवश्यकताओं के लिए रास्टराइज़ेशन विकल्प कस्टमाइज़ कर सकता हूँ?**  
A2: हाँ, Aspose.CAD रास्टराइज़ेशन विकल्प सेट करने में लचीलापन प्रदान करता है, जिससे आप आउटपुट को अपनी आवश्यकताओं (आकार, DPI, बैकग्राउंड रंग, आदि) के अनुसार अनुकूलित कर सकते हैं।

**Q3: Aspose.CAD‑संबंधी प्रश्नों के लिए समर्थन कहाँ मिल सकता है?**  
A3: सहायता प्राप्त करने और समुदाय के साथ जुड़ने के लिए **[Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19)** पर जाएँ।

**Q4: क्या Aspose.CAD for Java के लिए मुफ्त ट्रायल उपलब्ध है?**  
A4: हाँ, आप **[यहाँ](https://releases.aspose.com/)** एक मुफ्त ट्रायल प्राप्त करके Aspose.CAD की सुविधाओं का अन्वेषण कर सकते हैं।

**Q5: मैं Aspose.CAD for Java कैसे खरीद सकता हूँ?**  
A5: Aspose.CAD for Java खरीदने के लिए, **[purchase page](https://purchase.aspose.com/buy)** पर जाएँ।

---

**अंतिम अद्यतन:** 2025-12-16  
**परीक्षण किया गया संस्करण:** Aspose.CAD for Java 24.11 (लेखन समय पर नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}