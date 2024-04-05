---
title: जावा का उपयोग करके विशेष DWG को छवि में बदलें
linktitle: जावा का उपयोग करके विशेष DWG को छवि में बदलें
second_title: Aspose.CAD जावा एपीआई
description: Java के लिए Aspose.CAD के साथ छवियों में DWG के निर्बाध रूपांतरण का अन्वेषण करें। कुशल फ़ाइल स्वरूप परिवर्तनों के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 14
url: /hi/java/dwg-file-operations/convert-dwg-to-image/
---
## परिचय

डिजिटल डिज़ाइन के लगातार विकसित हो रहे परिदृश्य में, DWG चित्रों को छवियों में बदलने की आवश्यकता एक सामान्य आवश्यकता है। जावा के लिए Aspose.CAD इस कार्य को निर्बाध रूप से प्राप्त करने के लिए एक शक्तिशाली उपकरण के रूप में उभरा है। इस ट्यूटोरियल में, हम जावा के लिए Aspose.CAD का उपयोग करके एक विशेष DWG फ़ाइल को एक छवि में परिवर्तित करने की प्रक्रिया में आपका मार्गदर्शन करेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
1.  जावा डेवलपमेंट किट (जेडीके): जावा के लिए Aspose.CAD को आपके सिस्टम पर एक संगत जेडीके स्थापित करने की आवश्यकता है। आप नवीनतम JDK यहां से डाउनलोड कर सकते हैं[ओरेकल की वेबसाइट](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  जावा लाइब्रेरी के लिए Aspose.CAD: जावा लाइब्रेरी के लिए Aspose.CAD को यहां से डाउनलोड और इंस्टॉल करें[Aspose.CAD डाउनलोड पृष्ठ](https://releases.aspose.com/cad/java/).
3. एकीकृत विकास पर्यावरण (आईडीई): जावा विकास के लिए अपनी पसंद का एक आईडीई चुनें, जैसे इंटेलीजे आईडीईए या एक्लिप्स।

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, सुचारू एकीकरण के लिए आवश्यक Aspose.CAD पैकेज आयात करें। अपने कोड में निम्नलिखित शामिल करें:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.ArrayList;
import java.util.Collection;
import java.util.Iterator;
import java.util.List;
import java.util.ListIterator;
```

## चरण 1: अपना प्रोजेक्ट सेट करें

सुनिश्चित करें कि आपका जावा प्रोजेक्ट आवश्यक Aspose.CAD लाइब्रेरी के साथ सेट है, और JDK आपके IDE में ठीक से कॉन्फ़िगर किया गया है।

## चरण 2: DWG फ़ाइल पथ निर्दिष्ट करें

उस DWG फ़ाइल का पथ परिभाषित करें जिसे आप कनवर्ट करना चाहते हैं। अद्यतन करें`dataDir` और`sourceFilePath` तदनुसार परिवर्तनशील.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String sourceFilePath = dataDir + "visualization_-_conference_room.dwg";
```

## चरण 3: टेक्स्ट इकाइयों को फ़िल्टर करें

DWG इकाइयों के माध्यम से पुनरावृति करें और Aspose.CAD लाइब्रेरी का उपयोग करके पाठ इकाइयों को फ़िल्टर करें।

```java
CadImage cadImage = (CadImage) (Image.load(sourceFilePath));
CadBaseEntity[] entities = cadImage.getEntities();
List<CadBaseEntity> filteredEntities = new ArrayList<>();
for (CadBaseEntity baseEntity : entities) {
    if ((baseEntity.getTypeName() == CadEntityTypeName.TEXT)) {
        filteredEntities.add(baseEntity);
    }
}
CadBaseEntity[] arr = new CadBaseEntity[filteredEntities.size()];
cadImage.setEntities(filteredEntities.toArray(arr));
```

## चरण 4: रैस्टराइज़ेशन विकल्प सेट करें

 का एक उदाहरण बनाएं`CadRasterizationOptions` और पीडीएफ रूपांतरण के लिए इसके गुणों को कॉन्फ़िगर करें।

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## चरण 5: पीडीएफ में निर्यात करें

 एक बनाने के`PdfOptions` उदाहरण के लिए, वेक्टर रैस्टराइज़ेशन विकल्प सेट करें, और परिवर्तित पीडीएफ फ़ाइल को सहेजें।

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
String outFile = dataDir + "result_out_generated.pdf";
cadImage.save(outFile, pdfOptions);
```

बधाई हो! आपने जावा के लिए Aspose.CAD का उपयोग करके एक विशिष्ट DWG फ़ाइल को सफलतापूर्वक एक छवि में परिवर्तित कर दिया है।

## निष्कर्ष

जावा के लिए Aspose.CAD आपके डिज़ाइन वर्कफ़्लो में लचीलापन और दक्षता प्रदान करते हुए, छवि रूपांतरण के लिए DWG की प्रक्रिया को सरल बनाता है। उत्पादकता बढ़ाने और फ़ाइल प्रारूप परिवर्तनों को सुव्यवस्थित करने के लिए इस टूल को अपनी परियोजनाओं में शामिल करें।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD DWG फ़ाइलों के सभी संस्करणों के साथ संगत है?

A1: Aspose.CAD विभिन्न फ़ाइल स्वरूपों के साथ संगतता सुनिश्चित करते हुए, DWG संस्करणों की एक विस्तृत श्रृंखला का समर्थन करता है।

### Q2: क्या मैं आउटपुट छवि के रिज़ॉल्यूशन को अनुकूलित कर सकता हूँ?

उ2: हां, ट्यूटोरियल दर्शाता है कि पेज की चौड़ाई और ऊंचाई कैसे सेट करें, जिससे आप रिज़ॉल्यूशन को नियंत्रित कर सकते हैं।

### Q3: क्या Aspose.CAD बैच रूपांतरण के लिए उपयुक्त है?

A3: बिल्कुल. Aspose.CAD बैच प्रोसेसिंग की अनुमति देता है, जिससे आप एक साथ कई DWG फ़ाइलों को परिवर्तित कर सकते हैं।

### Q4: मुझे अतिरिक्त सहायता या सामुदायिक चर्चाएँ कहाँ मिल सकती हैं?

 A4: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) समर्थन और चर्चा के लिए.

### Q5: क्या मैं खरीदने से पहले Aspose.CAD आज़मा सकता हूँ?

 A5: हां, यहां उपलब्ध निःशुल्क परीक्षण के साथ टूल का अन्वेषण करें[इस लिंक](https://releases.aspose.com/).