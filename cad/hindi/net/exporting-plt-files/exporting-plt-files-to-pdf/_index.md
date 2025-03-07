---
title: पीएलटी फाइलों को पीडीएफ में निर्यात करना - Aspose.CAD गाइड
linktitle: पीएलटी फाइलों को पीडीएफ में निर्यात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का उपयोग करके आसानी से PLT फ़ाइलों को PDF में परिवर्तित करें। निर्बाध एकीकरण और विश्वसनीय परिणामों के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 11
url: /hi/net/exporting-plt-files/exporting-plt-files-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# पीएलटी फाइलों को पीडीएफ में निर्यात करना - Aspose.CAD गाइड

कंप्यूटर-एडेड डिज़ाइन (सीएडी) के गतिशील क्षेत्र में, पीएलटी फ़ाइलों को पीडीएफ प्रारूप में निर्बाध रूप से परिवर्तित करने की क्षमता एक मूल्यवान कौशल है। .NET के लिए Aspose.CAD डेवलपर्स को इस कार्य को सहजता से पूरा करने का अधिकार देता है। इस ट्यूटोरियल में, हम हर मोड़ पर स्पष्टता और समझ सुनिश्चित करते हुए, चरण दर चरण प्रक्रिया से गुजरेंगे।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1.  .NET लाइब्रेरी के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास Aspose.CAD लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

2. विकास परिवेश: एक कार्यशील .NET विकास परिवेश तैयार रखें।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, आवश्यक नामस्थान आयात करके प्रारंभ करें:

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

ये नामस्थान सीएडी संचालन को संभालने के लिए आवश्यक कक्षाएं और कार्यक्षमताएं प्रदान करेंगे।

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

अपने कोड में अपनी दस्तावेज़ निर्देशिका का पथ परिभाषित करके प्रारंभ करें:

```csharp
string MyDir = "Your Document Directory";
```

"आपकी दस्तावेज़ निर्देशिका" को अपने दस्तावेज़ों के वास्तविक पथ से बदलें।

## चरण 2: पीएलटी फ़ाइल लोड करें

निम्नलिखित कोड स्निपेट का उपयोग करके PLT फ़ाइल को CAD छवि में लोड करें:

```csharp
string sourceFilePath = MyDir + "50states.plt";

using (Image cadImage = Image.Load(sourceFilePath))
{
    // आपका कोड यहां जाता है
}
```

## चरण 3: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

पीडीएफ में निर्यात करने के लिए रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें। पृष्ठ आयाम, ड्राइंग प्रकार और पृष्ठभूमि रंग सेट करें:

```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1600,
    PageWidth = 1600,
    DrawType = CadDrawTypeMode.UseObjectColor,
    BackgroundColor = Color.White
};
```

## चरण 4: पीडीएफ विकल्प सेट करें

पीडीएफ विकल्पों को परिभाषित करें और उन्हें पहले से निर्धारित रास्टराइज़ेशन विकल्पों से लिंक करें:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```

## चरण 5: पीडीएफ के रूप में सहेजें

CAD छवि को PDF फ़ाइल के रूप में सहेजें:

```csharp
cadImage.Save(MyDir + "50states.pdf", pdfOptions);
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने .NET के लिए Aspose.CAD का उपयोग करके PLT फ़ाइलों को PDF में निर्यात करने की प्रक्रिया के बारे में जाना है। यह बहुमुखी लाइब्रेरी CAD संचालन को सरल बनाती है, जिससे यह कुशल और विश्वसनीय फ़ाइल रूपांतरण की आवश्यकता वाले डेवलपर्स के लिए एक अमूल्य उपकरण बन जाती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अपने वेब एप्लिकेशन में .NET के लिए Aspose.CAD का उपयोग कर सकता हूं?

A1: हां, .NET के लिए Aspose.CAD डेस्कटॉप और वेब एप्लिकेशन दोनों के साथ संगत है।

### Q2: क्या .NET के लिए Aspose.CAD का निःशुल्क परीक्षण उपलब्ध है?

 उ2: निश्चित रूप से, आप निःशुल्क परीक्षण का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं .NET के लिए Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A3: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और मार्गदर्शन के लिए।

### Q4: Aspose.CAD किन फ़ाइल स्वरूपों का समर्थन करता है?

A4: Aspose.CAD DWG, DXF और PLT सहित CAD प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### Q5: मुझे .NET के लिए Aspose.CAD के लिए विस्तृत दस्तावेज़ कहां मिल सकते हैं?

 A5: का संदर्भ लें[Aspose.CAD दस्तावेज़ीकरण](https://reference.aspose.com/cad/net/) गहन जानकारी के लिए.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
