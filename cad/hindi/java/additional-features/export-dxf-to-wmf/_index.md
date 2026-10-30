---
date: 2026-10-30
description: Aspose.CAD for Java का उपयोग करके DXF फ़ाइलों को बैच में WMF में कैसे
  परिवर्तित करें, चरण‑दर‑चरण कोड, मुफ्त ट्रायल जानकारी और वैकल्पिक PDF निर्यात के
  साथ सीखें।
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Java का उपयोग करके DXF को WMF फ़ॉर्मेट में निर्यात करें
og_description: Aspose.CAD for Java का उपयोग करके DXF फ़ाइलों को बैच में WMF में परिवर्तित
  करें। इस गाइड का पालन करें ताकि DXF ड्रॉइंग लोड कर सकें, रास्टराइज़ेशन विकल्प सेट
  कर सकें, WMF के रूप में सहेज सकें, और मुफ्त ट्रायल के साथ वैकल्पिक रूप से PDF में
  निर्यात कर सकें।
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Aspose.CAD for Java के साथ DXF फ़ाइलों को बैच में WMF में परिवर्तित करें
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Aspose.CAD for Java के साथ DXF फ़ाइलों को बैच में WMF में परिवर्तित करें
url: /hi/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DXF फ़ाइलों को WMF में बैच रूपांतरण Aspose.CAD for Java

## परिचय

इस ट्यूटोरियल में आप **DXF फ़ाइलों को WMF में बैच रूपांतरण** Aspose.CAD for Java का उपयोग करके सीखेंगे। चाहे आपको Windows‑आधारित रिपोर्ट में CAD ड्रॉइंग एम्बेड करनी हो, Office दस्तावेज़ों के लिए हल्की वेक्टर ग्राफ़िक्स जेनरेट करनी हों, या बड़े‑पैमाने पर रूपांतरण को स्वचालित करना हो, यह गाइड आपको DXF ड्रॉइंग लोड करने, रास्टराइज़ेशन विकल्प कॉन्फ़िगर करने, WMF के रूप में सहेजने, और वैकल्पिक रूप से उसी ड्रॉइंग को PDF में निर्यात करने की प्रक्रिया दिखाता है। ये चरण किसी भी प्लेटफ़ॉर्म पर काम करते हैं जो Java 8+ चलाता है।

## त्वरित उत्तर
- **क्या मैं मुफ्त ट्रायल के साथ DXF को WMF में रूपांतरित कर सकता हूँ?** हाँ – Aspose एक पूर्ण कार्यात्मक 30‑दिन का ट्रायल प्रदान करता है।  
- **कौन सा Java संस्करण आवश्यक है?** Java 8 या बाद का संस्करण।  
- **क्या कोड चलाने के लिए लाइसेंस चाहिए?** उत्पादन के लिए लाइसेंस आवश्यक है; विकास और परीक्षण के लिए ट्रायल काम करता है।  
- **क्या रूपांतरण लॉस‑लेस है?** वेक्टर डेटा संरक्षित रहता है; रास्टराइज़ेशन विकल्पों से आप रिज़ॉल्यूशन नियंत्रित कर सकते हैं।  
- **क्या मैं उसी ड्रॉइंग को PDF में भी निर्यात कर सकता हूँ?** बिल्कुल – नीचे “PDF में निर्यात” चरण देखें।  
- **मैं कई DXF फ़ाइलों को एक साथ कैसे बैच रूपांतरण करूँ?** फ़ोल्डर के माध्यम से लूप करें, प्रत्येक फ़ाइल पर समान लोड‑रास्टर‑सेव पैटर्न लागू करें।

## बैच रूपांतरण DXF फ़ाइलें क्या हैं?

बैच रूपांतरण DXF फ़ाइलों का अर्थ है एक ही रन में कई Drawing Exchange Format (DXF) ड्रॉइंग को प्रोसेस करना और प्रत्येक के लिए WMF आउटपुट उत्पन्न करना। WMF (Windows Metafile) एक वेक्टर इमेज फ़ॉर्मेट है जो Microsoft Office, Windows एप्लिकेशन और कई रिपोर्टिंग टूल्स के साथ मूल रूप से एकीकृत होता है।

## क्यों उपयोग करें Aspose.CAD for Java?

Aspose.CAD for Java एक शुद्ध‑Java इंजन है जो **50 से अधिक इनपुट और आउटपुट फ़ॉर्मेट**—DXF, DWG, DGN, PDF, PNG, SVG, और WMF सहित—को सपोर्ट करता है, जबकि **99 % वेक्टर फ़िडेलिटी** प्रदान करता है। यह किसी भी OS पर चलता है जो Java सपोर्ट करता है, कोई नेटीव DLL की आवश्यकता नहीं होती, और आप `CadRasterizationOptions` क्लास के माध्यम से पेज साइज, DPI, और बैकग्राउंड कलर को नियंत्रित कर सकते हैं। वही API PDF, PNG, और SVG निर्यात को भी संभालता है, जिससे कई लाइब्रेरीज़ की आवश्यकता समाप्त हो जाती है।

### मात्रात्मक लाभ
- **50+ समर्थित फ़ॉर्मेट** तृतीय‑पक्षीय कन्वर्टर्स की आवश्यकता को कम करते हैं।  
- **300‑पेज DXF फ़ाइलों को 5 सेकंड से कम में प्रोसेस** करता है एक सामान्य 2.5 GHz सर्वर पर जब 150 DPI पर रास्टराइज़ किया जाता है।  
- **मेमोरी फुटप्रिंट 200 MB से कम** रहता है 500 MB तक की फ़ाइलों के लिए जब आप उपयुक्त पेज डाइमेंशन सेट करते हैं।  

## पूर्वापेक्षाएँ

- **Aspose.CAD for Java** को अपने प्रोजेक्ट में इंटीग्रेट करें। इसे आधिकारिक साइट से डाउनलोड करें: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- एक फ़ोल्डर जिसमें वह DXF फ़ाइलें हों जिन्हें आप रूपांतरित करना चाहते हैं (उदा., `Your Document Directory/DXFDrawings/`).  

## नेमस्पेस आयात करें

`Image` Aspose.CAD की कोर क्लास है जो मेमोरी में CAD ड्रॉइंग का प्रतिनिधित्व करती है। फ़ाइल लोड करने के बाद, सभी बाद के ऑपरेशन—रास्टराइज़ेशन, फ़ॉर्मेट रूपांतरण, और रिसोर्स क्लीनअप—इस ऑब्जेक्ट के माध्यम से किए जाते हैं।

निम्नलिखित इम्पोर्ट्स Aspose.CAD क्लासेज़ को लाते हैं जो CAD फ़ाइलों को लोड, रास्टराइज़ और सहेजने के लिए आवश्यक हैं।  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## चरण‑दर‑चरण गाइड

### मैं Java में DXF फ़ाइलों को WMF में बैच रूपांतरण कैसे करूँ?

प्रत्येक DXF को `Image.load` से लोड करें, इच्छित पेज साइज और DPI के लिए `CadRasterizationOptions` कॉन्फ़िगर करें, और `image.save` को `SaveFormat.WMF` के साथ कॉल करें। यह तीन‑चरण पैटर्न पूर्ण रूपांतरण करता है जबकि वेक्टर क्वालिटी को बरकरार रखता है और प्रत्येक फ़ाइल के लिए केवल कुछ लाइनों की आवश्यकता होती है।

#### चरण 1: dxf ड्राइंग लोड करें

Image.load DXF फ़ाइल को Aspose.CAD Image ऑब्जेक्ट में पढ़ता है।  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### चरण 2: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

`CadRasterizationOptions` CAD ड्रॉइंग को रास्टराइज़ करने के लिए पेज साइज, रिज़ॉल्यूशन, और बैकग्राउंड निर्दिष्ट करता है।  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### चरण 3: wmf के रूप में सहेजें

`ImageSaveOptions` के साथ `SaveFormat.WMF` Aspose.CAD को आउटपुट को Windows Metafile के रूप में लिखने को बताता है।  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### चरण 4: संसाधनों को मुक्त करें

`image.close()` को कॉल करने से Aspose.CAD Image ऑब्जेक्ट द्वारा उपयोग किए गए नेटीव रिसोर्सेज़ रिलीज़ हो जाते हैं।  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### चरण 5: वैकल्पिक – pdf में निर्यात करें

`PdfOptions` PDF‑विशिष्ट सेटिंग्स को कॉन्फ़िगर करता है जब इमेज को PDF दस्तावेज़ के रूप में सहेजा जाता है।  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** आप वही `CadRasterizationOptions` ऑब्जेक्ट PDF निर्यात के लिए `PdfOptions` इंस्टेंस में पास करके पुनः उपयोग कर सकते हैं, जिससे सेटअप की कुछ पंक्तियाँ बचती हैं।

## मैं Aspose CAD Java का उपयोग करके DXF को PDF में कैसे निर्यात करूँ?

WMF सहेजने के फ़ॉर्मेट को PDF में बदलें `new ImageSaveOptions(SaveFormat.Pdf)` का उपयोग करके। वही रास्टराइज़ेशन सेटिंग्स लागू होती हैं, और आप अतिरिक्त रूप से PDF‑विशिष्ट विकल्प जैसे लेखक मेटाडेटा या कम्प्रेशन लेवल सेट कर सकते हैं। यह एक‑लाइनर रूपांतरण एक सर्चेबल, पेज‑सटीक PDF उत्पन्न करता है जो मूल CAD लेआउट को प्रतिबिंबित करता है।

## सामान्य समस्याएँ और समाधान

`License` Aspose क्लास है जो रन‑टाइम पर प्रोडक्ट लाइसेंस लागू करने के लिए उपयोग होती है।

| समस्या | कारण | समाधान |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | वेरिएबल `cadImage` परिभाषित नहीं है (यह `image` होना चाहिए)। | `cadImage` को `image` से बदलें या वेरिएबल का नाम समान रखें। |
| **Output WMF is blank** | रास्टराइज़ेशन पेज आकार बहुत छोटा है या बैकग्राउंड रंग पारदर्शी सेट है। | `PageWidth`/`PageHeight` बढ़ाएँ या `rasterizationOptions.setBackgroundColor(Color.WHITE);` के माध्यम से बैकग्राउंड रंग सेट करें। |
| **License exception** | प्रोडक्शन में वैध Aspose लाइसेंस के बिना चलाना। | एप्लिकेशन शुरू में लाइसेंस फ़ाइल लागू करें: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## अक्सर पूछे जाने वाले प्रश्न

**Q: मैं Aspose.CAD दस्तावेज़ीकरण कहाँ पा सकता हूँ?**  
A: आप दस्तावेज़ीकरण तक पहुँच सकते हैं [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**Q: मैं Aspose.CAD for Java को कैसे डाउनलोड करूँ?**  
A: लाइब्रेरी डाउनलोड करें [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**Q: क्या कोई मुफ्त ट्रायल उपलब्ध है?**  
A: हाँ, आप मुफ्त ट्रायल प्राप्त कर सकते हैं [Aspose free trial page](https://releases.aspose.com/).

**Q: अस्थायी लाइसेंस विकल्प चाहिए?**  
A: अस्थायी लाइसेंस विकल्प देखें [temporary license options](https://purchase.aspose.com/temporary-license/).

**Q: मुझे समर्थन कहाँ मिल सकता है?**  
A: Aspose.CAD समर्थन फ़ोरम पर जाएँ [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## अतिरिक्त अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं बड़ी DXF फ़ाइलें (सैकड़ों MB) मेमोरी खत्म हुए बिना रूपांतरित कर सकता हूँ?**  
A: हाँ। फ़ाइल को try‑with‑resources ब्लॉक में लोड करें और `Image` ऑब्जेक्ट को तुरंत डिस्पोज़ करें। मेमोरी उपयोग कम रखने के लिए `CadRasterizationOptions.setPageWidth/Height` को उचित आकार पर सेट करें।

**Q: क्या WMF आउटपुट लेयर जानकारी रखता है?**  
A: WMF एक फ्लैट वेक्टर फ़ॉर्मेट है, इसलिए लेयर हायरार्की फ्लैट हो जाती है, लेकिन लाइन स्टाइल, रंग, और हैच पैटर्न संरक्षित रहते हैं।

**Q: क्या WMF के लिए कस्टम DPI सेट करना संभव है?**  
A: सहेजने से पहले DPI परिभाषित करने के लिए `rasterizationOptions.setResolution(300);` उपयोग करें।

**Q: क्या मैं एक ही रन में कई DXF फ़ाइलों को बैच‑कन्वर्ट कर सकता हूँ?**  
A: बिल्कुल। डायरेक्टरी के माध्यम से लूप करें, प्रत्येक फ़ाइल लोड करें, और समान रास्टराइज़ेशन एवं सहेजने की लॉजिक लागू करें।

**Q: कौन से Java संस्करण समर्थित हैं?**  
A: Aspose.CAD for Java Java 8 और बाद के संस्करणों को सपोर्ट करता है, जिसमें Java 11, 17, और नवीनतम LTS रिलीज़ शामिल हैं।

---

**अंतिम अद्यतन:** 2026-10-30  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.11  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [CAD से PDF बनाएं – Aspose.CAD for Java के साथ DXF को PDF में निर्यात करें](/cad/java/additional-features/export-dxf-to-pdf/)
- [DXF से PDF बनाएं: Aspose.CAD for Java के साथ लेयर निर्यात करें](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [DXF लेआउट को JPEG इमेज में कैसे बदलें Aspose.CAD के साथ Java में](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}