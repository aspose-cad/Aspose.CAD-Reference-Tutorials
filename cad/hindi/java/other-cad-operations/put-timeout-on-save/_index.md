---
date: 2026-06-19
description: Aspose.CAD for Java के साथ CAD ड्रॉइंग्स को सहेजते समय timeout सेट करना
  सीखें। प्रदर्शन को बढ़ाएँ, हैंग्स से बचें, और CAD को PDF में कुशलतापूर्वक export
  करें।
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: सहेजने पर timeout लगाएँ
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD के साथ CAD के लिए सहेजने पर timeout कैसे सेट करें
url: /hi/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD में Aspose.CAD के साथ सहेजने पर टाइमआउट कैसे सेट करें

## परिचय

इस व्यापक गाइड में आप सीखेंगे **कैसे टाइमआउट सेट करें** जब आप Aspose.CAD for Java का उपयोग करके CAD ड्रॉइंग्स को सहेजते हैं। टाइमआउट लागू करने से लंबे समय तक चलने वाले सहेजने के ऑपरेशन आपके एप्लिकेशन को हैंग होने से रोकते हैं, जो विशेष रूप से तब महत्वपूर्ण है जब आपको बैच प्रोसेसिंग परिदृश्यों में **CAD को PDF में निर्यात** करना हो या **DWG को PDF में बदलना** हो। Aspose.CAD for Java 50 से अधिक CAD फ़ॉर्मैट्स का समर्थन करता है और पूरे दस्तावेज़ को मेमोरी में लोड किए बिना कई सौ पृष्ठों वाली फ़ाइलों को संभाल सकता है, जिससे आपको पूर्वानुमानित प्रदर्शन और संसाधन उपयोग मिलता है।

## त्वरित उत्तर
- **टाइमआउट क्या करता है?** यह निर्दिष्ट अवधि के बाद सहेजने के ऑपरेशन को रोक देता है, थ्रेड को मुक्त करता है और संसाधन लीक को रोकता है।  
- **कौन सा क्लास टाइमआउट को नियंत्रित करता है?** `InterruptionTokenSource` सहेजने की प्रक्रिया में उपयोग किए जाने वाले कैंसलेशन टोकन को प्रदान करता है।  
- **क्या टाइमआउट के बाद भी मैं CAD को PDF में निर्यात कर सकता हूँ?** हाँ – आप इंटरप्शन एक्सेप्शन को पकड़ सकते हैं और पुनः प्रयास कर सकते हैं या विफलता को लॉग कर सकते हैं।  
- **क्या मुझे विशेष लाइसेंस चाहिए?** एक सामान्य Aspose.CAD लाइसेंस पर्याप्त है; टाइमआउट फीचर अंतर्निहित है।  
- **क्या यह तरीका थ्रेड‑सेफ है?** हाँ, जब प्रत्येक सहेजना अपने स्वयं के थ्रेड में अपने टोकन के साथ चलता है।

## CAD सहेजने के ऑपरेशन्स में टाइमआउट क्या है?
टाइमआउट एक कॉन्फ़िगर करने योग्य समय सीमा है जो यदि पार हो जाती है तो सहेजने की प्रक्रिया को रोक देती है और एक इंटरप्शन एक्सेप्शन उठाती है। यह आपके Java एप्लिकेशन को जटिल ड्रॉइंग्स या I/O बाधाओं के कारण अनिश्चितकालीन हैंग से बचाता है।

## CAD फ़ाइलें सहेजते समय टाइमआउट क्यों सेट करें?
Aspose.CAD सामान्य ड्रॉइंग्स के लिए **DWG को PDF में बदल** सकता है और **CAD को PDF में निर्यात** कर सकता है, जो एक सेकंड से कम समय में होता है, लेकिन अत्यधिक बड़ी या भ्रष्ट फ़ाइलें मिनटों तक ले सकती हैं। एक टाइमआउट निर्धारित करके आप सुनिश्चित करते हैं कि कोई भी एकल सहेजना, उदाहरण के लिए, 30 सेकंड से अधिक न हो, जिससे कुल बैच थ्रूपुट स्थिर रहता है और थ्रेड की कमी से बचा जा सकता है।

## पूर्वापेक्षाएँ

ट्यूटोरियल में डुबकी लगाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:
- **Aspose.CAD for Java Library** – सुनिश्चित करें कि आपके प्रोजेक्ट में Aspose.CAD for Java लाइब्रेरी एकीकृत है। आप लाइब्रेरी को [website](https://releases.aspose.com/cad/java/) से डाउनलोड कर सकते हैं।
- **Development Environment** – सभी आवश्यक टूल्स और डिपेंडेंसीज़ के साथ अपना Java विकास पर्यावरण सेट अप करें।

## पैकेज इम्पोर्ट करें

शुरू करने के लिए, आवश्यक पैकेजों को अपने Java प्रोजेक्ट में इम्पोर्ट करें। अपने Java फ़ाइल की शुरुआत में निम्नलाइनों को जोड़ें:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

अब, चलिए उदाहरण कोड को चरण‑दर‑चरण निर्देशों में विभाजित करते हैं:

## CAD ड्रॉइंग्स को सहेजते समय टाइमआउट कैसे सेट करें?

अपनी CAD फ़ाइल लोड करें, इच्छित टाइमआउट के साथ एक `InterruptionTokenSource` बनाएं, और टोकन को PDF सहेजने के विकल्पों में पास करें। यदि ऑपरेशन टाइमआउट से अधिक हो जाता है, तो Aspose.CAD एक `OperationCanceledException` फेंकता है, जिसे आप पकड़ कर विफलता को सुगमता से संभाल सकते हैं।

### चरण 1: स्रोत और आउटपुट डायरेक्टरी सेट करें

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

सुनिश्चित करें कि आपके CAD ड्रॉइंग्स के लिए सही स्रोत और आउटपुट डायरेक्टरी हैं।

### चरण 2: इंटरप्शन टोकन स्रोत बनाएं

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

सहेजने के ऑपरेशन के दौरान इंटरप्शन को प्रबंधित करने के लिए एक इंटरप्शन टोकन स्रोत को इनिशियलाइज़ करें।

### चरण 3: CAD ड्रॉइंग लोड करें

`CadImage` क्लास Aspose.CAD का मुख्य ऑब्जेक्ट है जो मेमोरी में CAD ड्रॉइंग को दर्शाता है, और रेंडरिंग तथा कन्वर्ज़न के लिए मेथड्स प्रदान करता है।

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### चरण 4: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

`CadRasterizationOptions` यह निर्दिष्ट करता है कि CAD ड्रॉइंग को इमेज में कैसे रास्टराइज़ किया जाए।

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

CAD ड्रॉइंग के लिए रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें।

### चरण 5: PDF विकल्प कॉन्फ़िगर करें

`PdfOptions` CAD ड्रॉइंग को PDF दस्तावेज़ के रूप में सहेजने की सेटिंग्स को परिभाषित करता है।

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

वेक्टर रास्टराइज़ेशन विकल्प और इंटरप्शन टोकन के साथ PDF विकल्प सेट करें।

### चरण 6: टाइमआउट के साथ ड्रॉइंग सहेजें

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

निर्दिष्ट टाइमआउट के साथ CAD ड्रॉइंग को PDF फ़ाइल में सहेजें।

### चरण 7: इंटरप्शन को संभालें

`OperationCanceledException` तब फेंका जाता है जब सहेजने का ऑपरेशन निर्दिष्ट टाइमआउट से अधिक हो जाता है।

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

सहेजने के ऑपरेशन को संभालने के लिए एक थ्रेड बनाएं और निर्दिष्ट टाइमआउट के बाद उसे इंटरप्ट करें।

## सामान्य समस्याएँ और समाधान

- **टाइमआउट बहुत छोटा** – यदि आपको बार‑बार इंटरप्शन मिलते हैं, तो बड़े ड्रॉइंग्स को संभालने के लिए टाइमआउट मान बढ़ाएँ।  
- **InterruptedException नहीं पकड़ा गया** – एप्लिकेशन को क्रैश होने से बचाने के लिए हमेशा सहेजने के कॉल को `OperationCanceledException` के लिए try‑catch ब्लॉक में रखें।  
- **मेमोरी खपत** – पूरी फ़ाइल को मेमोरी में लोड करने के बजाय आउटपुट को स्ट्रीम करने के लिए `PdfOptions.setVectorRasterizationOptions` का उपयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं इस फीचर का उपयोग बैच जॉब में DWG को PDF में बदलने के लिए कर सकता हूँ?**  
A: हाँ, प्रत्येक कन्वर्ज़न को अपने स्वयं के थ्रेड में अलग इंटरप्शन टोकन के साथ रैप करें ताकि प्रति‑फ़ाइल समय सीमा लागू हो सके।

**Q: क्या टाइमआउट सभी आउटपुट फ़ॉर्मैट्स पर काम करता है?**  
A: टाइमआउट मैकेनिज़्म `InterruptionTokenSource` से जुड़ा है और किसी भी फ़ॉर्मैट के साथ काम करता है जो टोकन का सम्मान करता है, जिसमें PDF, PNG, और SVG शामिल हैं।

**Q: टाइमआउट के बाद आंशिक रूप से लिखी गई फ़ाइलों के साथ क्या होता है?**  
A: Aspose.CAD स्वचालित रूप से अधूरी आउटपुट को हटा देता है, इसलिए आपको भ्रष्ट PDF नहीं मिलेंगे।

**Q: क्या उत्पादन उपयोग के लिए लाइसेंस आवश्यक है?**  
A: हाँ, व्यावसायिक डिप्लॉयमेंट के लिए एक वैध Aspose.CAD लाइसेंस आवश्यक है; मूल्यांकन के लिए एक मुफ्त ट्रायल उपलब्ध है।

**Q: इंटरप्शन टोकन्स के उपयोग के अधिक उदाहरण मैं कहाँ पा सकता हूँ?**  
A: आधिकारिक Aspose.CAD दस्तावेज़ अतिरिक्त कोड स्निपेट्स और सर्वोत्तम प्रथाओं के दिशानिर्देश प्रदान करता है।

## अतिरिक्त संसाधन

- [releases पेज](https://releases.aspose.com/cad/java/) – नवीनतम Aspose.CAD for Java रिलीज़ के लिए प्रत्यक्ष डाउनलोड पेज।  
- [दस्तावेज़ीकरण](https://reference.aspose.com/cad/java/) – पूरा API रेफ़रेंस और डेवलपर गाइड्स।  
- [यह लिंक](https://releases.aspose.com/) – सामान्य Aspose उत्पाद रिलीज़।  
- [यहाँ](https://purchase.aspose.com/temporary-license/) – परीक्षण के लिए एक अस्थायी लाइसेंस प्राप्त करें।  
- [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) – समुदाय समर्थन और चर्चाएँ।

## निष्कर्ष

आप अब Aspose.CAD for Java के साथ CAD ड्रॉइंग्स को सहेजते समय **टाइमआउट सेट करने** में निपुण हो गए हैं। अपने वर्कफ़्लो में `InterruptionTokenSource` को एकीकृत करके आप विश्वसनीय रूप से **CAD को PDF में निर्यात** या **DWG को PDF में बदल** सकते हैं, बिना लंबे समय तक चलने वाले हैंग के जोखिम के, जिससे आपका एप्लिकेशन उत्तरदायी और स्केलेबल बना रहता है।

---

**Last Updated:** 2026-06-19  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [Aspose.CAD for Java का उपयोग करके DWG को PDF या रास्टर में निर्यात करें](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java का उपयोग करके विशिष्ट DWG लेआउट को PDF में निर्यात करें](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Aspose.CAD for Java का उपयोग करके DWG को PNG और अन्य रास्टर फ़ॉर्मैट्स में बदलें](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}