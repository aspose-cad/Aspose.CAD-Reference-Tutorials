---
date: 2025-12-28
description: Aspose.CAD for Java का उपयोग करके DWG फ़ाइलें पढ़ना सीखें और DWG फ़ाइलों
  में लेआउट को आसानी से सूचीबद्ध करें। अपने Java अनुप्रयोगों में शक्तिशाली CAD कार्यक्षमता
  को एकीकृत करें।
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java का उपयोग करके DWG को कैसे पढ़ें और DWG में लेआउट्स की सूची
  बनाएं
url: /hi/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java का उपयोग करके DWG को पढ़ना और DWG में लेआउट्स की सूची बनाना

## Introduction

यदि आपको प्रोग्रामेटिक रूप से **DWG** फ़ाइलें पढ़नी हैं और लेआउट नाम जैसी जानकारी निकालनी है, तो Aspose.CAD for Java इसे सरल बनाता है। इस चरण‑दर‑चरण ट्यूटोरियल में हम आपको **DWG को पढ़ना** और DWG (या DXF) फ़ाइल में मौजूद सभी लेआउट्स की सूची दिखाना बताएँगे। गाइड के अंत तक आप इस क्षमता को किसी भी Java एप्लिकेशन में जोड़ सकेंगे जो CAD डेटा के साथ काम करता है।

## Quick Answers
- **What library is required?** Aspose.CAD for Java.
- **Can I read DWG files on any OS?** Yes – Java is cross‑platform.
- **Do I need a license to run the sample?** A free trial works for evaluation; a license is required for production.
- **Which CAD formats are supported?** DWG, DXF, DWF, and others.
- **Is the code compatible with Java 8+?** Absolutely.

## What is “how to read dwg” in Java?

DWG फ़ाइल को पढ़ना का अर्थ है बाइनरी CAD डेटा को एक ऑब्जेक्ट मॉडल में लोड करना जिसे आप क्वेरी कर सकें। Aspose.CAD जटिल DWG संरचना को सरल .NET/Java क्लासेज़ के पीछे छिपा देता है, जिससे आप केवल आवश्यक जानकारी—इस मामले में लेआउट नाम—पर ध्यान केंद्रित कर सकते हैं।

## Why list layouts in a DWG file?

DWG में कई लेआउट (पेपर स्पेस, मॉडल स्पेस, कस्टम शीट) हो सकते हैं। लेआउट नाम जानने से आप:
- प्रत्येक लेआउट के लिए रिपोर्ट जनरेट कर सकते हैं।
- विशिष्ट लेआउट को इमेज या PDF में एक्सपोर्ट कर सकते हैं।
- ड्रॉइंग्स की बैच प्रोसेसिंग को ऑटोमेट कर सकते हैं।

## Prerequisites

कोड में डुबकी लगाने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- **Aspose.CAD for Java Library** – नवीनतम JAR को [website](https://releases.aspose.com/cad/java/) से डाउनलोड करें।
- **Java Development Environment** – JDK 8 या उससे ऊपर, और आपका पसंदीदा IDE या बिल्ड टूल।

## Import Namespaces

अपने Java स्रोत फ़ाइल में आवश्यक Aspose.CAD क्लासेज़ को इम्पोर्ट करें:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Step 1: Set up Your Document Directory

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

**“Your Document Directory”** को उस पूर्ण पथ से बदलें जहाँ आपके CAD फ़ाइलें स्थित हैं।

## Step 2: Load the DWG File

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

`Image.load` मेथड फ़ाइल फ़ॉर्मेट को स्वचालित रूप से पहचानता है, इसलिए आप **DWG** और **DXF** दोनों फ़ाइलों के लिए समान कोड उपयोग कर सकते हैं।

## Step 3: Get Layouts and Print Names

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

यह लूप प्रत्येक लेआउट ऑब्जेक्ट पर इटररेट करता है और उसका नाम कंसोल पर प्रिंट करता है – यह सत्यापित करने का एक सरल तरीका है कि आपने सफलतापूर्वक **DWG** पढ़ ली है और लेआउट जानकारी निकाली है।

## Common Pitfalls & Tips

- **Incorrect file path** – Double‑check that `dataDir` ends with a separator (`/` or `\\`) appropriate for your OS.
- **Unsupported DWG version** – Ensure you are using a recent Aspose.CAD version; older DWG versions may need conversion.
- **Memory usage** – Large drawings can consume significant memory. Dispose of the `CadImage` object when done: `cadImage.dispose();`.

## Conclusion

बधाई हो! अब आप Aspose.CAD for Java का उपयोग करके **DWG को पढ़ना** और उसके लेआउट्स की सूची बनाना जानते हैं। यह तकनीक अधिक उन्नत CAD ऑटोमेशन के लिए आधार बनती है, जैसे कि विशिष्ट लेआउट को इमेज या PDF में एक्सपोर्ट करना। अधिक गहन जानकारी के लिए आधिकारिक [documentation](https://reference.aspose.com/cad/java/) देखें।

## FAQ's

### Q1: Can I use Aspose.CAD for Java with other CAD file formats?

A1: Yes, Aspose.CAD supports various CAD formats, including DWG, DXF, DWF, and more.

### Q2: Is there a free trial available for Aspose.CAD for Java?

A2: Yes, you can obtain a free trial from [here](https://releases.aspose.com/).

### Q3: Where can I get community support for Aspose.CAD for Java?

A3: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support.

### Q4: How do I purchase a license for Aspose.CAD for Java?

A4: You can buy a license from the [purchase page](https://purchase.aspose.com/buy).

### Q5: Can I use a temporary license for testing purposes?

A5: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

**Additional Questions**

**Q: Does this approach work for reading DWG files on Linux?**  
A: Absolutely. Since the solution is pure Java, it runs on any OS with a compatible JDK.

**Q: Can I read a DWG file without loading the entire drawing into memory?**  
A: Aspose.CAD loads the drawing into memory; for very large files consider processing them in separate threads or using streaming APIs if available in future releases.

**Q: Is there a way to filter layouts by name?**  
A: Yes – after retrieving the `CadLayoutDictionary`, you can check `layout.getLayoutName().equalsIgnoreCase("MyLayout")` before processing.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}