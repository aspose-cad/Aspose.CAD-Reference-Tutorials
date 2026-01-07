---
date: 2026-01-07
description: Aspose.CAD for Java का उपयोग करके CAD को PDF में निर्यात करना और DGN
  को PDF में बदलना सीखें। जावा डेवलपर्स के लिए चरण‑दर‑चरण गाइड।
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: CAD को PDF में निर्यात करें – Aspose.CAD for Java के साथ एम्बेडेड DGN निर्यात
  करें
url: /hi/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD को PDF में निर्यात करें – Aspose.CAD for Java के साथ एम्बेडेड DGN निर्यात करें

## परिचय

इस ट्यूटोरियल में आप **CAD को PDF में निर्यात करने** का तरीका जानेंगे, जहाँ एक एम्बेडेड DGN फ़ाइल को Aspose.CAD for Java के साथ उच्च‑गुणवत्ता वाले PDF दस्तावेज़ में परिवर्तित किया जाता है। Aspose.CAD एक मजबूत लाइब्रेरी है जो Java डेवलपर्स को CAD फ़ाइलों के प्रबंधन पर पूर्ण नियंत्रण देती है, चाहे आपको **DGN को PDF में बदलना**, **DWG को PDF में बदलना** हो, या बस CAD ड्रॉइंग्स को अन्य फ़ॉर्मेट में रेंडर करना हो। नीचे दिए गए चरण‑बद्ध मार्गदर्शक का पालन करें, और आप इस क्षमता को अपनी एप्लिकेशन में मिनटों में एकीकृत कर सकेंगे।

## त्वरित उत्तर
- **“export CAD to PDF” क्या मतलब है?** यह CAD ड्रॉइंग्स (DWG, DGN, आदि) को PDF फ़ाइलों में परिवर्तित करता है जबकि वेक्टर गुणवत्ता को बनाए रखता है।  
- **कौन सी लाइब्रेरी उपयोग की गई है?** Aspose.CAD for Java।  
- **क्या मुझे लाइसेंस की आवश्यकता है?** उत्पादन के लिए लाइसेंस आवश्यक है; एक मुफ्त ट्रायल उपलब्ध है।  
- **मुख्य पूर्वापेक्षाएँ क्या हैं?** Java विकास वातावरण और Aspose.CAD for Java JAR।  
- **क्या मैं आउटपुट को कस्टमाइज़ कर सकता हूँ?** हाँ – आप लेआउट चुन सकते हैं, रास्टराइज़ेशन विकल्प सेट कर सकते हैं, और PDF सेटिंग्स को नियंत्र सकते हैं।

## “export CAD to PDF” क्या है?
CAD को PDF में निर्यात करना का अर्थ है मूल CAD फ़ाइल (जैसे DWG या DGN) को एक PDF दस्तावेज़ में बदलना जो मूल ज्यामिति को सटीक रूप से दर्शाता है। PDF को किसी भी प्लेटफ़ॉर्म पर CAD सॉफ़्टवेयर की आवश्यकता के बिना देखा जा सकता है, जिससे यह साझा करने, प्रिंट करने या संग्रहित करने के लिए आदर्श बन जाता है।

## Aspose.CAD for Java का उपयोग करके DGN को PDF में बदलने के कारण?
- **कोई बाहरी निर्भरताएँ नहीं** – पूरी तरह Java में काम करता है।  
- **वेक्टर डेटा संरक्षित रहता है** – PDF किसी भी ज़ूम स्तर पर स्पष्ट रहता है।  
- **सूक्ष्म नियंत्रण** – विशिष्ट लेआउट चुनें, रास्टराइज़ेशन DPI सेट करें, और फ़ॉन्ट एम्बेड करें।  
- **एंटरप्राइ‑रेडी** – बड़े फ़ाइलों, बैच प्रोसेसिंग, और लाइसेंस विकल्पों को सपोर्ट करता है।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- **Java Development Environment** – JDK 8 या उससे ऊपर स्थापित और कॉन्फ़िगर किया हुआ।  
- **Aspose.CAD for Java** – नवीनतम JAR [here](https://releases.aspose.com/cad/java/) से डाउनलोड करें।  

## पैकेज आयात करें

शुरू करने के लिए, आपको अपने Java प्रोजेक्ट में आवश्यक क्लासेज़ आयात करने की जरूरत है। अपने स्रोत फ़ाइल में निम्नलिखित इम्पोर्ट स्टेटमेंट्स जोड़ें:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Aspose.CAD for Java का उपयोग करके DGN को PDF में कैसे निर्यात करें?

नीचे एक स्पष्ट, क्रमांकित walkthrough दिया गया है जो दिखाता है कि एम्बेडेड DGN फ़ाइल (जो एक DWG के अंदर संग्रहीत है) को PDF में कैसे बदलें।

### चरण 1: इनपुट और आउटपुट पाथ सेट करें

डायरेक्टरी को परिभाषित करें जिसमें आपका स्रोत फ़ाइल है और वह DWG निर्दिष्ट करें जिसमें एम्बेडेड DGN मौजूद है।

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### चरण 2: DWG फ़ाइल लोड करें

DWG फ़ाइल को एक `Image` ऑब्जेक्ट में लोड करें। Aspose.CAD स्वचालित रूप से एम्बेडेड DGN डेटा का पता लगाता है।

```java
Image objImage = Image.load(fileName);
```

### चरण 3: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

निर्धारित करें कि आप PDF में कौन‑से लेआउट(s) शामिल करना चाहते हैं। इस उदाहरण में हम केवल **Model** लेआउट निर्यात कर रहे हैं।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### चरण 4: PDF विकल्प कॉन्फ़िगर करें

रास्टराइज़ेशन सेटिंग्स को PDF निर्यात विकल्पों से जोड़ें।

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### चरण 5: PDF फ़ाइल सहेजें

अंत में, कॉन्फ़िगर किए गए विकल्पों का उपयोग करके PDF को डिस्क पर लिखें।

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## DWG को PDF में बदलें – एक अतिरिक्त टिप

यदि आपका स्रोत फ़ाइल एक साधारण DWG है (जिसमें एम्बेडेड DGN नहीं है), तो आप वही कोड पुनः उपयोग कर सकते हैं – केवल `fileName` को उस DWG की ओर इंगित करने के लिए बदलें जिसे आप बदलना चाहते हैं। रास्टराइज़ेशन और PDF विकल्प समान रहते हैं, जिससे आपको एक सुसंगत **DWG को PDF में बदलने** वर्कफ़्लो मिलता है।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|--------|----------|
| **Blank PDF output** | Layout name mismatch | Verify that the layout name passed to `setLayouts` exactly matches the layout in the source file (case‑sensitive). |
| **License exception** | Using the trial without a license | Apply a valid Aspose.CAD license before loading the image (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **File not found** | Incorrect `dataDir` path | Use an absolute path or ensure the relative path is correct relative to the project’s working directory. |
| **Low‑resolution graphics** | Default rasterization DPI is low | Set `rasterizationOptions.setPageWidth/Height` or `setResolution` to increase DPI. |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.CAD for Java को व्यावसायिक प्रोजेक्ट में उपयोग कर सकता हूँ?**  
A: हाँ, Aspose.CAD for Java एक वाणिज्यिक लाइब्रेरी है। आप लाइसेंस [here](https://purchase.aspose.com/buy) से प्राप्त कर सकते हैं।

**Q: क्या कोई मुफ्त ट्रायल उपलब्ध है?**  
A: हाँ, आप Aspose.CAD for Java का मुफ्त ट्रायल [here](https://releases.aspose.com/) से एक्सेस कर सकते हैं।

**Q: Aspose.CAD for Java के लिए समर्थन कैसे प्राप्त करूँ?**  
A: आप Aspose.CAD समुदाय से [forum](https://forum.aspose.com/c/cad/19) पर सहायता ले सकते हैं।

**Q: यदि मुझे एक अस्थायी लाइसेंस चाहिए तो?**  
A: आप अस्थायी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

**Q: दस्तावेज़ीकरण कहाँ मिल सकता है?**  
A: दस्तावेज़ीकरण उपलब्ध है [here](https://reference.aspose.com/cad/java/)।

## निष्कर्ष

आपने अब **CAD को PDF में निर्यात करना**, विशेष रूप से **DGN को PDF में बदलना** और यहाँ तक कि **DWG को PDF में बदलना** Aspose.CAD for Java का उपयोग करके सीख लिया है। ऊपर दिए गए चरणों का पालन करके, आप किसी भी Java‑आधारित समाधान में सहज CAD‑to‑PDF रूपांतरण को एकीकृत कर सकते हैं, जिससे उपयोगकर्ताओं को अतिरिक्त CAD सॉफ़्टवेयर की आवश्यकता के बिना उच्च‑गुणवत्ता वाले PDF प्रदान किए जा सकें।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**अंतिम अद्यतन:** 2026-01-07  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.12  
**लेखक:** Aspose