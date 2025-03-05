---
title: .NET के लिए Aspose.CAD में DGN को रैस्टर इमेज में निर्यात करें
linktitle: डीजीएन को रास्टर छवि में निर्यात करें
second_title: Aspose.CAD .NET - CAD और BIM फ़ाइल स्वरूप
description: .NET के लिए Aspose.CAD का उपयोग करके आसानी से DGN को रेखापुंज छवियों में परिवर्तित करें। चरण-दर-चरण मार्गदर्शिका का अन्वेषण करें और CAD फ़ाइल हेरफेर में .NET की शक्ति को उजागर करें।
type: docs
weight: 13
url: /hi/net/cad-export-formats/export-dgn-to-raster-image/
---
## परिचय

.NET विकास के गतिशील क्षेत्र में, Aspose.CAD कंप्यूटर-एडेड डिज़ाइन (CAD) फ़ाइलों को संभालने के लिए एक शक्तिशाली उपकरण के रूप में उभरता है। यह ट्यूटोरियल .NET के लिए Aspose.CAD का उपयोग करके छवियों को रेखापुंज करने के लिए DGN फ़ाइलों को निर्यात करने की प्रक्रिया पर प्रकाश डालता है। यदि आप अपनी डीजीएन फाइलों को सहजता से आकर्षक रेखापुंज छवियों में बदलने के इच्छुक हैं, तो आप सही जगह पर हैं।

## आवश्यक शर्तें

इससे पहले कि हम इस यात्रा पर निकलें, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

-  .NET के लिए Aspose.CAD: सुनिश्चित करें कि आपके .NET प्रोजेक्ट में Aspose.CAD लाइब्रेरी स्थापित है। आप लाइब्रेरी और प्रासंगिक दस्तावेज़ यहां पा सकते हैं[वेबसाइट](https://reference.aspose.com/cad/net/).

- नमूना डीजीएन फ़ाइल: रूपांतरण के लिए एक डीजीएन फ़ाइल तैयार रखें। हमारे उदाहरण में, हम "Nikon_D90_Camera.dgn" का उपयोग करेंगे।

अब, आइए चरण-दर-चरण मार्गदर्शिका के बारे में जानें।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.CAD के लिए आवश्यक नामस्थान आयात करके प्रारंभ करें। यह चरण आपको छवि रूपांतरण को रेखापुंज करने के लिए डीजीएन के लिए आवश्यक कक्षाओं और विधियों तक पहुंचने की अनुमति देता है।

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## चरण 1: डीजीएन फ़ाइल लोड करें

 DGN फ़ाइल को a में लोड करके प्रारंभ करें`CadImage` वस्तु। यह आगामी परिचालनों के लिए आधार प्रदान करता है।

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // आगे की प्रक्रिया के लिए आपका कोड यहां जाता है
}
```

## चरण 2: रैस्टराइज़ेशन विकल्पों को परिभाषित करें

 एक बनाने के`CadRasterizationOptions` अपनी आवश्यकताओं के अनुसार रैस्टराइज़ेशन प्रक्रिया को अनुकूलित करने के लिए ऑब्जेक्ट बनाएं और विभिन्न गुण सेट करें।

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## चरण 3: JpegOptions ऑब्जेक्ट बनाएं

 चूंकि हमारा लक्ष्य डीजीएन फ़ाइल को जेपीईजी में परिवर्तित करना है, इसलिए एक बनाएं`JpegOptions` ऑब्जेक्ट करें और पहले से परिभाषित असाइन करें`CadRasterizationOptions` इसे.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## चरण 4: रेखापुंज छवि सहेजें

 का उपयोग करें`Save` की विधि`CadImage` डीजीएन फ़ाइल को वांछित प्रारूप में एक रेखापुंज छवि में निर्यात करने के लिए क्लास, इस मामले में, एक जेपीईजी।

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.CAD का उपयोग करके DGN फ़ाइल को रैस्टर छवि में निर्यात करने के चरणों को सफलतापूर्वक पार कर लिया है। इस ट्यूटोरियल ने आपको इस कार्यक्षमता को आपके .NET प्रोजेक्ट्स में सहजता से एकीकृत करने के लिए आवश्यक ज्ञान से सुसज्जित किया है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं DGN फ़ाइलों को JPEG के अलावा अन्य प्रारूपों में निर्यात कर सकता हूँ?

A1: हाँ, .NET के लिए Aspose.CAD विभिन्न आउटपुट स्वरूपों का समर्थन करता है। आप चरण 3 में तदनुसार विकल्पों को संशोधित कर सकते हैं।

### Q2 मैं रूपांतरण प्रक्रिया के दौरान अपवादों को कैसे संभाल सकता हूँ?

A2: सुनिश्चित करें कि आपके पास संभावित समस्याओं के समाधान के लिए उचित अपवाद प्रबंधन है, जैसा कि दिए गए कोड में दिखाया गया है।

### Q3: क्या .NET के लिए Aspose.CAD का कोई परीक्षण संस्करण उपलब्ध है?

 उ3: हां, आप नि:शुल्क परीक्षण के साथ उत्पाद का पता लगा सकते हैं। मिलने जाना[यहाँ](https://releases.aspose.com/) अधिक जानकारी के लिए।

### Q4: मैं .NET के लिए Aspose.CAD से संबंधित मुद्दों पर कहां सहायता मांग सकता हूं या चर्चा कर सकता हूं?

 ए4: की ओर जाएं[Aspose.CAD फोरम](https://forum.aspose.com/c/cad/19) सामुदायिक समर्थन और चर्चा के लिए।

### Q5: मैं .NET के लिए Aspose.CAD के लिए अस्थायी लाइसेंस कैसे प्राप्त करूं?

 ए5: विजिट करें[इस लिंक](https://purchase.aspose.com/temporary-license/)अपनी विकास आवश्यकताओं के लिए एक अस्थायी लाइसेंस प्राप्त करने के लिए।