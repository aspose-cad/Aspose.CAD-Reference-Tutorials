---
date: 2026-02-17
description: Aspose.CAD का उपयोग करके जावा में DWG को JPEG के रूप में सहेजना सीखें,
  कई लेयर जोड़ें, और सटीक इमेज रूपांतरण के लिए CAD आयाम समायोजित करें।
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: जावा में लेयर समर्थन के साथ DWG को JPEG के रूप में सहेजें
url: /hi/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में लेयर समर्थन के साथ DWG को JPEG के रूप में सहेजें

## परिचय

इस ट्यूटोरियल में आप सीखेंगे कि **DWG को JPEG के रूप में कैसे सहेजें** और Aspose.CAD for Java में लेयर समर्थन का पूरा लाभ कैसे उठाएँ। लेयर्स आपको ड्रॉइंग के विशिष्ट भागों को अलग करने की सुविधा देती हैं, जिससे केवल आवश्यक भाग को एक्सपोर्ट करना आसान हो जाता है। हम प्रत्येक चरण को विस्तार से देखेंगे, पर्यावरण सेटअप से लेकर केवल चुनी हुई लेयर्स के साथ JPEG एक्सपोर्ट करने तक।

## त्वरित उत्तर
- **“DWG को JPEG के रूप में सहेजना” क्या मतलब है?** यह DWG (या अन्य CAD) ड्रॉइंग को एक रास्टर JPEG इमेज में बदल देता है।  
- **क्या मैं केवल चयनित लेयर्स शामिल कर सकता हूँ?** हाँ – `setLayers` मेथड का उपयोग करके आप रेंडर करने वाली लेयर्स निर्दिष्ट कर सकते हैं।  
- **इमेज का आकार कैसे बदलूँ?** `CadRasterizationOptions` में `setPageWidth` और `setPageHeight` को समायोजित करें।  
- **क्या यह केवल Java समाधान है?** उदाहरण Aspose.CAD for Java का उपयोग करता है, लेकिन समान अवधारणाएँ अन्य भाषाओं पर भी लागू होती हैं।  
- **क्या लाइसेंस की आवश्यकता है?** परीक्षण के लिए फ्री ट्रायल काम करता है; उत्पादन के लिए एक कॉमर्शियल लाइसेंस आवश्यक है।

## “DWG को JPEG के रूप में सहेजना” क्या है?
DWG को JPEG के रूप में सहेजना का अर्थ है एक वेक्टर‑आधारित CAD फ़ाइल (DWG, DWF, DXF आदि) को एक मानक JPEG बिटमैप में रास्टराइज़ करना। यह तब उपयोगी होता है जब आपको CAD ड्रॉइंग को वेब पेज, ईमेल या रिपोर्ट में एम्बेड करना हो जो केवल रास्टर इमेज को सपोर्ट करती हैं।

## लेयर‑अवेयर JPEG रूपांतरण क्यों उपयोग करें?
- **संबंधित डेटा पर फोकस:** केवल आवश्यक लेयर्स को एक्सपोर्ट करें, जिससे फ़ाइल आकार और दृश्य अव्यवस्था कम हो।  
- **डिज़ाइन इंटेंट को बनाए रखें:** लेयर्स ऑब्जेक्ट्स के लॉजिकल ग्रुपिंग को संरक्षित करती हैं, जिससे आप एक ही स्रोत फ़ाइल को विभिन्न आउटपुट के लिए पुनः उपयोग कर सकते हैं।  
- **आयामों पर पूर्ण नियंत्रण:** रास्टराइज़ेशन विकल्पों को समायोजित करके आप उच्च‑रिज़ॉल्यूशन इमेज बना सकते हैं जो आपके प्रकाशन आवश्यकताओं से मेल खाती हैं।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हों:

1. **Aspose.CAD for Java Library** – इसे [website](https://releases.aspose.com/cad/java/) से डाउनलोड करें। इंस्टॉलेशन गाइड का पालन करके JAR फ़ाइलों को अपने प्रोजेक्ट की क्लासपाथ में जोड़ें।  
2. **Java Development Environment** – आपके मशीन पर एक हालिया JDK (8 या उससे नया) स्थापित हो।

अब जब सेटअप पूरा हो गया है, चलिए कोड देखें जो **DWG को JPEG के रूप में सहेजता** है और चयनात्मक लेयर रेंडरिंग को सक्षम करता है।

## नेमस्पेस इम्पोर्ट करें

आवश्यक Aspose.CAD क्लासेज़ और मानक Java यूटिलिटीज़ को इम्पोर्ट करें:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## चरण‑दर‑चरण गाइड

### चरण 1: फ़ाइल पाथ सेट करें

परिभाषित करें कि स्रोत DWF फ़ाइल कहाँ स्थित है और आउटपुट JPEG कहाँ लिखी जाएगी।

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

यदि आप एक से अधिक लेयर रेंडर करना चाहते हैं, तो उनके नाम सूची में जोड़ें। यहाँ हम “LayerA” नाम की एकल लेयर से शुरू करते हैं।

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Pro tip:* **एकाधिक लेयर्स जोड़ने** के लिए `Arrays.asList` कॉल को विस्तारित करें, उदाहरण के लिए `Arrays.asList("LayerA", "LayerB", "LayerC")`। इससे आप **विशिष्ट CAD लेयर्स** को रूपांतरण के लिए चुन सकते हैं।

### चरण 5: JPEG विकल्प कॉन्फ़िगर करें (Java Convert CAD Image)

रास्टराइज़ेशन सेटिंग्स को JPEG आउटपुट फ़ॉर्मेट से जोड़ें।

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### चरण 6: JPG में एक्सपोर्ट करें (DWG को JPEG के रूप में सहेजें)

अंत में, इमेज को डिस्क पर लिखें। यह चरण **CAD ड्रॉइंग को JPEG फ़ाइल के रूप में सहेजता** है जिसमें केवल चयनित लेयर्स होती हैं।

```java
image.save(outFile, jpegOptions);
```

इन चरणों का पालन करके आपने सफलतापूर्वक **DWG को JPEG के रूप में सहेजा** है, जबकि आप लेयर्स को नियंत्रित कर रहे हैं और इमेज के आयामों को कस्टमाइज़ कर रहे हैं।

## लेयर चयन के साथ DWF को JPEG में कैसे बदलें

हालाँकि उदाहरण में DWF स्रोत का उपयोग किया गया है, वही रास्टराइज़ेशन पाइपलाइन किसी भी समर्थित CAD फ़ॉर्मेट (DWG, DXF, DGN आदि) के लिए काम करती है। `srcFile` में फ़ाइल एक्सटेंशन बदलें और लाइब्रेरी स्वचालित रूप से **convert DWF to JPEG** (या अन्य फ़ॉर्मेट) ऑपरेशन को संभाल लेगी।

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **लेयर्स नहीं दिख रही हैं** | सुनिश्चित करें कि लेयर नाम DWF फ़ाइल में मौजूद नामों से बिल्कुल मेल खाते हों (केस‑सेंसिटिव)। |
| **आउटपुट इमेज खाली है** | `setPageWidth` और `setPageHeight` को ड्रॉइंग की सीमा के अनुसार पर्याप्त बड़ा रखें। |
| **लाइसेंस अपवाद** | परीक्षण के लिए ट्रायल लाइसेंस उपयोग करें; उत्पादन के लिए पूर्ण लाइसेंस प्राप्त करें। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं रास्टराइज़ेशन विकल्पों में कई लेयर्स जोड़ सकता हूँ?**  
उत्तर: बिल्कुल। `stringList` में अतिरिक्त लेयर नाम जोड़ें, उदाहरण के लिए `Arrays.asList("LayerA", "LayerB")`।

**प्रश्न: क्या Aspose.CAD अन्य CAD फ़ॉर्मेट्स के साथ संगत है?**  
उत्तर: हाँ, यह DWG, DXF, DWF और कई अन्य फ़ॉर्मेट्स को सपोर्ट करता है।

**प्रश्न: आउटपुट इमेज के आयाम कैसे बदलूँ?**  
उत्तर: `CadRasterizationOptions` इंस्टेंस में `setPageWidth` और `setPageHeight` को संशोधित करें।

**प्रश्न: Aspose.CAD के लिए लाइसेंस कहाँ खरीद सकता हूँ?**  
उत्तर: आप लाइसेंसिंग विकल्पों को [here](https://purchase.aspose.com/buy) पर देख सकते हैं।

**प्रश्न: समुदाय समर्थन कहाँ प्राप्त कर सकता हूँ?**  
उत्तर: सहायता और चर्चा के लिए Aspose.CAD समुदाय में [forum](https://forum.aspose.com/c/cad/19) से जुड़ें।

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}