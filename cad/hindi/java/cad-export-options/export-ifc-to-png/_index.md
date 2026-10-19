---
date: 2026-10-19
description: केवल कुछ कोड लाइनों में Aspose.CAD for Java के साथ PNG थंबनेल IFC फ़ाइलें
  बनाना सीखें।
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: IFC को PNG में निर्यात करें
og_description: Aspose.CAD for Java का उपयोग करके PNG थंबनेल IFC फ़ाइलें आसानी से
  बनाएं। यह चरण‑दर‑चरण गाइड दिखाता है कि कैसे लोड करें, rasterize करें, और IFC मॉडल
  को उच्च‑गुणवत्ता वाले PNG इमेज के रूप में सहेजें।
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Aspose.CAD for Java के साथ PNG थंबनेल IFC बनाएं
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Aspose.CAD for Java के साथ PNG थंबनेल IFC कैसे बनाएं
url: /hi/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# IFC को PNG में निर्यात करें Aspose.CAD for Java के साथ

## परिचय

इस ट्यूटोरियल में आप सीखेंगे कि Aspose.CAD for Java के साथ **PNG थंबनेल IFC** फ़ाइलें कैसे बनाएं। चाहे आपको BIM पोर्टल के लिए तेज़ प्रीव्यू चाहिए, दस्तावेज़ प्रबंधन प्रणाली के लिए थंबनेल बनाना हो, या बैच रूपांतरण को स्वचालित करना हो, नीचे दिए गए चरण आपको केवल कुछ ही Java कोड लाइनों में 3‑D IFC मॉडल को एक स्पष्ट 2‑D PNG छवि में रास्टराइज़ करने की अनुमति देते हैं।

## त्वरित उत्तर
- **कौनसी लाइब्रेरी आवश्यक है?** Aspose.CAD for Java.  
- **क्या मैं कुछ लाइनों के कोड में PNG थंबनेल IFC बना सकता हूँ?** हाँ – पूरा कार्यप्रवाह 20 लाइनों से कम में फिट हो जाता है।  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** परीक्षण के लिए एक अस्थायी लाइसेंस काम करता है; व्यावसायिक तैनाती के लिए पूर्ण लाइसेंस आवश्यक है।  
- **क्या आउटपुट स्केलेबल है?** आप कोई भी पिक्सेल आयाम सेट कर सकते हैं, इसलिए PNG को आप जिस आकार में चाहें स्केल कर सकते हैं।  
- **कौनसा Java संस्करण समर्थित है?** Java 8 या उससे ऊपर।

## “IFC को PNG में बदलना” क्या है?
IFC (Industry Foundation Classes) को PNG में बदलना का अर्थ है 3‑D बिल्डिंग मॉडल को 2‑D बिटमैप छवि में रास्टराइज़ करना। यह प्रक्रिया एक दृश्य थंबनेल बनाती है जिसे ब्राउज़र, रिपोर्ट या मोबाइल ऐप में पूर्ण CAD व्यूअर की आवश्यकता के बिना प्रदर्शित किया जा सकता है।

## Aspose.CAD for Java का उपयोग क्यों करें?
Aspose.CAD **30+ CAD और BIM फ़ॉर्मेट** का समर्थन करता है, जिसमें IFC, DWG, DXF, और DGN शामिल हैं, और **2 GB** तक की फ़ाइलों को पूरी दस्तावेज़ को मेमोरी में लोड किए बिना प्रोसेस कर सकता है। यह लाइब्रेरी शुद्ध Java है, **कोई बाहरी निर्भरताएँ नहीं** है, और Windows, Linux, और macOS पर चलती है, जिससे यह सर्वर‑साइड इमेज जेनरेशन के लिए आदर्श बनती है।  
यह उच्च‑प्रदर्शन रास्टराइज़ेशन, व्यापक फ़ॉर्मेट समर्थन, और Java अनुप्रयोगों में आसान एकीकरण प्रदान करती है।

## पूर्वापेक्षाएँ

- **Aspose.CAD लाइब्रेरी** – नवीनतम JAR [डाउनलोड लिंक](https://releases.aspose.com/cad/java/) से डाउनलोड करें।  
- **Java Development Kit** – आपके मशीन पर JDK 8 या नया स्थापित हो।  
- **IFC स्रोत फ़ाइल** – फ़ाइल को उस फ़ोल्डर में रखें जिसे आप अपने कोड से संदर्भित कर सकें।

## नेमस्पेस इम्पोर्ट करें

`com.aspose.cad` पैकेज वह सभी क्लासेस प्रदान करता है जिनकी आपको आवश्यकता है। `CadImage` CAD फ़ाइलों को लोड करने का एंट्री पॉइंट है, जबकि `PngOptions` रास्टराइज़ेशन सेटिंग्स को कॉन्फ़िगर करता है।

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Java में PNG थंबनेल IFC कैसे बनाएं?

IFC फ़ाइल को लोड करें, रास्टराइज़ेशन विकल्प निर्धारित करें, और परिणाम को PNG छवि के रूप में सहेजें – यह संपूर्ण रूपांतरण कार्यप्रवाह है। नीचे के अनुभाग प्रत्येक चरण को विभाजित करते हैं, ताकि आप स्निपेट्स को कॉपी‑पेस्ट करके अपने प्रोजेक्ट में तुरंत चला सकें।

### चरण 1: IFC फ़ाइल लोड करें
सबसे पहले, उस फ़ोल्डर की ओर इशारा करें जहाँ आपकी IFC फ़ाइल स्थित है और इसे `CadImage.load` से लोड करें।  
`CadImage.load` एक CAD फ़ाइल पढ़ता है और एक इमेज ऑब्जेक्ट लौटाता है जिसे रास्टराइज़ किया जा सकता है।

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **यह क्यों महत्वपूर्ण है:** फ़ाइल को `CadImage` के रूप में लोड करने से आपको वेक्टर‑रास्टर रूपांतरण विकल्पों तक पहुँच मिलती है जो रिज़ॉल्यूशन, बैकग्राउंड रंग, और लाइन वजन को नियंत्रित करते हैं।

### चरण 2: रास्टराइज़ेशन विकल्प सेट करें
`VectorRasterizationOptions` के माध्यम से आउटपुट आयाम और अन्य वेक्टर‑संबंधित सेटिंग्स निर्धारित करें।  
`VectorRasterizationOptions` आपको आउटपुट आकार, बैकग्राउंड रंग, और अन्य रास्टराइज़ेशन पैरामीटर निर्दिष्ट करने की अनुमति देता है।

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> अंतिम PNG रिज़ॉल्यूशन को नियंत्रित करने के लिए `PageWidth` और `PageHeight` को समायोजित करें, जो उच्च‑गुणवत्ता वाले प्रिंट या वेब थंबनेल के लिए **PNG java** फ़ाइलें सहेजते समय आवश्यक है।

### चरण 3: PNG विकल्प कॉन्फ़िगर करें
`PngOptions` इंस्टेंस बनाकर रास्टराइज़ेशन विकल्पों को PNG एक्सपोर्टर से लिंक करें।

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### चरण 4: छवि को PNG के रूप में सहेजें
अंत में, `save` मेथड का उपयोग करके रास्टराइज़्ड छवि को डिस्क पर लिखें।  
`save` रास्टराइज़्ड छवि को चुने हुए फ़ॉर्मेट में निर्दिष्ट फ़ाइल पथ पर लिखता है।

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> इस चरण के बाद आप सफलतापूर्वक **PNG थंबनेल IFC** बना चुके हैं और उत्पन्न `example.png` को कहीं भी रास्टर इमेज की आवश्यकता होने पर उपयोग कर सकते हैं।

## सामान्य उपयोग केस
- **BIM मॉडल के लिए वेब पोर्टल में थंबनेल बनाना।**  
- **फ़्लोर‑प्लान स्नैपशॉट को PDF या Word रिपोर्ट में एम्बेड करना।**  
- **आर्काइव या माइग्रेशन प्रोजेक्ट्स के लिए बड़े IFC लाइब्रेरी की स्वचालित बैच रूपांतरण।**

## समस्या निवारण और टिप्स
- **मेमोरी समस्याएँ:** बहुत बड़े IFC फ़ाइलों के लिए JVM हीप (`-Xmx2g` या अधिक) बढ़ाएँ।  
- **टेक्सचर गायब:** सुनिश्चित करें कि IFC फ़ाइल के बाहरी संसाधन `dataDir` से पहुँच योग्य हों।  
- **प्रो टिप:** यदि आप डिफ़ॉल्ट ट्रांसपेरेंट PNG के बजाय सफ़ेद बैकग्राउंड चाहते हैं तो `vectorOptions.setBackgroundColor(Color.getWhite())` का उपयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या Aspose.CAD सभी IFC फ़ाइल संस्करणों के साथ संगत है?
A1: Aspose.CAD विभिन्न IFC संस्करणों का समर्थन करता है। विस्तृत संगतता जानकारी के लिए [डॉक्यूमेंटेशन](https://reference.aspose.com/cad/java/) देखें।

### प्रश्न 2: क्या मैं रास्टराइज़ेशन विकल्पों को आगे अनुकूलित कर सकता हूँ?
A2: बिल्कुल! DPI नियंत्रण, एंटी‑एलियासिंग, और लाइन मोटाई जैसे उन्नत सेटिंग्स के लिए [डॉक्यूमेंटेशन](https://reference.aspose.com/cad/java/) देखें।

### प्रश्न 3: क्या कोई ट्रायल संस्करण उपलब्ध है?
A3: हाँ, आप मुफ्त ट्रायल को [Aspose.CAD फ्री ट्रायल](https://releases.aspose.com/) से डाउनलोड कर सकते हैं।

### प्रश्न 4: परीक्षण के लिए अस्थायी लाइसेंस कैसे प्राप्त करूँ?
A4: आप [Aspose.CAD अस्थायी लाइसेंस पेज](https://purchase.aspose.com/temporary-license/) से एक अस्थायी लाइसेंस प्राप्त कर सकते हैं।

### प्रश्न 5: मैं प्रश्न पूछने या समस्याएँ रिपोर्ट करने के लिए कहाँ जा सकता हूँ?
A5: समर्थन के लिए Aspose इंजीनियरों और अन्य डेवलपर्स से मदद पाने हेतु [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) में शामिल हों।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं इस विधि का उपयोग करके अन्य CAD फ़ॉर्मेट को PNG में बदल सकता हूँ?**  
उत्तर: हाँ, Aspose.CAD कई फ़ॉर्मेट (DWG, DXF, DGN, आदि) का समर्थन करता है। बस फ़ाइल एक्सटेंशन बदलें और उपयुक्त इमेज क्लास लोड करें।

**प्रश्न: क्या लाइब्रेरी मुझे कस्टम DPI सेट करने देती है?**  
उत्तर: DPI को अप्रत्यक्ष रूप से `PageWidth`/`PageHeight` के माध्यम से नियंत्रित किया जाता है। वांछित भौतिक आकार के अनुसार इन मानों को समायोजित करके आवश्यक DPI प्राप्त करें।

**प्रश्न: क्या PNG आउटपुट लॉस‑लेस है?**  
उत्तर: PNG एक लॉसलेस फ़ॉर्मेट है, इसलिए रास्टराइज़्ड छवि मूल वेक्टर डेटा की पूरी दृश्य शुद्धता को बनाए रखती है।

## निष्कर्ष

अब आपके पास Aspose.CAD for Java का उपयोग करके **PNG थंबनेल IFC** फ़ाइलें बनाने की एक पूर्ण, उत्पादन‑तैयार विधि है। इन चरणों को डेस्कटॉप टूल्स, सर्वर‑साइड सेवाओं, या क्लाउड फ़ंक्शन्स में एकीकृत करें ताकि BIM विज़ुअलाइज़ेशन पाइपलाइन को स्वचालित किया जा सके और अंतिम उपयोगकर्ताओं को तेज़, उच्च‑गुणवत्ता वाले थंबनेल प्रदान किए जा सकें।

---

**अंतिम अपडेट:** 2026-10-19  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.11  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Aspose.CAD for Java के साथ STL को PNG में कैसे बदलें](/cad/java/cad-export-options/export-stl-to-png/)
- [DWG को PNG में बदलें – Aspose.CAD for Java का उपयोग करके CAD को PNG के रूप में सहेजें](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [Java में DWG को PDF में निर्यात करें – Aspose.CAD के साथ PDF पेज साइज सेट करें](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}