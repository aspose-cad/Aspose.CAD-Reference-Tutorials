---
date: 2026-02-23
description: Aspose CAD DWG for Java का उपयोग करके DWG फ़ाइलें लोड करना और अंडरले
  फ़्लैग्स निकालना सीखें – डेवलपर्स के लिए चरण‑दर‑चरण गाइड।
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – DWG लोड करें और अंडरले फ़्लैग्स तक पहुंचें (Java)
url: /hi/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG फ़ाइल लोड करें और अंडरले फ़्लैग्स तक पहुँचें – Aspose.CAD for Java

आधुनिक CAD कार्यप्रवाहों में, **with aspose cad dwg you can quickly load a DWG file** और ऐसे अंडरले विवरण निकाल सकते हैं जो अक्सर सामान्य दर्शकों से छिपे रहते हैं। चाहे आप एक Java DWG viewer बना रहे हों, बैच प्रोसेस dwg पाइपलाइन को स्वचालित कर रहे हों, या GIS एकीकरण के लिए मेटाडेटा निकाल रहे हों, Aspose.CAD for Java आपको एक साफ़, कोड‑फ़र्स्ट तरीका प्रदान करता है। इस ट्यूटोरियल में हम **load a DWG file**, उसकी एंटिटीज़ को इटरेट करने, और उन अंडरले फ़्लैग्स को पढ़ने के सटीक चरणों से गुजरेंगे जिन्हें कई डेवलपर्स नजरअंदाज़ करते हैं।

## त्वरित उत्तर
- **DWG खोलने के लिए मुख्य क्लास कौन सी है?** `com.aspose.cad.Image.load()` एक `CadImage` लौटाता है।
- **कौन सा ऑब्जेक्ट अंडरले जानकारी रखता है?** `CadUnderlay` (या उसके डेराइव्ड टाइप जैसे `CadDgnUnderlay`)।
- **क्या विकास के लिए लाइसेंस चाहिए?** परीक्षण के लिए एक फ्री ट्रायल काम करता है; प्रोडक्शन के लिए एक कमर्शियल लाइसेंस आवश्यक है।
- **क्या मैं लूप में कई DWG फ़ाइलें प्रोसेस कर सकता हूँ?** हाँ – बस लोड‑एंड‑इटरेट पैटर्न को दोहराएँ।
- **क्या यह तरीका Java 11+ के साथ संगत है?** बिल्कुल, Aspose.CAD Java 8 से लेकर नवीनतम LTS रिलीज़ तक सपोर्ट करता है।

## aspose cad dwg – Loading a DWG File (Java)

`Image.load()` बाइनरी DWG कंटेंट को पढ़ता है और एक इन‑मे़मोरी `CadImage` ऑब्जेक्ट बनाता है। इसके बाद आप लेयर्स, ब्लॉक्स, और अंडरले एंटिटीज़ को बिना DWG फ़ाइल फ़ॉर्मेट को समझे एक्सप्लोर कर सकते हैं।

## DWG से अंडरले फ़्लैग्स निकालने का कारण

अंडरले फ़्लैग्स यह बताते हैं कि एक एक्सटर्नल रेफ़रेंस (जैसे DGN या PDF अंडरले) ड्राइंग के भीतर कैसे पोज़िशन, स्केल, और रोटेट किया गया है। इन मानों को जानने से आप:

- कस्टम **java dwg viewer** में सटीक विज़ुअल लेआउट को पुनः बनाना।
- अंडरले को नेेटिव CAD एंटिटीज़ में बदलना ताकि आगे एडिट किया जा सके।
- अनुपालन या डॉक्यूमेंटेशन के लिए अंडरले मेटाडेटा शामिल करने वाली रिपोर्ट जनरेट करना।
- **Batch process dwg** फ़ाइलें और उनके अंडरले मेटाडेटा को बाद में विश्लेषण के लिए डेटाबेस में स्टोर करना।

## आवश्यकताएँ
- **Aspose.CAD Library** – [releases](https://releases.aspose.com/cad/java/) पेज से डाउनलोड करें।  
- **Java Development Kit** – JDK 8 या नया।  
- **एक फ़ोल्डर** जिसमें वह DWG फ़ाइलें हों जिन्हें आप विश्लेषण करना चाहते हैं। कोड में `"Your Document Directory"` को अपने वास्तविक पथ से बदलें।

## Import Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## चरण‑दर‑चरण गाइड

### चरण 1: रिसोर्स डायरेक्टरी सेट करें
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
परिभाषित करें कि आपकी DWG फ़ाइलें कहाँ स्थित हैं। एक समर्पित फ़ोल्डर उपयोग करने से सैंपल साफ़ और पोर्टेबल रहता है।

### चरण 2: DWG फ़ाइल लोड करें
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
यहाँ हम **load dwg file** `BlockRefDgn.dwg` को एक `CadImage` इंस्टेंस में लोड करते हैं, जो निरीक्षण के लिए तैयार है।

### चरण 3: DWG एंटिटीज़ को इटरेट करें
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
यह लूप हर एंटिटी—लाइन, सर्कल, ब्लॉक, और अंडरले—पर चलता है ताकि हम आवश्यक एंटिटीज़ को चुन सकें।

### चरण 4: CadDgnUnderlay एंटिटीज़ की पहचान करें
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
केवल `CadDgnUnderlay` ऑब्जेक्ट्स में वह अंडरले फ़्लैग्स होते हैं जिनकी हमें आवश्यकता है, इसलिए हम उन्हें फ़िल्टर करते हैं।

### चरण 5: अंडरले जानकारी तक पहुँचें
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
एक बार जब हमारे पास `CadUnderlay` हो, तो हम उसका पाथ, नाम, इन्सर्शन पॉइंट, रोटेशन, स्केल फैक्टर्स, और `UnderlayFlags` एन्नुम पढ़ सकते हैं जो विज़िबिलिटी, क्लिपिंग, और अन्य रेंडरिंग विकल्प दर्शाता है।

## बैच प्रोसेस में dwg फ़ाइलें कैसे लोड करें

यदि आपको **batch process dwg** फ़ाइलें करनी हैं, तो ऊपर दिए गए चरणों को एक साधारण `for` लूप में रैप करें जो `dataDir` में सभी फ़ाइलों पर इटरेट करे। वही `Image.load()` कॉल प्रत्येक फ़ाइल के लिए काम करता है, और आप निकाले गए फ़्लैग्स को CSV या डेटाबेस में स्टोर कर सकते हैं आगे की रिपोर्टिंग के लिए।

## सामान्य समस्याएँ और टिप्स
- **Null underlay path** – सुनिश्चित करें कि DWG वास्तव में एक एक्सटर्नल फ़ाइल रेफ़रेंस करता है; अन्यथा पाथ खाली रहेगा।
- **Unsupported underlay type** – Aspose.CAD वर्तमान में DGN अंडरले को सपोर्ट करता है; PDF अंडरले अभी तक API के माध्यम से एक्सपोज़ नहीं किए गए हैं।
- **License exceptions** – वैध लाइसेंस के बिना कोड चलाने पर किसी भी एक्सपोर्टेड इमेज में वॉटरमार्क जुड़ जाएगा।
- **Performance tip:** कई फ़ाइलों को बैच में प्रोसेस करते समय एक ही `Image` इंस्टेंस को री‑यूज़ करें ताकि GC प्रेशर कम हो।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.CAD for Java को अन्य CAD फ़ाइल फ़ॉर्मेट्स के साथ उपयोग कर सकता हूँ?**  
A: Aspose.CAD मुख्यतः DWG फ़ॉर्मेट पर केंद्रित है, लेकिन यह DXF, DWF, और अन्य CAD फ़ॉर्मेट्स को भी सपोर्ट करता है।

**Q: क्या Aspose.CAD for Java के लिए एक ट्रायल वर्ज़न उपलब्ध है?**  
A: हाँ, आप [यहाँ](https://releases.aspose.com/) से फ्री ट्रायल के साथ फीचर्स का अन्वेषण कर सकते हैं।

**Q: मैं Aspose.CAD for Java के लिए सपोर्ट या सहायता कैसे प्राप्त करूँ?**  
A: समुदाय समर्थन और चर्चा के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) देखें।

**Q: क्या Aspose.CAD for Java के लिए टेम्पररी लाइसेंस उपलब्ध हैं?**  
A: हाँ, आप टेम्पररी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

**Q: Aspose.CAD for Java की व्यापक डॉक्यूमेंटेशन कहाँ मिल सकती है?**  
A: विस्तृत जानकारी के लिए [documentation](https://reference.aspose.com/cad/java/) देखें।

---

**Last Updated:** 2026-02-23  
**Tested With:** Aspose.CAD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}