---
date: 2026-10-04
description: Aspose.CAD for Java का उपयोग करके DWG को PNG में तेज़ी से कैसे बदलें
  और CAD को PNG या अन्य रास्टर फ़ॉर्मेट में निर्यात करें, यह सीखें। तेज़ी से उच्च‑गुणवत्ता
  वाले परिणाम प्राप्त करें।
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: CAD लेआउट को रास्टर इमेज फ़ॉर्मेट में बदलें
og_description: Aspose.CAD for Java के साथ DWG को PNG में तेज़ी से बदलें। चरण‑दर‑चरण
  सीखें कि CAD को PNG, JPEG, TIFF और अन्य फ़ॉर्मेट में कैसे निर्यात करें।
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Aspose.CAD for Java का उपयोग करके DWG को PNG और अन्य रास्टर फ़ॉर्मेट में
  बदलें
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Aspose.CAD for Java का उपयोग करके DWG को PNG और अन्य रास्टर फ़ॉर्मेट में बदलें
url: /hi/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG को PNG और अन्य रास्टर फ़ॉर्मेट में Aspose.CAD for Java का उपयोग करके परिवर्तित करें

## परिचय

`Aspose.CAD for Java` को एक लाइब्रेरी है जो CAD फ़ाइलों को PNG, JPEG, और TIFF जैसे रास्टर इमेज में प्रोग्रामेटिक रूप से बदलने में सक्षम बनाती है। DWG को PNG (या अन्य रास्टर इमेज फ़ॉर्मेट) में बदलना एक सामान्य आवश्यकता है जब आपको CAD ड्रॉइंग्स को टीम के साथ साझा करना हो जो CAD व्यूअर नहीं रखते, डिज़ाइन को दस्तावेज़ीकरण में एम्बेड करना हो, या वेब गैलरी के लिए थंबनेल बनाना हो। इस गाइड में आप सीखेंगे कि कैसे dwg को png को तेज़ और भरोसेमंद तरीके से बदलें, चाहे आप पूर्ण‑ड्रॉइंग फ़ाइल के साथ काम कर रहे हों या केवल एक विशिष्ट लेआउट के साथ। आपको वेब प्रीव्यू, रिपोर्टिंग टूल्स, या मोबाइल ऐप्स के लिए **convert CAD to raster** करने की भी आवश्यकता पड़ सकती है।

## त्वरित उत्तर

- **DWG को PNG संभालने वाली लाइब्रेरी कौन सी है?** Aspose.CAD for Java रूपांतरण इंजन प्रदान करता है।  
- **मैं कौन से रास्टर फ़ॉर्मेट एक्सपोर्ट कर सकता हूँ?** PNG, JPEG, TIFF, PDF, BMP, और 30 से अधिक अतिरिक्त फ़ॉर्मेट।  
- **परीक्षण के लिए मुझे लाइसेंस चाहिए?** एक फ्री ट्रायल विकास के लिए काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं एक विशिष्ट लेआउट चुन सकता हूँ?** हाँ – `setLayouts` का उपयोग करके “Model”, “Layout1”, आदि को टार्गेट करें।  
- **क्या हाई‑रेज़ोल्यूशन आउटपुट संभव है?** बिल्कुल – DPI को नियंत्रित करने के लिए `setPageWidth` और `setPageHeight` (या `setResolution`) को समायोजित करें।

## “convert dwg to png” क्या है?

Convert dwg to png का मतलब है DWG वेक्टर ड्रॉइंग को पिक्सेल‑आधारित PNG इमेज में बदलना जो किसी भी मानक इमेज व्यूअर द्वारा प्रदर्शित किया जा सकता है। यह प्रक्रिया वेक्टर एंटिटीज़ को रास्टराइज़ करती है, लाइन वेट, रंग, और लेयर्स को संरक्षित रखते हुए उन्हें एक निश्चित‑रेज़ोल्यूशन बिटमैप में बदल देती है। परिणाम PDFs, Word दस्तावेज़ों, या वेब पेजों में एम्बेड करने के लिए आदर्श है जहाँ वेक्टर समर्थन सीमित है।

## CAD को PNG (या अन्य रास्टर फ़ॉर्मेट) के रूप में एक्सपोर्ट क्यों करें?

CAD को PNG के रूप में एक्सपोर्ट करने से आपको सार्वभौमिक संगतता, तेज़ लोडिंग, और सभी प्रमुख प्लेटफ़ॉर्म पर आसान एम्बेडिंग मिलती है। रास्टर इमेजेज़ भारी DWG फ़ाइल खोलने की तुलना में तुरंत लोड होते हैं, और PNG का लॉस‑लेस कम्प्रेशन विज़ुअल फ़िडेलिटी सुनिश्चित करता है। रेज़ोल्यूशन, बैकग्राउंड रंग, और लेआउट को नियंत्रित करके आप यह गारंटी देते हैं कि हर स्टेकहोल्डर को समान दिखावट मिले, चाहे फ़ाइल डेस्कटॉप, मोबाइल डिवाइस, या ब्राउज़र में देखी जाए।

## सामान्य उपयोग केस

| परिदृश्य | रास्टर आउटपुट क्यों मदद करता है |
|----------|------------------------|
| **परियोजना दस्तावेज़ीकरण** | PDFs या Word दस्तावेज़ों में PNGs एम्बेड करने से समीक्षकों को CAD सॉफ़्टवेयर की आवश्यकता नहीं रहती। |
| **वेब पोर्टल्स** | DWG फ़ाइलों से उत्पन्न थंबनेल तुरंत लोड होते हैं और उपयोगकर्ता अनुभव को सुधारते हैं। |
| **मोबाइल ऐप्स** | रास्टर इमेजेज़ उन डिवाइसों पर सही ढंग से प्रदर्शित होते हैं जिनमें CAD व्यूअर नहीं होते। |
| **स्वचालित रिपोर्टिंग** | कई लेआउट्स को बैच‑कन्वर्ट करके PNG/JPEG में चार्ट या डैशबोर्ड में शामिल किया जाता है। |

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास है:

1. **Java विकास पर्यावरण** – JDK 8 या नया स्थापित और कॉन्फ़िगर किया हुआ।  
2. **Aspose.CAD for Java** – नवीनतम JAR को [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/) से डाउनलोड करें।  

## नेमस्पेस इम्पोर्ट करें

`com.aspose.cad.Image` वह कोर क्लास है जो मेमोरी में किसी भी CAD फ़ाइल का प्रतिनिधित्व करता है। `com.aspose.cad.imageoptions.*` प्रत्येक रास्टर फ़ॉर्मेट के लिए विकल्प ऑब्जेक्ट प्रदान करता है। उन क्लासेज़ को इम्पोर्ट करें जिनकी आपको ड्रॉइंग लोड करने, रास्टराइज़ेशन कॉन्फ़िगर करने, और आउटपुट सेव करने के लिए आवश्यकता होगी।

> **Pro tip:** यदि आप TIFF के बजाय **export CAD as PNG** करने की योजना बना रहे हैं, तो `TiffOptions` को `PngOptions` (जो `com.aspose.cad.imageoptions.PngOptions` में पाया जाता है) से बदलें।

## चरण‑दर‑चरण गाइड

### चरण 1: रिसोर्स डायरेक्टरी सेट अप करें

`"Your Document Directory"` को उस पूर्ण पथ से बदलें जहाँ आपके CAD फ़ाइलें स्थित हैं। यह डायरेक्टरी इनपुट और आउटपुट दोनों फ़ाइलों के लिए उपयोग की जाएगी।

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### चरण 2: CAD फ़ाइल लोड करें

`Image.load` स्रोत फ़ाइल को पार्स करता है और एक इन‑मेमोरी प्रतिनिधित्व बनाता है जिसे आप रास्टराइज़ कर सकते हैं। आप कोई भी समर्थित फ़ॉर्मेट (DWG, DXF, DGN, आदि) लोड कर सकते हैं – यह **how to convert cad** भाग है।

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### चरण 3: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

`CadRasterizationOptions` निर्धारित करता है कि वेक्टर डेटा को पिक्सेल में कैसे बदला जाता है। `setPageWidth` और `setPageHeight` आउटपुट रेज़ोल्यूशन को नियंत्रित करते हैं (बड़े मान = उच्च DPI)। `setLayouts` आपको विशिष्ट लेआउट्स के लिए **convert CAD to raster** करने देता है; इसे छोड़ दें ताकि पूरी ड्रॉइंग रास्टराइज़ हो सके।

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### चरण 4: इमेज विकल्प सेट करें

`TiffOptions` (या PNG के लिए `PngOptions`) Aspose को बताता है कि कौन सा रास्टर फ़ॉर्मेट जेनरेट करना है और आपको कम्प्रेशन, कलर डेप्थ, और अन्य फ़ॉर्मेट‑विशिष्ट सेटिंग्स को फाइन‑ट्यून करने देता है। वह विकल्प क्लास चुनें जो आपके वांछित आउटपुट से मेल खाता हो।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### चरण 5: परिणामी इमेज सहेजें

`Image` इंस्टेंस पर `save` कॉल करें, आउटपुट फ़ाइल नाम और विकल्प ऑब्जेक्ट पास करते हुए। फ़ाइल एक्सटेंशन को `.png` में बदलें (और `PngOptions` का उपयोग करें) ताकि **save CAD as PNG** हो सके। वही पैटर्न JPEG, BMP, या PDF के लिए भी काम करता है।

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Common pitfall:** फ़ाइल एक्सटेंशन को विकल्प क्लास से मिलाना न भूलें, नहीं तो `UnsupportedFormatException` होगा। हमेशा उन्हें सिंक्रनाइज़ रखें।

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|----------|----------|
| **खाली आउटपुट इमेज** | `setLayouts` में लेआउट नाम स्रोत CAD फ़ाइल में मौजूद नामों से बिल्कुल मेल खाते हों, यह सत्यापित करें। |
| **कम‑रेज़ोल्यूशन PNG** | `setPageWidth` / `setPageHeight` बढ़ाएँ या रास्टराइज़ेशन विकल्पों पर `setResolution` सेट करें। |
| **असमर्थित DWG संस्करण** | सुनिश्चित करें कि आप नवीनतम Aspose.CAD संस्करण का उपयोग कर रहे हैं; पुराने रिलीज़ नए DWG रिलीज़ को सपोर्ट नहीं कर सकते। |
| **बड़ी फ़ाइलों पर मेमोरी त्रुटियाँ** | पेज़ को एक बार में एक प्रोसेस करें या JVM हीप बढ़ाएँ (`-Xmx2g`). |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या Aspose.CAD विभिन्न CAD फ़ाइल फ़ॉर्मेट्स के साथ संगत है?**  
A: हाँ, यह 30 से अधिक CAD और रास्टर फ़ॉर्मेट्स को सपोर्ट करता है, जिसमें DWG, DXF, DGN, और SVG शामिल हैं।

**Q: क्या मैं आउटपुट रास्टर इमेज के रेज़ोल्यूशन को कस्टमाइज़ कर सकता हूँ?**  
A: बिल्कुल। इच्छित DPI प्राप्त करने के लिए `CadRasterizationOptions` में `setPageWidth`, `setPageHeight`, या `setResolution` को समायोजित करें।

**Q: मैं एक ही रन में कई CAD लेआउट्स को कैसे बदल सकता हूँ?**  
A: `setLayouts` को सभी लेआउट नामों की एरे दें, उदाहरण के लिए, `new String[]{"Model","Layout1","Layout2"}`।

**Q: क्या TIFF के अलावा अन्य आउटपुट फ़ॉर्मेट्स सपोर्टेड हैं?**  
A: हाँ—PNG, JPEG, BMP, PDF, और अधिक उनके संबंधित `*Options` क्लासेज़ के माध्यम से उपलब्ध हैं।

**Q: मैं Aspose.CAD के साथ मदद कहाँ प्राप्त कर सकता हूँ या अपना अनुभव कहाँ साझा कर सकता हूँ?**  
A: समुदाय समर्थन और आधिकारिक सहायता के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

## निष्कर्ष

इन चरणों का पालन करके आप **convert DWG to PNG**, **export CAD as PNG**, **save CAD as JPEG**, या अपनी आवश्यकता के अनुसार कोई भी अन्य रास्टर फ़ॉर्मेट जेनरेट कर सकते हैं। Aspose.CAD for Java भारी काम संभालता है, जिससे आप अपने एप्लिकेशन, दस्तावेज़ीकरण, या वेब पोर्टल्स में उच्च‑गुणवत्ता वाली इमेजेज़ को इंटीग्रेट करने पर ध्यान केंद्रित कर सकते हैं। लाइब्रेरी का 30+ फ़ॉर्मेट्स का समर्थन और पूरी फ़ाइल को मेमोरी में लोड किए बिना कई‑सौ‑पेज़ ड्रॉइंग्स को रेंडर करने की क्षमता इसे एंटरप्राइज़‑ग्रेड CAD रास्टराइज़ेशन के लिए एक मजबूत विकल्प बनाती है।

---

**अंतिम अपडेट:** 2026-10-04  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.12  
**लेखक:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## संबंधित ट्यूटोरियल

- [जावा CAD लाइब्रेरी Aspose.CAD for Java का उपयोग करके DWG को PDF या रास्टर में तेज़ी से एक्सपोर्ट करें](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java के साथ DWG को BMP में बदलें](/cad/java/cad-export-options/export-to-bmp/)
- [Aspose.CAD for Java का उपयोग करके विशिष्ट लेआउट के साथ DWG को PDF में एक्सपोर्ट करें](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}