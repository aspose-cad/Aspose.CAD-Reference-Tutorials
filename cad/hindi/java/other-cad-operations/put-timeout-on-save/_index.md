---
title: Aspose.CAD के साथ CAD के लिए सहेजें पर टाइमआउट
linktitle: टाइमआउट को सेव पर रखें
second_title: Aspose.CAD जावा एपीआई
description: जानें कि Aspose.CAD के साथ अपने जावा एप्लिकेशन के प्रदर्शन को कैसे बढ़ाया जाए। CAD ड्रॉइंग के लिए सेव पर टाइमआउट लगाएं। हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें.
weight: 15
url: /hi/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD के साथ CAD के लिए सहेजें पर टाइमआउट

## परिचय

जावा के लिए Aspose.CAD का उपयोग करके सेव पर टाइमआउट लगाने के ट्यूटोरियल में आपका स्वागत है। इस गाइड में, हम आपको आपके एप्लिकेशन के प्रदर्शन को बढ़ाने के लिए सीएडी ड्राइंग को सहेजने के लिए टाइमआउट सेट करने की प्रक्रिया के बारे में बताएंगे। जावा के लिए Aspose.CAD एक शक्तिशाली लाइब्रेरी है जो आपको अपने जावा अनुप्रयोगों में CAD फ़ाइलों के साथ निर्बाध रूप से काम करने की अनुमति देती है।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
-  जावा लाइब्रेरी के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास जावा लाइब्रेरी के लिए Aspose.CAD आपके प्रोजेक्ट में एकीकृत है। आप लाइब्रेरी को यहां से डाउनलोड कर सकते हैं[वेबसाइट](https://releases.aspose.com/cad/java/).
- विकास परिवेश: सभी आवश्यक उपकरणों और निर्भरताओं के साथ अपना जावा विकास परिवेश स्थापित करें।

## पैकेज आयात करें

आरंभ करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। अपनी जावा फ़ाइल की शुरुआत में निम्नलिखित पंक्तियाँ जोड़ें:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

अब, आइए उदाहरण कोड को चरण-दर-चरण निर्देशों में विभाजित करें:

## चरण 1: स्रोत और आउटपुट निर्देशिकाएँ सेट करें

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

सुनिश्चित करें कि आपके पास अपने CAD चित्रों के लिए सही स्रोत और आउटपुट निर्देशिकाएँ हैं।

## चरण 2: व्यवधान टोकन स्रोत बनाएं

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

सेव ऑपरेशन के दौरान रुकावटों को प्रबंधित करने के लिए एक रुकावट टोकन स्रोत को आरंभ करें।

## चरण 3: सीएडी ड्राइंग लोड करें

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 CAD ड्राइंग को a में लोड करें`CadImage` वस्तु।

## चरण 4: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

सीएडी ड्राइंग के लिए रेखापुंज विकल्प कॉन्फ़िगर करें।

## चरण 5: पीडीएफ विकल्प कॉन्फ़िगर करें

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

वेक्टर रैस्टराइज़ेशन विकल्पों और रुकावट टोकन के साथ पीडीएफ विकल्प सेट करें।

## चरण 6: टाइमआउट के साथ ड्राइंग सहेजें

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

निर्दिष्ट टाइमआउट के साथ सीएडी ड्राइंग को एक पीडीएफ फाइल में सहेजें।

## चरण 7: व्यवधान को संभालें

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

सेव ऑपरेशन को संभालने और एक निर्दिष्ट समय समाप्ति के बाद इसे बाधित करने के लिए एक थ्रेड बनाएं।

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि जावा के लिए Aspose.CAD का उपयोग करके सेव पर टाइमआउट कैसे लगाया जाता है। यह सुविधा आपके सीएडी-संबंधित अनुप्रयोगों की दक्षता को काफी बढ़ा सकती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: मैं जावा के लिए Aspose.CAD कैसे डाउनलोड कर सकता हूं?

 A1: आप इसे यहां से डाउनलोड कर सकते हैं[पृष्ठ जारी करता है](https://releases.aspose.com/cad/java/).

### Q2: मैं जावा के लिए Aspose.CAD के लिए दस्तावेज़ कहां पा सकता हूं?

 A2: देखें[प्रलेखन](https://reference.aspose.com/cad/java/) विस्तृत जानकारी के लिए.

### Q3: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

उ3: हाँ, आप नि:शुल्क परीक्षण प्राप्त कर सकते हैं[इस लिंक](https://releases.aspose.com/).

### Q4: मैं अस्थायी लाइसेंस कैसे प्राप्त करूं?

 ए4: विजिट करें[यहाँ](https://purchase.aspose.com/temporary-license/) अस्थायी लाइसेंस विवरण के लिए.

### Q5: सहायता चाहिए या कोई प्रश्न हैं?

 A5: की ओर जाएं[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन के लिए.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
