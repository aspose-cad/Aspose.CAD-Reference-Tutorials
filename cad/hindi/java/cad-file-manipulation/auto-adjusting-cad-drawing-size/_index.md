---
title: जावा के लिए Aspose.CAD का उपयोग करके CAD ड्राइंग आकार को स्वतः समायोजित करना
linktitle: सीएडी ड्राइंग आकार का स्वतः समायोजन
second_title: Aspose.CAD जावा एपीआई
description: Aspose.CAD का उपयोग करके जावा में CAD ड्राइंग आकारों को स्वतः समायोजित करने की निर्बाध प्रक्रिया का अन्वेषण करें। कुशल सीएडी फ़ाइल हेरफेर के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 13
url: /hi/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के लिए Aspose.CAD का उपयोग करके CAD ड्राइंग आकार को स्वतः समायोजित करना

## परिचय

CAD (कंप्यूटर-एडेड डिज़ाइन) की दुनिया में, ड्राइंग आकार समायोजित करना एक सामान्य आवश्यकता है, और जावा के लिए Aspose.CAD के साथ, यह एक सहज प्रक्रिया बन जाती है। यह शक्तिशाली लाइब्रेरी जावा अनुप्रयोगों में सीएडी फ़ाइलों को संभालने के लिए व्यापक उपकरण प्रदान करती है। इस ट्यूटोरियल में, हम Aspose.CAD का उपयोग करके CAD ड्राइंग आकारों को स्वचालित रूप से समायोजित करने की चरण-दर-चरण प्रक्रिया का पता लगाएंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1.  जावा विकास पर्यावरण: सुनिश्चित करें कि आपकी मशीन पर जावा स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://www.java.com/en/download/).

2.  Aspose.CAD लाइब्रेरी: जावा के लिए Aspose.CAD लाइब्रेरी को डाउनलोड और इंस्टॉल करें[यहाँ](https://releases.aspose.com/cad/java/).

3. नमूना सीएडी फ़ाइल: आपके दस्तावेज़ निर्देशिका में एक नमूना सीएडी फ़ाइल (जैसे, नमूना.dwg) उपलब्ध है।

## नामस्थान आयात करें

अपने जावा एप्लिकेशन में, Aspose.CAD कार्यक्षमता का उपयोग करने के लिए आवश्यक नामस्थान शामिल करें। यहाँ एक उदाहरण है:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

अब, आइए CAD ड्राइंग आकारों को स्वचालित रूप से समायोजित करने की प्रक्रिया को प्रबंधनीय चरणों में विभाजित करें।

## चरण 1: सीएडी ड्राइंग लोड करें

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

इस चरण में निर्दिष्ट फ़ाइल पथ से सीएडी ड्राइंग लोड करना शामिल है।

## चरण 2: BmpOptions बनाएं

```java
BmpOptions bmpOptions = new BmpOptions();
```

 त्वरित करें`BmpOptions` क्लास, जिसका उपयोग बीएमपी प्रारूप के लिए विभिन्न विकल्प सेट करने के लिए किया जाएगा।

## चरण 3: कैडरास्टराइज़ेशन विकल्प बनाएं

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 का एक उदाहरण बनाएं`CadRasterizationOptions` CAD फ़ाइल के लिए रैस्टराइज़ेशन सेटिंग्स को अनुकूलित करने के लिए।

## चरण 4: लेआउट प्रॉपर्टी सेट करें

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

वे लेआउट निर्दिष्ट करें जिन्हें आप आउटपुट में शामिल करना चाहते हैं। इस मामले में, हम "मॉडल" लेआउट का उपयोग करते हैं।

## चरण 5: बीएमपी प्रारूप में निर्यात करें

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

अंत में, समायोजित सीएडी ड्राइंग को बीएमपी प्रारूप में निर्दिष्ट आउटपुट पथ पर सहेजें।

अपने जावा एप्लिकेशन में इन चरणों को दोहराएं, और आप जावा के लिए Aspose.CAD का उपयोग करके CAD ड्राइंग आकार को सफलतापूर्वक स्वचालित रूप से समायोजित कर लेंगे।

## निष्कर्ष

इस ट्यूटोरियल में, हमने जावा के लिए Aspose.CAD का उपयोग करके CAD ड्राइंग आकारों को स्वचालित रूप से समायोजित करने की प्रक्रिया का अध्ययन किया है। यह लाइब्रेरी CAD फ़ाइल हेरफेर को सरल बनाती है, डेवलपर्स के लिए एक मजबूत समाधान प्रदान करती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD विभिन्न CAD फ़ाइल स्वरूपों के साथ संगत है?

A1: हां, Aspose.CAD DWG, DXF, DGN और अन्य सहित विभिन्न CAD प्रारूपों का समर्थन करता है।

### Q2: क्या मैं व्यावसायिक परियोजनाओं के लिए Aspose.CAD का उपयोग कर सकता हूँ?

 ए2: बिल्कुल! मिलने जाना[यहाँ](https://purchase.aspose.com/buy) लाइसेंसिंग विकल्पों का पता लगाने के लिए।

### Q3: मैं परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A3: एक अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/) परीक्षण और मूल्यांकन के लिए.

### Q4: मुझे Aspose.CAD के लिए समर्थन कहां मिल सकता है?

 A4: Aspose.CAD समुदाय से जुड़ें[मंच](https://forum.aspose.com/c/cad/19) सहायता और चर्चा के लिए.

### Q5: क्या Java के लिए Aspose.CAD का कोई निःशुल्क परीक्षण उपलब्ध है?

 A5: हाँ, आप निःशुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/) पुस्तकालय की क्षमताओं का पता लगाने के लिए।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
