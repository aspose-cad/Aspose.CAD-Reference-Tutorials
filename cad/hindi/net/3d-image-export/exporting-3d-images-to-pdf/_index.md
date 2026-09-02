---
date: 2026-07-04
description: Aspose.CAD for .NET का उपयोग करके 3D CAD इमेजेज से PDF पेज आकार सेट करना
  और PDF एक्सपोर्ट करना सीखें – DWG को PDF में बदलने और CAD को PDF के रूप में सेव
  करने के लिए चरण‑दर‑चरण गाइड।
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: 3D इमेजेज को PDF में एक्सपोर्ट करना
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: PDF पेज आकार सेट करें – Aspose.CAD के साथ 3D इमेजेज को PDF में एक्सपोर्ट करें
url: /hi/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 3D छवियों को PDF में निर्यात करना - Aspose.CAD ट्यूटोरियल

## परिचय

यदि आपको 3‑D CAD ड्राइंग को PDF में बदलते समय **PDF पेज साइज सेट करना** है, तो आप सही जगह पर आए हैं। यह ट्यूटोरियल आपको चरण दर चरण दिखाता है कि CAD फ़ाइल को कैसे लोड करें, रास्टराइज़ेशन विकल्पों को कॉन्फ़िगर करें—जिसमें कस्टम पेज डाइमेंशन शामिल हैं—और Aspose.CAD for .NET का उपयोग करके उच्च‑गुणवत्ता वाला PDF उत्पन्न करें। अंत तक आप **CAD से PDF निर्यात करना**, **CAD को PDF के रूप में सहेजना**, और AutoCAD स्थापित किए बिना हर लेआउट विवरण को नियंत्रित कर पाएँगे।

## त्वरित उत्तर
- **“CAD से PDF निर्यात” का क्या अर्थ है?** यह एक CAD ड्राइंग (DWG, DXF, DGN, आदि) को PDF में बदलता है जिसे किसी भी डिवाइस पर खोला जा सकता है।  
- **कौन सी लाइब्रेरी रूपांतरण करती है?** Aspose.CAD for .NET रास्टराइज़ेशन और PDF निर्यात बिना बाहरी निर्भरताओं के प्रदान करती है।  
- **क्या मुझे लाइसेंस की आवश्यकता है?** उत्पादन के लिए एक अस्थायी या पूर्ण लाइसेंस आवश्यक है; एक मुफ्त ट्रायल उपलब्ध है।  
- **क्या मैं कस्टम पेज डाइमेंशन सेट कर सकता हूँ?** हाँ—`RasterizationOptions` में `PageWidth` और `PageHeight` का उपयोग करें।  
- **क्या 3‑D ज्योमेट्री बरकरार रहेगी?** 3‑D एंटिटीज़ को रास्टराइज़ किया जाता है; पूर्ण 3‑D समर्थन के लिए `TypeOfEntities.Entities3D` सक्षम करें।

## CAD के संदर्भ में “export PDF” क्या है?

CAD से PDF निर्यात करने का अर्थ है एक CAD ड्राइंग (DWG, DXF, DGN, आदि) को लेकर उसे PDF फ़ाइल में बदलना, जिसमें वेक्टर ग्राफिक्स, रास्टराइज़्ड 3‑D दृश्य, और सटीक पेज लेआउट जानकारी हो सकती है, जिससे उन लोगों के साथ साझा करना आसान हो जाता है जिनके पास CAD सॉफ़्टवेयर नहीं है।

## PDF निर्यात करने के लिए Aspose.CAD का उपयोग क्यों करें?

Aspose.CAD आपको **PDF पेज साइज सेट करें** और PDFs को पूरी तरह से प्रबंधित .NET कोड में निर्यात करने देता है। यह 50 से अधिक CAD फ़ॉर्मैट्स का समर्थन करता है, 2 GB तक की फ़ाइलों को बिना पूरे दस्तावेज़ को मेमोरी में लोड किए प्रोसेस करता है, और लाइन वेट, रंग, तथा वैकल्पिक 3‑D एंटिटी रेंडरिंग को अधिकतम 1200 DPI रास्टराइज़ेशन के साथ संरक्षित रखता है। लाइब्रेरी Windows, Linux, और macOS पर चलती है, इसलिए उत्पन्न PDFs किसी भी प्लेटफ़ॉर्म पर काम करेंगे।

## पूर्वापेक्षाएँ

- **Aspose.CAD for .NET** स्थापित है। इसे [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) से डाउनलोड करें।  
- एक फ़ोल्डर जिसमें वह CAD फ़ाइलें हों जिन्हें आप बदलना चाहते हैं (उदा., `C:\CAD\`).  
- .NET 6.0 या बाद का संस्करण (या .NET Framework 4.7.2)।  

## नेमस्पेस आयात करें

`using` स्टेटमेंट्स Aspose.CAD नेमस्पेस को आयात करते हैं जो रास्टराइज़ेशन और PDF विकल्पों के साथ काम करने के लिए आवश्यक हैं।  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## स्टेप‑बाय‑स्टेप गाइड

### CAD को PDF में निर्यात करते समय PDF पेज साइज कैसे सेट करें?

अपनी CAD फ़ाइल लोड करें, `RasterizationOptions` में पेज डाइमेंशन कॉन्फ़िगर करें, उन विकल्पों को `PdfOptions` इंस्टेंस से जोड़ें, और `Save` को कॉल करें। यह चार‑स्टेप प्रक्रिया आपको आउटपुट साइज और क्वालिटी पर पूर्ण नियंत्रण देती है जबकि कोड को संक्षिप्त रखती है।

### स्टेप 1: CAD इमेज लोड करें

`Image` क्लास एक CAD ड्राइंग को दर्शाती है जो मेमोरी में लोड हुई है, रास्टराइज़ेशन के लिए तैयार।  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### स्टेप 2: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें (CAD को PDF के रूप में सहेजें)

`RasterizationOptions` क्लास यह निर्धारित करती है कि CAD डेटा कैसे रास्टराइज़ किया जाता है, जिसमें पेज साइज, DPI, और 3‑D एंटिटीज़ का रेंडर होना शामिल है।  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### स्टेप 3: PDF विकल्प सेट करें (CAD से PDF बनाएं)

`PdfOptions` क्लास आउटपुट फ़ॉर्मेट सेटिंग्स को रखती है और रास्टराइज़ेशन विकल्पों को PDF जनरेशन से जोड़ती है।  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### स्टेप 4: PDF के रूप में सहेजें (3D मॉडल से PDF जनरेट करें)

`Image` ऑब्जेक्ट पर `Save` मेथड रास्टराइज़्ड कंटेंट को निर्दिष्ट PDF फ़ाइल में लिखता है, जिससे एक तैयार‑शेयर करने योग्य दस्तावेज़ बनता है।  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## सामान्य समस्याएँ और समाधान

| Issue | Reason | Fix |
|-------|--------|-----|
| **आउटपुट PDF खाली है** | गलत लेआउट नाम या `Model` लेआउट गायब है। | `rasterizationOptions.Layouts` CAD फ़ाइल में मौजूद लेआउट से मेल खाता है, यह सत्यापित करें। |
| **कम रिज़ॉल्यूशन** | डिफ़ॉल्ट रास्टराइज़ेशन DPI कम है। | सेव करने से पहले `rasterizationOptions.Resolution = 300;` सेट करें। |
| **3‑D एंटिटीज़ नहीं दिख रही हैं** | `TypeOfEntities` टिप्पणी किया गया है। | `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;` की टिप्पणी हटाएँ। |
| **लाइसेंस अपवाद** | लाइसेंस के बिना ट्रायल का उपयोग करना। | `License license = new License(); license.SetLicense("Aspose.CAD.lic");` के माध्यम से अस्थायी या स्थायी लाइसेंस लागू करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या Aspose.CAD सभी CAD फ़ाइल फ़ॉर्मैट्स के साथ संगत है?**  
A: हाँ, Aspose.CAD 50 से अधिक इनपुट और आउटपुट फ़ॉर्मैट्स का समर्थन करता है, जिसमें DWG, DXF, DGN, STL, और IFC शामिल हैं, जो किसी भी प्रोजेक्ट के लिए लचीलापन सुनिश्चित करता है।

**Q: क्या मैं PDF निर्यात करते समय पेज डाइमेंशन को कस्टमाइज़ कर सकता हूँ?**  
A: बिल्कुल। `Save` कॉल करने से पहले `RasterizationOptions` में `PageWidth` और `PageHeight` को पॉइंट्स, इंच या मिलीमीटर में किसी भी आकार में सेट करें।

**Q: क्या Aspose.CAD के लिए अस्थायी लाइसेंस उपलब्ध हैं?**  
A: हाँ, आप [Temporary License](https://purchase.aspose.com/temporary-license/) पर जाकर Aspose.CAD के लिए अस्थायी लाइसेंस प्राप्त कर सकते हैं।

**Q: मैं अतिरिक्त समर्थन या समुदाय चर्चा कहाँ पा सकता हूँ?**  
A: विशेषज्ञ सहायता और साथियों‑से‑साथियों सलाह के लिए [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

**Q: क्या Aspose.CAD का मुफ्त ट्रायल संस्करण उपलब्ध है?**  
A: हाँ, आप [free trial](https://releases.aspose.com/) तक पहुँचकर Aspose.CAD की सुविधाओं का अन्वेषण कर सकते हैं।

## निष्कर्ष

अब आपके पास Aspose.CAD for .NET का उपयोग करके **PDF पेज साइज सेट करें** और **3D CAD छवियों से PDF निर्यात करें** के लिए एक पूर्ण, उत्पादन‑तैयार विधि है। रास्टराइज़ेशन विकल्पों को समायोजित करके आप रिज़ॉल्यूशन, पेज लेआउट, और 3‑D एंटिटी रेंडरिंग को किसी भी दस्तावेज़ीकरण आवश्यकता के अनुसार बारीकी से ट्यून कर सकते हैं। विभिन्न DPI सेटिंग्स और पेज डाइमेंशन के साथ प्रयोग करें ताकि फ़ाइल आकार और दृश्य गुणवत्ता के बीच सही संतुलन प्राप्त हो सके।

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [विशिष्ट लेआउट्स को PDF में निर्यात करना - Aspose.CAD गाइड](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [DWG को PDF या रास्टर इमेजेज में निर्यात करना - Aspose.CAD गाइड](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Aspose.CAD for .NET में DGN को PDF में निर्यात करें](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**अंतिम अपडेट:** 2026-07-04  
**परीक्षित संस्करण:** Aspose.CAD 24.11 for .NET  
**लेखक:** Aspose