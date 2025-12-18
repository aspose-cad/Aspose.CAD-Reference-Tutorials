---
date: 2025-12-18
description: Aspose.CAD for Java के साथ DWG को PNG और अन्य रास्टर इमेज फ़ॉर्मेट में
  कैसे बदलें, सीखें। CAD को PNG के रूप में निर्यात करें और उच्च‑गुणवत्ता वाले परिणाम
  प्राप्त करें।
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java का उपयोग करके DWG को PNG और अन्य रास्टर फ़ॉर्मैट्स में
  बदलें
url: /hi/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java का उपयोग करके DWG को PNG और अन्य रास्टर फ़ॉर्मैट में परिवर्तित करें

## परिचय

## त्वरित उत्तर
- **DWG को PNG में बदलने के लिए कौन‑सी लाइब्रेरी उपयोग होती है?** Aspose.CAD for Java  
- **कौन‑से फ़ॉर्मैट निर्यात किए जा सकते हैं?** PNG, JPEG, TIFF, PDF, BMP, और अधिक  
- **परीक्षण के लिए लाइसेंस चाहिए?** विकास के लिए मुफ्त ट्रायल काम करता है; उत्पादन के लिए लाइसेंस आवश्यक है  
- **क्या मैं किसी विशिष्ट लेआउट को चुन सकता हूँ?** हाँ, `setLayouts` का उपयोग करके “Model”, “Layout1”, आदि को लक्षित करें।  
- **क्या हाई‑रेज़ोल्यूशन आउटपुट संभव है?** बिल्कुल—`setPageWidth` और `setPageHeight` को समायोजित करके DPI नियंत्रित करें  

## “convert dwg to png” क्या है?

वाक्यांश “convert dwg to png” वह प्रक्रिया दर्शाता है जिसमें वेक्टर‑आधारित DWG फ़ाइल (कई CAD अनुप्रयोगों का मूल फ़ॉर्मैट) को पिक्सेल‑आधारित PNG इमेज में रास्टराइज़ किया जाता है। रास्टर इमेज वेब डिस्प्ले, ई‑मेल शेयरिंग, और गैर‑CAD सॉफ़्टवेयर में एकीकरण के लिए आदर्श हैं।

## CAD को PNG (या अन्य रास्टर फ़ॉर्मैट) के रूप में निर्यात क्यों करें?

- **सर्वव्यापी संगतता:** PNG और JPEG लगभग सभी इमेज व्यूअर और ब्राउज़र द्वारा समर्थित हैं।  
- **तेज़ लोडिंग:** रास्टर इमेज भारी DWG फ़ाइल खोलने की तुलना में तुरंत लोड होते हैं।  
- **आसान एम्बेडिंग:** PNG को सीधे Word, PowerPoint, या HTML में बिना अतिरिक्त प्लगइन के डालें।  
- **सुसंगत उपस्थिति:** आप रिज़ॉल्यूशन, बैकग्राउंड और लेआउट को नियंत्रित करते हैं, जिससे सभी हितधारकों को समान दृश्य मिलता है।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास:

1. **Java Development Environment** – JDK 8 या नया स्थापित और कॉन्फ़िगर किया हुआ।  
2. **Aspose.CAD for Java** – नवीनतम JAR को [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/) से डाउनलोड करें।  

## इम्पोर्ट नेमस्पेस

सबसे पहले, उन क्लासेज़ को इम्पोर्ट करें जिनकी आपको आवश्यकता होगी। ये इम्पोर्ट इमेज लोडिंग, रास्टराइज़ेशन विकल्प, और TIFF/PNG आउटपुट सेटिंग्स तक पहुँच प्रदान करते हैं।

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Pro tip:** यदि आप TIFF के बजाय PNG में निर्यात करने की योजना बना रहे हैं, तो `TiffOptions` को `PngOptions` (जो `com.aspose.cad.imageoptions.PngOptions` में पाया जाता है) से बदलें।

## स्टेप‑बाय‑स्टेप गाइड

### स्टेप 1: रिसोर्स डायरेक्टरी सेट करें

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

`"Your Document Directory"` को उस पूर्ण पथ से बदलें जहाँ आपके CAD फ़ाइलें स्थित हैं।

### स्टेप 2: CAD फ़ाइल लोड करें

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

आप किसी भी समर्थित फ़ॉर्मैट (DWG, DXF, DGN, आदि) को लोड कर सकते हैं। यह **how to convert cad** भाग है—सिर्फ फ़ाइल की ओर संकेत करें और Aspose को पार्सिंग संभालने दें।

### स्टेप 3: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` आउटपुट रिज़ॉल्यूशन को नियंत्रित करते हैं (बड़े मान = उच्च DPI)।  
- `setLayouts` आपको विशिष्ट लेआउट के लिए **convert cad to raster** करने देता है; पूरे ड्रॉइंग को रास्टराइज़ करने के लिए इसे छोड़ दें।

### स्टेप 4: इमेज विकल्प सेट करें

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

यदि आप PNG पसंद करते हैं, तो `TiffOptions` के बजाय `PngOptions` को इंस्टैंशिएट करें। यही वह जगह है जहाँ आप **export cad as png** करते हैं।

### स्टेप 5: परिणामस्वरूप इमेज सहेजें

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

फ़ाइल एक्सटेंशन को `.png` (और विकल्प ऑब्जेक्ट को `PngOptions`) में बदलें ताकि **save CAD as JPEG/PNG** किया जा सके।

> **Common Pitfall:** फ़ाइल एक्सटेंशन को विकल्प क्लास के साथ मिलाना न भूलें, अन्यथा `UnsupportedFormatException` उत्पन्न होगा। हमेशा इन्हें सिंक में रखें।

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **Blank output image** | सुनिश्चित करें कि `setLayouts` में लेआउट नाम स्रोत CAD फ़ाइल में मौजूद लेआउट नामों से बिल्कुल मेल खाते हों। |
| **Low‑resolution PNG** | `setPageWidth` / `setPageHeight` बढ़ाएँ या रास्टराइज़ेशन विकल्पों में `setResolution` सेट करें। |
| **Unsupported DWG version** | नवीनतम Aspose.CAD संस्करण का उपयोग करें; पुराने संस्करण नवीनतम DWG रिलीज़ को सपोर्ट नहीं कर सकते। |
| **Memory errors on large files** | पेजों को एक‑एक करके प्रोसेस करें या JVM हीप (`-Xmx2g`) बढ़ाएँ। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या Aspose.CAD विभिन्न CAD फ़ाइल फ़ॉर्मैट्स के साथ संगत है?**  
A: हाँ, यह DWG, DXF, DGN, और कई अन्य को सपोर्ट करता है।

**Q: क्या मैं आउटपुट रास्टर इमेज के रिज़ॉल्यूशन को कस्टमाइज़ कर सकता हूँ?**  
A: बिल्कुल। `setPageWidth`, `setPageHeight`, या `CadRasterizationOptions` में `setResolution` को समायोजित करें।

**Q: एक ही रन में कई CAD लेआउट्स को कैसे बदल सकता हूँ?**  
A: सभी लेआउट नामों की एक एरे `setLayouts` को प्रदान करें, उदाहरण के लिए `new String[]{"Model","Layout1","Layout2"}`।

**Q: क्या TIFF के अलावा अन्य आउटपुट फ़ॉर्मैट सपोर्टेड हैं?**  
A: हाँ—PNG, JPEG, BMP, PDF, और अधिक उनके संबंधित `*Options` क्लासेज़ के माध्यम से उपलब्ध हैं।

**Q: Aspose.CAD के साथ मदद कैसे प्राप्त करूँ या अपना अनुभव साझा करूँ?**  
A: समुदाय समर्थन और आधिकारिक सहायता के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

## निष्कर्ष

इन चरणों का पालन करके आप **DWG को PNG में बदल सकते हैं**, **CAD को PNG के रूप में निर्यात कर सकते हैं**, **CAD को JPEG के रूप में सहेज सकते हैं**, या अपनी आवश्यकता के अनुसार कोई भी अन्य रास्टर फ़ॉर्मैट जेनरेट कर सकते हैं। Aspose.CAD for Java भारी काम संभालता है, जिससे आप अपने अनुप्रयोगों, दस्तावेज़ों, या वेब पोर्टलों में उच्च‑गुणवत्ता वाली इमेज को एकीकृत करने पर ध्यान केंद्रित कर सकते हैं।

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}