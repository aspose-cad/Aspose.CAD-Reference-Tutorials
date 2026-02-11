---
date: 2026-01-02
description: Aspose.CAD for Java के साथ इस चरण‑दर‑चरण ट्यूटोरियल में सीखें कि DWG
  को PDF के रूप में निर्यात कैसे करें, छिपी हुई रेखाओं को सक्षम करें, और DWG को PDF
  में कैसे परिवर्तित करें।
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: छिपी हुई लाइनों के साथ DWG को PDF के रूप में निर्यात करें – Aspose.CAD for
  Java
url: /hi/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# छिपी हुई लाइनों के साथ DWG को PDF में निर्यात करें – Aspose.CAD for Java

## परिचय

इस ट्यूटोरियल में आप सीखेंगे कि Aspose.CAD for Java का उपयोग करके छिपी हुई लाइनों को संरक्षित रखते हुए **DWG को PDF में निर्यात** कैसे करें। चाहे आपको **DWG को PDF में बदलना** हो, **dwg to pdf tutorial**‑शैली गाइड बनाना हो, या बस **DWG को PDF के रूप में सहेजना** छिपी हुई लाइन समर्थन के साथ, हम आपको हर कदम पर मार्गदर्शन करेंगे। अंत तक, आपके पास एक तैयार‑से‑उपयोग समाधान होगा जिसे आप किसी भी Java प्रोजेक्ट में जोड़ सकते हैं।

## त्वरित उत्तर
- **यह ट्यूटोरियल क्या कवर करता है?** Aspose.CAD for Java के साथ DWG को PDF में निर्यात करते समय छिपी हुई लाइन रेंडरिंग को सक्षम करना।  
- **कौन सा मुख्य ऑपरेशन किया जाता है?** `export dwg as pdf`.  
- **क्या मुझे लाइसेंस चाहिए?** टेस्टिंग के लिए एक मुफ्त ट्रायल काम करता है; प्रोडक्शन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **पूर्वापेक्षाएँ क्या हैं?** Java विकास पर्यावरण, Aspose.CAD for Java लाइब्रेरी, और DWG फाइलें।  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** बेसिक सेटअप के लिए लगभग 10‑15 मिनट।

## “export dwg as pdf” क्या है?
DWG फ़ाइल को PDF में निर्यात करने से वेक्टर‑आधारित CAD ड्राइंग को एक पोर्टेबल डॉक्यूमेंट फॉर्मेट में बदल दिया जाता है, जबकि लेयर्स, लाइन टाइप्स, और वैकल्पिक छिपी हुई लाइन रेंडरिंग को संरक्षित रखा जाता है। इससे उन हितधारकों के साथ CAD डिज़ाइनों को साझा करना आसान हो जाता है जिनके पास CAD सॉफ़्टवेयर नहीं हो सकता।

## निर्यात करते समय छिपी हुई लाइनों को क्यों सक्षम करें?
छिपी हुई लाइनों से जटिल 3D मॉडलों का 2‑D पृष्ठ पर स्पष्ट दृश्य प्रतिनिधित्व मिलता है, जिससे केवल दिखाई देने वाले किनारे प्रमुख होते हैं। यह पठनीयता को सुधारता है और अक्सर इंजीनियरिंग दस्तावेज़ीकरण के लिए आवश्यक होता है।

## पूर्वापेक्षाएँ

1. **Aspose.CAD for Java** – आधिकारिक साइट से लाइब्रेरी डाउनलोड करें [यहाँ](https://releases.aspose.com/cad/java/).  
2. **DWG files** – स्रोत DWG ड्रॉइंग्स को किसी ज्ञात डायरेक्टरी में संग्रहीत रखें।  
3. **Java development environment** – JDK 8+ और आपका पसंदीदा IDE (Eclipse, IntelliJ, आदि)।  

अब जब आप सेट हो गए हैं, चलिए कोड में डुबकी लगाते हैं।

## नेमस्पेस आयात करें

CAD इमेजेज़ और PDF विकल्पों के साथ काम करने के लिए आवश्यक क्लासेस को आयात करके शुरू करें।

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## चरण 1: अपना प्रोजेक्ट सेट अप करें

एक Java प्रोजेक्ट बनाएं और Aspose.CAD JAR को अपने बिल्ड पाथ में जोड़ें। फिर वह डायरेक्टरी परिभाषित करें जिसमें आपके DWG फाइलें हों।

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **प्रो टिप:** एक एब्सॉल्यूट पाथ का उपयोग करें या अपने प्रोजेक्ट के रिसोर्सेज़ फ़ोल्डर के आधार पर एक रिलेटिव पाथ कॉन्फ़िगर करें।

## चरण 2: DWG फ़ाइल लोड करें

स्रोत DWG फ़ाइल को एक `CadImage` ऑब्जेक्ट में लोड करें ताकि आप इसे हेरफेर कर सकें।

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## चरण 3: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

वह लेयर्स चुनें जिन्हें आप शामिल करना चाहते हैं और पेज साइज को मूल ड्राइंग के अनुसार सेट करें। यहाँ हम लेआउट निर्दिष्ट करके छिपी हुई लाइन रेंडरिंग को सक्षम करते हैं।

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## चरण 4: PDF विकल्प सेट करें

Aspose.CAD को बताएं कि वेक्टर डेटा को PDF में रास्टराइज़ करे, “Model” लेआउट का उपयोग करके छिपी हुई लाइनों को छिपा रखे।

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## चरण 5: परिणाम सहेजें

अंत में, DWG को PDF फ़ाइल के रूप में निर्यात करें। छिपी हुई लाइनों का सम्मान आपके द्वारा सेट किए गए लेआउट के अनुसार किया जाएगा।

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **सामान्य गलती:** लेआउट को `"Model"` पर सेट करना भूल जाने से सभी लाइनों (छिपी हुई लाइनों सहित) PDF में ठोस दिखेंगी।

## निष्कर्ष

अब आपके पास Aspose.CAD for Java का उपयोग करके छिपी हुई लाइन समर्थन के साथ **DWG को PDF में निर्यात** करने की एक पूर्ण, प्रोडक्शन‑रेडी विधि है। इस दृष्टिकोण को बैच प्रोसेसिंग टूल्स, वेब सर्विसेज़, या डेस्कटॉप एप्लिकेशन्स में एकीकृत किया जा सकता है ताकि CAD‑to‑PDF रूपांतरण को स्वचालित किया जा सके।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.CAD for Java को अन्य CAD फ़ाइल फ़ॉर्मेट्स के साथ उपयोग कर सकता हूँ?
A1: हाँ, Aspose.CAD विभिन्न CAD फ़ॉर्मेट्स जैसे DWG, DXF, DWF, आदि को सपोर्ट करता है।

### Q2: क्या Aspose.CAD for Java के लिए कोई मुफ्त ट्रायल उपलब्ध है?
A2: हाँ, आप मुफ्त ट्रायल [यहाँ](https://releases.aspose.com/) पा सकते हैं।

### Q3: मैं Aspose.CAD for Java के लिए सपोर्ट कैसे प्राप्त करूँ?
A3: समुदाय समर्थन के लिए Aspose.CAD फ़ोरम [यहाँ](https://forum.aspose.com/c/cad/19) पर जाएँ।

### Q4: मैं Aspose.CAD for Java के विस्तृत दस्तावेज़ कहाँ पा सकता हूँ?
A4: दस्तावेज़ीकरण [यहाँ](https://reference.aspose.com/cad/java/) देखें।

### Q5: क्या मैं Aspose.CAD for Java के लिए एक अस्थायी लाइसेंस खरीद सकता हूँ?
A5: हाँ, आप अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

### Q6: क्या यह विधि हेडलेस सर्वर वातावरण में DWG को PDF में बदलने के लिए भी काम करती है?
A6: बिल्कुल। चूँकि कोड केवल Aspose.CAD API का उपयोग करता है, यह किसी भी UI निर्भरता के बिना चलता है, जिससे यह सर्वर‑साइड ऑटोमेशन के लिए आदर्श बनता है।

**अंतिम अपडेट:** 2026-01-02  
**परीक्षण किया गया संस्करण:** Aspose.CAD for Java 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}