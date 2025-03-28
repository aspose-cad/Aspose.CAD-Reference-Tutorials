---
title: सीएडी ड्रॉइंग में निःशुल्क दृष्टिकोण - Aspose.CAD गाइड
linktitle: सीएडी ड्रॉइंग में निःशुल्क दृष्टिकोण
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD के साथ CAD विज़ुअलाइज़ेशन की स्वतंत्रता का अन्वेषण करें। अद्वितीय दृष्टिकोण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 11
url: /hi/net/advanced-cad-techniques/free-point-of-view-in-cad-drawings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# सीएडी ड्रॉइंग में निःशुल्क दृष्टिकोण - Aspose.CAD गाइड

कंप्यूटर-एडेड डिज़ाइन (सीएडी) के क्षेत्र में, चित्रों में स्वतंत्र दृष्टिकोण प्राप्त करना जटिल डिज़ाइनों को देखने और प्रस्तुत करने का एक महत्वपूर्ण पहलू है। .NET के लिए Aspose.CAD इस स्वतंत्रता को प्राप्त करने के लिए एक मजबूत समाधान प्रदान करता है, जिससे उपयोगकर्ता आसानी से CAD चित्रों में हेरफेर और अनुकूलन कर सकते हैं। इस चरण-दर-चरण मार्गदर्शिका में, हम .NET के लिए Aspose.CAD का उपयोग करके CAD ड्राइंग में एक निःशुल्क दृष्टिकोण प्राप्त करने की प्रक्रिया का पता लगाएंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1. Aspose.CAD इंस्टालेशन
 सुनिश्चित करें कि आपके विकास परिवेश में .NET के लिए Aspose.CAD स्थापित है। यदि नहीं, तो आप इसे यहां से डाउनलोड कर सकते हैं[Aspose.CAD वेबसाइट](https://releases.aspose.com/cad/net/).

2. सीएडी ड्राइंग फ़ाइल
एक CAD ड्राइंग फ़ाइल तैयार करें जिसमें आप हेरफेर करना चाहते हैं। इस गाइड के लिए, हम "conic_pyramid.dxf" नामक एक नमूना फ़ाइल का उपयोग करेंगे।

3. विकास पर्यावरण
विजुअल स्टूडियो या किसी पसंदीदा आईडीई के साथ एक कार्यशील .NET विकास वातावरण स्थापित करें।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.CAD कार्यक्षमता के लिए आवश्यक नामस्थान आयात करें। अपनी फ़ाइल के शीर्ष पर निम्नलिखित कोड स्निपेट जोड़ें:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```


## चरण 1: दस्तावेज़ निर्देशिका को परिभाषित करें

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string MyDir = "Your Document Directory";
```

"आपकी दस्तावेज़ निर्देशिका" को अपनी दस्तावेज़ निर्देशिका के वास्तविक पथ से बदलना सुनिश्चित करें।

## चरण 2: स्रोत फ़ाइल निर्दिष्ट करें

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

अपनी CAD ड्राइंग फ़ाइल को पथ प्रदान करें।

## चरण 3: आउटपुट पथ सेट करें

```csharp
var outPath = Path.Combine(MyDir, "FreePointOfView_out.jpg");
```

उस पथ को परिभाषित करें जहां हेरफेर की गई CAD ड्राइंग सहेजी जाएगी।

## चरण 4: CAD छवि लोड करें

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
```

Aspose.CAD का उपयोग करके CAD ड्राइंग लोड करें।

## चरण 5: JPEG विकल्प कॉन्फ़िगर करें

```csharp
JpegOptions options = new JpegOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500, PageHeight = 1500
    }
};
```

CAD ड्राइंग को JPEG प्रारूप में निर्यात करने के लिए विकल्पों को कॉन्फ़िगर करें।

## चरण 6: घूर्णन कोण सेट करें

```csharp
float xAngle = 10; //एक्स अक्ष के अनुदिश घूर्णन का कोण
float yAngle = 30; //Y अक्ष के अनुदिश घूर्णन का कोण
float zAngle = 40; //Z अक्ष के अनुदिश घूर्णन का कोण
((CadRasterizationOptions)(options.VectorRasterizationOptions)).ObserverPoint = new ObserverPoint(xAngle, yAngle, zAngle);
```

वांछित दृष्टिकोण प्राप्त करने के लिए एक्स, वाई और जेड अक्षों के साथ घूर्णन कोण निर्दिष्ट करें।

## चरण 7: हेरफेर की गई सीएडी ड्राइंग को सहेजें

```csharp
cadImage.Save(outPath, options);
}
```

हेरफेर किए गए CAD ड्राइंग को निर्दिष्ट आउटपुट पथ पर सहेजें।

## चरण 8: सफलता संदेश प्रदर्शित करें

```csharp
Console.WriteLine("\n3D images exported successfully to JPEG.\nFile saved at " + outPath);
```

उपयोगकर्ता को 3डी छवि के सफल निर्यात के बारे में सूचित करें।

## निष्कर्ष

इस ट्यूटोरियल में, हमने .NET के लिए Aspose.CAD का उपयोग करके CAD ड्राइंग में एक स्वतंत्र दृष्टिकोण प्राप्त करने की प्रक्रिया का पता लगाया है। इन चरण-दर-चरण निर्देशों का पालन करके, आप अपनी सीएडी विज़ुअलाइज़ेशन क्षमताओं को बढ़ा सकते हैं और अपने डिज़ाइन को एक नए दृष्टिकोण के साथ प्रस्तुत कर सकते हैं।


## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य CAD फ़ाइल स्वरूपों के साथ .NET के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: हाँ, .NET के लिए Aspose.CAD DWG और DXF सहित विभिन्न CAD फ़ाइल स्वरूपों का समर्थन करता है।

### Q2: क्या Aspose.CAD का कोई परीक्षण संस्करण उपलब्ध है?

 उ2: हां, आप यहां से नि:शुल्क परीक्षण संस्करण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A3: आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q4: मुझे Aspose.CAD के लिए अतिरिक्त सहायता कहां मिल सकती है?

 A4: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और चर्चा के लिए।

### Q5: क्या मैं विभिन्न छवि प्रारूपों के लिए निर्यात विकल्पों को अनुकूलित कर सकता हूँ?

ए5: निश्चित रूप से! Aspose.CAD अनुकूलन के लिए विकल्पों की एक श्रृंखला प्रदान करता है, जिससे आप निर्यात प्रक्रिया को अपनी विशिष्ट आवश्यकताओं के अनुरूप बना सकते हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
