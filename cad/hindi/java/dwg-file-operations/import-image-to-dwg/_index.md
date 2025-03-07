---
title: Aspose.CAD Java का उपयोग करके DWG फ़ाइलों में सहज छवि आयात
linktitle: जावा का उपयोग करके छवि को DWG फ़ाइल में आयात करें
second_title: Aspose.CAD जावा एपीआई
description: Java के लिए Aspose.CAD का उपयोग करके DWG फ़ाइलों में छवियों के निर्बाध एकीकरण का अन्वेषण करें। कुशल विकास के लिए हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 10
url: /hi/java/dwg-file-operations/import-image-to-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD Java का उपयोग करके DWG फ़ाइलों में सहज छवि आयात

## परिचय

जावा विकास की गतिशील दुनिया में, DWG फ़ाइलों में छवियों को शामिल करना कई अनुप्रयोगों का एक महत्वपूर्ण पहलू बन गया है। जावा के लिए Aspose.CAD उन डेवलपर्स के लिए एक मजबूत समाधान प्रदान करता है जो DWG फ़ाइलों में छवियों को आयात करने के लिए कुशल तरीकों की तलाश कर रहे हैं। इस ट्यूटोरियल में, हम जावा के लिए Aspose.CAD का उपयोग करके छवियों का निर्बाध एकीकरण सुनिश्चित करते हुए, चरण दर चरण प्रक्रिया में आपका मार्गदर्शन करेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:
- जावा के लिए Aspose.CAD: सुनिश्चित करें कि आपके पास Aspose.CAD लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cad/java/).
- जावा विकास पर्यावरण: सभी आवश्यक कॉन्फ़िगरेशन के साथ अपना जावा विकास वातावरण स्थापित करें।

## पैकेज आयात करें

आरंभ करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक Aspose.CAD पैकेज आयात करें:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## चरण 1: DWG फ़ाइल और छवि लोड करें

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

## चरण 2: कैडरैस्टरइमेज को परिभाषित करें

```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

## चरण 3: सम्मिलन बिंदु और वेक्टर सेट करें

```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## चरण 4: कैडरास्टरइमेज ऑब्जेक्ट बनाएं

```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

## चरण 5: छवि को DWG में जोड़ें

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

## चरण 6: पीडीएफ विकल्प सेट करें

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## चरण 7: पीडीएफ सहेजें

```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

इन चरणों का पालन करके, आप जावा के लिए Aspose.CAD का उपयोग करके आसानी से छवियों को DWG फ़ाइलों में आयात कर सकते हैं।

## निष्कर्ष

अंत में, जावा के लिए Aspose.CAD जावा डेवलपर्स को DWG फ़ाइलों में छवियों को सहजता से एकीकृत करके अपने अनुप्रयोगों को बढ़ाने का अधिकार देता है। प्रदान की गई चरण-दर-चरण मार्गदर्शिका इस सुविधा का सुचारू और कुशल कार्यान्वयन सुनिश्चित करती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या जावा के लिए Aspose.CAD सभी जावा विकास परिवेशों के साथ संगत है?

A1: हाँ, Java के लिए Aspose.CAD अधिकांश जावा विकास परिवेशों के साथ संगत है।

### Q2: क्या मैं व्यावसायिक परियोजनाओं के लिए जावा के लिए Aspose.CAD का उपयोग कर सकता हूँ?

 उ2: हाँ, आप व्यावसायिक परियोजनाओं के लिए जावा के लिए Aspose.CAD का उपयोग कर सकते हैं। मिलने जाना[यहाँ](https://purchase.aspose.com/buy) लाइसेंसिंग विवरण के लिए.

### Q3: क्या Java के लिए Aspose.CAD का निःशुल्क परीक्षण उपलब्ध है?

 उ3: हाँ, आप नि:शुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं जावा के लिए Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A4: आप पर समर्थन मांग सकते हैं[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19).

### Q5: क्या मैं जावा के लिए Aspose.CAD के लिए अस्थायी लाइसेंस प्राप्त कर सकता हूँ?

 A5: हाँ, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
