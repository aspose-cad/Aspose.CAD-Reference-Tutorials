---
title: C# के साथ DWG फ़ाइलों में छवियाँ आयात करना - Aspose.CAD गाइड
linktitle: C# के साथ DWG फ़ाइलों में छवियाँ आयात करना
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD के साथ C# का उपयोग करके DWG फ़ाइलों में छवियों को आयात करना सीखें। निर्बाध एकीकरण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 11
url: /hi/net/image-manipulation-and-rendering/importing-images-into-dwg/
---
## परिचय

कंप्यूटर-एडेड डिज़ाइन (CAD) के दायरे में, DWG फ़ाइलों में छवियों को शामिल करना एक सामान्य और महत्वपूर्ण कार्य है। .NET के लिए Aspose.CAD इस प्रक्रिया को सुव्यवस्थित करने के लिए उपकरणों का एक शक्तिशाली सेट प्रदान करता है, जो इसे C# डेवलपर्स के लिए सुलभ बनाता है। इस ट्यूटोरियल में, हम चरण दर चरण छवियों को DWG फ़ाइलों में आयात करने का तरीका जानेंगे।

## आवश्यक शर्तें

गाइड में गोता लगाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- सी# प्रोग्रामिंग का बुनियादी ज्ञान।
-  .NET के लिए Aspose.CAD स्थापित। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).
- एक विकास वातावरण स्थापित किया गया।

## नामस्थान आयात करें

अपने C# प्रोजेक्ट में आवश्यक नामस्थान शामिल करना सुनिश्चित करें:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## चरण 1: अपनी दस्तावेज़ निर्देशिका सेट करें

```csharp
string MyDir = "Your Document Directory";
```

## चरण 2: DWG फ़ाइल लोड करें

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## चरण 3: छवि गुणों को परिभाषित करें

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## चरण 4: सम्मिलन बिंदु और वेक्टर सेट करें

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## चरण 5: रैस्टर छवि बनाएं और कॉन्फ़िगर करें

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## चरण 6: छवि को DWG फ़ाइल में जोड़ें

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## चरण 7: पीडीएफ के रूप में सहेजें

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## निष्कर्ष

.NET के लिए C# और Aspose.CAD का उपयोग करके छवियों को DWG फ़ाइलों में एकीकृत करना एक सहज प्रक्रिया है, जो डेवलपर्स को दृश्य तत्वों के साथ अपने CAD प्रोजेक्टों को सहजता से बढ़ाने के लिए सशक्त बनाती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य प्रोग्रामिंग भाषाओं के साथ .NET के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: Aspose.CAD मुख्य रूप से .NET के लिए डिज़ाइन किया गया है, लेकिन Aspose विभिन्न प्रोग्रामिंग भाषाओं के लिए लाइब्रेरी प्रदान करता है।

### Q2: क्या .NET के लिए Aspose.CAD का निःशुल्क परीक्षण उपलब्ध है?

 उ2: हां, आप निःशुल्क परीक्षण का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मुझे Aspose.CAD के लिए विस्तृत दस्तावेज़ कहाँ मिल सकते हैं?

 A3: दस्तावेज़ उपलब्ध है[यहाँ](https://reference.aspose.com/cad/net/).

### Q4: मैं .NET के लिए Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 ए4: विजिट करें[इस लिंक](https://purchase.aspose.com/temporary-license/) अस्थायी लाइसेंस प्राप्त करने के लिए.

### Q5: क्या Aspose.CAD समर्थन के लिए कोई सामुदायिक मंच हैं?

 A5: हां, आप समर्थन मांग सकते हैं और समुदाय से जुड़ सकते हैं[यहाँ](https://forum.aspose.com/c/cad/19).