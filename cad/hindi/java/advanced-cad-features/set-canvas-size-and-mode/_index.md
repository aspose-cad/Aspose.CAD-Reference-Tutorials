---
date: 2026-08-29
description: Aspose.CAD for Java का उपयोग करके pdf पेज आकार सेट करने और CAD को PDF
  में बदलने का तरीका जानें, जिसमें automatic layout scaling और TIFF निर्यात शामिल
  है।
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: pdf पेज आकार सेट करें – CAD को pdf में बदलें
og_description: Aspose.CAD का उपयोग करके Java में CAD ड्रॉइंग्स को PDF में बदलते समय
  pdf पेज आकार सेट करने का तरीका जानें। यह गाइड canvas dimensions, automatic layout
  scaling, और high‑resolution TIFF निर्यात को कवर करता है।
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: pdf पेज आकार सेट करें – Aspose के साथ Java में CAD को PDF में बदलें
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: pdf पेज आकार सेट करें – CAD को pdf में बदलें (Java)
url: /hi/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF पृष्ठ आकार सेट करें – CAD को PDF में बदलें (Java)

## परिचय

यदि आपको CAD ड्रॉइंग्स को PDF में बदलते समय **set pdf page size** सेट करने की आवश्यकता है, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में हम आपको दिखाएंगे कि Aspose.CAD for Java का उपयोग करके सटीक कैनवास आयाम कैसे निर्धारित करें, ऑटोमैटिक लेआउट स्केलिंग सक्षम करें, और फिर परिणाम को PDF और TIFF दोनों में निर्यात करें। चाहे आप प्रिंट के लिए इंजीनियरिंग स्कीमैटिक तैयार कर रहे हों या वेब गैलरी के लिए थंबनेल बना रहे हों, पृष्ठ आकार और आउटपुट रिज़ॉल्यूशन को नियंत्रित करना आवश्यक है।

## त्वरित उत्तर
- **convert CAD to PDF क्या है?** एक CAD ड्रॉइंग (जैसे DXF, DWG) को PDF दस्तावेज़ में बदलना, जिसे किसी भी प्लेटफ़ॉर्म पर देखा जा सकता है।  
- **क्या मैं TIFF में भी निर्यात कर सकता हूँ?** हाँ—उच्च‑रिज़ॉल्यूशन रास्टर इमेज बनाने के लिए `TiffOptions` का उपयोग करें।  
- **Java में कैनवास आकार नियंत्रित करने वाला विकल्प कौन सा है?** `CadRasterizationOptions.setPageWidth/Height`.  
- **automatic layout scaling क्या है?** एक फ़्लैग (`setAutomaticLayoutsScaling(true)`) जो कैनवास आकार बदलने पर मूल लेआउट अनुपात को बनाए रखता है।  
- **क्या मुझे Aspose.CAD के लिए लाइसेंस चाहिए?** उत्पादन उपयोग के लिए एक अस्थायी या स्थायी लाइसेंस आवश्यक है।

## CAD को PDF में बदलते समय Java में PDF पृष्ठ आकार कैसे सेट करें

अपना CAD फ़ाइल लोड करें, इच्छित चौड़ाई और ऊँचाई के साथ `CadRasterizationOptions` को कॉन्फ़िगर करें, ऑटोमैटिक लेआउट स्केलिंग सक्षम करें, और फिर परिणाम को PDF के रूप में सहेजें। यह दो‑चरणीय तरीका आपको आउटपुट पृष्ठ के सटीक आयाम को नियंत्रित करने देता है बिना वेक्टर गुणवत्ता का बलिदान किए।

## convert CAD to PDF क्या है?

CAD को PDF में बदलना मतलब वेक्टर‑आधारित इंजीनियरिंग ड्रॉइंग्स को PDF पृष्ठों के रूप में रेंडर करना है, जिसमें रेखा कार्य, लेयर और ज्यामिति को संरक्षित रखा जाता है जबकि फ़ाइल को सार्वभौमिक रूप से सुलभ बनाया जाता है। प्रक्रिया निर्दिष्ट विकल्पों के अनुसार ड्रॉइंग को रास्टराइज़ करती है, जिससे एक PDF बनता है जिसे किसी भी डिवाइस पर CAD सॉफ़्टवेयर की आवश्यकता के बिना खोला जा सकता है, और मूल डिज़ाइन की दृश्य सटीकता को बनाए रखता है।

## Java में कैनवास आकार क्यों सेट करें?

Java में कैनवास आकार सेट करने से आप आउटपुट रिज़ॉल्यूशन और पृष्ठ आयाम निर्धारित कर सकते हैं, जिससे उत्पन्न PDF या TIFF आपके प्रिंट या डिस्प्ले आवश्यकताओं से मेल खाता है। यह आपको स्केलिंग व्यवहार पर नियंत्रण भी देता है, जो बड़े‑फ़ॉर्मेट ड्रॉइंग्स के लिए आवश्यक है।

## आवश्यकताएँ

ट्यूटोरियल में प्रवेश करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यकताएँ मौजूद हैं:

- Aspose.CAD for Java: सुनिश्चित करें कि आपके Java वातावरण में Aspose.CAD लाइब्रेरी स्थापित है। आप Aspose.CAD for Java लाइब्रेरी [here](https://releases.aspose.com/cad/java/) से डाउनलोड कर सकते हैं।
- Document directory: अपने CAD फ़ाइलों को संग्रहीत करने के लिए एक दस्तावेज़ डायरेक्टरी सेट करें। इस डायरेक्टरी का संदर्भ ट्यूटोरियल चरणों में दिया जाएगा।

अब, चलिए चरण‑दर‑चरण गाइड शुरू करते हैं।

## नेमस्पेस आयात करें

इस चरण में, हम आपके Aspose.CAD प्रोजेक्ट को शुरू करने के लिए आवश्यक नेमस्पेस आयात करेंगे।

`Image` वह मुख्य क्लास है जिसका उपयोग CAD फ़ाइलों को लोड करने के लिए किया जाता है।

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## चरण 1: Aspose.CAD क्लासेस आयात करें

`Image` क्लास CAD ड्रॉइंग्स को लोड और सहेजने के लिए मेथड्स प्रदान करता है।

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

इस स्निपेट में, हम रिसोर्स डायरेक्टरी का पाथ सेट करते हैं और Aspose.CAD की `Image` क्लास का उपयोग करके एक DXF फ़ाइल लोड करते हैं।

## चरण 2: CadRasterizationOptions प्रॉपर्टीज़ सेट करें (set canvas size java)

`CadRasterizationOptions` CAD‑से‑रास्टर रूपांतरण के लिए पृष्ठ आकार और स्केलिंग जैसी रास्टराइज़ेशन सेटिंग्स निर्दिष्ट करता है।

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

यहाँ, हम `CadRasterizationOptions` का एक इंस्टेंस बनाते हैं और पृष्ठ चौड़ाई, पृष्ठ ऊँचाई, और **automatic layout scaling** जैसी प्रॉपर्टीज़ कॉन्फ़िगर करते हैं। यह आपके रूपांतरण के लिए **configure canvas mode** का मूल भाग है।

## चरण 3: PdfOptions बनाएं और vectorRasterizationOptions सेट करें

`PdfOptions` रूपांतरण के लिए PDF आउटपुट सेटिंग्स को परिभाषित करता है।

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

अब, हम एक `PdfOptions` इंस्टेंस बनाते हैं और उसकी `VectorRasterizationOptions` प्रॉपर्टी को पहले कॉन्फ़िगर किए गए `CadRasterizationOptions` पर सेट करते हैं।

## चरण 4: PDF में निर्यात करें (convert CAD to PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

अंत में, हम निर्दिष्ट विकल्पों का उपयोग करके CAD इमेज को PDF फ़ाइल में सहेजते हैं, जिससे **convert CAD to PDF** प्रक्रिया पूरी होती है।

## चरण 5: TiffOptions बनाएं और vectorRasterizationOptions सेट करें (export CAD to TIFF)

`TiffOptions` TIFF आउटपुट पैरामीटर जैसे संपीड़न और रिज़ॉल्यूशन को कॉन्फ़िगर करता है।

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## चरण 6: TIFF में निर्यात करें

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

अंत में, हम निर्दिष्ट विकल्पों का उपयोग करके CAD इमेज को TIFF फ़ाइल में सहेजते हैं, जिससे कैनवास आकार कॉन्फ़िगर करने के बाद **export CAD to TIFF** कैसे किया जाए, यह प्रदर्शित होता है।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|-------|-----|
| आउटपुट PDF खाली है | `setNoScaling(true)` कुछ ड्रॉइंग्स के लिए रेंडरिंग को अक्षम करता है | `setNoScaling(true)` को हटाएँ या इसे `false` पर सेट करें। |
| TIFF रिज़ॉल्यूशन कम दिख रहा है | पृष्ठ चौड़ाई/ऊँचाई बहुत छोटी है | `setPageWidth` / `setPageHeight` मान बढ़ाएँ। |
| लेआउट विकृत दिख रहा है | ऑटोमैटिक लेआउट स्केलिंग अक्षम है | सुनिश्चित करें कि `setAutomaticLayoutsScaling(true)` सक्षम है। |

## कैनवास आकार और DPI क्यों समायोजित करें?

कैनवास आकार बदलने से आउटपुट की रास्टराइज़ेशन रिज़ॉल्यूशन सीधे प्रभावित होती है। यदि आपको **TIFF रिज़ॉल्यूशन बढ़ाने** की आवश्यकता है, तो बस `setPageWidth` / `setPageHeight` मान बढ़ाएँ या `TiffOptions` बनाने से पहले `rasterizationOptions.setResolution(300)` कॉल करें। इससे आपको प्रिंट या विस्तृत निरीक्षण के लिए उपयुक्त उच्च‑गुणवत्ता वाली रास्टर इमेज मिलती है।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या मैं Aspose.CAD for Java को अन्य Java फ्रेमवर्क्स के साथ उपयोग कर सकता हूँ?**  
A: हाँ, Aspose.CAD विभिन्न Java फ्रेमवर्क्स के साथ सहजता से एकीकृत होने के लिए डिज़ाइन किया गया है।

**Q2: क्या Aspose.CAD के लिए एक अस्थायी लाइसेंस उपलब्ध है?**  
A: हाँ, आप अस्थायी लाइसेंस पृष्ठ [here](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

**Q3: मैं Aspose.CAD के लिए समुदाय समर्थन कहाँ प्राप्त कर सकता हूँ?**  
A: समुदाय समर्थन और चर्चा के लिए Aspose.CAD फ़ोरम [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

**Q4: क्या मैं Aspose.CAD को मुफ्त में आज़मा सकता हूँ?**  
A: बिल्कुल! मुफ्त ट्रायल डाउनलोड पृष्ठ [here](https://releases.aspose.com/) प्राप्त करें।

**Q5: मैं Aspose.CAD for Java को कैसे खरीदूँ?**  
A: Aspose.CAD for Java खरीदें [here](https://purchase.aspose.com/buy)।

**Q: क्या कैनवास आकार PDF में वेक्टर गुणवत्ता को प्रभावित करता है?**  
A: नहीं। कैनवास आकार पृष्ठ आयाम नियंत्रित करता है; वेक्टर डेटा रिज़ॉल्यूशन‑स्वतंत्र रहता है, जिससे किसी भी ज़ूम स्तर पर स्पष्ट रेंडरिंग सुनिश्चित होती है।

**Q: क्या मैं TIFF आउटपुट के लिए अलग DPI सेट कर सकता हूँ?**  
A: हाँ। `TiffOptions` बनाने से पहले `rasterizationOptions.setResolution(dpiValue)` को समायोजित करें।

**Q: मैं CAD को पुनः‑रेंडर किए बिना मौजूदा PDF के आयाम कैसे बदल सकता हूँ?**  
A: जेनरेटेड PDF को लोड करने के लिए Aspose.PDF का उपयोग करें और `pdf.getPages().setPageSize(PageSize.A4)` या कस्टम आकार को कॉल करें।

**Q: लेयर्स को संरक्षित रखते हुए dxf को pdf में बदलने का सबसे अच्छा तरीका क्या है?**  
A: `setAutomaticLayoutsScaling(true)` रखें और `setNoScaling(true)` से बचें; इससे लेयर दृश्यता और लेआउट की सटीकता बनी रहती है।

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक **convert CAD to PDF** और **export CAD to TIFF** किया है जबकि **set canvas size java** किया, **automatic layout scaling** सक्षम किया, और उच्च‑गुणवत्ता आउटपुट के लिए **configure canvas mode** सीख लिया। यह ट्यूटोरियल आपके CAD रूपांतरण प्रोजेक्ट्स के लिए एक ठोस आधार प्रदान करता है। अधिक सुविधाओं और संभावनाओं का अन्वेषण करें [Aspose.CAD documentation](https://reference.aspose.com/cad/java/) में।

---

**अंतिम अपडेट:** 2026-08-29  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.12  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [कैनवास आकार सेट करें – Aspose.CAD for Java के साथ उन्नत CAD फीचर्स](/cad/java/advanced-cad-features/)
- [Java में DWG को PDF में निर्यात करें – Aspose.CAD के साथ PDF पृष्ठ आकार सेट करें](/cad/java/cad-export-options/export-to-pdf/)
- [कस्टम पृष्ठ आकार सेट करें – ऑटो लेआउट स्केलिंग के साथ CAD से PDF](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}