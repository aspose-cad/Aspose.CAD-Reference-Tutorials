---
date: 2026-02-15
description: Aspose.CAD for Java का उपयोग करके PDF पेज आकार सेट करना और CAD को PDF
  में बदलना सीखें, जिसमें स्वचालित लेआउट स्केलिंग और TIFF निर्यात शामिल है।
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: PDF पेज आकार सेट करें – CAD को PDF में परिवर्तित करें (Java)
url: /hi/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Set Canvas Size and Mode

## Introduction

यदि आपको CAD ड्रॉइंग को PDF में बदलते समय **PDF पेज आकार सेट** करना है, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में हम दिखाएंगे कि Aspose.CAD for Java का उपयोग करके सटीक कैनवास आयाम कैसे निर्धारित करें, ऑटोमैटिक लेआउट स्केलिंग सक्षम करें, और फिर परिणाम को PDF और TIFF दोनों में एक्सपोर्ट करें। चाहे आप प्रिंट के लिए इंजीनियरिंग स्कीमैटिक तैयार कर रहे हों या वेब गैलरी के लिए थंबनेल बना रहे हों, पेज आकार और आउटपुट रिज़ॉल्यूशन को नियंत्रित करना आवश्यक है।

## Quick Answers
- **What does “convert CAD to PDF” mean?** CAD ड्रॉइंग (जैसे DXF, DWG) को PDF दस्तावेज़ में बदलना, जिसे किसी भी प्लेटफ़ॉर्म पर देखा जा सकता है।  
- **Can I also export to TIFF?** हाँ—`TiffOptions` का उपयोग करके हाई‑रेज़ॉल्यूशन रास्टर इमेज बनाएं।  
- **Which option controls canvas size in Java?** `CadRasterizationOptions.setPageWidth/Height`।  
- **What is automatic layout scaling?** एक फ़्लैग (`setAutomaticLayoutsScaling(true)`) जो कैनवास आकार बदलने पर मूल लेआउट अनुपात को बनाए रखता है।  
- **Do I need a license for Aspose.CAD?** प्रोडक्शन उपयोग के लिए एक टेम्पररी या परमानेंट लाइसेंस आवश्यक है।

## How to Set PDF Page Size When Converting CAD to PDF (Java)

PDF पेज आकार (या कैनवास आकार) सेट करने से आप दस्तावेज़ के अंतिम आयाम निर्धारित कर सकते हैं, जो विशेष रूप से तब उपयोगी होता है जब आपको **PDF आयाम बदलने** की आवश्यकता प्रिंटिंग मानकों या UI आवश्यकताओं के अनुसार होती है। नीचे हम प्रत्येक चरण को विस्तार से समझाते हैं, प्रत्येक कोड लाइन के पीछे का *क्यों* बताते हैं।

## What is **convert CAD to PDF**?

CAD को PDF में बदलना मतलब वेक्टर‑आधारित इंजीनियरिंग ड्रॉइंग को PDF पेज के रूप में रेंडर करना, जिससे लाइन वर्क, लेयर्स और ज्योमेट्री बरकरार रहती है और फ़ाइल सार्वभौमिक रूप से एक्सेसिबल बनती है।

## Why set canvas size **java**?

Java में कैनवास आकार सेट करने से आप आउटपुट रिज़ॉल्यूशन और पेज आयाम निर्धारित कर सकते हैं, यह सुनिश्चित करते हुए कि परिणामी PDF या TIFF आपके प्रिंट या डिस्प्ले आवश्यकताओं को पूरा करे। यह स्केलिंग व्यवहार पर नियंत्रण भी देता है, जो बड़े‑फ़ॉर्मेट ड्रॉइंग्स के लिए आवश्यक है।

## Prerequisites

ट्यूटोरियल शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित प्री‑रिक्विज़िट्स हैं:

- Aspose.CAD for Java: सुनिश्चित करें कि आपके Java वातावरण में Aspose.CAD लाइब्रेरी इंस्टॉल है। आप इसे [here](https://releases.aspose.com/cad/java/) से डाउनलोड कर सकते हैं।
- Document Directory: CAD फ़ाइलों को स्टोर करने के लिए एक डॉक्यूमेंट डायरेक्टरी सेट अप करें। इस डायरेक्टरी का संदर्भ ट्यूटोरियल चरणों में दिया जाएगा।

अब चलिए स्टेप‑बाय‑स्टेप गाइड शुरू करते हैं।

## Import Namespaces

इस चरण में, हम आवश्यक नेमस्पेसेज़ इम्पोर्ट करेंगे ताकि आपका Aspose.CAD प्रोजेक्ट शुरू हो सके।

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Step 1: Import Aspose.CAD Classes

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

इस स्निपेट में, हम रिसोर्स डायरेक्टरी का पाथ सेट करते हैं और Aspose.CAD की `Image` क्लास का उपयोग करके एक DXF फ़ाइल लोड करते हैं।

## Step 2: Set **CadRasterizationOptions** Properties (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

यहाँ हम `CadRasterizationOptions` का एक इंस्टेंस बनाते हैं और पेज चौड़ाई, पेज ऊँचाई, तथा **automatic layout scaling** जैसी प्रॉपर्टीज़ कॉन्फ़िगर करते हैं। यह आपके कन्वर्ज़न के लिए **configure canvas mode** का मुख्य भाग है।

## Step 3: Create PdfOptions and Set VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

अब हम एक `PdfOptions` इंस्टेंस बनाते हैं और उसकी `VectorRasterizationOptions` प्रॉपर्टी को पहले कॉन्फ़िगर किए गए `CadRasterizationOptions` पर सेट करते हैं।

## Step 4: Export to PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

अंत में, हम निर्दिष्ट विकल्पों के साथ CAD इमेज को PDF फ़ाइल में सेव करते हैं, जिससे **convert CAD to PDF** प्रक्रिया पूरी होती है।

## Step 5: Create TiffOptions and Set VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

इस चरण में, हम एक `TiffOptions` इंस्टेंस सेट अप करते हैं और उसकी `VectorRasterizationOptions` प्रॉपर्टी को कॉन्फ़िगर करते हैं।

## Step 6: Export to TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

अंत में, हम निर्दिष्ट विकल्पों के साथ CAD इमेज को TIFF फ़ाइल में सेव करते हैं, जिससे **export CAD to TIFF** प्रक्रिया पूरी होती है।

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| Output PDF is blank | `setNoScaling(true)` कुछ ड्रॉइंग्स के लिए रेंडरिंग को डिसेबल कर देता है | `setNoScaling(true)` को हटाएँ या `false` सेट करें। |
| TIFF resolution looks low | Page width/height बहुत छोटा है | `setPageWidth` / `setPageHeight` मान बढ़ाएँ। |
| Layout looks distorted | Automatic layout scaling डिसेबल है | सुनिश्चित करें कि `setAutomaticLayoutsScaling(true)` सक्षम है। |

## Why Adjust Canvas Size and DPI?

कैनवास आकार बदलने से आउटपुट की रास्टराइज़ेशन रिज़ॉल्यूशन सीधे प्रभावित होती है। यदि आपको **TIFF रिज़ॉल्यूशन बढ़ाना** है, तो बस `setPageWidth` / `setPageHeight` मान बढ़ाएँ या `TiffOptions` बनाने से पहले `rasterizationOptions.setResolution(300)` कॉल करें। इससे प्रिंट या विस्तृत निरीक्षण के लिए हाई‑क्वालिटी रास्टर इमेज मिलती है।

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other Java frameworks?

A1: हाँ, Aspose.CAD विभिन्न Java फ्रेमवर्क्स के साथ सहजता से इंटीग्रेट करने के लिए डिज़ाइन किया गया है।

### Q2: Is a temporary license available for Aspose.CAD?

A2: हाँ, आप एक टेम्पररी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

### Q3: Where can I get community support for Aspose.CAD?

A3: समुदाय समर्थन और चर्चा के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) देखें।

### Q4: Can I try Aspose.CAD for free?

A4: बिल्कुल! फ्री ट्रायल [here](https://releases.aspose.com/) प्राप्त करें।

### Q5: How do I purchase Aspose.CAD for Java?

A5: प्रोडक्ट को [here](https://purchase.aspose.com/buy) से खरीदें।

**Additional Q&A**

**Q: Does the canvas size affect vector quality in the PDF?**  
A: नहीं। कैनवास आकार पेज आयाम नियंत्रित करता है; वेक्टर डेटा रिज़ॉल्यूशन‑इंडिपेंडेंट रहता है, जिससे किसी भी ज़ूम लेवल पर स्पष्ट रेंडरिंग मिलती है।

**Q: Can I set a different DPI for the TIFF output?**  
A: हाँ। `TiffOptions` बनाने से पहले `rasterizationOptions.setResolution(dpiValue)` को एडजस्ट करें।

**Q: How can I **change PDF dimensions** for an existing PDF without re‑rendering the CAD?**  
A: Aspose.PDF का उपयोग करके जनरेटेड PDF लोड करें और `pdf.getPages().setPageSize(PageSize.A4)` या कस्टम साइज कॉल करें।

**Q: What is the best way to **convert dxf to pdf** while preserving layers?**  
A: `setAutomaticLayoutsScaling(true)` रखें और `setNoScaling(true)` से बचें; इससे लेयर विज़िबिलिटी और लेआउट फ़िडेलिटी बनी रहती है।

## Conclusion

बधाई हो! आपने सफलतापूर्वक **convert CAD to PDF** और **export CAD to TIFF** किया, साथ ही **set canvas size java**, **automatic layout scaling** को सक्षम किया, और **configure canvas mode** को हाई‑क्वालिटी आउटपुट के लिए समझा। यह ट्यूटोरियल आपके CAD कन्वर्ज़न प्रोजेक्ट्स के लिए एक ठोस आधार प्रदान करता है। अधिक फीचर्स और संभावनाओं के लिए [Aspose.CAD documentation](https://reference.aspose.com/cad/java/) देखें।

---

**Last Updated:** 2026-02-15  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}