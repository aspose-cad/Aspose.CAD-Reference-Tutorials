---
title: C# में DWG फ़ाइलों में टेक्स्ट जोड़ना - Aspose.CAD ट्यूटोरियल
linktitle: C# में DWG फ़ाइलों में टेक्स्ट जोड़ना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: C# और Aspose.CAD का उपयोग करके DWG फ़ाइलों में टेक्स्ट जोड़ने का तरीका जानें। निर्बाध एकीकरण के लिए इस चरण-दर-चरण ट्यूटोरियल का पालन करें। व्यापक मार्गदर्शन के लिए Aspose.CAD दस्तावेज़ देखें।
type: docs
weight: 14
url: /hi/net/dwg-file-manipulation/adding-text-to-dwg/
---
## परिचय

कंप्यूटर-एडेड डिज़ाइन (CAD) और .NET विकास के गतिशील क्षेत्र में, Aspose.CAD DWG फ़ाइलों में हेरफेर करने के लिए एक शक्तिशाली उपकरण के रूप में सामने आता है। DWG फ़ाइलों में टेक्स्ट जोड़ना एक सामान्य आवश्यकता है, और इस ट्यूटोरियल में, हम पता लगाएंगे कि C# और Aspose.CAD का उपयोग करके इसे कैसे प्राप्त किया जाए।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित स्थान हैं:

-  Aspose.CAD लाइब्रेरी: Aspose.CAD लाइब्रेरी को डाउनलोड और इंस्टॉल करें[लिंक को डाउनलोड करें](https://releases.aspose.com/cad/net/).

-  दस्तावेज़ निर्देशिका: अपने दस्तावेज़ों के लिए एक निर्देशिका सेट करें, और उसका पथ इस प्रकार नोट करें`MyDir`.

अब, आइए इस प्रक्रिया को प्रबंधनीय चरणों में विभाजित करें।

## नामस्थान आयात करें

अपने C# कोड में, Aspose.CAD कार्यात्मकताओं तक पहुँचने के लिए आवश्यक नामस्थान शामिल करें।

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## चरण 1: DWG फ़ाइल लोड करें

 DWG फ़ाइल को एक में लोड करें`Image` Aspose.CAD लाइब्रेरी का उपयोग करके ऑब्जेक्ट।

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // अगले चरणों के लिए आपका कोड यहां दिया गया है
}
```

## चरण 2: कैडटेक्स्ट ऑब्जेक्ट बनाएं

 त्वरित करें ए`CadText` उस पाठ का प्रतिनिधित्व करने के लिए ऑब्जेक्ट जिसे आप DWG फ़ाइल में जोड़ना चाहते हैं।

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;
cadText.ScaleX = 0.0;
```

## चरण 3: DWG में टेक्स्ट जोड़ें

 बनाए गए को जोड़ें`CadText` Aspose.CAD का उपयोग करके DWG फ़ाइल पर आपत्ति करें।

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## चरण 4: पीडीएफ विकल्प कॉन्फ़िगर करें

संशोधित DWG फ़ाइल को पीडीएफ के रूप में सहेजने के लिए पीडीएफ विकल्पों को कॉन्फ़िगर करें।

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## चरण 5: पीडीएफ के रूप में सहेजें

संशोधित DWG फ़ाइल को जोड़े गए टेक्स्ट के साथ PDF के रूप में सहेजें।

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

अब, आपने C# और Aspose.CAD का उपयोग करके DWG फ़ाइल में सफलतापूर्वक टेक्स्ट जोड़ दिया है। अपनी CAD हेरफेर आवश्यकताओं के लिए Aspose.CAD की अधिक सुविधाओं और कार्यात्मकताओं का पता लगाने के लिए स्वतंत्र महसूस करें।

## निष्कर्ष

इस ट्यूटोरियल में, हमने C# और Aspose.CAD का उपयोग करके DWG फ़ाइलों में टेक्स्ट जोड़ने के लिए आवश्यक चरणों को कवर किया है। यह शक्तिशाली संयोजन गतिशील और अनुकूलित सीएडी दस्तावेज़ निर्माण की संभावनाओं को खोलता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD DWG फ़ाइलों के सभी संस्करणों के साथ संगत है?

A1: Aspose.CAD विभिन्न CAD सॉफ़्टवेयर के साथ संगतता सुनिश्चित करते हुए, DWG फ़ाइल संस्करणों की एक विस्तृत श्रृंखला का समर्थन करता है।

### Q2: क्या मैं Aspose.CAD का उपयोग करके एक ही DWG फ़ाइल में एकाधिक टेक्स्ट इकाइयाँ जोड़ सकता हूँ?

उ2: हाँ, आप ट्यूटोरियल में उल्लिखित प्रक्रिया को दोहराकर एक DWG फ़ाइल में एकाधिक टेक्स्ट इकाइयाँ जोड़ सकते हैं।

### Q3: मैं Aspose.CAD में टेक्स्ट फ़ॉन्ट और शैली कैसे बदल सकता हूँ?

 A3: टेक्स्ट फ़ॉन्ट और शैली को संशोधित करने के लिए, के गुणों को समायोजित करें`CadText` इसे DWG फ़ाइल में जोड़ने से पहले ऑब्जेक्ट करें।

### Q4: क्या किसी वाणिज्यिक परियोजना में Aspose.CAD का उपयोग करने के लिए कोई लाइसेंस संबंधी विचार हैं?

 A4: हाँ, Aspose.CAD लाइसेंसिंग शर्तों का अनुपालन सुनिश्चित करें। को देखें[Aspose.CAD खरीद](https://purchase.aspose.com/buy) जानकारी के लिए।

### Q5: मैं कहां से सहायता मांग सकता हूं या Aspose.CAD से संबंधित प्रश्नों पर चर्चा कर सकता हूं?

A5: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19)समुदाय से जुड़ने और समर्थन प्राप्त करने के लिए।