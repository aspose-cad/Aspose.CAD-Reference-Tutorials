---
date: 2026-03-13
description: Aspose.CAD for .NET का उपयोग करके CAD रास्टराइज़ेशन विकल्प सेट करना और
  विशिष्ट DWG लेआउट को PDF में निर्यात करना सीखें – CAD फ़ाइल से PDF बनाने के लिए
  अंतिम मार्गदर्शिका।
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD रास्टराइज़ेशन विकल्प सेट करें – विशिष्ट लेआउट को PDF में निर्यात करें -
  Aspose.CAD गाइड
url: /hi/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

Let's craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF में विशिष्ट लेआउट निर्यात करना - Aspose.CAD गाइड

## Introduction

इस ट्यूटोरियल में आप **CAD रास्टराइज़ेशन विकल्प कैसे सेट करें** यह जानेंगे ताकि आप DWG फ़ाइल से एकल लेआउट—या कई लेआउट—को सीधे PDF में निर्यात कर सकें। Aspose.CAD for .NET *dwg to pdf conversion c#* प्रक्रिया को सरल बनाता है, जिससे आप पेज आकार, रिज़ॉल्यूशन और लेआउट चयन पर पूर्ण नियंत्रण प्राप्त कर सकते हैं। गाइड के अंत तक आप केवल कुछ लाइनों के कोड से **CAD फ़ाइल से PDF बनाना** सीख जाएंगे।

## Quick Answers
- **“set cad rasterization options” क्या करता है?**  
  यह Aspose.CAD को बताता है कि वेक्टर डेटा (लेआउट, लेयर, लाइन वेट) को रास्टराइज़्ड PDF पेजों में कैसे रेंडर किया जाए।  
- **कौन सा मेथड DWG लेआउट को PDF में निर्यात करता है?**  
  `Image.Save` का उपयोग करें, जिसमें एक कॉन्फ़िगर किया गया `PdfOptions` हो जिसमें आपका `CadRasterizationOptions` शामिल हो।  
- **क्या मैं एक साथ एक से अधिक लेआउट निर्यात कर सकता हूँ?**  
  हाँ – `Layouts` प्रॉपर्टी में लेआउट नामों की एक एरे प्रदान करें।  
- **उत्पादन उपयोग के लिए क्या मुझे लाइसेंस चाहिए?**  
  एक व्यावसायिक लाइसेंस आवश्यक है; मूल्यांकन के लिए एक फ्री ट्रायल उपलब्ध है।  
- **कौन से .NET संस्करण समर्थित हैं?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 और उसके बाद के संस्करण।

## What is “set cad rasterization options”?

`CadRasterizationOptions` वह क्लास है जो नियंत्रित करती है कि CAD एंटिटीज़ को PDF जैसे रास्टर‑बेस्ड फ़ॉर्मेट में बदलते समय कैसे रास्टराइज़ किया जाए। इसके प्रॉपर्टीज़—पेज डायमेंशन, लेआउट चयन, बैकग्राउंड कलर आदि—को कॉन्फ़िगर करके आप **export dwg layout to pdf** ऑपरेशन के विज़ुअल आउटपुट को निर्धारित करते हैं।

## Why set CAD rasterization options?

- **Precision** – मूल CAD ड्रॉइंग में जैसा दिखता है, लाइन वेट और स्केल को बिल्कुल वैसा ही संरक्षित रखें।  
- **Performance** – केवल वही लेआउट रेंडर करें जिसकी आपको आवश्यकता है, जिससे फ़ाइल आकार और प्रोसेसिंग समय कम हो जाता है।  
- **Flexibility** – पेज की चौड़ाई/ऊँचाई, DPI, और बैकग्राउंड को अपने रिपोर्टिंग मानकों के अनुसार समायोजित करें।  

## Prerequisites

कोड में जाने से पहले सुनिश्चित करें कि आपके पास है:

- **Aspose.CAD for .NET** स्थापित। आप इसे [here](https://releases.aspose.com/cad/net/) से डाउनलोड कर सकते हैं।  
- एक .NET विकास वातावरण (Visual Studio, VS Code, या कोई भी पसंदीदा IDE)।  
- एक DWG फ़ाइल जिसमें कम से कम एक लेआउट हो (यहाँ उपयोग की गई सैंपल फ़ाइल `visualization_-_conference_room.dwg` है)।

## Import Namespaces

अपने .NET प्रोजेक्ट में Aspose.CAD के लिए आवश्यक नेमस्पेसेस इम्पोर्ट करें:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG file

पहले, Aspose.CAD को उस स्रोत DWG फ़ाइल की ओर इंगित करें जिसे आप कन्वर्ट करना चाहते हैं।

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Step 2: Set **CadRasterizationOptions**

यहाँ हम रास्टराइज़ेशन सेटिंग्स को कॉन्फ़िगर करते हैं जो PDF पेज का आकार और रिज़ॉल्यूशन निर्धारित करती हैं।

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Pro tip:** `PageWidth` और `PageHeight` को अपने लक्ष्य PDF लेआउट के आयामों के अनुसार समायोजित करें। बड़े मान विवरण बढ़ाते हैं लेकिन फ़ाइल आकार भी बढ़ाता है।

### Step 3: Specify the layout name

Aspose.CAD को बताएं कि कौन‑से लेआउट(s) रेंडर करने हैं। `"Layout1"` को अपने DWG फ़ाइल में मौजूद लेआउट के सटीक नाम से बदलें।

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Why this matters:** `Layouts` एरे को सीमित करके आप अनावश्यक शीट्स के निर्यात से बचते हैं, जिससे **dwg to pdf conversion c#** ऑपरेशन तेज़ और परिणामी PDF साफ़ रहता है।

### Step 4: Create `PdfOptions`

रास्टराइज़ेशन सेटिंग्स को PDF निर्यात विकल्पों से लिंक करें।

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Step 5: Export to PDF

अंत में, रेंडर किए गए लेआउट को PDF फ़ाइल के रूप में सहेजें।

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Step 6: Display a success message

एक त्वरित कंसोल आउटपुट ऑपरेशन की सफलता की पुष्टि करता है।

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Common Issues & Solutions

| समस्या | कारण | समाधान |
|-------|-------|-----|
| **PDF नहीं बनाया गया** | `Layouts` एरे DWG में किसी भी लेआउट नाम से मेल नहीं खाता। | CAD व्यूअर का उपयोग करके लेआउट नामों की पुष्टि करें और `Layouts` प्रॉपर्टी को अपडेट करें। |
| **खाली पृष्ठ** | `PageWidth`/`PageHeight` को 0 या बहुत छोटे मान पर सेट किया गया है। | वास्तविक आयाम (जैसे 1600 × 1600) उपयोग करें या इन प्रॉपर्टीज़ को छोड़कर Aspose को स्वतः गणना करने दें। |
| **गलत स्केलिंग** | उच्च‑रिज़ॉल्यूशन आउटपुट की आवश्यकता होने पर DPI सेट नहीं किया गया। | निर्यात करने से पहले `rasterizationOptions.Resolution = 300;` (या इच्छित DPI) सेट करें। |

## Frequently Asked Questions

**Q: क्या मैं कई लेआउट एक साथ निर्यात कर सकता हूँ?**  
A: हाँ, केवल Step 3 में `Layouts` एरे को सभी इच्छित लेआउट नामों को शामिल करने के लिए संशोधित करें, उदाहरण के लिए `new string[] { "Layout1", "Layout2" }`।

**Q: क्या Aspose.CAD अन्य CAD फ़ाइल फ़ॉर्मेट्स के साथ संगत है?**  
A: बिल्कुल। यह DWG, DXF, DWF, DGN और कई अन्य फ़ॉर्मेट्स को सपोर्ट करता है।

**Q: पेज आकार के अलावा PDF आउटपुट सेटिंग्स को कैसे समायोजित करूँ?**  
A: `CadRasterizationOptions` की अतिरिक्त प्रॉपर्टीज़ जैसे `Resolution`, `BackgroundColor`, और `DrawType` को एक्सप्लोर करके परिणाम को फाइन‑ट्यून करें।

**Q: अतिरिक्त Aspose.CAD दस्तावेज़ कहाँ मिलेंगे?**  
A: विस्तृत API रेफ़रेंस और उदाहरणों के लिए [documentation](https://reference.aspose.com/cad/net/) देखें।

**Q: क्या फ्री ट्रायल उपलब्ध है?**  
A: हाँ, आप फ्री ट्रायल को [here](https://releases.aspose.com/) से एक्सेस कर सकते हैं।

## Conclusion

आपने अब **CAD रास्टराइज़ेशन विकल्प सेट करना** और उन्हें **विशिष्ट DWG लेआउट्स को PDF में निर्यात करने** के लिए Aspose.CAD for .NET के साथ उपयोग करना सीख लिया है। यह तरीका आपको कन्वर्ज़न प्रक्रिया पर सटीक नियंत्रण देता है, जिससे आप किसी भी C# एप्लिकेशन में CAD‑to‑PDF कार्यक्षमता को जल्दी और विश्वसनीय रूप से इंटीग्रेट कर सकते हैं।

---

**अंतिम अपडेट:** 2026-03-13  
**परीक्षण किया गया:** Aspose.CAD 24.11 for .NET  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}