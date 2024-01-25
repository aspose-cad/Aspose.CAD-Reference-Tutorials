---
title: जावा के लिए Aspose.CAD के साथ पीडीएफ में निर्यात करें
linktitle: पीडीएफ में निर्यात करें
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD के साथ आसानी से CAD फ़ाइलों को PDF में निर्यात करना सीखें। निर्बाध एकीकरण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 13
url: /hi/java/cad-export-options/export-to-pdf/
---
## परिचय

जावा के लिए Aspose.CAD का उपयोग करके CAD फ़ाइलों को PDF में निर्यात करने पर इस व्यापक ट्यूटोरियल में आपका स्वागत है। यदि आप अपने सीएडी चित्रों को व्यापक रूप से समर्थित पीडीएफ प्रारूप में आसानी से परिवर्तित करना चाहते हैं, तो आप सही जगह पर हैं। इस चरण-दर-चरण मार्गदर्शिका में, हम प्रक्रिया को विघटित करेंगे, यह सुनिश्चित करते हुए कि आप सफल पीडीएफ निर्यात प्राप्त करने के लिए प्रत्येक चरण को समझें।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  जावा के लिए Aspose.CAD: सुनिश्चित करें कि आपके जावा वातावरण में Aspose.CAD लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/java/).

- संसाधन निर्देशिका: एक निर्देशिका स्थापित करें जहाँ आपकी CAD फ़ाइलें संग्रहीत हैं। दिए गए कोड स्निपेट में "आपकी दस्तावेज़ निर्देशिका" को वास्तविक पथ से बदलें।

अब, चलिए मुख्य चरणों पर चलते हैं।

## नामस्थान आयात करें

अपने जावा प्रोजेक्ट में, Aspose.CAD कार्यात्मकताओं के उपयोग को सक्षम करने के लिए आवश्यक नामस्थान आयात करके प्रारंभ करें।

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//आयात com.aspose.cad.imageoptions.TypeOfEntities;
```

## चरण 1: CAD फ़ाइल लोड करें

अपनी CAD फ़ाइल को Aspose.CAD Image ऑब्जेक्ट में लोड करें। "site.dwf" को अपने वास्तविक CAD फ़ाइल नाम से बदलें।

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## चरण 2: पीडीएफ विकल्प कॉन्फ़िगर करें

पीडीएफ निर्यात विकल्प सेट करें, जिसमें पृष्ठ की ऊंचाई, चौड़ाई और लेआउट जैसे वेक्टर रेखापुंज विकल्प शामिल हैं।

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## चरण 3: पीडीएफ में निर्यात करें

जेनरेट की गई पीडीएफ फाइल के लिए आउटपुट पथ निर्दिष्ट करें और कॉन्फ़िगर किए गए पीडीएफ विकल्पों के साथ छवि को सहेजें।

```java
String outPath = dataDir + "site.pdf";
image.save(outPath, pdfOptions);
```

बधाई हो! आपने Java के लिए Aspose.CAD का उपयोग करके अपनी CAD फ़ाइल को सफलतापूर्वक PDF में निर्यात कर लिया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने Java के लिए Aspose.CAD का उपयोग करके CAD फ़ाइलों को PDF में निर्यात करने की चरण-दर-चरण प्रक्रिया का पता लगाया। इन सरल लेकिन प्रभावी चरणों का पालन करके, आप इस कार्यक्षमता को अपने जावा अनुप्रयोगों में सहजता से एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD सभी CAD फ़ाइल स्वरूपों के साथ संगत है?

A1: हाँ, Aspose.CAD विभिन्न डिज़ाइन सॉफ़्टवेयर के साथ अनुकूलता सुनिश्चित करते हुए, CAD प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### Q2: क्या मैं पीडीएफ आउटपुट सेटिंग्स को कस्टमाइज कर सकता हूं?

ए2: बिल्कुल। ट्यूटोरियल अनुकूलन विकल्पों की एक झलक प्रदान करता है, लेकिन आप अपनी आवश्यकताओं के अनुसार आउटपुट को तैयार करने के लिए और अधिक खोज कर सकते हैं।

### Q3: मुझे Aspose.CAD के लिए अतिरिक्त सहायता कहां मिल सकती है?

 उ3: किसी भी प्रश्न या समस्या के लिए, पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) समुदाय से सहायता लेने के लिए.

### Q4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ4: हां, आप Aspose.CAD के निःशुल्क परीक्षण तक पहुंच सकते हैं[यहाँ](https://releases.aspose.com/).

### Q5: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A5: अस्थायी लाइसेंस के लिए, यहां जाएं[इस लिंक](https://purchase.aspose.com/temporary-license/).