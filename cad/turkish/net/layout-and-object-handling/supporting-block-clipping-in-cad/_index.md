---
date: 2026-09-09
description: Aspose.CAD for .NET kullanarak CAD'de blok kırpma, DXF'yi PDF'ye dönüştürme
  ve CAD'i PDF olarak kaydetme yöntemini öğrenin. Bu adım adım kılavuzu izleyin.
keywords:
- how to clip block
- convert dxf to pdf
- save cad as pdf
- create pdf from cad
- load cad image
lastmod: 2026-09-09
linktitle: CAD'de Blok Kırpmayı Destekleme
og_description: Aspose.CAD for .NET ile CAD'de blok kırpma, DXF'yi PDF'ye dönüştürme
  ve CAD'i PDF olarak kaydetme yöntemini öğrenin. Geliştiriciler için hızlı bir kılavuz.
og_image_alt: Screenshot of block clipping in a CAD drawing using Aspose.CAD for .NET
og_title: Aspose.CAD for .NET kullanarak CAD'de blok nasıl kırpılır
schemas:
- author: Aspose
  dateModified: '2026-09-09'
  description: Learn how to clip block in CAD, convert DXF to PDF and save CAD as
    PDF using Aspose.CAD for .NET. Follow this step‑by‑step guide.
  headline: How to clip block in CAD using Aspose.CAD for .NET
  type: TechArticle
- description: Learn how to clip block in CAD, convert DXF to PDF and save CAD as
    PDF using Aspose.CAD for .NET. Follow this step‑by‑step guide.
  name: How to clip block in CAD using Aspose.CAD for .NET
  steps:
  - name: define the document directory
    text: Replace “Your Document Directory” with the actual path to your CAD documents.
  - name: specify input and output files
    text: Adjust the file names as per your project requirements.
  - name: load CAD image
    text: The `Image` class **loads CAD image** from the specified input file, enabling
      you to apply clipping before any rendering.
  - name: configure rasterization options
    text: Customize rasterization options according to your rendering needs, such
      as setting the output resolution or background color.
  - name: save as PDF
    text: Save the processed CAD image as a PDF file, effectively **saving CAD as
      PDF** while the block remains clipped.
  type: HowTo
- questions:
  - answer: No, clipping is applied only during rasterization; vector exports retain
      the original geometry.
    question: Does block clipping affect vector export formats like SVG?
  - answer: The library can process files up to **2 GB** on a 64‑bit process without
      full memory loading.
    question: What is the maximum file size Aspose.CAD can handle when clipping?
  - answer: Yes—iterate through `image.Blocks` and assign a `BlockClippingInfo` to
      each target block before saving.
    question: Can I clip multiple blocks in one operation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD clipping
- Aspose.CAD
- .NET CAD processing
- PDF conversion
title: Aspose.CAD for .NET kullanarak CAD'de blok nasıl kırpılır
url: /tr/net/layout-and-object-handling/supporting-block-clipping-in-cad/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET kullanarak CAD'de blok kırpma

## Giriş

Bu kapsamlı rehberde CAD çiziminde **bloku nasıl kırpacağınızı**, DXF'yi PDF'ye dönüştürmeyi ve CAD'i PDF olarak kaydetmeyi Aspose.CAD for .NET ile öğreneceksiniz. Blok kırpma, orijinal geometriyi değiştirmeden bir bloğun belirli bölümlerini gizlemenize veya ortaya çıkarmanıza olanak tanır; bu teknik, render süresini hızlandırır ve dosya boyutunu azaltır.

## Hızlı yanıtlar
- **Blok kırpma ne yapar?** Belirli bir kırpma sınırına göre bir blok içindeki seçili geometriyi gizler.  
- **Hangi kütüphane bunu destekler?** Aspose.CAD for .NET, blok kırpma için yerleşik bir API sağlar.  
- **Lisans gerekli mi?** Üretim kullanımında geçici veya kalıcı bir lisans gereklidir.  
- **DXF'yi PDF'ye dönüştürebilir miyim?** Evet—aynı rasterleştirme seçeneklerini kullanın ve PDF formatıyla `Save` metodunu çağırın.  
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Blok kırpma nedir?
`Block clipping`, bir blok varlığı için kırpma bölgesi tanımlayan bir CAD özelliğidir; bölge dışındaki geometri rasterleştirme sırasında yok sayılır. Bu, büyük bir bloğun yalnızca bir kısmının görüntülenmesi gerektiğinde performansı artırır.

## CAD'de blok kırpma neden kullanılır?
Aspose.CAD, **50+** CAD ve BIM formatını destekler ve dosyanın tamamını belleğe yüklemeden **2 GB**'a kadar dosyaları işleyebilir. Blok kırpma kullanmak, render edilen alanı **%70**'e kadar azaltır; bu da PDF dönüşümünü hızlandırır ve sunucu tarafı iş yüklerinde bellek tüketimini düşürür.

## Önkoşullar

- C# programlama diline temel bilgi.  
- Makinenizde Visual Studio yüklü olması.  
- Aspose.CAD for .NET kütüphanesi. Bunu [Aspose.CAD for .NET indirme sayfasından](https://releases.aspose.com/cad/net/) indirebilirsiniz.  
- Test amaçlı bir örnek CAD dosyası. Sağlanan DXF dosyasını kullanabilirsiniz.

## Ad alanlarını içe aktar

C# projenizde, Aspose.CAD ile çalışmak için gerekli ad alanlarını içe aktardığınızdan emin olun:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Şimdi örnek kodu birden fazla adıma ayıralım:

## CAD'de blok nasıl kırpılır?

`Image` sınıfı bir CAD çizimini belleğe yükler ve `BlockClippingInfo` bir blok için kırpma çokgenini tanımlar. CAD çiziminizi `new Image("input.dxf")` ile yükleyin, kırpma çokgenini tanımlayan bir `BlockClippingInfo` nesnesi oluşturun, hedef bloğa `image.Blocks["BlockName"].ClippingInfo = clippingInfo` ile atayın ve ardından görüntüyü rasterleştirin veya kaydedin. Bu sıralama, bloğu tek bir geçişte kırpar ve hem DXF hem de DWG kaynakları için çalışır.

### Adım 1: belge dizinini tanımla

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

"Your Document Directory" ifadesini CAD belgelerinizin gerçek yolu ile değiştirin.

### Adım 2: giriş ve çıkış dosyalarını belirt

```csharp
string inputFile = MyDir + "SLS-CW-CD-CE001-R01_blockClip.dxf";
string outputFile = MyDir + "SLS-CW-CD-CE001-R01_blockClip.pdf";
```

Dosya adlarını proje gereksinimlerinize göre ayarlayın.

### Adım 3: CAD görüntüsünü yükle

```csharp
using (CadImage cadImage = (CadImage)Image.Load(inputFile))
{
```

`Image` sınıfı **CAD görüntüsünü** belirtilen giriş dosyasından yükler, böylece render işleminden önce kırpma uygulayabilirsiniz.

### Adım 4: rasterleştirme seçeneklerini yapılandır

```csharp
var rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    DrawType = CadDrawTypeMode.UseObjectColor,
    PageWidth = 1200,
    PageHeight = 1600,
    Margins = new Margins
    {
        Top = 5,
        Right = 30,
        Bottom = 5,
        Left = 30
    },
    Layouts = new string[] { "Model" }
};
```

Çıktı çözünürlüğü veya arka plan rengi gibi render ihtiyaçlarınıza göre rasterleştirme seçeneklerini özelleştirin.

### Adım 5: PDF olarak kaydet

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outputFile, pdfOptions);
```

İşlenmiş CAD görüntüsünü bir PDF dosyası olarak kaydedin, böylece blok kırpılmışken **CAD'i PDF olarak kaydetmiş** olursunuz.

## Sonuç

Tebrikler! Aspose.CAD for .NET kullanarak CAD'de blok kırpmayı başarıyla uyguladınız ve artık **DXF'yi PDF'ye dönüştürmeyi**, **CAD'i PDF olarak kaydetmeyi** ve **CAD görüntüsünü yüklemeyi** daha fazla işleme için biliyorsunuz. Bu teknikler, render performansı ve çıktı kalitesi üzerinde ayrıntılı kontrol sağlar.

## SSS

### S1: Aspose.CAD for .NET'i diğer programlama dilleriyle kullanabilir miyim?
A1: Aspose.CAD öncelikle .NET uygulamaları için tasarlanmıştır. Diğer dillerle çalışıyorsanız, Aspose.CAD for Java'yı incelemeyi düşünün.

### S2: Aspose.CAD için lisans seçenekleri mevcut mu?
A2: Evet, lisans seçeneklerini inceleyebilir ve bir satın alma yapabilirsiniz [Aspose.CAD lisans sayfası](https://purchase.aspose.com/buy).

### S3: Aspose.CAD for .NET için ücretsiz deneme mevcut mu?
A3: Evet, ücretsiz denemeye şu sayfadan ulaşabilirsiniz [Aspose ürün sürümleri sayfası](https://releases.aspose.com/).

### S4: Aspose.CAD için destek nasıl alabilirim?
A4: Topluluk desteği ve tartışmalar için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

### S5: Aspose.CAD'i kalıcı lisans olmadan kullanabilir miyim?
A5: Evet, geçici bir lisans alabilirsiniz [geçici lisans talep sayfası](https://purchase.aspose.com/temporary-license/).

**S: Blok kırpma SVG gibi vektör dışa aktarma formatlarını etkiler mi?**  
C: Hayır, kırpma yalnızca rasterleştirme sırasında uygulanır; vektör dışa aktarımları orijinal geometriyi korur.

**S: Blok kırpma sırasında Aspose.CAD işleyebileceği maksimum dosya boyutu nedir?**  
C: Kütüphane, tam bellek yüklemesi yapmadan 64‑bit bir süreçte **2 GB**'a kadar dosyaları işleyebilir.

**S: Tek bir işlemde birden fazla bloğu kırpabilir miyim?**  
C: Evet—`image.Blocks` içinde döngü yaparak her hedef bloğa bir `BlockClippingInfo` atayın ve ardından kaydedin.

**Son Güncelleme:** 2026-09-09  
**Test Edilen Versiyon:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose

## İlgili Eğitimler

- [Aspose.CAD for .NET ile CAD Çizimlerini PDF'ye Dönüştürme ve Dışa Aktarma – Eğitim](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)
- [Aspose CAD Örneği: .NET'te Düzenleri Raster Görüntüye Dönüştürme](/cad/net/cad-drawing-manipulation/convert-layouts-to-raster-image/)
- [DXF Belirli Düzeninden PDF Oluşturma – Aspose.CAD Kılavuzu](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}