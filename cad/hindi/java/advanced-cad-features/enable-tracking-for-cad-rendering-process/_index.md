---
date: 2025-12-07
description: Aspose.CAD for Java का उपयोग करके CAD को PDF में बदलते समय PDF पेज आकार
  कैसे सेट करें, सीखें। ट्रैकिंग सक्षम करने, CAD को PDF में बदलने और CAD को PDF के
  रूप में कुशलतापूर्वक सहेजने के लिए इस चरण‑दर‑चरण गाइड का पालन करें।
language: hi
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: PDF पेज आकार कैसे सेट करें और CAD रेंडरिंग प्रक्रिया के लिए ट्रैकिंग सक्षम
  करें
url: /java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD रेंडरिंग प्रक्रिया के लिए ट्रैकिंग सक्षम करें

## परिचय

इस ट्यूटोरियल में आप सीखेंगे कि **Aspose.CAD for Java** का उपयोग करके **CAD को PDF में बदलते** समय **PDF पेज आकार कैसे सेट करें**। ट्रैकिंग सक्षम करने से आपको रेंडरिंग पाइपलाइन की पूरी दृश्यता मिलती है, जिससे CAD फ़ाइलों (जैसे DXF) को PDF में परिवर्तित करने के दौरान डिबग करना और अनुकूलन करना आसान हो जाता है। चाहे आपको **CAD को PDF के रूप में सहेजना** हो, DXF से PDF बनाना हो, या केवल आउटपुट आयामों को नियंत्रित करना हो, नीचे दिए गए चरण आपको पूरी प्रक्रिया के माध्यम से ले जाएंगे।

## त्वरित उत्तर
- **“PDF पेज आकार सेट करें” क्या करता है?** यह CAD रेंडरिंग के दौरान उत्पन्न PDF पेज की चौड़ाई और ऊँचाई निर्धारित करता है।  
- **ट्रैकिंग क्यों सक्षम करें?** ट्रैकिंग प्रत्येक परिवर्तन चरण को लॉग करती है, जिससे आप प्रदर्शन बाधाओं या त्रुटियों को पहचान सकते हैं।  
- **क्या मुझे लाइसेंस चाहिए?** मूल्यांकन के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए व्यावसायिक लाइसेंस आवश्यक है।  
- **कौन से CAD फ़ॉर्मेट समर्थित हैं?** DWG, DXF, DGN और कई अन्य – पूर्ण सूची के लिए Aspose.CAD दस्तावेज़ीकरण देखें।  
- **क्या मैं पेज आयामों को तुरंत बदल सकता हूँ?** हाँ – बस `CadRasterizationOptions` में `PageWidth` और `PageHeight` मानों को समायोजित करें।

## CAD रेंडरिंग में “PDF पेज आकार सेट करें” क्या है?

PDF पेज आकार सेट करने से रास्टराइज़र को बताया जाता है कि वेक्टर CAD डेटा को PDF पेज में रास्टराइज़ करते समय कैनवास कितना बड़ा होना चाहिए। यह दृश्य सटीकता बनाए रखने के लिए महत्वपूर्ण है, विशेषकर विस्तृत इंजीनियरिंग ड्रॉइंग्स के साथ काम करते समय।

## CAD रेंडरिंग के लिए ट्रैकिंग क्यों सक्षम करें?

ट्रैकिंग सक्षम करने से प्रत्येक चरण का विस्तृत लॉग मिलता है—स्रोत फ़ाइल लोड करने से लेकर PDF आउटपुट लिखने तक। यह आपको मदद करता है:

- किसी विशेष ड्रॉइंग के गलत रेंडर होने का कारण पहचानना।  
- प्रत्येक चरण में लगने वाले समय को मापना, जो प्रदर्शन ट्यूनिंग के लिए उपयोगी है।  
- यह सत्यापित करना कि आप द्वारा कॉन्फ़िगर किया गया पेज आकार वास्तव में लागू हुआ है।

## पूर्वापेक्षाएँ

ट्रैकिंग सेटअप में जाने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हों:

1. **Java विकास पर्यावरण** – आपके मशीन पर Java 8 या बाद का संस्करण स्थापित हो।  
2. **Aspose.CAD लाइब्रेरी** – Aspose.CAD लाइब्रेरी को डाउनलोड करके अपने Java प्रोजेक्ट में एकीकृत करें। आप डाउनलोड लिंक [यहाँ](https://releases.aspose.com/cad/java/) पा सकते हैं।  
3. **डॉक्यूमेंट डायरेक्टरी** – एक डायरेक्टरी तैयार करें जहाँ आप अपनी CAD फ़ाइलें और उत्पन्न PDF संग्रहीत करेंगे।

## नेमस्पेस आयात करें

अपने Java प्रोजेक्ट में Aspose.CAD कार्यात्मकताओं का उपयोग करने के लिए आवश्यक नेमस्पेस आयात करें। कोड की शुरुआत में निम्नलाइनों को जोड़ें:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## संसाधन निर्देशिका पथ सेट करें

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

`"Your Document Directory"` को अपने डॉक्यूमेंट डायरेक्टरी के वास्तविक पथ से बदलें।

## CAD फ़ाइल लोड करें

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

अपनी CAD फ़ाइल का पथ निर्दिष्ट करें, यह सुनिश्चित करते हुए कि वह निर्दिष्ट डॉक्यूमेंट डायरेक्टरी के भीतर हो।

## PDF आउटपुट विकल्प सेट करें

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

एक आउटपुट स्ट्रीम बनाएं और परिवर्तन के लिए PDF विकल्प सेट करें।

## CadRasterizationOptions कॉन्फ़िगर करें (PDF पेज आकार सेट करें)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

यहाँ हम `PageWidth` और `PageHeight` को परिभाषित करके **PDF पेज आकार सेट** करते हैं। इन मानों को अपने इंजीनियरिंग ड्रॉइंग की आवश्यक आयामों के अनुसार समायोजित करें। यह चरण सीधे इस बात को प्रभावित करता है कि CAD सामग्री अंतिम PDF में कैसे स्केल और रेंडर होगी।

## PDF फ़ाइल सहेजें

```java
image.save(stream, pdfOptions);
```

निर्दिष्ट विकल्पों के साथ रेंडर की गई PDF फ़ाइल को सहेजें।

## ट्रैकिंग सक्षम होने की पुष्टि करें

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

सुनिश्चित करें कि CAD रेंडरिंग प्रक्रिया के लिए ट्रैकिंग सफलतापूर्वक सक्षम है।

## सामान्य समस्याएँ एवं ट्रबलशूटिंग

| लक्षण | संभावित कारण | समाधान |
|---------|--------------|-----|
| PDF पेज खाली दिखता है | `PageWidth`/`PageHeight` को 0 पर सेट किया गया | शून्य‑से‑भिन्न आयाम प्रदान करें। |
| आउटपुट फ़ाइल भ्रष्ट है | आउटपुट स्ट्रीम बंद नहीं हुई | `image.save(...)` के बाद `stream.close()` कॉल करें। |
| PDF में लेयर्स गायब हैं | CAD फ़ाइल में असमर्थित एंटिटीज़ हैं | सत्यापित करें कि फ़ाइल फ़ॉर्मेट Aspose.CAD द्वारा पूरी तरह समर्थित है। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD सभी CAD फ़ाइल फ़ॉर्मेट के साथ संगत है?

A1: Aspose.CAD कई CAD फ़ॉर्मेट का समर्थन करता है, जिसमें DWG, DXF, DGN और अधिक शामिल हैं। विस्तृत सूची के लिए [दस्तावेज़ीकरण](https://reference.aspose.com/cad/java/) देखें।

### Q2: क्या मैं PDF फ़ाइल के आउटपुट आयामों को कस्टमाइज़ कर सकता हूँ?

A2: बिल्कुल! आउटपुट आयामों को अनुकूलित करने के लिए `CadRasterizationOptions` में `PageWidth` और `PageHeight` पैरामीटर को समायोजित करें।

### Q3: क्या Aspose.CAD for Java के लिए कोई मुफ्त ट्रायल उपलब्ध है?

A3: हाँ, आप Aspose.CAD की क्षमताओं को एक मुफ्त ट्रायल [यहाँ](https://releases.aspose.com/) प्राप्त करके आज़मा सकते हैं।

### Q4: Aspose.CAD‑संबंधित प्रश्नों के लिए मैं समुदाय समर्थन कैसे प्राप्त करूँ?

A4: समुदाय के साथ जुड़ने और सहायता प्राप्त करने के लिए [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) पर जाएँ।

### Q5: क्या Aspose.CAD के लिए अस्थायी लाइसेंस उपलब्ध हैं?

A5: हाँ, यदि आपको अस्थायी लाइसेंस चाहिए, तो आप इसे [यहाँ](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

## निष्कर्ष

बधाई हो! अब आप **Aspose.CAD for Java** का उपयोग करके **PDF पेज आकार सेट** करने और CAD रेंडरिंग के लिए ट्रैकिंग सक्षम करने में सक्षम हैं। यह गाइड आपको **CAD को PDF में बदलने**, **CAD को PDF के रूप में सहेजने**, और DXF से PDF उत्पन्न करने में पूर्ण पेज आयाम नियंत्रण और विस्तृत निष्पादन लॉग प्रदान करता है। विभिन्न पेज आकारों के साथ प्रयोग करने और अपने विशिष्ट इंजीनियरिंग वर्कफ़्लो के अनुरूप अतिरिक्त रास्टराइज़ेशन विकल्पों का अन्वेषण करने में संकोच न करें।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**अंतिम अपडेट:** 2025-12-07  
**परीक्षण किया गया:** Aspose.CAD for Java 24.12 (लेखन के समय नवीनतम)  
**लेखक:** Aspose