---
title: जावा के लिए Aspose.CAD के साथ यूनिट प्रकार का उपयोग करके CAD ड्राइंग आकार को समायोजित करना
linktitle: यूनिट प्रकार का उपयोग करके सीएडी ड्राइंग आकार को समायोजित करना
second_title: Aspose.CAD जावा एपीआई
description: आसानी से CAD ड्राइंग आकार समायोजित करने में Java के लिए Aspose.CAD की शक्ति का अन्वेषण करें। सटीकता और अनुकूलनशीलता के लिए हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 14
url: /hi/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---
## परिचय

कंप्यूटर-एडेड डिज़ाइन (सीएडी) के निरंतर विकसित हो रहे क्षेत्र में, सटीकता और अनुकूलनशीलता सर्वोपरि है। एक सामान्य आवश्यकता विशिष्ट इकाई प्रकारों के आधार पर सीएडी चित्रों के आकार को समायोजित करना है। जावा के लिए Aspose.CAD एक शक्तिशाली सहयोगी के रूप में उभरता है, जो CAD फ़ाइलों को प्रोग्रामेटिक रूप से हेरफेर करने के लिए निर्बाध क्षमताएं प्रदान करता है।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- जावा विकास पर्यावरण: सुनिश्चित करें कि आपकी मशीन पर एक कार्यात्मक जावा विकास वातावरण स्थापित है।

-  जावा लाइब्रेरी के लिए Aspose.CAD: Aspose.CAD लाइब्रेरी को अपने जावा प्रोजेक्ट में डाउनलोड और एकीकृत करें। आप लाइब्रेरी प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/cad/java/).

## नामस्थान आयात करें

अपने जावा कोड में, Aspose.CAD कार्यात्मकताओं तक पहुँचने के लिए आवश्यक नामस्थान शामिल करें। निम्नलिखित आयात जोड़ें:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

अब, आइए यूनिट प्रकार का उपयोग करके सीएडी ड्राइंग आकार को समायोजित करने की प्रक्रिया को प्रबंधनीय चरणों में विभाजित करें:

## चरण 1: डेटा निर्देशिका को परिभाषित करें

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

उस निर्देशिका के लिए पथ सेट करें जहां आपकी CAD फ़ाइलें स्थित हैं।

## चरण 2: सीएडी ड्राइंग लोड करें

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Aspose.CAD का उपयोग करके CAD ड्राइंग लोड करें`Image` कक्षा।

## चरण 3: बीएमपी विकल्प बनाएं

```java
BmpOptions bmpOptions = new BmpOptions();
```

 त्वरित करें`BmpOptions` सीएडी लेआउट को बीएमपी प्रारूप में निर्यात करने के लिए क्लास।

## चरण 4: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 का एक उदाहरण बनाएं`CadRasterizationOptions` और इसे इसके साथ संबद्ध करें`BmpOptions` वेक्टर रेखापुंज के लिए.

## चरण 5: इकाई प्रकार सेट करें

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

सीएडी ड्राइंग के लिए वांछित इकाई प्रकार निर्दिष्ट करें। इस उदाहरण में, हमने इसे सेंटीमीटर पर सेट किया है।

## चरण 6: लेआउट सेट करें

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

निर्यात के दौरान विचार किए जाने वाले लेआउट को परिभाषित करें। इस मामले में, हमने "मॉडल" लेआउट का चयन किया है।

## चरण 7: बीएमपी को निर्यात करें

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

अंत में, संशोधित CAD ड्राइंग को BMP प्रारूप में सहेजें।

## निष्कर्ष

जावा के लिए Aspose.CAD के साथ, CAD ड्राइंग आकार समायोजित करना आसान हो जाता है। इस ट्यूटोरियल ने आपको सटीक परिणाम प्राप्त करने में प्रत्येक चरण के महत्व पर जोर देते हुए प्रक्रिया से परिचित कराया है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य प्रोग्रामिंग भाषाओं के साथ जावा के लिए Aspose.CAD का उपयोग कर सकता हूँ?

A1: Aspose.CAD मुख्य रूप से Java का समर्थन करता है, लेकिन .NET जैसी अन्य भाषाओं के लिए भी संस्करण उपलब्ध हैं।

### Q2: क्या Aspose.CAD के लिए कोई लाइसेंसिंग विकल्प हैं?

 उ2: हां, आप लाइसेंसिंग विकल्प तलाश सकते हैं और Aspose.CAD खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### Q3: क्या Aspose.CAD के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

 उ3: निश्चित रूप से, आप निःशुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं जावा के लिए Aspose.CAD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A4: Aspose.CAD फोरम पर जाएँ[यहाँ](https://forum.aspose.com/c/cad/19) व्यापक समर्थन के लिए.

### Q5: क्या मैं Aspose.CAD के लिए अस्थायी लाइसेंस प्राप्त कर सकता हूँ?

 A5: हाँ, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).