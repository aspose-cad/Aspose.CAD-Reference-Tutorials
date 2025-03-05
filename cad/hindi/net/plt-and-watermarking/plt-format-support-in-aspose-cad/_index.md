---
title: Aspose.CAD में PLT प्रारूप समर्थन - एक व्यापक ट्यूटोरियल
linktitle: Aspose.CAD में PLT प्रारूप समर्थन - ट्यूटोरियल
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD में निर्बाध PLT प्रारूप समर्थन खोजें। अपने .NET अनुप्रयोगों में PLT फ़ाइलों को सहजता से एकीकृत करने के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 10
url: /hi/net/plt-and-watermarking/plt-format-support-in-aspose-cad/
---
## परिचय

.NET के लिए Aspose.CAD में PLT प्रारूप समर्थन पर हमारे गहन ट्यूटोरियल में आपका स्वागत है! यदि आप एक डेवलपर हैं और PLT फ़ाइलों के साथ काम करना चाहते हैं और Aspose.CAD की शक्ति का उपयोग करना चाहते हैं, तो आप सही जगह पर हैं। इस गाइड में, हम आपको आवश्यक चरणों, पूर्वापेक्षाओं के बारे में बताएंगे, और यह सुनिश्चित करने के लिए विस्तृत उदाहरण प्रदान करेंगे कि आप अपने .NET अनुप्रयोगों में पीएलटी समर्थन को निर्बाध रूप से एकीकृत कर सकें।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
-  .NET के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास Aspose.CAD लाइब्रेरी स्थापित है। यदि नहीं, तो आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).
- विकास परिवेश: आवश्यक उपकरणों के साथ अपना .NET विकास परिवेश स्थापित करें।
अब जब आपने सब कुछ सेट कर लिया है तो चलिए शुरू करते हैं!

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, आवश्यक नामस्थान आयात करके प्रारंभ करें। Aspose.CAD कार्यक्षमता तक पहुँचने के लिए यह चरण महत्वपूर्ण है।
```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## चरण 1: अपना प्रोजेक्ट सेट करें

अपने पसंदीदा विकास परिवेश में एक नया .NET प्रोजेक्ट बनाकर प्रारंभ करें।

## चरण 2: Aspose.CAD संदर्भ जोड़ें

 अपने प्रोजेक्ट में Aspose.CAD लाइब्रेरी का संदर्भ लें। आप इसे NuGet पैकेज मैनेजर का उपयोग करके या लाइब्रेरी डाउनलोड करके कर सकते हैं[Aspose वेबसाइट](https://purchase.aspose.com/buy).

## चरण 3: Aspose.CAD नेमस्पेस शामिल करें

अपनी कोड फ़ाइल की शुरुआत में आवश्यक Aspose.CAD नामस्थान शामिल करें, जैसा कि ऊपर "नामस्थान आयात करें" अनुभाग में दिखाया गया है।

## चरण 4: पीएलटी फ़ाइल लोड करें

 अपनी पीएलटी फ़ाइल का पथ निर्दिष्ट करें और इसका उपयोग करके इसे लोड करें`Image.Load` तरीका।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "themepark.plt";
Image image = Image.Load((sourceFilePath));
```

## चरण 5: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

पीएलटी फ़ाइल के लिए रैस्टराइज़ेशन विकल्पों को परिभाषित करें, जैसे पृष्ठ की ऊँचाई, पृष्ठ की चौड़ाई, आदि।

```csharp
ImageOptionsBase imageOptions = new JpegOptions();
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 500,
    PageWidth = 1000,
};
imageOptions.VectorRasterizationOptions = options;
```

## चरण 6: JPEG के रूप में सहेजें

रैस्टराइज़्ड PLT फ़ाइल को JPEG छवि के रूप में सहेजें।

```csharp
image.Save((MyDir+"themepark.jpg"), imageOptions);
```

## चरण 7: अंतिम कोड

सुनिश्चित करें कि आपका कोड ऊपर "ट्यूटोरियल" अनुभाग में दिए गए उदाहरण जैसा दिखता है। यह पीएलटी प्रारूप समर्थन के लिए एक संपूर्ण कोड स्निपेट है।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "themepark.plt";
Image image = Image.Load((sourceFilePath));
ImageOptionsBase imageOptions = new JpegOptions();
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 500,
    PageWidth = 1000,
};
imageOptions.VectorRasterizationOptions = options;
image.Save((MyDir+"themepark.jpg"), imageOptions);
```

बधाई हो! आपने .NET के लिए Aspose.CAD का उपयोग करके PLT प्रारूप समर्थन को सफलतापूर्वक एकीकृत कर लिया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने .NET के लिए Aspose.CAD का उपयोग करके PLT फ़ाइलों के साथ काम करने के लिए आवश्यक चरणों को कवर किया है। इन चरणों का पालन करके, आप अपने .NET अनुप्रयोगों को मजबूत PLT प्रारूप समर्थन के साथ बढ़ा सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD अन्य CAD प्रारूपों के साथ संगत है?

A1: हां, Aspose.CAD बहुमुखी एकीकरण संभावनाएं प्रदान करते हुए, CAD प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### Q2: क्या मैं विभिन्न आउटपुट स्वरूपों के लिए रैस्टराइज़ेशन विकल्पों को अनुकूलित कर सकता हूँ?

ए2: बिल्कुल! जैसा कि ट्यूटोरियल में दिखाया गया है, आप अपनी विशिष्ट आवश्यकताओं के आधार पर रैस्टराइज़ेशन विकल्पों को तैयार कर सकते हैं।

### Q3: मुझे अतिरिक्त सहायता या सामुदायिक चर्चाएँ कहाँ मिल सकती हैं?

 A3: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) समर्थन और सामुदायिक बातचीत के लिए।

### Q4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ4: हां, आप निःशुल्क परीक्षण का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/) Aspose.CAD की क्षमताओं का अनुभव करने के लिए।

### Q5: मैं अस्थायी लाइसेंस कैसे प्राप्त करूं?

 A5: अस्थायी लाइसेंस के लिए, यहां जाएं[इस लिंक](https://purchase.aspose.com/temporary-license/).