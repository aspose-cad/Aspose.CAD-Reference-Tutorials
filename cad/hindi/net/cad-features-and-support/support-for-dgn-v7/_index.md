---
title: .NET के लिए Aspose.CAD में DGN V7 के लिए समर्थन
linktitle: डीजीएन वी7 के लिए समर्थन
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: DGN V7 के लिए .NET के निर्बाध समर्थन के लिए Aspose.CAD का अन्वेषण करें। चरण-दर-चरण मार्गदर्शन के साथ आसानी से डीजीएन फ़ाइलों को रेखापुंज छवियों में परिवर्तित करें।
weight: 19
url: /hi/net/cad-features-and-support/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.CAD में DGN V7 के लिए समर्थन

## परिचय

.NET विकास के क्षेत्र में, Aspose.CAD कंप्यूटर-एडेड डिज़ाइन (CAD) फ़ाइलों को संभालने के लिए एक शक्तिशाली लाइब्रेरी के रूप में सामने आता है। यह ट्यूटोरियल .NET के लिए Aspose.CAD की एक विशिष्ट सुविधा - DGN V7 फ़ाइलों के लिए समर्थन - पर प्रकाश डालता है। डीजीएन, डिज़ाइन का संक्षिप्त रूप, सीएडी डोमेन में व्यापक रूप से उपयोग किया जाने वाला फ़ाइल स्वरूप है। Aspose.CAD DGN V7 फ़ाइलों के साथ काम करने की प्रक्रिया को सरल बनाता है, जिससे डेवलपर्स को एक सहज अनुभव मिलता है।

## आवश्यक शर्तें

इससे पहले कि हम कार्यान्वयन में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:

-  .NET के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास Aspose.CAD लाइब्रेरी स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[वेबसाइट](https://releases.aspose.com/cad/net/).

- विकास पर्यावरण: विज़ुअल स्टूडियो या किसी अन्य पसंदीदा आईडीई सहित एक कार्यशील .NET विकास वातावरण स्थापित करें।

अब जब हमने पूर्वापेक्षाएँ सुलझा ली हैं, तो आइए देखें कि .NET के लिए Aspose.CAD में DGN V7 के लिए समर्थन का लाभ कैसे उठाया जाए।

## नामस्थान आयात करें

Aspose.CAD की कार्यक्षमता तक पहुँचने के लिए आवश्यक नामस्थान आयात करके प्रारंभ करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## चरण 1: डीजीएन फ़ाइल लोड करें

 मौजूदा DGN फ़ाइल को एक के रूप में लोड करके प्रारंभ करें`CadImage` प्रतिस्थापित करें`"Your Document Directory"` और`"Nikon_D90_Camera.dgn"` उपयुक्त निर्देशिका पथ और फ़ाइल नाम के साथ।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // आगे के चरणों के लिए कोड यहां दिया गया है...
}
```

## चरण 2: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

 एक बनाने के`CadRasterizationOptions` रैस्टराइज़ेशन से संबंधित विभिन्न गुणों को परिभाषित और सेट करने के लिए ऑब्जेक्ट।

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## चरण 3: वेक्टर रैस्टराइज़ेशन विकल्प सेट करें

 एक बनाने के`JpegOptions` ऑब्जेक्ट क्योंकि हम DGN फ़ाइल को JPEG में कनवर्ट करना चाहते हैं। पहले बनाए गए को असाइन करें`CadRasterizationOptions` इस पर आपत्ति करो.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## चरण 4: रास्टराइज़्ड छवि सहेजें

 बुलाएं`Save` की विधि`CadImage` डीजीएन फ़ाइल को रैस्टर छवि में निर्यात करने के लिए क्लास ऑब्जेक्ट, इस मामले में, एक जेपीईजी।

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

इन चरणों के पूरा होने पर, DGN फ़ाइल सफलतापूर्वक एक रैस्टर छवि में निर्यात की जाती है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने .NET के लिए Aspose.CAD में DGN V7 के लिए निर्बाध समर्थन का पता लगाया। चरण-दर-चरण मार्गदर्शिका का पालन करके, डेवलपर्स अपने .NET अनुप्रयोगों की क्षमताओं का विस्तार करते हुए, आसानी से DGN फ़ाइलों को रेखापुंज छवियों में परिवर्तित कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD नवीनतम DGN V7 विशिष्टताओं के साथ संगत है?

A1: हाँ, Aspose.CAD को नवीनतम विशिष्टताओं के साथ अनुकूलता सुनिश्चित करते हुए, DGN V7 फ़ाइलों को निर्बाध रूप से संभालने के लिए डिज़ाइन किया गया है।

### Q2: क्या मैं DGN फ़ाइल रूपांतरण के लिए रैस्टराइज़ेशन विकल्पों को अनुकूलित कर सकता हूँ?

 ए2: बिल्कुल। ट्यूटोरियल दर्शाता है कि कैसे बनाएं और कॉन्फ़िगर करें`CadRasterizationOptions` रूपांतरण प्रक्रिया को अनुकूलित करने के लिए.

### Q3: क्या JPEG के अलावा अन्य समर्थित आउटपुट प्रारूप हैं?

A3: हाँ, Aspose.CAD विभिन्न आउटपुट स्वरूपों का समर्थन करता है। आप विस्तृत सूची के लिए दस्तावेज़ का पता लगा सकते हैं।

### Q4: मैं Aspose.CAD-संबंधित प्रश्नों के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A4: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और चर्चा के लिए।

### Q5: क्या .NET के लिए Aspose.CAD का निःशुल्क परीक्षण उपलब्ध है?

 A5: हाँ, आप निःशुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
