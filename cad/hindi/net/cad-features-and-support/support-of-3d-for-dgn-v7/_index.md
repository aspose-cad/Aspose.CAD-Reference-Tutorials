---
date: 2026-03-29
description: Aspose.CAD for .NET का उपयोग करके CAD रास्टराइज़ेशन विकल्पों को कॉन्फ़िगर
  करना और 3D समर्थन के साथ DGN को PDF में निर्यात करना सीखें।
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DGN V7 3D के लिए CAD रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें
url: /hi/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD रास्टराइज़ेशन विकल्पों को DGN V7 3D के लिए कॉन्फ़िगर करें

## परिचय

इस व्यापक ट्यूटोरियल में आप सीखेंगे **कैसे CAD रास्टराइज़ेशन विकल्पों को कॉन्फ़िगर करें** ताकि Aspose.CAD for .NET का उपयोग करके 3‑D DGN V7 फ़ाइल को PDF में निर्यात किया जा सके। चाहे आप एक CAD व्यूअर, रिपोर्टिंग टूल, या स्वचालित रूपांतरण पाइपलाइन बना रहे हों, इन सेटिंग्स में महारत हासिल करने से आपको पेज आकार, लेआउट स्केलिंग, बैकग्राउंड रंग, और उन विशिष्ट दृश्यों पर सटीक नियंत्रण मिलता है जिन्हें आप रेंडर करना चाहते हैं। चलिए प्रक्रिया को चरण दर चरण देखते हैं।

## त्वरित उत्तर
- **“configure CAD rasterization options” क्या मतलब है?**  
  यह CAD फ़ाइल को रास्टर फ़ॉर्मेट (जैसे PDF) में बदलने से पहले पेज आयाम, स्केलिंग, बैकग्राउंड रंग और लेआउट चयन जैसी प्रॉपर्टीज़ सेट करने को दर्शाता है।
- **3‑D समर्थन के साथ DGN को PDF में कैसे निर्यात करें?**  
  `DgnImage` के साथ DGN लोड करें, `PdfOptions` + `CadRasterizationOptions` निर्धारित करें, फिर `Save` कॉल करें।
- **क्या उत्पादन उपयोग के लिए लाइसेंस चाहिए?**  
  हाँ – परिनियोजन के लिए एक व्यावसायिक लाइसेंस आवश्यक है; एक मुफ्त ट्रायल उपलब्ध है।
- **कौन से .NET संस्करण समर्थित हैं?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7।
- **क्या मैं निर्यात के लिए विशिष्ट दृश्यों का चयन कर सकता हूँ?**  
  बिल्कुल – रास्टराइज़ेशन विकल्पों में `Layouts` एरे सेट करें।

## “configure CAD rasterization options” क्या है?

CAD रास्टराइज़ेशन विकल्पों को कॉन्फ़िगर करना मतलब CAD ड्राइंग को रास्टर (वेक्टर से बिटमैप या PDF) में बदलने के तरीके को अनुकूलित करना है। इन सेटिंग्स को समायोजित करके आप विज़ुअल आउटपुट, प्रदर्शन और उत्पन्न दस्तावेज़ के फ़ाइल आकार को नियंत्रित करते हैं।

## 3‑D DGN V7 निर्यात के लिए Aspose.CAD क्यों उपयोग करें?

- **Full .NET integration** – कोई COM या नेटिव DLL आवश्यक नहीं।  
- **Supports 3‑D geometry** – PDF में रेंडर करते समय गहराई की जानकारी बरकरार रखता है।  
- **Fine‑grained control** – सटीक लेआउट, स्केलिंग और बैकग्राउंड रंग चुनें।  
- **Cross‑platform** – .NET Core के साथ Windows, Linux और macOS पर काम करता है।

## आवश्यकताएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास है:

- **Aspose.CAD for .NET** – इसे [here](https://releases.aspose.com/cad/net/) से डाउनलोड करें।  
- **Visual Studio** या कोई भी संगत .NET IDE।  
- **एक सैंपल DGN फ़ाइल** – इस गाइड के लिए हम `Nikon_D90_Camera.dgn` का उपयोग करेंगे (Aspose सैंपल पैक में शामिल)।

अब जब सब तैयार है, चलिए कोड में डुबकी लगाते हैं।

## नेमस्पेस आयात करें

अपने .NET प्रोजेक्ट में आवश्यक नेमस्पेस आयात करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## चरण 1: अपने दस्तावेज़ निर्देशिका को सेट अप करें

एक वेरिएबल बनाएं जो उस फ़ोल्डर की ओर इशारा करे जहाँ आपका स्रोत DGN और आउटपुट फ़ाइलें स्थित होंगी।

```csharp
string MyDir = "Your Document Directory";
```

## चरण 2: DGN फ़ाइल लोड करें

`DgnImage` के रूप में DGN फ़ाइल लोड करें। यह ऑब्जेक्ट आपको CAD डेटा और रास्टराइज़ेशन पाइपलाइन तक पहुँच देता है।

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## चरण 3: PDF निर्यात विकल्प कॉन्फ़िगर करें (CAD रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें)

यहाँ हम **CAD रास्टराइज़ेशन विकल्पों** को कॉन्फ़िगर करते हैं जो निर्धारित करते हैं कि 3‑D मॉडल PDF में कैसे रेंडर होगा। आप पेज आकार, स्वचालित लेआउट स्केलिंग, बैकग्राउंड रंग सेट कर सकते हैं, और वह सटीक लेआउट (व्यू) चुन सकते हैं जिसे आप निर्यात करना चाहते हैं।

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## चरण 4: रास्टर इमेज सहेजें

अंत में, आपने अभी जो विकल्प कॉन्फ़िगर किए हैं उनका उपयोग करके DGN को PDF फ़ाइल में निर्यात करें।

```csharp
dgnImage.Save(outFile, options);
```

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **खाली PDF आउटपुट** | सत्यापित करें कि `Layouts` एरे में DGN फ़ाइल में मौजूद सही व्यू पहचानकर्ता हैं। |
| **गलत रंग** | सुनिश्चित करें कि `BackgroundColor` इच्छित मान पर सेट है; हल्के बैकग्राउंड के लिए `Color.White` उपयोग करें। |
| **बड़े फ़ाइलों पर प्रदर्शन बाधा** | `AutomaticLayoutsScaling` सक्षम करें और छोटे रास्टर रिज़ॉल्यूशन के लिए `PageWidth/PageHeight` घटाने पर विचार करें। |
| **लाइसेंस अपवाद** | ट्रायल वॉटरमार्क से बचने के लिए इमेज लोड करने से पहले एक वैध Aspose.CAD लाइसेंस स्थापित करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.CAD for .NET को अन्य CAD फ़ाइल फ़ॉर्मेट्स के साथ उपयोग कर सकता हूँ?**  
A: हाँ, Aspose.CAD DWG, DXF, DWF, DGN और कई अन्य फ़ॉर्मेट्स को सपोर्ट करता है।

**Q: Aspose.CAD के साथ काम करते समय अपवादों को कैसे संभालूँ?**  
A: अपने कोड को `try‑catch` ब्लॉक में रखें और विस्तृत त्रुटि जानकारी के लिए `Aspose.CAD.CADException` की जाँच करें।

**Q: क्या Aspose.CAD व्यावसायिक प्रोजेक्ट्स के लिए उपयुक्त है?**  
A: बिल्कुल। आप एक लाइसेंस [here](https://purchase.aspose.com/buy) खरीद सकते हैं।

**Q: क्या मैं खरीदने से पहले Aspose.CAD for .NET को आज़मा सकता हूँ?**  
A: हाँ, एक मुफ्त ट्रायल उपलब्ध है [here](https://releases.aspose.com/)।

**Q: Aspose.CAD के लिए सामुदायिक समर्थन कहाँ मिल सकता है?**  
A: चर्चा फ़ोरम [here](https://forum.aspose.com/c/cad/19) में शामिल हों।

---

**अंतिम अद्यतन:** 2026-03-29  
**परीक्षित संस्करण:** Aspose.CAD 24.11 for .NET  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}