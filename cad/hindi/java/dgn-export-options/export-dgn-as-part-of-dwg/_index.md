---
title: जावा के लिए Aspose.CAD के साथ DGN को DWG में निर्यात करें
linktitle: DWG के भाग के रूप में DGN निर्यात करें
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD का उपयोग करके DWG के हिस्से के रूप में DGN को निर्यात करने का तरीका जानें। कुशल सीएडी फ़ाइल हेरफेर के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 10
url: /hi/java/dgn-export-options/export-dgn-as-part-of-dwg/
---
## परिचय

इस ट्यूटोरियल में, हम जानेंगे कि DWG (ऑटोकैड ड्रॉइंग) फ़ाइल के हिस्से के रूप में DGN (माइक्रोस्टेशन डिज़ाइन) फ़ाइल को निर्यात करने के लिए जावा के लिए Aspose.CAD का उपयोग कैसे करें। Aspose.CAD एक शक्तिशाली लाइब्रेरी है जो CAD फ़ाइल स्वरूपों के साथ काम करने के लिए व्यापक कार्यक्षमता प्रदान करती है। यह चरण-दर-चरण मार्गदर्शिका आपको जावा का उपयोग करके DWG के भाग के रूप में DGN निर्यात करने की प्रक्रिया को समझने में मदद करेगी।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
1. Aspose.CAD लाइब्रेरी: जावा के लिए Aspose.CAD लाइब्रेरी डाउनलोड और इंस्टॉल करें। आप पुस्तकालय पा सकते हैं[यहाँ](https://releases.aspose.com/cad/java/).
2. जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जावा स्थापित है।
3. एकीकृत विकास पर्यावरण (आईडीई): बेहतर विकास अनुभव के लिए एक्लिप्स या इंटेलीजे जैसी जावा आईडीई चुनें।

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, CAD फ़ाइल हेरफेर को सक्षम करने के लिए आवश्यक Aspose.CAD पैकेज आयात करें। यहाँ एक उदाहरण है:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## चरण 1: फ़ाइल पथ सेट करें

 DWG फ़ाइल के लिए इनपुट और आउटपुट फ़ाइल पथ परिभाषित करें। अद्यतन करें`dataDir`, `fileName` , और`outPath` तदनुसार परिवर्तनशील.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## चरण 2: पीडीएफऑप्शंस इंस्टेंस बनाएं

 का एक उदाहरण बनाएं`PdfOptions` क्लास, क्योंकि हम DWG फ़ाइल को पीडीएफ प्रारूप में निर्यात कर रहे हैं।

```java
PdfOptions exportOptions = new PdfOptions();
```

## चरण 3: DWG फ़ाइल लोड करें

 मौजूदा DWG फ़ाइल को एक छवि के रूप में लोड करें और इसे इसमें कनवर्ट करें`CadImage` प्रकार।

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## चरण 4: संस्थाओं के माध्यम से पुनरावृति करें

DWG फ़ाइल के अंदर प्रत्येक इकाई पर जाएँ और जाँचें कि क्या यह एक छवि परिभाषा है। यदि ऐसा है, तो ऑब्जेक्ट का बाहरी संदर्भ पुनः प्राप्त करें।

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## चरण 5: रैस्टराइज़ेशन विकल्पों को परिभाषित करें

 के लिए सेटिंग्स परिभाषित करें`CadRasterizationOptions`ऑब्जेक्ट, जिसमें पेज की चौड़ाई, ऊंचाई, लेआउट और पृष्ठभूमि का रंग शामिल है।

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## चरण 6: वेक्टर रैस्टराइज़ेशन विकल्प सेट करें

निर्यात के लिए वेक्टर रेखापुंज विकल्प सेट करें।

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## चरण 7: DWG को पीडीएफ में निर्यात करें

 अंत में, कॉल करके DWG को PDF में निर्यात करें`save` तरीका।

```java
cadImage.save(outPath, exportOptions);
```

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.CAD का उपयोग करके DWG फ़ाइल के भाग के रूप में DGN फ़ाइल को निर्यात करना सफलतापूर्वक सीख लिया है। यह शक्तिशाली लाइब्रेरी CAD फ़ाइलों के साथ काम करने के लिए व्यापक क्षमताएं प्रदान करती है, जिससे आपके CAD फ़ाइल हेरफेर कार्य कुशल और सरल हो जाते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: मैं जावा के लिए Aspose.CAD के लिए दस्तावेज़ कहां पा सकता हूं?

 A1: दस्तावेज़ पाया जा सकता है[यहाँ](https://reference.aspose.com/cad/java/).

### Q2: मैं जावा के लिए Aspose.CAD लाइब्रेरी कैसे डाउनलोड कर सकता हूं?

 A2: आप लाइब्रेरी को यहां से डाउनलोड कर सकते हैं[इस लिंक](https://releases.aspose.com/cad/java/).

### Q3: क्या Java के लिए Aspose.CAD का निःशुल्क परीक्षण उपलब्ध है?

 उ3: हाँ, आप निःशुल्क परीक्षण पा सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं जावा के लिए Aspose.CAD के लिए अस्थायी लाइसेंस कहां से प्राप्त कर सकता हूं?

 ए4: एक अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: सहायता चाहिए या कोई प्रश्न हैं?

 A5: Aspose.CAD समुदाय सहायता फ़ोरम पर जाएँ[यहाँ](https://forum.aspose.com/c/cad/19).