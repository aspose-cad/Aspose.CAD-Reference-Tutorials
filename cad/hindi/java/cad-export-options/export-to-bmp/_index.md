---
date: 2025-12-21
description: Aspose.CAD for Java का उपयोग करके DWG को BMP में बदलना और CAD को BMP
  में निर्यात करना इस चरण‑दर‑चरण गाइड के साथ सीखें।
linktitle: Export to BMP
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java के साथ DWG को BMP में कैसे बदलें
url: /hi/java/cad-export-options/export-to-bmp/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java के साथ DWG को BMP में बदलें

## परिचय

आधुनिक डिजिटल‑डिज़ाइन वर्कफ़्लो में, **DWG को BMP में बदलना** तेज़ और भरोसेमंद होना अत्यंत आवश्यक है। चाहे आप बैच‑प्रोसेसिंग सेवा बना रहे हों या एकल‑फ़ाइल रूपांतरण की आवश्यकता हो, Aspose.CAD for Java आपको एक मजबूत API प्रदान करता है जिससे आप **CAD को BMP में निर्यात** कर सकते हैं और रास्टराइज़ेशन सेटिंग्स पर पूर्ण नियंत्रण रख सकते हैं। इस ट्यूटोरियल में आप प्रत्येक चरण से गुजरेंगे—DWG फ़ाइल लोड करने से लेकर अंतिम BMP इमेज सहेजने तक—ताकि आप इस रूपांतरण को अपने Java एप्लिकेशन में आत्मविश्वास के साथ एकीकृत कर सकें।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी चाहिए?** Aspose.CAD for Java.  
- **क्या मैं DWG को BMP में एक ही लाइन कोड से बदल सकता हूँ?** नहीं, आपको फ़ाइल लोड करनी होगी, रास्टराइज़ेशन विकल्प सेट करने होंगे, और फिर सहेजना होगा।  
- **क्या प्रोडक्शन के लिए लाइसेंस आवश्यक है?** हाँ, एक व्यावसायिक लाइसेंस आवश्यक है; एक फ्री ट्रायल उपलब्ध है।  
- **क्या API बैच रूपांतरण का समर्थन करता है?** बिल्कुल—फ़ाइलों पर लूप करें और वही विकल्प पुनः उपयोग करें।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 और उसके बाद के संस्करण।

## “DWG को BMP में बदलना” क्या है?

DWG (AutoCAD ड्राइंग) फ़ाइल को BMP (बिटमैप) इमेज में बदलना वेक्टर डेटा को पिक्सेल‑आधारित फ़ॉर्मेट में रास्टराइज़ करता है। यह तब उपयोगी होता है जब आपको रिपोर्ट, थंबनेल, या वेब प्रीव्यू के लिए एक सार्वभौमिक रूप से देखी जा सकने वाली इमेज चाहिए, बिना CAD सॉफ़्टवेयर की आवश्यकता के।

## Aspose.CAD for Java के साथ CAD को BMP में निर्यात क्यों करें?

- **कोई बाहरी निर्भरताएँ नहीं** – शुद्ध Java, कोई नेटिव DLL नहीं।  
- **सूक्ष्म रास्टराइज़ेशन** – पेज आकार, लेआउट, एंटी‑एलियासिंग पर नियंत्रण।  
- **उच्च सटीकता** – लाइन वेट, रंग, और लेयर को संरक्षित रखता है।  
- **स्केलेबल** – एकल फ़ाइल या बड़े बैच जॉब दोनों के लिए उपयुक्त।

## पूर्वापेक्षाएँ

कोड में डुबकी लगाने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हों:

- **Aspose.CAD for Java लाइब्रेरी** – इसे [यहाँ](https://releases.aspose.com/cad/java/) से डाउनलोड करें।  
- **Java विकास वातावरण** – JDK 8+ और आपका पसंदीदा IDE।  
- **बुनियादी Java ज्ञान** – क्लास, मेथड, और फ़ाइल I/O की समझ।

## नेमस्पेस आयात करें

अपने Java प्रोजेक्ट में आवश्यक नेमस्पेस आयात करें ताकि आप Aspose.CAD की कार्यक्षमताओं तक पहुँच सकें:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.BmpOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## चरण 1: रिसोर्स डायरेक्टरी पाथ सेट करें

उस फ़ोल्डर को परिभाषित करें जिसमें वह DWG (या अन्य CAD) फ़ाइल हो जिसे आप बदलना चाहते हैं।

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

## चरण 2: CAD फ़ाइल लोड करें

स्रोत DWG फ़ाइल लोड करके एक `Image` ऑब्जेक्ट बनाएं।

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## चरण 3: BMP निर्यात विकल्प कॉन्फ़िगर करें

`BmpOptions` का एक इंस्टेंस बनाएं और एक `CadRasterizationOptions` ऑब्जेक्ट संलग्न करें जो वेक्टर डेटा के रास्टराइज़ेशन को नियंत्रित करता है।

```java
BmpOptions bmpOptions = new BmpOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## चरण 4: रास्टराइज़ेशन पैरामीटर सेट करें

पेज डायमेंशन समायोजित करें और यह निर्दिष्ट करें कि कौन‑से लेआउट रेंडर करने हैं। ये सेटिंग्स सीधे उत्पन्न BMP की गुणवत्ता और आकार को प्रभावित करती हैं।

```java
rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## चरण 5: BMP में निर्यात करें

आउटपुट पाथ प्रदान करें और BMP फ़ाइल लिखने के लिए `save` को कॉल करें।

```java
String outPath = dataDir + "site.bmp";
image.save(outPath, bmpOptions);
```

ऊपर बताए गए चरणों को प्रत्येक CAD फ़ाइल के लिए दोहराएँ जिसे आप **Aspose.CAD for Java** का उपयोग करके **DWG को BMP में बदलना** चाहते हैं।

## सामान्य समस्याएँ एवं सुझाव

- **गलत लेआउट नाम** – सुनिश्चित करें कि लेआउट स्ट्रिंग आपके DWG फ़ाइल में परिभाषित लेआउट्स में से किसी एक से मेल खाती हो (जैसे `"Model"` या `"Layout1"`)।  
- **कम‑रिज़ॉल्यूशन आउटपुट** – उच्च DPI परिणामों के लिए `PageWidth` और `PageHeight` बढ़ाएँ।  
- **मेमोरी खपत** – बहुत बड़े ड्रॉइंग्स के लिए, फ़ाइलों को एक‑एक करके प्रोसेस करें और प्रत्येक सहेजने के बाद `Image` ऑब्जेक्ट को डिस्पोज़ करें।

## अक्सर पूछे जाने वाले प्रश्न (FAQ's)

### Q1: क्या Aspose.CAD for Java बैच प्रोसेसिंग के लिए उपयुक्त है?

A1: बिल्कुल! Aspose.CAD for Java बैच प्रोसेसिंग का समर्थन करता है, जिससे आप कई CAD फ़ाइलों को एक साथ कुशलतापूर्वक संभाल सकते हैं।

### Q2: क्या मैं विभिन्न लेआउट्स के लिए रास्टराइज़ेशन विकल्प कस्टमाइज़ कर सकता हूँ?

A2: हाँ, आप पेज डायमेंशन और लेआउट्स जैसे रास्टराइज़ेशन विकल्पों को अपनी विशिष्ट आवश्यकताओं के अनुसार कस्टमाइज़ कर सकते हैं।

### Q3: Aspose.CAD for Java के लिए अतिरिक्त समर्थन कहाँ मिल सकता है?

A3: समुदाय समर्थन और चर्चा के लिए [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) देखें।

### Q4: क्या कोई फ्री ट्रायल उपलब्ध है?

A4: हाँ, आप Aspose.CAD for Java का फ्री ट्रायल [यहाँ](https://releases.aspose.com/) से एक्सप्लोर कर सकते हैं।

### Q5: मैं अस्थायी लाइसेंस कैसे प्राप्त करूँ?

A5: Aspose.CAD for Java के लिए अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) प्राप्त करें।

## अक्सर पूछे जाने वाले प्रश्न (Frequently Asked Questions)

**प्रश्न: क्या मैं अन्य CAD फ़ॉर्मेट (जैसे DXF, DGN) को BMP में बदल सकता हूँ?**  
उत्तर: हाँ, वही API DXF, DGN, DWF और अन्य समर्थित फ़ॉर्मेट्स के साथ काम करता है।

**प्रश्न: क्या रूपांतरण लेयर विज़िबिलिटी को संरक्षित रखता है?**  
उत्तर: डिफ़ॉल्ट रूप से सभी दृश्यमान लेयर रास्टराइज़्ड होते हैं; आवश्यकता पड़ने पर `CadRasterizationOptions` के माध्यम से लेयर को छिपाया जा सकता है।

**प्रश्न: क्या BMP के लिए बैकग्राउंड कलर सेट करना संभव है?**  
उत्तर: हाँ, सहेजने से पहले `rasterizationOptions.setBackgroundColor(Color.getWhite());` का उपयोग करें।

**प्रश्न: पासवर्ड‑प्रोटेक्टेड CAD फ़ाइलों को कैसे हैंडल करूँ?**  
उत्तर: फ़ाइल को `Image.load(fileName, loadOptions)` के साथ लोड करें जहाँ `loadOptions` में पासवर्ड शामिल हो।

**प्रश्न: बड़े बैच के लिए प्रदर्शन सुधारने का सबसे अच्छा तरीका क्या है?**  
उत्तर: एक ही `BmpOptions` इंस्टेंस को पुनः उपयोग करें और प्रत्येक इटरेशन के लिए केवल इनपुट फ़ाइल पाथ बदलें।

## निष्कर्ष

इस गाइड का पालन करके, अब आपके पास **DWG को BMP में बदलने** और **Aspose.CAD for Java के साथ CAD को BMP में निर्यात करने** की ठोस नींव है। इन चरणों को अपने एप्लिकेशन में एकीकृत करें ताकि इमेज जेनरेशन को ऑटोमेट कर सकें, थंबनेल बना सकें, या डाउनस्ट्रीम प्रोसेसिंग के लिए एसेट तैयार कर सकें।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**अंतिम अपडेट:** 2025-12-21  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.11  
**लेखक:** Aspose