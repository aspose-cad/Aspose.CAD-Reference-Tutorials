---
title: एंबेडेड डीजीएन फ़ाइलें निर्यात करना - Aspose.CAD ट्यूटोरियल
linktitle: एंबेडेड डीजीएन फ़ाइलें निर्यात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD की शक्ति का अन्वेषण करें। इस चरण-दर-चरण ट्यूटोरियल के साथ आसानी से एम्बेडेड डीजीएन फ़ाइलों को पीडीएफ में निर्यात करना सीखें।
weight: 14
url: /hi/net/export-techniques/exporting-embedded-dgn-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# एंबेडेड डीजीएन फ़ाइलें निर्यात करना - Aspose.CAD ट्यूटोरियल

## परिचय

सॉफ़्टवेयर विकास की गतिशील दुनिया में, .NET के लिए Aspose.CAD कंप्यूटर-एडेड डिज़ाइन (CAD) फ़ाइलों को संभालने के लिए एक शक्तिशाली उपकरण के रूप में सामने आता है। यह ट्यूटोरियल आपको .NET के लिए Aspose.CAD का उपयोग करके एम्बेडेड DGN फ़ाइलों को निर्यात करने की प्रक्रिया में मार्गदर्शन करेगा। चाहे आप एक अनुभवी डेवलपर हों या जिज्ञासु शुरुआती, यह चरण-दर-चरण मार्गदर्शिका आपको Aspose.CAD की क्षमताओं का प्रभावी ढंग से उपयोग करने में मदद करेगी।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1.  .NET के लिए Aspose.CAD: यहां से लाइब्रेरी डाउनलोड और इंस्टॉल करें[.NET के लिए Aspose.CAD](https://releases.aspose.com/cad/net/).

2. विकास परिवेश: विज़ुअल स्टूडियो या किसी अन्य पसंदीदा IDE के साथ एक .NET विकास परिवेश स्थापित करें।

3. नमूना DXF फ़ाइल: इस ट्यूटोरियल के लिए, हम "conic_pyramid.dxf" फ़ाइल का उपयोग करेंगे। सुनिश्चित करें कि यह आपके निर्दिष्ट दस्तावेज़ निर्देशिका में उपलब्ध है।

## नामस्थान आयात करें

अपने C# कोड में, आवश्यक नामस्थान आयात करना सुनिश्चित करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## चरण 1: DXF फ़ाइल लोड करें

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //आगे के चरणों के लिए आपका कोड यहां जाएगा
}
```

## चरण 2: रैस्टराइज़ेशन विकल्प सेट करें

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## चरण 3: पीडीएफ विकल्प सेट करें

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## चरण 4: पीडीएफ के रूप में सहेजें

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## चरण 5: सफलता संदेश प्रदर्शित करें

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.CAD का उपयोग करके एम्बेडेड DGN फ़ाइल को PDF में सफलतापूर्वक निर्यात कर लिया है। इस ट्यूटोरियल में आवश्यक चरणों को शामिल किया गया है, जो आपको Aspose.CAD द्वारा प्रदान की जाने वाली अधिक उन्नत कार्यक्षमताओं का पता लगाने के लिए आधार प्रदान करता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य प्रोग्रामिंग भाषाओं के साथ .NET के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: Aspose.CAD मुख्य रूप से .NET का समर्थन करता है, लेकिन Aspose जावा और पायथन सहित विभिन्न भाषाओं के लिए लाइब्रेरी प्रदान करता है।

### Q2: क्या .NET के लिए Aspose.CAD का निःशुल्क परीक्षण उपलब्ध है?

 उ2: हाँ, आप नि:शुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मुझे .NET के लिए Aspose.CAD के लिए व्यापक दस्तावेज़ कहाँ मिल सकते हैं?

 A3: दस्तावेज़ देखें[यहाँ](https://reference.aspose.com/cad/net/).

### Q4: मैं .NET के लिए Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त करूं?

 ए4: एक अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: सहायता की आवश्यकता है या समुदाय के साथ जुड़ना चाहते हैं?

A5: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) समर्थन और चर्चा के लिए.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
