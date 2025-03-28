---
title: .NET के लिए Aspose.CAD में DGN V7 के लिए 3D का समर्थन
linktitle: DGN V7 के लिए 3D का समर्थन
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD में DGN V7 के लिए 3D समर्थन की शक्ति को अनलॉक करें। हमारे चरण-दर-चरण ट्यूटोरियल का अनुसरण करें।
weight: 20
url: /hi/net/cad-features-and-support/support-of-3d-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.CAD में DGN V7 के लिए 3D का समर्थन

## परिचय

.NET के लिए Aspose.CAD में DGN V7 के लिए 3D के समर्थन का लाभ उठाने पर हमारे व्यापक ट्यूटोरियल में आपका स्वागत है! Aspose.CAD एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को उनके .NET अनुप्रयोगों में CAD फ़ाइलों के साथ निर्बाध रूप से काम करने में सक्षम बनाती है। इस ट्यूटोरियल में, हम DGN V7 के लिए 3D समर्थन का उपयोग करने के चरणों का पता लगाएंगे, जो आपको आपकी CAD-संबंधित परियोजनाओं को बढ़ाने के लिए ज्ञान प्रदान करेगा।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास .NET के लिए Aspose.CAD स्थापित है। यदि नहीं, तो आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

- विकास वातावरण: .NET अनुप्रयोग विकास के लिए विजुअल स्टूडियो जैसे उपयुक्त विकास वातावरण स्थापित करें।

- नमूना डीजीएन फ़ाइल: परीक्षण के लिए एक नमूना डीजीएन फ़ाइल तैयार रखें। आप प्रदत्त नमूना फ़ाइल "Nikon_D90_Camera.dgn" का उपयोग कर सकते हैं।

अब, आइए .NET के लिए Aspose.CAD का उपयोग करके DGN V7 के लिए 3D समर्थन प्राप्त करने के चरणों पर आगे बढ़ें!

## नामस्थान आयात करें

अपने .NET एप्लिकेशन में, आवश्यक नामस्थान आयात करके प्रारंभ करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## चरण 1: अपनी दस्तावेज़ निर्देशिका सेट करें

 सुनिश्चित करें कि आपके पास अपने प्रोजेक्ट में एक दस्तावेज़ निर्देशिका स्थापित है। प्रतिस्थापित करें`"Your Document Directory"` आपकी दस्तावेज़ निर्देशिका के वास्तविक पथ के साथ।

```csharp
string MyDir = "Your Document Directory";
```

## चरण 2: डीजीएन फ़ाइल लोड करें

निम्नलिखित कोड का उपयोग करके मौजूदा डीजीएन फ़ाइल को कैडइमेज के रूप में लोड करें:

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // आगे की प्रक्रिया के लिए आपका कोड यहां जाता है
}
```

## चरण 3: पीडीएफ निर्यात विकल्प कॉन्फ़िगर करें

पीडीएफ में निर्यात करने के लिए विकल्प सेट करें, पृष्ठ आयाम, स्वचालित लेआउट स्केलिंग, पृष्ठभूमि रंग और निर्यात करने के लिए लेआउट जैसे वेक्टर रेखापुंज विकल्प निर्दिष्ट करें।

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // केवल निर्दिष्ट दृश्य निर्यात करें
    }
};
```

## चरण 4: रेखापुंज छवि सहेजें

कॉन्फ़िगर किए गए विकल्पों के साथ डीजीएन फ़ाइल को रास्टर छवि के रूप में सहेजें।

```csharp
dgnImage.Save(outFile, options);
```

## निष्कर्ष

बधाई हो! आपने रास्टर छवि में 3D समर्थन के साथ DGN फ़ाइल निर्यात करने के लिए .NET के लिए Aspose.CAD का सफलतापूर्वक उपयोग किया है। इस ट्यूटोरियल ने आपको इस कार्यक्षमता को आपके CAD प्रोजेक्ट्स में एकीकृत करने के लिए आवश्यक चरणों से सुसज्जित किया है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य CAD फ़ाइल स्वरूपों के साथ .NET के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: हाँ, Aspose.CAD DWG और DXF सहित विभिन्न CAD फ़ाइल स्वरूपों का समर्थन करता है।

### Q2: Aspose.CAD के साथ काम करते समय मैं अपवादों को कैसे संभाल सकता हूं?

A2: अपवादों को खूबसूरती से संभालने के लिए, अपने कोड को ट्राई-कैच ब्लॉक में लपेटें, जैसा कि दिए गए उदाहरण में दिखाया गया है।

### Q3: क्या Aspose.CAD व्यावसायिक परियोजनाओं के लिए उपयुक्त है?

 उ3: बिल्कुल! आप .NET के लिए Aspose.CAD खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### Q4: क्या मैं खरीदने से पहले .NET के लिए Aspose.CAD आज़मा सकता हूँ?

ए4: निश्चित रूप से! निःशुल्क परीक्षण का अन्वेषण करें[यहाँ](https://releases.aspose.com/).

### Q5: मुझे .NET के लिए Aspose.CAD के लिए सामुदायिक समर्थन कहां मिल सकता है?

 A5: सामुदायिक मंच पर जाएँ[यहाँ](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
