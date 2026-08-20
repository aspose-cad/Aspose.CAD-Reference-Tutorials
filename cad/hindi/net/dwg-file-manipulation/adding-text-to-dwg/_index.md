---
date: 2026-04-06
description: C# और Aspose.CAD का उपयोग करके DWG को PDF में बदलना और कस्टम टेक्स्ट
  जोड़ना सीखें। यह चरण‑दर‑चरण गाइड DWG से PDF जनरेट करने, टेक्स्ट एंटिटी डालने, और
  DWG टेक्स्ट फ़ॉन्ट बदलने को कवर करता है।
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: C# में DWG फ़ाइलों में टेक्स्ट जोड़ना
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG को PDF में बदलें और C# में टेक्स्ट जोड़ें – Aspose.CAD ट्यूटोरियल
url: /hi/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG को PDF में बदलें और C# में टेक्स्ट जोड़ें – Aspose.CAD ट्यूटोरियल

## परिचय

CAD और .NET विकास की तेज़ गति वाली दुनिया में, **converting DWG to PDF** के साथ कस्टम एनोटेशन डालना एक सामान्य आवश्यकता है। चाहे आपको क्लाइंट्स के लिए प्रिंटेबल ड्रॉइंग्स बनानी हों या DWG में सीधे डायनामिक नोट्स एम्बेड करने हों, Aspose.CAD काम को सरल बनाता है। इस ट्यूटोरियल में आप सीखेंगे कि कैसे **convert DWG to PDF**, **add a text entity**, और यहाँ तक कि C# का उपयोग करके **change DWG text font** किया जाता है।

## त्वरित उत्तर

- **DWG‑to‑PDF रूपांतरण के लिए कौनसी लाइब्रेरी सबसे अच्छी है?** Aspose.CAD for .NET  
- **रूपांतरण के दौरान कस्टम टेक्स्ट जोड़ सकता हूँ?** हाँ – `CadText` एंटिटी बनाकर सहेजने से पहले जोड़ें।  
- **प्रोडक्शन उपयोग के लिए लाइसेंस चाहिए?** एक व्यावसायिक लाइसेंस आवश्यक है; एक मुफ्त ट्रायल उपलब्ध है।  
- **कौनसे .NET संस्करण समर्थित हैं?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **टेक्स्ट फ़ॉन्ट बदलना संभव है?** हाँ, `CadText` की `StyleType` और `TextHeight` जैसी प्रॉपर्टीज़ को समायोजित करें।

## “convert dwg to pdf” क्या है?

DWG फ़ाइल को PDF में बदलने से एक वेक्टर‑आधारित CAD ड्रॉइंग को व्यापक रूप से साझा योग्य, डिवाइस‑स्वतंत्र दस्तावेज़ में परिवर्तित किया जाता है। PDF मूल ज्यामिति और लेयर्स को बरकरार रखता है, साथ ही आपको एनोटेशन, टेक्स्ट या अन्य मेटाडेटा एम्बेड करने की सुविधा देता है। Aspose.CAD स्वचालित रूप से रास्टराइज़ेशन और वेक्टर रेंडरिंग संभालता है, इसलिए सर्वर पर किसी थर्ड‑पार्टी CAD सॉफ़्टवेयर की आवश्यकता नहीं होती।

## रूपांतरण से पहले DWG में टेक्स्ट क्यों जोड़ें?

टेक्स्ट को सीधे DWG में एम्बेड करने से आपको प्लेसमेंट, स्टाइलिंग और लेयर असाइनमेंट पर पूर्ण नियंत्रण मिलता है। जब फ़ाइल बाद में PDF में बदलती है, तो टेक्स्ट ठीक उसी जगह पर दिखाई देता है जहाँ आपने रखा था, जिससे डिज़ाइन इंटेंट बरकरार रहता है और PDF एडिटर में पोस्ट‑प्रोसेसिंग की आवश्यकता नहीं रहती।

## आवश्यकताएँ

- **Aspose.CAD Library** – इसे [डाउनलोड लिंक](https://releases.aspose.com/cad/net/) से डाउनलोड करें।  
- **एक कार्यशील .NET वातावरण** (Visual Studio 2022, .NET 6, या कोई संगत संस्करण)।  
- **आपकी टेस्ट फ़ाइलों के लिए एक फ़ोल्डर** – हम इसे गाइड में `MyDir` कहेंगे।

अब, चलिए प्रक्रिया को चरण‑दर‑चरण देखते हैं।

## नेमस्पेसेस आयात करें

Aspose.CAD क्लासेस तक पहुंचने के लिए आवश्यक `using` स्टेटमेंट्स जोड़ें।

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

अपने स्रोत DWG फ़ाइल को एक `Image` ऑब्जेक्ट में लोड करें। यह ऑब्जेक्ट आपको अंतर्निहित CAD एंटिटीज़ तक पहुंच प्रदान करता है।

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## चरण 2: CadText ऑब्जेक्ट बनाएं (टेक्स्ट एंटिटी डालें)

`CadText` क्लास DWG में एक लाइन टेक्स्ट का प्रतिनिधित्व करती है। यहाँ हम इसकी स्टाइल, वैल्यू, रंग, लेयर और पोज़िशन सेट करते हैं। `StyleType` या `TextHeight` को समायोजित करके **change DWG text font** किया जा सकता है।

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## चरण 3: टेक्स्ट एंटिटी को मॉडल स्पेस में जोड़ें

DWG मॉडल स्पेस अधिकांश ड्रॉइंग एंटिटीज़ को रखता है। हमारे `CadText` को `*Model_Space` ब्लॉक में जोड़ने से टेक्स्ट ड्रॉइंग का हिस्सा बन जाता है।

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## चरण 4: PDF विकल्प कॉन्फ़िगर करें (DWG से PDF उत्पन्न करें)

रास्टराइज़ेशन विकल्प सेट करें जो नियंत्रित करते हैं कि DWG को PDF में कैसे रेंडर किया जाए। आप पेज साइज, ड्रॉ टाइप और लेआउट को समायोजित कर सकते हैं।

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## चरण 5: संशोधित DWG को PDF के रूप में सहेजें

अंत में, संशोधित ड्रॉइंग को एक्सपोर्ट करें। परिणामी PDF में नया जोड़ा गया टेक्स्ट शामिल होगा।

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Pro tip:** यदि आपको उच्च‑रिज़ॉल्यूशन PDF चाहिए, तो `PageHeight` और `PageWidth` को समानुपातिक रूप से बढ़ाएँ।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|--------|-----|
| PDF में टेक्स्ट नहीं दिख रहा है | गलत लेयर या कलर आईडी | सुनिश्चित करें कि `LayerName` मौजूद है और `ColorId` को एक दृश्यमान रंग (जैसे, सफ़ेद के लिए 7) पर सेट किया गया है। |
| टेक्स्ट गलत जगह पर है | असही अलाइनमेंट कॉर्डिनेट्स | ड्रॉइंग की इकाइयों के सापेक्ष `FirstAlignment.X/Y` मानों की जाँच करें। |
| PDF खाली है | रास्टराइज़ेशन विकल्प सेट नहीं हैं | `DrawType` को `UseObjectColor` या `UseObjectLineWeight` पर सेट करें। |

## अक्सर पूछे जाने वाले प्रश्न (Existing)

### Q1: क्या Aspose.CAD सभी DWG फ़ाइल संस्करणों के साथ संगत है?

A1: Aspose.CAD विभिन्न DWG फ़ाइल संस्करणों की एक विस्तृत श्रृंखला का समर्थन करता है, जिससे विभिन्न CAD सॉफ़्टवेयर के साथ संगतता सुनिश्चित होती है।

### Q2: क्या मैं Aspose.CAD का उपयोग करके एक ही DWG फ़ाइल में कई टेक्स्ट एंटिटीज़ जोड़ सकता हूँ?

A2: हाँ, आप ट्यूटोरियल में बताए गए चरणों को दोहराकर DWG फ़ाइल में कई टेक्स्ट एंटिटीज़ जोड़ सकते हैं।

### Q3: Aspose.CAD में टेक्स्ट फ़ॉन्ट और स्टाइल कैसे बदलें?

A3: `CadText` ऑब्जेक्ट की प्रॉपर्टीज़ को समायोजित करके, जैसे `StyleType` और `TextHeight`, आप टेक्स्ट फ़ॉन्ट और स्टाइल बदल सकते हैं, इससे पहले कि इसे DWG फ़ाइल में जोड़ा जाए।

### Q4: व्यावसायिक प्रोजेक्ट में Aspose.CAD उपयोग करने के लिए कोई लाइसेंस संबंधी विचार हैं?

A5: हाँ, Aspose.CAD लाइसेंस शर्तों का पालन सुनिश्चित करें। विवरण के लिए [Aspose.CAD Purchase](https://purchase.aspose.com/buy) देखें।

### Q5: मैं Aspose.CAD‑संबंधित प्रश्नों के लिए मदद या चर्चा कहाँ प्राप्त कर सकता हूँ?

A5: समुदाय से जुड़ने और समर्थन पाने के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

## अतिरिक्त FAQs

**Q: टेक्स्ट जोड़ें बिना DWG से PDF कैसे जनरेट करें?**  
A: `CadText` निर्माण चरण को छोड़ दें और सीधे `PdfOptions` को कॉन्फ़िगर करके `image.Save(...)` कॉल करें।

**Q: क्या मैं प्रोग्रामेटिक रूप से टेक्स्ट का रंग बदल सकता हूँ?**  
A: हाँ, `cadText.ColorId` को एक विशिष्ट ACI कलर नंबर (जैसे, लाल के लिए 1) पर सेट करें।

**Q: मल्टीलाइन टेक्स्ट डालना संभव है?**  
A: मल्टीलाइन टेक्स्ट ब्लॉक्स के लिए `CadMText` का उपयोग करें; तरीका `CadText` जैसा ही है।

**Q: क्या Aspose.CAD कई DWG फ़ाइलों की बैच रूपांतरण का समर्थन करता है?**  
A: बिल्कुल – DWG फ़ाइलों की डायरेक्टरी पर लूप चलाएँ, समान चरण लागू करें, और प्रत्येक को PDF के रूप में सहेजें।

## निष्कर्ष

आपके पास अब एक पूर्ण, प्रोडक्शन‑रेडी वर्कफ़्लो है जिससे आप **DWG को PDF में बदल सकते हैं**, **कस्टम टेक्स्ट जोड़ सकते हैं**, और C# तथा Aspose.CAD का उपयोग करके **टेक्स्ट की उपस्थिति को अनुकूलित** कर सकते हैं। यह तकनीक स्वचालित ड्रॉइंग जनरेशन, रिपोर्टिंग पाइपलाइन, या किसी भी परिदृश्य में उपयोगी है जहाँ आपको CAD फ़ाइलों को तुरंत समृद्ध करने की आवश्यकता होती है।

---

**अंतिम अपडेट:** 2026-04-06  
**परीक्षित संस्करण:** Aspose.CAD 24.11 for .NET  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}