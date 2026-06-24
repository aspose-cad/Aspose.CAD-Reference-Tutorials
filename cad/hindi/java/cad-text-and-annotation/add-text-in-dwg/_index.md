---
date: 2026-02-28
description: Aspose.CAD for Java के साथ DWG से PDF बनाना, DWG को PDF के रूप में सहेजना,
  और DWG ड्रॉइंग्स में टेक्स्ट जोड़ना सीखें—स्टेप‑बाय‑स्टेप गाइड।
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: DWG से PDF बनाएं और Aspose.CAD for Java का उपयोग करके टेक्स्ट जोड़ें
url: /hi/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java का उपयोग करके DWG से PDF बनाएं और टेक्स्ट जोड़ें

## परिचय

यदि आपको **DWG फ़ाइलों से PDF बनाना** है और साथ ही कस्टम टेक्स्ट डालना है, तो आप सही जगह पर हैं। इस ट्यूटोरियल में हम पूरी प्रक्रिया को समझेंगे—DWG ड्रॉइंग लोड करना, टेक्स्ट एनोटेशन जोड़ना, और अंत में परिणाम को Aspose.CAD for Java का उपयोग करके PDF के रूप में सहेजना। अंत तक आप समझ जाएंगे कि **DWG को PDF के रूप में कैसे सहेजें**, टेक्स्ट की ऊँचाई कैसे कस्टमाइज़ करें, और बेसिक एनोटेशन कैसे जोड़ें।

## त्वरित उत्तर
- **क्या मैं Java में DWG को PDF में बदल सकता हूँ?** हाँ, Aspose.CAD for Java एक सरल API प्रदान करता है।  
- **उत्पादन उपयोग के लिए लाइसेंस चाहिए?** एक व्यावसायिक लाइसेंस आवश्यक है; एक फ्री ट्रायल उपलब्ध है।  
- **DWG में टेक्स्ट जोड़ने की विधि कौन सी है?** `CadText` ऑब्जेक्ट का उपयोग करें और इसे मॉडल स्पेस में जोड़ें।  
- **क्या मैं टेक्स्ट की ऊँचाई सेट कर सकता हूँ?** बिल्कुल—`CadText` इंस्टेंस पर `setTextHeight()` का उपयोग करें।  
- **क्या आउटपुट वेक्टर‑आधारित है?** जब रास्टराइज़ेशन विकल्प `UseObjectColor` पर सेट होते हैं, तो PDF उच्च‑गुणवत्ता वाला वेक्टर डेटा बनाए रखता है।

## “DWG से PDF बनाना” क्या है?
DWG ड्रॉइंग से PDF बनाना का अर्थ है मूल CAD फ़ॉर्मेट को एक व्यापक रूप से समर्थित, केवल‑पढ़ने योग्य दस्तावेज़ में बदलना, जबकि मूल ज्यामिति को संरक्षित रखना। यह रूपांतरण तब आवश्यक होता है जब आपको ऐसे स्टेकहोल्डर्स के साथ डिज़ाइन साझा करना हो जिनके पास CAD सॉफ़्टवेयर नहीं है।

## DWG को PDF में बदलने के लिए Aspose.CAD for Java क्यों उपयोग करें?
Aspose.CAD एक शुद्ध‑Java समाधान प्रदान करता है जिसे किसी बाहरी CAD इंस्टॉलेशन की आवश्यकता नहीं होती। यह **DWG को PDF में बदलना** सपोर्ट करता है, वेक्टर फ़िडेलिटी बनाए रखता है, और आपको रूपांतरण से पहले प्रोग्रामेटिक रूप से टेक्स्ट, डाइमेंशन या कस्टम ग्राफ़िक्स जैसी एनोटेशन जोड़ने की सुविधा देता है।

## पूर्वापेक्षाएँ

ट्यूटोरियल शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हों:

- Aspose.CAD for Java लाइब्रेरी: लाइब्रेरी को [Aspose.CAD for Java पेज](https://releases.aspose.com/cad/java/) से डाउनलोड और इंस्टॉल करें।  
- Java Development Kit (JDK): सुनिश्चित करें कि आपके सिस्टम पर नवीनतम JDK स्थापित है।  
- DWG ड्रॉइंग: वह DWG फ़ाइल तैयार रखें जिसमें आप टेक्स्ट जोड़ना चाहते हैं।

## नेमस्पेस इम्पोर्ट करें

अपने Java कोड में Aspose.CAD के लिए आवश्यक नेमस्पेस इम्पोर्ट करें:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

अब, प्रदान किए गए कोड स्निपेट को कई चरणों में विभाजित करते हैं:

## चरण 1: डॉक्यूमेंट डायरेक्टरी और DWG फ़ाइल पाथ सेट करें

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## चरण 2: DWG इमेज लोड करें

```java
Image image = Image.load(dwgPathToFile);
```

## चरण 3: CadText ऑब्जेक्ट बनाएं (DWG में टेक्स्ट जोड़ें)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## चरण 4: CadImage में टेक्स्ट जोड़ें (एनोटेशन डालें)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## चरण 5: PDF विकल्प सेट करें (DWG से PDF बनाने की तैयारी)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## चरण 6: CadRasterizationOptions कॉन्फ़िगर करें (PDF रेंडरिंग नियंत्रित करें)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## चरण 7: संशोधित DWG को PDF के रूप में सहेजें (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

इन चरणों का पालन करके आप **DWG से PDF बना सकते हैं**, कस्टम टेक्स्ट जोड़ सकते हैं, और टेक्स्ट की ऊँचाई को नियंत्रित कर सकते हैं—सिर्फ कुछ ही Java लाइनों के साथ।

## Java में बड़े पैमाने पर DWG को PDF में कैसे बदलें?
यदि आपको **DWG PDF फ़ाइलों को बैच में बदलना** है, तो ऊपर दिया गया कोड एक लूप में रखें जो DWG ड्रॉइंग्स के फ़ोल्डर पर इटरेट करे। आवश्यकतानुसार `pageHeight`/`pageWidth` को ही समायोजित करें ताकि मेमोरी उपयोग कम रहे, और प्रत्येक फ़ाइल के लिए वही `PdfOptions` इंस्टेंस पुन: उपयोग करें जिससे प्रदर्शन बेहतर हो।

## सामान्य समस्याएँ एवं सुझाव

- **टेक्स्ट नहीं दिख रहा?** X/Y कॉर्डिनेट्स ड्रॉइंग की सीमाओं के भीतर हैं और लेयर दृश्यमान है, यह जांचें।  
- **टेक्स्ट की ऊँचाई गलत?** `setTextHeight()` को समायोजित करें; मान ड्रॉइंग की यूनिट सिस्टम में होता है।  
- **PDF रास्टराइज़्ड दिख रहा है?** वेक्टर जानकारी बनाए रखने के लिए `CadDrawTypeMode.UseObjectColor` सेट है, यह सुनिश्चित करें।  
- **बड़ी फ़ाइलों पर प्रदर्शन?** केवल आवश्यक होने पर ही `pageHeight`/`pageWidth` बढ़ाएँ; बड़े मान अधिक मेमोरी खपत करते हैं।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या Aspose.CAD सभी संस्करणों की DWG फ़ाइलों के साथ संगत है?**  
उत्तर: Aspose.CAD विभिन्न DWG संस्करणों को सपोर्ट करता है, जिससे यह कई CAD सॉफ़्टवेयर के साथ संगत रहता है।

**प्रश्न: क्या मैं जोड़े गए टेक्स्ट का फ़ॉन्ट और फ़ॉर्मेट कस्टमाइज़ कर सकता हूँ?**  
उत्तर: हाँ, आप Aspose.CAD का उपयोग करके DWG फ़ाइलों में जोड़े गए टेक्स्ट के फ़ॉन्ट, स्टाइल और अन्य फ़ॉर्मेटिंग विकल्पों को कस्टमाइज़ कर सकते हैं।

**प्रश्न: क्या Aspose.CAD for Java के लिए फ्री ट्रायल उपलब्ध है?**  
उत्तर: हाँ, आप [यहाँ](https://releases.aspose.com/) से Aspose.CAD का फ्री ट्रायल प्राप्त कर सकते हैं।

**प्रश्न: Aspose.CAD for Java की विस्तृत डॉक्यूमेंटेशन कहाँ मिल सकती है?**  
उत्तर: विस्तृत जानकारी और उदाहरणों के लिए डॉक्यूमेंटेशन को [यहाँ](https://reference.aspose.com/cad/java/) देखें।

**प्रश्न: मैं Aspose.CAD के लिए सपोर्ट या मदद कैसे प्राप्त कर सकता हूँ?**  
उत्तर: सहायता और समुदाय से जुड़ने के लिए [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) पर जाएँ।

---

**अंतिम अपडेट:** 2026-02-28  
**परीक्षित संस्करण:** Aspose.CAD for Java 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}