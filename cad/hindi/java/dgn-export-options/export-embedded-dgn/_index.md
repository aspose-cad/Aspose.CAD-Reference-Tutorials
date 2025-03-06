---
title: जावा के लिए Aspose.CAD के साथ एंबेडेड DGN को पीडीएफ में निर्यात करें
linktitle: एंबेडेड डीजीएन निर्यात करें
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD का उपयोग करके एम्बेडेड DGN फ़ाइलों को पीडीएफ में निर्यात करने पर चरण-दर-चरण मार्गदर्शिका देखें। निर्बाध सीएडी फ़ाइल हेरफेर के साथ अपने जावा एप्लिकेशन को बेहतर बनाएं।
weight: 11
url: /hi/java/dgn-export-options/export-embedded-dgn/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के लिए Aspose.CAD के साथ एंबेडेड DGN को पीडीएफ में निर्यात करें

## परिचय

जावा के लिए Aspose.CAD का उपयोग करके एम्बेडेड DGN फ़ाइलों को निर्यात करने पर इस व्यापक ट्यूटोरियल में आपका स्वागत है। Aspose.CAD एक शक्तिशाली लाइब्रेरी है जो जावा डेवलपर्स को CAD फ़ाइलों के साथ निर्बाध रूप से काम करने में सक्षम बनाती है। इस ट्यूटोरियल में, हम चरण-दर-चरण निर्देशों का उपयोग करके एम्बेडेड डीजीएन फ़ाइलों को पीडीएफ में निर्यात करने की प्रक्रिया में आपका मार्गदर्शन करेंगे। चाहे आप एक अनुभवी डेवलपर हों या अभी शुरुआत कर रहे हों, यह ट्यूटोरियल आपके जावा अनुप्रयोगों को बढ़ाने के लिए Aspose.CAD की क्षमताओं का उपयोग करने में आपकी सहायता करेगा।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
- जावा विकास वातावरण: सुनिश्चित करें कि आपकी मशीन पर जावा विकास वातावरण स्थापित है।
-  जावा के लिए Aspose.CAD: जावा लाइब्रेरी के लिए Aspose.CAD को डाउनलोड और इंस्टॉल करें[यहाँ](https://releases.aspose.com/cad/java/).

## पैकेज आयात करें

आरंभ करने के लिए, आपको अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करने होंगे। अपने कोड में निम्नलिखित आयात विवरण जोड़ें:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

अब, आइए उदाहरण कोड को कई चरणों में विभाजित करें:

## चरण 1: इनपुट और आउटपुट पथ सेट करें

उस निर्देशिका पथ को परिभाषित करें जहां आपका दस्तावेज़ स्थित है और इनपुट DWG फ़ाइल नाम निर्दिष्ट करें।

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## चरण 2: DWG फ़ाइल लोड करें

 DWG फ़ाइल को एक में लोड करें`Image` Aspose.CAD का उपयोग करके ऑब्जेक्ट।

```java
Image objImage = Image.load(fileName);
```

## चरण 3: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

निर्यात में शामिल किए जाने वाले लेआउट जैसे रेखापुंज विकल्प कॉन्फ़िगर करें।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## चरण 4: पीडीएफ विकल्प कॉन्फ़िगर करें

वेक्टर रैस्टराइज़ेशन विकल्पों सहित पीडीएफ विकल्प सेट करें।

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## चरण 5: पीडीएफ फाइल सहेजें

कॉन्फ़िगर किए गए विकल्पों के साथ पीडीएफ फाइल को सेव करें।
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## निष्कर्ष

बधाई हो! आपने Java के लिए Aspose.CAD का उपयोग करके एम्बेडेड DGN फ़ाइल को PDF में सफलतापूर्वक निर्यात कर लिया है। इस ट्यूटोरियल में कुशल CAD फ़ाइल हेरफेर के लिए Aspose.CAD को आपके जावा एप्लिकेशन में एकीकृत करने के लिए आवश्यक चरणों को शामिल किया गया है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं किसी व्यावसायिक परियोजना में जावा के लिए Aspose.CAD का उपयोग कर सकता हूँ?

 A1: हाँ, Java के लिए Aspose.CAD एक व्यावसायिक लाइब्रेरी है। आप यहां से लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### Q2: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 A2: हाँ, आप Java के लिए Aspose.CAD का निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं जावा के लिए Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

उ3: आप Aspose.CAD समुदाय से समर्थन प्राप्त कर सकते हैं[मंच](https://forum.aspose.com/c/cad/19).

### Q4: यदि मुझे अस्थायी लाइसेंस की आवश्यकता हो तो क्या होगा?

 A4: आप एक अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: मुझे दस्तावेज़ कहां मिल सकते हैं?

 A5: दस्तावेज़ उपलब्ध है[यहाँ](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
