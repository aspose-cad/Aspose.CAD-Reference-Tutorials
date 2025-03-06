---
title: CAD ड्रॉइंग में वॉटरमार्क जोड़ें - जावा ट्यूटोरियल के लिए Aspose.CAD
linktitle: वॉटरमार्क जोड़ें
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD का उपयोग करके वैयक्तिकृत वॉटरमार्क के साथ अपने CAD चित्रों को बेहतर बनाएं। निर्बाध एकीकरण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 12
url: /hi/java/other-cad-operations/add-watermark/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD ड्रॉइंग में वॉटरमार्क जोड़ें - जावा ट्यूटोरियल के लिए Aspose.CAD

## परिचय

जावा के लिए Aspose.CAD का उपयोग करके CAD चित्रों में वॉटरमार्क जोड़ने पर इस व्यापक मार्गदर्शिका में आपका स्वागत है। इस ट्यूटोरियल में, आप सीखेंगे कि वॉटरमार्क को कुशलतापूर्वक कैसे एकीकृत किया जाए, व्यक्तिगत संदेशों या ब्रांडिंग के साथ अपने सीएडी दस्तावेज़ों को बढ़ाया जाए। जावा के लिए Aspose.CAD वॉटरमार्क जोड़ने की प्रक्रिया को सरल बनाते हुए सुविधाओं का एक शक्तिशाली सेट प्रदान करता है।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

-  जावा के लिए Aspose.CAD: सुनिश्चित करें कि आपके जावा वातावरण में Aspose.CAD लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/java/).
- जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जेडीके का नवीनतम संस्करण स्थापित है।

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, आरंभ करने के लिए आवश्यक Aspose.CAD पैकेज आयात करें:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## चरण 1: नया MTEXT जोड़ें

```java
//नया MTEXT जोड़ें
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## चरण 2: टेक्स्ट जैसी सरल इकाई जोड़ें

आप टेक्स्ट जैसी अधिक सरल इकाई भी जोड़ सकते हैं:

```java
// या टेक्स्ट जैसी अधिक सरल इकाई जोड़ें
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## चरण 3: पीडीएफ में निर्यात करें

जोड़े गए वॉटरमार्क के साथ CAD ड्राइंग को एक पीडीएफ फाइल में निर्यात करें:

```java
// पीडीएफ में निर्यात करें
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.CAD का उपयोग करके अपने CAD चित्रों में सफलतापूर्वक वॉटरमार्क जोड़ दिए हैं। यह सरल लेकिन शक्तिशाली प्रक्रिया आपको अपने डिज़ाइन को निजीकृत करने या ब्रांडिंग के साथ उनकी सुरक्षा करने की अनुमति देती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD सभी CAD फ़ाइल स्वरूपों के साथ संगत है?

A1: Aspose.CAD DWG, DXF, DWT और DWF सहित विभिन्न CAD प्रारूपों का समर्थन करता है।

### Q2: क्या मैं वॉटरमार्क टेक्स्ट के स्वरूप को अनुकूलित कर सकता हूँ?

उ2: हां, टेक्स्ट आकार, रंग और स्थिति सहित वॉटरमार्क की उपस्थिति पर आपका पूरा नियंत्रण है।

### Q3: क्या Java के लिए Aspose.CAD का कोई परीक्षण संस्करण उपलब्ध है?

 उ3: हाँ, आप परीक्षण संस्करण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A4: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन के लिए.

### Q5: मैं जावा के लिए Aspose.CAD के लिए संपूर्ण दस्तावेज़ कहां पा सकता हूं?

 A5: का संदर्भ लें[प्रलेखन](https://reference.aspose.com/cad/java/) विस्तृत जानकारी के लिए.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
