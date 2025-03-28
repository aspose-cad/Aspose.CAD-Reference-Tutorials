---
title: आईजीईएस फाइलों को पीडीएफ में निर्यात करना - Aspose.CAD गाइड
linktitle: आईजीईएस फाइलों को पीडीएफ में निर्यात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का उपयोग करके आसानी से IGES फ़ाइलों को PDF में निर्यात करना सीखें। सटीक सीएडी फ़ाइल हेरफेर के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 11
url: /hi/net/exporting-to-image-formats/exporting-iges-files-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# आईजीईएस फाइलों को पीडीएफ में निर्यात करना - Aspose.CAD गाइड

## परिचय

कंप्यूटर-एडेड डिज़ाइन (CAD) की गतिशील दुनिया में, IGES फ़ाइलों को पीडीएफ प्रारूप में परिवर्तित करने की आवश्यकता एक सामान्य आवश्यकता है। .NET के लिए Aspose.CAD इस कार्य के लिए एक शक्तिशाली समाधान प्रदान करता है, जो CAD फ़ाइलों को संभालने में लचीलापन और सटीकता प्रदान करता है। इस ट्यूटोरियल में, हम आपको .NET के लिए Aspose.CAD का उपयोग करके IGES फ़ाइलों को PDF में निर्यात करने की प्रक्रिया के बारे में बताएंगे। आइए गोता लगाएँ!

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1.  .NET लाइब्रेरी के लिए Aspose.CAD: सुनिश्चित करें कि आपके प्रोजेक्ट में .NET लाइब्रेरी के लिए Aspose.CAD एकीकृत है। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

2. विकास परिवेश: आवश्यक कॉन्फ़िगरेशन के साथ विजुअल स्टूडियो जैसा एक .NET विकास परिवेश स्थापित करें।

अब जब आपके पास पूर्वापेक्षाएँ व्यवस्थित हो गई हैं, तो आइए आवश्यक नामस्थान आयात करने के लिए आगे बढ़ें।

## नामस्थान आयात करें

अपने कोड में, निम्नलिखित नामस्थान शामिल करें:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;
```

ये नामस्थान सीएडी छवियों और रेखापुंज विकल्पों के साथ काम करने के लिए आवश्यक कक्षाएं प्रदान करते हैं।

## चरण 1: अपना प्रोजेक्ट सेट करें

कोड में गोता लगाने से पहले, एक नया प्रोजेक्ट बनाएं या अपने पसंदीदा .NET विकास परिवेश में मौजूदा प्रोजेक्ट खोलें।

## चरण 2: Aspose.CAD संदर्भ जोड़ें

अपने प्रोजेक्ट में Aspose.CAD लाइब्रेरी का संदर्भ लें। आप डाउनलोड की गई Aspose.CAD DLL फ़ाइल को जोड़कर ऐसा कर सकते हैं।

## चरण 3: पथ प्रारंभ करें

अपनी दस्तावेज़ निर्देशिका का पथ सेट करें जहां IGES फ़ाइल स्थित है:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "figa2.igs";
```

## चरण 4: सीएडी छवि लोड करें

 Aspose.CAD का उपयोग करें`Image.Load` IGES फ़ाइल लोड करने की विधि:

```csharp
using (Image cadImage = Image.Load(sourceFilePath))
{
    // आपका कोड यहां जाता है
}
```

## चरण 5: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

पीडीएफ आउटपुट को अनुकूलित करने के लिए रेखापुंज विकल्पों को परिभाषित करें:

```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1000,
    PageWidth = 1000,
};

PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```

## चरण 6: पीडीएफ के रूप में सहेजें

निर्दिष्ट विकल्पों के साथ सीएडी छवि को पीडीएफ फाइल के रूप में सहेजें:

```csharp
cadImage.Save(MyDir + "figa2.pdf", pdfOptions);
```

इन छह सीधे चरणों के साथ, आपने .NET के लिए Aspose.CAD का उपयोग करके IGES फ़ाइल को PDF में सफलतापूर्वक निर्यात कर लिया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने .NET के लिए Aspose.CAD का उपयोग करके IGES फ़ाइलों को पीडीएफ में बदलने का एक सहज तरीका खोजा है। चरण-दर-चरण मार्गदर्शिका एक सुचारू और कुशल प्रक्रिया सुनिश्चित करती है, जो आपको CAD फ़ाइलों को सटीकता से संभालने में सशक्त बनाती है।


## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं वेब एप्लिकेशन में .NET के लिए Aspose.CAD का उपयोग कर सकता हूं?

A1: हाँ, .NET के लिए Aspose.CAD डेस्कटॉप और वेब अनुप्रयोगों दोनों के लिए उपयुक्त है, जो CAD फ़ाइल हेरफेर के लिए बहुमुखी समाधान प्रदान करता है।

### Q2: मुझे Aspose.CAD के लिए अतिरिक्त दस्तावेज़ कहां मिल सकते हैं?

 A2: व्यापक दस्तावेज़ीकरण का अन्वेषण करें[यहाँ](https://reference.aspose.com/cad/net/) .NET के लिए Aspose.CAD में विस्तृत जानकारी के लिए।

### Q3: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ3: हाँ, आप निःशुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/) .NET के लिए Aspose.CAD की क्षमताओं का अनुभव करने के लिए।

### Q4: मैं अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A4: अस्थायी लाइसेंस के लिए, यहां जाएं[इस लिंक](https://purchase.aspose.com/temporary-license/) आवश्यक लाइसेंसिंग जानकारी प्राप्त करने के लिए।

### Q5: सहायता चाहिए या कोई प्रश्न हैं?

A5: Aspose.CAD समुदाय से जुड़ें[सहयता मंच](https://forum.aspose.com/c/cad/19) त्वरित सहायता और चर्चा के लिए.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
