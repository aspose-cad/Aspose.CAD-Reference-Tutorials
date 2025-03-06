---
title: C# में DWG दस्तावेज़ प्रस्तुत करना - Aspose.CAD गाइड
linktitle: C# में DWG दस्तावेज़ प्रस्तुत करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: Aspose.CAD का उपयोग करके DWG दस्तावेज़ों को C# में प्रस्तुत करना सीखें। यह चरण-दर-चरण मार्गदर्शिका कोड उदाहरणों के साथ आयात करना, कॉन्फ़िगर करना और सहेजना शामिल करती है।
weight: 17
url: /hi/net/image-manipulation-and-rendering/rendering-dwg-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# में DWG दस्तावेज़ प्रस्तुत करना - Aspose.CAD गाइड

## परिचय

Aspose.CAD का उपयोग करके DWG दस्तावेज़ों को C# में प्रस्तुत करने पर व्यापक मार्गदर्शिका में आपका स्वागत है। चाहे आप एक अनुभवी डेवलपर हों या अभी .NET से शुरुआत कर रहे हों, यह ट्यूटोरियल आपको DWG फ़ाइलों को कुशलतापूर्वक प्रस्तुत करने के लिए Aspose.CAD का लाभ उठाने की प्रक्रिया से परिचित कराएगा। Aspose.CAD एक शक्तिशाली एपीआई है जो CAD फ़ाइल स्वरूपों के साथ काम करने के लिए मजबूत कार्यक्षमता प्रदान करता है, जिससे यह DWG फ़ाइलों से निपटने वाले डेवलपर्स के लिए एक पसंदीदा विकल्प बन जाता है।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

- C# प्रोग्रामिंग भाषा का बुनियादी ज्ञान।
- आपकी मशीन पर विज़ुअल स्टूडियो स्थापित है।
-  Aspose.CAD लाइब्रेरी आपके प्रोजेक्ट में एकीकृत है। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).
- उदाहरणों के साथ अनुसरण करने के लिए एक नमूना DWG फ़ाइल, जैसे "Bottom_plate.dwg"।

## नामस्थान आयात करें

आरंभ करने के लिए, अपने C# कोड की शुरुआत में आवश्यक नामस्थान आयात करना सुनिश्चित करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

अब, आइए दिए गए उदाहरण को कई चरणों में तोड़ें:

## चरण 1: DWG फ़ाइल लोड करें

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // DWG फ़ाइल लोड करने के लिए आपका कोड यहां दिया गया है।
}
```

## चरण 2: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//अतिरिक्त रैस्टराइज़ेशन कॉन्फ़िगरेशन यहां जोड़े जा सकते हैं।
```

## चरण 3: आरेखित करने के लिए क्षेत्र को परिभाषित करें

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## चरण 4: एक नया व्यूपोर्ट बनाएं

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## चरण 5: सक्रिय व्यूपोर्ट बदलें

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## चरण 6: पीडीएफ विकल्प कॉन्फ़िगर करें

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## चरण 7: रेंडर किए गए DWG को पीडीएफ के रूप में सहेजें

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## निष्कर्ष

बधाई हो! आपने C# में Aspose.CAD का उपयोग करके DWG दस्तावेज़ को PDF में सफलतापूर्वक प्रस्तुत किया है। अधिक सुविधाओं का पता लगाने और अपनी विशिष्ट आवश्यकताओं के आधार पर कोड को अनुकूलित करने के लिए स्वतंत्र महसूस करें।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य CAD फ़ाइल स्वरूपों के साथ Aspose.CAD का उपयोग कर सकता हूँ?

A1: हां, Aspose.CAD DWG, DXF, DWF और अन्य सहित विभिन्न CAD प्रारूपों का समर्थन करता है।

### Q2: क्या Aspose.CAD .NET कोर के साथ संगत है?

A2: हां, Aspose.CAD .NET फ्रेमवर्क और .NET कोर दोनों के साथ संगत है।

### Q3: मैं DWG फ़ाइल में विभिन्न लेआउट कैसे संभाल सकता हूँ?

 A3: आप इसमें वांछित लेआउट निर्दिष्ट कर सकते हैं`Layouts` की संपत्ति`CadRasterizationOptions`.

### Q4: क्या Aspose.CAD का उपयोग करने के लिए कोई लाइसेंस संबंधी विचार हैं?

 A4: लाइसेंसिंग विवरण के लिए, यहां जाएं[यहाँ](https://purchase.aspose.com/buy).

### Q5: मुझे अतिरिक्त सहायता कहां मिल सकती है?

A5: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और चर्चा के लिए।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
