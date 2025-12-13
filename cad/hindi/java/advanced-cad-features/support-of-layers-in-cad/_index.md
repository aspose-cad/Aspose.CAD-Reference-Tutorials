---
date: 2025-12-13
description: जावा में Aspose.CAD का उपयोग करके CAD को JPEG के रूप में सहेजना, कई लेयर
  जोड़ना, और सटीक इमेज रूपांतरण के लिए CAD आयामों को समायोजित करना सीखें।
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: जावा में लेयर समर्थन के साथ CAD को JPEG के रूप में सहेजें
url: /hi/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में लेयर समर्थन के साथ CAD को JPEG के रूप में सहेजें

## परिचय

इस ट्यूटोरियल में आप सीखेंगे कि **CAD को JPEG के रूप में कैसे सहेजें** और Aspose.CAD for Java में लेयर समर्थन का पूरा लाभ कैसे उठाएँ। लेयर्स आपको ड्रॉइंग के विशिष्ट भागों को अलग‑अलग करने की सुविधा देती हैं, जिससे आप केवल आवश्यक भाग को ही एक्सपोर्ट कर सकते हैं। हम पर्यावरण सेटअप से लेकर केवल चुनी गई लेयर्स के साथ JPEG एक्सपोर्ट करने तक के सभी चरणों को क्रमवार समझेंगे।

## त्वरित उत्तर
- **“CAD को JPEG के रूप में सहेजना” का क्या अर्थ है?** यह CAD ड्रॉइंग को एक रास्टर JPEG इमेज में बदल देता है।  
- **क्या मैं केवल चयनित लेयर्स को शामिल कर सकता हूँ?** हाँ – `setLayers` मेथड का उपयोग करके आप रेंडर करने वाली लेयर्स निर्दिष्ट कर सकते हैं।  
- **इमेज का आकार कैसे बदलूँ?** `CadRasterizationOptions` में `setPageWidth` और `setPageHeight` को समायोजित करें।  
- **क्या यह केवल Java‑के लिए समाधान है?** उदाहरण Aspose.CAD for Java का उपयोग करता है, लेकिन समान अवधारणाएँ अन्य भाषाओं में भी लागू होती हैं।  
- **क्या लाइसेंस की आवश्यकता है?** परीक्षण के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Aspose.CAD for Java लाइब्रेरी** – इसे [website](https://releases.aspose.com/cad/java/) से डाउनलोड करें। इंस्टॉलेशन गाइड का पालन करके JAR फ़ाइलों को अपने प्रोजेक्ट के क्लासपाथ में जोड़ें।  
2. **Java विकास पर्यावरण** – आपके मशीन पर JDK (संस्करण 8 या नया) स्थापित होना चाहिए।

अब जब सेटअप हो गया है, चलिए उस कोड को देखते हैं जो **CAD को JPEG के रूप में सहेजने** के साथ चयनात्मक लेयर रेंडरिंग को सक्षम करता है।

## नेमस्पेस आयात करें

आवश्यक Aspose.CAD क्लासेज़ और मानक Java यूटिलिटीज़ को आयात करें:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## चरण‑दर‑चरण गाइड

### चरण 1: फ़ाइल पथ निर्धारित करें

स्रोत DWF फ़ाइल का स्थान और आउटपुट JPEG कहाँ लिखना है, यह निर्धारित करें।

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### चरण 2: DWF इमेज लोड करें

Aspose.CAD के `Image.load` मेथड का उपयोग करके CAD ड्रॉइंग को पढ़ें।

```java
Image image = Image.load(srcFile);
```

### चरण 3: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें (CAD आयाम समायोजित करें)

एक `CadRasterizationOptions` इंस्टेंस बनाएं और इच्छित आउटपुट आकार सेट करें। इन मानों को बदलने से आप अंतिम JPEG के लिए **CAD आयाम समायोजित** कर सकते हैं।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### चरण 4: लेयर्स निर्दिष्ट करें (एकाधिक लेयर्स जोड़ें)

यदि आप एक से अधिक लेयर रेंडर करना चाहते हैं, तो उनके नाम सूची में जोड़ें। यहाँ हम “LayerA” नाम की एकल लेयर से शुरू कर रहे हैं।

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Pro tip:* **एकाधिक लेयर्स जोड़ने** के लिए `Arrays.asList` कॉल को विस्तारित करें, उदाहरण के लिए `Arrays.asList("LayerA", "LayerB", "LayerC")`।

### चरण 5: JPEG विकल्प कॉन्फ़िगर करें (Java में CAD इमेज कनवर्ट करें)

रास्टराइज़ेशन सेटिंग्स को JPEG आउटपुट फ़ॉर्मेट से जोड़ें।

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### चरण 6: JPG में एक्सपोर्ट करें (CAD को JPEG के रूप में सहेजें)

अंत में, इमेज को डिस्क पर लिखें। यह चरण **CAD ड्रॉइंग को JPEG फ़ाइल के रूप में सहेजता** है जिसमें केवल चयनित लेयर्स शामिल होती हैं।

```java
image.save(outFile, jpegOptions);
```

इन चरणों का पालन करके आपने सफलतापूर्वक **CAD को JPEG के रूप में सहेजा** है, साथ ही यह नियंत्रित किया है कि कौन‑सी लेयर्स दिखाई दें और इमेज के आयाम कैसे अनुकूलित हों।

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **लेयर्स नहीं दिख रही हैं** | सुनिश्चित करें कि लेयर नाम DWF फ़ाइल में मौजूद नामों से बिल्कुल मेल खाते हों (case‑sensitive)। |
| **आउटपुट इमेज खाली है** | `setPageWidth` और `setPageHeight` को ड्रॉइंग के विस्तार के अनुसार पर्याप्त बड़ा रखें। |
| **लाइसेंस अपवाद** | परीक्षण के लिए ट्रायल लाइसेंस उपयोग करें; उत्पादन के लिए पूर्ण लाइसेंस प्राप्त करें। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न:** क्या मैं रास्टराइज़ेशन विकल्पों में कई लेयर्स जोड़ सकता हूँ?  
**उत्तर:** बिल्कुल। `stringList` में अतिरिक्त लेयर नाम जोड़ें, उदाहरण के लिए `Arrays.asList("LayerA", "LayerB")`।

**प्रश्न:** क्या Aspose.CAD अन्य CAD फ़ॉर्मेट्स के साथ संगत है?  
**उत्तर:** हाँ, यह DWG, DXF, DWF और कई अन्य फ़ॉर्मेट्स को सपोर्ट करता है।

**प्रश्न:** आउटपुट इमेज के आयाम कैसे बदलूँ?  
**उत्तर:** `CadRasterizationOptions` इंस्टेंस में `setPageWidth` और `setPageHeight` को संशोधित करें।

**प्रश्न:** Aspose.CAD का लाइसेंस कहाँ खरीद सकता हूँ?  
**उत्तर:** आप लाइसेंस विकल्पों को [यहाँ](https://purchase.aspose.com/buy) देख सकते हैं।

**प्रश्न:** समुदाय समर्थन कहाँ प्राप्त कर सकता हूँ?  
**उत्तर:** सहायता और चर्चा के लिए Aspose.CAD समुदाय के [फ़ोरम](https://forum.aspose.com/c/cad/19) में शामिल हों।

---

**अंतिम अपडेट:** 2025-12-13  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}