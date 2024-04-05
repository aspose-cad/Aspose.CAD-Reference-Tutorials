---
title: जावा के लिए Aspose.CAD का उपयोग करके पृष्ठभूमि और ड्राइंग रंग सेट करना
linktitle: पृष्ठभूमि और ड्राइंग रंग सेट करना
second_title: Aspose.CAD जावा एपीआई
description: Java के लिए Aspose.CAD का उपयोग करके आसानी से CAD फ़ाइलों को PDF और TIFF में बदलें। दृश्यमान आश्चर्यजनक परिणामों के लिए कस्टम पृष्ठभूमि और ड्राइंग रंग सेट करें।
type: docs
weight: 15
url: /hi/java/advanced-cad-features/setting-background-and-drawing-color/
---
## परिचय

कंप्यूटर-एडेड डिज़ाइन (सीएडी) की गतिशील दुनिया में, निर्बाध सहयोग और संचार के लिए कुशल फ़ाइल रूपांतरण महत्वपूर्ण है। जावा के लिए Aspose.CAD एक शक्तिशाली उपकरण के रूप में उभरा है, जो CAD फ़ाइलों को पीडीएफ और टीआईएफएफ प्रारूपों में परिवर्तित करने के लिए मजबूत क्षमताएं प्रदान करता है। इस ट्यूटोरियल में, हम जावा के लिए Aspose.CAD का उपयोग करके पृष्ठभूमि सेट करने और रंग खींचने की प्रक्रिया में गहराई से उतरेंगे, जो आपको इष्टतम परिणामों के लिए चरण-दर-चरण मार्गदर्शिका प्रदान करेगा।

## आवश्यक शर्तें

इससे पहले कि हम इस यात्रा पर निकलें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

-  जावा लाइब्रेरी के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास जावा लाइब्रेरी के लिए Aspose.CAD स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/java/).

-  दस्तावेज़ निर्देशिका: अपनी CAD फ़ाइलों के लिए एक समर्पित निर्देशिका रखें। प्रतिस्थापित करें`"Your Document Directory" + "CADConversion/"` आपकी निर्देशिका के पथ के साथ।

अब, आइए इस प्रक्रिया में गहराई से उतरें।

## नामस्थान आयात करें

सुनिश्चित करें कि आप Java के लिए Aspose.CAD की कार्यक्षमताओं का लाभ उठाने के लिए आवश्यक नामस्थान आयात करें। हमारे उदाहरण में, हम निम्नलिखित का उपयोग करते हैं:

```java
import java.awt.Color;
import java.awt.Image;

import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## चरण 1: CAD फ़ाइल लोड करें

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(srcFile);
```

## चरण 2: पृष्ठभूमि और ड्राइंग रंग सेट करें

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBeige());
rasterizationOptions.setDrawType(CadDrawTypeMode.UseDrawColor);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBlue());
```

## चरण 3: पीडीएफ बनाएं और सेव करें

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

## चरण 4: TIFF बनाएं और सहेजें

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

जावा के लिए Aspose.CAD का उपयोग करके CAD से PDF और TIFF रूपांतरण में इष्टतम परिणाम प्राप्त करने के लिए इन चरणों का परिश्रमपूर्वक पालन करें।

## निष्कर्ष

जावा के लिए Aspose.CAD डेवलपर्स को CAD फ़ाइल हेरफेर के लिए एक बहुमुखी टूलसेट के साथ सशक्त बनाता है। पृष्ठभूमि सेट करने और रंग खींचने की जटिलताओं में महारत हासिल करके, आप दिखने में आकर्षक और सटीक रूपांतरण उत्पन्न करने की अपनी क्षमता बढ़ाते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या जावा के लिए Aspose.CAD थोक रूपांतरणों के लिए उपयुक्त है?

A1: बिल्कुल! जावा के लिए Aspose.CAD बड़े पैमाने पर रूपांतरणों में उत्कृष्टता प्रदान करता है, दक्षता और सटीकता प्रदान करता है।

### Q2: क्या मैं जेनरेट की गई फ़ाइलों में पृष्ठभूमि रंग को अनुकूलित कर सकता हूँ?

उ2: हां, ट्यूटोरियल दर्शाता है कि पीडीएफ और टीआईएफएफ आउटपुट दोनों के लिए कस्टम पृष्ठभूमि रंग कैसे सेट करें।

### Q3: मैं जावा के लिए Aspose.CAD के लिए व्यापक दस्तावेज़ कहां पा सकता हूं?

 A3: का संदर्भ लें[प्रलेखन](https://reference.aspose.com/cad/java/) गहन अंतर्दृष्टि और उदाहरणों के लिए।

### Q4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 A4: हां, इसके साथ सुविधाओं का अन्वेषण करें[मुफ्त परीक्षण](https://releases.aspose.com/).

### Q5: मैं जावा के लिए Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

A5: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सहायता प्राप्त करना और समुदाय के साथ जुड़ना।
