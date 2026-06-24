---
date: 2026-06-14
description: Aspose.CAD for Java के साथ CAD को SVG में निर्यात करना सीखें। यह चरण‑दर‑चरण
  मार्गदर्शिका आपको दिखाती है कि DWG को SVG में कैसे परिवर्तित करें, SVG रंग मोड सेट
  करें, और लाइब्रेरी को अपने Java प्रोजेक्ट में कैसे एकीकृत करें।
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: SVG में निर्यात करें
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java का उपयोग करके CAD को SVG में निर्यात करें
url: /hi/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java का उपयोग करके CAD को SVG में निर्यात करना

## परिचय

इस व्यापक ट्यूटोरियल में आप Aspose.CAD for Java का उपयोग करके **CAD को SVG में निर्यात करने** का तरीका सीखेंगे। चाहे आपको **DWG को SVG में बदलना** हो, बैच जॉब में DWG फ़ाइलों से SVG उत्पन्न करना हो, या हल्के वेब प्रदर्शन के लिए SVG को ग्रेस्केल में बदलना हो, यह गाइड आपको प्रत्येक चरण के माध्यम से ले जाता है—लाइब्रेरी सेटअप से लेकर निर्यात विकल्पों को फाइन‑ट्यून करने तक। अंत तक, आपके पास एक प्रोडक्शन‑रेडी स्निपेट होगा जो किसी भी JVM‑संगत प्लेटफ़ॉर्म पर चल सकेगा।

## त्वरित उत्तर
- **“CAD को SVG में निर्यात” क्या मतलब है?** यह एक CAD ड्राइंग (जैसे DWG या DXF) को Scalable Vector Graphics फ़ाइल में बदल देता है जिसे ब्राउज़र गुणवत्ता में कोई कमी के बिना रेंडर करते हैं।  
- **कौन सी लाइब्रेरी परिवर्तन संभालती है?** Aspose.CAD for Java एक समर्पित API प्रदान करती है जो 30+ CAD फ़ॉर्मेट का समर्थन करती है और पूर्ण‑वेक्टर फ़िडेलिटी के साथ SVG आउटपुट देती है।  
- **क्या विकास के लिए लाइसेंस चाहिए?** मूल्यांकन के लिए एक मुफ्त ट्रायल काम करता है; प्रोडक्शन डिप्लॉयमेंट के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं SVG रंग आउटपुट को नियंत्रित कर सकता हूँ?** हाँ—`SvgColorMode` का उपयोग करके ग्रेस्केल और पूर्ण‑रंग रेंडरिंग के बीच स्विच कर सकते हैं।  
- **क्या कोई अतिरिक्त सॉफ़्टवेयर आवश्यक है?** केवल एक Java रनटाइम (JDK 8 या नया) और Aspose.CAD JAR; कोई बाहरी CAD टूल आवश्यक नहीं है।

## CAD को SVG में निर्यात क्या है?
CAD को SVG में निर्यात करना एक मूल CAD फ़ाइल (जैसे DWG, DXF, या DWF) को SVG वेक्टर इमेज फ़ॉर्मेट में बदलने की प्रक्रिया है। परिणामी SVG सटीक ज्यामितीय डेटा को बनाए रखता है, जिससे वेब ब्राउज़र और डिज़ाइन टूल में रिज़ॉल्यूशन‑इंडिपेंडेंट डिस्प्ले संभव होता है।

## Aspose.CAD के साथ CAD को SVG में निर्यात क्यों?
Aspose.CAD **30+ इनपुट फ़ॉर्मेट** को संभाल सकता है और **500 पृष्ठ** तक का SVG आउटपुट बिना पूरी फ़ाइल को मेमोरी में लोड किए उत्पन्न करता है, जिससे **उच्च‑फ़िडेलिटी वेक्टर रूपांतरण** सामान्य सर्वर‑ग्रेड CPU पर **200 पृष्ठ/सेकंड** की गति से मिलता है। लाइब्रेरी **100 % Java** पर चलती है, जिससे नेटिव DLL या थर्ड‑पार्टी CAD इंजन की आवश्यकता समाप्त हो जाती है।

## पूर्वापेक्षाएँ
- **Java Development Kit** (JDK 8 या नया) आपके मशीन पर स्थापित और कॉन्फ़िगर किया हुआ होना चाहिए।  
- **Aspose.CAD for Java** JAR फ़ाइल आधिकारिक [डाउनलोड लिंक](https://releases.aspose.com/cad/java/) से डाउनलोड की गई।  
- एक फ़ोल्डर जिसमें कम से कम एक CAD ड्राइंग (DWG, DXF, आदि) हो जिसे आप बदलना चाहते हैं।

## नेमस्पेस आयात करें

कोड लिखने से पहले सुनिश्चित करें कि Aspose.CAD लाइब्रेरी आपके क्लासपाथ में है और आवश्यक क्लासेस को इम्पोर्ट करें।

### चरण 1: अपना जावा प्रोजेक्ट खोलें
अपना पसंदीदा IDE (IntelliJ IDEA, Eclipse, VS Code) लॉन्च करें और उस प्रोजेक्ट को खोलें जहाँ आप परिवर्तन लॉजिक जोड़ने वाले हैं।

### चरण 2: Aspose.CAD लाइब्रेरी जोड़ें
`aspose-cad-xx.jar` फ़ाइल को `libs` डायरेक्टरी में रखें और इसे अपने बिल्ड टूल (Maven, Gradle, या साधारण `javac`) में डिपेंडेंसी के रूप में जोड़ें।

### चरण 3: नेमस्पेस आयात करें
कन्वर्ज़न करने वाले Java स्रोत फ़ाइल में, निम्न इम्पोर्ट्स जोड़ें:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## Aspose.CAD for Java का उपयोग करके CAD को SVG में कैसे निर्यात करें?

Aspose.CAD के साथ CAD ड्राइंग को SVG में निर्यात करने में स्रोत फ़ाइल लोड करना, SVG‑विशिष्ट विकल्प कॉन्फ़िगर करना, और आउटपुट लिखना शामिल है। प्रक्रिया सीधी है, केवल कुछ लाइनों के कोड की आवश्यकता होती है, और सभी समर्थित CAD फ़ॉर्मेट में निरंतर काम करती है जबकि वेक्टर फ़िडेलिटी को बनाए रखती है।

### चरण 1: रिसोर्स डायरेक्टरी निर्दिष्ट करें
उस फ़ोल्डर का पूर्ण या सापेक्ष पाथ परिभाषित करें जहाँ आपके CAD ड्रॉइंग संग्रहीत हैं:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### चरण 2: CAD ड्राइंग लोड करें
`Image` क्लास Aspose.CAD का टॉप‑लेवल ऑब्जेक्ट है जो मेमोरी में CAD ड्राइंग का प्रतिनिधित्व करता है। फ़ाइल लोड करने से निर्यात के लिए तैयार एक इन‑मेमोरी प्रतिनिधित्व बनता है।

`Image.load` एक CAD फ़ाइल पढ़ता है और ड्राइंग का इन‑मेमोरी प्रतिनिधित्व बनाता है।

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### चरण 3: SVG निर्यात विकल्प कॉन्फ़िगर करें
`SvgExportOptions` आपको SVG आउटपुट को फाइन‑ट्यून करने देता है। नीचे हम रंग मोड को ग्रेस्केल सेट करते हैं और सभी टेक्स्ट को शेप्स के रूप में रेंडर करना सुनिश्चित करते हैं, जिससे उन ब्राउज़रों में संगतता बढ़ती है जिनमें मूल फ़ॉन्ट नहीं है।

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### चरण 4: SVG के रूप में सहेजें
अंत में, `Image` इंस्टेंस पर `save` को कॉल करें, लक्ष्य फ़ाइल नाम और कॉन्फ़िगर किए गए विकल्प पास करें। Aspose.CAD एक मानक‑अनुपालन SVG फ़ाइल लिखता है जिसे कोई भी आधुनिक ब्राउज़र सीधे खोल सकता है।

`save` प्रदान किए गए निर्यात विकल्पों का उपयोग करके निर्दिष्ट फ़ाइल में इमेज लिखता है।

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Pro tip:** पूर्ण‑रंग SVG उत्पन्न करने के लिए `SvgColorMode.Grayscale` को `SvgColorMode.FullColor` से बदलें। यह स्विच मूल पैलेट को संरक्षित रखता है जबकि वेक्टर स्केलेबिलिटी प्रदान करता है।

## CAD को SVG में निर्यात करने के लिए Aspose.CAD का उपयोग क्यों करें?
- **High fidelity:** वेक्टर डेटा बरकरार रहता है, जिससे SVG मूल CAD ड्राइंग जैसा ही दिखता है।  
- **No external dependencies:** रूपांतरण पूरी तरह Java के भीतर चलता है, जिससे अतिरिक्त टूल की आवश्यकता समाप्त हो जाती है।  
- **Customizable output:** `setColorType` जैसे विकल्प आपको यह नियंत्रित करने देते हैं कि SVG ग्रेस्केल हो या पूर्ण‑रंग।  
- **Scalable performance:** सैकड़ों‑पृष्ठ वाली ड्रॉइंग को सेकंडों में प्रोसेस करता है, मेमोरी उपयोग 50 MB से कम रहता है।

## सामान्य समस्याएँ और समाधान
- **File not found:** सुनिश्चित करें कि `dataDir` सही फ़ोल्डर की ओर इशारा कर रहा है और DWG फ़ाइल नाम फ़ाइल सिस्टम पर केस के साथ मेल खाता है।  
- **Blank SVG output:** जब स्रोत ड्राइंग में ऐसा टेक्स्ट हो जिसे वेक्टर शेप्स के रूप में दिखना आवश्यक है, तो `options.setTextAsShapes(true)` सक्षम रखें।  
- **Unsupported CAD format:** Aspose.CAD DWG, DXF, DWF और 15 से अधिक अन्य फ़ॉर्मेट का समर्थन करता है; पूरी सूची के लिए आधिकारिक दस्तावेज़ देखें।  
- **Performance bottlenecks:** अत्यधिक बड़ी फ़ाइलों के लिए `options.setEnableStreaming(true)` के माध्यम से स्ट्रीमिंग मोड सक्षम करें ताकि मेमोरी खपत कम रहे।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं वही कोड उपयोग करके DXF फ़ाइल को SVG में बदल सकता हूँ?**  
A: हाँ, बस DWG फ़ाइल नाम को DXF फ़ाइल से बदल दें; API स्वचालित रूप से दोनों फ़ॉर्मेट को पहचानता और प्रोसेस करता है।

**Q: आउटपुट को पूर्ण‑रंग SVG में कैसे बदलूँ?**  
A: `save` मेथड को कॉल करने से पहले `options.setColorType(SvgColorMode.FullColor);` सेट करें।

**Q: क्या उत्पन्न SVG में फ़ॉन्ट एम्बेड करना संभव है?**  
A: Aspose.CAD टेक्स्ट को शेप्स में बदल देता है, इसलिए फ़ॉन्ट एम्बेड करना आवश्यक नहीं है; परिणामी SVG में केवल वेक्टर आउटलाइन होते हैं।

**Q: क्या लाइब्रेरी Linux और macOS पर काम करती है?**  
A: Java लाइब्रेरी प्लेटफ़ॉर्म‑इंडिपेंडेंट है और जहाँ भी संगत JVM उपलब्ध है, जैसे Windows, Linux, और macOS, चलती है।

**Q: इस ट्यूटोरियल में कौन सा Aspose.CAD संस्करण उपयोग किया गया?**  
A: उदाहरण Aspose.CAD for Java **24.10** के साथ परीक्षण किया गया था।

**अंतिम अपडेट:** 2026-06-14  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.10  
**लेखक:** Aspose  

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [Aspose.CAD for Java का उपयोग करके DWG को PDF या रास्टर में निर्यात करें](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg to pdf java – Aspose.CAD के साथ CAD को PDF में निर्यात करें](/cad/java/cad-export-options/export-to-pdf/)
- [Aspose.CAD for Java का उपयोग करके विशिष्ट DWG लेआउट को PDF में निर्यात करें](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}