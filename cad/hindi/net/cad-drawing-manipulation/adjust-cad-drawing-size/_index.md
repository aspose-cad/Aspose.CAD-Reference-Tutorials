---
date: 2026-03-19
description: Aspose.CAD के साथ .NET में CAD ड्रॉइंग्स को री‑साइज़ करना सीखें, जिसमें
  CAD ड्रॉइंग यूनिट्स को स्केल करना और लेआउट आकार को समायोजित करना शामिल है। हमारे
  चरण‑दर‑चरण गाइड का पालन करें।
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET के साथ CAD ड्रॉइंग्स को कैसे रिसाइज़ करें
url: /hi/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET के साथ CAD ड्रॉइंग्स को कैसे री-साइज़ करें

## परिचय

यदि आपको अपने .NET एप्लिकेशन से सीधे **CAD को री-साइज़ करने का तरीका** चाहिए, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में हम आपको दिखाएंगे कि कैसे CAD यूनिट सेटिंग्स बदलें, CAD ड्रॉइंग के आयामों को स्केल करें, और Aspose.CAD for .NET का उपयोग करके प्रोग्रामेटिक रूप से CAD आकार को समायोजित करें। गाइड के अंत तक आपके पास किसी भी समर्थित CAD फ़ॉर्मेट को री-साइज़ करने के लिए एक ठोस, प्रोडक्शन‑रेडी समाधान होगा।

## त्वरित उत्तर
- **क्या लाइब्रेरी आवश्यक है?** Aspose.CAD for .NET  
- **क्या मैं यूनिट टाइप बदल सकता हूँ?** हाँ – `CadRasterizationOptions` में `UnitType` सेट करें  
- **क्या प्रोडक्शन के लिए लाइसेंस आवश्यक है?** नॉन‑ट्रायल उपयोग के लिए एक वैध Aspose.CAD लाइसेंस आवश्यक है  
- **उदाहरण किस इमेज फॉर्मेट में एक्सपोर्ट करता है?** BMP (पर कोई भी समर्थित रास्टर फॉर्मेट काम करेगा)  
- **कोड की कितनी लाइन्स?** पूर्ण री-साइज़ ऑपरेशन के लिए 30 लाइनों से कम  

## व्यावहारिक रूप में “CAD को री-साइज़ करने का तरीका” क्या है?
CAD ड्रॉइंग को री-साइज़ करना मतलब वेक्टर डेटा को एक विशिष्ट स्केल या यूनिट (जैसे सेंटीमीटर, इंच) पर रास्टर इमेज में बदलना है। यह तब उपयोगी होता है जब आपको रिपोर्ट में ड्रॉइंग एम्बेड करनी हो, थंबनेल बनाना हो, या CAD विज़ुअल्स को वेब पेज में इंटीग्रेट करना हो।

## Aspose.CAD के साथ CAD आकार को समायोजित क्यों करें?
- **कोई बाहरी CAD सॉफ़्टवेयर नहीं** – सब कुछ आपके .NET कोड के भीतर चलता है।  
- **सूक्ष्म नियंत्रण** यूनिट्स, लेआउट्स, और रास्टराइज़ेशन विकल्पों पर।  
- **क्रॉस‑फ़ॉर्मेट सपोर्ट** – वही कोड DWG, DXF, DWF, आदि के लिए काम करता है।  

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास है:

- Aspose.CAD for .NET लाइब्रेरी: लाइब्रेरी को [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) से डाउनलोड और इंस्टॉल करें।  
- सैंपल CAD ड्रॉइंग: `sample.dwg` जैसी फ़ाइल को आपके प्रोजेक्ट की डॉक्यूमेंट डायरेक्टरी में रखें।  

## नेमस्पेस इम्पोर्ट करें

पहले, उन नेमस्पेस को इम्पोर्ट करें जो आपको Aspose.CAD की क्लासेज़ तक पहुँच प्रदान करते हैं।

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## चरण 1: CAD ड्रॉइंग लोड करें

स्रोत फ़ाइल को एक `Image` ऑब्जेक्ट में लोड करें। यह ऑब्जेक्ट मेमोरी में CAD ड्रॉइंग का प्रतिनिधित्व करता है और आगे की सभी ऑपरेशन्स की आधारशिला होगा।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## चरण 2: BmpOptions बनाएं (या कोई अन्य रास्टर फ़ॉर्मेट)

`BmpOptions` Aspose.CAD को बताता है कि जब आप इसे बिटमैप के रूप में सेव करते हैं तो वेक्टर डेटा को कैसे रेंडर करना है। आप इसे अपने लक्षित फ़ॉर्मेट के अनुसार `PngOptions`, `JpegOptions` आदि से बदल सकते हैं।

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## चरण 3: CadRasterizationOptions सेट करें

`CadRasterizationOptions` स्केलिंग, यूनिट रूपांतरण, और लेआउट चयन के मुख्य सेटिंग्स रखता है। इसे `BmpOptions` की `VectorRasterizationOptions` प्रॉपर्टी से लिंक करने से रास्टराइज़र आपके कस्टम सेटिंग्स का उपयोग करता है।

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## चरण 4: UnitType सेट करें (CAD यूनिट बदलें)

यहाँ हम CAD यूनिट को उसके डिफ़ॉल्ट से सेंटीमीटर में बदलते हैं। यही वह जगह है जहाँ **change cad unit** कीवर्ड स्थित है, और यह सीधे अंतिम इमेज आकार को प्रभावित करता है।

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## चरण 5: लेआउट चुनें (CAD लेआउट सेट करें)

यदि आपके ड्रॉइंग में कई लेआउट्स (जैसे Model, Sheet1) हैं, तो निर्दिष्ट करें कि आप किन्हें रास्टराइज़ करना चाहते हैं। सही लेआउट का चयन करना आवश्यक है जब आप **set cad layouts** के साथ री-साइज़्ड आउटपुट बनाते हैं।

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## चरण 6: BMP में एक्सपोर्ट करें (CAD ड्रॉइंग री-साइज़ करें)

अंत में, रास्टराइज़्ड इमेज को सेव करें। आउटपुट फ़ाइल आपके द्वारा कॉन्फ़िगर किए गए नए आकार, यूनिट, और लेआउट को दर्शाती है—जिससे **resize CAD drawing** ऑपरेशन प्रभावी रूप से पूरा हो जाता है।

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

अब आपके पास एक BMP फ़ाइल है जो री-साइज़्ड CAD ड्रॉइंग को दर्शाती है, आगे की प्रोसेसिंग या डिस्प्ले के लिए तैयार है।

## सामान्य समस्याएँ और समाधान

| समस्या | क्यों होता है | समाधान |
|--------|--------------|--------|
| आउटपुट धुंधला है | डिफ़ॉल्ट रूप से कम DPI (डॉट्स पर इंच) | सेव करने से पहले `cadRasterizationOptions.Resolution = 300;` सेट करें |
| गलत लेआउट दिख रहा है | लेआउट नाम में टाइपो | CAD व्यूअर या `Layouts` कलेक्शन का उपयोग करके सटीक लेआउट नाम की जाँच करें |
| यूनिट रूपांतरण गलत दिख रहा है | मीट्रिक और इम्पीरियल यूनिट्स का मिश्रण | `UnitType` को इच्छित माप प्रणाली से मेल खाने के लिए सुनिश्चित करें |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD for .NET सभी CAD फ़ॉर्मेट्स के साथ संगत है?

A1: Aspose.CAD for .NET DWG, DXF, DWF और कई अन्य सहित व्यापक रेंज के CAD फ़ॉर्मेट्स को सपोर्ट करता है। पूरी सूची के लिए [documentation](https://reference.aspose.com/cad/net/) देखें।

### Q2: क्या मैं एक साथ कई लेआउट्स को री-साइज़ कर सकता हूँ?

A2: हाँ, आप `CadRasterizationOptions` में `Layouts` एरे को समायोजित करके कई लेआउट्स को री-साइज़ कर सकते हैं।

### Q3: Aspose.CAD for .NET के लिए समर्थन कहाँ प्राप्त कर सकता हूँ?

A3: समुदाय समर्थन और सहायता के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

### Q4: क्या कोई फ्री ट्रायल उपलब्ध है?

A4: हाँ, आप Aspose.CAD for .NET की सुविधाओं का मूल्यांकन करने के लिए एक [free trial](https://releases.aspose.com/) एक्सप्लोर कर सकते हैं।

### Q5: Aspose.CAD for .NET के लिए अस्थायी लाइसेंस कैसे प्राप्त करें?

A5: परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से प्राप्त करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q: CAD ड्रॉइंग को यूनिट टाइप बदले बिना कैसे स्केल करूँ?**  
A: `CadRasterizationOptions` की `Zoom` प्रॉपर्टी को समायोजित करें (उदा., `cadRasterizationOptions.Zoom = 2.0;`) ताकि मूल यूनिट रखे हुए आकार दोगुना हो जाए।

**Q: क्या मैं BMP के अलावा अन्य फ़ॉर्मेट्स में एक्सपोर्ट कर सकता हूँ?**  
A: बिल्कुल। `BmpOptions` को `PngOptions`, `JpegOptions` या किसी भी अन्य समर्थित रास्टर फ़ॉर्मेट क्लास से बदल दें।

**Q: क्या ड्रॉइंग्स के फ़ोल्डर को बैच‑प्रोसेस करना संभव है?**  
A: हाँ। डायरेक्टरी में फ़ाइलों पर लूप चलाएँ, समान रास्टराइज़ेशन लॉजिक लागू करें, और प्रत्येक आउटपुट को एक अनूठे नाम से सेव करें।

---

**अंतिम अपडेट:** 2026-03-19  
**परिक्षण किया गया:** Aspose.CAD for .NET 24.11 (लेखन के समय नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}