---
title: जावा में Aspose.CAD का उपयोग करके DXF को WMF प्रारूप में निर्यात करें
linktitle: जावा का उपयोग करके DXF को WMF प्रारूप में निर्यात करें
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD की शक्ति को अनलॉक करें। हमारे विस्तृत ट्यूटोरियल से जानें कि डीएक्सएफ ड्राइंग को आसानी से डब्लूएमएफ प्रारूप में कैसे निर्यात किया जाए। लाइब्रेरी डाउनलोड करें, हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें, और अपनी CAD फ़ाइल प्रबंधन को उन्नत करें।
weight: 14
url: /hi/java/additional-features/export-dxf-to-wmf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा में Aspose.CAD का उपयोग करके DXF को WMF प्रारूप में निर्यात करें

## परिचय

DXF ड्राइंग को WMF प्रारूप में निर्यात करने के लिए जावा के लिए Aspose.CAD का उपयोग करने पर हमारी चरण-दर-चरण मार्गदर्शिका में आपका स्वागत है। Aspose.CAD एक शक्तिशाली जावा लाइब्रेरी है जो CAD फ़ाइलों के साथ काम करने के लिए व्यापक क्षमताएं प्रदान करती है। इस ट्यूटोरियल में, हम आपको Aspose.CAD का उपयोग करके DXF फ़ाइलों को WMF प्रारूप में परिवर्तित करने की प्रक्रिया के बारे में बताएंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  जावा के लिए Aspose.CAD: सुनिश्चित करें कि आपके जावा प्रोजेक्ट में Aspose.CAD लाइब्रेरी एकीकृत है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/java/).

- दस्तावेज़ निर्देशिका: एक दस्तावेज़ निर्देशिका स्थापित करें जहाँ आपके DXF चित्र संग्रहीत हैं।

## नामस्थान आयात करें

अपने जावा प्रोजेक्ट में, Aspose.CAD द्वारा प्रदान की गई कार्यक्षमताओं तक पहुँचने के लिए आवश्यक नामस्थान आयात करें:

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

## चरण 1: डीएक्सएफ ड्राइंग लोड करें

उस DXF ड्राइंग को लोड करें जिसे आप WMF प्रारूप में निर्यात करना चाहते हैं। सुनिश्चित करें कि DXF फ़ाइल का पथ सही ढंग से निर्दिष्ट है।

```java
// संसाधन निर्देशिका का पथ.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## चरण 2: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

आउटपुट पेज की चौड़ाई और ऊंचाई को परिभाषित करने के लिए रैस्टराइज़ेशन विकल्पों को कॉन्फ़िगर करें। इस उदाहरण में, हम पृष्ठ की चौड़ाई और ऊंचाई 100 इकाइयों पर सेट करते हैं।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

## चरण 3: WMF के रूप में सहेजें

कॉन्फ़िगर किए गए विकल्पों का उपयोग करके लोड की गई DXF ड्राइंग को WMF प्रारूप के रूप में सहेजें।

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

## चरण 4: संसाधनों का निपटान

मेमोरी खाली करने और कुशल संसाधन प्रबंधन सुनिश्चित करने के लिए संसाधनों का निपटान करें।

```java
finally
{
  cadImage.dispose();
}
```

## चरण 5: पीडीएफ में निर्यात करें

वैकल्पिक रूप से, Aspose.CAD का उपयोग करके DXF ड्राइंग को पीडीएफ प्रारूप में निर्यात करें।

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

बधाई हो! आपने जावा के लिए Aspose.CAD का उपयोग करके DXF ड्राइंग को WMF प्रारूप में सफलतापूर्वक निर्यात किया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने DXF ड्राइंग को WMF प्रारूप में निर्यात करने के लिए जावा के लिए Aspose.CAD का उपयोग करने की प्रक्रिया का पता लगाया। अपनी व्यापक सुविधाओं और उपयोग में आसानी के साथ, Aspose.CAD जावा परियोजनाओं में CAD फ़ाइलों के साथ काम करने के लिए एक विश्वसनीय समाधान प्रदान करता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: मुझे Aspose.CAD दस्तावेज़ कहां मिल सकता है?

 A1: आप दस्तावेज़ तक पहुंच सकते हैं[यहाँ](https://reference.aspose.com/cad/java/).

### Q2: मैं जावा के लिए Aspose.CAD कैसे डाउनलोड करूं?

 A2: लाइब्रेरी डाउनलोड करें[यहाँ](https://releases.aspose.com/cad/java/).

### Q3: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

उ3: हाँ, आप निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: अस्थायी लाइसेंसिंग विकल्पों की आवश्यकता है?

 A4: अस्थायी लाइसेंस का अन्वेषण करें[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: मुझे सहायता कहाँ से मिल सकती है?

 A5: Aspose.CAD सहायता फ़ोरम पर जाएँ[यहाँ](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
