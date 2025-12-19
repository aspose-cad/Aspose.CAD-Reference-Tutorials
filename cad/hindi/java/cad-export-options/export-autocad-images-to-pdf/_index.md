---
date: 2025-12-19
description: AutoCAD PDF को Aspose.CAD for Java का उपयोग करके निर्यात करना सीखें।
  यह चरण-दर-चरण गाइड दिखाता है कि DWG को PDF में कैसे बदलें, CAD को PDF के रूप में
  कैसे सहेजें, और लाइसेंसिंग को कैसे संभालें।
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: AutoCAD PDF निर्यात - Aspose.CAD for Java ट्यूटोरियल के साथ AutoCAD छवियों
  को PDF में निर्यात करें
url: /hi/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export AutoCAD PDF - Aspose.CAD for Java के साथ AutoCAD इमेज को PDF में निर्यात करें

## परिचय

क्या आप Java का उपयोग करके **AutoCAD PDF निर्यात** करना चाहते हैं? आगे देखिए! इस ट्यूटोरियल में हम Aspose.CAD for Java का उपयोग करके AutoCAD इमेज को PDF में बदलने की प्रक्रिया को चरण‑दर‑चरण समझाएंगे, जो **DWG को PDF में बदलना** आसान बनाता है। अंत तक आप जानेंगे कि **CAD को PDF के रूप में सहेजें**, कस्टम रास्टराइज़ेशन सेटिंग्स कैसे लागू करें, और प्रोडक्शन उपयोग के लिए Aspose.CAD लाइसेंस के साथ कैसे काम करें।

## त्वरित उत्तर
- **क्या मैं Java से DWG को PDF में बदल सकता हूँ?** हाँ, Aspose.CAD for Java DWG, DXF और कई अन्य फॉर्मैट को सपोर्ट करता है।  
- **क्या लाइसेंस की आवश्यकता है?** अनलिमिटेड उपयोग के लिए **Aspose CAD लाइसेंस** आवश्यक है; मूल्यांकन के लिए एक टेम्पररी लाइसेंस उपलब्ध है।  
- **कौन सा Java संस्करण समर्थित है?** Java 8+ (लाइब्रेरी सभी आधुनिक JDK के साथ संगत है)।  
- **क्या मैं PDF पेज साइज कस्टमाइज़ कर सकता हूँ?** बिल्कुल – रास्टराइज़ेशन विकल्पों में `pageWidth` और `pageHeight` को समायोजित करें।  
- **क्या 3‑D रास्टराइज़ेशन संभव है?** हाँ, पूर्ण 3‑D रेंडरिंग के लिए `TypeOfEntities.Entities3D` को सक्षम करें।

## **export autocad pdf** क्या है?
AutoCAD PDF निर्यात का अर्थ है वेक्टर‑आधारित CAD ड्रॉइंग्स (DWG, DXF, DWF आदि) को एक पोर्टेबल PDF दस्तावेज़ में बदलना, जबकि लेयर्स, लाइन वेट्स और वैकल्पिक रूप से 3‑D जियोमेट्री को संरक्षित रखना। यह क्लाइंट्स के साथ डिज़ाइन साझा करने, आर्काइविंग या बिना CAD सॉफ़्टवेयर के प्रिंट करने के लिए उपयोगी है।

## Aspose.CAD for Java के साथ **export autocad pdf** क्यों उपयोग करें?
- **पूर्ण फॉर्मैट समर्थन** – DWG, DXF, DWF और कई अन्य फॉर्मैट्स के साथ काम करता है।  
- **कोई बाहरी निर्भरताएँ नहीं** – शुद्ध Java लाइब्रेरी, कोई नेटिव DLL नहीं।  
- **उच्च‑गुणवत्ता रास्टराइज़ेशन** – DPI, पेज साइज और लेआउट पर नियंत्रण।  
- **लाइसेंस लचीलापन** – मुफ्त ट्रायल से शुरू करें, फिर स्थायी **Aspose CAD लाइसेंस** में अपग्रेड करें।  

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास है:

- **Java विकास वातावरण** – JDK 8 या उसके बाद का संस्करण स्थापित हो।  
- **Aspose.CAD for Java लाइब्रेरी** – [डाउनलोड लिंक](https://releases.aspose.com/cad/java/) से डाउनलोड करें।  
- **डॉक्यूमेंट डायरेक्टरी** – आपके मशीन पर एक फ़ोल्डर जहाँ स्रोत CAD फ़ाइलें और उत्पन्न PDF रखे जाएंगे।

## नेमस्पेस इम्पोर्ट करें

अपने Java प्रोजेक्ट में Aspose.CAD के साथ काम करने के लिए आवश्यक क्लासेज़ इम्पोर्ट करें:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

अब कोड को चरण‑दर‑चरण देखें।

## चरण‑दर‑चरण गाइड

### चरण 1: रिसोर्स डायरेक्टरी पाथ सेट करें

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **प्रो टिप:** `"Your Document Directory"` को उस फ़ोल्डर के पूर्ण पाथ से बदलें जिसे आपने पूर्वापेक्षाओं में बनाया था।

### चरण 2: CAD इमेज लोड करें

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **यह क्यों महत्वपूर्ण है:** CAD फ़ाइल को `Image` ऑब्जेक्ट में लोड करने से आपको Aspose.CAD के रास्टराइज़ेशन इंजन तक पूरी पहुँच मिलती है।

### चरण 3: रास्टराइज़ेशन विकल्प सेट करें

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- आउटपुट PDF का आकार बदलने के लिए `pageWidth` और `pageHeight` को समायोजित करें।  
- यदि आपको 3‑D एंटिटीज़ के लिए **java convert cad pdf** चाहिए तो `setTypeOfEntities` लाइन को अनकमेंट करें।  
- `setLayouts` कॉल यह निर्धारित करता है कि कौन सा लेआउट (Model, Layout1, आदि) रेंडर किया जाएगा।

### चरण 4: PDF विकल्प कॉन्फ़िगर करें

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

यह रास्टराइज़ेशन सेटिंग्स को PDF आउटपुट से जोड़ता है, जिससे वेक्टर डेटा सही ढंग से परिवर्तित हो सके।

### चरण 5: PDF सहेजें

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

परिणामी फ़ाइल, `Export3DImagestoPDF_out_.pdf`, आपके मूल AutoCAD ड्रॉइंग का **save cad as pdf** प्रतिनिधित्व है।

## सामान्य समस्याएँ और समाधान

| लक्षण | संभावित कारण | समाधान |
|---------|--------------|-----|
| खाली PDF आउटपुट | रास्टराइज़ेशन विकल्प सेट नहीं हैं या लेआउट मेल नहीं खा रहा | `setLayouts` को अपने CAD फ़ाइल के लेआउट नाम से मिलाएँ। |
| कम‑रिज़ॉल्यूशन इमेज | `pageWidth`/`pageHeight` बहुत छोटा है | आयाम बढ़ाएँ या `rasterizationOptions.setResolution(...)` से उच्च DPI सेट करें। |
| लाइसेंस एक्सेप्शन | वैध लाइसेंस लागू नहीं किया गया | **Aspose CAD लाइसेंस** लागू करें या परीक्षण के लिए टेम्पररी लाइसेंस उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.CAD for Java को अन्य CAD फ़ाइल फॉर्मैट्स के साथ उपयोग कर सकता हूँ?
A1: हाँ, Aspose.CAD DWG, DWF, DGN और कई अन्य फॉर्मैट्स को सपोर्ट करता है, जिससे आपके प्रोजेक्ट्स में लचीलापन आता है।

### Q2: Aspose.CAD for Java के लिए टेम्पररी लाइसेंस कैसे प्राप्त करूँ?
A2: मूल्यांकन के लिए टेम्पररी लाइसेंस प्राप्त करने हेतु [यहाँ](https://purchase.aspose.com/temporary-license/) जाएँ।

### Q3: रास्टराइज़ेशन के लिए कोई लेआउट विकल्प हैं?
A3: हाँ, आप `setLayouts` मेथड के माध्यम से लेआउट (जैसे `"Model"`, `"Layout1"`) को कस्टमाइज़ कर सकते हैं ताकि इच्छित व्यू रेंडर हो।

### Q4: क्या मैं आउटपुट PDF फ़ाइल का आकार कस्टमाइज़ कर सकता हूँ?
A4: बिल्कुल! रास्टराइज़ेशन विकल्पों में `pageWidth` और `pageHeight` पैरामीटर को अपनी इच्छित डाइमेंशन के अनुसार समायोजित करें।

### Q5: Aspose.CAD for Java से संबंधित मदद या चर्चा के लिए मैं कहाँ जा सकता हूँ?
A5: समर्पित सपोर्ट और कम्युनिटी चर्चा के लिए [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) पर जाएँ।

---

**आखिरी अपडेट:** 2025-12-19  
**टेस्टेड संस्करण:** Aspose.CAD for Java 24.10  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}