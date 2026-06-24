---
date: 2026-04-06
description: Aspose.CAD का उपयोग करके C# में DWF को JPG में कैसे बदलें सीखें और DWG
  फ़ाइलों से DWF लेआउट आकार निकालने का तरीका जानें।
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: C# में DWG फ़ाइलों के साथ काम करना - DWF लेआउट का आकार प्राप्त करें
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: C# में DWF को JPG में बदलें – DWG से DWF लेआउट आकार प्राप्त करें
url: /hi/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWF को JPG में C# के साथ परिवर्तित करें – DWG से DWF लेआउट आकार प्राप्त करें

## परिचय

यदि आपको **DWF को JPG में परिवर्तित** करना है और साथ ही सटीक लेआउट आयाम पता करने हैं, तो आप सही जगह पर हैं। इस ट्यूटोरियल में हम एक पूर्ण, एंड‑टू‑एंड उदाहरण के माध्यम से दिखाएंगे कि कैसे Aspose.CAD for .NET का उपयोग करके DWG‑आधारित DWF फ़ाइल को खोलें, प्रत्येक लेआउट का आकार पढ़ें, और लेआउट को उच्च‑गुणवत्ता वाले JPG इमेज के रूप में सहेजें। अंत तक आप न केवल DWF लेआउट जानकारी निकालना जानेंगे बल्कि कोई भी C# प्रोजेक्ट में डालने योग्य पुन: उपयोग योग्य कोड स्निपेट भी प्राप्त करेंगे।

## त्वरित उत्तर
- **“convert DWF to JPG” का क्या अर्थ है?** इसका मतलब है कि एक वेक्टर DWF लेआउट को बिटमैप JPEG छवि में रास्टराइज़ करना।  
- **लेआउट आकार पहले क्यों पढ़ें?** सटीक विस्तार को जानने से आप सही पेज आयाम सेट कर सकते हैं, जिससे खिंची या कट हुई आउटपुट से बचा जा सके।  
- **यह कार्य कौन सी लाइब्रेरी संभालती है?** Aspose.CAD for .NET DWG, DWF और रास्टर इमेज रूपांतरण के लिए पूर्ण समर्थन प्रदान करती है।  
- **क्या मुझे लाइसेंस चाहिए?** मूल्यांकन के लिए एक अस्थायी लाइसेंस काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **कौन से .NET संस्करण समर्थित हैं?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7।

## “convert DWF to JPG” क्या है और यह क्यों महत्वपूर्ण है?

DWF (Design Web Format) फ़ाइल को JPG में बदलने से एक पोर्टेबल इमेज बनती है जिसे ब्राउज़र में दिखाया जा सकता है, रिपोर्ट में एम्बेड किया जा सकता है, या उन स्टेकहोल्डर्स के साथ साझा किया जा सकता है जिनके पास CAD सॉफ़्टवेयर नहीं है। यह रूपांतरण आपको मानक इमेज‑प्रोसेसिंग टूल्स का उपयोग करके छवि को (रिसाइज़, कॉम्प्रेस, वॉटरमार्क) बदलने की लचीलापन भी देता है।

## DWF लेआउट आकार क्यों निकालें?

एक DWF फ़ाइल में कई लेआउट हो सकते हैं, प्रत्येक का अपना कोऑर्डिनेट सिस्टम और इकाइयाँ (इंच, मिलीमीटर आदि) होती हैं। लेआउट आकार निकालने से आप:

1. रास्टराइज़ करते समय मूल अनुपात को बनाए रख सकते हैं।  
2. हाई‑रेज़ोल्यूशन आउटपुट के लिए सही DPI चुन सकते हैं।  
3. कई लेआउट्स की बैच प्रोसेसिंग को मैन्युअल ट्यूनिंग के बिना स्वचालित कर सकते हैं।

## पूर्वापेक्षाएँ

इस ट्यूटोरियल को बिना रुकावट के फॉलो करने के लिए सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- Aspose.CAD for .NET: सुनिश्चित करें कि आपके पास Aspose.CAD for .NET स्थापित है। आप इसे [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) से डाउनलोड कर सकते हैं।

लाइब्रेरी तैयार होने से आप कोड पर ध्यान केंद्रित कर सकते हैं, न कि निर्भरताओं की खोज पर।

## नेमस्पेस आयात करें

कोड लिखना शुरू करने से पहले आवश्यक नेमस्पेस आयात करें। ये नेमस्पेस उन क्लासेज़ को प्रदान करेंगे जिनकी हमें CAD फ़ाइलों, रास्टराइज़ेशन विकल्पों और फ़ाइल I/O के साथ काम करने के लिए आवश्यकता होगी।

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## चरण 1: अपना वातावरण सेट करें

एक नया C# कंसोल या क्लास‑लाइब्रेरी प्रोजेक्ट बनाएं, **Aspose.CAD.dll** का रेफ़रेंस जोड़ें, और सुनिश्चित करें कि प्रोजेक्ट एक संगत .NET संस्करण को टार्गेट करता है।

## चरण 2: फ़ाइल पथ निर्धारित करें (DWF निकालने का तरीका)

निर्दिष्ट करें कि आपका स्रोत DWF फ़ाइल कहाँ स्थित है और उत्पन्न JPG फ़ाइलें कहाँ लिखी जाएँगी।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Pro tip:** विभिन्न OS पर सुरक्षित पाथ हैंडलिंग के लिए `Path.Combine(MyDir, "blocks_and_tables.dwf")` का उपयोग करें।

## चरण 3: DWF इमेज लोड करें

DWF फ़ाइल को `Aspose.CAD.Image` ऑब्जेक्ट में लोड करें। हमें इसे `DwfImage` में कास्ट करना है क्योंकि हमें पेज‑स्पेसिफिक प्रॉपर्टीज़ तक पहुंच चाहिए।

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## चरण 4: पेजों पर इटररेट करें

एक DWF में कई पेज (लेआउट) हो सकते हैं। प्रत्येक को लूप करें ताकि हम उन्हें व्यक्तिगत रूप से प्रोसेस कर सकें।

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## चरण 5: लेआउट जानकारी प्राप्त करें

लूप के अंदर, लेआउट का नाम प्राप्त करें। यह नाम लॉगिंग और आउटपुट JPG फ़ाइल के नामकरण दोनों के लिए उपयोग होगा।

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## चरण 6: JPG विकल्प सेट करें

एक `JpegOptions` इंस्टेंस बनाएं और रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें। `Layouts` प्रॉपर्टी Aspose.CAD को बताती है कि कौन सा लेआउट रेंडर करना है।

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## चरण 7: पेज आकार निर्धारित करें (dwg को jpg में बदलें)

लेआउट की चौड़ाई और ऊँचाई को उसकी मूल इकाइयों में गणना करें। यह जानकारी रास्टर पेज आकार को सही ढंग से सेट करने के लिए आवश्यक है।

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## चरण 8: पेज आयाम सेट करें

Aspose.CAD द्वारा प्रदान किए गए हेल्पर मेथड्स का उपयोग करके मूल इकाइयों (इंच या मिलीमीटर) को पिक्सेल में बदलें। यदि इकाई प्रकार इनमें से कोई नहीं है, तो हम कच्चे मानों का उपयोग करेंगे।

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## चरण 9: JPG फ़ाइल सहेजें

अंत में, रास्टराइज़ेशन विकल्पों को JPEG विकल्पों से बाइंड करें और इमेज को डिस्क पर सहेजें।

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

जब लूप समाप्त हो जाएगा, आपके पास प्रत्येक लेआउट के लिए एक JPG फ़ाइल होगी, जो मूल DWF आयामों से बिल्कुल मेल खाती होगी।

## सामान्य समस्याएँ और समाधान

| लक्षण | संभावित कारण | समाधान |
|--------|--------------|----------|
| खाली JPG आउटपुट | `options.Layouts` सही तरीके से सेट नहीं है | `page.Name` से मिलते हुए लेआउट नाम की जाँच करें। |
| विकृत छवि | गलत DPI रूपांतरण | रूपांतरण से पहले `CommonHelper.DPI = 300` (या आपका लक्ष्य DPI) उपयोग करें। |
| फ़ाइल नहीं मिली | गलत `MyDir` पथ | एब्सोल्यूट पाथ या `Path.Combine` का उपयोग करें। |
| लाइसेंस अपवाद | कोई लाइसेंस लागू नहीं किया गया | `Image.Load` कॉल करने से पहले अस्थायी या स्थायी लाइसेंस लोड करें। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD नवीनतम DWG फ़ाइल स्वरूपों के साथ संगत है?

A1: Aspose.CAD विभिन्न DWG फ़ाइल स्वरूपों का समर्थन करता है, जिसमें नवीनतम संस्करण भी शामिल हैं। विशिष्ट संगतता विवरण के लिए [documentation](https://reference.aspose.com/cad/net/) देखें।

### Q2: क्या मैं Aspose.CAD को व्यावसायिक और व्यक्तिगत दोनों प्रोजेक्ट्स में उपयोग कर सकता हूँ?

A2: हाँ, Aspose.CAD व्यावसायिक और व्यक्तिगत दोनों उपयोग के लिए लचीले लाइसेंस विकल्प प्रदान करता है। अधिक विवरण के लिए [purchase page](https://purchase.aspose.com/buy) देखें।

### Q3: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?

A3: आप मूल्यांकन उद्देश्यों के लिए [here](https://purchase.aspose.com/temporary-license/) से अस्थायी लाइसेंस प्राप्त कर सकते हैं।

### Q4: मैं Aspose.CAD के लिए समर्थन कहाँ पा सकता हूँ?

A4: किसी भी प्रश्न या सहायता के लिए, [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

### Q5: क्या Aspose.CAD के लिए मुफ्त ट्रायल उपलब्ध है?

A5: हाँ, आप Aspose.CAD का मुफ्त ट्रायल संस्करण [here](https://releases.aspose.com/) से एक्सेस कर सकते हैं।

### Q6: मैं DWF निकालने से पहले DWG फ़ाइल को सीधे JPG में कैसे बदल सकता हूँ?

A6: आप `Aspose.CAD.Image.Load` से DWG फ़ाइल लोड कर सकते हैं और वही रास्टराइज़ेशन वर्कफ़्लो उपयोग कर सकते हैं; बस `options.Layouts` को DWG से इच्छित लेआउट नाम(s) पर सेट करें।

### Q7: क्या रूपांतरण वेक्टर गुणवत्ता को बनाए रखता है?

A7: एक बार JPG में रास्टराइज़ होने पर, इमेज बिटमैप‑आधारित हो जाती है, इसलिए वेक्टर स्केलेबिलिटी खो जाती है। लॉसलेस स्केलिंग के लिए PNG या SVG में एक्सपोर्ट करने पर विचार करें।

---

**अंतिम अपडेट:** 2026-04-06  
**परीक्षण किया गया:** Aspose.CAD 24.11 for .NET  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}