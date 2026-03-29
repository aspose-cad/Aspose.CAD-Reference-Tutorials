---
date: 2026-03-29
description: Aspose.CAD for .NET का उपयोग करके CAD से PDF बनाना, कैनवास आकार सेट करना,
  और CAD को PDF या TIFF में निर्यात करना इस चरण‑दर‑चरण गाइड में सीखें।
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'CAD से PDF कैसे बनाएं: Aspose.CAD for .NET में कैनवास आकार और मोड सेट करें'
url: /hi/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET में कैनवास आकार और मोड सेट करना

## परिचय

CAD फ़ाइलों से **PDF बनाने** के लिए तैयार हैं जबकि आउटपुट आयामों को नियंत्रित कर रहे हैं? इस ट्यूटोरियल में हम कैनवास आकार और मोड सेट करने, CAD फ़ाइल लोड करने, और Aspose.CAD for .NET के साथ इसे PDF या TIFF में निर्यात करने की प्रक्रिया देखेंगे। चाहे आपको **DXF को PDF में बदलना** हो, हाई‑रेज़ोल्यूशन ड्रॉइंग्स बनानी हों, या बस रास्टराइज़ेशन क्षेत्र को समायोजित करना हो, नीचे दिए गए चरण आपको एक ठोस, प्रोडक्शन‑रेडी समाधान देंगे।

## त्वरित उत्तर
- **create PDF from CAD** का क्या अर्थ है? CAD ड्राइंग (जैसे DXF, DWG) को एक PDF दस्तावेज़ में परिवर्तित करना जो वेक्टर और रास्टर विवरण को संरक्षित रखता है।  
- **आउटपुट आकार को नियंत्रित करने वाला विकल्प कौन सा है?** `CadRasterizationOptions.PageWidth` और `PageHeight` (कैनवास आकार)।  
- **क्या मैं TIFF में भी निर्यात कर सकता हूँ?** हाँ – समान रास्टराइज़ेशन सेटिंग्स के साथ `TiffOptions` का उपयोग करें।  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** एक व्यावसायिक लाइसेंस आवश्यक है; एक मुफ्त ट्रायल उपलब्ध है।  
- **समर्थित .NET संस्करण?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## “create PDF from CAD” क्या है?
CAD से PDF बनाना मतलब CAD ड्राइंग को एक पेज‑ओरिएंटेड फ़ॉर्मेट (PDF) में रेंडर करना है जिसे CAD सॉफ़्टवेयर की आवश्यकता के बिना देखा, प्रिंट या साझा किया जा सकता है। Aspose.CAD इस प्रक्रिया को संभालता है, जिससे आप कैनवास आकार, स्केलिंग, और आउटपुट फ़ॉर्मेट निर्धारित कर सकते हैं।

## CAD से PDF बनाते समय कैनवास आकार क्यों सेट करें?
कैनवास आकार सेट करने से आपको परिणामी PDF या TIFF की रिज़ॉल्यूशन और आयामों पर सटीक नियंत्रण मिलता है। यह विशेष रूप से उपयोगी है जब:
- विशिष्ट कागज़ आकार पर प्रिंटिंग के लिए ड्रॉइंग तैयार की जा रही हों।  
- वेब प्रीव्यू के लिए थंबनेल या हाई‑रेज़ोल्यूशन इमेज़ बनानी हों।  
- कई दस्तावेज़ों में समान लेआउट सुनिश्चित करना हो।

## पूर्वापेक्षाएँ

- Aspose.CAD लाइब्रेरी: [Aspose.CAD वेबसाइट](https://releases.aspose.com/cad/net/) से Aspose.CAD लाइब्रेरी डाउनलोड और इंस्टॉल करें।  
- विकास पर्यावरण: सुनिश्चित करें कि आपके मशीन पर .NET विकास पर्यावरण स्थापित है।  
- नमूना CAD फ़ाइल: इस ट्यूटोरियल के लिए हम एक नमूना DXF फ़ाइल का उपयोग करेंगे। आप इसे [Aspose.CAD दस्तावेज़ीकरण](https://reference.aspose.com/cad/net/) में पा सकते हैं।

## नेमस्पेस आयात करें

पहले, CAD प्रोसेसिंग के लिए आवश्यक नेमस्पेस आयात करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## कस्टम कैनवास आकार के साथ CAD से PDF कैसे बनाएं

### चरण 1: CAD फ़ाइल लोड करें

हम **CAD फ़ाइल लोड करने** (जैसे, एक DXF) से शुरू करते हैं और इसे `Image` ऑब्जेक्ट में लोड करते हैं। यह वह बिंदु है जहाँ आप **CAD फ़ाइल** को मेमोरी में लोड करते हैं।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### चरण 2: CadRasterizationOptions बनाएं

`CadRasterizationOptions` का एक इंस्टेंस बनाएं और कैनवास आकार निर्धारित करें। `PageWidth` और `PageHeight` प्रॉपर्टी आपको आवश्यक सटीक आयामों के साथ **कैनवास आकार सेट** करने देती हैं।

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### चरण 3: PdfOptions बनाएं (CAD को PDF में निर्यात करें)

रास्टराइज़ेशन सेटिंग्स को `PdfOptions` ऑब्जेक्ट से लिंक करें। यह कॉन्फ़िगरेशन आपको परिभाषित कस्टम कैनवास के साथ **CAD को PDF में निर्यात** करने में सक्षम बनाता है।

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### चरण 4: PDF में निर्यात करें (DXF को PDF में बदलें)

अब इमेज को PDF के रूप में सहेजें। यह चरण सेट किए गए विकल्पों का उपयोग करके **CAD से PDF बनाता** है।

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### चरण 5: TiffOptions बनाएं (CAD को TIFF में निर्यात करें)

यदि आपको रास्टर इमेज भी चाहिए, तो `TiffOptions` को कॉन्फ़िगर करें। वही रास्टराइज़ेशन विकल्प पुनः उपयोग किए जाते हैं, इसलिए **CAD को TIFF में निर्यात** कैनवास आकार का सम्मान करता है।

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### चरण 6: TIFF में निर्यात करें

अंत में, ड्रॉइंग को TIFF फ़ाइल के रूप में सहेजें।

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## सामान्य समस्याएँ और समाधान

- **Canvas appears cropped** – सुनिश्चित करें कि `AutomaticLayoutsScaling` `true` पर सेट है और `NoScaling` `false` है ताकि ड्रॉइंग कैनवास में फिट होने के लिए स्केल हो।  
- **Low‑resolution PDF** – `PageWidth`/`PageHeight` बढ़ाएँ या `CadRasterizationOptions` पर `Resolution` सेट करें।  
- **File not found error** – सुनिश्चित करें कि `MyDir` एक वैध डायरेक्टरी की ओर इशारा कर रहा है और DXF फ़ाइल नाम बिल्कुल मेल खाता है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं Aspose.CAD को अन्य .NET लाइब्रेरीज़ के साथ उपयोग कर सकता हूँ?
A1: हाँ, Aspose.CAD अन्य .NET लाइब्रेरीज़ के साथ सहजता से एकीकृत होता है, जिससे CAD हेरफेर के लिए उन्नत क्षमताएँ मिलती हैं।

### प्रश्न 2: क्या Aspose.CAD के लिए मुफ्त ट्रायल उपलब्ध है?
A2: हाँ, आप Aspose.CAD की सुविधाओं को मुफ्त ट्रायल के साथ एक्सप्लोर कर सकते हैं। शुरू करने के लिए [यहाँ](https://releases.aspose.com/) जाएँ।

### प्रश्न 3: मैं Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूँ?
A3: समर्थन और चर्चा के लिए, [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) पर जाएँ।

### प्रश्न 4: मैं Aspose.CAD की व्यापक दस्तावेज़ीकरण कहाँ पा सकता हूँ?
A4: विस्तृत जानकारी और उदाहरणों के लिए [Aspose.CAD दस्तावेज़ीकरण](https://reference.aspose.com/cad/net/) देखें।

### प्रश्न 5: मैं .NET के लिए Aspose.CAD कैसे खरीदूँ?
A5: Aspose.CAD खरीदने के लिए, [खरीद पृष्ठ](https://purchase.aspose.com/buy) पर जाएँ।

**अतिरिक्त प्रश्नोत्तर**

**प्रश्न: क्या मैं मल्टी‑पेज CAD ड्रॉइंग को एक ही PDF में निर्यात कर सकता हूँ?**  
**उत्तर:** हाँ। `CadRasterizationOptions` में `PageCount` सेट करें और लाइब्रेरी पृष्ठों को एक PDF में जोड़ देगी।

**प्रश्न: क्या कैनवास आकार वेक्टर डेटा की गुणवत्ता को प्रभावित करता है?**  
**उत्तर:** वेक्टर डेटा रिज़ॉल्यूशन‑स्वतंत्र रहता है; कैनवास आकार केवल रास्टराइज़्ड तत्वों और इमेज़ रिज़ॉल्यूशन को प्रभावित करता है।

---

**अंतिम अपडेट:** 2026-03-29  
**परीक्षित संस्करण:** Aspose.CAD 24.11 for .NET  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}