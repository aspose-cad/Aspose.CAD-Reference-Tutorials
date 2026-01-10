---
date: 2026-01-10
description: Aspose.CAD for Java का उपयोग करके DWG फ़ाइलें पढ़ना और मल्टीलीडर DWG
  एंटिटीज़ बनाना इस चरण‑दर‑चरण ट्यूटोरियल में सीखें।
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java के साथ DWG को पढ़ना और MLeader का समर्थन कैसे करें
url: /hi/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Read DWG and Support MLeader with Aspose.CAD for Java

## Introduction

यदि आपको **DWG** फ़ाइलें पढ़नी हैं और एक Java एप्लिकेशन में **multileader DWG** एंटिटीज़ के साथ काम करना है, तो आप सही जगह पर आए हैं। Aspose.CAD for Java आपको DWG ड्रॉइंग्स को खोलने, MLeader ऑब्जेक्ट्स का निरीक्षण करने और उनकी प्रॉपर्टीज़ को वैलिडेट करने का एक साफ़, प्रोग्रामेटिक तरीका देता है—बिना किसी पूर्ण‑स्तरीय CAD वर्कस्टेशन की आवश्यकता के। इस ट्यूटोरियल में हम हर कदम को समझेंगे, DWG फ़ाइल लोड करने से लेकर यह पुष्टि करने तक कि मल्टीलीडर डेटा अपेक्षित शैली से मेल खाता है।

## Quick Answers
- **What does “how to read dwg” involve?** Loading the DWG with `Image.load()` and casting to `CadImage`.
- **Can I create multileader dwg entities?** Yes – you can add, edit, and validate MLeader objects using the CadMLeader API.
- **Which library version is required?** Any recent Aspose.CAD for Java release (the API shown works with the 2024+ builds).
- **Do I need a license for development?** A temporary license works for testing; a full license is required for production.
- **Is the code cross‑platform?** Absolutely – Java runs on Windows, Linux, and macOS.

## What is “how to read dwg” with Aspose.CAD?

DWG फ़ाइल को पढ़ना मतलब बाइनरी ड्रॉइंग को मेमोरी में `CadImage` ऑब्जेक्ट में बदलना। एक बार यह ऑब्जेक्ट मिल जाने पर, आप उसकी एंटिटीज़ (लाइन, सर्कल, टेक्स्ट, **MLeader** ऑब्जेक्ट्स, आदि) को एनेमरेट कर सकते हैं और उनकी प्रॉपर्टीज़ का निरीक्षण कर सकते हैं।

## Why support MLeader entities?

MLeader (multileader) ऑब्जेक्ट्स लीडर लाइनों को जुड़े टेक्स्ट या ब्लॉक्स के साथ मिलाते हैं, जिससे वे इंजीनियरिंग ड्रॉइंग्स में एनोटेशन के लिए अत्यंत महत्वपूर्ण होते हैं। उनका समर्थन करने से आप:

- यह सत्यापित कर सकते हैं कि एनोटेशन कंपनी मानकों के अनुरूप हैं।
- डाउनस्ट्रीम प्रोसेसिंग (जैसे BOM जेनरेशन) के लिए टेक्स्ट निकाल सकते हैं।
- प्रोग्रामेटिक रूप से लीडर स्टाइल को बदल सकते हैं या ब्लॉक कंटेंट को प्रतिस्थापित कर सकते हैं।

## Prerequisites

शुरू करने से पहले सुनिश्चित करें कि आपके पास हैं:

1. **Java Development Environment** – JDK 11+ और आपका पसंदीदा IDE (IntelliJ, Eclipse, VS Code)।  
2. **Aspose.CAD for Java** – नवीनतम JAR [download link](https://releases.aspose.com/cad/java/) से डाउनलोड करें।  

## Import Namespaces

अपने Java क्लास में निम्नलिखित इम्पोर्ट जोड़ें ताकि आप DWG एंटिटीज़ और रास्टराइज़ेशन विकल्पों के साथ काम कर सकें:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## How to Read DWG Files Using Aspose.CAD for Java

### Step 1: Load the DWG file and get a `CadImage`

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### Step 2: Validate that the drawing contains MLeader entities

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### Step 3: Verify MLeader style and basic attributes

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### Step 4: Access the MLeader context data (the heart of the multileader)

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### Step 5: Validate context‑level attributes

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### Step 6: Work with the MLeader node and its leader line

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

### Step 7: Validate additional MLeader node attributes

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### Step 8: Check text‑related properties

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### Step 9: Review other MLeader attributes for completeness

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Common Issues and Solutions

| समस्या | क्यों होता है | समाधान |
|-------|----------------|-----|
| `ClassCastException` when casting entity | चयनित इंडेक्स MLeader ऑब्जेक्ट नहीं है। | कास्ट करने से पहले `cadImage.getEntities()[i] instanceof CadMLeader` की जाँच करें। |
| `null` values for leader line points | ड्रॉइंग एक कस्टम लीडर स्टाइल उपयोग करती है जो पूरी तरह समर्थित नहीं है। | नवीनतम Aspose.CAD संस्करण का उपयोग करें या परीक्षण के लिए डिफ़ॉल्ट स्टाइल पर वापस जाएँ। |
| Assertion failures on numeric values | CAD संस्करणों के बीच हल्के राउंडिंग अंतर। | उदाहरणों में दिखाए अनुसार `Assert.areEqual(..., delta)` में टॉलरेंस समायोजित करें। |

## Frequently Asked Questions

**Q: क्या मैं Aspose.CAD for Java को अन्य CAD फ़ॉर्मैट्स के साथ उपयोग कर सकता हूँ?**  
A: हाँ, Aspose.CAD DWG के अलावा DXF, DWF, DGN और कई रास्टर फ़ॉर्मैट्स को सपोर्ट करता है।

**Q: Aspose.CAD for Java की विस्तृत डॉक्यूमेंटेशन कहाँ मिल सकती है?**  
A: API विवरण और कोड नमूनों के लिए आधिकारिक [documentation](https://reference.aspose.com/cad/java/) देखें।

**Q: क्या कोई फ्री ट्रायल उपलब्ध है?**  
A: बिल्कुल – आप [free trial](https://releases.aspose.com/) पेज से ट्रायल डाउनलोड कर सकते हैं।

**Q: परीक्षण के लिए अस्थायी लाइसेंस कैसे प्राप्त करूँ?**  
A: [temporary license link](https://purchase.aspose.com/temporary-license/) से अस्थायी लाइसेंस प्राप्त करें।

**Q: समुदाय से मदद कैसे प्राप्त करूँ?**  
A: प्रश्न और समाधान साझा करने के लिए सबसे अच्छा स्थान है [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)।

## Conclusion

अब आपके पास **DWG** फ़ाइलें पढ़ने और **multileader DWG** एंटिटीज़ बनाने के लिए Aspose.CAD for Java का एक पूर्ण‑से‑पूर्ण मार्गदर्शन है। ऊपर दिए गए चरणों का पालन करके आप MLeader स्टाइल को वैलिडेट कर सकते हैं, एनोटेशन डेटा निकाल सकते हैं, और DWG प्रोसेसिंग को किसी भी Java‑आधारित वर्कफ़्लो में एकीकृत कर सकते हैं।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.CAD 24.11 for Java  
**Author:** Aspose