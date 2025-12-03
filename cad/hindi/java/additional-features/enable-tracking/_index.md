---
date: 2025-12-03
description: DWG को PDF में बदलते समय PDF पेज आकार सेट करना और Aspose.CAD for Java
  का उपयोग करके DWG फ़ाइलों में ट्रैकिंग सक्षम करना सीखें – सटीकता के साथ CAD ड्राइंग
  को PDF में निर्यात करने के लिए एक पूर्ण गाइड।
language: hi
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Aspose.CAD in Java का उपयोग करके DWG फ़ाइलों में PDF पेज आकार सेट करें और ट्रैकिंग
  सक्षम करें
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF पेज साइज सेट करें और DWG फ़ाइलों में ट्रैकिंग सक्षम करें Aspose.CAD का उपयोग करके Java में

## परिचय

यदि आपको **PDF पेज साइज सेट** करना है जब आप *DWG को PDF में बदलते* हैं और साथ ही किसी भी रेंडरिंग समस्या को ट्रैक करना चाहते हैं, तो Aspose.CAD for Java दोनों कार्यों को करने के लिए एक साफ़, प्रोग्रामेटिक तरीका प्रदान करता है। इस ट्यूटोरियल में हम पेज डाइमेंशन कॉन्फ़िगर करने, ट्रैकिंग सक्षम करने, और CAD ड्रॉइंग को PDF के रूप में एक्सपोर्ट करने के सटीक चरणों से गुजरेंगे—सभी Java से। अंत तक आप समझ जाएंगे कि CAD ड्रॉइंग्स के लिए सही पेज साइज सेट करना क्यों महत्वपूर्ण है और एक्सपोर्ट प्रक्रिया के दौरान विस्तृत ट्रैकिंग जानकारी कैसे कैप्चर की जाए।

## त्वरित उत्तर
- **“PDF पेज साइज सेट” करने से क्या प्रभावित होता है?** यह उत्पन्न PDF कैनवास की चौड़ाई और ऊँचाई निर्धारित करता है, जिससे आपका ड्रॉइंग पूरी तरह फिट हो जाता है।  
- **क्या इस फीचर को उपयोग करने के लिए लाइसेंस चाहिए?** परीक्षण के लिए ट्रायल काम करता है; उत्पादन के लिए वाणिज्यिक लाइसेंस आवश्यक है।  
- **कौन सा Aspose.CAD संस्करण आवश्यक है?** कोई भी हालिया संस्करण जो `CadRasterizationOptions` को सपोर्ट करता है।  
- **क्या मैं इसे अन्य CAD फ़ॉर्मैट्स के साथ उपयोग कर सकता हूँ?** उदाहरण में DWG/DXF दिखाया गया है, लेकिन वही तरीका अधिकांश समर्थित फ़ॉर्मैट्स पर काम करता है।  
- **कन्वर्ज़न में कितना समय लगता है?** सामान्य फ़ाइलों के लिए आमतौर पर एक सेकंड से कम; बड़े ड्रॉइंग्स में अधिक समय लग सकता है।

## CAD निर्यात के संदर्भ में “set PDF page size” क्या है?
PDF पेज साइज सेट करने का मतलब है रेंडरर को आउटपुट कैनवास के सटीक आयाम (पिक्सेल या पॉइंट में) बताना। यह तकनीकी ड्रॉइंग्स के लिए विशेष रूप से महत्वपूर्ण है जहाँ स्केल और लेआउट को बरकरार रखना आवश्यक होता है। स्पष्ट पेज‑साइज़ सेटिंग न होने पर PDF डिफ़ॉल्ट साइज पर डिफ़ॉल्ट हो सकता है, जिससे ड्रॉइंग कट या विकृत हो सकता है।

## CAD ड्रॉइंग्स को निर्यात करते समय PDF पेज साइज क्यों सेट करें?
- **स्केल बनाए रखें** – इंजीनियर सटीक‑स्केल प्रिंट पर भरोसा करते हैं।  
- **पेपर में फिट करें** – प्रोजेक्ट स्पेसिफ़िकेशन के अनुसार A4, Letter, या कस्टम साइज चुनें।  
- **पढ़ने में आसानी** – बड़े पेज छोटे विवरणों को ज़ूम किए बिना दिखा सकते हैं।  
- **सुसंगत आउटपुट** – ऑटोमेटेड पाइपलाइन हर रन में समान आयाम वाले PDF बनाती है।

## DWG को PDF में बदलते समय PDF पेज साइज कैसे सेट करें?
नीचे हम `CadRasterizationOptions` को कस्टम चौड़ाई और ऊँचाई मानों के साथ कॉन्फ़िगर करेंगे, फिर एक्सपोर्ट करेंगे। यह चरण सीधे मुख्य कीवर्ड **set PDF page size** को संबोधित करता है।

## पूर्वापेक्षाएँ

- **Java Development Kit (JDK)** – आपके मशीन पर Java 8 या नया स्थापित होना चाहिए।  
- **Aspose.CAD for Java** – आधिकारिक [Aspose CAD download page](https://releases.aspose.com/cad/java/) से डाउनलोड करें।  
- **Document Directory** – वह फ़ोल्डर जिसमें आप प्रोसेस करने वाले DWG/DXF फ़ाइलें हों।

## नेमस्पेस इम्पोर्ट करें

पहले उन क्लासों को इम्पोर्ट करें जिनकी आपको आवश्यकता होगी। कोड ब्लॉक मूल ट्यूटोरियल जैसा ही रहेगा।

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

## चरण 1: DWG/DXF फ़ाइल लोड करें

अपने स्रोत ड्रॉइंग को लोड करें। पाथ को अपने फ़ाइल के अनुसार समायोजित करें।

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## चरण 2: PDF निर्यात विकल्प कॉन्फ़िगर करें (पेज साइज सहित)

यहाँ हम पेज की चौड़ाई और ऊँचाई सेट करते हैं—यही वह जगह है जहाँ हम **PDF पेज साइज सेट** करते हैं। मान पिक्सेल में हैं; आप आवश्यकता अनुसार इंच या मिलीमीटर से बदल सकते हैं।

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Tip:** यदि आप मानक पेपर साइज पसंद करते हैं, तो `1 inch = 72 points` रूपांतरण का उपयोग करें। A4 पेज (8.27 × 11.69 in) के लिए `pageWidth = 595` और `pageHeight = 842` सेट करें।

## चरण 3: ट्रैकिंग लागू करें

ट्रैकिंग किसी भी रेंडरिंग समस्या को कैप्चर करती है। हम एक कस्टम हैंडलर संलग्न करते हैं जो एक्सपोर्ट के बाद कॉल होगा।

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## चरण 4: PDF में निर्यात करें

अब कन्वर्ज़न करें। PDF आपके द्वारा निर्दिष्ट आयामों के साथ बनाया जाएगा, और कोई भी ट्रैकिंग जानकारी कंसोल में प्रिंट होगी।

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## चरण 5: CadRenderHandler क्लास

यह हैंडलर रेंडरिंग के दौरान हुई किसी भी विफलता को प्रिंट करता है। यह आपको **CAD ड्रॉइंग PDF एक्सपोर्ट** करते समय समस्याओं को डिबग करने में मदद करता है।

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

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|-------|-----|
| **खाली PDF** | पेज साइज 0 या बहुत छोटा सेट किया गया है | सत्यापित करें कि `setPageWidth` और `setPageHeight` सकारात्मक मान हैं। |
| **ज्यामिति गायब** | हैंडलर द्वारा कैप्चर किए गए रेंडरिंग त्रुटियाँ | `ErrorHandler` के कंसोल आउटपुट की समीक्षा करें और विशिष्ट `RenderCode` को ठीक करें। |
| **फ़ाइल नहीं मिली** | गलत `dataDir` पथ | एक पूर्ण पथ उपयोग करें या सुनिश्चित करें कि डायरेक्टरी मौजूद है। |
| **लाइसेंस अपवाद** | बड़े फ़ाइलों के लिए वैध लाइसेंस के बिना ट्रायल का उपयोग करना | इमेज लोड करने से पहले अपना Aspose.CAD लाइसेंस लागू करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.CAD for Java का उपयोग करके अन्य CAD फ़ाइल फ़ॉर्मैट्स के लिए ट्रैकिंग सक्षम कर सकता हूँ?**  
A: Aspose.CAD मुख्यतः ट्रैकिंग के लिए DWG/DXF को सपोर्ट करता है। अन्य फ़ॉर्मैट्स के लिए आधिकारिक दस्तावेज़ देखें।

**Q: Aspose.CAD for Java में अतिरिक्त एक्सपोर्ट विकल्पों को कैसे संभालूँ?**  
A: लाइब्रेरी कई विकल्प प्रदान करती है जैसे DPI, बैकग्राउंड कलर, और वेक्टर रास्टराइज़ेशन। विवरण के लिए [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) देखें।

**Q: क्या Aspose.CAD for Java के लिए ट्रायल संस्करण उपलब्ध है?**  
A: हाँ, आप [Aspose.CAD Free Trial](https://releases.aspose.com/) से मुफ्त ट्रायल डाउनलोड कर सकते हैं।

**Q: Aspose.CAD for Java से संबंधित सहायता या मुद्दों पर चर्चा कहाँ करूँ?**  
A: समुदाय समर्थन और आधिकारिक उत्तरों के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) देखें।

**Q: Aspose.CAD for Java के लिए अस्थायी लाइसेंस कैसे प्राप्त करूँ?**  
A: अस्थायी लाइसेंस के लिए [Temporary License](https://purchase.aspose.com/temporary-license/) पेज पर दिए गए चरणों का पालन करें।

**अंतिम अपडेट:** 2025-12-03  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.11 (लेखन समय पर नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}