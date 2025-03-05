---
title: Aspose.CAD ट्यूटोरियल के साथ जावा DGN से JPEG रूपांतरण
linktitle: डीजीएन को ऑटोकैड फॉर्मेट में रैस्टर इमेज फॉर्मेट में निर्यात करना
second_title: Aspose.CAD जावा एपीआई
description: Aspose.CAD का उपयोग करके जावा में DGN फ़ाइलों को JPEG छवियों में निर्यात करना सीखें। यह चरण-दर-चरण ट्यूटोरियल आपको प्रक्रिया में सहजता से मार्गदर्शन करता है।
type: docs
weight: 13
url: /hi/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## परिचय

जावा के लिए Aspose.CAD का उपयोग करके डीजीएन (डिज़ाइन) फ़ाइलों को रैस्टर इमेज फॉर्मेट में निर्यात करने पर इस व्यापक ट्यूटोरियल में आपका स्वागत है। Aspose.CAD एक शक्तिशाली लाइब्रेरी है जो जावा डेवलपर्स को CAD फ़ाइलों के साथ निर्बाध रूप से काम करने में सक्षम बनाती है। इस ट्यूटोरियल में, हम आपको चरण-दर-चरण निर्देश और कोड उदाहरण प्रदान करते हुए डीजीएन फ़ाइलों को जेपीईजी छवियों में परिवर्तित करने की प्रक्रिया में मार्गदर्शन करेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
1.  Aspose.CAD लाइब्रेरी: सुनिश्चित करें कि आपके पास जावा लाइब्रेरी के लिए Aspose.CAD स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/java/).
2. जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपकी मशीन पर जावा स्थापित है।
3. एकीकृत विकास पर्यावरण (आईडीई): IntelliJ या Eclipse जैसी जावा-संगत आईडीई का उपयोग करें।

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, Aspose.CAD के लिए आवश्यक पैकेज आयात करें। अपने कोड में निम्नलिखित पंक्तियाँ जोड़ें:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## चरण 1: डीजीएन फ़ाइल लोड करें

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## चरण 2: JpegOptions ऑब्जेक्ट बनाएं

```java
ImageOptionsBase options = new JpegOptions();
```

## चरण 3: रैस्टराइज़ेशन विकल्प निर्दिष्ट करें

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## चरण 4: परिवर्तित छवि को सहेजें

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

अपनी विशिष्ट DGN फ़ाइलों के लिए इन चरणों को दोहराएँ, फ़ाइल पथों को तदनुसार समायोजित करें।

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.CAD का उपयोग करके DGN फ़ाइलों को रैस्टर इमेज फॉर्मेट में निर्यात करना सफलतापूर्वक सीख लिया है। इस ट्यूटोरियल ने आपको इस कार्यक्षमता को अपने जावा अनुप्रयोगों में शामिल करने के ज्ञान से सुसज्जित किया है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य CAD फ़ाइल स्वरूपों के साथ Java के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: हां, Aspose.CAD विभिन्न CAD प्रारूपों का समर्थन करता है, जो जावा डेवलपर्स के लिए एक बहुमुखी समाधान प्रदान करता है।

### Q2: क्या जावा के लिए Aspose.CAD के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

 उ2: हाँ, आप निःशुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं जावा के लिए Aspose.CAD के लिए दस्तावेज़ कहां पा सकता हूं?

 A3: दस्तावेज़ देखें[यहाँ](https://reference.aspose.com/cad/java/).

### Q4: मैं जावा के लिए Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 उ4: सहायता मंच पर जाएँ[यहाँ](https://forum.aspose.com/c/cad/19).

### Q5: मैं जावा के लिए Aspose.CAD का लाइसेंस कहां से खरीद सकता हूं?

 A5: आप लाइसेंस खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).