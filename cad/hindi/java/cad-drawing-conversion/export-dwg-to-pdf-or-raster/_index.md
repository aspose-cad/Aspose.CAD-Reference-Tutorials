---
date: 2025-12-18
description: जावा में Aspose.CAD का उपयोग करके dwg को pdf या रास्टर इमेजेज़ में निर्यात
  करने के तरीके का अन्वेषण करें। यह चरण-दर-चरण मार्गदर्शिका DWG फ़ाइलों के सटीक, कुशल
  और आसान रूपांतरण को सुनिश्चित करती है।
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java का उपयोग करके DWG को PDF या रास्टर में निर्यात करें
url: /hi/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java का उपयोग करके DWG को PDF या रास्टर में निर्यात करें

## परिचय

कंप्यूटर‑सहायता डिज़ाइन (CAD) की गतिशील दुनिया में, ड्रॉइंग्स का कुशल प्रबंधन अत्यंत महत्वपूर्ण है। **Aspose.CAD for Java** के साथ आप कुछ ही कोड लाइनों में **dwg को pdf** — या रास्टर इमेज — में निर्यात कर सकते हैं। यह ट्यूटोरियल आपको पूरी प्रक्रिया के माध्यम से ले जाता है, DWG फ़ाइल को लोड करने से लेकर उच्च‑गुणवत्ता वाला PDF उत्पन्न करने तक, और यह भी बताता है कि CAD रूपांतरण कार्यों के लिए Aspose.CAD Java क्यों प्रमुख लाइब्रेरी है।

## त्वरित उत्तर
- **यह ट्यूटोरियल क्या कवर करता है?** Aspose.CAD for Java का उपयोग करके DWG फ़ाइलों को PDF या रास्टर इमेज में निर्यात करना।  
- **क्या मुझे लाइसेंस की आवश्यकता है?** मूल्यांकन के लिए एक मुफ्त अस्थायी लाइसेंस उपलब्ध है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण समर्थित है?** कोई भी Java 8+ रनटाइम नवीनतम Aspose.CAD Java API के साथ काम करता है।  
- **क्या मैं DWG को अन्य इमेज फ़ॉर्मेट में बदल सकता हूँ?** हाँ – वही रास्टराइज़ेशन विकल्प आपको PNG, JPEG, BMP आदि में आउटपुट करने की अनुमति देते हैं।  
- **रूपांतरण में कितना समय लगता है?** सामान्य ड्रॉइंग्स के लिए आमतौर पर एक सेकंड से कम; बड़े फ़ाइलों में कुछ सेकंड लग सकते हैं।

## “export dwg to pdf” क्या है?
DWG को PDF में निर्यात करना मतलब मूल AutoCAD ड्रॉइंग को एक पोर्टेबल, डिवाइस‑स्वतंत्र PDF दस्तावेज़ में बदलना है। उत्पन्न PDF वेक्टर डेटा, लेयर्स और स्केलिंग को संरक्षित करता है, जिससे यह साझा करने, प्रिंट करने या अभिलेखित करने के लिए आदर्श बन जाता है।

## इस रूपांतरण के लिए Aspose.CAD Java क्यों उपयोग करें?
- **कोई बाहरी निर्भरताएँ नहीं** – शुद्ध Java, कोई नेटिव DLL नहीं।  
- **सटीक यूनिट हैंडलिंग** – स्वचालित रूप से मीट्रिक या इम्पीरियल यूनिट्स का सम्मान करता है।  
- **उच्च‑गुणवत्ता वाला रास्टर आउटपुट** – DPI और पेज आकार नियंत्रण के साथ फाइन‑ट्यून किया गया।  
- **पूर्ण PDF समर्थन** – अतिरिक्त लाइब्रेरी की आवश्यकता के बिना वेक्टर‑संरक्षित PDF जनरेशन।

## पूर्वापेक्षाएँ

कोड में डुबकी लगाने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- Java प्रोग्रामिंग का बुनियादी ज्ञान।  
- Aspose.CAD for Java लाइब्रेरी स्थापित हो। यदि आपने अभी तक इसे डाउनलोड नहीं किया है, तो इसे **[here](https://releases.aspose.com/cad/java/)** से प्राप्त करें।  
- परीक्षण के लिए एक DWG फ़ाइल – इस गाइड में नमूना **Bottom_plate.dwg** उपयोग किया गया है।

## नेमस्पेस आयात करें

अपने Java प्रोजेक्ट में आवश्यक क्लासेज़ को आयात करें ताकि रूपांतरण शुरू किया जा सके:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## चरण‑दर‑चरण गाइड

### चरण 1: DWG फ़ाइल लोड करें

सबसे पहले, `Image` क्लास का उपयोग करके अपनी DWG ड्रॉइंग लोड करें। यह एक इन‑मेमोरी प्रतिनिधित्व बनाता है जिसे Aspose.CAD उपयोग कर सकता है।

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### चरण 2: यूनिट प्रकार निर्धारित करें

ड्रॉइंग मीट्रिक है या इम्पीरियल, यह समझना सही स्केलिंग के लिए आवश्यक है। हेल्पर मेथड `IsMetric` (कार्यान्वयन यहाँ नहीं दिया गया) एक बूलियन फ़्लैग लौटाता है।

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### चरण 3: रास्टराइज़ेशन विकल्प सेट करें

यूनिट सिस्टम के आधार पर पेज आकार, स्केलिंग और लक्ष्य यूनिट प्रकार कॉन्फ़िगर करें। ये विकल्प निर्धारित करते हैं कि DWG को PDF में रैप करने से पहले कैसे रास्टराइज़ किया जाएगा।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### चरण 4: PDF विकल्प कॉन्फ़िगर करें

एक `PdfOptions` इंस्टेंस बनाएं और रास्टराइज़ेशन सेटिंग्स को संलग्न करें। यह Aspose.CAD को बताता है कि अंतिम PDF में रास्टराइज़्ड कंटेंट को कैसे एम्बेड किया जाए।

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### चरण 5: PDF के रूप में सहेजें

अंत में, ड्रॉइंग को PDF फ़ाइल में निर्यात करें। `save` मेथड आउटपुट पाथ और कॉन्फ़िगर किए गए `PdfOptions` को लेता है।

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

जब कोड समाप्त हो जाएगा, आपको अपने `DWGDrawings` फ़ोल्डर में **Saved.pdf** मिलेगा, जो वितरण या अभिलेख के लिए तैयार है।

## सामान्य समस्याएँ एवं सुझाव

- **गलत पेज आकार** – यूनिट रूपांतरण लॉजिक को दोबारा जांचें; असंगत गुणांक बड़े पेज बना सकते हैं।  
- **फ़ॉन्ट या लाइनवेट्स गायब** – रूपांतरण से पहले सुनिश्चित करें कि DWG किसी भी बाहरी संसाधन को संदर्भित करता है।  
- **बड़ी ड्रॉइंग्स पर प्रदर्शन** – केवल तब `CadRasterizationOptions` में `DPI` सेटिंग बढ़ाएँ जब उच्च गुणवत्ता आवश्यक हो; कम DPI प्रोसेसिंग को तेज़ करता है।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं Aspose.CAD for Java को अन्य Java फ्रेमवर्क्स के साथ उपयोग कर सकता हूँ?**  
उत्तर: हाँ, Aspose.CAD for Java सहजता से Spring, Jakarta EE और Android जैसे लोकप्रिय Java फ्रेमवर्क्स के साथ एकीकृत होता है।

**प्रश्न: क्या Aspose.CAD for Java के लिए एक अस्थायी लाइसेंस उपलब्ध है?**  
उत्तर: हाँ, आप एक अस्थायी लाइसेंस **[here](https://purchase.aspose.com/temporary-license/)** प्राप्त कर सकते हैं।

**प्रश्न: Aspose.CAD for Java के लिए समर्थन कहाँ मिल सकता है?**  
उत्तर: सहायता के लिए **[Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19)** देखें, जहाँ समुदाय और Aspose इंजीनियर्स मदद करते हैं।

**प्रश्न: Aspose.CAD for Java का लाइसेंस कैसे खरीदूँ?**  
उत्तर: आप लाइसेंस **[here](https://purchase.aspose.com/buy)** खरीद सकते हैं।

**प्रश्न: Aspose.CAD for Java किन यूनिट्स को सपोर्ट करता है?**  
उत्तर: Aspose.CAD for Java मीट्रिक और इम्पीरियल दोनों यूनिट्स को सपोर्ट करता है, और ड्रॉइंग के यूनिट सिस्टम को स्वतः पहचान लेता है।

**प्रश्न: क्या मैं उसी API का उपयोग करके DWG को अन्य इमेज फ़ॉर्मेट (जैसे PNG, JPEG) में बदल सकता हूँ?**  
उत्तर: बिल्कुल। `PdfOptions` को उपयुक्त रास्टर इमेज विकल्प (जैसे `PngOptions`) से बदलें और वही `CadRasterizationOptions` पुनः उपयोग करें।

## निष्कर्ष

इस ट्यूटोरियल ने दिखाया कि कैसे Aspose.CAD for Java का उपयोग करके **dwg को pdf** और रास्टर इमेज में निर्यात किया जा सकता है। चरण‑दर‑चरण गाइड का पालन करके आप किसी भी Java एप्लिकेशन में विश्वसनीय CAD रूपांतरण को एकीकृत कर सकते हैं, चाहे आपको दस्तावेज़ीकरण के लिए PDF चाहिए या वेब डिस्प्ले के लिए रास्टर इमेज।

---

**अंतिम अपडेट:** 2025-12-18  
**परीक्षण किया गया संस्करण:** Aspose.CAD for Java 24.10  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}