---
title: जावा के लिए Aspose.CAD के साथ निःशुल्क पॉइंट ऑफ़ व्यू रेंडरिंग
linktitle: निःशुल्क दृष्टिकोण
second_title: Aspose.CAD जावा एपीआई
description: CAD ड्राइंग के लिए निःशुल्क पॉइंट ऑफ़ व्यू रेंडरिंग प्राप्त करने के लिए इस ट्यूटोरियल में Java के लिए Aspose.CAD की शक्ति का अन्वेषण करें। Aspose.CAD की क्षमता को उजागर करें।
weight: 14
url: /hi/java/other-cad-operations/free-point-of-view/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के लिए Aspose.CAD के साथ निःशुल्क पॉइंट ऑफ़ व्यू रेंडरिंग

## परिचय

"फ्री पॉइंट ऑफ़ व्यू - जावा ट्यूटोरियल के लिए Aspose.CAD" में आपका स्वागत है। इस व्यापक मार्गदर्शिका में, हम आपको CAD चित्रों के लिए निःशुल्क दृष्टिकोण प्रतिपादन प्राप्त करने के लिए जावा के लिए Aspose.CAD का लाभ उठाने की प्रक्रिया के बारे में बताएंगे। Aspose.CAD एक शक्तिशाली जावा लाइब्रेरी है जो कंप्यूटर-एडेड डिज़ाइन (CAD) फ़ाइलों के साथ काम करने के लिए कई प्रकार की सुविधाएँ प्रदान करती है। ट्यूटोरियल में आवश्यक शर्तें, आवश्यक पैकेज आयात करना और प्रत्येक उदाहरण को चरण-दर-चरण मार्गदर्शिकाओं में विभाजित करना शामिल होगा।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
-  जावा लाइब्रेरी के लिए Aspose.CAD: जावा लाइब्रेरी के लिए Aspose.CAD को यहां से डाउनलोड और इंस्टॉल करें[लिंक को डाउनलोड करें](https://releases.aspose.com/cad/java/).
- जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपकी मशीन पर जावा स्थापित है।

## पैकेज आयात करें

आरंभ करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करें। अपनी जावा फ़ाइल की शुरुआत में कोड की निम्नलिखित पंक्तियाँ जोड़ें:
```java
import com.aspose.cad.fileformats.ObserverPoint;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.ObserverPoint;
```

ये पैकेज CAD फ़ाइलों के साथ काम करने और रेंडरिंग विकल्पों को अनुकूलित करने के लिए आवश्यक हैं।

अब, आइए दिए गए उदाहरण को कई चरणों में तोड़ें:

## चरण 1: अपनी दस्तावेज़ निर्देशिका सेट करें

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

"आपकी दस्तावेज़ निर्देशिका" को अपनी वास्तविक दस्तावेज़ निर्देशिका के पथ से बदलें।

## चरण 2: सीएडी ड्राइंग लोड करें

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(sourceFilePath);
```

अपने CAD ड्राइंग के लिए पथ निर्दिष्ट करें, और इसका उपयोग करके इसे लोड करें`Image` कक्षा।

## चरण 3: CAD रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
cadRasterizationOptions.setPageHeight(1500);
cadRasterizationOptions.setPageWidth(1500);
```

अपनी आवश्यकताओं, जैसे पृष्ठ की ऊंचाई और चौड़ाई के अनुसार सीएडी रेखापुंज विकल्पों को अनुकूलित करें।

## चरण 4: JpegOptions सेट करें

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(cadRasterizationOptions);
```

 का एक उदाहरण बनाएं`JpegOptions` और इसे पहले से कॉन्फ़िगर किए गए रैस्टराइज़ेशन विकल्पों के साथ संबद्ध करें।

## चरण 5: घूर्णन कोणों को परिभाषित करें

```java
float xAngle = 10;
float yAngle = 30;
float zAngle = 40;
ObserverPoint obvPoint = new ObserverPoint(xAngle, yAngle, zAngle);
cadRasterizationOptions.setObserverPoint(obvPoint);
```

मुक्त बिंदु दृश्य प्रतिपादन के लिए एक्स, वाई और जेड अक्षों के साथ घूर्णन कोण निर्दिष्ट करें।

## चरण 6: प्रस्तुत छवि को सहेजें

```java
objImage.save(dataDir + "FreePointOfView_out.jpeg", options);
```

निर्दिष्ट विकल्पों के साथ प्रदान की गई छवि को वांछित स्थान पर सहेजें।

अपने विशिष्ट उपयोग के मामले के लिए इन चरणों को दोहराएं, जिससे आपके सीएडी चित्रों के लिए एक स्वतंत्र दृष्टिकोण प्रतिपादन सुनिश्चित हो सके।

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.CAD का उपयोग करके निःशुल्क पॉइंट ऑफ़ व्यू रेंडरिंग को कार्यान्वित करने का तरीका सफलतापूर्वक सीख लिया है। इस ट्यूटोरियल में पूर्वापेक्षाएँ सेट करने से लेकर रेंडरिंग विकल्पों को अनुकूलित करने और आउटपुट छवि को सहेजने तक आवश्यक कदम शामिल हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं कई प्लेटफ़ॉर्म पर Java के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: हाँ, Java के लिए Aspose.CAD प्लेटफ़ॉर्म-स्वतंत्र है और इसका उपयोग विभिन्न ऑपरेटिंग सिस्टम पर किया जा सकता है।

### Q2: क्या जावा के लिए Aspose.CAD के लिए कोई लाइसेंसिंग विकल्प हैं?

 उ2: हां, आप लाइसेंसिंग विकल्प तलाश सकते हैं और खरीदारी कर सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### Q3: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ3: हां, आप निःशुल्क परीक्षण संस्करण तक पहुंच सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मुझे जावा के लिए Aspose.CAD के लिए समर्थन कहां मिल सकता है?

 A4: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और चर्चा के लिए।

### Q5: मैं अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A5: एक अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
