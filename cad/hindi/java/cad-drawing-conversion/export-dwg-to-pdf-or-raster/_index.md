---
title: जावा के लिए Aspose.CAD का उपयोग करके DWG को PDF या Raster में निर्यात करें
linktitle: DWG को PDF या Raster में निर्यात करें
second_title: Aspose.CAD जावा एपीआई
description: Aspose.CAD का उपयोग करके जावा में DWG फ़ाइलों को PDF या रेखापुंज छवियों में निर्यात करने की निर्बाध प्रक्रिया का अन्वेषण करें। यह चरण-दर-चरण मार्गदर्शिका सटीकता और दक्षता सुनिश्चित करती है।
weight: 13
url: /hi/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के लिए Aspose.CAD का उपयोग करके DWG को PDF या Raster में निर्यात करें

## परिचय

कंप्यूटर-एडेड डिज़ाइन (सीएडी) की गतिशील दुनिया में, चित्रों का कुशल संचालन महत्वपूर्ण है। जावा के लिए Aspose.CAD DWG फ़ाइलों को पीडीएफ या रैस्टर छवियों में निर्यात करने के लिए एक शक्तिशाली समाधान प्रदान करता है। यह ट्यूटोरियल आपको प्रक्रिया के माध्यम से मार्गदर्शन करेगा, यह सुनिश्चित करते हुए कि आप जावा के लिए Aspose.CAD की पूरी क्षमता का उपयोग करेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- जावा प्रोग्रामिंग की बुनियादी समझ.
-  जावा लाइब्रेरी के लिए Aspose.CAD स्थापित किया गया। यदि नहीं, तो इसे डाउनलोड करें[यहाँ](https://releases.aspose.com/cad/java/).
- परीक्षण प्रयोजनों के लिए एक DWG फ़ाइल। आप प्रदत्त "Bottom_plate.dwg" फ़ाइल का उपयोग कर सकते हैं।

## नामस्थान आयात करें

अपने जावा प्रोजेक्ट में, प्रक्रिया को किकस्टार्ट करने के लिए आवश्यक नामस्थान आयात करें:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## चरण 1: DWG फ़ाइल लोड करें

 Aspose.CAD का उपयोग करके अपनी DWG फ़ाइल लोड करके प्रारंभ करें`Image` कक्षा:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## चरण 2: इकाई प्रकार निर्धारित करें

इसके बाद, लोड की गई DWG फ़ाइल के यूनिट प्रकार की जाँच करें:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## चरण 3: रैस्टराइज़ेशन विकल्प सेट करें

इकाई प्रकार के आधार पर, रैस्टराइज़ेशन विकल्पों को कॉन्फ़िगर करें:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // मीट्रिक इकाइयां
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // शाही इकाइयां
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## चरण 4: पीडीएफ विकल्प कॉन्फ़िगर करें

पीडीएफ निर्यात विकल्प सेट करें:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## चरण 5: पीडीएफ के रूप में सहेजें

अंत में, DWG फ़ाइल को PDF के रूप में सहेजें:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

आखिर तुमने इसे हासिल कर ही लिया है! आपने Java के लिए Aspose.CAD का उपयोग करके DWG फ़ाइल को PDF में सफलतापूर्वक निर्यात कर लिया है।

## निष्कर्ष

इस ट्यूटोरियल ने जावा के लिए DWG फ़ाइलों को पीडीएफ या रैस्टर छवियों में निर्यात करने के लिए Aspose.CAD का लाभ उठाने पर चरण-दर-चरण मार्गदर्शिका प्रदान की है। यह लाइब्रेरी प्रक्रिया को सरल बनाती है, जिससे आप अपने जावा अनुप्रयोगों में सीएडी ड्राइंग को कुशलतापूर्वक संभाल सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं जावा के लिए अन्य जावा फ्रेमवर्क के साथ Aspose.CAD का उपयोग कर सकता हूँ?

A1: हां, जावा के लिए Aspose.CAD लोकप्रिय जावा फ्रेमवर्क के साथ सहजता से एकीकृत होता है।

### Q2: क्या जावा के लिए Aspose.CAD के लिए एक अस्थायी लाइसेंस उपलब्ध है?

 उ2: हां, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q3: मुझे जावा के लिए Aspose.CAD के लिए समर्थन कहां मिल सकता है?

 A3: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) समुदाय से सहायता के लिए.

### Q4: मैं जावा के लिए Aspose.CAD का लाइसेंस कैसे खरीद सकता हूं?

 A4: आप लाइसेंस खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### Q5: जावा के लिए Aspose.CAD किन इकाइयों का समर्थन करता है?

A5: Java के लिए Aspose.CAD मीट्रिक और इंपीरियल दोनों इकाइयों का समर्थन करता है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
