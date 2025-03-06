---
title: जावा के लिए Aspose.CAD के साथ IFC को PNG में निर्यात करें
linktitle: आईएफसी को पीएनजी में निर्यात करें
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD के साथ IFC को आसानी से PNG में बदलें। हमारे चरण-दर-चरण ट्यूटोरियल का अनुसरण करें।
weight: 18
url: /hi/java/cad-export-options/export-ifc-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के लिए Aspose.CAD के साथ IFC को PNG में निर्यात करें

## परिचय

जावा के लिए Aspose.CAD का उपयोग करके IFC (इंडस्ट्री फाउंडेशन क्लासेस) को PNG में निर्यात करने पर इस चरण-दर-चरण ट्यूटोरियल में आपका स्वागत है। Aspose.CAD एक शक्तिशाली जावा लाइब्रेरी है जो IFC प्रारूप सहित CAD फ़ाइलों के साथ काम करने के लिए व्यापक क्षमताएं प्रदान करती है। इस ट्यूटोरियल में, हम प्रत्येक चरण पर विस्तृत स्पष्टीकरण के साथ एक आईएफसी फ़ाइल को पीएनजी छवि में परिवर्तित करने की प्रक्रिया में आपका मार्गदर्शन करेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  Aspose.CAD लाइब्रेरी: जावा के लिए Aspose.CAD लाइब्रेरी को डाउनलोड और इंस्टॉल करें[लिंक को डाउनलोड करें](https://releases.aspose.com/cad/java/).

- दस्तावेज़ निर्देशिका: अपने सिस्टम पर एक निर्देशिका तैयार करें जहाँ आपकी IFC फ़ाइल स्थित है।

## नामस्थान आयात करें

अपने जावा प्रोजेक्ट में, आवश्यक नामस्थान आयात करें जैसा कि नीचे दिखाया गया है:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## चरण 1: IFC फ़ाइल लोड करें

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

इस चरण में Aspose.CAD का उपयोग करके IFC फ़ाइल लोड करना शामिल है।

## चरण 2: वेक्टर विकल्प सेट करें

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

पृष्ठ की चौड़ाई और ऊंचाई निर्दिष्ट करते हुए, रेखापुंज के लिए वेक्टर विकल्प कॉन्फ़िगर करें।

## चरण 3: पीएनजी विकल्प सेट करें

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

वेक्टर रैस्टराइज़ेशन विकल्पों सहित पीएनजी विकल्प सेट करें।

## चरण 4: पीएनजी के रूप में सहेजें

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

संसाधित छवि को पीएनजी प्रारूप में सहेजें।

## निष्कर्ष

बधाई हो! आपने Java के लिए Aspose.CAD का उपयोग करके IFC फ़ाइल को सफलतापूर्वक PNG में परिवर्तित कर लिया है। इस ट्यूटोरियल ने एक व्यापक मार्गदर्शिका प्रदान की है, जिससे यह सुनिश्चित होता है कि आप इस कार्यक्षमता को अपनी परियोजनाओं में निर्बाध रूप से एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD IFC फ़ाइलों के सभी संस्करणों के साथ संगत है?

 A1: Aspose.CAD IFC फ़ाइलों के विभिन्न संस्करणों का समर्थन करता है। को देखें[प्रलेखन](https://reference.aspose.com/cad/java/) अनुकूलता विवरण के लिए.

### Q2: क्या मैं रैस्टराइज़ेशन विकल्पों को और अधिक अनुकूलित कर सकता हूँ?

 ए2: बिल्कुल! पता लगाएं[प्रलेखन](https://reference.aspose.com/cad/java/) उन्नत अनुकूलन विकल्पों के लिए।

### Q3: क्या कोई परीक्षण संस्करण उपलब्ध है?

उ3: हां, आप नि:शुल्क परीक्षण संस्करण तक पहुंच सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A4: से एक अस्थायी लाइसेंस प्राप्त करें[इस लिंक](https://purchase.aspose.com/temporary-license/).

### Q5: मैं कहां सहायता मांग सकता हूं या मुद्दों पर चर्चा कर सकता हूं?

A5: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन के लिए.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
