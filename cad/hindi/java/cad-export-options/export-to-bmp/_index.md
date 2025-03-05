---
title: जावा के लिए Aspose.CAD के साथ BMP में निर्यात करें
linktitle: बीएमपी को निर्यात करें
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD के साथ निर्बाध CAD से BMP रूपांतरण का अन्वेषण करें। कुशल और सटीक निर्यात के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 12
url: /hi/java/cad-export-options/export-to-bmp/
---
## परिचय

डिजिटल डिज़ाइन के लगातार विकसित हो रहे परिदृश्य में, कंप्यूटर-एडेड डिज़ाइन (सीएडी) फ़ाइलों को विभिन्न प्रारूपों में निर्बाध रूप से निर्यात करने की क्षमता महत्वपूर्ण है। जावा के लिए Aspose.CAD एक शक्तिशाली समाधान के रूप में सामने आता है, जो डेवलपर्स को CAD फ़ाइलों को BMP प्रारूप में कुशलतापूर्वक निर्यात करने के लिए आवश्यक उपकरण प्रदान करता है। यह ट्यूटोरियल आपको चरण दर चरण प्रक्रिया के माध्यम से मार्गदर्शन करेगा, हर बार एक सहज और सफल निर्यात सुनिश्चित करेगा।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- जावा लाइब्रेरी के लिए Aspose.CAD: जावा लाइब्रेरी के लिए Aspose.CAD को डाउनलोड और इंस्टॉल करें[यहाँ](https://releases.aspose.com/cad/java/).

- जावा विकास वातावरण: सुनिश्चित करें कि आपके सिस्टम पर जावा विकास वातावरण स्थापित है।

- बुनियादी जावा ज्ञान: बुनियादी जावा प्रोग्रामिंग अवधारणाओं से खुद को परिचित करें।

## नामस्थान आयात करें

अपने जावा प्रोजेक्ट में, Aspose.CAD कार्यात्मकताओं तक पहुँचने के लिए आवश्यक नामस्थान आयात करें:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.BmpOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//आयात com.aspose.cad.imageoptions.TypeOfEntities;
```

## चरण 1: संसाधन निर्देशिका पथ सेट करें

अपनी संसाधन निर्देशिका के पथ को परिभाषित करके प्रारंभ करें जहां CAD फ़ाइल स्थित है।

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

## चरण 2: सीएडी फ़ाइल लोड करें

 CAD फ़ाइल को Aspose.CAD में लोड करें`Image` वस्तु।

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## चरण 3: बीएमपी निर्यात विकल्प कॉन्फ़िगर करें

रैस्टराइज़ेशन सेटिंग्स सहित बीएमपी निर्यात विकल्प बनाएं और कॉन्फ़िगर करें।

```java
BmpOptions bmpOptions = new BmpOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## चरण 4: रैस्टराइज़ेशन पैरामीटर सेट करें

रेखापुंजीकरण के लिए पृष्ठ की ऊंचाई, पृष्ठ की चौड़ाई और लेआउट जैसे मापदंडों को परिभाषित करें।

```java
rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## चरण 5: बीएमपी को निर्यात करें

आउटपुट पथ निर्दिष्ट करें और बीएमपी फ़ाइल सहेजें।

```java
String outPath = dataDir + "site.bmp";
image.save(outPath, bmpOptions);
```

प्रत्येक CAD फ़ाइल के लिए इन चरणों को दोहराएँ जिसे आप Java के लिए Aspose.CAD का उपयोग करके BMP में निर्यात करना चाहते हैं।

## निष्कर्ष

Java के लिए Aspose.CAD के साथ CAD फ़ाइलों को BMP प्रारूप में निर्यात करना आसान बना दिया गया है। इस चरण-दर-चरण मार्गदर्शिका का पालन करके, आप कुशल और सटीक रूपांतरण सुनिश्चित करते हुए, इस कार्यक्षमता को अपने जावा अनुप्रयोगों में सहजता से एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या जावा के लिए Aspose.CAD बैच प्रोसेसिंग के लिए उपयुक्त है?

A1: बिल्कुल! जावा के लिए Aspose.CAD बैच प्रोसेसिंग का समर्थन करता है, जिससे आप एक साथ कई CAD फ़ाइलों को कुशलतापूर्वक संभाल सकते हैं।

### Q2: क्या मैं विभिन्न लेआउट के लिए रैस्टराइज़ेशन विकल्पों को अनुकूलित कर सकता हूँ?

उ2: हाँ, आप अपनी विशिष्ट आवश्यकताओं के अनुसार पृष्ठ आयाम और लेआउट जैसे रेखापुंज विकल्पों को अनुकूलित कर सकते हैं।

### Q3: मुझे जावा के लिए Aspose.CAD के लिए अतिरिक्त समर्थन कहां मिल सकता है?

 A3: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और चर्चा के लिए।

### Q4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ4: हां, आप जावा के लिए Aspose.CAD का निःशुल्क परीक्षण देख सकते हैं[यहाँ](https://releases.aspose.com/).

### Q5: मैं अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A5: Java के लिए Aspose.CAD के लिए एक अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/).