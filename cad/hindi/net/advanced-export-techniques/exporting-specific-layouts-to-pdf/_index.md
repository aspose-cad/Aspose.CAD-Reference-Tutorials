---
title: पीडीएफ में विशिष्ट लेआउट निर्यात करना - Aspose.CAD गाइड
linktitle: पीडीएफ में विशिष्ट लेआउट निर्यात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का उपयोग करके विशिष्ट लेआउट को PDF में निर्यात करना सीखें। निर्बाध एकीकरण के लिए चरण-दर-चरण मार्गदर्शिका।
weight: 13
url: /hi/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# पीडीएफ में विशिष्ट लेआउट निर्यात करना - Aspose.CAD गाइड

## परिचय

.NET के लिए Aspose.CAD का उपयोग करके विशिष्ट लेआउट को PDF में निर्यात करने पर हमारी चरण-दर-चरण मार्गदर्शिका में आपका स्वागत है। Aspose.CAD एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को CAD फ़ाइल स्वरूपों के साथ निर्बाध रूप से काम करने की अनुमति देती है। इस ट्यूटोरियल में, हम .NET वातावरण में Aspose.CAD का उपयोग करके DWG फ़ाइल से पीडीएफ में विशिष्ट लेआउट निर्यात करने पर ध्यान केंद्रित करेंगे।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET लाइब्रेरी के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास Aspose.CAD लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

- विकास परिवेश: एक .NET विकास परिवेश स्थापित करें, जैसे विज़ुअल स्टूडियो।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.CAD के लिए आवश्यक नामस्थान आयात करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## चरण 1: DWG फ़ाइल लोड करें

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // आगे के चरणों के लिए आपका कोड यहां दिया गया है।
}
```

## चरण 2: कैडरास्टराइज़ेशन विकल्प सेट करें

```csharp
// CadRasterizationOptions का एक उदाहरण बनाएं और इसके विभिन्न गुण सेट करें
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## चरण 3: लेआउट नाम निर्दिष्ट करें

```csharp
// वांछित लेआउट नाम निर्दिष्ट करें
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

## चरण 4: पीडीएफ विकल्प बनाएं

```csharp
// PdfOptions का एक उदाहरण बनाएं
PdfOptions pdfOptions = new PdfOptions();
// वेक्टररैस्टराइज़ेशनऑप्शंस प्रॉपर्टी सेट करें
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## चरण 5: पीडीएफ में निर्यात करें

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// DWG को पीडीएफ में निर्यात करें
image.Save(MyDir, pdfOptions);
```

## चरण 6: सफलता संदेश प्रदर्शित करें

```csharp
// सफलता संदेश प्रदर्शित करें
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.CAD का उपयोग करके विशिष्ट लेआउट को PDF में निर्यात करना सफलतापूर्वक सीख लिया है। यह मार्गदर्शिका एक विस्तृत पूर्वाभ्यास प्रदान करती है, जिससे यह सुनिश्चित होता है कि आप इस कार्यक्षमता को अपनी परियोजनाओं में सहजता से एकीकृत कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं एक साथ कई लेआउट निर्यात कर सकता हूँ?

 A1: हाँ, बस संशोधित करें`Layouts` सभी वांछित लेआउट के नाम शामिल करने के लिए चरण 3 में सरणी बनाएं।

### Q2: क्या Aspose.CAD अन्य CAD फ़ाइल स्वरूपों के साथ संगत है?

A2: हां, Aspose.CAD DWG, DXF, DWF और अन्य सहित विभिन्न CAD प्रारूपों का समर्थन करता है।

### Q3: मैं पीडीएफ आउटपुट सेटिंग्स को कैसे समायोजित कर सकता हूं?

 A3: की संपत्तियों का अन्वेषण करें`CadRasterizationOptions` अनुकूलन विकल्पों के लिए चरण 2 में।

### Q4: मुझे अतिरिक्त Aspose.CAD दस्तावेज़ कहां मिल सकते हैं?

 A4: पर जाएँ[प्रलेखन](https://reference.aspose.com/cad/net/) गहन जानकारी के लिए.

### Q5: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 A5: हाँ, आप निःशुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
