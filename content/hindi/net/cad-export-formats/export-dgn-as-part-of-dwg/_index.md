---
title: .NET के लिए Aspose.CAD में DWG के भाग के रूप में DGN निर्यात करें
linktitle: DWG के भाग के रूप में DGN निर्यात करें
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: जानें कि .NET के लिए Aspose.CAD में DWG के भाग के रूप में DGN को कैसे निर्यात किया जाए। निर्बाध एकीकरण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 11
url: /hi/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## परिचय

.NET विकास की दुनिया में, Aspose.CAD कंप्यूटर-एडेड डिज़ाइन (CAD) फ़ाइलों के साथ काम करने के लिए एक शक्तिशाली लाइब्रेरी के रूप में सामने आता है। यह ट्यूटोरियल आपको .NET के लिए Aspose.CAD का उपयोग करके DWG (ड्राइंग) फ़ाइल के हिस्से के रूप में DGN (डिज़ाइन) फ़ाइल को निर्यात करने की प्रक्रिया में मार्गदर्शन करेगा। चाहे आप एक अनुभवी डेवलपर हों या अभी शुरुआत कर रहे हों, यह चरण-दर-चरण मार्गदर्शिका आपको इस विशिष्ट कार्य को कुशलतापूर्वक पूरा करने के लिए Aspose.CAD की क्षमताओं का उपयोग करने में मदद करेगी।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास .NET के लिए Aspose.CAD लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/net/).

- विकास परिवेश: अपना पसंदीदा .NET विकास परिवेश सेट करें, जैसे विज़ुअल स्टूडियो।

- C# का बुनियादी ज्ञान: C# प्रोग्रामिंग भाषा से खुद को परिचित करें।

## नामस्थान आयात करें

अपने C# प्रोजेक्ट में, Aspose.CAD कार्यक्षमता तक पहुँचने के लिए आवश्यक नामस्थान शामिल करें। अपनी कोड फ़ाइल की शुरुआत में निम्नलिखित निर्देशों का उपयोग करके जोड़ें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

अब, आइए दिए गए कोड को कई चरणों में तोड़ें:

## चरण 1: फ़ाइल पथ परिभाषित करें

```csharp
//इनपुट और आउटपुट फ़ाइल पथ
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## चरण 2: पीडीएफऑप्शंस इंस्टेंस बनाएं

```csharp
// DWG को PDF में निर्यात करने के लिए PdfOptions क्लास का एक उदाहरण बनाएं
PdfOptions exportOptions = new PdfOptions();
```

## चरण 3: DWG फ़ाइल लोड करें

```csharp
// मौजूदा DWG फ़ाइल को एक छवि के रूप में लोड करें और इसे कैडइमेज प्रकार में परिवर्तित करें
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## चरण 4: संस्थाओं के माध्यम से पुनरावृति करें

```csharp
// DWG फ़ाइल के अंदर प्रत्येक इकाई के माध्यम से पुनरावृति करें
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## चरण 5: इकाई प्रकार की जाँच करें

```csharp
// जांचें कि क्या इकाई एक छवि परिभाषा है
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## चरण 6: अंडरले पथ प्राप्त करें

```csharp
// यदि यह एक छवि परिभाषा है, तो वस्तु का बाहरी संदर्भ प्राप्त करें
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## चरण 7: रैस्टराइज़ेशन विकल्पों को परिभाषित करें

```csharp
// CadRasterizationOptions ऑब्जेक्ट के लिए सेटिंग्स परिभाषित करें
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## चरण 8: DWG को पीडीएफ में निर्यात करें

```csharp
// सेव विधि को कॉल करके DWG को पीडीएफ में निर्यात करें
cadImage.Save(outPath, exportOptions);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.CAD का उपयोग करके DWG फ़ाइल के भाग के रूप में DGN फ़ाइल को निर्यात करने की प्रक्रिया को सफलतापूर्वक पूरा कर लिया है। इस ट्यूटोरियल ने आपको इस विशिष्ट कार्य को निर्बाध रूप से प्राप्त करने के लिए मूलभूत चरण और कोड स्निपेट प्रदान किए हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अपने व्यावसायिक प्रोजेक्ट में .NET के लिए Aspose.CAD का उपयोग कर सकता हूँ?
 A1: हाँ, आप कर सकते हैं। मिलने जाना[यहाँ](https://purchase.aspose.com/buy) लाइसेंसिंग विकल्पों का पता लगाने के लिए।

### Q2: क्या DWG फ़ाइलों के आकार पर कोई सीमाएँ हैं जिन्हें मैं संसाधित कर सकता हूँ?
A2: Aspose.CAD बड़ी DWG फ़ाइलों को संभालने का समर्थन करता है, लेकिन हार्डवेयर सीमाएँ लागू हो सकती हैं।

### Q3: क्या कोई परीक्षण संस्करण उपलब्ध है?
उ3: हाँ, आप निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?
 A4: अस्थायी लाइसेंस प्राप्त किया जा सकता है[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q5: यदि मुझे कोई समस्या आती है तो मैं कहां सहायता मांग सकता हूं?
 A5: आप Aspose.CAD फोरम पर जा सकते हैं[यहाँ](https://forum.aspose.com/c/cad/19) समर्थन के लिए।