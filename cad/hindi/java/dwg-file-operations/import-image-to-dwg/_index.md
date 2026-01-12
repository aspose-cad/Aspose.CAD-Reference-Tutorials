---
date: 2026-01-12
description: Aspose.CAD for Java का उपयोग करके DWG फ़ाइलों में इमेज जोड़ना और DWG
  को PDF में बदलना सीखें। कुशल विकास के लिए हमारे चरण-दर-चरण गाइड का पालन करें।
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: Aspose.CAD Java का उपयोग करके DWG फ़ाइलों में सहजता से छवि जोड़ें
url: /hi/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD Java का उपयोग करके DWG फ़ाइलों में आसानी से इमेज जोड़ें

आधुनिक Java अनुप्रयोगों में, **DWG में इमेज जोड़ना** एक सामान्य आवश्यकता है—चाहे आप CAD व्यूअर बना रहे हों, ड्रॉइंग अपडेट को स्वचालित कर रहे हों, या दस्तावेज़ जनरेट कर रहे हों। Aspose.CAD for Java आपको एक सरल, उच्च‑प्रदर्शन तरीका प्रदान करता है जिससे आप रास्टर इमेज को सीधे DWG ड्रॉइंग में एम्बेड कर सकते हैं, बिना किसी पूर्ण CAD इंजन की आवश्यकता के। इस ट्यूटोरियल में हम आपको पूरी प्रक्रिया दिखाएंगे, DWG लोड करने से लेकर परिणाम को PDF के रूप में एक्सपोर्ट करने तक।

## त्वरित उत्तर
- **मुझे कौन सी लाइब्रेरी चाहिए?** Aspose.CAD for Java  
- **क्या मैं PDF में भी एक्सपोर्ट कर सकता हूँ?** हाँ – `PdfOptions` को `CadRasterizationOptions` के साथ उपयोग करें  
- **क्या विकास के लिए लाइसेंस चाहिए?** एक फ्री ट्रायल परीक्षण के लिए काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण समर्थित है?** Java 8 और उससे ऊपर  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बेसिक इमेज इम्पोर्ट के लिए लगभग 10‑15 मिनट  

## DWG में इमेज जोड़ना क्या है?
DWG फ़ाइल में इमेज जोड़ना का मतलब है कि रास्टर चित्र (PNG, JPEG, आदि) को `CadRasterImage` ऑब्जेक्ट के रूप में ड्रॉइंग के मॉडल स्पेस में सम्मिलित करना। इमेज CAD एंटिटी ट्री का हिस्सा बन जाता है और इसे किसी भी अन्य CAD ऑब्जेक्ट की तरह स्थित, स्केल और क्लिप किया जा सकता है।

## DWG में इमेज जोड़ने के लिए Aspose.CAD for Java का उपयोग क्यों करें?
- **CAD सॉफ़्टवेयर की आवश्यकता नहीं** – API आंतरिक रूप से DWG पार्सिंग संभालता है।  
- **इन्सर्शन पॉइंट, स्केलिंग वेक्टर, और क्लिपिंग पर सूक्ष्म नियंत्रण**  
- **इन‑बिल्ट PDF कन्वर्ज़न** जिससे आप उसी वर्कफ़्लो में प्रिंटेबल PDF बना सकते हैं।  
- **क्रॉस‑प्लेटफ़ॉर्म** – Windows, Linux, और macOS पर काम करता है।  

## पूर्वापेक्षाएँ
- Aspose.CAD for Java: सुनिश्चित करें कि आपके पास Aspose.CAD लाइब्रेरी स्थापित है। आप इसे [यहाँ](https://releases.aspose.com/cad/java/) से डाउनलोड कर सकते हैं।  
- Java विकास पर्यावरण: JDK 8+ आपके पसंदीदा IDE (IntelliJ, Eclipse, VS Code, आदि) के साथ।  

## पैकेज इम्पोर्ट करें
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## स्टेप‑बाय‑स्टेप गाइड

### स्टेप 1: DWG फ़ाइल लोड करें
सबसे पहले, उस फ़ोल्डर की ओर संकेत करें जिसमें आपका DWG ड्रॉइंग है और इसे `Image.load` के साथ लोड करें।  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### स्टेप 2: रास्टर इमेज डिफ़िनिशन निर्धारित करें
`CadRasterImageDef` बनाएं जो उस बाहरी PNG को संदर्भित करता है जिसे आप एम्बेड करना चाहते हैं। कंस्ट्रक्टर इमेज फ़ाइल नाम और उसकी पिक्सेल डाइमेंशन लेता है।  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### स्टेप 3: इन्सर्शन पॉइंट और स्केलिंग वेक्टर सेट करें
इन्सर्शन पॉइंट निर्धारित करता है कि इमेज का निचला‑बायाँ कोना कहाँ दिखाई देगा। **U** और **V** वेक्टर क्षैतिज और लंबवत स्केलिंग को नियंत्रित करते हैं।  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### स्टेप 4: CadRasterImage ऑब्जेक्ट बनाएं
डिफ़िनिशन, इन्सर्शन पॉइंट, और वेक्टर को मिलाकर एक `CadRasterImage` बनाएं। यदि आप केवल चित्र का कुछ हिस्सा दिखाना चाहते हैं तो आप क्लिपिंग बाउंडरी भी सेट कर सकते हैं।  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### स्टेप 5: इमेज को मॉडल स्पेस में जोड़ें
रास्टर इमेज को `*Model_Space` ब्लॉक में डालें, फिर ड्रॉइंग की ऑब्जेक्ट कलेक्शन को अपडेट करें ताकि डिफ़िनिशन सेव हो जाए।  
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

### स्टेप 6: PDF एक्सपोर्ट विकल्प कॉन्फ़िगर करें (वैकल्पिक)
यदि आपको ड्रॉइंग का PDF संस्करण भी चाहिए, तो `PdfOptions` को `CadRasterizationOptions` के साथ कॉन्फ़िगर करें। यह स्टेप दिखाता है कि कैसे **dwg को pdf में बदलें** उसी फ्लो में।  
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### स्टेप 7: परिणामी PDF सहेजें
अंत में, संशोधित ड्रॉइंग को PDF फ़ाइल के रूप में एक्सपोर्ट करें। वही `image` इंस्टेंस उपयोग किया जाता है, इसलिए PDF में नया जोड़ा गया रास्टर इमेज दिखेगा।  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

इन स्टेप्स को फॉलो करके, आप जल्दी से **dwg में इमेज जोड़ सकते** हैं और आवश्यकता पड़ने पर **dwg को pdf के रूप में सहेज सकते** हैं।

## सामान्य समस्याएँ और समाधान
- **Image not appearing** – यह सुनिश्चित करें कि इमेज फ़ाइल पाथ (`road-sign-custom.png`) सही है और इमेज डाइमेंशन `CadRasterImageDef` को पास किए गए मानों से मेल खाते हैं।  
- **Incorrect scaling** – U और V वेक्टर को समायोजित करें; ये पिक्सेल प्रति ड्रॉइंग यूनिट को दर्शाते हैं।  
- **PDF looks blank** – सुनिश्चित करें कि `CadRasterizationOptions.setDrawType` को `UseObjectColor` या किसी अन्य उपयुक्त मोड पर सेट किया गया है।  

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या Aspose.CAD for Java सभी Java विकास पर्यावरणों के साथ संगत है?**  
A: हाँ, Aspose.CAD for Java अधिकांश Java विकास पर्यावरणों के साथ संगत है।

**Q: क्या मैं Aspose.CAD for Java को वाणिज्यिक प्रोजेक्ट्स के लिए उपयोग कर सकता हूँ?**  
A: हाँ, आप Aspose.CAD for Java को वाणिज्यिक प्रोजेक्ट्स के लिए उपयोग कर सकते हैं। लाइसेंसिंग विवरण के लिए [यहाँ](https://purchase.aspose.com/buy) देखें।

**Q: क्या Aspose.CAD for Java के लिए कोई फ्री ट्रायल उपलब्ध है?**  
A: हाँ, आप फ्री ट्रायल [यहाँ](https://releases.aspose.com/) से एक्सेस कर सकते हैं।

**Q: मैं Aspose.CAD for Java के लिए सपोर्ट कैसे प्राप्त कर सकता हूँ?**  
A: आप सपोर्ट के लिए [Aspose.CAD फ़ोरम](https://forum.aspose.com/c/cad/19) पर जा सकते हैं।

**Q: क्या मैं Aspose.CAD for Java के लिए अस्थायी लाइसेंस प्राप्त कर सकता हूँ?**  
A: हाँ, आप अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

---

**अंतिम अपडेट:** 2026-01-12  
**परीक्षण किया गया:** Aspose.CAD for Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}