---
date: 2025-12-09
description: dwg ट्रैकिंग जावा को कैसे सक्षम करें और Aspose.CAD के साथ जावा द्वारा
  dxf को pdf में कैसे परिवर्तित करें, यह जानें। यह चरण‑दर‑चरण गाइड सहयोगी CAD प्रोजेक्ट्स
  के लिए पूर्ण कार्यप्रवाह दिखाता है।
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Aspose.CAD का उपयोग करके जावा में DWG फ़ाइलों में ट्रैकिंग सक्षम करें
url: /hi/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD के साथ Java में DWG फ़ाइलों में ट्रैकिंग सक्षम करें

## परिचय

आधुनिक CAD कार्यप्रवाहों में, **enable dwg tracking java** सक्षम करना उन टीमों के लिए आवश्यक है जिन्हें परिवर्तन मॉनिटर करने, त्रुटियों को जल्दी पकड़ने, और सभी हितधारकों को एक ही पृष्ठ पर रखने की आवश्यकता होती है। यह ट्यूटोरियल आपको Aspose.CAD for Java का उपयोग करके DWG फ़ाइलों के लिए ट्रैकिंग चालू करने के सटीक चरणों के माध्यम से ले जाता है, और इस प्रक्रिया में आप देखेंगे कि **java convert dxf pdf** कैसे निर्यात प्रक्रिया का हिस्सा बनता है। अंत तक, आपके पास एक तैयार‑चलाने योग्य स्निपेट होगा जो न केवल रूपांतरण करता है बल्कि किसी भी रेंडरिंग समस्या की रिपोर्ट भी करता है।

## त्वरित उत्तर
- **enable dwg tracking java क्या करता है?** यह Aspose.CAD के एरर‑हैंडलिंग कॉलबैक को सक्रिय करता है जिससे आप निर्यात के दौरान रेंडरिंग समस्याएँ देख सकते हैं।  
- **क्या मुझे लाइसेंस चाहिए?** परीक्षण के लिए एक ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं DXF को PDF में भी बदल सकता हूँ?** हाँ – DWG के लिए उपयोग किए गए वही `PdfOptions` DXF के लिए भी काम करता है, जिससे *java convert dxf pdf* परिदृश्य पूरा होता है।  
- **कौन सा JDK संस्करण आवश्यक है?** Java 8 या उससे ऊपर।  
- **और उदाहरण कहाँ मिलेंगे?** नीचे लिंक किए गए Aspose.CAD Java Documentation देखें।  

## enable dwg tracking java क्या है?
Java एप्लिकेशन में DWG ट्रैकिंग सक्षम करना इसका अर्थ है एक कस्टम रेंडर हैंडलर संलग्न करना जो CAD फ़ाइल को रास्टराइज़ या निर्यात करते समय चेतावनियाँ, त्रुटियाँ और अन्य निदान जानकारी कैप्चर करता है। यह दृश्यता डेवलपर्स को रूपांतरण पाइपलाइन को डिबग करने में मदद करती है और उच्च गुणवत्ता वाले डिलिवरेबल्स सुनिश्चित करती है।

## Java के लिए Aspose.CAD क्यों उपयोग करें?
- **पूर्ण‑फ़ीचर CAD समर्थन** – DWG, DXF, DGN, और अधिक।  
- **कोई बाहरी निर्भरताएँ नहीं** – शुद्ध Java लाइब्रेरी, सर्वर‑साइड ऑटोमेशन के लिए आदर्श।  
- **इन‑बिल्ट ट्रैकिंग** – `CadRenderHandler` के माध्यम से विस्तृत रेंडर परिणाम।  
- **आसान PDF निर्यात** – वेक्टर डेटा को संरक्षित रखते हुए एक‑लाइन रूपांतरण।  

## पूर्वापेक्षाएँ

इम्प्लीमेंटेशन में डुबकी लगाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- Java Development Kit (JDK): सुनिश्चित करें कि आपके सिस्टम पर Java स्थापित है।  
- Aspose.CAD for Java: Aspose.CAD for Java को [download link](https://releases.aspose.com/cad/java/) से डाउनलोड और इंस्टॉल करें।  
- Document Directory: वह डायरेक्टरी तैयार करें जहाँ आपकी DWG फ़ाइलें स्थित हैं।

## नेमस्पेस आयात करें

अपने Java प्रोजेक्ट में, Aspose.CAD कार्यक्षमताओं का उपयोग करने के लिए आवश्यक नेमस्पेस आयात करके शुरू करें:

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

## चरण 1: DWG फ़ाइल लोड करें

DWG (या DXF) फ़ाइल को अपने Java एप्लिकेशन में लोड करके शुरू करें। फ़ाइल पथ को तदनुसार समायोजित करें:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## चरण 2: PDF निर्यात विकल्प कॉन्फ़िगर करें

PDF निर्यात विकल्प सेट करें, CAD के लिए वेक्टर रास्टराइज़ेशन विकल्प निर्दिष्ट करें। यह *java convert dxf pdf* क्षमता भी दर्शाता है:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## चरण 3: ट्रैकिंग लागू करें

एक कस्टम एरर हैंडलर क्लास का उपयोग करके ट्रैकिंग लागू करें। यह क्लास रेंडरिंग समस्याओं को कैप्चर करेगा और उन्हें कंसोल में प्रदर्शित करेगा:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## चरण 4: PDF में निर्यात करें

DWG/DXF फ़ाइल को PDF में रूपांतरित करने के लिए निर्यात प्रक्रिया शुरू करें, जिसमें ट्रैकिंग सक्षम हो:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## चरण 5: CadRenderHandler क्लास

`ErrorHandler` क्लास (जो `CadRenderHandler` को एक्सटेंड करता है) को परिभाषित करें ताकि रेंडरिंग परिणामों को प्रोसेस किया जा सके और ट्रैकिंग जानकारी आउटपुट की जा सके:

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

- **`RenderResult` पर `NullPointerException`** – सुनिश्चित करें कि आप Aspose.CAD संस्करण 23.10 या बाद का उपयोग कर रहे हैं; पुराने रिलीज़ में `RenderResult` API नहीं है।  
- **फ़ाइल नहीं मिली** – पुष्टि करें कि `dataDir` सही फ़ोल्डर की ओर इशारा कर रहा है और फ़ाइल नाम बिल्कुल मेल खाता है, केस सहित।  
- **ट्रैकिंग आउटपुट गायब** – पुष्टि करें कि कस्टम `ErrorHandler` सही ढंग से `cadRasterizationOptions.RenderResult` को असाइन किया गया है।  

## अक्सर पूछे जाने वाले प्रश्न

**Q:** क्या मैं Aspose.CAD for Java का उपयोग करके अन्य CAD फ़ाइल फ़ॉर्मैट्स के लिए ट्रैकिंग सक्षम कर सकता हूँ?  
**A:** Aspose.CAD मुख्यतः DWG ट्रैकिंग का समर्थन करता है। अन्य फ़ॉर्मैट्स के लिए आधिकारिक दस्तावेज़ देखें।

**Q:** Aspose.CAD for Java में अतिरिक्त निर्यात विकल्पों को कैसे संभालूँ?  
**A:** विस्तृत दस्तावेज़ीकरण को [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) पर देखें।

**Q:** क्या Aspose.CAD for Java के लिए कोई ट्रायल संस्करण उपलब्ध है?  
**A:** हाँ, आप ट्रायल संस्करण को [Aspose.CAD Free Trial](https://releases.aspose.com/) से एक्सेस कर सकते हैं।

**Q:** Aspose.CAD for Java से संबंधित सहायता या मुद्दों पर चर्चा कहाँ करूँ?  
**A:** समुदाय समर्थन के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

**Q:** Aspose.CAD for Java के लिए अस्थायी लाइसेंस कैसे प्राप्त करूँ?  
**A:** प्रक्रिया के लिए [Temporary License](https://purchase.aspose.com/temporary-license/) देखें।

## निष्कर्ष

Aspose.CAD के साथ Java में DWG ट्रैकिंग सक्षम करने से न केवल रूपांतरण समस्याओं में दृश्यता मिलती है बल्कि सहयोगी डिज़ाइन कार्यप्रवाह भी सुगम होते हैं। ऊपर दिए गए चरणों का पालन करके आप **enable dwg tracking java** कर सकते हैं, DXF को PDF में बदल सकते हैं, और किसी भी रेंडरिंग समस्या को सहजता से संभाल सकते हैं।

---

**Last Updated:** 2025-12-09  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}