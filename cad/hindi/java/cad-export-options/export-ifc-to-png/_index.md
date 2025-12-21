---
date: 2025-12-21
description: Aspose.CAD for Java के साथ IFC को PNG में आसानी से बदलें। हमारे चरण‑दर‑चरण
  ट्यूटोरियल का पालन करें।
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java के साथ IFC को PNG में बदलें
url: /hi/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java के साथ IFC को PNG में परिवर्तित करें

## परिचय

इस ट्यूटोरियल में आप **IFC को PNG में कैसे परिवर्तित करें** सीखेंगे, जो कि शक्तिशाली Aspose.CAD लाइब्रेरी for Java का उपयोग करता है। चाहे आप एक BIM व्यूअर बना रहे हों, किसी कंस्ट्रक्शन पोर्टल के लिए थंबनेल जेनरेट कर रहे हों, या डॉक्यूमेंटेशन पाइपलाइन को ऑटोमेट कर रहे हों, IFC (Industry Foundation Classes) फ़ाइलों को रास्टर इमेज में बदलना एक सामान्य आवश्यकता है। हम प्रत्येक चरण को विस्तार से देखेंगे, सेटिंग्स के पीछे की तर्क को समझाएंगे, और आपको सर्वोत्तम विज़ुअल परिणाम प्राप्त करने के टिप्स देंगे।

## त्वरित उत्तर
- **कौनसी लाइब्रेरी आवश्यक है?** Aspose.CAD for Java (नि:शुल्क ट्रायल उपलब्ध)।  
- **समर्थित IFC संस्करण?** अधिकांश IFC 2x3 और IFC4 फ़ाइलें संभाली जाती हैं।  
- **सामान्य रूपांतरण समय?** मानक मॉडलों के लिए कुछ सेकंड; फ़ाइल आकार पर निर्भर करता है।  
- **क्या मुझे लाइसेंस चाहिए?** प्रोडक्शन उपयोग के लिए एक अस्थायी लाइसेंस आवश्यक है।  
- **क्या मैं इमेज आकार को अनुकूलित कर सकता हूँ?** हाँ – चौड़ाई और ऊँचाई सेट करने के लिए `CadRasterizationOptions` का उपयोग करें।

## “IFC को PNG में परिवर्तित करना” क्या है?
IFC को PNG में परिवर्तित करना का अर्थ है 3‑D बिल्डिंग मॉडल (IFC) को 2‑D बिटमैप इमेज (PNG) में रास्टराइज़ करना। यह प्रक्रिया ज्यामिति को सपाट करती है, डिफ़ॉल्ट विज़ुअल स्टाइल लागू करती है, और एक पोर्टेबल इमेज बनाती है जिसे ब्राउज़र, रिपोर्ट या मोबाइल ऐप में CAD व्यूअर की आवश्यकता के बिना दिखाया जा सकता है।

## Aspose.CAD for Java का उपयोग क्यों करें?
- **कोई बाहरी CAD सॉफ़्टवेयर नहीं** – शुद्ध Java API, किसी भी प्लेटफ़ॉर्म पर काम करता है।  
- **उच्च‑फ़िडेलिटी रेंडरिंग** – लाइन वेट, रंग और लेयर्स को संरक्षित रखता है।  
- **पूर्ण नियंत्रण** – रास्टराइज़ेशन विकल्प आपको रिज़ॉल्यूशन, बैकग्राउंड आदि निर्धारित करने देते हैं।  
- **आसान लाइसेंसिंग** – ट्रायल और अस्थायी लाइसेंस मूल्यांकन को सरल बनाते हैं।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास है:

- **Aspose.CAD Library** – इसे [download link](https://releases.aspose.com/cad/java/) से डाउनलोड और इंस्टॉल करें।  
- **Java Development Kit (JDK)** – संस्करण 8 या बाद का।  
- **एक फ़ोल्डर** जिसमें वह IFC फ़ाइल हो जिसे आप परिवर्तित करना चाहते हैं।

## Namespaces आयात करें

अपने Java प्रोजेक्ट में आवश्यक क्लासेस आयात करें:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## स्टेप‑बाय‑स्टेप गाइड

### स्टेप 1: IFC फ़ाइल लोड करें

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

यहाँ हम स्रोत IFC फ़ाइल को `IfcImage` ऑब्जेक्ट में लोड करते हैं। Aspose.CAD स्वचालित रूप से IFC संरचना को पार्स करता है और रास्टराइज़ेशन के लिए तैयार करता है।

### स्टेप 2: वेक्टर (रास्टराइज़ेशन) विकल्प सेट करें

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

`CadRasterizationOptions` नियंत्रित करता है कि 3‑D ज्यामिति कैसे सपाट की जाती है। इच्छित PNG रिज़ॉल्यूशन से मेल खाने के लिए `PageWidth` और `PageHeight` समायोजित करें। बड़े मान अधिक‑विवरण वाली इमेज देते हैं लेकिन मेमोरी उपयोग बढ़ाते हैं।

### स्टेप 3: PNG निर्यात सेटिंग्स कॉन्फ़िगर करें

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

`PngOptions` Aspose.CAD को PNG फ़ाइल आउटपुट करने के लिए बताता है और पिछले चरण में परिभाषित रास्टराइज़ेशन सेटिंग्स को जोड़ता है।

### स्टेप 4: इमेज को PNG के रूप में सहेजें

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

`save` मेथड रास्टराइज़्ड इमेज को डिस्क पर लिखता है। इस लाइन के चलने के बाद, आप `example.png` को अपने स्रोत IFC फ़ाइल की समान डायरेक्टरी में पाएँगे।

## सामान्य समस्याएँ और समाधान

| समस्या | क्यों होता है | समाधान |
|-------|----------------|-----|
| **खाली PNG आउटपुट** | रास्टराइज़ेशन विकल्पों की चौड़ाई/ऊँचाई 0 या बहुत छोटी सेट की गई है। | `PageWidth` और `PageHeight` को सकारात्मक पूर्णांक (जैसे 1500) सुनिश्चित करें। |
| **लेयर्स या रंग गायब** | डिफ़ॉल्ट व्यू कुछ लेयर्स को छिपा सकता है। | `vectorOptions.setRenderMode(CadRenderMode.Wireframe)` का उपयोग करें या आवश्यकता अनुसार API के माध्यम से लेयर विज़िबिलिटी समायोजित करें। |
| **बड़े IFC फ़ाइलों के लिए Out‑of‑memory त्रुटियाँ** | बहुत उच्च रिज़ॉल्यूशन बहुत अधिक RAM उपयोग करता है। | रिज़ॉल्यूशन कम करें या मॉडल को सेक्शनों में प्रोसेस करें। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD सभी संस्करणों की IFC फ़ाइलों के साथ संगत है?

Aspose.CAD विभिन्न संस्करणों की IFC फ़ाइलों को समर्थन देता है। संगतता विवरण के लिए [documentation](https://reference.aspose.com/cad/java/) देखें।

### Q2: क्या मैं रास्टराइज़ेशन विकल्पों को और अनुकूलित कर सकता हूँ?

बिल्कुल! उन्नत अनुकूलन विकल्पों के लिए [documentation](https://reference.aspose.com/cad/java/) देखें।

### Q3: क्या ट्रायल संस्करण उपलब्ध है?

हाँ, आप मुफ्त ट्रायल संस्करण [यहाँ](https://releases.aspose.com/) से प्राप्त कर सकते हैं।

### Q4: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त करूँ?

अस्थायी लाइसेंस [इस लिंक](https://purchase.aspose.com/temporary-license/) से प्राप्त करें।

### Q5: मैं मदद कहाँ प्राप्त कर सकता हूँ या समस्याओं पर चर्चा कर सकता हूँ?

समुदाय समर्थन के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

## अतिरिक्त अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं कई IFC फ़ाइलों को बैच में परिवर्तित कर सकता हूँ?**  
**उत्तर:** हाँ। लोडिंग और सहेजने की लॉजिक को एक लूप में रखें जो फ़ाइल पाथ की सूची पर इटररेट करे।

**प्रश्न: PNG की बैकग्राउंड रंग कैसे बदलूँ?**  
**उत्तर:** `PngOptions` बनाने से पहले `vectorOptions.setBackgroundColor(Color.getWhite())` (या कोई भी `java.awt.Color`) सेट करें।

**प्रश्न: क्या JPEG या BMP जैसे अन्य रास्टर फ़ॉर्मेट में निर्यात करना संभव है?**  
**उत्तर:** बिल्कुल। `PngOptions` को `JpegOptions` या `BmpOptions` से बदलें और फ़ॉर्मेट‑विशिष्ट सेटिंग्स को समायोजित करें।

**प्रश्न: क्या रूपांतरण के बाद संसाधनों को रिलीज़ करना आवश्यक है?**  
**उत्तर:** समाप्त होने पर `cadImage.dispose()` कॉल करके नेटिव मेमोरी मुक्त करें।

---

**अंतिम अपडेट:** 2025-12-21  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.12 (लेखन समय पर नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}