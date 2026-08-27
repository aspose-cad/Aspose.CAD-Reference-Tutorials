---
date: 2026-06-09
description: Aspose.CAD for Java के साथ DXF को WMF में कैसे बदलें सीखें, जिसमें मुफ्त
  ट्रायल, Java 8+ समर्थन, और वैकल्पिक PDF निर्यात शामिल है। कोड उदाहरणों के साथ चरण‑दर‑चरण
  गाइड।
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: जावा का उपयोग करके DXF को WMF फ़ॉर्मेट में निर्यात करें
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD का उपयोग करके जावा में DXF को WMF में बदलें
url: /hi/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DXF को WMF में Aspose.CAD का उपयोग करके Java में परिवर्तित करें

## परिचय

इस ट्यूटोरियल में आप सीखेंगे कि Aspose.CAD for Java के साथ **convert DXF to WMF** कैसे किया जाता है। चाहे आपको CAD ड्रॉइंग्स को Windows‑आधारित रिपोर्ट में एम्बेड करना हो, Office दस्तावेज़ों के लिए हल्के वेक्टर ग्राफ़िक्स बनाना हो, या बैच रूपांतरण को स्वचालित करना हो, DXF को WMF में परिवर्तित करना इंजीनियरिंग और रिपोर्टिंग पाइपलाइन में एक सामान्य आवश्यकता है। हम DXF ड्रॉइंग को लोड करने, रास्टराइज़ेशन विकल्पों को कॉन्फ़िगर करने, परिणाम को WMF के रूप में सहेजने, और वैकल्पिक रूप से उसी ड्रॉइंग को PDF में निर्यात करने की प्रक्रिया को चरण-दर-चरण देखेंगे।

## त्वरित उत्तर

- **क्या मैं मुफ्त ट्रायल के साथ DXF को WMF में परिवर्तित कर सकता हूँ?** हाँ – Aspose एक पूर्ण कार्यात्मक 30‑दिन का ट्रायल प्रदान करता है।  
- **कौन सा Java संस्करण आवश्यक है?** Java 8 या बाद का।  
- **क्या कोड चलाने के लिए लाइसेंस चाहिए?** उत्पादन के लिए लाइसेंस आवश्यक है; ट्रायल विकास और परीक्षण के लिए काम करता है।  
- **क्या रूपांतरण बिना नुकसान के है?** वेक्टर डेटा संरक्षित रहता है; रास्टराइज़ेशन विकल्प आपको रिज़ॉल्यूशन नियंत्रित करने देते हैं।  
- **क्या मैं उसी ड्रॉइंग को PDF में भी निर्यात कर सकता हूँ?** बिल्कुल – नीचे “Export to PDF” चरण देखें।  

## “convert DXF to WMF” क्या है?

DXF को WMF में परिवर्तित करना का अर्थ है Drawing Exchange Format (DXF) फ़ाइल—जो एक व्यापक रूप से उपयोग किया जाने वाला CAD फ़ॉर्मेट है—को Windows Metafile (WMF) में बदलना। WMF एक वेक्टर इमेज फ़ॉर्मेट है जो Microsoft Office, Windows एप्लिकेशन और कई रिपोर्टिंग टूल्स के साथ सहजता से एकीकृत होता है।

## Java के लिए Aspose.CAD क्यों उपयोग करें?

Aspose.CAD for Java एक शुद्ध‑Java, बिना‑नेटीव‑DLL इंजन प्रदान करता है जो CAD फ़ाइलों को **99 % से अधिक वेक्टर फ़िडेलिटी** के साथ परिवर्तित करता है, लेयर्स, रंग, लाइन स्टाइल और हैच पैटर्न को संरक्षित रखता है। यह **50+ इनपुट और आउटपुट फ़ॉर्मेट**—जिसमें DXF, DWG, DGN, PDF, PNG, SVG, और WMF शामिल हैं—को सपोर्ट करता है, साथ ही बिल्ट‑इन रास्टराइज़ेशन विकल्पों के माध्यम से पेज साइज, DPI, और बैकग्राउंड कलर को फाइन‑ट्यून करने की सुविधा देता है। वही API PDF, PNG, और SVG निर्यात को भी संभालता है, जिससे कई लाइब्रेरीज़ की आवश्यकता समाप्त हो जाती है।

### मुख्य लाभ
- **कोई बाहरी निर्भरताएँ नहीं** – शुद्ध Java, किसी भी OS पर काम करता है जो Java चलाता है।  
- **उच्च‑फ़िडेलिटी रेंडरिंग** – लाइन वेट, रंग, और हैच विवरण को बनाए रखता है।  
- **बिल्ट‑इन रास्टराइज़ेशन** – पेज आयाम, रिज़ॉल्यूशन, और बैकग्राउंड को नियंत्रित करता है।  
- **वन‑स्टॉप रूपांतरण** – वही क्लासेज WMF, PDF, PNG, SVG आदि में निर्यात करती हैं।  

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास है:

- **Aspose.CAD for Java** को अपने प्रोजेक्ट में इंटीग्रेट किया हुआ। इसे आधिकारिक साइट से डाउनलोड करें: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **डॉक्यूमेंट डायरेक्टरी** जहाँ आपके DXF फ़ाइलें संग्रहीत हैं (उदा., `Your Document Directory/DXFDrawings/`).  

## नेमस्पेस आयात करें

निम्नलिखित इम्पोर्ट्स Aspose.CAD क्लासेज़ को लाते हैं जो CAD फ़ाइलों को लोड करने, रास्टराइज़ करने और सहेजने के लिए आवश्यक हैं।
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## स्टेप‑बाय‑स्टेप गाइड

### Java में DXF को WMF में कैसे परिवर्तित करें?

अपने DXF फ़ाइल को `Image.load("yourFile.dxf")` से लोड करें, इच्छित पेज साइज और DPI के लिए `CadRasterizationOptions` को कॉन्फ़िगर करें, फिर `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))` को कॉल करें। यह तीन‑स्टेप पैटर्न पूर्ण रूपांतरण करता है जबकि वेक्टर क्वालिटी को बरकरार रखता है और केवल कुछ लाइनों के कोड की आवश्यकता होती है।

#### चरण 1: DXF ड्रॉइंग लोड करें

Image.load DXF फ़ाइल को Aspose.CAD Image ऑब्जेक्ट में पढ़ता है।
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### चरण 2: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

CadRasterizationOptions CAD ड्रॉइंग को रास्टराइज़ करने के लिए पेज साइज, रिज़ॉल्यूशन, और बैकग्राउंड निर्दिष्ट करता है।
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### चरण 3: WMF के रूप में सहेजें

ImageSaveOptions जिसमें SaveFormat.WMF है, Aspose.CAD को आउटपुट को Windows Metafile के रूप में लिखने के लिए बताता है।
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### चरण 4: संसाधनों को मुक्त करें

image.close() को कॉल करने से Aspose.CAD Image ऑब्जेक्ट द्वारा उपयोग किए गए नेटिव संसाधन मुक्त हो जाते हैं।
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### चरण 5: वैकल्पिक – PDF में निर्यात करें

PdfOptions तब PDF‑विशिष्ट सेटिंग्स को कॉन्फ़िगर करता है जब इमेज को PDF दस्तावेज़ के रूप में सहेजा जाता है।
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** आप वही `CadRasterizationOptions` ऑब्जेक्ट PDF निर्यात के लिए `PdfOptions` इंस्टेंस में पास करके पुनः उपयोग कर सकते हैं, जिससे सेटअप की कुछ लाइनों की बचत होगी।

## Aspose CAD Java का उपयोग करके DXF को PDF में कैसे निर्यात करें?

PDF में निर्यात करने के लिए वही लोडिंग और रास्टराइज़ेशन चरणों का पालन किया जाता है; बस WMF सहेजने के फ़ॉर्मेट को PDF से बदलें। `new ImageSaveOptions(SaveFormat.Pdf)` का उपयोग करें और वैकल्पिक रूप से PDF‑विशिष्ट विकल्प जैसे कम्प्रेशन लेवल या लेखक मेटाडेटा सेट करें। यह एक‑लाइनर रूपांतरण एक सर्चेबल, पेज‑सटीक PDF उत्पन्न करता है जो मूल CAD लेआउट को प्रतिबिंबित करता है।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | वेरिएबल `cadImage` परिभाषित नहीं है (यह `image` होना चाहिए)। | `cadImage` को `image` से बदलें या वेरिएबल का नाम लगातार रखें। |
| **Output WMF is blank** | रास्टराइज़ेशन पेज साइज बहुत छोटा है या बैकग्राउंड रंग ट्रांसपेरेंट सेट है। | `PageWidth`/`PageHeight` बढ़ाएँ या `rasterizationOptions.setBackgroundColor(Color.WHITE);` के माध्यम से बैकग्राउंड रंग सेट करें। |
| **License exception** | प्रोडक्शन में वैध Aspose लाइसेंस के बिना चल रहा है। | एप्लिकेशन शुरू होने पर लाइसेंस फ़ाइल लागू करें: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## निष्कर्ष

अब आपके पास Aspose.CAD for Java का उपयोग करके **DXF को WMF में परिवर्तित** करने के लिए एक पूर्ण, प्रोडक्शन‑रेडी वर्कफ़्लो है, जिसमें **उसी ड्रॉइंग को PDF में निर्यात** करने का वैकल्पिक चरण भी शामिल है। यह तरीका आपको उच्च‑गुणवत्ता वाला वेक्टर आउटपुट देता है जो Windows‑आधारित रिपोर्टिंग और डॉक्यूमेंटेशन टूल्स के साथ सहजता से एकीकृत होता है, जबकि आपका कोडबेस सरल और निर्भरता‑मुक्त रहता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: मैं Aspose.CAD दस्तावेज़ीकरण कहाँ पा सकता हूँ?
A1: आप दस्तावेज़ीकरण यहाँ प्राप्त कर सकते हैं [यहाँ](https://reference.aspose.com/cad/java/).

### Q2: मैं Aspose.CAD for Java कैसे डाउनलोड करूँ?
A2: लाइब्रेरी यहाँ डाउनलोड करें [यहाँ](https://releases.aspose.com/cad/java/).

### Q3: क्या कोई मुफ्त ट्रायल उपलब्ध है?
A3: हाँ, आप एक मुफ्त ट्रायल यहाँ प्राप्त कर सकते हैं [यहाँ](https://releases.aspose.com/).

### Q4: अस्थायी लाइसेंस विकल्प चाहिए?
A4: अस्थायी लाइसेंस यहाँ देखें [यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: मैं समर्थन कहाँ प्राप्त कर सकता हूँ?
A5: Aspose.CAD समर्थन फ़ोरम यहाँ देखें [यहाँ](https://forum.aspose.com/c/cad/19).

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं बड़ी DXF फ़ाइलें (सैकड़ों MB) मेमोरी खत्म हुए बिना परिवर्तित कर सकता हूँ?**  
A: हाँ। फ़ाइल को try‑with‑resources ब्लॉक में लोड करें और `Image` ऑब्जेक्ट को तुरंत डिस्पोज़ करें। मेमोरी उपयोग कम रखने के लिए `CadRasterizationOptions.setPageWidth/Height` को उचित आकार पर सेट करें।

**Q: क्या WMF आउटपुट लेयर जानकारी को बनाए रखता है?**  
A: WMF एक फ्लैट वेक्टर फ़ॉर्मेट है, इसलिए लेयर हायरार्की फ्लैट हो जाती है, लेकिन लाइन स्टाइल, रंग, और हैच पैटर्न संरक्षित रहते हैं।

**Q: क्या WMF के लिए कस्टम DPI सेट करना संभव है?**  
A: सहेजने से पहले DPI निर्धारित करने के लिए `rasterizationOptions.setResolution(300);` का उपयोग करें।

**Q: क्या मैं एक ही रन में कई DXF फ़ाइलों को बैच‑कन्वर्ट कर सकता हूँ?**  
A: बिल्कुल। एक डायरेक्टरी के माध्यम से लूप करें, प्रत्येक फ़ाइल को लोड करें, और वही रास्टराइज़ेशन और सहेजने की लॉजिक लागू करें।

**Q: कौन से Java संस्करण समर्थित हैं?**  
A: Aspose.CAD for Java Java 8 और बाद के संस्करणों को सपोर्ट करता है, जिसमें Java 11, 17, और नए LTS रिलीज़ शामिल हैं।

---

**अंतिम अपडेट:** 2026-06-09  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.11  
**लेखक:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## संबंधित ट्यूटोरियल

- [CAD से PDF बनाएं – Aspose.CAD for Java के साथ DXF को PDF में निर्यात करें](/cad/java/additional-features/export-dxf-to-pdf/)
- [DXF से PDF बनाएं: Aspose.CAD for Java के साथ लेयर निर्यात करें](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Aspose.CAD के साथ Java में DXF लेआउट को JPEG इमेज में कैसे परिवर्तित करें](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}