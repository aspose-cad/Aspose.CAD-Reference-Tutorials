---
title: बीएमपी प्रारूप में निर्यात करना - Aspose.CAD ट्यूटोरियल
linktitle: बीएमपी प्रारूप में निर्यात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का उपयोग करके BMP में 3D छवि निर्यात की निर्बाध दुनिया का अन्वेषण करें। परेशानी मुक्त अनुभव के लिए हमारे ट्यूटोरियल का अनुसरण करें।
type: docs
weight: 11
url: /hi/net/file-format-conversion/exporting-to-bmp-format/
---
## परिचय

सॉफ़्टवेयर विकास की गतिशील दुनिया में, .NET के लिए Aspose.CAD कंप्यूटर-एडेड डिज़ाइन (CAD) फ़ाइलों को संभालने के लिए एक शक्तिशाली उपकरण के रूप में सामने आता है। यदि आप सीएडी छवियों को व्यापक रूप से उपयोग किए जाने वाले बीएमपी प्रारूप में निर्यात करना चाहते हैं, तो यह ट्यूटोरियल आपके लिए मार्गदर्शक है। इस चरण-दर-चरण वॉकथ्रू में, हम .NET के लिए Aspose.CAD का उपयोग करके BMP में 3D छवियों को निर्यात करने की प्रक्रिया का पता लगाएंगे। आइए गोता लगाएँ!

## आवश्यक शर्तें

इससे पहले कि हम इस ट्यूटोरियल को शुरू करें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET के लिए Aspose.CAD: Aspose.CAD लाइब्रेरी को डाउनलोड और इंस्टॉल करें[यहाँ](https://releases.aspose.com/cad/net/).
- विकास परिवेश: एक .NET विकास परिवेश स्थापित करें।
- सीएडी फ़ाइल: निर्यात के लिए एक सीएडी फ़ाइल तैयार रखें। इस उदाहरण के लिए, हम "18-12-11 9644 - site.dwf" का उपयोग करेंगे।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, आवश्यक नामस्थान आयात करना सुनिश्चित करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## चरण 1: सीएडी छवि लोड करें

अपने प्रोजेक्ट में CAD छवि लोड करके शुरुआत करें। "आपकी दस्तावेज़ निर्देशिका" को वास्तविक निर्देशिका पथ से बदलें।

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    // छवि लोड करने के लिए आपका कोड यहां जाता है
}
```

## चरण 2: बीएमपी निर्यात विकल्प कॉन्फ़िगर करें

सीएडी फ़ाइलों के लिए वेक्टर रैस्टराइज़ेशन विकल्पों सहित बीएमपी निर्यात विकल्प सेट करें।

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## चरण 3: बीएमपी को निर्यात करें

बीएमपी फ़ाइल के लिए आउटपुट पथ निर्दिष्ट करते हुए, निर्यात प्रक्रिया निष्पादित करें।

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.CAD का उपयोग करके BMP में एक 3D छवि सफलतापूर्वक निर्यात कर ली है। यह ट्यूटोरियल Aspose.CAD की बहुमुखी प्रतिभा की एक झलक प्रदान करता है, जिससे जटिल कार्य आसान हो जाते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं किसी भी CAD फ़ाइल प्रारूप के साथ .NET के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: हाँ, Aspose.CAD विभिन्न CAD फ़ाइल स्वरूपों का समर्थन करता है, जो आपकी परियोजनाओं में लचीलापन प्रदान करता है।

### Q2: क्या परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस उपलब्ध है?

 ए2: निश्चित रूप से! आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/) मूल्यांकन के लिए।

### Q3: मुझे Aspose.CAD के लिए व्यापक दस्तावेज़ कहाँ मिल सकते हैं?

 A3: दस्तावेज़ देखें[यहाँ](https://reference.aspose.com/cad/net/) विस्तृत जानकारी और उदाहरणों के लिए.

### Q4: मैं समर्थन कैसे प्राप्त करूं या समुदाय से कैसे जुड़ूं?

 A4: Aspose.CAD फोरम पर जाएँ[यहाँ](https://forum.aspose.com/c/cad/19) प्रश्न पूछने और समुदाय के साथ जुड़ने के लिए।

### Q5: क्या मैं .NET के लिए Aspose.CAD खरीद सकता हूँ?

 A5: हाँ, आप Aspose.CAD खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy) अपनी परियोजनाओं के लिए इसकी पूरी क्षमता को अनलॉक करने के लिए।
