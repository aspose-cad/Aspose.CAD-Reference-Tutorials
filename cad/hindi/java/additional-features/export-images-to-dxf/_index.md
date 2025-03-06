---
title: जावा के लिए Aspose.CAD का उपयोग करके छवियों को DXF प्रारूप में निर्यात करें
linktitle: जावा का उपयोग करके छवियों को डीएक्सएफ प्रारूप में निर्यात करें
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD का उपयोग करके छवियों को DXF प्रारूप में निर्यात करने की निर्बाध प्रक्रिया का अन्वेषण करें। चरण-दर-चरण मार्गदर्शिका, अक्सर पूछे जाने वाले प्रश्न और बहुत कुछ।
weight: 15
url: /hi/java/additional-features/export-images-to-dxf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के लिए Aspose.CAD का उपयोग करके छवियों को DXF प्रारूप में निर्यात करें

## परिचय

जावा के लिए Aspose.CAD का उपयोग करके छवियों को DXF प्रारूप में निर्यात करने पर एक व्यापक ट्यूटोरियल में आपका स्वागत है। Aspose.CAD एक शक्तिशाली जावा लाइब्रेरी है जो डेवलपर्स को CAD चित्रों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देती है। इस ट्यूटोरियल में, हम आपको छवियों को डीएक्सएफ प्रारूप में निर्यात करने की प्रक्रिया के बारे में बताएंगे, इस कार्य को प्राप्त करने के लिए विभिन्न चरणों और तकनीकों का प्रदर्शन करेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- जावा प्रोग्रामिंग की बुनियादी समझ.
-  जावा लाइब्रेरी के लिए Aspose.CAD स्थापित किया गया। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/java/).
- Aspose.CAD के लिए एक वैध लाइसेंस या अस्थायी लाइसेंस। इसे प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/).
- परीक्षण के लिए डीएक्सएफ प्रारूप में कुछ नमूना छवियां।

## नामस्थान आयात करें

अपने जावा प्रोजेक्ट में, Aspose.CAD के लिए आवश्यक नामस्थान आयात करें:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
import java.io.File;
import static java.lang.System.in;
```

## चरण 1: प्रति दस्तावेज़ नया फ़ॉन्ट सेट करें

```java
// संसाधन निर्देशिका का पथ.
String dataDir = "Your Document Directory" + "DXFDrawings/";

File[] files = new File(dataDir).listFiles();
for (File file : files) {
    String extension = GetFileExtension(file);
    if (extension.equals(".dxf")) {
        CadImage cadImage = (CadImage)Image.load(file.getName());
        for (Object style : cadImage.getStyles()) {
            ((CadStyleTableObject)style).setPrimaryFontName("Broadway");
        }
        cadImage.save(file.getName() + "_font.dxf");
    }
}
```

## चरण 2: सभी "सीधी" रेखाएँ छिपाएँ

```java
CadImage cadImageEntity = (CadImage)Image.load(file.getName());
for (CadBaseEntity entity : cadImageEntity.getEntities()) {
    if (entity.getTypeName() == CadEntityTypeName.LINE) {
        entity.setVisible((short)0);
    }
}
cadImageEntity.save(file.getName() + "_lines.dxf");
```

## चरण 3: पाठ के साथ हेरफेर

```java
CadImage cadImageText = (CadImage)Image.load(file.getName());
for (CadBaseEntity entity : cadImageText.getEntities()) {
    if (entity.getTypeName() == CadEntityTypeName.TEXT) {
        ((CadText)entity).setDefaultValue("New text here!!! :)");
        break;
    }
}
cadImageText.save(file.getName() + "_text.dxf");
```

अपनी निर्देशिका में प्रत्येक DXF फ़ाइल के लिए इन चरणों को दोहराएँ।

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.CAD का उपयोग करके छवियों को DXF प्रारूप में निर्यात करने का तरीका सफलतापूर्वक सीख लिया है। इस ट्यूटोरियल में आवश्यक चरणों को शामिल किया गया है, जिसमें फ़ॉन्ट सेट करना, लाइनें छिपाना और सीएडी छवियों के भीतर टेक्स्ट में हेरफेर करना शामिल है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं बिना लाइसेंस के जावा के लिए Aspose.CAD का उपयोग कर सकता हूँ?

 A1: आप इसे उपलब्ध अस्थायी लाइसेंस के साथ उपयोग कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q2: मुझे Aspose.CAD दस्तावेज़ कहाँ मिल सकते हैं?

 A2: दस्तावेज़ उपलब्ध है[यहाँ](https://reference.aspose.com/cad/java/).

### Q3: मुझे Aspose.CAD के लिए समर्थन कैसे मिलेगा?

 उ3: सहायता मंच पर जाएँ[यहाँ](https://forum.aspose.com/c/cad/19).

### Q4: मैं जावा के लिए Aspose.CAD कहां से डाउनलोड कर सकता हूं?

 A4: लाइब्रेरी डाउनलोड करें[यहाँ](https://releases.aspose.com/cad/java/).

### Q5: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 A5: हाँ, आप निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
