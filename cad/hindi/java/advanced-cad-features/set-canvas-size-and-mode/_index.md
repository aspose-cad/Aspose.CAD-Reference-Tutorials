---
date: 2025-12-10
description: Aspose.CAD for Java का उपयोग करके CAD को PDF में कैसे बदलें, साथ ही कैनवास
  आकार सेट करना, स्वचालित लेआउट स्केलिंग, और TIFF में निर्यात करना सीखें।
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: CAD को PDF में बदलें – कैनवास आकार और मोड सेट करें (Java)
url: /hi/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# कैनवास आकार और मोड सेट करें

## परिचय

क्या आप **convert CAD to PDF** करते समय कैनवास आकार और रेंडरिंग मोड पर पूर्ण नियंत्रण चाहते हैं? यह व्यापक गाइड आपको जावा में कैनवास आकार सेट करने, ऑटोमैटिक लेआउट स्केलिंग सक्षम करने, और फिर Aspose.CAD का उपयोग करके परिणाम को PDF और TIFF दोनों फ़ॉर्मेट में निर्यात करने के सटीक चरणों के माध्यम से ले जाता है। चाहे आप प्रोडक्शन पाइपलाइन को परिष्कृत कर रहे हों या प्रोटोटाइप के साथ प्रयोग कर रहे हों, यहाँ आपको स्पष्ट, क्रियात्मक निर्देश मिलेंगे।

## त्वरित उत्तर
- **convert CAD to PDF** क्या है?  
  CAD ड्रॉइंग (जैसे DXF, DWG) को PDF दस्तावेज़ में बदलना, जिसे किसी भी प्लेटफ़ॉर्म पर देखा जा सकता है।  
- **क्या मैं TIFF में भी निर्यात कर सकता हूँ?**  
  हाँ—उच्च‑रिज़ॉल्यूशन रास्टर इमेज बनाने के लिए `TiffOptions` का उपयोग करें।  
- **जावा में कैनवास आकार को नियंत्रित करने वाला विकल्प कौन सा है?**  
  `CadRasterizationOptions.setPageWidth/Height`।  
- **ऑटोमैटिक लेआउट स्केलिंग क्या है?**  
  एक फ़्लैग (`setAutomaticLayoutsScaling(true)`) जो कैनवास आकार बदलने पर मूल लेआउट अनुपात को बनाए रखता है।  
- **क्या मुझे Aspose.CAD के लिए लाइसेंस चाहिए?**  
  उत्पादन उपयोग के लिए एक अस्थायी या स्थायी लाइसेंस आवश्यक है।

## क्या है **convert CAD to PDF**?
CAD को PDF में बदलना मतलब वेक्टर‑आधारित इंजीनियरिंग ड्रॉइंग को PDF पृष्ठों के रूप में रेंडर करना है, जिसमें लाइन वर्क, लेयर्स और ज्योमेट्री को संरक्षित रखा जाता है और फ़ाइल को सार्वभौमिक रूप से सुलभ बनाया जाता है।

## जावा में कैनवास आकार **java** क्यों सेट करें?
जावा में कैनवास आकार सेट करने से आप आउटपुट रिज़ॉल्यूशन और पेज डाइमेंशन निर्धारित कर सकते हैं, जिससे परिणामी PDF या TIFF आपके प्रिंटिंग या डिस्प्ले आवश्यकताओं से मेल खाता है। यह स्केलिंग व्यवहार पर नियंत्रण भी देता है, जो बड़े‑फ़ॉर्मेट ड्रॉइंग के लिए आवश्यक है।

## पूर्वापेक्षाएँ

ट्यूटोरियल में डुबने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- Aspose.CAD for Java: सुनिश्चित करें कि आपके जावा वातावरण में Aspose.CAD लाइब्रेरी स्थापित है। आप इसे [here](https://releases.aspose.com/cad/java/) से डाउनलोड कर सकते हैं।  
- Document Directory: अपने CAD फ़ाइलों को संग्रहीत करने के लिए एक दस्तावेज़ डायरेक्टरी सेट करें। इस डायरेक्टरी का संदर्भ ट्यूटोरियल चरणों में दिया जाएगा।

अब, चलिए चरण‑दर‑चरण गाइड शुरू करते हैं।

## Namespaces आयात करें

इस चरण में, हम आपके Aspose.CAD प्रोजेक्ट को शुरू करने के लिए आवश्यक namespaces आयात करेंगे।

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## चरण 1: Aspose.CAD क्लासेस आयात करें

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

इस स्निपेट में, हम रिसोर्स डायरेक्टरी का पाथ सेट करते हैं और Aspose.CAD के `Image` क्लास का उपयोग करके एक DXF फ़ाइल लोड करते हैं।

## चरण 2: **CadRasterizationOptions** प्रॉपर्टीज़ सेट करें (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

यहाँ, हम `CadRasterizationOptions` का एक इंस्टेंस बनाते हैं और पेज चौड़ाई, पेज ऊँचाई, और **automatic layout scaling** जैसी प्रॉपर्टीज़ को कॉन्फ़िगर करते हैं। यह आपके रूपांतरण के लिए **configure canvas mode** का मुख्य भाग है।

## चरण 3: PdfOptions बनाएं और VectorRasterizationOptions सेट करें

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

अब, हम एक `PdfOptions` इंस्टेंस बनाते हैं और उसकी `VectorRasterizationOptions` प्रॉपर्टी को पहले कॉन्फ़िगर किए गए `CadRasterizationOptions` पर सेट करते हैं।

## चरण 4: PDF में निर्यात करें (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

अंत में, हम निर्दिष्ट विकल्पों का उपयोग करके CAD इमेज को PDF फ़ाइल में सहेजते हैं, जिससे **convert CAD to PDF** प्रक्रिया पूरी होती है।

## चरण 5: TiffOptions बनाएं और VectorRasterizationOptions सेट करें (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

इस चरण में, हम एक `TiffOptions` इंस्टेंस सेट करते हैं और उसकी `VectorRasterizationOptions` प्रॉपर्टी को कॉन्फ़िगर करते हैं।

## चरण 6: TIFF में निर्यात करें

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

अंत में, हम निर्दिष्ट विकल्पों का उपयोग करके CAD इमेज को TIFF फ़ाइल में सहेजते हैं, जिससे कैनवास आकार कॉन्फ़िगर करने के बाद **export CAD to TIFF** कैसे किया जाता है, यह प्रदर्शित होता है।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|-------|-----|
| आउटपुट PDF खाली है | `setNoScaling(true)` कुछ ड्रॉइंग्स के लिए रेंडरिंग को अक्षम करता है | `setNoScaling(true)` को हटाएँ या इसे `false` सेट करें। |
| TIFF रिज़ॉल्यूशन कम दिख रहा है | पेज चौड़ाई/ऊँचाई बहुत छोटी है | `setPageWidth` / `setPageHeight` मान बढ़ाएँ। |
| लेआउट विकृत दिख रहा है | ऑटोमैटिक लेआउट स्केलिंग अक्षम है | सुनिश्चित करें कि `setAutomaticLayoutsScaling(true)` सक्षम है। |

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक **convert CAD to PDF** और **export CAD to TIFF** किया है जबकि **set canvas size java** किया, **automatic layout scaling** सक्षम किया, और उच्च‑गुणवत्ता आउटपुट के लिए **configure canvas mode** सीख लिया। यह ट्यूटोरियल आपके CAD रूपांतरण प्रोजेक्ट्स के लिए एक ठोस आधार प्रदान करता है। अधिक सुविधाओं और संभावनाओं का अन्वेषण करें [Aspose.CAD documentation](https://reference.aspose.com/cad/java/) में।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.CAD for Java को अन्य जावा फ्रेमवर्क्स के साथ उपयोग कर सकता हूँ?
A1: हाँ, Aspose.CAD विभिन्न जावा फ्रेमवर्क्स के साथ सहजता से एकीकृत होने के लिए डिज़ाइन किया गया है।

### Q2: क्या Aspose.CAD के लिए एक अस्थायी लाइसेंस उपलब्ध है?
A2: हाँ, आप अस्थायी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

### Q3: मैं Aspose.CAD के लिए सामुदायिक समर्थन कहाँ प्राप्त कर सकता हूँ?
A3: समुदाय समर्थन और चर्चाओं के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) देखें।

### Q4: क्या मैं Aspose.CAD को मुफ्त में आज़मा सकता हूँ?
A4: बिल्कुल! आप मुफ्त ट्रायल [here](https://releases.aspose.com/) से प्राप्त कर सकते हैं।

### Q5: मैं Aspose.CAD for Java कैसे खरीदूँ?
A5: उत्पाद [here](https://purchase.aspose.com/buy) से खरीदें।

**Additional Q&A**

**Q: क्या कैनवास आकार PDF में वेक्टर क्वालिटी को प्रभावित करता है?**  
A: नहीं। कैनवास आकार पेज डाइमेंशन नियंत्रित करता है; वेक्टर डेटा रिज़ॉल्यूशन‑स्वतंत्र रहता है, जिससे किसी भी ज़ूम लेवल पर स्पष्ट रेंडरिंग सुनिश्चित होती है।

**Q: क्या मैं TIFF आउटपुट के लिए अलग DPI सेट कर सकता हूँ?**  
A: हाँ। `TiffOptions` बनाने से पहले `rasterizationOptions.setResolution(dpiValue)` को समायोजित करें।

---

**अंतिम अपडेट:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}