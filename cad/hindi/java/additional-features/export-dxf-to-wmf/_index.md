---
date: 2025-11-29
description: Aspose.CAD for Java के साथ DXF को WMF में कैसे बदलें, DXF ड्राइंग लोड
  करें, और वैकल्पिक रूप से Aspose के माध्यम से PDF निर्यात का उपयोग करें, यह सीखें।
  कोड उदाहरणों के साथ चरण-दर-चरण गाइड।
language: hi
linktitle: Export DXF to WMF Format Using Java
second_title: Aspose.CAD Java API
title: Aspose.CAD का उपयोग करके जावा में DXF को WMF में परिवर्तित करें
url: /java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java का उपयोग करके DXF को WMF में परिवर्तित करें

## परिचय

इस ट्यूटोरियल में आप **Aspose.CAD for Java** के साथ **DXF को WMF में परिवर्तित** करना सीखेंगे। चाहे आपको Windows‑आधारित रिपोर्ट में CAD ड्रॉइंग एम्बेड करनी हो या सिर्फ हल्का वेक्टर फ़ॉर्मेट चाहिए, DXF को WMF में बदलना एक सामान्य आवश्यकता है। हम DXF ड्रॉइंग लोड करने, रास्टराइज़ेशन विकल्पों को कॉन्फ़िगर करने, परिणाम को WMF के रूप में सहेजने, और वैकल्पिक रूप से Aspose के PDF निर्यात का उपयोग करने की प्रक्रिया को चरण‑दर‑चरण देखेंगे।

## त्वरित उत्तर

- **क्या मैं मुफ्त ट्रायल के साथ DXF को WMF में परिवर्तित कर सकता हूँ?** हाँ – Aspose पूरी तरह कार्यात्मक 30‑दिनीय ट्रायल प्रदान करता है।  
- **कौन सा Java संस्करण आवश्यक है?** Java 8 या बाद का।  
- **क्या कोड चलाने के लिए लाइसेंस चाहिए?** उत्पादन के लिए लाइसेंस आवश्यक है; ट्रायल विकास और परीक्षण के लिए काम करता है।  
- **क्या परिवर्तन बिना नुकसान के है?** वेक्टर डेटा संरक्षित रहता है; रास्टराइज़ेशन विकल्पों से आप रिज़ॉल्यूशन नियंत्रित कर सकते हैं।  
- **क्या मैं उसी ड्रॉइंग को PDF में भी निर्यात कर सकता हूँ?** बिल्कुल – नीचे “Export to PDF” चरण देखें।

## DXF को WMF में परिवर्तित करना क्या है?

DXF को WMF में परिवर्तित करना का मतलब है Drawing Exchange Format (DXF) फ़ाइल—जो एक व्यापक रूप से उपयोग किया जाने वाला CAD फ़ॉर्मेट है—को Windows Metafile (WMF) में बदलना। WMF एक वेक्टर इमेज फ़ॉर्मेट है जो Microsoft Office, Windows एप्लिकेशन और कई रिपोर्टिंग टूल्स के साथ सहजता से एकीकृत होता है।

## Java के लिए Aspose.CAD क्यों उपयोग करें?

- **कोई बाहरी निर्भरताएँ नहीं** – शुद्ध Java, कोई नेटिव DLL नहीं।  
- **उच्च सटीकता** – लेयर्स, रंग, और लाइन स्टाइल्स को संरक्षित करता है।  
- **इनबिल्ट रास्टराइज़ेशन** – पेज आकार, रिज़ॉल्यूशन, और बैकग्राउंड को बारीकी से समायोजित करें।  
- **वन-स्टॉप समाधान** – वही API PDF, PNG, SVG आदि में निर्यात का समर्थन करता है।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास:

- **Aspose.CAD for Java** आपके प्रोजेक्ट में एकीकृत हो। इसे आधिकारिक साइट से डाउनलोड करें: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Document directory** जहाँ आपके DXF फ़ाइलें संग्रहीत हैं (उदाहरण के लिए `Your Document Directory/DXFDrawings/`).

## नेमस्पेस आयात करें

अपने Java स्रोत फ़ाइल में, आवश्यक Aspose.CAD क्लासेज़ को आयात करें:

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

## स्टेप‑बाय‑स्टेप गाइड

### चरण 1: DXF ड्रॉइंग लोड करें

पहले, **DXF ड्रॉइंग** को लोड करें जिसे आप परिवर्तित करना चाहते हैं। `Image.load` मेथड फ़ाइल को मेमोरी में पढ़ता है।

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### चरण 2: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

आउटपुट WMF के आकार को नियंत्रित करने वाले रास्टराइज़ेशन पैरामीटर सेट करें। इस उदाहरण में हम 100 × 100 यूनिट पेज का उपयोग करते हैं।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

### चरण 3: WMF के रूप में सहेजें

अब ऊपर परिभाषित विकल्पों का उपयोग करके लोड की गई ड्रॉइंग को WMF फ़ाइल के रूप में सहेजें।

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

### चरण 4: संसाधनों को मुक्त करें

संसाधनों को सही तरीके से रिलीज़ करना मेमोरी लीक को रोकता है, विशेषकर जब कई ड्रॉइंग प्रोसेस की जा रही हों।

```java
finally
{
  cadImage.dispose();
}
```

### चरण 5: वैकल्पिक – Aspose को PDF में निर्यात करें

यदि आपको उसी ड्रॉइंग का PDF संस्करण भी चाहिए, तो Aspose.CAD इसे एक लाइन में कर देता है।

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

> **Pro tip:** आप वही `CadRasterizationOptions` ऑब्जेक्ट PDF निर्यात के लिए `PdfOptions` इंस्टेंस में पास करके पुनः उपयोग कर सकते हैं।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | वेरिएबल `cadImage` परिभाषित नहीं है (यह `image` होना चाहिए)। | `cadImage` को `image` से बदलें या वेरिएबल को लगातार उसी नाम से रखें। |
| **Output WMF is blank** | रास्टराइज़ेशन पेज आकार बहुत छोटा है या बैकग्राउंड रंग ट्रांसपेरेंट सेट है। | `PageWidth`/`PageHeight` बढ़ाएँ या `rasterizationOptions.setBackgroundColor(Color.getWhite());` के द्वारा बैकग्राउंड रंग सेट करें। |
| **License exception** | उत्पादन में वैध Aspose लाइसेंस के बिना चल रहा है। | एप्लिकेशन शुरू होने पर लाइसेंस फ़ाइल लागू करें: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## निष्कर्ष

अब आपके पास **Aspose.CAD for Java** का उपयोग करके **DXF को WMF में परिवर्तित** करने की एक पूर्ण, उत्पादन‑तैयार वर्कफ़्लो है, जिसमें **Aspose के PDF निर्यात** का वैकल्पिक चरण भी शामिल है। यह तरीका उच्च‑गुणवत्ता वाला वेक्टर आउटपुट प्रदान करता है जो Windows‑आधारित रिपोर्टिंग और डॉक्यूमेंटेशन टूल्स के साथ सहजता से एकीकृत होता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: मैं Aspose.CAD दस्तावेज़ कहाँ प्राप्त कर सकता हूँ?

A1: आप दस्तावेज़ **[यहाँ](https://reference.aspose.com/cad/java/)** प्राप्त कर सकते हैं।

### Q2: मैं Aspose.CAD for Java कैसे डाउनलोड करूँ?

A2: लाइब्रेरी **[यहाँ](https://releases.aspose.com/cad/java/)** डाउनलोड करें।

### Q3: क्या मुफ्त ट्रायल उपलब्ध है?

A3: हाँ, आप मुफ्त ट्रायल **[यहाँ](https://releases.aspose.com/)** प्राप्त कर सकते हैं।

### Q4: क्या अस्थायी लाइसेंस विकल्प चाहिए?

A4: अस्थायी लाइसेंस **[यहाँ](https://purchase.aspose.com/temporary-license/)** देखें।

### Q5: मुझे समर्थन कहाँ मिल सकता है?

A5: Aspose.CAD सपोर्ट फ़ोरम **[यहाँ](https://forum.aspose.com/c/cad/19)** देखें।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं बड़ी DXF फ़ाइलें (सैकड़ों MB) मेमोरी खत्म हुए बिना परिवर्तित कर सकता हूँ?**  
A: हाँ। फ़ाइल को `try‑with‑resources` ब्लॉक में लोड करें और `Image` ऑब्जेक्ट को तुरंत डिस्पोज़ करें। मेमोरी उपयोग कम रखने के लिए `CadRasterizationOptions.setPageWidth/Height` को उचित आकार पर सेट करें।

**Q: क्या WMF आउटपुट लेयर जानकारी को बनाए रखता है?**  
A: WMF एक फ्लैट वेक्टर फ़ॉर्मेट है, इसलिए लेयर हायरार्की फ्लैट हो जाती है, लेकिन लाइन स्टाइल्स और रंग संरक्षित रहते हैं।

**Q: क्या WMF के लिए कस्टम DPI सेट करना संभव है?**  
A: सहेजने से पहले DPI निर्धारित करने के लिए `rasterizationOptions.setResolution(300);` का उपयोग करें।

**Q: क्या मैं एक ही रन में कई DXF फ़ाइलों को बैच‑कन्वर्ट कर सकता हूँ?**  
A: बिल्कुल। एक डायरेक्टरी के माध्यम से लूप करें, प्रत्येक फ़ाइल लोड करें, और वही रास्टराइज़ेशन व सहेजने की लॉजिक लागू करें।

**Q: कौन से Java संस्करण समर्थित हैं?**  
A: Aspose.CAD for Java Java 8 और बाद के संस्करणों (जैसे Java 11, 17, और नए LTS रिलीज़) को समर्थन देता है।

---

**Last Updated:** 2025-11-29  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}