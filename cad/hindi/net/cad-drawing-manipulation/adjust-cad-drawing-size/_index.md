---
title: .NET के लिए Aspose.CAD में CAD ड्राइंग आकार समायोजित करना
linktitle: सीएडी ड्राइंग आकार समायोजित करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: Aspose.CAD का उपयोग करके .NET में CAD ड्राइंग आकार को आसानी से समायोजित करना सीखें। निर्बाध आकार बदलने के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 10
url: /hi/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.CAD में CAD ड्राइंग आकार समायोजित करना

## परिचय

क्या आप अपने .NET अनुप्रयोगों में CAD ड्राइंग के आकार को सहजता से समायोजित करना चाहते हैं? .NET के लिए Aspose.CAD एक मजबूत समाधान प्रदान करता है, जो आपको CAD ड्राइंग के आकार को आसानी से संभालने की अनुमति देता है। इस ट्यूटोरियल में, हम आपको प्रक्रिया के माध्यम से मार्गदर्शन करेंगे, प्रत्येक चरण को तोड़कर यह सुनिश्चित करेंगे कि आप Aspose.CAD का उपयोग करके CAD चित्रों के आकार बदलने की जटिलताओं को समझ सकें।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- .NET लाइब्रेरी के लिए Aspose.CAD: लाइब्रेरी को डाउनलोड और इंस्टॉल करें[.NET डाउनलोड पेज के लिए Aspose.CAD](https://releases.aspose.com/cad/net/).
- नमूना CAD ड्राइंग: सुनिश्चित करें कि आपके दस्तावेज़ निर्देशिका में एक नमूना CAD ड्राइंग फ़ाइल (उदाहरण के लिए, "sample.dwg") है।

## नामस्थान आयात करें

अपने .NET एप्लिकेशन में आवश्यक नामस्थान आयात करके प्रारंभ करें। .NET के लिए Aspose.CAD द्वारा प्रदान की गई कार्यक्षमताओं तक पहुँचने के लिए यह चरण महत्वपूर्ण है।

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## चरण 1: सीएडी ड्राइंग लोड करें

CAD ड्राइंग को Aspose.CAD.Image वर्ग के एक उदाहरण में लोड करके प्रारंभ करें। सुनिश्चित करें कि आपके पास अपने नमूना ड्राइंग के लिए सही फ़ाइल पथ है।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// छवि के एक उदाहरण में CAD ड्राइंग लोड करें
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // आपका कोड यहां...
}
```

## चरण 2: BmpOptions बनाएं

BmpOptions वर्ग का एक उदाहरण बनाएं, जो CAD ड्राइंग को BMP फ़ाइल के रूप में सहेजते समय विकल्प निर्दिष्ट करने के लिए ज़िम्मेदार है।

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## चरण 3: कैडरास्टराइज़ेशन विकल्प सेट करें

CadRasterizationOptions क्लास को इंस्टेंट करें और वेक्टर रैस्टराइजेशन के लिए इसके गुणों को कॉन्फ़िगर करें।

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## चरण 4: यूनिटटाइप प्रॉपर्टी सेट करें

आकार बदलने के लिए इकाई प्रकार निर्दिष्ट करने के लिए CadRasterizationOptions की UnitType संपत्ति सेट करें। इस उदाहरण में, इसे सेंटीमीटर पर सेट किया गया है।

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## चरण 5: लेआउट प्रॉपर्टी सेट करें

लेआउट प्रॉपर्टी सेट करके उन लेआउट को निर्दिष्ट करें जिन्हें आप संशोधित ड्राइंग में शामिल करना चाहते हैं।

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## चरण 6: बीएमपी को निर्यात करें

अंत में, सेव विधि का उपयोग करके संशोधित लेआउट को बीएमपी फ़ाइल के रूप में सहेजें।

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

अब आपने .NET के लिए Aspose.CAD का उपयोग करके अपने CAD ड्राइंग के आकार को सफलतापूर्वक समायोजित कर लिया है!

## निष्कर्ष

इस ट्यूटोरियल में, हमने Aspose.CAD का उपयोग करके .NET में CAD चित्रों का आकार बदलने की प्रक्रिया के बारे में जाना। इन चरणों का पालन करके, आप इस कार्यक्षमता को अपने एप्लिकेशन में सहजता से एकीकृत कर सकते हैं, जिससे एक सहज उपयोगकर्ता अनुभव प्राप्त होगा।

## पूछे जाने वाले प्रश्न

### Q1: क्या .NET के लिए Aspose.CAD सभी CAD प्रारूपों के साथ संगत है?

 A1: .NET के लिए Aspose.CAD DWG, DXF, DWF और अन्य सहित CAD प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है। जाँचें[प्रलेखन](https://reference.aspose.com/cad/net/) पूरी सूची के लिए.

### Q2: क्या मैं एक साथ कई लेआउट का आकार बदल सकता हूँ?

A2: हां, आप CadRasterizationOptions में लेआउट सरणी को समायोजित करके कई लेआउट का आकार बदल सकते हैं।

### Q3: मुझे .NET के लिए Aspose.CAD के लिए समर्थन कहां मिल सकता है?

 A3: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और सहायता के लिए।

### Q4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 ए4: हां, आप एक्सप्लोर कर सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/) .NET के लिए Aspose.CAD की विशेषताओं का मूल्यांकन करने के लिए।

### Q5: मैं .NET के लिए Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A5: परीक्षण उद्देश्यों के लिए एक अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
