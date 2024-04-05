---
title: जावा के लिए Aspose.CAD के साथ DWG प्रारूप के लिए MLeader इकाई का समर्थन करें
linktitle: जावा के साथ DWG प्रारूप के लिए MLeader इकाई का समर्थन करें
second_title: Aspose.CAD जावा एपीआई
description: DWG प्रारूप में MLeader संस्थाओं का समर्थन करने पर हमारे चरण-दर-चरण ट्यूटोरियल के साथ जावा के लिए Aspose.CAD की शक्ति को अनलॉक करें।
type: docs
weight: 12
url: /hi/java/cad-text-and-formatting/support-mleader-entity/
---
## परिचय

जावा के साथ कंप्यूटर-एडेड डिज़ाइन (CAD) के क्षेत्र में, DWG प्रारूप में MLeader संस्थाओं के लिए समर्थन को समझना और लागू करना एक मूल्यवान कौशल है। जावा के लिए Aspose.CAD ऐसे कार्यों के लिए एक मजबूत समाधान प्रदान करता है, जो शक्तिशाली उपकरणों और कार्यात्मकताओं का एक सेट पेश करता है। यह ट्यूटोरियल आपको Aspose.CAD के साथ जावा का उपयोग करके DWG फ़ाइलों के भीतर MLeader इकाइयों का समर्थन करने की प्रक्रिया में मार्गदर्शन करेगा।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में गहराई से जाएँ, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1. जावा विकास वातावरण: सुनिश्चित करें कि आपके सिस्टम पर जावा विकास वातावरण स्थापित है।

2.  Aspose.CAD लाइब्रेरी: जावा के लिए Aspose.CAD लाइब्रेरी को डाउनलोड और इंस्टॉल करें[लिंक को डाउनलोड करें](https://releases.aspose.com/cad/java/).

## नामस्थान आयात करें

अपने जावा प्रोजेक्ट में, Aspose.CAD की क्षमताओं का प्रभावी ढंग से लाभ उठाने के लिए आवश्यक नामस्थान आयात करें। अपने कोड में निम्नलिखित पंक्तियाँ शामिल करें:

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

अब, आइए Aspose.CAD के साथ जावा का उपयोग करके DWG प्रारूप के लिए MLeader इकाइयों का समर्थन करने के लिए चरण-दर-चरण मार्गदर्शिका में कोड को विभाजित करें।

## 1. DWG फ़ाइल लोड करें और कैडइमेज तक पहुंचें

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. एमएलएडर संस्थाओं को मान्य करें

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. एमएलएडर शैली और विशेषताओं को सत्यापित करें

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. एमएलएडर संदर्भ डेटा तक पहुंचें

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. संदर्भ विशेषताओं को मान्य करें

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. एमएलएडर नोड और लीडर लाइन तक पहुंचें

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

## 7. अतिरिक्त विधायक विशेषताओं को मान्य करें

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. टेक्स्ट विशेषताओं को मान्य करें

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. अतिरिक्त विधायक गुण

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## निष्कर्ष

बधाई हो! आपने Java और Aspose.CAD का उपयोग करके DWG प्रारूप के लिए MLeader इकाइयों का समर्थन करने पर व्यापक मार्गदर्शिका को सफलतापूर्वक पार कर लिया है। यह क्षमता उन्नत सीएडी जोड़तोड़ के द्वार खोलती है और आपके जावा विकास टूलकिट को बढ़ाती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य CAD प्रारूपों के साथ Java के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: हाँ, Aspose.CAD, DWG से परे विभिन्न CAD प्रारूपों का समर्थन करता है, जो आपकी परियोजनाओं में बहुमुखी प्रतिभा प्रदान करता है।

### Q2: मैं जावा के लिए Aspose.CAD के लिए विस्तृत दस्तावेज़ कहां पा सकता हूं?

 A2: देखें[प्रलेखन](https://reference.aspose.com/cad/java/) Aspose.CAD की क्षमताओं की गहन जानकारी के लिए।

### Q3: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ3: हां, इसके साथ सीधे कार्यप्रणाली का अन्वेषण करें[मुफ्त परीक्षण](https://releases.aspose.com/).

### Q4: मैं Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

A4: के माध्यम से एक अस्थायी लाइसेंस प्राप्त करें[इस लिंक](https://purchase.aspose.com/temporary-license/).

### Q5: मैं सामुदायिक समर्थन और सहायता कहाँ से प्राप्त कर सकता हूँ?

A5: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) समुदाय से जुड़ने और सहायता प्राप्त करने के लिए।