---
date: 2025-12-01
description: Aspose.CAD for Java का उपयोग करके PDF पेज आकार सेट करना, DWG को PDF में
  बदलना और DWG परिवर्तनों को ट्रैक करने की सुविधा को सक्षम करना सीखें।
language: hi
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Aspose.CAD Java के साथ PDF पेज आकार सेट करें और DWG को ट्रैक करें
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD Java के साथ PDF पेज आकार सेट करें और DWG को ट्रैक करें

## परिचय

CAD प्रोजेक्ट्स पर सहयोग करते समय आपको अक्सर **PDF पेज आकार सेट** करना पड़ता है ताकि लेआउट सुसंगत रहे, **DWG को PDF में बदलना** पड़े, और ड्रॉइंग में किए गए हर परिवर्तन को ट्रैक करना हो। Aspose.CAD for Java इन सभी कार्यों को एक ही सहज वर्कफ़्लो में संभव बनाता है। इस ट्यूटोरियल में हम **PDF पेज आकार सेट** करने, **DWG परिवर्तन ट्रैक** करने, और ड्रॉइंग को PDF के रूप में एक्सपोर्ट करने के सटीक चरणों को Java का उपयोग करके दिखाएंगे।

## त्वरित उत्तर
- **PDF पेज आकार कैसे सेट करें?** एक्सपोर्ट करने से पहले `CadRasterizationOptions.setPageWidth()` और `setPageHeight()` का उपयोग करें।  
- **क्या एक्सपोर्ट करते समय परिवर्तन ट्रैक कर सकते हैं?** हाँ – कस्टम `CadRenderHandler` लागू करके ट्रैकिंग परिणाम प्राप्त करें।  
- **DWG को PDF में बदलने की विधि कौन सी है?** विकल्पों को कॉन्फ़िगर करने के बाद `image.save(stream, pdfOptions)` को कॉल करें।  
- **मुख्य पूर्वापेक्षाएँ क्या हैं?** JDK, Aspose.CAD for Java, और DWG/DXF फ़ाइलों वाला फ़ोल्डर।  
- **प्रोडक्शन के लिए लाइसेंस आवश्यक है?** हाँ, गैर‑ट्रायल डिप्लॉयमेंट के लिए वैध Aspose.CAD लाइसेंस आवश्यक है।

## “PDF पेज आकार सेट” का अर्थ DWG एक्सपोर्ट के संदर्भ में क्या है?

PDF पेज आकार सेट करने से उत्पन्न PDF कैनवास के आयाम (चौड़ाई × ऊँचाई पिक्सेल में) निर्धारित होते हैं। यह तब आवश्यक होता है जब आप चाहते हैं कि एक्सपोर्ट किया गया ड्रॉइंग किसी विशिष्ट कागज़ के आकार या स्क्रीन लेआउट में फिट हो, जिससे सभी तत्व ठीक उसी जगह पर दिखें जहाँ आप चाहते हैं।

## DWG फ़ाइलें एक्सपोर्ट करते समय ट्रैकिंग क्यों सक्षम करें?

ट्रैकिंग (या चेंज‑ट्रैकिंग) रेंडरिंग समस्याओं, गायब फ़ॉन्ट्स, या असमर्थित एंटिटीज़ को रिकॉर्ड करती है जो कन्वर्ज़न के दौरान उत्पन्न होती हैं। इस जानकारी को कैप्चर करके आप:

- अंतिम डिलीवरी से पहले ठीक करने योग्य समस्याओं की जल्दी पहचान कर सकते हैं।  
- टीम के सदस्यों को यह स्पष्ट फीडबैक दे सकते हैं कि क्या बदला या छोड़ा गया।  
- कंप्लायंस‑भारी उद्योगों के लिए ऑडिट ट्रेल बनाए रख सकते हैं।

## पूर्वापेक्षाएँ

- **Java Development Kit (JDK)** – कोई भी हालिया संस्करण (8+)।  
- **Aspose.CAD for Java** – आधिकारिक [Aspose CAD डाउनलोड पेज](https://releases.aspose.com/cad/java/) से डाउनलोड करें।  
- **डॉक्यूमेंट डायरेक्टरी** – वह फ़ोल्डर जिसमें आप प्रोसेस करने वाली DWG/DXF फ़ाइलें हों।

## नेमस्पेस इम्पोर्ट करें

आवश्यक Aspose.CAD क्लासेज़ और मानक Java I/O क्लासेज़ को इम्पोर्ट करके शुरू करें।

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## चरण 1: DWG (या DXF) फ़ाइल लोड करें

अपने स्रोत ड्रॉइंग को `Image` ऑब्जेक्ट में लोड करें। पाथ को अपने डायरेक्टरी के अनुसार समायोजित करें।

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## चरण 2: PDF एक्सपोर्ट विकल्प कॉन्फ़िगर करें (पेज आकार सहित)

यहाँ हम PDF विकल्प सेट करते हैं और स्पष्ट रूप से **PDF पेज आकार** को 800 × 600 पिक्सेल पर सेट करते हैं। यही वह जगह है जहाँ मुख्य कीवर्ड लागू होता है।

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## चरण 3: ट्रैकिंग लागू करें

एक कस्टम एरर‑हैंडलर बनाएं जो कन्वर्ज़न प्रक्रिया के दौरान ट्रैकिंग जानकारी प्राप्त करेगा।

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## चरण 4: PDF में एक्सपोर्ट करें

विकल्पों और ट्रैकिंग हैंडलर को सेट करने के बाद, ड्रॉइंग को एक्सपोर्ट करें। यह चरण **DWG को PDF में बदलता** है (या हमारे उदाहरण में DXF को PDF में)।

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## चरण 5: CadRenderHandler क्लास – ट्रैकिंग परिणाम कैप्चर करना

`ErrorHandler` क्लास `CadRenderHandler` को एक्सटेंड करती है और **DWG फ़ाइलों में परिवर्तन ट्रैक** करते समय उत्पन्न किसी भी रेंडरिंग समस्या को प्रिंट करती है।

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## सामान्य समस्याएँ एवं समाधान

| समस्या | कारण | समाधान |
|-------|------|--------|
| **Missing fonts** | CAD फ़ाइल उन फ़ॉन्ट्स को रेफ़रेंस करती है जो सर्वर पर इंस्टॉल नहीं हैं। | आवश्यक फ़ॉन्ट्स इंस्टॉल करें या उन्हें स्रोत ड्रॉइंग में एम्बेड करें। |
| **Unsupported entities** | कुछ DWG एंटिटीज़ अभी तक Aspose.CAD द्वारा सपोर्ट नहीं की गई हैं। | ट्रैकिंग आउटपुट का उपयोग करके उन्हें पहचानें और ड्रॉइंग को सरल बनाएं। |
| **Incorrect page size** | एक्सपोर्ट से पहले `setPageWidth/Height` नहीं बुलाया गया। | ऊपर दिखाए अनुसार `CadRasterizationOptions` में पेज आकार सेट करना सुनिश्चित करें। |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं Aspose.CAD for Java का उपयोग करके अन्य CAD फ़ाइल फ़ॉर्मैट्स के लिए ट्रैकिंग सक्षम कर सकता हूँ?

A1: Aspose.CAD मुख्यतः DWG/DXF फ़ाइलों के लिए ट्रैकिंग सपोर्ट करता है। अन्य फ़ॉर्मैट्स के लिए उपलब्ध फीचर्स के बारे में आधिकारिक डॉक्यूमेंटेशन देखें।

### Q2: Aspose.CAD for Java में अतिरिक्त एक्सपोर्ट विकल्पों को कैसे हैंडल करूँ?

A2: लाइब्रेरी कई विकल्प प्रदान करती है जैसे DPI, बैकग्राउंड कलर, और वेक्टर रास्टराइज़ेशन। इन्हें [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) में देखें।

### Q3: क्या Aspose.CAD for Java का ट्रायल संस्करण उपलब्ध है?

A3: हाँ, आप [Aspose.CAD Free Trial](https://releases.aspose.com/) से मुफ्त ट्रायल डाउनलोड कर सकते हैं।

### Q4: Aspose.CAD for Java से संबंधित सहायता या मुद्दों पर चर्चा करने के लिए कहाँ जा सकता हूँ?

A4: [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर कम्युनिटी फ़ोरम एक अच्छा स्थान है जहाँ आप प्रश्न पूछ सकते हैं और अनुभव साझा कर सकते हैं।

### Q5: Aspose.CAD for Java के लिए अस्थायी लाइसेंस कैसे प्राप्त करूँ?

A5: मूल्यांकन के लिए समय‑सीमित लाइसेंस प्राप्त करने हेतु [Temporary License](https://purchase.aspose.com/temporary-license/) पेज पर दिए गए चरणों का पालन करें।

### Q6: क्या मैं **DWG को PDF में बदलते** समय लेयर्स को संरक्षित रख सकता हूँ?

A6: हाँ। `CadRasterizationOptions` को कॉन्फ़िगर करके आप परिणामी PDF में लेयर जानकारी को संरक्षित रख सकते हैं।

### Q7: कस्टम पेज डाइमेंशन के साथ **DWG को PDF के रूप में एक्सपोर्ट** करने का सबसे अच्छा तरीका क्या है?

A7: `image.save()` को कॉल करने से पहले `setPageWidth` और `setPageHeight` के माध्यम से इच्छित चौड़ाई और ऊँचाई सेट करें – जैसा कि चरण 2 में दिखाया गया है।

## निष्कर्ष

ऊपर बताए गए चरणों का पालन करके आप **PDF पेज आकार सेट**, **DWG को PDF में बदल**, और **DWG फ़ाइलों में परिवर्तन ट्रैक** कर सकते हैं, वह भी Aspose.CAD for Java का उपयोग करके। यह वर्कफ़्लो आपको आउटपुट लेआउट पर पूर्ण नियंत्रण देता है और मूल्यवान डायग्नॉस्टिक्स प्रदान करता है, जिससे आपका CAD सहयोग सुगम और त्रुटि‑रहित बनता है। अतिरिक्त रेंडरिंग विकल्पों का अन्वेषण करें और इस कोड को बड़े ऑटोमेशन पाइपलाइन में इंटीग्रेट करें।

---

**Last Updated:** 2025-12-01  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}