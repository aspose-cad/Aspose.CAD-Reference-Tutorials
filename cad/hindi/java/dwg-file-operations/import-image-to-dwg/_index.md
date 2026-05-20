---
date: 2026-05-20
description: Aspose.CAD for Java का उपयोग करके DWG फ़ाइलों में इमेज कैसे जोड़ें और
  साथ ही DWG को PDF में कैसे कनवर्ट करें, सीखें। कुशल विकास के लिए हमारी चरण-दर-चरण
  गाइड का पालन करें।
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Java का उपयोग करके DWG फ़ाइल में इमेज इम्पोर्ट करें
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD Java का उपयोग करके DWG फ़ाइलों में आसानी से इमेज जोड़ें
url: /hi/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD Java का उपयोग करके DWG फ़ाइलों में आसानी से छवि जोड़ें

आधुनिक Java अनुप्रयोगों में, **adding an image to DWG** फ़ाइलें एक सामान्य आवश्यकता है—चाहे आप CAD व्यूअर बना रहे हों, ड्राइंग अपडेट को स्वचालित कर रहे हों, या दस्तावेज़ीकरण उत्पन्न कर रहे हों। Aspose.CAD for Java आपको एक सरल, उच्च‑प्रदर्शन तरीका प्रदान करता है जिससे आप रास्टर छवियों को सीधे DWG ड्रॉइंग में एम्बेड कर सकते हैं बिना किसी पूर्ण‑स्तरीय CAD इंजन की आवश्यकता के। इस ट्यूटोरियल में हम आपको पूरी प्रक्रिया के माध्यम से ले जाएंगे, DWG लोड करने से लेकर परिणाम को PDF के रूप में निर्यात करने तक, और हम यह भी कवर करेंगे कि कैसे **import image into dwg** और **convert dwg to pdf** एक ही कार्यप्रवाह में किया जा सकता है।

## त्वरित उत्तर
- **मुझे कौनसी लाइब्रेरी चाहिए?** Aspose.CAD for Java  
- **क्या मैं PDF में भी निर्यात कर सकता हूँ?** Yes – use `PdfOptions` with `CadRasterizationOptions`  
- **क्या विकास के लिए लाइसेंस चाहिए?** A free trial works for testing; a commercial license is required for production  
- **कौनसा Java संस्करण समर्थित है?** Java 8 and higher  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** About 10‑15 minutes for a basic image import  

## “add image to dwg” क्या है?
DWG फ़ाइल में छवि जोड़ना का मतलब है रास्टर चित्र (PNG, JPEG, आदि) को **CadRasterImage** इकाई के रूप में ड्राइंग के मॉडल स्पेस में एम्बेड करना, जहाँ इसे किसी भी अन्य CAD ऑब्जेक्ट की तरह स्थित, स्केल और वैकल्पिक रूप से क्लिप किया जा सकता है। यह ड्रॉइंग की ऑब्जेक्ट टेबल में संग्रहीत होता है और मानक CAD व्यूअर्स द्वारा प्रदर्शित किया जाता है।

## DWG में छवि जोड़ने के लिए Aspose.CAD for Java का उपयोग क्यों करें?
आप बिना किसी थर्ड‑पार्टी CAD सॉफ़्टवेयर को स्थापित किए DWG फ़ाइलों में रास्टर ग्राफ़िक्स एम्बेड कर सकते हैं, और API आपको इन्सर्शन पॉइंट, स्केलिंग वेक्टर और क्लिपिंग बाउंड्रीज़ पर पिक्सेल‑परफेक्ट नियंत्रण देती है। Aspose.CAD 2 GB तक के फ़ाइलों को प्रोसेस करता है, **50+ input and output formats** का समर्थन करता है, और Windows, Linux, तथा macOS पर चलता है, जिससे आप किसी भी Java‑आधारित बैकएंड में CAD मैनिपुलेशन को एकीकृत कर सकते हैं।

## पूर्वापेक्षाएँ
- **Aspose.CAD for Java** – आधिकारिक साइट से नवीनतम JAR डाउनलोड करें **[here](https://releases.aspose.com/cad/java/)**।  
- **Java Development Kit** – JDK 8 या नया, आपके पसंदीदा IDE (IntelliJ IDEA, Eclipse, VS Code, आदि) के साथ।  
- उत्पादन उपयोग के लिए एक वैध **Aspose.CAD license** (ट्रायल प्रयोग के लिए काम करता है)।  

## पैकेज आयात करें
निम्नलिखित इम्पोर्ट्स आवश्यक Aspose.CAD क्लासेज़ को लाते हैं जो छवि हेरफेर और PDF रूपांतरण के लिए उपयोग होते हैं।  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## स्टेप‑बाय‑स्टेप गाइड

### चरण 1: DWG फ़ाइल लोड करें
सबसे पहले, उस फ़ोल्डर की ओर संकेत करें जिसमें आपका DWG ड्रॉइंग है और इसे `Image.load` के साथ लोड करें।  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### चरण 2: रास्टर इमेज डिफिनिशन निर्धारित करें
`CadRasterImageDef` क्लास वह बाहरी रास्टर इमेज रिसोर्स निर्धारित करती है जिसे ड्रॉइंग में एम्बेड किया जाएगा।  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### चरण 3: इन्सर्शन पॉइंट और स्केलिंग वेक्टर सेट करें
इन्सर्शन पॉइंट निर्धारित करता है कि छवि का निचला‑बायाँ कोना कहाँ दिखाई देगा। **U** और **V** वेक्टर क्षैतिज और ऊर्ध्वाधर स्केलिंग को नियंत्रित करते हैं।  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### चरण 4: CadRasterImage ऑब्जेक्ट बनाएं
`CadRasterImage` इकाई DWG मॉडल स्पेस में रखी गई रास्टर छवि को दर्शाती है।  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### चरण 5: इमेज को मॉडल स्पेस में जोड़ें
रास्टर इमेज को `*Model_Space` ब्लॉक में डालें, फिर ड्रॉइंग की ऑब्जेक्ट कलेक्शन को अपडेट करें ताकि डिफिनिशन सहेजा जा सके।  
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

### चरण 6: PDF निर्यात विकल्प कॉन्फ़िगर करें (वैकल्पिक)
`PdfOptions` CAD ड्रॉइंग को PDF फ़ाइल के रूप में सहेजने के लिए सेटिंग्स निर्दिष्ट करता है। `CadRasterizationOptions` PDF रूपांतरण के दौरान CAD कंटेंट को कैसे रास्टर किया जाता है, यह परिभाषित करता है।  
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### चरण 7: परिणामी PDF सहेजें
अंत में, संशोधित ड्रॉइंग को PDF फ़ाइल के रूप में निर्यात करें। वही `image` इंस्टेंस उपयोग किया गया है, इसलिए PDF में नई जोड़ी गई रास्टर इमेज दिखेगी।  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

इन चरणों का पालन करके, आप **add image to dwg** फ़ाइलों को जल्दी से जोड़ सकते हैं और आवश्यकता पड़ने पर **save dwg as pdf** भी कर सकते हैं, जिससे एक ही संक्षिप्त रूटीन में सबसे सामान्य **dwg file operations** को कवर किया जाता है।

## सामान्य समस्याएँ और समाधान
- **Image not appearing** – जांचें कि इमेज फ़ाइल पाथ (`road-sign-custom.png`) सही है और इमेज के आयाम `CadRasterImageDef` को पास किए गए मानों से मेल खाते हैं।  
- **Incorrect scaling** – U और V वेक्टर को समायोजित करें; वे ड्रॉइंग यूनिट्स प्रति पिक्सेल को दर्शाते हैं।  
- **PDF looks blank** – सुनिश्चित करें कि `CadRasterizationOptions.setDrawType` को `UseObjectColor` या किसी अन्य उपयुक्त मोड पर सेट किया गया है।  

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या Aspose.CAD for Java सभी Java विकास परिवेशों के साथ संगत है?**  
A: हाँ, Aspose.CAD for Java किसी भी IDE के साथ काम करता है जो JDK 8+ को सपोर्ट करता है, जिसमें IntelliJ IDEA, Eclipse, और VS Code शामिल हैं।

**Q: क्या मैं Aspose.CAD for Java को व्यावसायिक प्रोजेक्ट्स के लिए उपयोग कर सकता हूँ?**  
A: हाँ, आप Aspose.CAD for Java को व्यावसायिक प्रोजेक्ट्स के लिए उपयोग कर सकते हैं। लाइसेंसिंग विवरण के लिए **[here](https://purchase.aspose.com/buy)** देखें।

**Q: क्या Aspose.CAD for Java के लिए कोई मुफ्त ट्रायल उपलब्ध है?**  
A: हाँ, आप मुफ्त ट्रायल **[here](https://releases.aspose.com/)** पर एक्सेस कर सकते हैं।

**Q: मैं Aspose.CAD for Java के लिए समर्थन कैसे प्राप्त कर सकता हूँ?**  
A: आप **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** पर समर्थन प्राप्त कर सकते हैं।

**Q: क्या मैं Aspose.CAD for Java के लिए एक अस्थायी लाइसेंस प्राप्त कर सकता हूँ?**  
A: हाँ, आप अस्थायी लाइसेंस **[here](https://purchase.aspose.com/temporary-license/)** पर प्राप्त कर सकते हैं।

**अंतिम अपडेट:** 2026-05-20  
**परीक्षण किया गया:** Aspose.CAD for Java 24.11  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [Aspose.CAD for Java का उपयोग करके DWG को PDF या रास्टर में निर्यात करें](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java का उपयोग करके DWG फ़ाइलों में कस्टम प्रॉपर्टीज़ जोड़ें](/cad/java/additional-features/add-custom-properties/)
- [CAD को PNG के रूप में सहेजें – Aspose.CAD for Java का उपयोग करके CAD ड्रॉइंग को रास्टर इमेज फ़ॉर्मेट में बदलें](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}