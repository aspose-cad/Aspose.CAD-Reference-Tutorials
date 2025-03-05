---
title: जावा के लिए Aspose.CAD का उपयोग करके DWG में लेआउट की सूची बनाएं
linktitle: DWG में सूची लेआउट
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD का अन्वेषण करें और DWG फ़ाइलों में आसानी से लेआउट सूचीबद्ध करें। अपने जावा अनुप्रयोगों में शक्तिशाली CAD कार्यक्षमता को एकीकृत करें।
type: docs
weight: 12
url: /hi/java/cad-file-manipulation/list-layouts-in-dwg/
---
## परिचय

DWG फ़ाइलों में लेआउट सूचीबद्ध करने के लिए जावा के लिए Aspose.CAD का उपयोग करने पर हमारी चरण-दर-चरण मार्गदर्शिका में आपका स्वागत है। Aspose.CAD एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को CAD फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने में सक्षम बनाती है। इस ट्यूटोरियल में, हम एक विशिष्ट कार्य पर ध्यान केंद्रित करेंगे: DWG फ़ाइल में लेआउट सूचीबद्ध करना। इस गाइड के अंत तक, आप इस कार्यक्षमता को अपने जावा अनुप्रयोगों में निर्बाध रूप से एकीकृत करने में सक्षम होंगे।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  जावा लाइब्रेरी के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास Java के लिए Aspose.CAD लाइब्रेरी स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[वेबसाइट](https://releases.aspose.com/cad/java/).

- जावा विकास वातावरण: अपनी मशीन पर जावा विकास वातावरण स्थापित करें।

## नामस्थान आयात करें

अपने जावा एप्लिकेशन में, आपको Aspose.CAD का उपयोग करने के लिए आवश्यक नामस्थान आयात करने की आवश्यकता है। अपनी जावा फ़ाइल की शुरुआत में निम्नलिखित पंक्तियाँ जोड़ें:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## चरण 1: अपनी दस्तावेज़ निर्देशिका सेट करें

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

"आपकी दस्तावेज़ निर्देशिका" को उस निर्देशिका के पथ से बदलना सुनिश्चित करें जहाँ आपकी CAD फ़ाइलें संग्रहीत हैं।

## चरण 2: DWG फ़ाइल लोड करें

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

निर्दिष्ट फ़ाइल पथ का उपयोग करके DWG फ़ाइल लोड करें।

## चरण 3: लेआउट प्राप्त करें और नाम प्रिंट करें

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

DWG फ़ाइल से लेआउट पुनर्प्राप्त करें और उनके नाम कंसोल पर प्रिंट करें।

## निष्कर्ष

 बधाई हो! आपने Java के लिए Aspose.CAD का उपयोग करके DWG फ़ाइल में लेआउट को सफलतापूर्वक सूचीबद्ध कर लिया है। इस ट्यूटोरियल में आपके परिवेश को सेट करने से लेकर लेआउट नामों को प्रिंट करने तक, आवश्यक चरणों को शामिल किया गया है। जावा के लिए Aspose.CAD की अधिक सुविधाओं का पता लगाने के लिए स्वतंत्र महसूस करें[प्रलेखन](https://reference.aspose.com/cad/java/).

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य CAD फ़ाइल स्वरूपों के साथ Java के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: हां, Aspose.CAD DWG, DXF, DWF और अन्य सहित विभिन्न CAD प्रारूपों का समर्थन करता है।

### Q2: क्या जावा के लिए Aspose.CAD के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

 उ2: हाँ, आप नि:शुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: जावा के लिए Aspose.CAD के लिए मुझे सामुदायिक समर्थन कहां मिल सकता है?

 A3: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन के लिए.

### Q4: मैं जावा के लिए Aspose.CAD का लाइसेंस कैसे खरीदूं?

 A4: आप यहां से लाइसेंस खरीद सकते हैं[खरीद पृष्ठ](https://purchase.aspose.com/buy).

### Q5: क्या मैं परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस का उपयोग कर सकता हूं?

 A5: हाँ, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).