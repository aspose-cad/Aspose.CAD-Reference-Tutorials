---
date: 2025-12-21
description: जानेँ कि Aspose.CAD for Java का उपयोग करके किसी विशिष्ट DWG लेआउट को
  PDF में निर्यात करके DWG को PDF में कैसे बदलें। अपने CAD कार्यप्रवाह को सुगम बनाने
  के लिए इस चरण‑दर‑चरण DWG‑से‑PDF ट्यूटोरियल का पालन करें।
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: DWG को PDF में बदलें – Aspose.CAD for Java के साथ लेआउट निर्यात करें
url: /hi/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG को PDF में बदलें – Aspose.CAD for Java का उपयोग करके विशिष्ट लेआउट निर्यात करें

## परिचय

कंप्यूटर‑एडेड डिज़ाइन (CAD) की गतिशील दुनिया में, **convert DWG to PDF** क्लाइंट्स, ठेकेदारों या गैर‑तकनीकी हितधारकों के साथ ड्रॉइंग्स साझा करने के लिए एक सामान्य आवश्यकता है। Aspose.CAD for Java इस रूपांतरण को सहज बनाता है, और यह आपको बहु‑लेआउट DWG फ़ाइल में से एकल लेआउट चुनने की सुविधा भी देता है। इस ट्यूटोरियल में हम **DWG‑विशिष्ट लेआउट को PDF में निर्यात करने** के चरणों को देखेंगे, ताकि आप अतिरिक्त पृष्ठों या मैन्युअल क्रॉपिंग के बिना ठीक वही प्रदान कर सकें जिसकी आपके प्रोजेक्ट को आवश्यकता है।

## त्वरित उत्तर
- **“convert DWG to PDF” का क्या अर्थ है?** यह DWG ड्रॉइंग को PDF दस्तावेज़ में बदलता है, जबकि वेक्टर डेटा और लेआउट की सटीकता को बरकरार रखता है।  
- **कौन सी लाइब्रेरी रूपांतरण संभालती है?** Aspose.CAD for Java एक तैयार‑उपयोग API प्रदान करती है।  
- **उत्पादन के लिए लाइसेंस आवश्यक है?** हाँ, एक व्यावसायिक लाइसेंस आवश्यक है; मूल्यांकन के लिए एक मुफ्त ट्रायल काम करता है।  
- **क्या मैं एकल लेआउट चुन सकता हूँ?** बिल्कुल – `Layouts` प्रॉपर्टी को इच्छित लेआउट नाम पर सेट करें।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 और बाद के संस्करण पूरी तरह संगत हैं।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हों:

- **Java विकास वातावरण** – JDK 8+ और आपका पसंदीदा IDE।  
- **Aspose.CAD लाइब्रेरी** – आधिकारिक साइट से नवीनतम JAR **[यहाँ](https://releases.aspose.com/cad/java/)** डाउनलोड करें।  
- **DWG फ़ाइल** – एक ड्रॉइंग जिसमें कम से कम एक लेआउट हो (उदाहरण के लिए *visualization_-_conference_room.dwg*)।  

## विशिष्ट DWG लेआउट को PDF में निर्यात क्यों करें?

कई DWG फ़ाइलों में कई पेपर स्पेस (लेआउट) होते हैं। पूरी फ़ाइल निर्यात करने से अनावश्यक पृष्ठों के साथ एक भारी PDF बन सकता है। एकल लेआउट चुनने से:

- फ़ाइल आकार घटता है।  
- दर्शक का ध्यान संबंधित ड्रॉइंग शीट पर केंद्रित रहता है।  
- प्रोजेक्ट दस्तावेज़ीकरण मानकों के साथ संरेखण होता है।  

## चरण‑दर‑चरण गाइड

### चरण 1: प्रोजेक्ट वातावरण सेट करें

एक नया Java प्रोजेक्ट (Maven, Gradle, या साधारण IDE) बनाएं और Aspose.CAD JAR को क्लासपाथ में जोड़ें। आप इसे **[यहाँ](https://releases.aspose.com/cad/java/)** डाउनलोड कर सकते हैं।

### चरण 2: आवश्यक पैकेज इम्पोर्ट करें

अपने Java क्लास में आवश्यक Aspose.CAD नेमस्पेस जोड़ें।

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### चरण 3: DWG फ़ाइल लोड करें

जिस DWG को आप बदलना चाहते हैं, उसका पथ दें और उसे `Image` ऑब्जेक्ट में लोड करें।

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### चरण 4: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

पृष्ठ आकार निर्धारित करें और, सबसे महत्वपूर्ण, वह लेआउट जिसे आप निर्यात करना चाहते हैं।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### चरण 5: PDF निर्यात विकल्प सेट करें

रास्टराइज़ेशन सेटिंग्स को PDF एक्सपोर्टर से जोड़ें।

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### चरण 6: DWG को PDF में निर्यात करें

परिणाम को PDF फ़ाइल के रूप में सहेजें। आउटपुट में केवल **Layout1** ही होगा, जिससे एक साफ़ **convert DWG to PDF** ऑपरेशन प्राप्त होगा।

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|------|--------|
| **लेआउट नहीं मिला** | लेआउट नाम गलत लिखा गया है या DWG में मौजूद नहीं है। | `image.getLayoutNames()` का उपयोग करके उपलब्ध लेआउट की सूची प्राप्त करें, फिर सही नाम चुनें। |
| **PDF की रेज़ॉल्यूशन कम** | `PageWidth`/`PageHeight` बहुत छोटे हैं। | आयाम बढ़ाएँ (उदाहरण: 2000 × 2000) या `rasterizationOptions.setResolution(300);` सेट करें। |
| **लाइसेंस अपवाद** | गैर‑ट्रायल वातावरण में वैध लाइसेंस नहीं है। | इमेज लोड करने से पहले अपना Aspose.CAD लाइसेंस लागू करें: `License license = new License(); license.setLicense("Aspose.CAD.lic");`। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न 1:** क्या मैं Aspose.CAD for Java को अन्य Java‑आधारित CAD लाइब्रेरी के साथ उपयोग कर सकता हूँ?  
**उत्तर:** Aspose.CAD for Java एक स्वतंत्र लाइब्रेरी है, लेकिन इसे विस्तारित कार्यक्षमताओं के लिए अन्य Java‑आधारित लाइब्रेरी के साथ एकीकृत किया जा सकता है।

**प्रश्न 2:** Aspose.CAD के लिए कौन‑से लाइसेंस विकल्प उपलब्ध हैं?  
**उत्तर:** हाँ, आप लाइसेंस विकल्पों का अन्वेषण कर सकते हैं और खरीद विवरण **[यहाँ](https://purchase.aspose.com/buy)** देख सकते हैं।

**प्रश्न 3:** मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त करूँ?  
**उत्तर:** अस्थायी लाइसेंस के लिए **[इस लिंक](https://purchase.aspose.com/temporary-license/)** पर जाएँ।

**प्रश्न 4:** Aspose.CAD के लिए समर्थन कहाँ मिल सकता है?  
**उत्तर:** किसी भी प्रश्न या सहायता के लिए **[Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19)** देखें।

**प्रश्न 5:** क्या Aspose.CAD का मुफ्त ट्रायल उपलब्ध है?  
**उत्तर:** हाँ, आप मुफ्त ट्रायल **[यहाँ](https://releases.aspose.com/)** से प्राप्त कर सकते हैं।

## निष्कर्ष

इस **dwg to pdf tutorial** को फॉलो करके, अब आपके पास एक विश्वसनीय तरीका है जिससे आप **convert DWG to PDF** करते समय केवल एकल लेआउट को लक्षित कर सकते हैं। यह दृष्टिकोण स्टोरेज बचाता है, दस्तावेज़ साझा करने की गति बढ़ाता है, और आपके CAD वर्कफ़्लो को व्यवस्थित रखता है। विभिन्न रास्टराइज़ेशन सेटिंग्स के साथ प्रयोग करने या कई लेआउट को एक ही PDF में संयोजित करने के लिए स्वतंत्र महसूस करें जैसे आपका प्रोजेक्ट विकसित होता है।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**अंतिम अपडेट:** 2025-12-21  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.12  
**लेखक:** Aspose