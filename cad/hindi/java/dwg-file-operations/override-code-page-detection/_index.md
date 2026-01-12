---
date: 2026-01-12
description: Aspose.CAD for Java का उपयोग करके DWG फ़ाइलों में स्वचालित कोड पेज डिटेक्शन
  को ओवरराइड करते हुए CAD को PDF में निर्यात करना सीखें। एन्कोडिंग और खराब CIF/MIF
  को संभालता है।
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: CAD को PDF में निर्यात करें – Java के साथ DWG फ़ाइलों में स्वचालित कोड पेज
  डिटेक्शन को ओवरराइड करें
url: /hi/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD को PDF में निर्यात करें – DWG फ़ाइलों में स्वचालित कोड पेज डिटेक्शन को ओवरराइड करें Java के साथ

## परिचय

इस व्यापक गाइड में आप **CAD को PDF में निर्यात करने** का तरीका जानेंगे, जबकि स्वचालित कोड पेज डिटेक्शन को ओवरराइड करेंगे जो DWG फ़ाइलों में टेक्स्ट को भ्रष्ट कर सकता है। Aspose.CAD for Java एन्कोडिंग पर सूक्ष्म नियंत्रण प्रदान करता है, जिससे आप विकृत CIF/MIF डेटा को पुनः प्राप्त कर सकते हैं और विश्वसनीय PDF आउटपुट बना सकते हैं। चाहे आप एक बैच कन्वर्टर बना रहे हों या CAD प्रोसेसिंग को बड़े Java एप्लिकेशन में एकीकृत कर रहे हों, नीचे दिए गए चरण पूरे वर्कफ़्लो को आपके लिए स्पष्ट करेंगे।

## त्वरित उत्तर
- **“ओवरराइड कोड पेज” क्या मतलब है?** यह Aspose.CAD को अनुमान लगाने के बजाय एक विशिष्ट कैरेक्टर एन्कोडिंग उपयोग करने के लिए मजबूर करता है।
- **क्या मैं DWG को सीधे PDF में निर्यात कर सकता हूँ?** हाँ – सही कोड पेज सेट करने के बाद, आप CAD इमेज को PDF के रूप में सहेज सकते हैं।
- **जापानी टेक्स्ट के लिए कौन सा एन्कोडिंग काम करता है?** `CodePages.Japanese` और `MifCodePages.Japanese` सही विकल्प हैं।
- **क्या उत्पादन उपयोग के लिए लाइसेंस चाहिए?** एक व्यावसायिक लाइसेंस आवश्यक है; परीक्षण के लिए एक अस्थायी लाइसेंस उपलब्ध है।
- **Aspose.CAD का कौन सा संस्करण चाहिए?** कोई भी नवीनतम संस्करण जो `LoadOptions` और `PdfOptions` को सपोर्ट करता हो।

## “CAD को PDF में निर्यात करना” क्या है?
CAD को PDF में निर्यात करना वेक्टर‑आधारित CAD ड्रॉइंग्स को एक व्यापक रूप से समर्थित, स्थिर‑लेआउट दस्तावेज़ फ़ॉर्मेट में बदलता है। परिणामी PDF रेखा कार्य, लेयर्स और टेक्स्ट को संरक्षित रखता है, जिससे ड्रॉइंग को साझा करना, प्रिंट करना या अन्य एप्लिकेशन में एम्बेड करना आसान हो जाता है।

## स्वचालित कोड पेज डिटेक्शन को ओवरराइड क्यों करें?
DWG फ़ाइलें अक्सर टेक्स्ट को लेगेसी कोड पेजेज़ में संग्रहीत करती हैं। Aspose.CAD की ऑटो‑डिटेक्शन इन बाइट्स को गलत समझ सकती है, जिससे गड़बड़ अक्षर दिखाई देते हैं। कोड पेज को मैन्युअल रूप से निर्दिष्ट करके आप सुनिश्चित करते हैं कि निर्यातित PDF में टेक्स्ट ठीक वैसा ही दिखे जैसा मूल में था, विशेषकर जापानी, सिरिलिक या अरबी जैसी गैर‑लैटिन स्क्रिप्ट्स के लिए।

## पूर्वापेक्षाएँ
- **Java विकास वातावरण** – JDK 8+ और आपका पसंदीदा IDE।
- **Aspose.CAD for Java** – आधिकारिक साइट से लाइब्रेरी डाउनलोड करें [यहाँ](https://releases.aspose.com/cad/java/)।
- **DWG सैंपल फ़ाइल** – प्रदान की गई `SimpleEntities.dwg` या कोई भी DWG फ़ाइल जिसका आप रूपांतरण करना चाहते हैं, उपयोग करें।

## पैकेज आयात करें
अपने Java प्रोजेक्ट में आवश्यक Aspose.CAD क्लासेस आयात करें:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## चरण‑दर‑चरण मार्गदर्शिका

### चरण 1: Java प्रोजेक्ट सेट अप करें
एक नया Maven या Gradle प्रोजेक्ट बनाएं और Aspose.CAD JAR को क्लासपाथ में जोड़ें। यह चरण IDE को आयातित क्लासेस को सही ढंग से पहचानने में मदद करता है।

### चरण 2: निर्दिष्ट कोड पेज के साथ DWG फ़ाइल लोड करें
Aspose.CAD को बताएं कि कौन सी एन्कोडिंग उपयोग करनी है और क्या विकृत CIF/MIF डेटा की पुनर्प्राप्ति करनी है।

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### चरण 3: CAD इमेज को PDF में निर्यात करें
सही कोड पेज लागू होने के बाद, आप सुरक्षित रूप से ड्रॉइंग को निर्यात कर सकते हैं। `PdfOptions` ऑब्जेक्ट आपको PDF आउटपुट (कम्प्रेशन, रास्टराइज़ेशन आदि) को सूक्ष्म रूप से ट्यून करने की सुविधा देता है।

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### चरण 4: सफलता की पुष्टि करें
एक साधा कंसोल संदेश यह पुष्टि करता है कि प्रक्रिया बिना किसी अपवाद के पूरी हो गई।

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

आप इन चरणों को कई DWG फ़ाइलों के लिए दोहरा सकते हैं, आवश्यकतानुसार स्रोत पथ और आउटपुट नाम को समायोजित कर सकते हैं।

## सामान्य समस्याएँ और समाधान
- **गड़बड़ अक्षर अभी भी दिख रहे हैं:** दोबारा जांचें कि `specifiedEncoding` मूल DWG के कोड पेज से मेल खाता है। आवश्यक होने पर अलग `CodePages` एन्नम का उपयोग करें।
- **`cadImage.save` पर `NullPointerException`:** सुनिश्चित करें कि DWG फ़ाइल सही ढंग से लोड हुई है; पथ और फ़ाइल अनुमतियों की जाँच करें।
- **PDF आकार बड़ा है:** `PdfOptions` में कम्प्रेशन सक्षम करें (उदा., `pdfOptions.setCompress(true)`)।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या Aspose.CAD सभी DWG फ़ाइल संस्करणों के साथ संगत है?**  
A1: Aspose.CAD DWG के कई संस्करणों को सपोर्ट करता है, जिसमें AutoCAD 2018 और उससे पहले के रिलीज़ शामिल हैं।

**Q2: क्या मैं Aspose.CAD को व्यावसायिक प्रोजेक्ट्स में उपयोग कर सकता हूँ?**  
A2: हाँ, उत्पादन उपयोग के लिए एक व्यावसायिक लाइसेंस आवश्यक है। आप लाइसेंस यहाँ [यहाँ](https://purchase.aspose.com/buy) प्राप्त कर सकते हैं।

**Q3: क्या फ्री ट्रायल संस्करण में कोई सीमाएँ हैं?**  
A3: ट्रायल आकार और फीचर प्रतिबंध लगाता है; विस्तृत जानकारी के लिए आधिकारिक दस्तावेज़ देखें।

**Q4: Aspose.CAD के लिए समर्थन कैसे प्राप्त करूँ?**  
A4: सहायता और चर्चा के लिए कम्युनिटी [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) पर जाएँ।

**Q5: क्या परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस उपलब्ध है?**  
A5: हाँ, अस्थायी लाइसेंस यहाँ [यहाँ](https://purchase.aspose.com/temporary-license/) अनुरोध किया जा सकता है।

---

**Last Updated:** 2026-01-12  
**Tested With:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}