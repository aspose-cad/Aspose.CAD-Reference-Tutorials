---
date: 2025-12-12
description: Aspose.CAD for Java का उपयोग करके CAD को PDF और TIFF में बदलते समय जावा
  में बैकग्राउंड रंग कैसे सेट करें, सीखें। पेशेवर परिणामों के लिए ड्राइंग रंग को कस्टमाइज़
  करें।
linktitle: Setting Background and Drawing Color
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java के साथ जावा में पृष्ठभूमि रंग सेट करें
url: /hi/java/advanced-cad-features/setting-background-and-drawing-color/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java के साथ बैकग्राउंड रंग सेट करें java

## परिचय

आधुनिक CAD कार्यप्रवाहों में, रूपांतरण के दौरान **set background color java** को सेट करना स्पष्ट, प्रस्तुति‑तैयार दस्तावेज़ बनाने के लिए आवश्यक है। Aspose.CAD for Java CAD फ़ाइलों को PDF या TIFF में बदलना आसान बनाता है और आपको बैकग्राउंड और ड्रॉइंग रंगों पर पूर्ण नियंत्रण देता है। इस ट्यूटोरियल में हम पूरी प्रक्रिया को चरण‑दर‑चरण देखेंगे—DXF फ़ाइल लोड करने से लेकर चुने हुए रंगों के साथ PDF और TIFF फ़ाइलों को निर्यात करने तक।

## त्वरित उत्तर
- **Java में CAD रूपांतरण को कौनसी लाइब्रेरी संभालती है?** Aspose.CAD for Java.  
- **क्या रूपांतरण के दौरान बैकग्राउंड रंग बदला जा सकता है?** हाँ, `CadRasterizationOptions.setBackgroundColor` का उपयोग करके।  
- **कौनसे आउटपुट फ़ॉर्मेट कवर किए गए हैं?** PDF और TIFF (दोनों रास्टराइज़्ड)।  
- **उत्पादन उपयोग के लिए लाइसेंस चाहिए?** एक वाणिज्यिक लाइसेंस आवश्यक है; एक मुफ्त ट्रायल उपलब्ध है।  
- **क्या बैच रूपांतरण समर्थित है?** बिल्कुल—एक ही सेटिंग्स के साथ लूप में कई फ़ाइलों को प्रोसेस किया जा सकता है।

## CAD रूपांतरण के संदर्भ में “set background color java” क्या है?
Java में बैकग्राउंड रंग सेट करना का अर्थ है रास्टराइज़ेशन विकल्पों को इस प्रकार कॉन्फ़िगर करना कि रेंडर की गई छवि (PDF या TIFF) डिफ़ॉल्ट सफ़ेद कैनवास की बजाय आप द्वारा निर्दिष्ट रंग का उपयोग करे। यह दृश्य कंट्रास्ट को बेहतर बनाता है, विशेषकर जब CAD ड्राइंग में हल्की लाइनों का उपयोग हो।

## CAD को PDF या TIFF में बदलने के लिए Aspose.CAD for Java क्यों उपयोग करें?
- **उच्च सटीकता** – लाइन वेट, लेयर्स और रंगों को बरकरार रखता है।  
- **कोई बाहरी निर्भरताएँ नहीं** – शुद्ध Java, कोई नेटिव लाइब्रेरी नहीं।  
- **लचीला रेंडरिंग** – पेज साइज, DPI, बैकग्राउंड और ड्रॉइंग रंगों पर नियंत्रण।  
- **बैच प्रोसेसिंग** – ऑटोमेशन पाइपलाइन के लिए आदर्श।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास है:

- **Aspose.CAD for Java लाइब्रेरी** – इसे [यहाँ](https://releases.aspose.com/cad/java/) से डाउनलोड करें।  
- **आपकी CAD फ़ाइलों के लिए एक फ़ोल्डर** – `"Your Document Directory" + "CADConversion/"` को अपने मशीन पर वास्तविक पथ से बदलें।

## नेमस्पेस आयात करें

सबसे पहले, उन क्लासों को आयात करें जिनकी आपको आवश्यकता होगी। ये इम्पोर्ट्स आपको रंग संभालने, रास्टराइज़ेशन विकल्पों और आउटपुट फ़ॉर्मेट्स तक पहुँच प्रदान करते हैं।

```java
import java.awt.Color;
import java.awt.Image;

import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## चरण‑दर‑चरण गाइड

### चरण 1: CAD फ़ाइल लोड करें

हम स्रोत DXF (या कोई भी समर्थित CAD फ़ॉर्मेट) को `Image` ऑब्जेक्ट में लोड करते हैं।

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(srcFile);
```

### चरण 2: बैकग्राउंड और ड्रॉइंग रंग कॉन्फ़िगर करें

यहाँ हम पेज आयाम सेट करते हैं, एक बैकग्राउंड रंग चुनते हैं, और रेंडरर को मूल CAD रंगों के बजाय एक विशिष्ट ड्रॉइंग रंग उपयोग करने के लिए कहते हैं।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBeige());   // example background
rasterizationOptions.setDrawType(CadDrawTypeMode.UseDrawColor);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBlue());   // overwrite with blue if needed
```

> **प्रो टिप:** यदि आप CAD के मूल रंगों को बनाए रखना चाहते हैं जबकि कस्टम बैकग्राउंड लागू करना चाहते हैं, तो `CadDrawTypeMode.UseOriginalColors` के साथ प्रयोग करें।

### चरण 3: PDF बनाएं और सहेजें

हम रास्टराइज़ेशन विकल्पों को `PdfOptions` से बाइंड करते हैं और परिणाम को PDF फ़ाइल के रूप में सहेजते हैं।

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

### चरण 4: TIFF बनाएं और सहेजें

उसी रास्टराइज़ेशन सेटिंग्स को TIFF आउटपुट के लिए पुनः उपयोग किया जा सकता है।

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **बैकग्राउंड रंग नहीं बदल रहा** | सुनिश्चित करें कि आप `setBackgroundColor` को *ड्रॉ टाइप* सेट करने के बाद कॉल करें। दूसरा कॉल पहला ओवरराइट कर देता है, इसलिए इच्छित रंग को अंतिम कॉल में रखें। |
| **आउटपुट धुंधला है** | `PageWidth`/`PageHeight` बढ़ाएँ या `rasterizationOptions.setResolution(...)` के माध्यम से उच्च DPI सेट करें। |
| **फ़ाइल नहीं मिली अपवाद** | पुष्टि करें कि `dataDir` पथ के अंत में एक सेपरेटर (`/` या `\\`) है और फ़ाइल वास्तव में मौजूद है। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या Aspose.CAD for Java बड़े पैमाने पर रूपांतरणों के लिए उपयुक्त है?**  
उत्तर: बिल्कुल। आप कोड को लूप में रख सकते हैं और समान रास्टराइज़ेशन सेटिंग्स के साथ दर्जनों फ़ाइलों को प्रोसेस कर सकते हैं।

**प्रश्न: क्या उत्पन्न फ़ाइलों में बैकग्राउंड रंग को कस्टमाइज़ किया जा सकता है?**  
उत्तर: हाँ। ट्यूटोरियल दर्शाता है कि कैसे `com.aspose.cad.Color` को PDF और TIFF दोनों आउटपुट के लिए सेट किया जा सकता है।

**प्रश्न: Aspose.CAD for Java की व्यापक दस्तावेज़ीकरण कहाँ मिल सकती है?**  
उत्तर: विस्तृत विवरण और अतिरिक्त उदाहरणों के लिए [documentation](https://reference.aspose.com/cad/java/) देखें।

**प्रश्न: क्या मुफ्त ट्रायल उपलब्ध है?**  
उत्तर: हाँ, [free trial](https://releases.aspose.com/) के साथ सुविधाओं का अन्वेषण करें।

**प्रश्न: Aspose.CAD for Java के लिए समर्थन कैसे प्राप्त करें?**  
उत्तर: समुदाय के साथ प्रश्न पूछने और अनुभव साझा करने के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

---

**अंतिम अपडेट:** 2025-12-12  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}