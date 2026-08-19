---
date: 2026-03-21
description: Aspose.CAD for .NET का उपयोग करके DWG से PDF बनाना और DWG के भाग के रूप
  में DGN निर्यात करना सीखें। यह गाइड यह भी दिखाता है कि DWG को PDF में कैसे बदलें
  और PDF विकल्प कैसे सेट करें।
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG से PDF बनाएं और DWG के हिस्से के रूप में DGN निर्यात करें – Aspose.CAD
  for .NET
url: /hi/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG से PDF बनाएं और DGN को DWG का हिस्सा के रूप में निर्यात करें – Aspose.CAD for .NET

## परिचय

यदि आपको **create PDF from DWG** फ़ाइलें बनानी हैं और साथ ही DGN डिज़ाइन को DWG का हिस्सा के रूप में एम्बेड करना है, तो Aspose.CAD for .NET इसे सरल बनाता है। इस ट्यूटोरियल में हम पूरे वर्कफ़्लो को कवर करेंगे: DWG लोड करना, एम्बेडेड DGN अंडरले खोजना, रास्टराइज़ेशन विकल्पों को कॉन्फ़िगर करना, और अंत में परिणाम को PDF दस्तावेज़ में निर्यात करना। चाहे आप बैच कन्वर्ज़न टूल, रिपोर्टिंग इंजन, या CAD‑BIM इंटीग्रेशन सेवा बना रहे हों, नीचे दिए गए चरण आपको एक ठोस, प्रोडक्शन‑रेडी आधार प्रदान करेंगे।

## त्वरित उत्तर
- **DWG → PDF रूपांतरण को कौनसी लाइब्रेरी संभालती है?** Aspose.CAD for .NET  
- **क्या मैं PDF बनाते समय DGN अंडरले निर्यात कर सकता हूँ?** हाँ – अंडरले को `CadDgnUnderlay` के माध्यम से एक्सेस किया जाता है।  
- **कौनसा मेथड PDF विकल्प सेट करता है?** `PdfOptions` साथ में `CadRasterizationOptions`।  
- **व्यावसायिक उपयोग के लिए लाइसेंस चाहिए?** हाँ, एक वैध Aspose.CAD लाइसेंस आवश्यक है।  
- **समर्थित .NET संस्करण?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7।

## “create PDF from DWG” क्या है?

DWG फ़ाइल से PDF बनाना का अर्थ है वेक्टर ड्राइंग को रास्टर या वेक्टर‑आधारित PDF दस्तावेज़ में रेंडर करना। यह प्रक्रिया उन स्टेकहोल्डर्स के साथ ड्रॉइंग साझा करने के लिए उपयोगी है जिनके पास CAD सॉफ़्टवेयर नहीं है, आर्काइविंग, या प्रिंटेबल रिपोर्ट जनरेट करने के लिए। Aspose.CAD इस कार्य को सरल बनाता है, DWG एंटिटीज़ को पार्स करने और `PdfOptions` के माध्यम से आउटपुट पर सूक्ष्म नियंत्रण प्रदान करने में मदद करता है।

## DWG का हिस्सा के रूप में DGN निर्यात क्यों करें?

DGN अंडरले अक्सर माइक्रोस्टेशन प्रोजेक्ट्स से रेफ़रेंस जियोमेट्री का प्रतिनिधित्व करता है। DGN को DWG के साथ निर्यात करके आप मूल डिज़ाइन संदर्भ को संरक्षित रखते हैं, जिससे डाउनस्ट्रीम उपयोगकर्ता पूर्ण ड्रॉइंग सेट देख सकें। यह विशेष रूप से बहु‑विषयक प्रोजेक्ट्स में मूल्यवान है जहाँ DWG और DGN फ़ाइलें दोनों मौजूद होती हैं।

## पूर्वापेक्षाएँ

- **Aspose.CAD for .NET** – इसे [here](https://releases.aspose.com/cad/net/) से डाउनलोड करें।  
- **डेवलपमेंट एनवायरनमेंट** – Visual Studio (कोई भी हालिया संस्करण) या आपका पसंदीदा .NET IDE।  
- **बेसिक C# नॉलेज** – आपको C# सिंटैक्स और .NET प्रोजेक्ट स्ट्रक्चर में सहज होना चाहिए।

## नेमस्पेस आयात करें

अपने C# स्रोत फ़ाइल के शीर्ष पर आवश्यक `using` निर्देश जोड़ें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## चरण‑दर‑चरण मार्गदर्शिका

### चरण 1: फ़ाइल पथ निर्धारित करें

इनपुट DWG फ़ाइल और आउटपुट PDF नाम सेट करें।

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### चरण 2: `PdfOptions` इंस्टेंस बनाएं (PDF विकल्प सेट करें)

`PdfOptions` आपको PDF के जनरेशन को नियंत्रित करने देता है, जैसे पेज साइज, कॉम्प्रेशन, और मेटाडेटा।

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### चरण 3: DWG फ़ाइल लोड करें

DWG को `CadImage` के रूप में लोड करें ताकि आप उसकी एंटिटीज़ का निरीक्षण कर सकें।

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### चरण 4: इंटिटीज़ के माध्यम से इटररेट करें

ड्रॉइंग में प्रत्येक एंटिटी के माध्यम से चलें ताकि DGN अंडरले को खोजा जा सके।

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### चरण 5: इंटिटी प्रकार जाँचें (dgn कैसे निर्यात करें)

पहचानें कि वर्तमान एंटिटी DGN अंडरले है या नहीं।

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### चरण 6: अंडरले पथ प्राप्त करें

DGN फ़ाइल के एक्सटर्नल रेफ़रेंस पथ को प्राप्त करें।

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### चरण 7: रास्टराइज़ेशन विकल्प निर्धारित करें (dwg को pdf में बदलें)

PDF में रखने से पहले DWG कैसे रास्टराइज़ किया जाएगा, इसे कॉन्फ़िगर करें।

```csharp
// Define settings for CadRasterizationOptions object
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

### चरण 8: DWG को PDF में निर्यात करें

अंत में, रेंडर की गई इमेज को PDF फ़ाइल के रूप में सहेजें।

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|--------|-----|
| **`Image.Load` throws “File not found”** | गलत पथ या फ़ाइल अनुपलब्ध। | पूर्ण पथ (absolute path) का उपयोग करें या सुनिश्चित करें कि DWG आउटपुट फ़ोल्डर में कॉपी हो गई है। |
| **Underlay path is empty** | DGN अंडरले एम्बेड नहीं है या रेफ़रेंस टूट गया है। | पुष्टि करें कि DWG वास्तव में DGN अंडरले रखता है और बाहरी DGN फ़ाइल सुलभ है। |
| **PDF output is blank** | रास्टराइज़ेशन विकल्प शून्य आकार पर सेट हैं। | `PageWidth`/ `PageHeight` को समायोजित करें या `NoScaling = false` सेट करें। |
| **License exception** | वैध Aspose.CAD लाइसेंस के बिना चल रहा है। | इमेज लोड करने से पहले लाइसेंस लागू करें: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.CAD for .NET को अपने व्यावसायिक प्रोजेक्ट्स में उपयोग कर सकता हूँ?
A1: हाँ, आप उपयोग कर सकते हैं। लाइसेंस विकल्पों के लिए [here](https://purchase.aspose.com/buy) देखें।

### Q2: क्या DWG फ़ाइलों के आकार पर कोई सीमा है जिसे मैं प्रोसेस कर सकता हूँ?
A2: Aspose.CAD बड़े DWG फ़ाइलों को संभाल सकता है, लेकिन हार्डवेयर सीमाएँ लागू हो सकती हैं।

### Q3: क्या कोई ट्रायल संस्करण उपलब्ध है?
A3: हाँ, आप एक मुफ्त ट्रायल [here](https://releases.aspose.com/) प्राप्त कर सकते हैं।

### Q4: मैं अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?
A4: अस्थायी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से प्राप्त किए जा सकते हैं।

### Q5: यदि मुझे समस्याएँ आती हैं तो मैं सहायता कहाँ प्राप्त कर सकता हूँ?
A5: समर्थन के लिए आप Aspose.CAD फ़ोरम [here](https://forum.aspose.com/c/cad/19) पर जा सकते हैं।

**Q: अतिरिक्त PDF मेटाडेटा (लेखक, शीर्षक, आदि) कैसे सेट करूँ?**  
A: `Save` कॉल करने से पहले `exportOptions.Metadata` प्रॉपर्टीज़ का उपयोग करें।

**Q: क्या मैं कई लेआउट को अलग-अलग PDF पेजों में निर्यात कर सकता हूँ?**  
A: हाँ – `CadRasterizationOptions` में `Layouts = new string[] { "Layout1", "Layout2" }` सेट करें।

**Q: क्या Aspose.CAD DWG को अन्य इमेज फ़ॉर्मैट्स में कन्वर्ट करने का समर्थन करता है?**  
A: बिल्कुल। आप PNG, JPEG, SVG, आदि में निर्यात कर सकते हैं, संबंधित `Image.Save` ओवरलोड्स का उपयोग करके।

**अंतिम अपडेट:** 2026-03-21  
**परीक्षित संस्करण:** Aspose.CAD 24.11 for .NET  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}