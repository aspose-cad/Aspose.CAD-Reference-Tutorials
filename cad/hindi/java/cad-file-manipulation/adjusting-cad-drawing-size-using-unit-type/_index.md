---
date: 2025-12-25
description: Aspose.CAD for Java का उपयोग करके DWG को BMP में निर्यात करना सीखें।
  यह चरण-दर-चरण गाइड CAD ड्राइंग का आकार समायोजित करने और CAD को BMP में कुशलतापूर्वक
  परिवर्तित करने को दर्शाता है।
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: DWG को BMP में निर्यात करें – यूनिट टाइप का उपयोग करके CAD आकार समायोजित करें
  (Java)
url: /hi/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG को BMP में निर्यात करें – Aspose.CAD for Java के साथ Unit Type का उपयोग करके CAD ड्रॉइंग आकार समायोजित करना

## परिचय

जब आपको **export DWG to BMP** करना हो, आउटपुट आकार और माप इकाई को नियंत्रित करना डाउनस्ट्रीम प्रोसेसिंग या प्रिंटिंग के लिए आवश्यक है। इस ट्यूटोरियल में आप सीखेंगे कि Aspose.CAD for Java के साथ CAD ड्रॉइंग आकार कैसे समायोजित करें और CAD को BMP में कैसे परिवर्तित करें, `UnitType` प्रॉपर्टी का उपयोग करके माप इकाई को परिभाषित किया जाता है। चरणों को सरल भाषा में समझाया गया है, इसलिए आप लाइब्रेरी में नए हों तो भी इसे आसानी से फॉलो कर सकते हैं।

## त्वरित उत्तर
- **What does “export DWG to BMP” mean?** DWG ड्रॉइंग को BMP रास्टर इमेज में परिवर्तित करना।  
- **Which property controls the output size?** `CadRasterizationOptions.setUnitType()` इकाई सेट करता है (जैसे, centimeter).  
- **Do I need a license to run the code?** मूल्यांकन के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए लाइसेंस आवश्यक है।  
- **Can I choose other layouts?** हाँ, `setLayouts()` का उपयोग करके मॉडल या पेपर स्पेस लेआउट निर्दिष्ट कर सकते हैं।  
- **What output formats are supported?** BMP के अलावा, आप विकल्प क्लास को बदलकर PNG, JPEG, TIFF आदि में निर्यात कर सकते हैं।

## क्या है **export DWG to BMP**?

DWG को BMP में निर्यात करना मतलब एक वेक्टर‑आधारित DWG फ़ाइल को बिटमैप इमेज (BMP) में रास्टराइज़ करना है। यह तब उपयोगी होता है जब आपको लेगेसी सिस्टम, इमेज प्रोसेसिंग पाइपलाइन, या सरल डिस्प्ले परिदृश्यों के लिए पिक्सेल‑परफेक्ट प्रतिनिधित्व चाहिए।

## क्यों समायोजित करें CAD ड्रॉइंग आकार **Unit Type** के साथ?

Unit Type सेट करने से आप निर्यात की गई इमेज के भौतिक आयामों को मैन्युअल स्केलिंग फ़ैक्टर की गणना किए बिना नियंत्रित कर सकते हैं। यह सुनिश्चित करता है कि बिटमैप वास्तविक दुनिया के माप (जैसे, सेंटीमीटर) से मेल खाता हो, जो इंजीनियरिंग ड्रॉइंग और प्रिंटेड डॉक्यूमेंटेशन के लिए अत्यंत महत्वपूर्ण है।

## पूर्वापेक्षाएँ

ट्यूटोरियल में आगे बढ़ने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हों:

- **Java Development Environment** – एक कार्यशील JDK (8 या बाद का) और एक IDE या बिल्ड टूल (Maven/Gradle)।  
- **Aspose.CAD for Java Library** – Aspose.CAD लाइब्रेरी को अपने Java प्रोजेक्ट में डाउनलोड और इंटीग्रेट करें। आप लाइब्रेरी [here](https://releases.aspose.com/cad/java/) से प्राप्त कर सकते हैं।

## Namespaces आयात करें

अपने Java कोड में, Aspose.CAD कार्यक्षमताओं तक पहुँचने के लिए आवश्यक नेमस्पेसेज़ शामिल करें। निम्नलिखित इम्पोर्ट्स जोड़ें:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

अब, Unit Type का उपयोग करके CAD ड्रॉइंग आकार को समायोजित करने की प्रक्रिया को प्रबंधनीय चरणों में विभाजित करते हैं:

## चरण 1: डेटा डायरेक्टरी निर्धारित करें

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

अपने CAD फ़ाइलों के स्थित डायरेक्टरी का पाथ सेट करें।

## चरण 2: CAD ड्रॉइंग लोड करें

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Aspose.CAD की `Image` क्लास का उपयोग करके CAD ड्रॉइंग लोड करें।

## चरण 3: BMP विकल्प बनाएं

```java
BmpOptions bmpOptions = new BmpOptions();
```

CAD लेआउट को BMP फॉर्मेट में निर्यात करने के लिए `BmpOptions` क्लास का एक इंस्टेंस बनाएं।

## चरण 4: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

वेक्टर रास्टराइज़ेशन के लिए `BmpOptions` के साथ `CadRasterizationOptions` का एक इंस्टेंस बनाएं और उसे संबद्ध करें।

## चरण 5: Unit Type सेट करें

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

CAD ड्रॉइंग के लिए इच्छित यूनिट टाइप निर्दिष्ट करें। इस उदाहरण में, हमने इसे **Centimeter** पर सेट किया है, जो सीधे **adjust CAD drawing size** करने पर निर्यात की गई इमेज के आकार को प्रभावित करता है।

## चरण 6: लेआउट सेट करें

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

निर्यात के दौरान विचार किए जाने वाले लेआउट को परिभाषित करें। इस मामले में, हमने **"Model"** लेआउट चुना है, लेकिन आवश्यकता पड़ने पर आप पेपर स्पेस लेआउट पर स्विच कर सकते हैं।

## चरण 7: BMP में निर्यात करें

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

अंत में, संशोधित CAD ड्रॉइंग को BMP फॉर्मेट में सहेजें। यह चरण **export DWG to BMP** वर्कफ़्लो को पूरा करता है जबकि आपने जो आकार समायोजन किए हैं उन्हें संरक्षित रखता है।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|--------|-----|
| **आउटपुट इमेज बहुत छोटी है** | Unit type सेट नहीं है या डिफ़ॉल्ट (पिक्सेल) उपयोग किया गया | इच्छित माप (जैसे, `UnitType.Centimeter`) के साथ `setUnitType()` कॉल करें। |
| **गलत लेआउट निर्यात हुआ** | लेआउट नाम में टाइपो | CAD व्यूअर से लेआउट नाम जांचें; `setLayouts()` में सटीक स्ट्रिंग उपयोग करें। |
| **लाइसेंस अपवाद** | प्रोडक्शन में वैध लाइसेंस के बिना चलाना | FAQ में वर्णित अनुसार एक अस्थायी या स्थायी लाइसेंस लागू करें। |

## अक्सर पूछे जाने वाले प्रश्न (विस्तारित)

**Q: क्या मैं Aspose.CAD for Java को अन्य प्रोग्रामिंग भाषाओं के साथ उपयोग कर सकता हूँ?**  
A: Aspose.CAD मुख्यतः Java का समर्थन करता है, लेकिन .NET जैसी अन्य भाषाओं के लिए भी संस्करण उपलब्ध हैं।

**Q: क्या Aspose.CAD के लिए कोई लाइसेंसिंग विकल्प उपलब्ध हैं?**  
A: हाँ, आप लाइसेंसिंग विकल्पों का पता लगा सकते हैं और Aspose.CAD [here](https://purchase.aspose.com/buy) से खरीद सकते हैं।

**Q: क्या Aspose.CAD के लिए कोई मुफ्त ट्रायल उपलब्ध है?**  
A: बिल्कुल, आप एक मुफ्त ट्रायल [here](https://releases.aspose.com/) तक पहुँच सकते हैं।

**Q: Aspose.CAD for Java के लिए समर्थन कैसे प्राप्त करूँ?**  
A: व्यापक समर्थन के लिए Aspose.CAD फ़ोरम [here](https://forum.aspose.com/c/cad/19) पर जाएँ।

**Q: क्या मैं Aspose.CAD के लिए अस्थायी लाइसेंस प्राप्त कर सकता हूँ?**  
A: हाँ, आप एक अस्थायी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

---

**अंतिम अपडेट:** 2025-12-25  
**परीक्षण किया गया:** Aspose.CAD for Java 24.10  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}