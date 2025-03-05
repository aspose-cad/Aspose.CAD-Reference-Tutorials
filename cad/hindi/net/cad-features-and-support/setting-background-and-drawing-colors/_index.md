---
title: .NET के लिए Aspose.CAD में पृष्ठभूमि सेट करना और रंग बनाना
linktitle: पृष्ठभूमि और ड्राइंग रंग सेट करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए मास्टर Aspose.CAD। पृष्ठभूमि और ड्राइंग रंग आसानी से सेट करें। हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें.
type: docs
weight: 15
url: /hi/net/cad-features-and-support/setting-background-and-drawing-colors/
---
## परिचय

.NET विकास की गतिशील दुनिया में, Aspose.CAD कंप्यूटर-एडेड डिज़ाइन (CAD) फ़ाइलों को संभालने के लिए एक शक्तिशाली उपकरण के रूप में उभरता है। यदि आप सीएडी ड्राइंग में हेरफेर करने में अपने कौशल को बढ़ाने के लिए उत्सुक हैं, तो यह ट्यूटोरियल आपका प्रवेश द्वार है। हम .NET के लिए Aspose.CAD का उपयोग करके पृष्ठभूमि सेट करने और रंग खींचने की जटिलताओं को गहराई से समझेंगे, आपको चरण-दर-चरण मार्गदर्शिका प्रदान करेंगे जो स्पष्टता और प्रभावशीलता सुनिश्चित करती है।

## आवश्यक शर्तें

इससे पहले कि हम इस यात्रा पर निकलें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

- .NET विकास की बुनियादी समझ।
-  .NET के लिए Aspose.CAD की स्थापना। अगर आपने अभी तक ऐसा नहीं किया है तो आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).
- प्रयोग के लिए एक नमूना सीएडी फ़ाइल। आप इसे अपनी दस्तावेज़ निर्देशिका में पा सकते हैं।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, आवश्यक नामस्थान आयात करके प्रारंभ करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## चरण 1: CAD फ़ाइल लोड करें

निम्नलिखित कोड स्निपेट का उपयोग करके उस CAD फ़ाइल को लोड करके प्रारंभ करें जिसके साथ आप काम करना चाहते हैं:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // आगे की प्रक्रिया के लिए आपका कोड यहां जाता है
}
```

## चरण 2: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

 का एक उदाहरण बनाएं`CadRasterizationOptions` और पृष्ठभूमि और ड्राइंग रंग सेटअप के लिए इसके गुण सेट करें:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.BackgroundColor = Color.Beige;
rasterizationOptions.DrawType = CadDrawTypeMode.UseDrawColor;
rasterizationOptions.DrawColor = Color.Blue;
```

## चरण 3: पीडीएफ में निर्यात करें

 का एक उदाहरण बनाएं`PdfOptions` और सेट करें`VectorRasterizationOptions` संपत्ति:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;

// सीएडी को पीडीएफ में निर्यात करें
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## चरण 4: TIFF में निर्यात करें

 का एक उदाहरण बनाएं`TiffOptions` और सेट करें`VectorRasterizationOptions` संपत्ति:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;

// CAD को TIFF में निर्यात करें
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि .NET के लिए Aspose.CAD में पृष्ठभूमि और ड्राइंग रंग कैसे सेट करें। यह ट्यूटोरियल आपको CAD फ़ाइलों में आसानी से हेरफेर करने के कौशल से लैस करता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं किसी भी प्रकार की CAD फ़ाइल के साथ .NET के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: हाँ, Aspose.CAD DWG, DXF और DGN सहित विभिन्न CAD प्रारूपों का समर्थन करता है।

### Q2: क्या .NET के लिए Aspose.CAD का निःशुल्क परीक्षण उपलब्ध है?

 उ2: हां, आप निःशुल्क परीक्षण का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मुझे .NET के लिए Aspose.CAD के लिए विस्तृत दस्तावेज़ कहां मिल सकते हैं?

 A3: दस्तावेज़ देखें[यहाँ](https://reference.aspose.com/cad/net/).

### Q4: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A4: अस्थायी लाइसेंस प्राप्त किया जा सकता है[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: सहायता की आवश्यकता है या समुदाय से जुड़ना चाहते हैं?

 A5: सहायता फ़ोरम पर जाएँ[यहाँ](https://forum.aspose.com/c/cad/19).
