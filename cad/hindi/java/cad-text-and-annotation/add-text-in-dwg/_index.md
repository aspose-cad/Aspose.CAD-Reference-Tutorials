---
title: Java के लिए Aspose.CAD का उपयोग करके DWG में टेक्स्ट जोड़ें
linktitle: DWG में टेक्स्ट जोड़ें
second_title: Aspose.CAD जावा एपीआई
description: Java के लिए Aspose.CAD के साथ अपने DWG चित्रों को सहजता से बढ़ाएं। हमारे चरण-दर-चरण मार्गदर्शिका के साथ सहजता से टेक्स्ट जोड़ें।
type: docs
weight: 10
url: /hi/java/cad-text-and-annotation/add-text-in-dwg/
---
## परिचय

कंप्यूटर-एडेड डिज़ाइन (सीएडी) के क्षेत्र में, जावा के लिए Aspose.CAD DWG चित्रों में हेरफेर करने और परिवर्तित करने के लिए एक शक्तिशाली उपकरण के रूप में सामने आता है। इसकी उपयोगी विशेषताओं में से एक DWG फ़ाइलों में पाठ को निर्बाध रूप से जोड़ने की क्षमता है। इस ट्यूटोरियल में, हम जावा के लिए Aspose.CAD का उपयोग करके आपके DWG चित्रों में टेक्स्ट जोड़ने की प्रक्रिया में आपका मार्गदर्शन करेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  जावा लाइब्रेरी के लिए Aspose.CAD: लाइब्रेरी को डाउनलोड और इंस्टॉल करें[जावा पेज के लिए Aspose.CAD](https://releases.aspose.com/cad/java/).

- जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर नवीनतम जेडीके स्थापित है।

- DWG ड्राइंग: एक DWG ड्राइंग फ़ाइल तैयार करें जहाँ आप टेक्स्ट जोड़ना चाहते हैं।

## नामस्थान आयात करें

अपने जावा कोड में, Aspose.CAD के लिए आवश्यक नामस्थान आयात करें:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

अब, आइए प्रदान किए गए कोड स्निपेट को कई चरणों में विभाजित करें:

## चरण 1: दस्तावेज़ निर्देशिका और DWG फ़ाइल पथ सेट करें

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## चरण 2: DWG छवि लोड करें

```java
Image image = Image.load(dwgPathToFile);
```

## चरण 3: कैडटेक्स्ट ऑब्जेक्ट बनाएं

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);
cadText.setScaleX(0);
```

## चरण 4: कैडइमेज में टेक्स्ट जोड़ें

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## चरण 5: पीडीएफ विकल्प सेट करें

```java
PdfOptions pdfOptions = new PdfOptions();
```

## चरण 6: कैडरास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## चरण 7: संशोधित DWG को पीडीएफ के रूप में सहेजें

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

इन चरणों का पालन करके, आप जावा के लिए Aspose.CAD का उपयोग करके अपने DWG चित्रों में निर्बाध रूप से टेक्स्ट जोड़ पाएंगे।

## निष्कर्ष

जावा के लिए Aspose.CAD डेवलपर्स को DWG चित्रों को प्रोग्रामेटिक रूप से बढ़ाने और संशोधित करने का अधिकार देता है। इस ट्यूटोरियल ने Aspose.CAD की सरलता और शक्ति को प्रदर्शित करते हुए, आपकी DWG फ़ाइलों में टेक्स्ट जोड़ने के लिए एक स्पष्ट चरण-दर-चरण मार्गदर्शिका प्रदान की है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD DWG फ़ाइलों के सभी संस्करणों के साथ संगत है?

A1: Aspose.CAD DWG फ़ाइलों के विभिन्न संस्करणों का समर्थन करता है, जिससे CAD सॉफ़्टवेयर की एक विस्तृत श्रृंखला के साथ संगतता सुनिश्चित होती है।

### Q2: क्या मैं जोड़े गए टेक्स्ट के फ़ॉन्ट और फ़ॉर्मेटिंग को अनुकूलित कर सकता हूँ?

A2: हाँ, आप Aspose.CAD का उपयोग करके DWG फ़ाइलों में जोड़े गए पाठ के लिए फ़ॉन्ट, शैली और अन्य स्वरूपण विकल्पों को अनुकूलित कर सकते हैं।

### Q3: क्या Java के लिए Aspose.CAD का निःशुल्क परीक्षण उपलब्ध है?

 उ3: हाँ, आप नि:शुल्क परीक्षण प्राप्त करके Aspose.CAD की विशेषताओं का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं जावा के लिए Aspose.CAD के लिए विस्तृत दस्तावेज़ कहां पा सकता हूं?

 A4: दस्तावेज़ देखें[यहाँ](https://reference.aspose.com/cad/java/) गहन जानकारी और उदाहरणों के लिए।

### Q5: मैं Aspose.CAD से कैसे सहायता प्राप्त कर सकता हूँ या मदद ले सकता हूँ?

A5: पर जाएँ[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सहायता प्राप्त करने और समुदाय से जुड़ने के लिए।