---
title: .NET के लिए Aspose.CAD में DGN को PDF में निर्यात करें
linktitle: डीजीएन को पीडीएफ में निर्यात करें
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD के साथ आसानी से DGN फ़ाइलों को PDF में निर्यात करना सीखें। निर्बाध सीएडी फ़ाइल हेरफेर के लिए चरण-दर-चरण मार्गदर्शिका।
type: docs
weight: 12
url: /hi/net/cad-export-formats/export-dgn-to-pdf/
---
## परिचय

.NET विकास की दुनिया में, Aspose.CAD एक शक्तिशाली लाइब्रेरी है जो CAD फ़ाइलों के हेरफेर और रूपांतरण की सुविधा प्रदान करती है। डेवलपर्स द्वारा अक्सर सामना किया जाने वाला एक सामान्य कार्य DGN फ़ाइलों को पीडीएफ प्रारूप में निर्यात करना है। इस ट्यूटोरियल में, हम .NET के लिए Aspose.CAD का उपयोग करते हुए चरण दर चरण प्रक्रिया के बारे में जानेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित स्थान हैं:

- C# और .NET फ्रेमवर्क का कार्यसाधक ज्ञान।
-  .NET लाइब्रेरी के लिए Aspose.CAD स्थापित किया गया। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).
- उदाहरण के लिए, इस ट्यूटोरियल के लिए एक नमूना DGN फ़ाइल, "Nikon_D90_Camera.dgn"।

## नामस्थान आयात करें

अपने C# प्रोजेक्ट में, आवश्यक नामस्थान आयात करके प्रारंभ करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## चरण 1: डीजीएन फ़ाइल लोड करें

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // आपका कोड यहां...
}
```

## चरण 2: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## चरण 3: पीडीएफ विकल्प बनाएं

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## चरण 4: पीडीएफ के रूप में सहेजें

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.CAD का उपयोग करके DGN फ़ाइल को PDF में सफलतापूर्वक निर्यात कर लिया है। इस ट्यूटोरियल में डीजीएन फ़ाइल को लोड करने से लेकर रास्टराइज़ेशन विकल्पों को कॉन्फ़िगर करने और आउटपुट को पीडीएफ के रूप में सहेजने तक आवश्यक चरणों को शामिल किया गया है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं पूर्व CAD ज्ञान के बिना .NET के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: बिल्कुल! Aspose.CAD जटिल CAD कार्यों को सरल बनाता है, जिससे यह विविध पृष्ठभूमि वाले डेवलपर्स के लिए सुलभ हो जाता है।

### Q2: मुझे Aspose.CAD के लिए और अधिक उदाहरण और दस्तावेज़ कहां मिल सकते हैं?

 ए2: अन्वेषण करें[प्रलेखन](https://reference.aspose.com/cad/net/) व्यापक मार्गदर्शिकाओं और उदाहरणों के लिए।

### Q3: क्या Aspose.CAD के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

उ3: हाँ, आप निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 ए4: अस्थायी लाइसेंस प्राप्त करें[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: सहायता चाहिए या कोई प्रश्न हैं?

A5: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन के लिए.