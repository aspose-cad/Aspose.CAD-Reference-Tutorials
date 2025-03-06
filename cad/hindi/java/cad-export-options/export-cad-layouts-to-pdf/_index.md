---
title: जावा के लिए Aspose.CAD के साथ CAD लेआउट को PDF में निर्यात करें
linktitle: सीएडी लेआउट को पीडीएफ में निर्यात करें
second_title: Aspose.CAD जावा एपीआई
description: आसानी से सीएडी लेआउट को पीडीएफ में निर्यात करने के लिए जावा के लिए Aspose.CAD का अन्वेषण करें। कुशल, विश्वसनीय और डेवलपर-अनुकूल।
weight: 11
url: /hi/java/cad-export-options/export-cad-layouts-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के लिए Aspose.CAD के साथ CAD लेआउट को PDF में निर्यात करें

## परिचय

कंप्यूटर-एडेड डिज़ाइन (सीएडी) के निरंतर विकसित हो रहे क्षेत्र में, जावा के लिए Aspose.CAD, CAD फ़ाइलों में हेरफेर और परिवर्तित करने के लिए एक शक्तिशाली उपकरण के रूप में सामने आता है। इस ट्यूटोरियल में, हम जावा के लिए Aspose.CAD का उपयोग करके CAD लेआउट को PDF में निर्यात करने की प्रक्रिया में आपका मार्गदर्शन करेंगे। चाहे आप एक अनुभवी डेवलपर हों या सिर्फ सीएडी की दुनिया में कदम रख रहे हों, यह चरण-दर-चरण मार्गदर्शिका आपको इस बहुमुखी जावा लाइब्रेरी की पूरी क्षमता का दोहन करने में मदद करेगी।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  जावा के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास लाइब्रेरी स्थापित है। आप इसे Aspose वेबसाइट से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/java/).

- जावा विकास वातावरण: सुनिश्चित करें कि आपकी मशीन पर जावा विकास वातावरण स्थापित है।

अब जब आपने सब कुछ सेट कर लिया है, तो आइए ट्यूटोरियल के साथ शुरुआत करें।

## नामस्थान आयात करें

अपने जावा कोड में, आवश्यक नामस्थान आयात करके प्रारंभ करें। ये आयात जावा के लिए Aspose.CAD के साथ काम करने के लिए आवश्यक कक्षाओं और विधियों तक पहुंच प्रदान करते हैं।

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//आयात com.aspose.cad.imageoptions.TypeOfEntities;
```

## चरण 1: CAD फ़ाइल लोड करें

 का उपयोग करके CAD फ़ाइल को अपने जावा एप्लिकेशन में लोड करके प्रारंभ करें`Image.load` तरीका। प्रतिस्थापित करें`"conic_pyramid.dxf"` आपकी CAD फ़ाइल के पथ के साथ।

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## चरण 2: रैस्टराइज़ेशन विकल्प सेट करें

 का एक उदाहरण बनाएं`CadRasterizationOptions` यह परिभाषित करने के लिए कि सीएडी संस्थाओं को कैसे व्यवस्थित किया जाना चाहिए। अपनी आवश्यकताओं के अनुसार पृष्ठ की चौड़ाई, पृष्ठ की ऊंचाई और लेआउट स्केलिंग जैसे मापदंडों को समायोजित करें।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## चरण 3: पीडीएफ विकल्प सेट करें

 का एक उदाहरण बनाएं`PdfOptions` और इसे रैस्टराइज़ेशन विकल्पों के साथ संबद्ध करें। इसके अतिरिक्त, पीडीएफ निर्यात के लिए ग्राफिक्स विकल्प सेट करें, जैसे स्मूथिंग मोड, टेक्स्ट रेंडरिंग हिंट और इंटरपोलेशन मोड।

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## चरण 4: पीडीएफ में निर्यात करें

 अंत में, का उपयोग करके CAD लेआउट को एक पीडीएफ फ़ाइल में निर्यात करें`save` की विधि`cadImage` वस्तु।

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

बधाई हो! आपने Java के लिए Aspose.CAD का उपयोग करके CAD लेआउट को PDF में सफलतापूर्वक निर्यात कर लिया है। अपने CAD फ़ाइल हेरफेर अनुभव को बढ़ाने के लिए Aspose.CAD द्वारा दी जाने वाली अतिरिक्त सुविधाओं और कार्यात्मकताओं का बेझिझक पता लगाएं।

## निष्कर्ष

इस ट्यूटोरियल में, हमने Java के लिए Aspose.CAD का उपयोग करके CAD लेआउट को PDF में निर्यात करने की प्रक्रिया के बारे में जाना। अपनी मजबूत सुविधाओं और उपयोग में आसान एपीआई के साथ, Aspose.CAD डेवलपर्स को अपने जावा अनुप्रयोगों में CAD फ़ाइलों के साथ कुशलतापूर्वक काम करने का अधिकार देता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य CAD फ़ाइल स्वरूपों के साथ Java के लिए Aspose.CAD का उपयोग कर सकता हूँ?

 A1: हां, Aspose.CAD DWG, DXF, DWF और अन्य सहित विभिन्न CAD प्रारूपों का समर्थन करता है। दस्तावेज़ीकरण की जाँच करें[यहाँ](https://reference.aspose.com/cad/java/) पूरी सूची के लिए.

### Q2: क्या जावा के लिए Aspose.CAD के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

 उ2: हां, आप नि:शुल्क परीक्षण के साथ Aspose.CAD की सुविधाओं का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं जावा के लिए Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A3: Aspose.CAD फोरम पर जाएँ[यहाँ](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन के लिए. प्रीमियम समर्थन के लिए, लाइसेंस खरीदने पर विचार करें[यहाँ](https://purchase.aspose.com/buy).

### Q4: स्वचालित और मैन्युअल लेआउट स्केलिंग के बीच क्या अंतर है?

A4: स्वचालित लेआउट स्केलिंग निर्दिष्ट पृष्ठ आयामों के आधार पर लेआउट आकार को समायोजित करती है, जबकि मैन्युअल स्केलिंग आपको कस्टम स्केलिंग मान सेट करने की अनुमति देती है।

### Q5: क्या मैं निर्यात की गई पीडीएफ फाइलों के स्वरूप को अनुकूलित कर सकता हूं?

A5: हां, आप निर्यातित पीडीएफ की गुणवत्ता और उपस्थिति को नियंत्रित करने के लिए कोड में ग्राफिक्स विकल्पों को अनुकूलित कर सकते हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
