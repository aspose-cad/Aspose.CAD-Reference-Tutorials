---
description: Aspose.CAD for .NET का उपयोग करके DWG को PNG में बदलना और DWG फ़ाइलों
  से OLE ऑब्जेक्ट निकालना सीखें – एक तेज़, कोड‑केंद्रित गाइड।
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG को PNG में बदलें और OLE ऑब्जेक्ट्स निर्यात करें - Aspose.CAD ट्यूटोरियल
url: /hi/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporting OLE Objects from DWG Files - Aspose.CAD Tutorial

## Introduction

यदि आपको **DWG को PNG में बदलने** के साथ-साथ एम्बेडेड OLE ऑब्जेक्ट्स को निकालना है, तो आप सही जगह पर आए हैं। Aspose.CAD for .NET इस दो‑स्टेप प्रक्रिया को सरल बनाता है, जिससे आप कुछ ही लाइनों के C# कोड में एक्सट्रैक्शन और रास्टराइज़ेशन को ऑटोमेट कर सकते हैं। अगले कुछ मिनटों में हम पूरे वर्कफ़्लो को देखेंगे, पर्यावरण सेटअप से लेकर प्रत्येक DWG को PNG के रूप में सेव करने तक, जिसमें निकाले गए OLE डेटा शामिल होगा।

## Quick Answers
- **यह ट्यूटोरियल क्या कवर करता है?** Aspose.CAD for .NET का उपयोग करके DWG को PNG में बदलना और OLE ऑब्जेक्ट्स को एक्सट्रैक्ट करना।  
- **क्या मुझे लाइसेंस चाहिए?** विकास के लिए एक फ्री ट्रायल काम करता है; प्रोडक्शन के लिए कमर्शियल लाइसेंस आवश्यक है।  
- **कौन से .NET संस्करण समर्थित हैं?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+।  
- **क्या मैं एक साथ कई DWG फ़ाइलों को प्रोसेस कर सकता हूँ?** हाँ – सैंपल फ़ाइल नामों की एक एरे पर लूप करता है।  
- **और उदाहरण कहाँ मिलेंगे?** नीचे दिए गए आधिकारिक Aspose.CAD दस्तावेज़ और फ़ोरम लिंक देखें।

## What is **convert DWG to PNG**?
DWG (AutoCAD ड्राइंग) को PNG इमेज में बदलना वेक्टर डेटा को रास्टराइज़ करता है, जिससे इसे वेब पेज, रिपोर्ट या अन्य एप्लिकेशन में देखना या एम्बेड करना आसान हो जाता है जो मूल रूप से DWG को सपोर्ट नहीं करते। जब OLE ऑब्जेक्ट्स मौजूद होते हैं, तो उन्हें कन्वर्ज़न के दौरान अलग-अलग एसेट्स के रूप में एक्सट्रैक्ट किया जा सकता है।

## Why extract OLE objects from CAD files?
कई DWG ड्रॉइंग्स स्प्रेडशीट, चार्ट या अन्य Office दस्तावेज़ों को OLE ऑब्जेक्ट्स के रूप में एम्बेड करती हैं। उन्हें एक्सट्रैक्ट करने से आप मूल डेटा को पुन: उपयोग कर सकते हैं, रिपोर्टिंग को ऑटोमेट कर सकते हैं, या एम्बेडेड जानकारी खोए बिना कंटेंट को नए फ़ॉर्मेट में माइग्रेट कर सकते हैं।

## Prerequisites

- Aspose.CAD for .NET Library: सुनिश्चित करें कि लाइब्रेरी इंस्टॉल है। आप इसे [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) से डाउनलोड कर सकते हैं।
- Document Directory: वह डायरेक्टरी सेट करें जहाँ आपके DWG फ़ाइलें संग्रहीत हैं। प्रदान किए गए कोड स्निपेट में `"Your Document Directory"` को वास्तविक पाथ से बदलें।

## Import Namespaces

In your .NET project, import the required namespaces:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Step‑by‑Step Guide

### Step 1: Set the Document Directory

```csharp
string MyDir = "Your Document Directory";
```

`"Your Document Directory"` को उस पाथ से बदलें जहाँ आपके DWG फ़ाइलें स्थित हैं।

### Step 2: List the DWG files you want to process

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Step 3: Configure export options for PNG conversion

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

आप `CadRasterizationOptions` (जैसे `PageWidth`, `PageHeight`, `BackgroundColor`) को अपनी इच्छित आउटपुट रिज़ॉल्यूशन के अनुसार समायोजित कर सकते हैं।

### Step 4: Iterate through each DWG and perform the conversion

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

इस लूप के दौरान लाइब्रेरी स्वचालित रूप से प्रत्येक ड्राइंग में एम्बेडेड **OLE ऑब्जेक्ट्स** को एक्सट्रैक्ट करती है और उत्पन्न PNG में शामिल करती है। यदि आपको रॉ OLE स्ट्रीम चाहिए, तो आप `cadImage.OleObjects` कलेक्शन तक पहुँच सकते हैं – यह प्रोग्रामेटिक रूप से **how to extract ole** डेटा प्राप्त करने का एक सुविधाजनक तरीका है।

## Common Issues & Troubleshooting

- **Missing layout name** – सुनिश्चित करें कि आप जिस लेआउट (`"Layout1"` उदाहरण में) को निर्दिष्ट कर रहे हैं, वह स्रोत DWG में मौजूद है; अन्यथा रास्टराइज़र डिफ़ॉल्ट मॉडल स्पेस पर फॉल बैक करता है।
- **Large files cause memory pressure** – फ़ाइलों को एक‑एक करके प्रोसेस करें (जैसा दिखाया गया है) और `using` के साथ `CadImage` ऑब्जेक्ट्स को तुरंत डिस्पोज़ करें।
- **Unexpected colors** – यदि ट्रांसपेरेंसी चाहिए तो `rasterizationOptions.BackgroundColor` को ड्राइंग के बैकग्राउंड के अनुसार सेट करें।

## Frequently Asked Questions

### Q1: Is Aspose.CAD for .NET suitable for both junior and senior CAD files?
A1: Yes, Aspose.CAD for .NET is versatile and can handle a wide range of CAD files, including both junior and senior variants.

### Q2: Can I customize export options for different layouts?
A2: Absolutely! As shown in the tutorial, you can tailor export options, including layouts, to suit your specific needs.

### Q3: Where can I find detailed documentation for Aspose.CAD for .NET?
A3: Explore the [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/) for in‑depth information and examples.

### Q4: Is there a free trial available?
A4: Yes, you can experience the capabilities of Aspose.CAD for .NET with a free trial. Visit [this link](https://releases.aspose.com/) to get started.

### Q5: How can I get support or connect with the community?
A5: For support and community engagement, visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q6: How do I **extract OLE from CAD** files without converting to PNG?
A6: Use the `CadImage.OleObjects` collection after loading the DWG; you can iterate through each `OleObject` and save its raw data to a file.

## Conclusion

आपने अब देखा कि कैसे **DWG को PNG में बदलते** हुए सहजता से **OLE ऑब्जेक्ट्स को एक्सट्रैक्ट** किया जा सकता है Aspose.CAD for .NET का उपयोग करके। यह तरीका समय बचाता है, मैन्युअल कॉपी‑पेस्ट चरणों को समाप्त करता है, और ऑटोमेटेड पाइपलाइन में साफ़-सुथरे ढंग से इंटीग्रेट होता है। अन्य रास्टर फ़ॉर्मेट (JPEG, BMP) के साथ प्रयोग करने या Aspose द्वारा प्रदान किए गए समृद्ध CAD मैनीपुलेशन फीचर्स को एक्सप्लोर करने में संकोच न करें।

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}