---
title: जावा के लिए Aspose.CAD का उपयोग करके CAD लेयर को रैस्टर इमेज फॉर्मेट में बदलें
linktitle: CAD लेयर को रैस्टर इमेज फॉर्मेट में बदलें
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD के साथ आसानी से CAD परतों को रेखापुंज छवियों में परिवर्तित करना सीखें। निर्बाध दस्तावेज़ विज़ुअलाइज़ेशन के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 11
url: /hi/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
---
## परिचय

कंप्यूटर-एडेड डिज़ाइन (सीएडी) के दायरे में, सीएडी परतों को रेखापुंज छवि प्रारूपों में निर्बाध रूप से परिवर्तित करने की क्षमता दस्तावेज़ हेरफेर और विज़ुअलाइज़ेशन का एक महत्वपूर्ण पहलू है। जावा के लिए Aspose.CAD एक शक्तिशाली उपकरण के रूप में उभरता है, जो इस रूपांतरण प्रक्रिया को सुव्यवस्थित करने के लिए असंख्य कार्यक्षमताओं की पेशकश करता है। यह चरण-दर-चरण मार्गदर्शिका आपको प्रक्रिया के बारे में बताएगी, यह सुनिश्चित करते हुए कि आप जावा के लिए Aspose.CAD की पूरी क्षमता का उपयोग करें।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- जावा विकास वातावरण: सुनिश्चित करें कि आपकी मशीन पर जावा विकास वातावरण स्थापित है।

-  Aspose.CAD लाइब्रेरी: जावा के लिए Aspose.CAD लाइब्रेरी को डाउनलोड और इंस्टॉल करें[लिंक को डाउनलोड करें](https://releases.aspose.com/cad/java/).

## नामस्थान आयात करें

इस चरण में, हम प्रक्रिया को शुरू करने के लिए आवश्यक नामस्थान आयात करेंगे।

### Aspose.CAD कक्षाएं आयात करें

अपने जावा कोड में, निम्नलिखित आयात विवरणों का उपयोग करके Aspose.CAD कक्षाएं शामिल करें:

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## CAD लेयर को रैस्टर इमेज फॉर्मेट में बदलें

अब, आइए निर्बाध रूपांतरण प्रक्रिया सुनिश्चित करने के लिए ट्यूटोरियल को कई चरणों में विभाजित करें।

### चरण 1: सीएडी फ़ाइल सेट करें

अपनी CAD फ़ाइल का पथ निर्दिष्ट करके और इसे छवि वर्ग के उदाहरण में लोड करके प्रारंभ करें।

```java
// संसाधन निर्देशिका का पथ.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### चरण 2: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

रैस्टराइजेशन के लिए सेटिंग्स को परिभाषित करने के लिए कैडरास्टराइजेशनऑप्शंस का एक उदाहरण बनाएं।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### चरण 3: CAD परतें निर्दिष्ट करें

रैस्टराइज़ेशन विकल्पों में वांछित CAD परत जोड़ें।

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### चरण 4: JPEG विकल्प सेट करें

JpegOptions (या रेखापुंज प्रारूपों के लिए कोई ImageOptions) का एक उदाहरण बनाएं और इसे CadRasterizationOptions से लिंक करें।

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### चरण 5: JPEG में निर्यात करें

अंत में, प्रत्येक परत को JPEG प्रारूप में निर्यात करें।

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

अतिरिक्त परतों के लिए इन चरणों को दोहराएं या अपनी आवश्यकताओं के अनुसार सेटिंग्स को अनुकूलित करें।

## निष्कर्ष

इस व्यापक मार्गदर्शिका का पालन करके, आपने CAD परतों को रेखापुंज छवि प्रारूपों में परिवर्तित करने के लिए जावा के लिए Aspose.CAD की क्षमताओं का सफलतापूर्वक उपयोग किया है। यह टूल आपको दस्तावेज़ विज़ुअलाइज़ेशन और हेरफेर को आसानी से बढ़ाने का अधिकार देता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य प्रोग्रामिंग भाषाओं के साथ जावा के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: Aspose.CAD मुख्य रूप से Java का समर्थन करता है, लेकिन .NET जैसी अन्य भाषाओं के लिए भी संस्करण उपलब्ध हैं।

### Q2: मुझे अतिरिक्त सहायता या सहायता कहां मिल सकती है?

 A2: किसी भी प्रश्न या सहायता के लिए, पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19).

### Q3: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ3: हां, आप नि:शुल्क परीक्षण प्राप्त करके Aspose.CAD का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A4: से एक अस्थायी लाइसेंस प्राप्त करें[इस लिंक](https://purchase.aspose.com/temporary-license/).

### Q5: क्या जावा के लिए Aspose.CAD के लिए कोई विशिष्ट सिस्टम आवश्यकताएँ हैं?

A5: सुनिश्चित करें कि आपके पास एक संगत जावा विकास वातावरण है; विस्तृत आवश्यकताओं के लिए दस्तावेज़ देखें।