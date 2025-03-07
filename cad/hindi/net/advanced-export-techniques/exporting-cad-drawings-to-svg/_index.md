---
title: CAD चित्र को SVG प्रारूप में निर्यात करना - Aspose.CAD गाइड
linktitle: CAD चित्र को SVG प्रारूप में निर्यात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का उपयोग करके CAD चित्रों को SVG में निर्यात करने की निर्बाध प्रक्रिया का अन्वेषण करें। लचीलेपन और अनुकूलन के साथ अपने सीएडी विकास को बढ़ाएं।
weight: 15
url: /hi/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD चित्र को SVG प्रारूप में निर्यात करना - Aspose.CAD गाइड

## परिचय

सीएडी (कंप्यूटर-एडेड डिज़ाइन) की गतिशील दुनिया में, चित्रों को विभिन्न प्रारूपों में निर्यात करने की क्षमता एक महत्वपूर्ण कौशल है। एसवीजी (स्केलेबल वेक्टर ग्राफिक्स) एक ऐसा प्रारूप है जिसने अपनी स्केलेबिलिटी और बहुमुखी प्रतिभा के कारण लोकप्रियता हासिल की है। इस ट्यूटोरियल में, हम यह पता लगाएंगे कि .NET लाइब्रेरी के लिए शक्तिशाली Aspose.CAD का उपयोग करके SVG में CAD चित्र कैसे निर्यात करें।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET लाइब्रेरी के लिए Aspose.CAD: .NET लाइब्रेरी के लिए Aspose.CAD को डाउनलोड और इंस्टॉल करें। आप पुस्तकालय पा सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

- विकास वातावरण: विजुअल स्टूडियो या किसी अन्य .NET विकास उपकरण के साथ एक उपयुक्त विकास वातावरण स्थापित करें।

## नामस्थान आयात करें

आरंभ करने के लिए, अपने प्रोजेक्ट में आवश्यक नामस्थान आयात करें:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string MyDir = "Your Document Directory";
```

## चरण 2: सीएडी ड्राइंग लोड करें

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

## चरण 3: एसवीजी निर्यात विकल्प कॉन्फ़िगर करें

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;
    options.TextAsShapes = true;
```

## चरण 4: एसवीजी फ़ाइल सहेजें

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

इन सरल चरणों का पालन करके, आप .NET के लिए Aspose.CAD का उपयोग करके CAD चित्रों को SVG में निर्बाध रूप से निर्यात कर सकते हैं। लाइब्रेरी लचीलापन और अनुकूलन विकल्प प्रदान करती है, जिससे आप अपनी आवश्यकताओं के अनुसार आउटपुट तैयार कर सकते हैं।

## निष्कर्ष

अंत में, .NET के लिए Aspose.CAD SVG को CAD चित्र निर्यात करने की प्रक्रिया को सरल बनाता है। इसकी सहज एपीआई और मजबूत विशेषताएं इसे सीएडी अनुप्रयोगों के साथ काम करने वाले डेवलपर्स के लिए एक मूल्यवान उपकरण बनाती हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD सभी CAD प्रारूपों के साथ संगत है?

A1: Aspose.CAD व्यापक अनुकूलता सुनिश्चित करते हुए DWG और DXF सहित विभिन्न CAD प्रारूपों का समर्थन करता है।

### Q2: क्या मैं एसवीजी को निर्यात करते समय रंग मोड को अनुकूलित कर सकता हूं?

A2: हाँ, Aspose.CAD आपको आउटपुट में लचीलापन प्रदान करते हुए, रंग मोड चुनने की अनुमति देता है।

### Q3: क्या अस्थायी लाइसेंस परीक्षण उद्देश्यों के लिए उपलब्ध हैं?

 उ3: हाँ, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/) मूल्यांकन के लिए।

### Q4: मुझे Aspose.CAD के लिए विस्तृत दस्तावेज़ कहां मिल सकते हैं?

 A4: दस्तावेज़ उपलब्ध है[यहाँ](https://reference.aspose.com/cad/net/).

### Q5: मैं Aspose.CAD से संबंधित समर्थन कैसे प्राप्त कर सकता हूं या प्रश्न कैसे पूछ सकता हूं?

 A5: सामुदायिक मंच पर जाएँ[यहाँ](https://forum.aspose.com/c/cad/19) समर्थन और चर्चा के लिए.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
