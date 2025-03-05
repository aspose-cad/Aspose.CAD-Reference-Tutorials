---
title: विभिन्न लेआउट के साथ एकल पीडीएफ बनाना - Aspose.CAD गाइड
linktitle: विभिन्न लेआउट के साथ एकल पीडीएफ बनाना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का उपयोग करके विभिन्न लेआउट के साथ एक एकल पीडीएफ बनाएं। निर्बाध एकीकरण और कुशल पीडीएफ पीढ़ी के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 13
url: /hi/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## परिचय

क्या आप .NET के लिए Aspose.CAD का उपयोग करके विभिन्न लेआउट के साथ CAD ड्राइंग से एक एकल पीडीएफ दस्तावेज़ तैयार करना चाह रहे हैं? यह चरण-दर-चरण मार्गदर्शिका आपको प्रक्रिया से गुजराएगी, जिससे आपको निर्बाध एकीकरण और कुशल पीडीएफ निर्माण प्राप्त करने में मदद मिलेगी। .NET के लिए Aspose.CAD, CAD चित्रों को प्रोग्रामेटिक रूप से हेरफेर करने के लिए शक्तिशाली सुविधाएँ प्रदान करता है, और इस ट्यूटोरियल में, हम विभिन्न लेआउट के साथ एक एकल पीडीएफ बनाने पर ध्यान केंद्रित करेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

-  .NET के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास .NET के लिए Aspose.CAD स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

- विकास परिवेश: एक .NET विकास परिवेश स्थापित करें, और C# प्रोग्रामिंग की बुनियादी समझ रखें।

## नामस्थान आयात करें

अपने C# प्रोजेक्ट में, .NET के लिए Aspose.CAD की कार्यक्षमताओं का लाभ उठाने के लिए आवश्यक नामस्थान शामिल करें:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## चरण 1: सीएडी छवि लोड करें

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // चरण 1 के लिए आपका कोड यहां जाता है
}
```

## चरण 2: रैस्टराइज़ेशन विकल्पों को अनुकूलित करें

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// कई लेआउट के लिए कस्टम आकार
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## चरण 3: पीडीएफ विकल्पों को परिभाषित करें

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## चरण 4: पीडीएफ के रूप में सहेजें

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

अब आपने .NET के लिए Aspose.CAD का उपयोग करके विभिन्न लेआउट के साथ एक एकल PDF दस्तावेज़ सफलतापूर्वक बना लिया है। अधिक सुविधाओं का पता लगाने और अपनी विशिष्ट आवश्यकताओं के अनुसार कोड को अनुकूलित करने के लिए स्वतंत्र महसूस करें।

## निष्कर्ष

इस ट्यूटोरियल में, हमने .NET के लिए Aspose.CAD का उपयोग करके विभिन्न लेआउट के साथ CAD ड्राइंग से एक एकल पीडीएफ बनाने की प्रक्रिया को कवर किया। यह शक्तिशाली लाइब्रेरी सीएडी हेरफेर कार्यों को सरल बनाती है और विभिन्न परिदृश्यों के लिए लचीलापन प्रदान करती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य CAD प्रारूपों के साथ .NET के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: हां, .NET के लिए Aspose.CAD विभिन्न CAD प्रारूपों जैसे DWG, DXF, DGN और अन्य का समर्थन करता है।

### Q2: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ2: हां, आप निःशुल्क परीक्षण का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं .NET के लिए Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A3: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन के लिए.

### Q4: मुझे विस्तृत दस्तावेज कहां मिल सकते हैं?

 A4: दस्तावेज़ देखें[यहाँ](https://reference.aspose.com/cad/net/).

### Q5: क्या मैं .NET के लिए Aspose.CAD का लाइसेंस खरीद सकता हूँ?

 A5: हाँ, आप लाइसेंस खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).