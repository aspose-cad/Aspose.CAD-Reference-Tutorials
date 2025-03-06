---
title: जावा के लिए Aspose.CAD के साथ सहज DGN से ऑटोकैड पीडीएफ निर्यात
linktitle: ऑटोकैड प्रारूप में डीजीएन को पीडीएफ में निर्यात करना
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD का उपयोग करके DGN फ़ाइलों को पीडीएफ में ऑटोकैड प्रारूप में निर्यात करने पर चरण-दर-चरण मार्गदर्शिका देखें। अपने जावा एप्लिकेशन की CAD हैंडलिंग क्षमताओं को सहजता से बढ़ाएं।
weight: 12
url: /hi/java/dgn-export-options/exporting-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के लिए Aspose.CAD के साथ सहज DGN से ऑटोकैड पीडीएफ निर्यात

## परिचय

ऑटोकैड प्रारूप में डीजीएन फ़ाइलों को पीडीएफ में निर्यात करने के लिए जावा के लिए Aspose.CAD का उपयोग करने पर इस व्यापक ट्यूटोरियल में आपका स्वागत है। यदि आप CAD फ़ाइलों को संभालने के लिए अपने जावा एप्लिकेशन की क्षमता को बढ़ाना चाहते हैं, तो Aspose.CAD एक उत्कृष्ट विकल्प है। इस ट्यूटोरियल में, हम आपको चरण दर चरण डीजीएन फ़ाइलों को निर्यात करने की प्रक्रिया के बारे में मार्गदर्शन देंगे।


## आवश्यक शर्तें
इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
-  Aspose.CAD लाइब्रेरी: सुनिश्चित करें कि आपके पास Java के लिए Aspose.CAD लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/java/).
- दस्तावेज़ निर्देशिका: एक दस्तावेज़ निर्देशिका स्थापित करें जहाँ आपकी इनपुट और आउटपुट फ़ाइलें संग्रहीत की जाएंगी।

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, Aspose.CAD कार्यात्मकताओं तक पहुँचने के लिए आवश्यक पैकेज आयात करें:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

अब, आइए उदाहरण कोड को कई चरणों में विभाजित करें:

## चरण 1: फ़ाइल पथ परिभाषित करें

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

"आपकी दस्तावेज़ निर्देशिका" को उस वास्तविक पथ से बदलना सुनिश्चित करें जहाँ आपकी फ़ाइलें स्थित हैं।

## चरण 2: डीजीएन छवि लोड करें

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Aspose.CAD का उपयोग करके DGN फ़ाइल लोड करें।

## चरण 3: पीडीएफ निर्यात विकल्प सेट करें

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // विशिष्ट दृश्य निर्यात करें
options.setVectorRasterizationOptions(vectorOptions);
```

पृष्ठ आयाम और लेआउट प्राथमिकताओं सहित पीडीएफ निर्यात विकल्पों को परिभाषित करें।

## चरण 4: पीडीएफ फाइल सहेजें

```java
objImage.save(outFile, options);
```

निर्यात की गई पीडीएफ फाइल को सहेजें।

किसी भी अतिरिक्त डीजीएन फ़ाइल के लिए इन चरणों को दोहराएँ जिसे आप कनवर्ट करना चाहते हैं। बधाई हो! आपने जावा के लिए Aspose.CAD का उपयोग करके DGN फ़ाइलों को पीडीएफ में ऑटोकैड प्रारूप में सफलतापूर्वक निर्यात किया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने पता लगाया कि आपके एप्लिकेशन की CAD फ़ाइल हैंडलिंग क्षमताओं को बढ़ाने के लिए Java के लिए Aspose.CAD का लाभ कैसे उठाया जाए। पालन करने में आसान चरणों और कोड उदाहरणों के साथ, अब आप DGN फ़ाइलों को पीडीएफ में ऑटोकैड प्रारूप में निर्बाध रूप से निर्यात कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD सभी CAD फ़ाइल स्वरूपों के साथ संगत है?

A1: हाँ, Aspose.CAD विभिन्न फ़ाइल प्रकारों को संभालने में बहुमुखी प्रतिभा सुनिश्चित करते हुए, CAD प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### Q2: क्या मैं पीडीएफ निर्यात सेटिंग्स को अनुकूलित कर सकता हूं?

ए2: बिल्कुल। जैसा कि ट्यूटोरियल में दिखाया गया है, आप अपनी आवश्यकताओं के अनुरूप पेज आयाम और लेआउट जैसे विकल्पों को समायोजित कर सकते हैं।

### Q3: मुझे अतिरिक्त सहायता या सहायता कहां मिल सकती है?

 A3: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और चर्चा के लिए।

### Q4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ4: हाँ, आप नि:शुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q5: मैं अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A5: एक अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
