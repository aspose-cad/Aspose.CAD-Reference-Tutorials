---
title: डीजीएन से पीडीएफ रूपांतरण गाइड - जावा के लिए Aspose.CAD
linktitle: डीजीएन वी7 के लिए समर्थन
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD का उपयोग करके आसानी से DGN फ़ाइलों को पीडीएफ में परिवर्तित करें। निर्बाध एकीकरण और कुशल वर्कफ़्लो के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 11
url: /hi/java/other-cad-operations/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# डीजीएन से पीडीएफ रूपांतरण गाइड - जावा के लिए Aspose.CAD

## परिचय

सीएडी (कंप्यूटर-एडेड डिज़ाइन) की गतिशील दुनिया में, डीजीएन (डिज़ाइन) फ़ाइलों का पीडीएफ (पोर्टेबल दस्तावेज़ प्रारूप) में कुशल रूपांतरण एक महत्वपूर्ण आवश्यकता है। जावा के लिए Aspose.CAD एक शक्तिशाली समाधान के रूप में उभरता है, जो निर्बाध एकीकरण और मजबूत क्षमताओं की पेशकश करता है। इस चरण-दर-चरण मार्गदर्शिका का उद्देश्य आपको जावा के लिए Aspose.CAD का उपयोग करके DGN फ़ाइलों को पीडीएफ में निर्यात करने की प्रक्रिया से परिचित कराना है, जिससे एक सुचारू और कुशल वर्कफ़्लो सुनिश्चित हो सके।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
-  जावा लाइब्रेरी के लिए Aspose.CAD: लाइब्रेरी को डाउनलोड और इंस्टॉल करें[जावा डाउनलोड पेज के लिए Aspose.CAD](https://releases.aspose.com/cad/java/).
- जावा विकास वातावरण: सुनिश्चित करें कि आपकी मशीन पर जावा विकास वातावरण स्थापित है।

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करके प्रारंभ करें:

## चरण 1: आवश्यक पैकेज आयात करें

अपने जावा प्रोजेक्ट में, जावा के लिए Aspose.CAD के लिए आवश्यक पैकेज आयात करें।
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## चरण 2: फ़ाइल पथ सेट करें

अपनी इनपुट डीजीएन फ़ाइल और आउटपुट पीडीएफ फ़ाइल के लिए पथ परिभाषित करें।

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## चरण 3: डीजीएन छवि लोड करें

Aspose.CAD लाइब्रेरी का उपयोग करके DGN छवि लोड करें।

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## चरण 4: पीडीएफ निर्यात विकल्प कॉन्फ़िगर करें

पीडीएफ में निर्यात करने के लिए विकल्प सेट करें, जिसमें पृष्ठ आयाम, स्वचालित लेआउट स्केलिंग, पृष्ठभूमि रंग और निर्यात करने के लिए विशिष्ट लेआउट शामिल हैं।

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //केवल 4 (1,2,3 और 9) दृश्य निर्यात करें
options.setVectorRasterizationOptions(vectorOptions);
```

## चरण 5: पीडीएफ फाइल सहेजें

निर्दिष्ट विकल्पों के साथ डीजीएन छवि को पीडीएफ फाइल के रूप में सहेजें।

```java
objImage.save(outFile, options);
```

विभिन्न DGN फ़ाइलों के लिए इन चरणों को दोहराएँ, फ़ाइल पथों और विकल्पों को आवश्यकतानुसार समायोजित करें।

## निष्कर्ष

जावा के लिए Aspose.CAD के साथ, DGN फ़ाइलों को पीडीएफ में परिवर्तित करना एक सीधी प्रक्रिया बन जाती है। यह मार्गदर्शिका आपको कुशल सीएडी फ़ाइल रूपांतरण की सुविधा प्रदान करते हुए लाइब्रेरी को आपके जावा प्रोजेक्ट्स में सहजता से एकीकृत करने के ज्ञान से सुसज्जित करती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य CAD फ़ाइल स्वरूपों के साथ Java के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: हां, Aspose.CAD विभिन्न CAD प्रारूपों का समर्थन करता है, जो DGN से पीडीएफ रूपांतरण से परे बहुमुखी कार्यक्षमता प्रदान करता है।

### Q2: क्या जावा के लिए Aspose.CAD के लिए एक अस्थायी लाइसेंस उपलब्ध है?

 उ2: हां, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/) परीक्षण प्रयोजनों के लिए.

### Q3: मैं जावा के लिए Aspose.CAD के बारे में समर्थन कैसे प्राप्त कर सकता हूं या प्रश्न कैसे पूछ सकता हूं?

 A3: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19)समुदाय से जुड़ने और सहायता प्राप्त करने के लिए।

### Q4: डीजीएन को पीडीएफ में परिवर्तित करते समय मैं कौन से लेआउट निर्यात कर सकता हूं?

 A4: आप कस्टमाइज़ करके निर्यात करने के लिए लेआउट निर्दिष्ट कर सकते हैं`setLayouts` कोड में सरणी.

### Q5: मैं जावा के लिए Aspose.CAD के लिए व्यापक दस्तावेज़ कहां पा सकता हूं?

 A5: का संदर्भ लें[जावा दस्तावेज़ीकरण के लिए Aspose.CAD](https://reference.aspose.com/cad/java/) विस्तृत जानकारी के लिए.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
