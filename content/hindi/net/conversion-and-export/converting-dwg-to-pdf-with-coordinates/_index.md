---
title: C# में निर्देशांक के साथ DWG को PDF में परिवर्तित करना - Aspose.CAD ट्यूटोरियल
linktitle: C# में निर्देशांक के साथ DWG को PDF में परिवर्तित करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: Aspose.CAD का उपयोग करके C# में विशिष्ट निर्देशांक के साथ DWG को PDF में परिवर्तित करना सीखें। सटीक और कुशल सीएडी फ़ाइल रूपांतरण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 11
url: /hi/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---
## परिचय

.NET के लिए Aspose.CAD का उपयोग करके निर्दिष्ट निर्देशांक के साथ DWG फ़ाइलों को पीडीएफ में परिवर्तित करने पर इस व्यापक ट्यूटोरियल में आपका स्वागत है। Aspose.CAD एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को उनके .NET अनुप्रयोगों में CAD फ़ाइल स्वरूपों के साथ निर्बाध रूप से काम करने की अनुमति देती है। इस ट्यूटोरियल में, हम आपको सटीकता बढ़ाने के लिए विशिष्ट निर्देशांक प्रदान करते हुए DWG फ़ाइल को पीडीएफ में परिवर्तित करने की प्रक्रिया के बारे में बताएंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

- Aspose.CAD लाइब्रेरी: .NET के लिए Aspose.CAD लाइब्रेरी डाउनलोड और इंस्टॉल करें। आप पुस्तकालय पा सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

- विकास पर्यावरण: सुनिश्चित करें कि आपके पास विज़ुअल स्टूडियो या किसी अन्य पसंदीदा आईडीई सहित एक संगत विकास वातावरण स्थापित है।

- DWG फ़ाइल: रूपांतरण के लिए एक DWG फ़ाइल तैयार रखें। आप दी गई उदाहरण फ़ाइल या अपनी कस्टम DWG फ़ाइल का उपयोग कर सकते हैं।

## नामस्थान आयात करें

अपने C# प्रोजेक्ट में, आवश्यक नामस्थान आयात करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

आइए बेहतर समझ के लिए कोड को चरण-दर-चरण मार्गदर्शिका में विभाजित करें:

## चरण 1: दस्तावेज़ निर्देशिका को परिभाषित करें

```csharp
string MyDir = "Your Document Directory";
```

## चरण 2: स्रोत DWG फ़ाइल पथ सेट करें

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## चरण 3: DWG फ़ाइल लोड करें और रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## चरण 4: निर्देशांक और व्यूपोर्ट को परिभाषित करें

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## चरण 5: व्यूपोर्ट सेटिंग्स लागू करें

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## चरण 6: पीडीएफ विकल्प कॉन्फ़िगर करें और निर्यात करें

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## चरण 7: सफलता संदेश प्रदर्शित करें

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.CAD का उपयोग करके निर्दिष्ट निर्देशांक के साथ एक DWG फ़ाइल को सफलतापूर्वक पीडीएफ में परिवर्तित कर लिया है। इस ट्यूटोरियल में आवश्यक चरणों को शामिल किया गया है और डेवलपर्स के लिए एक स्पष्ट मार्गदर्शिका प्रदान की गई है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य CAD फ़ाइल स्वरूपों के साथ Aspose.CAD का उपयोग कर सकता हूँ?

A1: हां, Aspose.CAD DWG, DXF, DWF और अन्य सहित विभिन्न CAD प्रारूपों का समर्थन करता है।

### Q2: मैं रूपांतरण प्रक्रिया के दौरान त्रुटियों को कैसे संभाल सकता हूँ?

A2: अपवादों को पकड़ने और प्रबंधित करने के लिए ट्राई-कैच ब्लॉक का उपयोग करके त्रुटि प्रबंधन तंत्र लागू करें।

### Q3: क्या Aspose.CAD विंडोज़ और लिनक्स दोनों वातावरणों के लिए उपयुक्त है?

A3: हां, Aspose.CAD विंडोज और लिनक्स दोनों प्लेटफार्मों के साथ संगत है।

### Q4: क्या मैं पीडीएफ आउटपुट को और अधिक अनुकूलित कर सकता हूं?

ए4: निश्चित रूप से! पीडीएफ आउटपुट को अपनी विशिष्ट आवश्यकताओं के अनुरूप बनाने के लिए Aspose.CAD द्वारा प्रदान किए गए व्यापक विकल्पों का अन्वेषण करें।

### Q5: मुझे अतिरिक्त सहायता या सामुदायिक चर्चाएँ कहाँ मिल सकती हैं?

A5: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और चर्चा के लिए।