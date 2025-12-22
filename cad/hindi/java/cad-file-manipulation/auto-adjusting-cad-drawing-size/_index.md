---
date: 2025-12-22
description: Aspose.CAD के साथ जावा में CAD ड्रॉइंग्स को निर्यात करना और DWG को BMP
  में बदलना सीखें। कुशल CAD फ़ाइल संचालन के लिए इस चरण‑दर‑चरण गाइड का पालन करें।
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java का उपयोग करके CAD ड्राइंग को BMP में निर्यात कैसे करें
url: /hi/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.CAD का उपयोग करके CAD ड्राइंग को BMP में एक्सपोर्ट करने का तरीका

## परिचय

यदि आप Java से **how to export cad** फ़ाइलों को स्पष्ट और विश्वसनीय तरीके से एक्सपोर्ट करने का तरीका खोज रहे हैं, तो आप सही जगह पर आए हैं। Aspose.CAD for Java के साथ आप न केवल ड्राइंग आकारों को ऑटो‑एडजस्ट कर सकते हैं, बल्कि कुछ ही कोड लाइनों में **convert DWG to BMP** भी कर सकते हैं। यह ट्यूटोरियल आपको सेटअप से लेकर BMP इमेज जेनरेट करने तक की पूरी प्रक्रिया दिखाता है, जो मूल CAD लेआउट को संरक्षित रखता है।

## त्वरित उत्तर
- **“how to export cad” का क्या अर्थ है?** यह CAD फ़ाइलों (DWG, DXF, आदि) को BMP, PNG या PDF जैसे अन्य फ़ॉर्मेट में बदलने को दर्शाता है।  
- **कौन सी लाइब्रेरी परिवर्तन संभालती है?** Aspose.CAD for Java इस कार्य के लिए सरल API प्रदान करती है।  
- **क्या लाइसेंस की आवश्यकता है?** परीक्षण के लिए एक अस्थायी लाइसेंस काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **क्या मैं एक साथ कई लेआउट एक्सपोर्ट कर सकता हूँ?** हाँ – `Layouts` प्रॉपर्टी सेट करके आप उन लेआउट्स को निर्दिष्ट कर सकते हैं जिन्हें रेंडर करना है।  
- **क्या BMP ही एकमात्र आउटपुट फ़ॉर्मेट है?** नहीं – आप PNG, JPEG, TIFF आदि में भी एक्सपोर्ट कर सकते हैं।

## Aspose.CAD के साथ “how to export cad” क्या है?
CAD को एक्सपोर्ट करने का मतलब है मूल CAD ड्राइंग (जैसे DWG फ़ाइल) को रास्टर इमेज या किसी अन्य वेक्टर फ़ॉर्मेट में बदलना। Aspose.CAD सभी जटिल कार्यों को संभालती है: CAD संरचना को पार्स करना, वेक्टर एंटिटीज़ को रास्टराइज़ करना, और परिणाम को आपके चुने हुए इमेज फ़ॉर्मेट में लिखना।

## **convert DWG to BMP** के लिए Java में Aspose.CAD क्यों उपयोग करें?
- **कोई बाहरी निर्भरताएँ नहीं** – शुद्ध Java, कोई नेटिव DLL नहीं।  
- **DWG, DXF, DGN और अन्य फ़ॉर्मेट्स के लिए पूर्ण समर्थन**।  
- **रास्टराइज़ेशन विकल्पों पर सूक्ष्म नियंत्रण** जैसे लेआउट चयन, स्केलिंग, और बैकग्राउंड रंग।  
- **उच्च प्रदर्शन** जो सर्वरों पर बैच प्रोसेसिंग के लिए उपयुक्त है।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Java Development Kit** – इसे [यहाँ](https://www.java.com/en/download/) से डाउनलोड करें।  
2. **Aspose.CAD for Java लाइब्रेरी** – नवीनतम JAR [यहाँ](https://releases.aspose.com/cad/java/) से प्राप्त करें।  
3. **सैंपल CAD फ़ाइल** – एक DWG फ़ाइल (जैसे `sample.dwg`) को अपने प्रोजेक्ट की `document` डायरेक्टरी में रखें।

## नेमस्पेस इम्पोर्ट करें

अपने Java एप्लिकेशन में Aspose.CAD कार्यक्षमता का उपयोग करने के लिए आवश्यक नेमस्पेस शामिल करें। नीचे एक उदाहरण दिया गया है:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

अब, **how to export cad** प्रक्रिया को समझने योग्य चरणों में विभाजित करते हैं।

## चरण‑दर‑चरण गाइड

### चरण 1: CAD ड्राइंग लोड करें

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

हम स्रोत DWG फ़ाइल को एक `Image` ऑब्जेक्ट में लोड करते हैं, जो सभी आगे के ऑपरेशन्स का एंट्री पॉइंट है।

### चरण 2: `BmpOptions` बनाएं

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions` BMP आउटपुट के लिए विशिष्ट रास्टराइज़ेशन सेटिंग्स रखेगा।

### चरण 3: रास्टराइज़ेशन सेटिंग्स कॉन्फ़िगर करें

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

यहाँ हम रास्टराइज़ेशन विकल्पों को BMP विकल्पों से लिंक करते हैं, जिससे हम CAD एंटिटीज़ के रेंडरिंग को नियंत्रित कर सकते हैं।

### चरण 4: एक्सपोर्ट करने के लिए लेआउट(s) सेट करें

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

`Layouts` प्रॉपर्टी Aspose.CAD को बताती है कि कौन‑से ड्राइंग लेआउट्स को शामिल करना है। अधिकांश मामलों में, `"Model"` वह मुख्य लेआउट है जिसे आप बदलना चाहते हैं।

### चरण 5: BMP फ़ॉर्मेट में एक्सपोर्ट करें

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

कॉन्फ़िगर किए गए `BmpOptions` के साथ `save` कॉल करने से BMP फ़ाइल डिस्क पर लिखी जाती है। यह **convert DWG to BMP** वर्कफ़्लो को पूरा करता है।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|--------|-----|
| आउटपुट इमेज खाली है | गलत लेआउट नाम या लेआउट अनुपलब्ध | लेआउट नाम CAD फ़ाइल से मेल खाता है (जैसे `"Model"`), यह सत्यापित करें। |
| कम रिज़ॉल्यूशन | डिफ़ॉल्ट DPI कम है | `cadRasterizationOptions.setResolution(300);` को सेव करने से पहले सेट करें। |
| बड़े फ़ाइलों के लिए Out‑of‑memory त्रुटि | बड़े ड्रॉइंग्स को अधिक हीप चाहिए | JVM हीप साइज बढ़ाएँ (`-Xmx2g`) या पेज़ को व्यक्तिगत रूप से प्रोसेस करें। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या Aspose.CAD विभिन्न CAD फ़ाइल फ़ॉर्मेट्स के साथ संगत है?**  
उत्तर: हाँ, Aspose.CAD DWG, DXF, DGN और कई अन्य फ़ॉर्मेट्स को सपोर्ट करता है।

**प्रश्न: क्या मैं Aspose.CAD को वाणिज्यिक प्रोजेक्ट्स में उपयोग कर सकता हूँ?**  
उत्तर: बिल्कुल। उत्पादन उपयोग के लिए लाइसेंस [यहाँ](https://purchase.aspose.com/buy) खरीदें।

**प्रश्न: परीक्षण के लिए अस्थायी लाइसेंस कैसे प्राप्त करूँ?**  
उत्तर: आप अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

**प्रश्न: समुदाय समर्थन कहाँ मिल सकता है?**  
उत्तर: Aspose.CAD कम्युनिटी फ़ोरम [forum](https://forum.aspose.com/c/cad/19) पर जुड़ें।

**प्रश्न: क्या Aspose.CAD for Java का फ्री ट्रायल उपलब्ध है?**  
उत्तर: हाँ, फ्री ट्रायल [यहाँ](https://releases.aspose.com/) डाउनलोड करें।

## निष्कर्ष

इस गाइड में हमने Java से **how to export cad** फ़ाइलों को **convert DWG to BMP** करने का तरीका Aspose.CAD का उपयोग करके दिखाया। ऊपर बताए गए पाँच चरणों का पालन करके आप किसी भी Java एप्लिकेशन में CAD‑to‑image रूपांतरण को एकीकृत कर सकते हैं, चाहे वह डेस्कटॉप टूल हो, वेब सर्विस, या बैच प्रोसेसिंग पाइपलाइन। विकल्प क्लास को बदलकर अन्य आउटपुट फ़ॉर्मेट्स (PNG, JPEG, PDF) भी एक्सप्लोर करें, और Aspose.CAD की समृद्ध सुविधाओं का लाभ उठाकर अपनी सभी CAD मैनिपुलेशन आवश्यकताओं को पूरा करें।

---

**Last Updated:** 2025-12-22  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}