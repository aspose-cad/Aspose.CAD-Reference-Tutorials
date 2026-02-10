---
date: 2025-12-28
description: Aspose.CAD for Java के साथ DWG से PDF बनाना, DWG को PDF के रूप में सहेजना,
  और DWG ड्रॉइंग्स में टेक्स्ट जोड़ना सीखें—स्टेप‑बाय‑स्टेप गाइड।
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java का उपयोग करके DWG से PDF बनाएं और टेक्स्ट जोड़ें
url: /hi/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java का उपयोग करके DWG से PDF बनाएं और टेक्स्ट जोड़ें

## परिचय

यदि आपको **DWG से PDF बनाना** है और साथ ही कस्टम टेक्स्ट डालना है, तो आप सही जगह पर हैं। इस ट्यूटोरियल में हम पूरी प्रक्रिया को चरण‑बद्ध तरीके से देखेंगे—DWG ड्राइंग लोड करना, टेक्स्ट एनोटेशन जोड़ना, और अंत में Aspose.CAD for Java का उपयोग करके परिणाम को PDF के रूप में सेव करना। अंत तक आप समझ जाएंगे कि **DWG को PDF के रूप में सेव** कैसे करें, टेक्स्ट की ऊँचाई कैसे कस्टमाइज़ करें, और बुनियादी एनोटेशन कैसे जोड़ें।

## त्वरित उत्तर
- **क्या मैं Java में DWG को PDF में बदल सकता हूँ?** हाँ, Aspose.CAD for Java एक सरल API प्रदान करता है।  
- **उत्पादन उपयोग के लिए लाइसेंस चाहिए?** एक वाणिज्यिक लाइसेंस आवश्यक है; एक मुफ्त ट्रायल उपलब्ध है।  
- **DWG में टेक्स्ट जोड़ने की विधि कौन सी है?** `CadText` ऑब्जेक्ट का उपयोग करें और इसे मॉडल स्पेस में जोड़ें।  
- **क्या मैं टेक्स्ट की ऊँचाई सेट कर सकता हूँ?** बिल्कुल—`CadText` इंस्टेंस पर `setTextHeight()` का उपयोग करें।  
- **क्या आउटपुट वेक्टर‑आधारित है?** जब रास्टराइज़ेशन विकल्प `UseObjectColor` पर सेट होते हैं, तो PDF उच्च‑गुणवत्ता वाला वेक्टर डेटा रखता है।

## पूर्वापेक्षाएँ

ट्यूटोरियल शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित चीज़ें उपलब्ध हों:

- Aspose.CAD for Java लाइब्रेरी: लाइब्रेरी को [Aspose.CAD for Java पेज](https://releases.aspose.com/cad/java/) से डाउनलोड और इंस्टॉल करें।

- Java Development Kit (JDK): सुनिश्चित करें कि आपके सिस्टम पर नवीनतम JDK स्थापित है।

- DWG ड्राइंग: वह DWG फ़ाइल तैयार रखें जिसमें आप टेक्स्ट जोड़ना चाहते हैं।

## नेमस्पेस आयात करें

अपने Java कोड में Aspose.CAD के आवश्यक नेमस्पेस आयात करें:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

अब, प्रदान किए गए कोड स्निपेट को कई चरणों में विभाजित करते हैं:

## चरण 1: दस्तावेज़ निर्देशिका और DWG फ़ाइल पथ सेट करें

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

## चरण 7: संशोधित DWG को PDF के रूप में सेव करें (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

इन चरणों का पालन करके आप **DWG से PDF बना** सकते हैं, कस्टम टेक्स्ट जोड़ सकते हैं, और टेक्स्ट की ऊँचाई नियंत्रित कर सकते हैं—सिर्फ कुछ ही लाइनों के Java कोड के साथ।

## DWG में टेक्स्ट क्यों जोड़ें और PDF में बदलें?

DWG फ़ाइल में सीधे टेक्स्ट जोड़ना कई कारणों से उपयोगी है:

- **डिज़ाइन पर नोट्स या पार्ट नंबर** के साथ मार्किंग करना।  
- **प्रिंटेबल दस्तावेज़ बनाना** जहाँ PDF एक रीड‑ओनली, व्यापक रूप से समर्थित फ़ॉर्मेट के रूप में कार्य करता है।  
- **बड़ी CAD लाइब्रेरी की बैच प्रोसेसिंग को स्वचालित करना** बिना मैन्युअल एडिटिंग के।

## सामान्य समस्याएँ और सुझाव

- **टेक्स्ट नहीं दिख रहा?** X/Y निर्देशांक ड्राइंग की सीमाओं के भीतर हैं और लेयर दृश्यमान है, यह जांचें।  
- **टेक्स्ट की ऊँचाई गलत?** `setTextHeight()` को समायोजित करें; मान ड्राइंग की यूनिट सिस्टम में होता है।  
- **PDF रास्टराइज़्ड दिख रहा है?** `CadDrawTypeMode.UseObjectColor` को सेट रखें ताकि वेक्टर जानकारी बनी रहे।  
- **बड़ी फ़ाइलों पर प्रदर्शन?** `pageHeight`/`pageWidth` को केवल आवश्यकतानुसार बढ़ाएँ; बड़े मान अधिक मेमोरी उपयोग करते हैं।

## अक्सर पूछे जाने वाले प्रश्न

**प्र: क्या Aspose.CAD सभी DWG फ़ाइल संस्करणों के साथ संगत है?**  
उ: Aspose.CAD विभिन्न DWG संस्करणों को सपोर्ट करता है, जिससे यह कई CAD सॉफ़्टवेयर के साथ संगत रहता है।

**प्र: क्या मैं जोड़े गए टेक्स्ट का फ़ॉन्ट और फ़ॉर्मेट कस्टमाइज़ कर सकता हूँ?**  
उ: हाँ, आप Aspose.CAD का उपयोग करके DWG फ़ाइलों में जोड़े गए टेक्स्ट के फ़ॉन्ट, शैली और अन्य फ़ॉर्मेटिंग विकल्पों को कस्टमाइज़ कर सकते हैं।

**प्र: क्या Aspose.CAD for Java का मुफ्त ट्रायल उपलब्ध है?**  
उ: हाँ, आप [यहाँ](https://releases.aspose.com/) से Aspose.CAD का मुफ्त ट्रायल प्राप्त कर सकते हैं।

**प्र: Aspose.CAD for Java के विस्तृत दस्तावेज़ कहाँ मिलेंगे?**  
उ: विस्तृत जानकारी और उदाहरणों के लिए दस्तावेज़ीकरण देखें: [यहाँ](https://reference.aspose.com/cad/java/)।

**प्र: Aspose.CAD के लिए सपोर्ट या मदद कैसे प्राप्त करूँ?**  
उ: सहायता और समुदाय से जुड़ने के लिए [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) पर जाएँ।

---

**अंतिम अपडेट:** 2025-12-28  
**परीक्षण किया गया:** Aspose.CAD for Java 24.12  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}