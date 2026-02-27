---
date: 2026-02-10
description: Aspose.CAD for Java का उपयोग करके DWG फ़ाइलों में ट्रैकिंग सक्षम करने
  और कस्टम एरर हैंडलर के साथ DXF को PDF में परिवर्तित करने के लिए चरण‑दर‑चरण गाइड।
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: जावा में Aspose.CAD का उपयोग करके DWG फ़ाइलों में ट्रैकिंग कैसे सक्षम करें
url: /hi/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD in Java का उपयोग करके DWG फ़ाइलों में ट्रैकिंग कैसे सक्षम करें

## परिचय

यदि आप सहयोगी CAD प्रोजेक्ट्स पर काम कर रहे हैं, तो अपने DWG वर्कफ़्लो में **how to enable tracking** को जानना एक गेम‑चेंजर है। यह आपको रेंडरिंग समस्याओं की रीयल‑टाइम जानकारी देता है, आपको कन्वर्ज़न गड़बड़ियों को जल्दी पकड़ने में मदद करता है, और सभी हितधारकों को सूचित रखता है। इस ट्यूटोरियल में हम Aspose.CAD for Java के साथ ट्रैकिंग सक्षम करने के सटीक चरणों को दिखाएंगे, और साथ ही **how to convert DXF to PDF** को उसी पाइपलाइन का हिस्सा बनाकर प्रदर्शित करेंगे। अंत तक आपके पास एक पूर्ण, प्रोडक्शन‑रेडी स्निपेट होगा जो ड्रॉइंग्स को एक्सपोर्ट करते समय **custom error handler Java** क्लास के माध्यम से त्रुटियों की रिपोर्ट करता है।

## त्वरित उत्तर
- **What does “enable dwg tracking java” do?** यह Aspose.CAD के एरर‑हैंडलिंग कॉलबैक्स को सक्रिय करता है जिससे आप एक्सपोर्ट के दौरान रेंडरिंग समस्याओं को देख सकते हैं।  
- **Do I need a license?** परीक्षण के लिए ट्रायल काम करता है; प्रोडक्शन के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **Can I also convert DXF to PDF?** हाँ – DWG के लिए उपयोग किए गए वही `PdfOptions` DXF के लिए भी काम करता है, जो *java convert dxf pdf* परिदृश्य को पूरा करता है।  
- **Which JDK version is required?** Java 8 या उससे ऊपर।  
- **Where can I find more examples?** नीचे लिंक किए गए Aspose.CAD Java Documentation देखें।  

## Aspose.CAD का उपयोग करके DWG फ़ाइलों में ट्रैकिंग कैसे सक्षम करें

Java एप्लिकेशन में DWG ट्रैकिंग सक्षम करने का मतलब है एक कस्टम रेंडर हैंडलर संलग्न करना जो CAD फ़ाइल के रास्टराइज़ या एक्सपोर्ट होने के दौरान चेतावनियों, त्रुटियों और अन्य डायग्नोस्टिक जानकारी को कैप्चर करता है। यह दृश्यता डेवलपर्स को कन्वर्ज़न पाइपलाइन को डिबग करने में मदद करती है और उच्च‑गुणवत्ता वाले डिलिवरेबल्स सुनिश्चित करती है।

## Aspose.CAD for Java का उपयोग क्यों करें?

- **Full‑feature CAD support** – DWG, DXF, DGN, और अधिक।  
- **No external dependencies** – शुद्ध Java लाइब्रेरी, सर्वर‑साइड ऑटोमेशन के लिए आदर्श।  
- **Built‑in tracking** – `CadRenderHandler` के माध्यम से विस्तृत रेंडर परिणाम।  
- **Easy PDF export** – वेक्टर डेटा को संरक्षित रखते हुए एक‑लाइन कन्वर्ज़न।  

## पूर्वापेक्षाएँ

इम्प्लीमेंटेशन में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- Java Development Kit (JDK): सुनिश्चित करें कि आपके सिस्टम पर Java स्थापित है।  
- Aspose.CAD for Java: Aspose.CAD for Java को [download link](https://releases.aspose.com/cad/java/) से डाउनलोड और इंस्टॉल करें।  
- Document Directory: एक डायरेक्टरी तैयार करें जहाँ आपके DWG फ़ाइलें स्थित हों।  

## Namespaces आयात करें

अपने Java प्रोजेक्ट में, Aspose.CAD कार्यक्षमताओं का उपयोग करने के लिए आवश्यक namespaces को आयात करके शुरू करें:

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

पहले DWG (या DXF) फ़ाइल को अपने Java एप्लिकेशन में लोड करें। फ़ाइल पथ को तदनुसार समायोजित करें:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## चरण 2: PDF एक्सपोर्ट विकल्प कॉन्फ़िगर करें (How to Convert DXF to PDF)

PDF एक्सपोर्ट विकल्प सेट करें, CAD के लिए वेक्टर रास्टराइज़ेशन विकल्प निर्दिष्ट करें। यह *java convert dxf pdf* क्षमता को भी दर्शाता है:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## चरण 3: ट्रैकिंग लागू करें (Custom Error Handler Java)

कस्टम एरर हैंडलर क्लास का उपयोग करके ट्रैकिंग लागू करें। यह क्लास रेंडरिंग समस्याओं को कैप्चर करेगा और उन्हें कंसोल में प्रदर्शित करेगा:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## चरण 4: PDF में एक्सपोर्ट करें

ट्रैकिंग सक्षम करते हुए DWG/DXF फ़ाइल को PDF में कन्वर्ट करने के लिए एक्सपोर्ट प्रक्रिया शुरू करें:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## चरण 5: CadRenderHandler क्लास

`ErrorHandler` क्लास को परिभाषित करें (`CadRenderHandler` को एक्स्टेंड करते हुए) ताकि रेंडरिंग परिणामों को प्रोसेस किया जा सके और ट्रैकिंग जानकारी आउटपुट की जा सके:

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

## यह क्यों महत्वपूर्ण है

ट्रैकिंग सक्षम करने से आपको प्रत्येक कन्वर्ज़न चरण का स्पष्ट ऑडिट ट्रेल मिलता है। यह विशेष रूप से नियामक उद्योगों (आर्किटेक्चर, इंजीनियरिंग, कंस्ट्रक्शन) में मूल्यवान है जहाँ सटीक रेंडरिंग का प्रमाण अनुपालन ऑडिट के लिए आवश्यक होता है। कस्टम एरर हैंडलर आपको समस्याओं को मॉनिटरिंग सिस्टम में लॉग करने या ऑटोमेटेड रीट्राई ट्रिगर करने का हुक भी प्रदान करता है।

## सामान्य समस्याएँ और समाधान

- **`NullPointerException` on `RenderResult`** – सुनिश्चित करें कि आप Aspose.CAD संस्करण 23.10 या बाद का उपयोग कर रहे हैं; पुराने रिलीज़ में `RenderResult` API नहीं है।  
- **File not found** – पुष्टि करें कि `dataDir` सही फ़ोल्डर की ओर इशारा कर रहा है और फ़ाइल नाम बिल्कुल मेल खाता है, केस सहित।  
- **Missing tracking output** – पुष्टि करें कि कस्टम `ErrorHandler` सही ढंग से `cadRasterizationOptions.RenderResult` को असाइन किया गया है।  

## अक्सर पूछे जाने वाले प्रश्न

**Q:** क्या मैं Aspose.CAD for Java का उपयोग करके अन्य CAD फ़ाइल फ़ॉर्मेट्स के लिए ट्रैकिंग सक्षम कर सकता हूँ?  
A: Aspose.CAD मुख्यतः DWG ट्रैकिंग का समर्थन करता है। अन्य फ़ॉर्मेट्स के लिए आधिकारिक दस्तावेज़ देखें।

**Q:** Aspose.CAD for Java में अतिरिक्त एक्सपोर्ट विकल्पों को कैसे संभालूँ?  
A: विस्तृत दस्तावेज़ीकरण देखें [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) पर।

**Q:** क्या Aspose.CAD for Java के लिए ट्रायल संस्करण उपलब्ध है?  
A: हाँ, आप ट्रायल संस्करण यहाँ प्राप्त कर सकते हैं: [Aspose.CAD Free Trial](https://releases.aspose.com/)।

**Q:** Aspose.CAD for Java से संबंधित सहायता या मुद्दों पर चर्चा कहाँ कर सकते हैं?  
A: समुदाय समर्थन के लिए [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) पर जाएँ।

**Q:** Aspose.CAD for Java के लिए टेम्पररी लाइसेंस कैसे प्राप्त करें?  
A: प्रक्रिया यहाँ दी गई है: [Temporary License](https://purchase.aspose.com/temporary-license/)।

## निष्कर्ष

Aspose.CAD के साथ Java में DWG ट्रैकिंग सक्षम करने से न केवल आपको कन्वर्ज़न समस्याओं की दृश्यता मिलती है बल्कि सहयोगी डिज़ाइन वर्कफ़्लो भी सुगम होते हैं। ऊपर दिए गए चरणों का पालन करके आप **how to enable tracking** कर सकते हैं, DXF को PDF में कन्वर्ट कर सकते हैं, और किसी भी रेंडरिंग समस्या को सहजता से संभाल सकते हैं।

---

**अंतिम अपडेट:** 2026-02-10  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}