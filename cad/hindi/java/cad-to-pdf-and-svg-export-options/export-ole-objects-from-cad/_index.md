---
title: जावा के लिए Aspose.CAD का उपयोग करके CAD से OLE ऑब्जेक्ट निर्यात करें
linktitle: CAD से OLE ऑब्जेक्ट निर्यात करें
second_title: Aspose.CAD जावा एपीआई
description: जावा के लिए Aspose.CAD की क्षमता को अनलॉक करें। CAD फ़ाइलों से OLE ऑब्जेक्ट को आसानी से निर्यात करें। निर्बाध सीएडी डेटा प्रबंधन के लिए अभी डाउनलोड करें।
weight: 10
url: /hi/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के लिए Aspose.CAD का उपयोग करके CAD से OLE ऑब्जेक्ट निर्यात करें

## परिचय

कंप्यूटर-एडेड डिज़ाइन (CAD) की गतिशील दुनिया में, OLE (ऑब्जेक्ट लिंकिंग और एंबेडिंग) ऑब्जेक्ट को कुशलतापूर्वक प्रबंधित करना और निकालना महत्वपूर्ण है। जावा के लिए Aspose.CAD, CAD फ़ाइलों से OLE ऑब्जेक्ट निर्यात करने के लिए एक शक्तिशाली समाधान प्रदान करता है। यह चरण-दर-चरण मार्गदर्शिका आपको प्रक्रिया के बारे में बताएगी, यह सुनिश्चित करते हुए कि आप इस उपकरण की पूरी क्षमता का उपयोग करें।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- जावा पर्यावरण: सुनिश्चित करें कि आपकी मशीन पर जावा विकास वातावरण स्थापित है।
-  जावा के लिए Aspose.CAD: जावा लाइब्रेरी के लिए Aspose.CAD को डाउनलोड और इंस्टॉल करें। आप लाइब्रेरी यहां पा सकते हैं[लिंक को डाउनलोड करें](https://releases.aspose.com/cad/java/).
- CAD फ़ाइलें: OLE ऑब्जेक्ट वाली CAD फ़ाइलें तैयार करें जिन्हें आप निर्यात करना चाहते हैं।

## नामस्थान आयात करें

आरंभ करने के लिए, अपने जावा प्रोजेक्ट में आवश्यक नामस्थान आयात करें। ये नामस्थान Aspose.CAD का उपयोग करके CAD फ़ाइलों के साथ काम करने के लिए आवश्यक आवश्यक कक्षाएं और कार्यक्षमताएं प्रदान करते हैं।

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

अब, आइए CAD से OLE ऑब्जेक्ट निर्यात करने की प्रक्रिया को कई चरणों में विभाजित करें:

## चरण 1: अपनी दस्तावेज़ निर्देशिका सेट करें

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

"आपकी दस्तावेज़ निर्देशिका" को अपनी CAD फ़ाइलों वाली निर्देशिका के पथ से बदलना सुनिश्चित करें।

## चरण 2: सीएडी फ़ाइल नाम परिभाषित करें

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

 उन CAD फ़ाइलों के नाम निर्दिष्ट करें जिन्हें आप संसाधित करना चाहते हैं`files` सरणी.

## चरण 3: पीएनजी निर्यात विकल्प सेट करें

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

वेक्टर रैस्टराइज़ेशन और लेआउट सेटिंग्स सहित पीएनजी निर्यात विकल्पों को कॉन्फ़िगर करें।

## चरण 4: CAD फ़ाइलों के माध्यम से पुनरावृति करें

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

प्रत्येक निर्दिष्ट CAD फ़ाइल के माध्यम से पुनरावृत्ति करें, इसे Aspose.CAD का उपयोग करके लोड करें, और OLE ऑब्जेक्ट को PNG छवियों के रूप में सहेजें।

## निष्कर्ष

इन सरल लेकिन शक्तिशाली चरणों के साथ, आप जावा के लिए Aspose.CAD का उपयोग करके CAD फ़ाइलों से OLE ऑब्जेक्ट को निर्बाध रूप से निर्यात कर सकते हैं। यह बहुमुखी उपकरण डेवलपर्स को CAD डेटा को कुशलतापूर्वक प्रबंधित करने में सक्षम बनाता है, जिससे CAD एप्लिकेशन विकास में नई संभावनाएं खुलती हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.CAD सभी CAD फ़ाइल स्वरूपों के साथ संगत है?

 A1: Aspose.CAD DWG, DXF और DGN सहित विभिन्न CAD प्रारूपों का समर्थन करता है। को देखें[प्रलेखन](https://reference.aspose.com/cad/java/) पूरी सूची के लिए.

### Q2: क्या मैं OLE ऑब्जेक्ट के लिए निर्यात सेटिंग्स को अनुकूलित कर सकता हूँ?

A2: हां, Aspose.CAD निर्यात सेटिंग्स को अनुकूलित करने के लिए व्यापक विकल्प प्रदान करता है, जिससे आप आउटपुट को अपनी विशिष्ट आवश्यकताओं के अनुरूप बना सकते हैं।

### Q3: क्या Aspose.CAD के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

 उ3: हां, आप नि:शुल्क परीक्षण प्राप्त करके Aspose.CAD की क्षमताओं का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मुझे Aspose.CAD के लिए सामुदायिक समर्थन कहाँ से मिल सकता है?

 A4: Aspose.CAD समुदाय में शामिल हों[मंच](https://forum.aspose.com/c/cad/19) सहायता लेने और अपने अनुभव साझा करने के लिए।

### Q5: मैं Aspose.CAD के लिए लाइसेंस कैसे खरीद सकता हूं?

A5: पर जाएँ[खरीद पृष्ठ](https://purchase.aspose.com/buy) ऐसा लाइसेंस प्राप्त करना जो आपकी विकास आवश्यकताओं के अनुरूप हो।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
