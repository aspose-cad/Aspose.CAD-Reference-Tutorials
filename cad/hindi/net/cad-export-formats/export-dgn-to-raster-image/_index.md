---
date: 2026-03-24
description: Aspose.CAD for .NET का उपयोग करके dgn को png में बदलना और cad को jpeg
  के रूप में सहेजना सीखें – CAD से इमेज रूपांतरण के लिए एक त्वरित गाइड।
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET में DGN को PNG में कैसे बदलें
url: /hi/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET में DGN को PNG में बदलें

आधुनिक .NET विकास में, **convert dgn to png** एक सामान्य आवश्यकता है जब आपको वेब पर CAD ड्रॉइंग्स दिखाने या रिपोर्ट में एम्बेड करने की जरूरत होती है। Aspose.CAD for .NET इस रूपांतरण को सरल बनाता है, जिससे आप कुछ ही कोड लाइनों के साथ DGN फ़ाइल को उच्च‑गुणवत्ता वाले रास्टर इमेज में बदल सकते हैं। इस गाइड में हम पूरी प्रक्रिया को कवर करेंगे, प्रोजेक्ट सेटअप से लेकर अंतिम PNG (या JPEG) फ़ाइल को सेव करने तक।

## Quick Answers
- **क्या मैं Aspose.CAD के साथ DGN को PNG में बदल सकता हूँ?** हाँ – केवल रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें और PNG या JPEG आउटपुट चुनें।  
- **उत्पादन उपयोग के लिए लाइसेंस चाहिए?** गैर‑ट्रायल डिप्लॉयमेंट के लिए वैध Aspose.CAD लाइसेंस आवश्यक है।  
- **कौन से .NET संस्करण समर्थित हैं?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7।  
- **कौन से इमेज फ़ॉर्मेट उपलब्ध हैं?** PNG, JPEG, BMP, GIF, TIFF, और अधिक।  
- **क्या एक्सेप्शन हैंडलिंग आवश्यक है?** बिल्कुल – फ़ाइल‑एक्सेस समस्याओं को संभालने के लिए try/catch में रूपांतरण को रैप करें।

## What is “convert dgn to png”?
DGN (MicroStation) फ़ाइल को PNG में बदलना मतलब वेक्टर CAD डेटा को पिक्सेल‑आधारित इमेज में रास्टराइज़ करना है। यह प्रीव्यू जनरेशन, HTML ई‑मेल में ड्रॉइंग एम्बेड करने, या डॉक्यूमेंट मैनेजमेंट सिस्टम के लिए थंबनेल बनाने में उपयोगी है।

## Why use Aspose.CAD for CAD to image conversion?
- **कोई बाहरी निर्भरताएँ नहीं** – पूरी तरह से मैनेज्ड कोड में काम करता है।  
- **उच्च फ़िडेलिटी** – लाइन वेट, लेयर्स, और रंगों को बरकरार रखता है।  
- **लचीला आउटपुट** – एक ही विकल्प बदलकर PNG, JPEG, BMP आदि में स्विच कर सकते हैं।  
- **परफ़ॉर्मेंस‑ऑप्टिमाइज़्ड** – बड़े ड्रॉइंग्स के लिए भी रास्टराइज़ेशन तेज़ है।

## Prerequisites

शुरू करने से पहले सुनिश्चित करें कि आपके पास है:

- **Aspose.CAD for .NET** आपके प्रोजेक्ट में इंस्टॉल हो। आप इसे [website](https://reference.aspose.com/cad/net/) से डाउनलोड कर सकते हैं।  
- एक सैंपल DGN फ़ाइल (जैसे `Nikon_D90_Camera.dgn`) जिसे आप किसी ज्ञात डायरेक्टरी में रखेंगे।

## Import Namespaces

आवश्यक `using` स्टेटमेंट्स जोड़ें ताकि आप Aspose.CAD क्लासेस तक पहुँच सकें।

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step 1: Load the DGN File

स्रोत DGN को `CadImage` ऑब्जेक्ट में लोड करें। यह ऑब्जेक्ट मेमोरी में CAD ड्रॉइंग का प्रतिनिधित्व करता है और रास्टराइज़ेशन का स्रोत होगा।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Step 2: Define Rasterization Options

CAD ड्रॉइंग को कैसे रास्टराइज़ किया जाना चाहिए, इसे कॉन्फ़िगर करें। यहाँ आप इमेज साइज, स्केलिंग, और बैकग्राउंड कलर नियंत्रित कर सकते हैं।

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Step 3: Choose the Output Format (PNG or JPEG)

हालाँकि ट्यूटोरियल PNG पर केंद्रित है, आप **save cad as jpeg** भी कर सकते हैं। उपयुक्त इमेज ऑप्शन ऑब्जेक्ट बनाएं और रास्टराइज़ेशन सेटिंग्स को अटैच करें।

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** PNG फ़ाइल जनरेट करने के लिए `new JpegOptions()` को `new PngOptions()` से बदलें।

## Step 4: Save the Raster Image

अंत में, `CadImage` इंस्टेंस पर `Save` कॉल करें, इच्छित फ़ाइल नाम और कॉन्फ़िगर किए गए ऑप्शन ऑब्जेक्ट को पास करें।

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

यदि आप `PngOptions` पर स्विच करते हैं, तो फ़ाइल `ExportDGNToRasterImage_out.png` के रूप में सेव होगी।

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| **Blank output image** | `NoScaling` गलत सेट है या लेआउट चयनित नहीं है | `AutomaticLayoutsScaling = true` सेट करें या इच्छित लेआउट निर्दिष्ट करें। |
| **Out‑of‑memory for large files** | बिना स्ट्रीमिंग के बड़े DGN को लोड करना | `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })` उपयोग करें। |
| **Unsupported DGN version** | पुराने MicroStation संस्करण | सुनिश्चित करें कि आपके पास लेगेसी फ़ॉर्मेट्स को सपोर्ट करने वाला नवीनतम Aspose.CAD संस्करण है। |

## Frequently Asked Questions

**Q: क्या मैं DGN फ़ाइलों को JPEG के अलावा अन्य फ़ॉर्मेट में एक्सपोर्ट कर सकता हूँ?**  
A: हाँ, Aspose.CAD for .NET PNG, BMP, GIF, TIFF, और अधिक को सपोर्ट करता है – बस ऑप्शन क्लास को बदलें (जैसे `new PngOptions()`)।

**Q: रूपांतरण के दौरान एक्सेप्शन को कैसे हैंडल करूँ?**  
A: रूपांतरण कोड को `try/catch` ब्लॉक में रैप करें और विस्तृत त्रुटि जानकारी के लिए `Aspose.CAD.CadException` को लॉग करें।

**Q: क्या Aspose.CAD for .NET का ट्रायल वर्ज़न उपलब्ध है?**  
A: हाँ, आप मुफ्त ट्रायल के साथ प्रोडक्ट का परीक्षण कर सकते हैं। अधिक जानकारी के लिए [here](https://releases.aspose.com/) देखें।

**Q: Aspose.CAD for .NET से संबंधित सहायता या मुद्दों पर चर्चा कहाँ करूँ?**  
A: समुदाय समर्थन और चर्चा के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

**Q: Aspose.CAD for .NET के लिए टेम्पररी लाइसेंस कैसे प्राप्त करूँ?**  
A: अपने विकास आवश्यकताओं के लिए टेम्पररी लाइसेंस प्राप्त करने हेतु [this link](https://purchase.aspose.com/temporary-license/) देखें।

## Conclusion

आपने अब **convert dgn to png** (या JPEG) को Aspose.CAD for .NET का उपयोग करके कैसे किया, सीख लिया है। रास्टराइज़ेशन विकल्पों को समायोजित करके और इमेज‑ऑप्शन क्लास को बदलकर आप आउटपुट को किसी भी प्रोजेक्ट की आवश्यकता के अनुसार कस्टमाइज़ कर सकते हैं। विभिन्न पेज साइज, DPI सेटिंग्स, और फ़ाइल फ़ॉर्मेट के साथ प्रयोग करने में संकोच न करें ताकि आपके एप्लिकेशन के लिए परफेक्ट रास्टर इमेज प्राप्त हो सके।

---

**Last Updated:** 2026-03-24  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}