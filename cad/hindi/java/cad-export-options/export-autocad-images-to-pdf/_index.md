---
date: 2026-10-19
description: Aspose.CAD for Java का उपयोग करके कस्टम PDF पेज साइज के साथ AutoCAD ड्रॉइंग्स
  को PDF में निर्यात करना सीखें। यह चरण‑दर‑चरण गाइड DWG को PDF में बदलने, रास्टराइज़ेशन
  विकल्पों और लाइसेंसिंग को कवर करता है।
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: AutoCAD इमेजेज को PDF में निर्यात करें
og_description: Aspose.CAD for Java का उपयोग करके AutoCAD ड्रॉइंग्स को PDF में निर्यात
  करते समय कस्टम PDF पेज साइज सेट करें। मिनटों में DWG से PDF रूपांतरण, रास्टराइज़ेशन
  सेटिंग्स और लाइसेंसिंग सीखें।
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Aspose.CAD के साथ AutoCAD निर्यात के लिए कस्टम PDF पेज साइज सेट करें
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Aspose.CAD के साथ AutoCAD निर्यात के लिए कस्टम PDF पेज साइज सेट करें
url: /hi/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# AutoCAD PDF निर्यात - AutoCAD छवियों को PDF में निर्यात करें Aspose.CAD for Java के साथ

## परिचय

यदि आपको **DWG को PDF में बदलना** है और आउटपुट फ़ाइल के सटीक आयामों को नियंत्रित करना है, तो आप सही जगह पर आए हैं। यह ट्यूटोरियल आपको दिखाता है कि Aspose.CAD for Java के साथ AutoCAD छवियों को PDF में निर्यात करते समय **कस्टम PDF पेज आकार** कैसे सेट किया जाए। गाइड के अंत तक आप जानेंगे कि DWG कैसे लोड करें, DPI और पेज चौड़ाई/ऊँचाई जैसी रास्टराइज़ेशन विकल्पों को कॉन्फ़िगर करें, लाइसेंस लागू करें, और प्रोडक्शन‑रेडी PDF जनरेट करें।

## त्वरित उत्तर
- **क्या मैं Java के साथ DWG को PDF में बदल सकता हूँ?** हाँ – Aspose.CAD for Java मूल रूप से DWG, DXF, DWF और कई अन्य CAD फ़ॉर्मेट्स को सपोर्ट करता है।  
- **क्या उत्पादन उपयोग के लिए लाइसेंस की आवश्यकता है?** एक पूर्ण Aspose.CAD लाइसेंस सभी मूल्यांकन सीमाओं को हटा देता है; परीक्षण के लिए एक अस्थायी लाइसेंस उपलब्ध है।  
- **कौन से Java संस्करण संगत हैं?** लाइब्रेरी Java 8 और उसके बाद के सभी JDK के साथ काम करती है।  
- **मैं PDF पेज के आयाम कैसे बदलूँ?** `PdfOptions.getRasterizationOptions()` पर `pageWidth` और `pageHeight` को अपनी आवश्यक किसी भी आकार में सेट करें।  
- **क्या 3‑D रेंडरिंग समर्थित है?** हाँ – 3‑D एंटिटीज़ को रास्टराइज़ करने के लिए `TypeOfEntities.Entities3D` को सक्षम करें।

## AutoCAD PDF निर्यात क्या है?
AutoCAD PDF निर्यात का अर्थ है वेक्टर‑आधारित CAD ड्रॉइंग्स (DWG, DXF, DWF, आदि) को एक पोर्टेबल PDF दस्तावेज़ में बदलना, जबकि लेयर्स, लाइन वेट्स और वैकल्पिक 3‑D ज्योमेट्री को संरक्षित रखना। इससे आप डिज़ाइनों को क्लाइंट्स के साथ साझा कर सकते हैं, ड्रॉइंग्स को आर्काइव कर सकते हैं, या CAD सॉफ़्टवेयर स्थापित किए बिना प्रिंट कर सकते हैं।

## DWG को PDF में बदलने के लिए Aspose.CAD for Java क्यों उपयोग करें?
Aspose.CAD for Java DWG को PDF में बदलने के लिए आदर्श है क्योंकि यह व्यापक फ़ॉर्मेट समर्थन प्रदान करता है, शुद्ध Java पर बिना किसी नेटिव डिपेंडेंसी के चलता है, DPI और पेज आकार पर पूर्ण नियंत्रण के साथ उच्च‑रिज़ॉल्यूशन रास्टराइज़ेशन देता है, और लचीला लाइसेंसिंग शामिल करता है जो आपको ट्रायल से शुरू करके प्रोडक्शन तक स्केल करने की सुविधा देता है।

- **विस्तृत फ़ॉर्मेट कवरेज** – 50+ इनपुट और आउटपुट फ़ॉर्मेट्स को सपोर्ट करता है, जिसमें DWG, DXF, DWF, DGN, और PDF शामिल हैं।  
- **शुद्ध Java इम्प्लीमेंटेशन** – कोई नेटिव DLLs या बाहरी डिपेंडेंसी नहीं, इसलिए किसी भी प्लेटफ़ॉर्म पर डिप्लॉयमेंट सरल है।  
- **उच्च‑रिज़ॉल्यूशन रास्टराइज़ेशन** – आप DPI, पेज आकार, और लेआउट निर्दिष्ट कर सकते हैं, जिससे आपको परिणाम के **कस्टम PDF पेज आकार** पर पूर्ण नियंत्रण मिलता है।  
- **स्केलेबल लाइसेंसिंग** – मुफ्त ट्रायल से शुरू करें, फिर स्थायी **Aspose CAD लाइसेंस** में अपग्रेड करें।  

## पूर्वापेक्षाएँ

- **Java Development Kit** – आपके मशीन पर JDK 8 या नया स्थापित हो।  
- **Aspose.CAD for Java** – नवीनतम JAR को [download link](https://releases.aspose.com/cad/java/) से डाउनलोड करें।  
- **वर्किंग डायरेक्टरी** – एक फ़ोल्डर जिसमें स्रोत DWG फ़ाइलें हों और जो उत्पन्न PDFs को प्राप्त करेगा।  

## नेमस्पेस आयात करें

`Image` क्लास Aspose.CAD का कोर ऑब्जेक्ट है जो मेमोरी में CAD ड्रॉइंग का प्रतिनिधित्व करता है। कोडिंग शुरू करने से पहले आवश्यक पैकेज आयात करें।

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

अब चलिए कोड को चरण‑दर‑चरण देखते हैं।

## DWG को PDF में निर्यात करते समय कस्टम PDF पेज आकार कैसे सेट करें?

अपना DWG लोड करें, इच्छित पेज चौड़ाई और ऊँचाई निर्धारित करें, और फिर परिणाम को PDF के रूप में सहेजें – यह सब कुछ है जो आपको कस्टम पेज आकार वाला PDF बनाने के लिए चाहिए। निम्नलिखित चरण सटीक क्रम और आवश्यक न्यूनतम कोड को दर्शाते हैं।

### चरण 1: रिसोर्स डायरेक्टरी पाथ सेट करें

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **प्रो टिप:** `"Your Document Directory"` को उस फ़ोल्डर के पूर्ण पाथ से बदलें जिसे आपने पूर्वापेक्षाओं में बनाया था।

### चरण 2: CAD इमेज लोड करें

`Image` क्लास CAD फ़ाइल को लोड करता है और आपको Aspose.CAD के रास्टराइज़ेशन इंजन तक पहुँच देता है।

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **यह क्यों महत्वपूर्ण है:** एक बार CAD फ़ाइल लोड हो जाने पर, आप PDF में रेंडर करने से पहले रास्टराइज़ेशन विकल्पों को बदल सकते हैं।

### चरण 3: रास्टराइज़ेशन विकल्प सेट करें

`CadRasterizationOptions` क्लास यह निर्धारित करता है कि CAD ड्रॉइंग को PDF के रूप में सहेजने से पहले कैसे रास्टराइज़ किया जाए। `pageWidth` और `pageHeight` को समायोजित करके **कस्टम PDF पेज आकार** परिभाषित करें। आप `setTypeOfEntities` लाइन को अनकमेंट करके 3‑D रेंडरिंग भी सक्षम कर सकते हैं।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – पिक्सेल में मापे जाते हैं; इन मानों को A4, Letter, या किसी भी कस्टम डाइमेंशन से मेल खाने के लिए बदलें।  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – आवश्यकता होने पर 3‑D एंटिटीज़ को रेंडर करता है।  
- `setLayouts` – निर्धारित करता है कि कौन सा लेआउट (Model, Layout1, आदि) रास्टराइज़ किया जाए।  

### चरण 4: PDF विकल्प कॉन्फ़िगर करें

`PdfOptions` क्लास PDF‑विशिष्ट सेटिंग्स रखता है और रास्टराइज़ेशन विकल्पों को आउटपुट फ़ाइल से जोड़ता है, जिससे कस्टम पेज आयाम सही ढंग से लागू होते हैं।

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### चरण 5: PDF सहेजें

`save` मेथड रेंडर की गई इमेज को निर्दिष्ट PDF फ़ाइल में लिखता है।

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

परिणामी फ़ाइल, `Export3DImagestoPDF_out_.pdf`, आपके मूल AutoCAD ड्रॉइंग का **save cad as pdf** प्रतिनिधित्व है, जिसमें आपने निर्दिष्ट सटीक पेज आयाम हैं।

## सामान्य समस्याएँ और समाधान

| लक्षण | संभावित कारण | समाधान |
|---------|--------------|-----|
| खाली PDF आउटपुट | रास्टराइज़ेशन विकल्प सेट नहीं हैं या लेआउट मेल नहीं खाता | `setLayouts` आपके CAD फ़ाइल में लेआउट नाम से मेल खाता है, यह सत्यापित करें। |
| कम‑रिज़ॉल्यूशन छवि | `pageWidth`/`pageHeight` बहुत छोटा है या DPI कम है | आयाम बढ़ाएँ या `rasterizationOptions.setResolution(...)` को उच्च DPI के साथ कॉल करें। |
| लाइसेंस अपवाद | कोई वैध लाइसेंस लागू नहीं किया गया | स्थायी Aspose.CAD लाइसेंस लागू करें या परीक्षण के लिए अस्थायी लाइसेंस का उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.CAD for Java को अन्य CAD फ़ाइल फ़ॉर्मेट्स के साथ उपयोग कर सकता हूँ?**  
**A:** हाँ, लाइब्रेरी DWG, DXF, DWF, DGN, और कई अन्य को सपोर्ट करती है, जिससे आपको प्रोजेक्ट्स में लचीलापन मिलता है।

**Q: Aspose.CAD for Java के लिए अस्थायी लाइसेंस कैसे प्राप्त करूँ?**  
**A:** मूल्यांकन के लिए समय‑सीमित लाइसेंस का अनुरोध करने हेतु [temporary license page](https://purchase.aspose.com/temporary-license/) पर जाएँ।

**Q: क्या रास्टराइज़ेशन के लिए लेआउट विकल्प हैं?**  
**A:** बिल्कुल। `setLayouts("Model")` का उपयोग करें या अन्य लेआउट नाम निर्दिष्ट करके यह नियंत्रित करें कि कौन सा दृश्य रेंडर किया जाए।

**Q: क्या मैं आउटपुट PDF फ़ाइल का आकार कस्टमाइज़ कर सकता हूँ?**  
**A:** हाँ – रास्टराइज़ेशन विकल्पों में `pageWidth` और `pageHeight` को अपनी आवश्यकता के अनुसार किसी भी आयाम में बदलें।

**Q: Aspose.CAD for Java से संबंधित मदद या मुद्दों पर चर्चा कहाँ कर सकते हैं?**  
**A:** समर्पित [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) समुदाय समर्थन और Aspose टीम की आधिकारिक प्रतिक्रियाएँ प्रदान करता है।

## अतिरिक्त FAQ (AI‑friendly फ़ॉर्मेट)

**Q: क्या Aspose.CAD को Windows या Linux पर किसी नेटिव लाइब्रेरी की आवश्यकता है?**  
**A:** नहीं। Aspose.CAD for Java एक शुद्ध‑Java लाइब्रेरी है, इसलिए यह किसी भी प्लेटफ़ॉर्म पर चलता है जो JDK को सपोर्ट करता है, बिना अतिरिक्त नेटिव DLLs के।

**Q: लाइब्रेरी कितनी बड़ी DWG फ़ाइल प्रोसेस कर सकती है?**  
**A:** लाइब्रेरी कई‑सौ पेजों वाले ड्रॉइंग्स (500 MB तक) को पूरी फ़ाइल को मेमोरी में लोड किए बिना संभाल सकती है, इसके स्ट्रीमिंग आर्किटेक्चर के कारण।

**Q: क्या एक ही रन में कई DWG फ़ाइलों को PDF में बैच‑कन्वर्ट करना संभव है?**  
**A:** हाँ। किसी डायरेक्टरी पर इटररेट करें, प्रत्येक फ़ाइल को `Image.load()` से लोड करें, समान रास्टराइज़ेशन विकल्प लागू करें, और प्रत्येक आउटपुट PDF के लिए `save()` कॉल करें।

**Q: एक सामान्य सर्वर पर मैं किस प्रदर्शन की उम्मीद कर सकता हूँ?**  
**A:** मानक 2.5 GHz CPU पर 300 DPI पर 100‑पेज DWG को कन्वर्ट करने में लगभग 12 सेकंड लगते हैं, Aspose के बेंचमार्क टेस्ट के आधार पर।

**Q: क्या लाइब्रेरी PDF में लेयर जानकारी को संरक्षित रखती है?**  
**A:** जबकि आउटपुट रास्टराइज़्ड है, लेयर्स, लाइन वेट्स, और रंगों की दृश्य उपस्थिति सटीक रूप से पुनः निर्मित होती है।

**Last Updated:** 2026-10-19  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## संबंधित ट्यूटोरियल

- [Aspose.CAD Java के साथ DWG को PDF में निर्यात करें और ट्रैकिंग सक्षम करें](/cad/java/additional-features/enable-tracking/)
- [Aspose.CAD Java का उपयोग करके DWG को PDF में निर्यात: विशिष्ट लेआउट](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Aspose.CAD for Java के साथ DWG को BMP में निर्यात और यूनिट टाइप से CAD आकार समायोजित करें](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}