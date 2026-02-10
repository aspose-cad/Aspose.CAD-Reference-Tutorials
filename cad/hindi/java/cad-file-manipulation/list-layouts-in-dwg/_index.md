---
date: 2025-12-28
description: Aspose.CAD for Java का उपयोग करके DWG फ़ाइलें पढ़ना सीखें और DWG फ़ाइलों
  में लेआउट को आसानी से सूचीबद्ध करें। अपने Java अनुप्रयोगों में शक्तिशाली CAD कार्यक्षमता
  को एकीकृत करें।
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java का उपयोग करके DWG को कैसे पढ़ें और DWG में लेआउट्स की सूची
  बनाएं
url: /hi/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java का उपयोग करके DWG को पढ़ना और DWG में लेआउट्स की सूची बनाना

## इंट्रोडक्शन

यदि आपको प्रोग्रामेटिक रूप से **DWG** फ़ाइलें पढ़नी हैं और लेआउट नाम जैसी जानकारी निकालनी है, तो Aspose.CAD for Java इसे सरल बनाता है। इस चरण‑दर‑चरण ट्यूटोरियल में हम आपको **DWG को पढ़ना** और DWG (या DXF) फ़ाइल में मौजूद सभी लेआउट्स की सूची दिखाना बताएँगे। गाइड के अंत तक आप इस क्षमता को किसी भी Java एप्लिकेशन में जोड़ सकेंगे जो CAD डेटा के साथ काम करता है।

## क्विक जवाब
- **कौन सी लाइब्रेरी ज़रूरी है?** Java के लिए Aspose.CAD.
- **क्या मैं किसी भी OS पर DWG फ़ाइलें पढ़ सकता हूँ?** हाँ – Java क्रॉस-प्लेटफ़ॉर्म है.
- **क्या मुझे सैंपल चलाने के लिए लाइसेंस चाहिए?** इवैल्यूएशन के लिए फ़्री ट्रायल काम करता है; प्रोडक्शन के लिए लाइसेंस ज़रूरी है.
- **कौन से CAD फ़ॉर्मैट सपोर्टेड हैं?** DWG, DXF, DWF, और दूसरे.
- **क्या कोड Java8+ के साथ कम्पैटिबल है?** बिल्कुल.

## Java में “dwg कैसे पढ़ें” क्या है?

DWG फ़ाइल को पढ़ना का अर्थ है बाइनरी CAD डेटा को एक ऑब्जेक्ट मॉडल में लोड करना जिसे आप क्वेरी कर सकें। Aspose.CAD जटिल DWG संरचना को सरल .NET/Java क्लासेज़ के पीछे छिपा देता है, जिससे आप केवल आवश्यक जानकारी—इस मामले में लेआउट नाम—पर ध्यान केंद्रित कर सकते हैं।

## DWG फ़ाइल में लेआउट क्यों लिस्ट करें?

DWG में कई लेआउट (पेपर स्पेस, मॉडल स्पेस, कस्टम शीट) हो सकते हैं। लेआउट नाम जानने से आप:
- प्रत्येक लेआउट के लिए रिपोर्ट जनरेट कर सकते हैं।
- विशिष्ट लेआउट को इमेज या PDF में एक्सपोर्ट कर सकते हैं।
- ड्रॉइंग्स की बैच प्रोसेसिंग को ऑटोमेट कर सकते हैं।

## ज़रूरी शर्तें

कोड में डुबकी लगाने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- **Aspose.CAD for Java Library** – नवीनतम JAR को [website](https://releases.aspose.com/cad/java/) से डाउनलोड करें।
- **Java Development Environment** – JDK 8 या उससे ऊपर, और आपका पसंदीदा IDE या बिल्ड टूल।

## नेमस्पेस इंपोर्ट करें

अपने Java स्रोत फ़ाइल में आवश्यक Aspose.CAD क्लासेज़ को इम्पोर्ट करें:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## स्टेप 1: अपनी डॉक्यूमेंट डायरेक्टरी सेट अप करें

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

**“Your Document Directory”** को उस पूर्ण पथ से बदलें जहाँ आपके CAD फ़ाइलें स्थित हैं।

## स्टेप 2: DWG फ़ाइल लोड करें

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

`Image.load` मेथड फ़ाइल फ़ॉर्मेट को स्वचालित रूप से पहचानता है, इसलिए आप **DWG** और **DXF** दोनों फ़ाइलों के लिए समान कोड उपयोग कर सकते हैं।

## स्टेप 3: लेआउट लें और नाम प्रिंट करें

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

यह लूप प्रत्येक लेआउट ऑब्जेक्ट पर इटररेट करता है और उसका नाम कंसोल पर प्रिंट करता है – यह सत्यापित करने का एक सरल तरीका है कि आपने सफलतापूर्वक **DWG** पढ़ ली है और लेआउट जानकारी निकाली है।

## आम गलतियाँ और टिप्स

- **गलत फ़ाइल पाथ** – दोबारा चेक करें कि `dataDir` आपके OS के लिए सही सेपरेटर (`/` या `\\`) के साथ खत्म होता है।
- **अनसपोर्टेड DWG वर्शन** – पक्का करें कि आप हाल का Aspose.CAD वर्शन इस्तेमाल कर रहे हैं; पुराने DWG वर्शन को बदलने की ज़रूरत पड़ सकती है।
- **मेमोरी का इस्तेमाल** – बड़ी ड्रॉइंग काफ़ी मेमोरी खा सकती हैं। हो जाने पर `CadImage` ऑब्जेक्ट को हटा दें: `cadImage.dispose();`.

## नतीजा

बधाई हो! अब आप Aspose.CAD for Java का इस्तेमाल करके **DWG को पढ़कर** और उसके लेआउट की लिस्ट बनाना जानते हैं। यह टेक्नीक ज़्यादा एडवांस्ड CAD ऑटोमेशन के लिए आधार बनती है, जैसे कि खास लेआउट को इमेज या PDF में एक्सपोर्ट करना। ज़्यादा गहन जानकारी के लिए ऑफिशियल [डॉक्यूमेंटेशन](https://reference.aspose.com/cad/java/) देखें।

## FAQ's

### Q1: क्या मैं दूसरे CAD फ़ाइल फ़ॉर्मैट के साथ Aspose.CAD for Java का इस्तेमाल कर सकता हूँ?

A1: हाँ, Aspose.CAD अलग-अलग CAD फ़ॉर्मैट को सपोर्ट करता है, जिसमें DWG, DXF, DWF, और भी बहुत कुछ शामिल हैं।

### Q2: क्या Aspose.CAD for Java के लिए कोई फ़्री ट्रायल उपलब्ध है?

A2: हाँ, आप [यहाँ](https://releases.aspose.com/) से फ़्री ट्रायल ले सकते हैं।

### Q3: मुझे Aspose.CAD for Java के लिए कम्युनिटी सपोर्ट कहाँ से मिल सकता है?

A3: कम्युनिटी सपोर्ट के लिए [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) पर जाएँ।

### Q4: मैं Aspose.CAD for Java के लिए लाइसेंस कैसे खरीदूँ?

A4: आप [परचेज़ पेज](https://purchase.aspose.com/buy) से लाइसेंस खरीद सकते हैं।

### Q5: क्या मैं टेस्टिंग के लिए टेम्पररी लाइसेंस इस्तेमाल कर सकता हूँ?

A5: हाँ, आप टेम्पररी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) ले सकते हैं।

**और सवाल**

**Q: क्या यह तरीका Linux पर DWG फ़ाइलें पढ़ने के लिए काम करता है?**
A: बिल्कुल। क्योंकि सॉल्यूशन प्योर Java है, यह कम्पैटिबल JDK वाले किसी भी OS पर चलता है।

**Q: क्या मैं पूरी ड्रॉइंग को मेमोरी में लोड किए बिना DWG फ़ाइल पढ़ सकता हूँ?**
A: Aspose.CAD ड्रॉइंग को मेमोरी में लोड करता है; बहुत बड़ी फ़ाइलों के लिए उन्हें अलग-अलग थ्रेड में प्रोसेस करने या भविष्य के रिलीज़ में उपलब्ध होने पर स्ट्रीमिंग API का इस्तेमाल करने पर विचार करें।

**सवाल: क्या नाम से लेआउट फ़िल्टर करने का कोई तरीका है?**
जवाब: हाँ – `CadLayoutDictionary` पाने के बाद, आप प्रोसेसिंग से पहले `layout.getLayoutName().equalsIgnoreCase("MyLayout")` चेक कर सकते हैं।

---

**पिछला अपडेट:** 2025-12-28
**इसके साथ टेस्ट किया गया:** Java 24.11 के लिए Aspose.CAD
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}