---
date: 2026-01-10
description: Aspose.CAD for Java का उपयोग करके DGN को DWG में निर्यात करना और MicroStation
  DGN को AutoCAD DWG में बदलना सीखें। चरण‑दर‑चरण मार्गदर्शिका।
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java के साथ DGN को DWG में निर्यात करें
url: /hi/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java के साथ DGN को DWG में निर्यात करें

## परिचय

इस ट्यूटोरियल में, आप सीखेंगे कि कैसे **export dgn to dwg** किया जाता है और Aspose.CAD लाइब्रेरी for Java का उपयोग करके एक MicroStation DGN डिज़ाइन को AutoCAD DWG फ़ाइल के भीतर एम्बेड किया जाता है। चाहे आप लेगेसी MicroStation ड्रॉइंग्स को माइग्रेट कर रहे हों या DGN अंडरलेज़ को DWG लेआउट्स के साथ संयोजित करने की आवश्यकता हो, यह गाइड आपको हर चरण के माध्यम से ले जाता है—पर्यावरण सेटअप से लेकर अंतिम DWG का PDF प्रीव्यू जनरेट करने तक।

## त्वरित उत्तर
- **export dgn to dwg** क्या प्राप्त करता है? यह DGN अंडरले को DWG में एम्बेड करता है, जिससे AutoCAD में सहज दृश्यता संभव होती है।
- **किस फ़ॉर्मेट में मैं परिणाम को त्वरित प्रीव्यू के लिए निर्यात कर सकता हूँ?** आप `PdfOptions` का उपयोग करके **export cad file to pdf** कर सकते हैं।
- **क्या कोड चलाने के लिए लाइसेंस आवश्यक है?** प्रोडक्शन उपयोग के लिए एक टेम्पररी या पेड Aspose.CAD लाइसेंस आवश्यक है.
- **कौन सा Java संस्करण समर्थित है?** Java 8 या बाद का संस्करण नवीनतम Aspose.CAD for Java रिलीज़ के साथ काम करता है.
- **क्या मुफ्त ट्रायल उपलब्ध है?** हाँ – Aspose वेबसाइट से ट्रायल डाउनलोड करें.

## “export dgn to dwg” क्या है?
DGN को DWG में निर्यात करना मतलब MicroStation DGN डिज़ाइन को AutoCAD DWG ड्रॉइंग के भीतर एक अंडरले के रूप में परिवर्तित या एम्बेड करना है। यह CAD पेशेवरों को मौजूदा DGN एसेट्स का उपयोग करने देता है बिना जियोमेट्री को शून्य से पुनः बनाने के।

## MicroStation DGN को AutoCAD DWG में क्यों परिवर्तित करें?
- **सहयोग:** AutoCAD उपयोग करने वाली टीमें DGN सामग्री को सीधे देख और संपादित कर सकती हैं.
- **मानकीकरण:** DWG कई डाउनस्ट्रीम वर्कफ़्लोज़ (जैसे PDF जनरेशन, 3D रेंडरिंग) के लिए डि‑फैक्टो फ़ॉर्मेट है.
- **संरक्षण:** मूल DGN रेफ़रेंसेज़ को अपरिवर्तित रखता है, जिससे डेटा हानि कम होती है.

## पूर्वापेक्षाएँ

ट्यूटोरियल में प्रवेश करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:
1. **Aspose.CAD Library:** Java के लिए Aspose.CAD लाइब्रेरी डाउनलोड और इंस्टॉल करें। आप लाइब्रेरी [here](https://releases.aspose.com/cad/java/) पर पा सकते हैं.
2. **Java Development Kit (JDK):** सुनिश्चित करें कि आपके सिस्टम पर Java स्थापित है.
3. **Integrated Development Environment (IDE):** सुगम विकास अनुभव के लिए Eclipse या IntelliJ जैसे Java IDE चुनें.

## पैकेज इम्पोर्ट करें

अपने Java प्रोजेक्ट में, CAD फ़ाइल हेरफेर को सक्षम करने के लिए आवश्यक Aspose.CAD पैकेज इम्पोर्ट करें। यहाँ एक उदाहरण है:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## चरण 1: फ़ाइल पाथ सेट करें

DWG फ़ाइल के लिए इनपुट और आउटपुट फ़ाइल पाथ परिभाषित करें। `dataDir`, `fileName`, और `outPath` वेरिएबल्स को तदनुसार अपडेट करें.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## चरण 2: PdfOptions इंस्टेंस बनाएं

`PdfOptions` क्लास का एक इंस्टेंस बनाएं, क्योंकि हम त्वरित सत्यापन के लिए **CAD फ़ाइल को PDF में निर्यात** कर रहे हैं.

```java
PdfOptions exportOptions = new PdfOptions();
```

## चरण 3: DWG फ़ाइल लोड करें

मौजूदा DWG फ़ाइल को इमेज के रूप में लोड करें और इसे `CadImage` टाइप में परिवर्तित करें.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## चरण 4: एंटिटीज़ के माध्यम से इटररेट करें

DWG फ़ाइल के भीतर प्रत्येक एंटिटी को देखें और जांचें कि क्या वह इमेज डिफ़िनिशन है। यदि हाँ, तो ऑब्जेक्ट के बाहरी रेफ़रेंस को प्राप्त करें.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## चरण 5: रास्टराइज़ेशन विकल्प परिभाषित करें

`CadRasterizationOptions` ऑब्जेक्ट के लिए सेटिंग्स परिभाषित करें, जिसमें पेज की चौड़ाई, ऊँचाई, लेआउट्स, और बैकग्राउंड रंग शामिल हैं.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## चरण 6: वेक्टर रास्टराइज़ेशन विकल्प सेट करें

निर्यात के लिए वेक्टर रास्टराइज़ेशन विकल्प सेट करें.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## चरण 7: DWG को PDF में निर्यात करें

अंत में, `save` मेथड को कॉल करके DWG को PDF में निर्यात करें.

```java
cadImage.save(outPath, exportOptions);
```

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|-------|----------|
| **कोई DGN अंडरले नहीं दिख रहा है** | DWG में `DGNUNDERLAY` एंटिटी नहीं है. | सुनिश्चित करें कि स्रोत DWG में DGN रेफ़रेंस शामिल है. |
| **PDF खाली है** | रास्टराइज़ेशन विकल्प शून्य आकार या गलत लेआउट पर सेट हैं. | सुनिश्चित करें कि `setPageWidth`/`setPageHeight` सकारात्मक हैं और `setLayouts` DWG लेआउट नाम से मेल खाता है. |
| **लाइसेंस अपवाद** | वैध Aspose.CAD लाइसेंस के बिना चलाना. | किसी भी API मेथड को कॉल करने से पहले टेम्पररी या खरीदा हुआ लाइसेंस लागू करें. |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: Aspose.CAD for Java की डॉक्यूमेंटेशन कहाँ मिल सकती है?
A1: डॉक्यूमेंटेशन [here](https://reference.aspose.com/cad/java/) पर मिल सकती है.

### Q2: मैं Aspose.CAD लाइब्रेरी for Java को कैसे डाउनलोड कर सकता हूँ?
A2: आप लाइब्रेरी [this link](https://releases.aspose.com/cad/java/) से डाउनलोड कर सकते हैं.

### Q3: क्या Aspose.CAD for Java के लिए मुफ्त ट्रायल उपलब्ध है?
A3: हाँ, आप मुफ्त ट्रायल [here](https://releases.aspose.com/) पर पा सकते हैं.

### Q4: Aspose.CAD for Java के लिए टेम्पररी लाइसेंस कहाँ प्राप्त कर सकता हूँ?
A4: टेम्पररी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से प्राप्त करें.

### Q5: मदद चाहिए या कोई प्रश्न हैं?
A5: Aspose.CAD कम्युनिटी सपोर्ट फ़ोरम [here](https://forum.aspose.com/c/cad/19) पर जाएँ.

### Q6: क्या मैं उत्पन्न PDF को फिर से DWG में बदल सकता हूँ?
A6: PDF एक रास्टर प्रीव्यू है; DWG में वापस परिवर्तन के लिए एक अलग रिवर्स‑इंजीनियरिंग टूल की आवश्यकता होती है.

### Q7: क्या यह तरीका अन्य CAD फ़ॉर्मेट जैसे DWF या DXF के साथ काम करता है?
A7: हाँ, Aspose.CAD कई फ़ॉर्मेट्स को सपोर्ट करता है; आपको केवल फ़ाइल एक्सटेंशन और रास्टराइज़ेशन सेटिंग्स को अनुसार बदलना होगा.

**अंतिम अपडेट:** 2026-01-10  
**परीक्षण किया गया:** Aspose.CAD for Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}