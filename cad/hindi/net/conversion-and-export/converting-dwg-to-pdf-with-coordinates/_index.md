---
date: 2026-04-03
description: Aspose.CAD का उपयोग करके C# में व्यूपोर्ट सेट करना और DWG को PDF में
  बदलना सीखें। यह DWG‑से‑PDF ट्यूटोरियल समन्वय के साथ सटीक निर्यात दिखाता है।
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: C# में निर्देशांक के साथ DWG को PDF में बदलना
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: C# में कोऑर्डिनेट्स के साथ DWG को PDF में बदलते समय व्यूपोर्ट कैसे सेट करें
  - Aspose.CAD ट्यूटोरियल
url: /hi/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# में कॉर्डिनेट्स के साथ DWG को PDF में बदलना - Aspose.CAD ट्यूटोरियल

## परिचय

Aspose.CAD for .NET का उपयोग करके निर्दिष्ट कॉर्डिनेट्स के साथ DWG फ़ाइलों को PDF में बदलते समय **viewport सेट करने** के बारे में इस व्यापक ट्यूटोरियल में आपका स्वागत है। viewport को नियंत्रित करके आप पिक्सेल‑परफेक्ट PDF प्राप्त करते हैं जो बिल्कुल वही क्षेत्र मिलते हैं जिसकी आपको आवश्यकता है—निर्माण ड्रॉइंग, फ़्लोर‑प्लान प्रीव्यू, या किसी भी BIM वर्कफ़्लो के लिए उपयुक्त।

## त्वरित उत्तर
- **“set viewport” का क्या अर्थ है?** यह रास्टराइज़ेशन के दौरान CAD ड्रॉइंग के दृश्यमान क्षेत्र और स्केलिंग को परिभाषित करता है।  
- **कौन सा लाइब्रेरी रूपांतरण संभालता है?** Aspose.CAD for .NET।  
- **क्या मुझे लाइसेंस चाहिए?** मूल्यांकन के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **समर्थित प्लेटफ़ॉर्म?** Windows, Linux, और macOS, .NET 5/6/7 या .NET Framework 4.6+ के साथ।  
- **आम तौर पर कार्यान्वयन समय?** बुनियादी रूपांतरण के लिए लगभग 10‑15 मिनट।

## पूर्वापेक्षाएँ

Before we begin, make sure you have the following prerequisites:

- **Aspose.CAD लाइब्रेरी** – .NET के लिए Aspose.CAD लाइब्रेरी डाउनलोड और इंस्टॉल करें। आप लाइब्रेरी [यहाँ](https://releases.aspose.com/cad/net/) पा सकते हैं।
- **डेवलपमेंट एनवायरनमेंट** – Visual Studio, Rider, या कोई भी IDE जो .NET विकास का समर्थन करता हो।
- **DWG फ़ाइल** – रूपांतरण के लिए एक तैयार DWG फ़ाइल रखें। आप प्रदान की गई उदाहरण फ़ाइल या अपनी कस्टम DWG फ़ाइल का उपयोग कर सकते हैं।

## सटीक PDF निर्यात के लिए Viewport कैसे सेट करें

Viewport सेट करना वह मुख्य चरण है जो आपको रेंडर करने के लिए ड्रॉइंग के सटीक क्षेत्र को परिभाषित करने देता है। नीचे के कोड में हम एक नया `CadVportTableObject` बनाते हैं, उसे टॉप‑लेफ़्ट कॉर्डिनेट से स्थित करते हैं, और चौड़ाई, ऊँचाई, तथा अनुपात की गणना करते हैं। यह **viewport कैसे सेट करें** कार्यान्वयन है जो रूपांतरण के बाकी हिस्सों को चलाता है।

## नेमस्पेस आयात करें

In your C# project, import the necessary namespaces:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

आइए कोड को बेहतर समझ के लिए चरण‑दर‑चरण मार्गदर्शिका में विभाजित करें:

## चरण 1: दस्तावेज़ डायरेक्टरी निर्धारित करें

```csharp
string MyDir = "Your Document Directory";
```

## चरण 2: स्रोत DWG फ़ाइल पथ सेट करें

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## चरण 3: DWG फ़ाइल लोड करें और रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## चरण 4: कॉर्डिनेट्स और Viewport निर्धारित करें  

Here we actually **set the viewport** (how to set viewport) by specifying the top‑left corner, width, and height of the area you want to export.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## चरण 5: Viewport सेटिंग्स लागू करें

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## चरण 6: PDF विकल्प कॉन्फ़िगर करें और निर्यात करें  

Now we tie everything together and **convert DWG to PDF** using the rasterization options we just prepared.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## चरण 7: सफलता संदेश प्रदर्शित करें

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## सामान्य उपयोग केस

- **निर्माण दस्तावेज़ीकरण** – विशिष्ट फ़्लोर‑प्लान सेक्शन के प्रिंटेबल PDF बनाएं।  
- **BIM समन्वय** – टकराव पहचान के लिए केवल इच्छित क्षेत्र निर्यात करें।  
- **क्लाइंट प्रस्तुतियाँ** – पूरे ड्रॉइंग को उजागर किए बिना चयनित कमरे या ऊँचाई का साफ़ PDF प्रदान करें।

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सटीक कॉर्डिनेट्स के साथ **DWG को PDF में बदल दिया** है और Aspose.CAD for .NET का उपयोग करके **viewport कैसे सेट करें** सीखा है। यह **dwg to pdf ट्यूटोरियल** दर्शाता है कि **dwg से pdf कैसे बनाएं** और **dwg को pdf c# के रूप में निर्यात करें** कैसे किया जाता है, जबकि आउटपुट क्षेत्र पर पूर्ण नियंत्रण बनाए रखा जाता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.CAD को अन्य CAD फ़ाइल फ़ॉर्मेट्स के साथ उपयोग कर सकता हूँ?

A1: हाँ, Aspose.CAD विभिन्न CAD फ़ॉर्मेट्स का समर्थन करता है, जिसमें DWG, DXF, DWF, और अधिक शामिल हैं।

### Q2: रूपांतरण प्रक्रिया के दौरान त्रुटियों को कैसे संभालूँ?

A2: अपवादों को पकड़ने और प्रबंधित करने के लिए try‑catch ब्लॉक्स का उपयोग करके त्रुटि संभालने की तंत्र लागू करें।

### Q3: क्या Aspose.CAD Windows और Linux दोनों वातावरणों के लिए उपयुक्त है?

A3: हाँ, Aspose.CAD Windows और Linux दोनों प्लेटफ़ॉर्म के साथ संगत है।

### Q4: क्या मैं PDF आउटपुट को और अनुकूलित कर सकता हूँ?

A4: बिल्कुल! अपने विशिष्ट आवश्यकताओं के अनुसार PDF आउटपुट को अनुकूलित करने के लिए Aspose.CAD द्वारा प्रदान किए गए विस्तृत विकल्पों का अन्वेषण करें।

### Q5: अतिरिक्त समर्थन या समुदाय चर्चा कहाँ पा सकता हूँ?

A5: समुदाय समर्थन और चर्चाओं के लिए [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) पर जाएँ।

## अतिरिक्त अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या यह तरीका बड़े DWG फ़ाइलों (सैकड़ों MB) के साथ काम करता है?**  
**उत्तर:** हाँ। रास्टराइज़ेशन पेज‑दर‑पेज किया जाता है, और आप `rasterizationOptions` (जैसे, `Resolution`) को समायोजित करके गुणवत्ता और मेमोरी उपयोग के बीच संतुलन बना सकते हैं।

**प्रश्न: क्या मैं कई viewports को अलग-अलग PDF पेजों में निर्यात कर सकता हूँ?**  
**उत्तर:** आप `cadImage.ViewPorts` के माध्यम से लूप कर सकते हैं, प्रत्येक को सक्रिय सेट करें, और प्रत्येक पेज के लिए `Save` कॉल करें, फिर Aspose.PDF का उपयोग करके PDF को मर्ज करें।

**प्रश्न: क्या उत्पन्न PDF में वॉटरमार्क जोड़ना संभव है?**  
**उत्तर:** PDF सहेजने के बाद, आप इसे Aspose.PDF के साथ पुनः खोल सकते हैं और उपयोगकर्ता को देने से पहले टेक्स्ट या इमेज वॉटरमार्क लागू कर सकते हैं।

---

**अंतिम अपडेट:** 2026-04-03  
**परीक्षण किया गया:** Aspose.CAD 24.11 for .NET  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}