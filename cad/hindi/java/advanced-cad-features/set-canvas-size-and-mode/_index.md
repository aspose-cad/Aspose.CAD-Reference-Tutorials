---
title: कैनवास का आकार और मोड सेट करें
linktitle: कैनवास का आकार और मोड सेट करें
second_title: Aspose.CAD जावा एपीआई
description: कैनवास आकार और मोड सेट करने पर हमारी चरण-दर-चरण मार्गदर्शिका के साथ जावा के लिए Aspose.CAD की शक्ति का अन्वेषण करें। CAD फ़ाइलों को आसानी से पीडीएफ और टीआईएफएफ प्रारूपों में परिवर्तित करें।
weight: 16
url: /hi/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# कैनवास का आकार और मोड सेट करें

## परिचय

क्या आप अपनी CAD रूपांतरण प्रक्रिया को बढ़ाने के लिए Java के लिए Aspose.CAD की शक्ति का उपयोग करना चाह रहे हैं? यह व्यापक मार्गदर्शिका आपको जावा के लिए Aspose.CAD का उपयोग करके कैनवास आकार और मोड सेट करने के चरणों के बारे में बताएगी। चाहे आप एक अनुभवी डेवलपर हों या अभी शुरुआत कर रहे हों, यह ट्यूटोरियल आपको आवश्यक अंतर्दृष्टि प्रदान करेगा।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  जावा के लिए Aspose.CAD: सुनिश्चित करें कि आपके जावा वातावरण में Aspose.CAD लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/java/).

- दस्तावेज़ निर्देशिका: अपनी CAD फ़ाइलों को संग्रहीत करने के लिए एक दस्तावेज़ निर्देशिका सेट करें। इस निर्देशिका को ट्यूटोरियल चरणों में संदर्भित किया जाएगा।

अब, आइए चरण-दर-चरण मार्गदर्शिका के साथ शुरुआत करें।

## नामस्थान आयात करें

इस चरण में, हम आपके Aspose.CAD प्रोजेक्ट को किकस्टार्ट करने के लिए आवश्यक नामस्थान आयात करेंगे।
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## चरण 1: Aspose.CAD कक्षाएं आयात करें

```java
// संसाधन निर्देशिका का पथ.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 इस स्निपेट में, हम संसाधन निर्देशिका के लिए पथ सेट करते हैं और Aspose.CAD का उपयोग करके एक DXF फ़ाइल लोड करते हैं`Image` कक्षा।

## चरण 2: कैडरास्टराइज़ेशनऑप्शंस गुण सेट करें

```java
// CadRasterizationOptions का एक उदाहरण बनाएं और इसके विभिन्न गुण सेट करें
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 यहां, हम इसका एक उदाहरण बनाते हैं`CadRasterizationOptions` और पृष्ठ की चौड़ाई, पृष्ठ की ऊंचाई और स्केलिंग विकल्प जैसे गुणों को कॉन्फ़िगर करें।

## चरण 3: PdfOptions बनाएं और वेक्टरRasterizationOptions सेट करें

```java
// PdfOptions का एक उदाहरण बनाएं
PdfOptions pdfOptions = new PdfOptions();

// वेक्टररैस्टराइज़ेशनऑप्शंस प्रॉपर्टी सेट करें
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 अब, हम एक बनाते हैं`PdfOptions` उदाहरण और इसे सेट करें`VectorRasterizationOptions` पहले से कॉन्फ़िगर की गई संपत्ति`CadRasterizationOptions`.

## चरण 4: पीडीएफ में निर्यात करें

```java
// सीएडी को पीडीएफ में निर्यात करें
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

अंत में, हम निर्दिष्ट विकल्पों का उपयोग करके सीएडी छवि को एक पीडीएफ फ़ाइल में सहेजते हैं।

## चरण 5: TiffOptions बनाएं और वेक्टरRasterizationOptions सेट करें

```java
// TiffOptions का एक उदाहरण बनाएं
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// वेक्टररैस्टराइज़ेशनऑप्शंस प्रॉपर्टी सेट करें
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

इस चरण में, हमने एक स्थापित किया`TiffOptions` उदाहरण और इसे कॉन्फ़िगर करें`VectorRasterizationOptions` संपत्ति।

## चरण 6: TIFF में निर्यात करें

```java
// CAD को TIFF में निर्यात करें
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

अंत में, हम निर्दिष्ट विकल्पों का उपयोग करके CAD छवि को TIFF फ़ाइल में सहेजते हैं।

## निष्कर्ष

 बधाई हो! आपने Java के लिए Aspose.CAD का उपयोग करके सफलतापूर्वक कैनवास आकार और मोड सेट कर लिया है। यह ट्यूटोरियल आपके CAD रूपांतरण परियोजनाओं के लिए एक ठोस आधार प्रदान करता है। इसमें अधिक सुविधाएँ और संभावनाएँ खोजें[Aspose.CAD दस्तावेज़ीकरण](https://reference.aspose.com/cad/java/).

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं जावा के लिए अन्य जावा फ्रेमवर्क के साथ Aspose.CAD का उपयोग कर सकता हूँ?

A1: हां, Aspose.CAD को विभिन्न जावा फ्रेमवर्क के साथ सहजता से एकीकृत करने के लिए डिज़ाइन किया गया है।

### Q2: क्या Aspose.CAD के लिए अस्थायी लाइसेंस उपलब्ध है?

 उ2: हां, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q3: Aspose.CAD के लिए मुझे सामुदायिक समर्थन कहाँ से मिल सकता है?

 A3: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और चर्चा के लिए।

### Q4: क्या मैं Aspose.CAD को मुफ़्त में आज़मा सकता हूँ?

 उ4: बिल्कुल! निःशुल्क परीक्षण प्राप्त करें[यहाँ](https://releases.aspose.com/).

### Q5: मैं जावा के लिए Aspose.CAD कैसे खरीदूं?

 A5: उत्पाद खरीदें[यहाँ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
