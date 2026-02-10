---
date: 2025-12-22
description: Aspose.CAD for Java के साथ DWG फ़ाइल को लोड करना और अंडरले जानकारी निकालना
  सीखें – अंडरले फ़्लैग्स को कवर करने वाला चरण‑दर‑चरण गाइड।
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: DWG फ़ाइल लोड करें और अंडरले फ़्लैग्स तक पहुंचें – Aspose.CAD for Java
url: /hi/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG फ़ाइल लोड करें और अंडरले फ़्लैग्स तक पहुँचें – Aspose.CAD for Java

आधुनिक CAD कार्यप्रवाहों में, **DWG फ़ाइल लोड करना** तेज़ी से और अंडरले विवरण निकालना एक सामान्य आवश्यकता है। चाहे आप एक व्यूअर बना रहे हों, बैच प्रोसेसिंग को स्वचालित कर रहे हों, या GIS एकीकरण के लिए मेटाडेटा निकाल रहे हों, Aspose.CAD for Java आपको इसे करने का साफ़, कोड‑पहला तरीका देता है। इस ट्यूटोरियल में हम **DWG फ़ाइल लोड करना**, उसकी एंटिटीज़ पर इटररेट करना, और उन अंडरले फ़्लैग्स को पढ़ना जो कई डेवलपर्स नजरअंदाज करते हैं, के सटीक चरणों को देखेंगे।

## त्वरित उत्तर
- **DWG खोलने के लिए मुख्य क्लास कौन सी है?** `com.aspose.cad.Image.load()` एक `CadImage` लौटाता है।
- **अंडरले जानकारी कौन सा ऑब्जेक्ट रखता है?** `CadUnderlay` (या इसके डेराइव्ड टाइप्स जैसे `CadDgnUnderlay`)।
- **क्या विकास के लिए लाइसेंस चाहिए?** परीक्षण के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।
- **क्या मैं लूप में कई DWG फ़ाइलों को प्रोसेस कर सकता हूँ?** हाँ – बस लोड‑और‑इटररेट पैटर्न को दोहराएँ।
- **क्या यह तरीका Java 11+ के साथ संगत है?** बिल्कुल, Aspose.CAD Java 8 से लेकर नवीनतम LTS रिलीज़ तक सपोर्ट करता है।

## Aspose.CAD में “load dwg file” क्या है?
`Image.load()` बाइनरी DWG सामग्री को पढ़ता है और एक इन‑मेमोरी `CadImage` ऑब्जेक्ट बनाता है। इसके बाद आप लेयर्स, ब्लॉक्स, और अंडरले एंटिटीज़ का अन्वेषण कर सकते हैं बिना DWG फ़ाइल फ़ॉर्मेट को स्वयं संभाले।

## DWG से अंडरले फ़्लैग्स निकालना क्यों आवश्यक है?
अंडरले फ़्लैग्स बताते हैं कि बाहरी रेफ़रेंस (जैसे DGN या PDF अंडरले) ड्राइंग के भीतर कैसे स्थित, स्केल और घुमाया गया है। इन मानों को जानने से आप:
- कस्टम व्यूअर में सटीक विज़ुअल लेआउट को पुनः बनाना।
- अंडरलेज़ को मूल CAD एंटिटीज़ में बदलना ताकि आगे संपादन किया जा सके।
- रिपोर्ट बनाना जिसमें अंडरले मेटाडेटा शामिल हो, अनुपालन या दस्तावेज़ीकरण के लिए।

## पूर्वापेक्षाएँ
- **Aspose.CAD लाइब्रेरी** – [releases](https://releases.aspose.com/cad/java/) पेज से डाउनलोड करें।
- **Java Development Kit** – JDK 8 या नया।
- **एक फ़ोल्डर** जिसमें वह DWG फ़ाइलें हों जिन्हें आप विश्लेषण करना चाहते हैं। कोड में `"Your Document Directory"` को अपने वास्तविक पथ से बदलें।

## नेमस्पेस इम्पोर्ट करें

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
अपने DWG फ़ाइलों के स्थान को निर्धारित करें। एक समर्पित फ़ोल्डर का उपयोग करने से सैंपल साफ़ और पोर्टेबल रहता है।

### चरण 2: DWG फ़ाइल लोड करें
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
यहाँ हम **DWG फ़ाइल लोड** `BlockRefDgn.dwg` को एक `CadImage` इंस्टेंस में लोड कर रहे हैं, जो निरीक्षण के लिए तैयार है।

### चरण 3: DWG एंटिटीज़ पर इटररेट करें
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
लूप हर एंटिटी—लाइन, सर्कल, ब्लॉक, और अंडरले—पर चलता है ताकि हम आवश्यक एंटिटीज़ को चुन सकें।

### चरण 4: CadDgnUnderlay एंटिटीज़ की पहचान करें
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
केवल `CadDgnUnderlay` ऑब्जेक्ट्स में वह अंडरले फ़्लैग्स होते हैं जिन्हें हम चाहते हैं, इसलिए हम उन्हें फ़िल्टर करते हैं।

### चरण 5: अंडरले जानकारी तक पहुँचें
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
एक बार जब हमारे पास `CadUnderlay` हो, तो हम उसका पाथ, नाम, इन्सर्शन पॉइंट, रोटेशन, स्केल फैक्टर्स, और `UnderlayFlags` एन्नुम पढ़ सकते हैं जो विज़िबिलिटी, क्लिपिंग, और अन्य रेंडरिंग विकल्पों को दर्शाता है।

## सामान्य समस्याएँ और टिप्स
- **नल अंडरले पाथ** – सुनिश्चित करें कि DWG वास्तव में किसी बाहरी फ़ाइल को रेफ़रेंस करता है; अन्यथा पाथ खाली रहेगा।
- **असमर्थित अंडरले प्रकार** – Aspose.CAD वर्तमान में DGN अंडरले को सपोर्ट करता है; PDF अंडरले अभी तक API के माध्यम से उपलब्ध नहीं हैं।
- **लाइसेंस अपवाद** – वैध लाइसेंस के बिना कोड चलाने पर किसी भी एक्सपोर्टेड इमेज में वॉटरमार्क जुड़ जाएगा।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.CAD for Java को अन्य CAD फ़ाइल फ़ॉर्मेट्स के साथ उपयोग कर सकता हूँ?**  
A: Aspose.CAD मुख्यतः DWG फ़ॉर्मेट पर केंद्रित है, लेकिन यह DXF, DWF, और अन्य CAD फ़ॉर्मेट्स को भी सपोर्ट करता है।

**Q: क्या Aspose.CAD for Java के लिए ट्रायल संस्करण उपलब्ध है?**  
A: हाँ, आप [यहाँ](https://releases.aspose.com/) से एक मुफ्त ट्रायल लेकर फीचर्स का अन्वेषण कर सकते हैं।

**Q: मैं Aspose.CAD for Java के लिए समर्थन या सहायता कैसे प्राप्त कर सकता हूँ?**  
A: समुदाय समर्थन और चर्चा के लिए [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) पर जाएँ।

**Q: क्या Aspose.CAD for Java के लिए अस्थायी लाइसेंस उपलब्ध हैं?**  
A: हाँ, आप एक अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

**Q: Aspose.CAD for Java की व्यापक दस्तावेज़ीकरण कहाँ मिल सकती है?**  
A: विस्तृत जानकारी के लिए [डॉक्यूमेंटेशन](https://reference.aspose.com/cad/java/) देखें।

---

**अंतिम अपडेट:** 2025-12-22  
**परीक्षित संस्करण:** Aspose.CAD 24.12 for Java  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}