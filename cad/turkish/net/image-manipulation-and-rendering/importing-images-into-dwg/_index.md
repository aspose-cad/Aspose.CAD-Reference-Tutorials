---
date: 2026-08-17
description: C# ve Aspose.CAD for .NET kullanarak dwg dosyalarına resim eklemeyi öğrenin.
  Bu rehber, resim ithalatı, ekleme noktalarının ayarlanması ve PDF'ye dışa aktarma
  süreçlerini adım adım gösterir.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: C# ile DWG Dosyalarına Resim İçe Aktarma
og_description: C# kullanarak dwg dosyalarına resim eklemeyi öğrenin. Bu öğretici,
  resim ithalatı, ekleme noktalarının ayarlanması ve dwg'yi Aspose.CAD ile pdf'ye
  dönüştürmeyi kapsar.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: C# ve Aspose.CAD kullanarak dwg dosyalarına resim ekleme
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: C# ve Aspose.CAD kullanarak dwg dosyalarına resim ekleme
url: /tr/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# ile Aspose.CAD kullanarak dwg dosyalarına resim ekleme

## Giriş

DWG dosyasına bir resim eklemek, CAD çizimlerini logo, fotoğraf veya raster grafiklerle zenginleştirmeniz gerektiğinde rutin bir gereksinimdir. Bu öğreticide C# ve Aspose.CAD for .NET kullanarak **dwg'ye resim eklemeyi** programatik olarak öğrenecek, ardından isteğe bağlı olarak sonucu PDF'ye dönüştürebileceksiniz. Adımlar, kendi projenize kopyalayıp yapıştırabileceğiniz şekilde bölünmüştür.

## Hızlı cevaplar
- **Hangi kütüphane işi yürütür?** Aspose.CAD for .NET.
- **PNG dosyalarını gömebilir miyim?** Evet – PNG, JPEG, BMP ve diğer raster formatlar desteklenir.
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme testi için yeterlidir; üretim için ticari lisans gereklidir.
- **PDF dışa aktarma destekleniyor mu?** Kesinlikle – güncellenen DWG'yi tek bir satırda PDF'ye dönüştürebilirsiniz.
- **Hangi .NET sürümleri uyumludur?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## DWG dosyası nedir?

DWG dosyası, Autodesk AutoCAD çizimlerinin yerel ikili formatıdır, vektör geometrisi, katmanlar ve meta verileri depolar. Mimarlık, mühendislik ve inşaatta yaygın olarak kullanılır ve Aspose.CAD, AutoCAD yüklü olmadan bu formatı okuyup yazabilir.

## Aspose.CAD ile dwg'ye neden resim ekleyelim?

Aspose.CAD **50+ giriş ve çıkış formatını** destekler, dosyaları belleğe tamamen yüklemeden 500 MB'den büyük dosyaları işleyebilir ve başsız sunucu ortamlarında çalışan deterministik bir API sunar. Bu, DWG çizimlerinin toplu işlenmesini hızlı ve güvenilir kılar.

## Önkoşullar
- C# programlama temelleri.
- Aspose.CAD for .NET yüklü. İndirmek için [Aspose.CAD for .NET indirme sayfasını](https://releases.aspose.com/cad/net/) ziyaret edin. Diğer Aspose ürünlerini ise [Aspose sürüm sayfasında](https://releases.aspose.com/) keşfedebilirsiniz.
- Visual Studio 2022 veya daha yeni bir geliştirme ortamı.

## Aspose.CAD kullanarak dwg'ye nasıl resim eklenir?

Hedef DWG'yi yükleyin, eklemek istediğiniz resmi tanımlayan bir raster görüntü nesnesi oluşturun, ekleme noktasını ve ölçek vektörlerini ayarlayın, ardından resmi çizime ekleyin. Son olarak, değiştirilmiş DWG'yi kaydedin veya doğrudan PDF olarak dışa aktarın. Tüm iş akışı sadece birkaç API çağrısı gerektirir ve tipik 2‑sayfalık çizimler için bir saniyeden az sürer.

### Ad alanlarını içe aktar
CAD sınıflarını kullanabilmek için gerekli ad alanlarını ekleyin.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Adım 1: belge dizininizi ayarlayın
Kaynak DWG ve eklemek istediğiniz resmin bulunduğu klasörü hazırlayın.

```csharp
string MyDir = "Your Document Directory";
```

### Adım 2: dwg dosyasını yükleyin
`CadImage` sınıfı bir DWG çizimini temsil eder ve varlıklarına, katmanlarına ve meta verilerine erişim sağlar.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Adım 3: resim özelliklerini tanımlayın
Raster dosyasına (ör. PNG) işaret eden bir `Image` nesnesi oluşturun ve formatını belirtin.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Adım 4: ekleme noktasını ve vektörleri ayarlayın
Resmin çizim içinde nerede görüneceğini ve nasıl ölçekleneceğini belirleyin. Ekleme noktası 2‑D bir koordinatla tanımlanırken, vektörler genişlik ve yüksekliği kontrol eder.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Adım 5: raster görüntüyü oluşturup yapılandırın
Bir `RasterImage` nesnesi örnekleyin, görüntü verisini atayın ve ek render seçeneklerini ayarlayın.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Adım 6: dwg dosyasına resmi ekleyin
Yapılandırılmış raster görüntüyü DWG'nin varlık koleksiyonuna ekleyerek çizimin bir parçası haline getirin.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Adım 7: pdf olarak kaydedin (dwg'yi pdf'ye dışa aktarın)
Resmi gömdükten sonra **dwg'yi pdf'ye dönüştürebilir** veya **dwg'yi pdf olarak kaydedebilirsiniz** tek bir çağrı ile. Bu, CAD yazılımı olmayan paydaşlarla çizimi paylaşmak için kullanışlıdır.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Resim gömdükten sonra dwg'yi pdf'ye nasıl dönüştürülür?

`CadImage` örneği üzerinde `Save` metodunu `SaveFormat.Pdf` ve isteğe bağlı olarak sayfa boyutu, rasterleştirme ve meta veri kontrolü sağlayan bir `PdfOptions` nesnesi ile çağırın. Aspose.CAD, gömülü raster görüntüyü, katmanları ve hat kalınlıklarını koruyarak herhangi bir görüntüleyicide açılabilen doğru bir PDF temsili üretir. Bu dönüşüm tek bir kod satırıyla gerçekleştirilir.

## Yaygın sorunlar ve çözümler
- **Resim yanlış konumda görünüyor** – ekleme noktası koordinatlarını ve yön vektörlerini iki kez kontrol edin; bunlar çizimin orijinine göre görecelidir.
- **Büyük resimler bellek dalgalanmalarına neden oluyor** – eklemeden önce raster görüntüde `Resize` seçeneğini kullanın veya daha düşük çözünürlüklü bir kopya ile çalışın.
- **PDF dışa aktarımı vektör kalitesini kaybediyor** – vektör verisini koruyan `PdfOptions` ile kaydettiğinizden emin olun; raster görüntüler her zaman olduğu gibi gömülür.

## Sıkça sorulan sorular

**Q: Aspose.CAD for .NET'i diğer programlama dilleriyle kullanabilir miyim?**  
A: Çekirdek kütüphane .NET‑özelidir, ancak Aspose Java, Python ve diğer platformlar için eşdeğer API'ler sunar.

**Q: Aspose.CAD için ücretsiz deneme mevcut mu?**  
A: Evet, [Aspose ücretsiz deneme sayfasında](https://releases.aspose.com/) ücretsiz deneme keşfedebilirsiniz.

**Q: Aspose.CAD için ayrıntılı belgeleri nerede bulabilirim?**  
A: Belgeler [Aspose.CAD .NET API referansında](https://reference.aspose.com/cad/net/) mevcuttur.

**Q: Aspose.CAD için geçici bir lisans nasıl alınır?**  
A: Geçici lisans almak için [geçici lisans sayfasını](https://purchase.aspose.com/temporary-license/) ziyaret edin.

**Q: Aspose.CAD desteği için topluluk forumları var mı?**  
A: Evet, [Aspose.CAD topluluk forumunda](https://forum.aspose.com/c/cad/19) destek alabilir ve toplulukla etkileşime geçebilirsiniz.

---

**Last Updated:** 2026-08-17  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## İlgili Öğreticiler

- [DWG'yi PDF veya Raster Görüntülere Dışa Aktarma - Aspose.CAD Rehberi](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [C# ile DWG'yi DXF Formatına Dışa Aktarma - Aspose.CAD Öğreticisi](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Belirli Düzenleri PDF'ye Dışa Aktarma - Aspose.CAD Rehberi](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}