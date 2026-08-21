---
date: 2026-05-04
description: Aspose.CAD for Java का उपयोग करके DGN को AutoCAD PDF में निर्यात करके
  CAD PDF फ़ाइलों को कैसे बदलें, सीखें। अनुकूलन योग्य PDF आकार और विकल्पों के साथ
  चरण‑दर‑चरण गाइड।
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: ऑटोकैड फ़ॉर्मेट में DGN को PDF में निर्यात करना
second_title: Aspose.CAD Java API
title: CAD PDF रूपांतरण – Aspose.CAD for Java के साथ DGN से AutoCAD PDF निर्यात आसान
url: /hi/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD PDF रूपांतरण: Aspose.CAD for Java के साथ DGN से AutoCAD PDF निर्यात आसान

## परिचय

यदि आपको DGN स्रोतों से सीधे **convert CAD PDF** फ़ाइलें बदलनी हैं, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में हम आपको Aspose.CAD for Java का उपयोग करके DGN फ़ाइलों को AutoCAD‑संगत PDF में निर्यात करने की प्रक्रिया दिखाएंगे। आप देखेंगे कि कैसे कस्टम पेज डाइमेंशन सेट करें, विशिष्ट लेआउट चुनें, और PDF आउटपुट को फाइन‑ट्यून करें—सभी स्पष्ट, चरण‑दर‑चरण कोड के साथ जिसे आप अपने प्रोजेक्ट में जोड़ सकते हैं।

## त्वरित उत्तर
- **convert CAD PDF** का क्या अर्थ है? यह CAD स्रोत फ़ाइलों (जैसे DGN) को ऐसे PDF में बदलने को दर्शाता है जो वेक्टर डेटा और लेआउट की सटीकता को बरकरार रखता है।  
- **कौन सी लाइब्रेरी रूपांतरण संभालती है?** Aspose.CAD for Java इस कार्य के लिए एक विश्वसनीय, लाइसेंस‑मुक्त ट्रायल प्रदान करता है।  
- **क्या विकास के लिए लाइसेंस आवश्यक है?** परीक्षण के लिए मुफ्त ट्रायल काम करता है; उत्पादन उपयोग के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं PDF आकार को अनुकूलित कर सकता हूँ?** हाँ – `CadRasterizationOptions` आपको पेज की चौड़ाई, ऊँचाई और स्केलिंग सेट करने की अनुमति देता है।  
- **कोड की कितनी पंक्तियों की आवश्यकता है?** PDF को लोड, कॉन्फ़िगर और सहेजने के लिए 20 से कम Java कोड पंक्तियों की आवश्यकता होती है।

## “convert CAD PDF” क्या है?
CAD PDF रूपांतरण का मतलब है मूल CAD ड्राइंग (जैसे DGN) को लेकर ऐसा PDF बनाना जो मूल वेक्टर ग्राफिक्स, लेयर्स और लेआउट जानकारी को बरकरार रखे। परिणामी PDF को किसी भी डिवाइस पर CAD सॉफ़्टवेयर की आवश्यकता के बिना देखा जा सकता है, जिससे यह साझा करने, प्रिंट करने या संग्रहित करने के लिए आदर्श बन जाता है।

## CAD PDF रूपांतरण के लिए Aspose.CAD for Java का उपयोग क्यों करें?
- **पूर्ण फ़ॉर्मेट समर्थन** – DGN, DWG, DXF, और कई अन्य।  
- **कोई बाहरी निर्भरताएँ नहीं** – शुद्ध Java, कोई नेटिव DLL नहीं।  
- **सूक्ष्म नियंत्रण** – आप चुन सकते हैं कि कौन से लेआउट निर्यात करने हैं, कस्टम पेज साइज सेट करें, और रास्टराइज़ेशन गुणवत्ता को नियंत्रित करें।  
- **बैच जॉब्स के लिए स्केलेबल** – लूप में दर्जनों फ़ाइलों को लोड और सहेजें, न्यूनतम ओवरहेड के साथ।

## पूर्वापेक्षाएँ
Before we dive in, ensure you have the following:

- **Aspose.CAD लाइब्रेरी** – इसे [यहाँ](https://releases.aspose.com/cad/java/) डाउनलोड करें।  
- **डॉक्यूमेंट डायरेक्टरी** – आपके मशीन पर एक फ़ोल्डर जहाँ इनपुट DGN फ़ाइलें और आउटपुट PDFs रखे जाएंगे।

## पैकेज आयात करें

In your Java project, import the necessary packages to access Aspose.CAD functionalities:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## चरण 1: फ़ाइल पथ निर्धारित करें (dgn निर्यात कैसे करें)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

सुनिश्चित करें कि `"Your Document Directory"` को अपने फ़ाइलों के वास्तविक पथ से बदलें।

## चरण 2: DGN इमेज लोड करें

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Aspose.CAD का उपयोग करके DGN फ़ाइल लोड करें।

## चरण 3: PDF निर्यात विकल्प सेट करें (pdf आकार अनुकूलित करें, pdf विकल्प सेट करें)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

यहाँ हम PDF निर्यात विकल्प परिभाषित करते हैं, जिसमें पेज डाइमेंशन, ऑटोमैटिक स्केलिंग, और विशिष्ट DGN लेआउट (व्यू) शामिल हैं जिन्हें आप अंतिम PDF में शामिल करना चाहते हैं।

## चरण 4: PDF फ़ाइल सहेजें

```java
objImage.save(outFile, options);
```

निर्यातित PDF फ़ाइल सहेजें। `save` मेथड पिछले चरण में कॉन्फ़िगर किए गए सभी विकल्पों को लागू करता है।

इन चरणों को किसी भी अतिरिक्त DGN फ़ाइलों के लिए दोहराएँ जिन्हें आप बदलना चाहते हैं। बधाई हो! आपने Aspose.CAD for Java का उपयोग करके DGN फ़ाइलों को AutoCAD फ़ॉर्मेट में PDF के रूप में निर्यात करके सफलतापूर्वक **convert CAD PDF** किया है।

## सामान्य समस्याएँ और समाधान
| Issue | Why it Happens | Fix |
|-------|----------------|-----|
| **फ़ाइल नहीं मिली** | गलत `dataDir` पथ | फ़ोल्डर पथ को दोबारा जाँचें और सुनिश्चित करें कि DGN फ़ाइल मौजूद है। |
| **PDF में खाली पृष्ठ** | `AutomaticLayoutsScaling` को `false` सेट किया गया है या लेआउट IDs गायब हैं | `setAutomaticLayoutsScaling(true)` रखें और लेआउट नामों (`"1","2",…`) की जाँच करें। |
| **कम‑रिज़ॉल्यूशन आउटपुट** | डिफ़ॉल्ट रास्टराइज़ेशन DPI कम है | गुणवत्ता बढ़ाने के लिए `vectorOptions.setResolution(300);` उपयोग करें ( `setVectorRasterizationOptions` से पहले जोड़ें)। |
| **लाइसेंस अपवाद** | उत्पादन में वैध लाइसेंस के बिना चलाना | Aspose दस्तावेज़ में वर्णित अनुसार एक अस्थायी या खरीदा गया लाइसेंस लागू करें। |

## अक्सर पूछे जाने वाले प्रश्न (अतिरिक्त)

**Q: क्या मैं बहु‑लेआउट DGN फ़ाइल से केवल एक लेआउट निर्यात कर सकता हूँ?**  
A: हाँ – इच्छित लेआउट IDs को `vectorOptions.setLayouts(new String[] { "2" });` में निर्दिष्ट करें।

**Q: क्या परिणामी PDF में फ़ॉन्ट एम्बेड करना संभव है?**  
A: Aspose.CAD आवश्यक फ़ॉन्ट्स को स्वचालित रूप से एम्बेड करता है जब वेक्टर डेटा रास्टराइज़ किया जाता है; यदि आवश्यक हो तो आप `PdfOptions` के माध्यम से फ़ॉन्ट एम्बेडिंग को नियंत्रित भी कर सकते हैं।

**Q: मैं कई DGN फ़ाइलों को बैच में कैसे प्रोसेस करूँ?**  
A: चरणों को एक `for` लूप में रखें जो फ़ाइल नामों की सूची पर इटररेट करता है, प्रत्येक इटरशन के लिए समान `PdfOptions` इंस्टेंस का पुनः उपयोग करते हुए।

**Q: क्या लाइब्रेरी पासवर्ड‑सुरक्षित PDFs का समर्थन करती है?**  
A: हाँ – आप `PdfOptions` ऑब्जेक्ट पर `options.setPassword("yourPassword");` के माध्यम से पासवर्ड सेट कर सकते हैं।

**Q: मैं और उदाहरण कहाँ पा सकता हूँ?**  
A: आधिकारिक Aspose.CAD दस्तावेज़ और सैंपल रिपॉज़िटरी में कई अतिरिक्त परिदृश्य शामिल हैं।

## FAQ (मूल)

### Q1: क्या Aspose.CAD सभी CAD फ़ाइल फ़ॉर्मेट्स के साथ संगत है?
A1: हाँ, Aspose.CAD कई CAD फ़ॉर्मेट्स को सपोर्ट करता है, जिससे विभिन्न फ़ाइल प्रकारों को संभालने में बहुमुखी प्रतिभा मिलती है।

### Q2: क्या मैं PDF निर्यात सेटिंग्स को अनुकूलित कर सकता हूँ?
A2: बिल्कुल। ट्यूटोरियल में दिखाए अनुसार, आप पेज डाइमेंशन और लेआउट जैसी विकल्पों को अपनी आवश्यकताओं के अनुसार समायोजित कर सकते हैं।

### Q3: मैं अतिरिक्त समर्थन या सहायता कहाँ पा सकता हूँ?
A3: समुदाय समर्थन और चर्चा के लिए [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) पर जाएँ।

### Q4: क्या कोई मुफ्त ट्रायल उपलब्ध है?
A4: हाँ, आप मुफ्त ट्रायल [यहाँ](https://releases.aspose.com/) से एक्सेस कर सकते हैं।

### Q5: मैं अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?
A5: अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) प्राप्त करें।

## निष्कर्ष

इस ट्यूटोरियल में हमने Aspose.CAD for Java का उपयोग करके **convert CAD PDF** फ़ाइलों को कैसे बदलें, इसका अन्वेषण किया। कुछ ही कोड पंक्तियों से आप DGN ड्राइंग लोड कर सकते हैं, PDF निर्यात विकल्पों को फाइन‑ट्यून कर सकते हैं, और उच्च‑गुणवत्ता वाले PDFs बना सकते हैं जो साझा करने या संग्रहित करने के लिए तैयार हैं। विभिन्न पेज साइज, लेआउट, या बैच प्रोसेसिंग के साथ प्रयोग करने में संकोच न करें ताकि आपके प्रोजेक्ट की आवश्यकताओं के अनुरूप हो सके।

---

**अंतिम अपडेट:** 2026-05-04  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}