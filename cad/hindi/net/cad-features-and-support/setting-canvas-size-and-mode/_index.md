---
title: .NET के लिए Aspose.CAD में कैनवास आकार और मोड सेट करना
linktitle: कैनवास का आकार और मोड सेट करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD में कैनवास आकार और मोड सेट करने पर चरण-दर-चरण मार्गदर्शिका देखें। इस व्यापक ट्यूटोरियल का उपयोग करके आसानी से अपने CAD रेंडरिंग को अनुकूलित करें।
weight: 16
url: /hi/net/cad-features-and-support/setting-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.CAD में कैनवास आकार और मोड सेट करना

## परिचय

क्या आप .NET के लिए Aspose.CAD की पूरी क्षमता को अनलॉक करने और अपने CAD रेंडरिंग अनुभव में क्रांति लाने के लिए तैयार हैं? इस चरण-दर-चरण ट्यूटोरियल में, हम शक्तिशाली Aspose.CAD लाइब्रेरी का उपयोग करके कैनवास आकार और मोड सेट करने की जटिलताओं को समझेंगे। चाहे आप एक अनुभवी डेवलपर हों या अभी शुरुआत कर रहे हों, यह मार्गदर्शिका आपको पूरी प्रक्रिया के बारे में बताएगी और यह सुनिश्चित करेगी कि आप Aspose.CAD की क्षमताओं का प्रभावी ढंग से उपयोग करें।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  Aspose.CAD लाइब्रेरी: Aspose.CAD लाइब्रेरी को डाउनलोड और इंस्टॉल करें[Aspose.CAD वेबसाइट](https://releases.aspose.com/cad/net/).

- विकास परिवेश: सुनिश्चित करें कि आपकी मशीन पर .NET विकास परिवेश स्थापित है।

-  नमूना CAD फ़ाइल: इस ट्यूटोरियल के लिए, हम एक नमूना DXF फ़ाइल का उपयोग करेंगे। आप इनमें से एक पा सकते हैं[Aspose.CAD दस्तावेज़ीकरण](https://reference.aspose.com/cad/net/).

## नामस्थान आयात करें

आरंभ करने के लिए, अपने .NET एप्लिकेशन की शुरुआत में आवश्यक नामस्थान आयात करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## चरण 1: CAD फ़ाइल लोड करें

निम्नलिखित कोड का उपयोग करके CAD फ़ाइल लोड करके प्रारंभ करें:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //आगे के चरणों के लिए आपका कोड यहां जाएगा
}
```

## चरण 2: कैडरास्टराइज़ेशन विकल्प बनाएं

 का एक उदाहरण बनाएं`CadRasterizationOptions` और इसके गुण सेट करें:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## चरण 3: पीडीएफ विकल्प बनाएं

 का एक उदाहरण बनाएं`PdfOptions` और इसे सेट करें`VectorRasterizationOptions` संपत्ति:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## चरण 4: पीडीएफ में निर्यात करें

कॉन्फ़िगर विकल्पों का उपयोग करके सीएडी फ़ाइल को पीडीएफ में निर्यात करें:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## चरण 5: टिफऑप्शंस बनाएं

 का एक उदाहरण बनाएं`TiffOptions` और इसे सेट करें`VectorRasterizationOptions` संपत्ति:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## चरण 6: TIFF में निर्यात करें

कॉन्फ़िगर विकल्पों का उपयोग करके CAD फ़ाइल को TIFF में निर्यात करें:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.CAD में कैनवास का आकार और मोड सफलतापूर्वक सेट कर लिया है। यह शक्तिशाली सुविधा CAD रेंडरिंग के लिए संभावनाओं की दुनिया खोलती है। विभिन्न विकल्पों के साथ प्रयोग करें और अपने .NET अनुप्रयोगों में Aspose.CAD की पूरी क्षमता की खोज करें।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य .NET लाइब्रेरीज़ के साथ Aspose.CAD का उपयोग कर सकता हूँ?

A1: हां, Aspose.CAD अन्य .NET लाइब्रेरीज़ के साथ सहजता से एकीकृत होता है, जो CAD हेरफेर के लिए उन्नत क्षमताएं प्रदान करता है।

### Q2: क्या Aspose.CAD के लिए निःशुल्क परीक्षण उपलब्ध है?

 उ2: हां, आप नि:शुल्क परीक्षण के साथ Aspose.CAD की सुविधाओं का पता लगा सकते हैं। मिलने जाना[यहाँ](https://releases.aspose.com/) प्रारंभ करना।

### Q3: मैं Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A3: समर्थन और चर्चा के लिए, पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19).

### Q4: मुझे Aspose.CAD के लिए व्यापक दस्तावेज़ कहाँ मिल सकते हैं?

 A4: का संदर्भ लें[Aspose.CAD दस्तावेज़ीकरण](https://reference.aspose.com/cad/net/) विस्तृत जानकारी और उदाहरणों के लिए.

### Q5: मैं .NET के लिए Aspose.CAD कैसे खरीदूं?

 A5: Aspose.CAD खरीदने के लिए, पर जाएँ[खरीद पृष्ठ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
