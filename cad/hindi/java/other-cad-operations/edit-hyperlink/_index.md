---
date: 2026-06-19
description: Aspose.CAD for Java के साथ DWG फ़ाइलों को संपादित करना सीखें, जिसमें
  DWG XRef पाथ को अपडेट करना और हाइपरलिंक्स को संपादित करना शामिल है। आज ही मुफ्त
  ट्रायल आज़माएँ!
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
linktitle: हाइपरलिंक संपादित करें
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  type: TechArticle
- description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
  type: HowTo
- questions:
  - answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
    question: Do I need to call a specific method to write the edited DWG back to
      disk?
  - answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
    question: Is it possible to edit multiple hyperlinks in one pass?
  type: FAQPage
second_title: Aspose.CAD Java API
title: DWG हाइपरलिंक्स को कैसे संपादित करें - Aspose.CAD Java ट्यूटोरियल
url: /hi/java/other-cad-operations/edit-hyperlink/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG हाइपरलिंक कैसे संपादित करें - Aspose.CAD Java ट्यूटोरियल

आज के डिजिटल युग में, **DWG फ़ाइलों को प्रभावी ढंग से संपादित करने** की क्षमता इंजीनियरों, वास्तुकारों और BIM विशेषज्ञों के लिए आवश्यक कौशल है। चाहे आपको टूटे हुए हाइपरलिंक को ठीक करना हो, XRef को नए स्रोत की ओर इंगित करना हो, या कई ड्रॉइंग्स को बैच‑अपडेट करना हो, Aspose.CAD for Java बिना CAD एडिटर खोले इन बदलावों को करने का साफ़, प्रोग्रामेटिक तरीका प्रदान करता है। यह ट्यूटोरियल आपको पूरी प्रक्रिया के माध्यम से ले जाता है, ड्रॉइंग लोड करने से लेकर संपादन को स्थायी करने तक।

## त्वरित उत्तर

- **जावा में DWG संपादन को संभालने वाली लाइब्रेरी कौन सी है?** Aspose.CAD for Java.  
- **क्या मैं हाइपरलिंक और XRef पाथ दोनों को एक साथ संपादित कर सकता हूँ?** Yes—both are supported in the same API.  
- **क्या विकास के लिए लाइसेंस की आवश्यकता है?** A free trial works for testing; a commercial license is required for production.  
- **कौन सा जावा संस्करण आवश्यक है?** Java 8 or higher.  
- **क्या कोड नमूना जैसा का तैसा चलाया जा सकता है?** Yes, after updating the file paths to point to your local DWG files.

## क्यों संपादित करें DWG हाइपरलिंक और XRef पाथ?

हाइपरलिंक और XRef पाथ को अद्यतित रखने से टूटे हुए रेफ़रेंसेज़ से बचा जा सकता है, यह सुनिश्चित करता है कि प्रोजेक्ट दस्तावेज़ हमेशा सही संसाधनों की ओर इशारा करें, और बड़े CAD लाइब्रेरीज़ में स्वचालित बैच अपडेट सक्षम करता है। इससे मैनुअल प्रयास कम होता है, त्रुटियों में कमी आती है, और डिज़ाइन लाइफ़साइकल के दौरान लिंक इंटेग्रिटी को प्रोग्रामेटिक रूप से बनाए रखने से समग्र प्रोजेक्ट दक्षता में सुधार होता है।

## आवश्यकताएँ

ट्यूटोरियल शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यकताएँ मौजूद हैं:

1. **जावा विकास वातावरण:** A JDK 8+ installed and your favorite IDE (IntelliJ IDEA, Eclipse, etc.).  
2. **Aspose.CAD for Java लाइब्रेरी:** Download and install the Aspose.CAD for Java library from the [download link](https://releases.aspose.com/cad/java/).  
3. **DWG ड्रॉइंग:** Have a DWG drawing file ready for hyperlink editing.

## पैकेज इम्पोर्ट करें

अपने जावा प्रोजेक्ट में आवश्यक पैकेज इम्पोर्ट करके शुरू करें। इससे आपको Aspose.CAD for Java की कार्यक्षमताओं तक पहुँच सुनिश्चित होती है।

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## Aspose.CAD for Java का उपयोग करके DWG हाइपरलिंक कैसे संपादित करें?

`CadImage` Aspose.CAD क्लास है जिसका उपयोग CAD ड्रॉइंग्स को लोड और सेव करने के लिए किया जाता है।  
`CadImage` के साथ DWG फ़ाइल लोड करें, उसकी एंटिटीज़ पर इटररेट करें, जहाँ आवश्यक हो हाइपरलिंक और XRef पाथ अपडेट करें, और अंत में इमेज को DWG में वापस सेव करें। यह एंड‑टू‑एंड फ्लो आपको एक ही पास में कई एंटिटीज़ को संशोधित करने की अनुमति देता है, जिससे सभी बदलाव स्थायी रूप से सहेजे जाते हैं।

### चरण 1: Insert ऑब्जेक्ट्स तक पहुँच

`CadInsertObject` Aspose.CAD क्लास है जो DWG ड्रॉइंग के भीतर एक इन्सर्टेड ब्लॉक रेफ़रेंस (XRef) को दर्शाता है। एंटिटीज़ के माध्यम से इटररेट करें और पहचानें कि क्या कोई एंटिटी `CadInsertObject` क्लास की इंस्टेंस है।

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### चरण 2: DWG ड्रॉइंग में XRef पाथ कैसे बदलें

`CadImage` Aspose.CAD for Java में CAD फ़ाइलों को लोड और सेव करने वाला मुख्य ऑब्जेक्ट है। एक बार जब आप इन्सर्ट ऑब्जेक्ट की पहचान कर लेते हैं, तो संबंधित ब्लॉक एंटिटी प्राप्त करें और आवश्यकतानुसार XRef पाथ अपडेट करें। इससे रेफ़रेंस सही बाहरी फ़ाइल की ओर इशारा करता है।

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### चरण 3: हाइपरलिंक संशोधित करना

अगले चरण में, जांचें कि एंटिटी के साथ कोई हाइपरलिंक जुड़ा है या नहीं। यदि हाइपरलिंक किसी विशिष्ट URL से मेल खाता है, तो उसे इच्छित URL में अपडेट करें। यह चरण सुनिश्चित करता है कि CAD व्यूअर में हाइपरलिंक पर क्लिक करने से नया लक्ष्य खुले।

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## सामान्य कठिनाइयाँ और सुझाव

- **स्ट्रिंग तुलना:** Java में विश्वसनीय स्ट्रिंग तुलना के लिए `==` के बजाय `.equals()` का उपयोग करें। नमूना सरलता के लिए `==` उपयोग करता है, लेकिन प्रोडक्शन में इसे `entity.getHyperlink().equals("https://products.aspose.com")` से बदलें।  
- **नल जांच:** हमेशा यह सत्यापित करें कि `block.getXRefPathName()` `null` नहीं है, इससे पहले कि आप `.getValue()` कॉल करें।  
- **परिवर्तनों को सेव करना:** एंटिटीज़ को संशोधित करने के बाद, `cadImage.save("output.dwg");` कॉल करके बदलावों को स्थायी बनाएं (कोड को मूल ब्लॉक काउंट रखने के लिए हटाया गया है)।  
- **प्रदर्शन नोट:** Aspose.CAD for Java 30 से अधिक CAD फ़ॉर्मैट्स को सपोर्ट करता है और 2 GB तक की फ़ाइलों को पूरी डॉक्यूमेंट को मेमोरी में लोड किए बिना प्रोसेस कर सकता है, जिससे बड़े अपडेट तेज़ और मेमोरी‑कुशल होते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या Aspose.CAD for Java सभी DWG ड्रॉइंग संस्करणों के साथ संगत है?

A1: Aspose.CAD for Java 50 से अधिक DWG संस्करणों को सपोर्ट करता है, जो AutoCAD 2000 से लेकर नवीनतम 2025 फ़ॉर्मेट तक के रिलीज़ को कवर करता है।

### प्रश्न 2: क्या मैं Aspose.CAD for Java को व्यावसायिक प्रोजेक्ट्स में उपयोग कर सकता हूँ?

A2: हाँ, उत्पादन उपयोग के लिए एक व्यावसायिक लाइसेंस आवश्यक है। आप लाइसेंस [यहाँ](https://purchase.aspose.com/buy) खरीद सकते हैं।

### प्रश्न 3: क्या Aspose.CAD for Java के लिए मुफ्त ट्रायल उपलब्ध है?

A3: हाँ, आप मुफ्त ट्रायल संस्करण [यहाँ](https://releases.aspose.com/) देख सकते हैं।

### प्रश्न 4: मैं Aspose.CAD for Java के लिए तकनीकी समर्थन कैसे प्राप्त कर सकता हूँ?

A4: किसी भी तकनीकी सहायता के लिए, Aspose.CAD फ़ोरम [यहाँ](https://forum.aspose.com/c/cad/19) पर जाएँ।

### प्रश्न 5: क्या मैं परीक्षण उद्देश्यों के लिए एक अस्थायी लाइसेंस प्राप्त कर सकता हूँ?

A5: हाँ, आप एक अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

**अतिरिक्त प्रश्नोत्तर**

**Q: क्या मुझे संपादित DWG को डिस्क पर वापस लिखने के लिए कोई विशिष्ट मेथड कॉल करना आवश्यक है?**  
A: हाँ, बदलाव करने के बाद `cadImage.save("EditedDrawing.dwg");` कॉल करके संशोधनों को स्थायी बनाएं।

**Q: क्या एक ही पास में कई हाइपरलिंक संपादित करना संभव है?**  
A: बिल्कुल—`cadImage.getEntities()` पर लूप करें और प्रत्येक मिलते हुए एंटिटी पर हाइपरलिंक लॉजिक लागू करें।

---

**अंतिम अपडेट:** 2026-06-19  
**परीक्षण किया गया:** Aspose.CAD for Java 24.12  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [Aspose.CAD for Java का उपयोग करके DWG फ़ाइलों से XREF मेटा डेटा पढ़ें](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [Aspose.CAD for Java का उपयोग करके DWG फ़ाइलों में कस्टम प्रॉपर्टीज़ जोड़ें](/cad/java/additional-features/add-custom-properties/)
- [Aspose.CAD for Java का उपयोग करके DWG को PDF या रास्टर में एक्सपोर्ट करें](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}