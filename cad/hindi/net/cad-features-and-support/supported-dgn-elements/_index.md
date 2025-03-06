---
title: .NET के लिए Aspose.CAD में समर्थित DGN तत्व
linktitle: समर्थित डीजीएन तत्व
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: DGN फ़ाइलों को संभालने के लिए .NET की शक्तिशाली सुविधाओं के लिए Aspose.CAD का अन्वेषण करें। 2डी और 3डी तत्वों के साथ निर्बाध रूप से काम करने के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 18
url: /hi/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.CAD में समर्थित DGN तत्व

## परिचय

क्या आप एक .NET डेवलपर हैं जो DGN फ़ाइलों के साथ निर्बाध रूप से काम करना चाहते हैं? .NET के लिए Aspose.CAD DGN फ़ाइलों को कुशलतापूर्वक संभालने के लिए एक मजबूत समाधान प्रदान करता है। इस ट्यूटोरियल में, हम समर्थित DGN तत्वों के बारे में विस्तार से जानेंगे और .NET के लिए Aspose.CAD के साथ काम करने की प्रक्रिया में आपका मार्गदर्शन करेंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- .NET प्रोग्रामिंग का बुनियादी ज्ञान।
- आपकी मशीन पर विज़ुअल स्टूडियो स्थापित है।
-  .NET लाइब्रेरी के लिए Aspose.CAD, जिसे आप डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

## नामस्थान आयात करें

अपने प्रोजेक्ट को किकस्टार्ट करने के लिए, अपने .NET एप्लिकेशन में आवश्यक नेमस्पेस आयात करें। यह चरण सुनिश्चित करता है कि आपके पास .NET के लिए Aspose.CAD द्वारा प्रदान की गई कार्यक्षमताओं तक पहुंच है।

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## चरण 1: डीजीएन फ़ाइल लोड करें

अपने .NET एप्लिकेशन में मौजूदा DGN फ़ाइल को कैडइमेज के रूप में लोड करके शुरुआत करें।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // आपका कोड यहाँ
}
```

## चरण 2: डीजीएन तत्वों के माध्यम से पुनरावृति करें

फ़ोरैच लूप का उपयोग करके DGN तत्वों के माध्यम से पुनरावृति करें। .NET के लिए Aspose.CAD विभिन्न प्रकार के DGN तत्व प्रकार प्रदान करता है जिनके साथ आप काम कर सकते हैं।

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // आपका कोड यहाँ
}
```

## चरण 3: पहले से समर्थित संस्थाओं को संभालें

पहले समर्थित 2डी इकाइयों को संभालें, जो अब 3डी के लिए भी समर्थित हैं।

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // अतिरिक्त मामले
        {
            // आपका कोड यहाँ
            break;
        }
}
```

## चरण 4: समर्थित 3डी इकाइयों को संभालें

.NET के लिए Aspose.CAD द्वारा प्रदान की गई समर्थित 3D इकाइयों को संभालें।

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // आपका कोड यहाँ
            break;
        }
}
```

## चरण 5: निर्यात करें और सहेजें

अंत में, संशोधित DGN फ़ाइल को एक रेखापुंज छवि में निर्यात करें और इसे निर्दिष्ट निर्देशिका में सहेजें।

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने DGN फ़ाइलों को संभालने और हेरफेर करने में .NET के लिए Aspose.CAD की क्षमताओं का पता लगाया। चरण-दर-चरण मार्गदर्शिका का पालन करके, आप समर्थित DGN तत्वों के साथ कुशलतापूर्वक काम कर सकते हैं, चाहे वे 2D या 3D इकाइयाँ हों। .NET के लिए Aspose.CAD आपको अपने .NET अनुप्रयोगों में DGN फ़ाइल प्रोसेसिंग को निर्बाध रूप से एकीकृत करने का अधिकार देता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: मुझे .NET के लिए Aspose.CAD का दस्तावेज़ कहां मिल सकता है?

 A1: आप दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/cad/net/).

### Q2: मैं .NET के लिए Aspose.CAD कैसे डाउनलोड करूं?

 A2: आप लाइब्रेरी डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

### Q3: क्या .NET के लिए Aspose.CAD का निःशुल्क परीक्षण उपलब्ध है?

 उ3: हाँ, आप नि:शुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं .NET के लिए Aspose.CAD के लिए अस्थायी लाइसेंस कहां से प्राप्त कर सकता हूं?

 A4: अस्थायी लाइसेंस उपलब्ध हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: सहायता चाहिए या कोई प्रश्न हैं?

 A5: .NET समुदाय के लिए Aspose.CAD पर जाएँ[सहयता मंच](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
