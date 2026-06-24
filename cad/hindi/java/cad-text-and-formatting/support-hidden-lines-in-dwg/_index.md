---
date: 2026-03-05
description: इस चरण‑दर‑चरण ट्यूटोरियल में Aspose.CAD for Java के साथ DWG को PDF में
  निर्यात करना, छिपी हुई रेखाओं को सक्षम करना, और DWG को PDF में परिवर्तित करना सीखें।
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: छिपी हुई रेखाओं के साथ DWG को PDF में निर्यात करें – Aspose.CAD for Java
url: /hi/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# छुपी रेखाओं के साथ DWG को PDF में निर्यात करें – Aspose.CAD for Java

## परिचय

इस ट्यूटोरियल में आप सीखेंगे कि कैसे Aspose.CAD for Java का उपयोग करके छुपी रेखाओं को संरक्षित रखते हुए **export dwg to pdf** किया जाए। चाहे आपको **convert DWG to PDF** करना हो, एक **dwg to pdf tutorial**‑शैली गाइड बनाना हो, या बस **save DWG as PDF** छुपी‑रेखा समर्थन के साथ चाहिए, हम आपको हर कदम पर मार्गदर्शन करेंगे। अंत तक, आपके पास एक तैयार‑उपयोग समाधान होगा जिसे आप किसी भी Java प्रोजेक्ट में जोड़ सकते हैं।

## त्वरित उत्तर
- **What does this tutorial cover?** Aspose.CAD for Java के साथ DWG को PDF में निर्यात करते समय छुपी‑रेखा रेंडरिंग को सक्षम करना।  
- **Which primary operation is performed?** `export dwg to pdf`.  
- **Do I need a license?** परीक्षण के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **What are the prerequisites?** Java विकास वातावरण, Aspose.CAD for Java लाइब्रेरी, और DWG फ़ाइलें।  
- **How long does implementation take?** बुनियादी सेटअप के लिए लगभग 10‑15 मिनट।

## “export dwg to pdf” क्या है?

DWG फ़ाइल को PDF में निर्यात करने से वेक्टर‑आधारित CAD ड्राइंग को पोर्टेबल डॉक्यूमेंट फ़ॉर्मेट में बदल दिया जाता है, जबकि लेयर्स, लाइन टाइप्स, और वैकल्पिक छुपी‑रेखा रेंडरिंग को संरक्षित रखा जाता है। यह उन हितधारकों के साथ CAD डिज़ाइनों को साझा करना आसान बनाता है जिनके पास CAD सॉफ़्टवेयर नहीं हो सकता।

## DWG को PDF में निर्यात करते समय छुपी रेखाओं को कैसे सक्षम करें

छुपी रेखाओं को रास्टराइज़ेशन विकल्पों में लेआउट सेटिंग के माध्यम से नियंत्रित किया जाता है। **Model** लेआउट चुनने पर, Aspose.CAD रेंडरर को बताता है कि छुपी किनारों को अदृश्य माना जाए, जिससे आपको 3‑D मॉडल की एक साफ़ 2‑D प्रस्तुति मिलती है।

## निर्यात करते समय छुपी रेखाओं को सक्षम क्यों करें?

छुपी रेखाएँ जटिल 3‑D मॉडलों की 2‑D पृष्ठ पर अधिक स्पष्ट दृश्य प्रस्तुति प्रदान करती हैं, जिससे केवल दिखाई देने वाली किनारों पर ज़ोर दिया जाता है। यह पठनीयता को सुधारता है और अक्सर इंजीनियरिंग दस्तावेज़ीकरण के लिए आवश्यक होता है।

## पूर्वापेक्षाएँ

1. **Aspose.CAD for Java** – आधिकारिक साइट से लाइब्रेरी डाउनलोड करें [here](https://releases.aspose.com/cad/java/)।  
2. **DWG files** – स्रोत DWG ड्रॉइंग्स को किसी ज्ञात डायरेक्टरी में संग्रहीत रखें।  
3. **Java development environment** – JDK 8+ और आपका पसंदीदा IDE (Eclipse, IntelliJ, आदि)।  

अब जब आप सेट हो गए हैं, चलिए कोड में डुबकी लगाते हैं।

## नेमस्पेस आयात करें

आवश्यक क्लासेज़ को आयात करके शुरू करें ताकि आप CAD इमेजेज़ और PDF विकल्पों के साथ काम कर सकें।

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## चरण 1: अपना प्रोजेक्ट सेट अप करें

एक Java प्रोजेक्ट बनाएं और Aspose.CAD JAR को अपने बिल्ड पाथ में जोड़ें। फिर उस डायरेक्टरी को परिभाषित करें जिसमें आपके DWG फ़ाइलें हैं।

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro tip:** एक absolute path का उपयोग करें या अपने प्रोजेक्ट के resources फ़ोल्डर के आधार पर relative path कॉन्फ़िगर करें।

## चरण 2: DWG फ़ाइल लोड करें

स्रोत DWG फ़ाइल को एक `CadImage` ऑब्जेक्ट में लोड करें ताकि आप इसे संशोधित कर सकें।

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## चरण 3: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

उन लेयर्स को चुनें जिन्हें आप शामिल करना चाहते हैं और पृष्ठ आकार को मूल ड्राइंग के अनुसार सेट करें। यहाँ हम लेआउट निर्दिष्ट करके छुपी‑रेखा रेंडरिंग को सक्षम करते हैं।

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## चरण 4: PDF विकल्प सेट करें

Aspose.CAD को बताएं कि वेक्टर डेटा को PDF में रास्टराइज़ करे, “Model” लेआउट का उपयोग करके छुपी रेखाओं को छुपा कर रखें।

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## चरण 5: परिणाम सहेजें

अंत में, DWG को PDF फ़ाइल के रूप में निर्यात करें। छुपी रेखाएँ आपके द्वारा सेट किए गए लेआउट के अनुसार सम्मानित होंगी।

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Common Pitfall:** लेआउट को `"Model"` पर सेट करना भूल जाने से सभी रेखाएँ (छुपी रेखाओं सहित) PDF में ठोस दिखाई देंगी।

## सामान्य समस्याएँ और समाधान

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| PDF सभी रेखाएँ ठोस दिखाता है | लेआउट **Model** पर सेट नहीं है | सुनिश्चित करें कि `rasterizationOptions.setLayouts(new String[] { "Model" });` को सहेजने से पहले कॉल किया गया है। |
| आउटपुट में लेयर्स गायब हैं | गलत लेयर नाम | DWG फ़ाइल में लेयर नामों को सत्यापित करें और उन्हें `list` में बिल्कुल समान रखें। |
| बड़ी फ़ाइलों पर Out‑of‑memory त्रुटि | बड़ी रास्टराइज़ेशन आकार | पृष्ठ आयाम कम करें या संभव हो तो ड्रॉइंग को भागों में प्रोसेस करें। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.CAD for Java को अन्य CAD फ़ाइल फ़ॉर्मेट्स के साथ उपयोग कर सकता हूँ?
A1: हाँ, Aspose.CAD विभिन्न CAD फ़ॉर्मेट्स जैसे DWG, DXF, DWF, आदि को समर्थन देता है।

### Q2: क्या Aspose.CAD for Java के लिए कोई मुफ्त ट्रायल उपलब्ध है?
A2: हाँ, आप मुफ्त ट्रायल [here](https://releases.aspose.com/) पर पा सकते हैं।

### Q3: मैं Aspose.CAD for Java के लिए समर्थन कैसे प्राप्त करूँ?
A3: समुदाय समर्थन के लिए Aspose.CAD फ़ोरम [here](https://forum.aspose.com/c/cad/19) पर जाएँ।

### Q4: मैं Aspose.CAD for Java के विस्तृत दस्तावेज़ कहाँ पा सकता हूँ?
A4: दस्तावेज़ीकरण [here](https://reference.aspose.com/cad/java/) पर देखें।

### Q5: क्या मैं Aspose.CAD for Java के लिए एक अस्थायी लाइसेंस खरीद सकता हूँ?
A5: हाँ, आप अस्थायी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

### Q6: क्या यह विधि हेडलेस सर्वर वातावरण में DWG को PDF में परिवर्तित करने के लिए भी काम करती है?
A6: बिल्कुल। चूँकि कोड केवल Aspose.CAD API का उपयोग करता है, यह किसी भी UI निर्भरता के बिना चलता है, जिससे यह सर्वर‑साइड ऑटोमेशन के लिए आदर्श बनता है।

## निष्कर्ष

अब आपके पास Aspose.CAD for Java का उपयोग करके छुपी‑रेखा समर्थन के साथ **export dwg to pdf** करने की एक पूर्ण, उत्पादन‑तैयार विधि है। इस दृष्टिकोण को बैच प्रोसेसिंग टूल्स, वेब सेवाओं, या डेस्कटॉप एप्लिकेशन्स में एकीकृत किया जा सकता है ताकि CAD‑to‑PDF रूपांतरण को स्वचालित किया जा सके।

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}