---
date: 2026-07-04
description: Aspose.CAD for .NET kullanarak 3D CAD images'den PDF sayfa boyutunu nasıl
  ayarlayacağınızı ve PDF'yi nasıl dışa aktaracağınızı öğrenin – DWG'yi PDF'ye dönüştürmek
  ve CAD'i PDF olarak kaydetmek için adım adım bir rehber.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: 3D Görüntüleri PDF'ye Dışa Aktarma
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: PDF sayfa boyutunu ayarlama – Aspose.CAD ile 3D Görüntüleri PDF'ye Dışa Aktarma
url: /tr/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 3D Görüntüleri PDF'ye Dışa Aktarma - Aspose.CAD Öğreticisi

## Giriş

3‑D CAD çizimini PDF'ye dönüştürürken **PDF sayfa boyutunu ayarlamanız** gerekiyorsa, doğru yerdesiniz. Bu öğretici, adım adım, bir CAD dosyasını nasıl yükleyeceğinizi, rasterleştirme seçeneklerini—özel sayfa boyutları dahil—nasıl yapılandıracağınızı ve Aspose.CAD for .NET kullanarak yüksek doğrulukta bir PDF nasıl oluşturacağınızı gösterir. Sonunda **CAD'den PDF dışa aktarabilir**, **CAD'yi PDF olarak kaydedebilir** ve AutoCAD kurmadan her düzen ayrıntısını kontrol edebileceksiniz.

## Hızlı Cevaplar
- **“CAD'den PDF dışa aktarma” ne anlama geliyor?** Bir CAD çizimini (DWG, DXF, DGN vb.) herhangi bir cihazda açılabilen bir PDF'ye dönüştürür.  
- **Dönüşümü hangi kütüphane gerçekleştiriyor?** Aspose.CAD for .NET, harici bağımlılıklar olmadan rasterleştirme ve PDF dışa aktarımı sağlar.  
- **Bir lisansa ihtiyacım var mı?** Üretim için geçici veya tam lisans gereklidir; ücretsiz deneme mevcuttur.  
- **Özel sayfa boyutları ayarlayabilir miyim?** Evet—`RasterizationOptions` içinde `PageWidth` ve `PageHeight` kullanın.  
- **3‑D geometri korunacak mı?** 3‑D varlıklar rasterleştirilir; tam 3‑D desteği için `TypeOfEntities.Entities3D` etkinleştirin.

## CAD bağlamında “PDF dışa aktarma” nedir?

CAD'den PDF dışa aktarmak, bir CAD çizimini (DWG, DXF, DGN vb.) vektör grafikleri, rasterleştirilmiş 3‑D görünümler ve kesin sayfa düzeni bilgileri içerebilen bir PDF dosyasına dönüştürmek anlamına gelir; bu sayede CAD yazılımı olmayan herkesle kolayca paylaşılabilir.

## PDF dışa aktarmak için neden Aspose.CAD kullanmalı?

Aspose.CAD, **PDF sayfa boyutunu ayarlamanıza** ve PDF'leri tamamen yönetilen .NET kodu içinde dışa aktarmanıza olanak tanır. 50'den fazla CAD formatını destekler, dosyaları belleğe tamamını yüklemeden 2 GB'a kadar işler ve çizgi kalınlıklarını, renkleri ve isteğe bağlı 3‑D varlık renderlamasını 1200 DPI'ye kadar rasterleştirme ile korur. Kütüphane Windows, Linux ve macOS'ta çalışır, böylece oluşturulan PDF'ler herhangi bir platformda kullanılabilir.

## Önkoşullar

- **Aspose.CAD for .NET** yüklü. [Aspose.CAD for .NET indirme sayfasından](https://releases.aspose.com/cad/net/) indirin.  
- Dönüştürmek istediğiniz CAD dosyalarını içeren bir klasör (ör. `C:\CAD\`).  
- .NET 6.0 veya daha yeni (veya .NET Framework 4.7.2).  

## Ad Alanlarını İçe Aktarma

`using` ifadeleri, rasterleştirme ve PDF seçenekleriyle çalışmak için gereken Aspose.CAD ad alanlarını içe aktarır.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Adım Adım Kılavuz

### CAD'den PDF'ye dışa aktarırken PDF sayfa boyutunu nasıl ayarlarsınız?

CAD dosyanızı yükleyin, `RasterizationOptions` içinde sayfa boyutlarını yapılandırın, bu seçenekleri bir `PdfOptions` örneğine ekleyin ve `Save` metodunu çağırın. Bu dört adımlı akış, kodu kısa tutarken çıktı boyutu ve kalitesi üzerinde tam kontrol sağlar.

### Adım 1: CAD Görüntüsünü Yükleyin

`Image` sınıfı, belleğe yüklenmiş ve rasterleştirmeye hazır bir CAD çizimini temsil eder.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Adım 2: Rasterleştirme Seçeneklerini Yapılandırın (CAD'yi PDF Olarak Kaydedin)

`RasterizationOptions` sınıfı, CAD verisinin nasıl rasterleştirileceğini tanımlar; sayfa boyutu, DPI ve 3‑D varlıkların renderlanıp renderlanmayacağı gibi ayarları içerir.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Adım 3: PDF Seçeneklerini Ayarlayın (CAD'den PDF Oluşturun)

`PdfOptions` sınıfı, çıktı formatı ayarlarını tutar ve rasterleştirme seçeneklerini PDF oluşturma ile bağlar.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Adım 4: PDF Olarak Kaydedin (3D Modelden PDF Oluşturun)

`Image` nesnesindeki `Save` metodu, rasterleştirilmiş içeriği belirtilen PDF dosyasına yazar ve paylaşılmaya hazır bir belge üretir.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Yaygın Sorunlar ve Çözümleri

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| **Çıktı PDF'si boş** | Yanlış düzen adı veya eksik `Model` düzeni. | `rasterizationOptions.Layouts` değerinin CAD dosyasındaki mevcut bir düzenle eşleştiğini doğrulayın. |
| **Düşük çözünürlük** | Varsayılan rasterleştirme DPI'si düşük. | Kaydetmeden önce `rasterizationOptions.Resolution = 300;` olarak ayarlayın. |
| **3‑D varlıklar gösterilmiyor** | `TypeOfEntities` yorum satırı olarak bırakılmış. | `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;` satırının yorumunu kaldırın. |
| **Lisans istisnası** | Lisans olmadan deneme sürümü kullanılıyor. | `License license = new License(); license.SetLicense("Aspose.CAD.lic");` kodu ile geçici veya kalıcı lisans uygulayın. |

## Sıkça Sorulan Sorular

**S: Aspose.CAD tüm CAD dosya formatlarıyla uyumlu mu?**  
C: Evet, Aspose.CAD, DWG, DXF, DGN, STL ve IFC dahil olmak üzere 50'den fazla giriş ve çıkış formatını destekler, böylece herhangi bir proje için esneklik sağlar.

**S: PDF'ye dışa aktarırken sayfa boyutlarını özelleştirebilir miyim?**  
C: Kesinlikle. `Save` metodunu çağırmadan önce `RasterizationOptions` içinde `PageWidth` ve `PageHeight` değerlerini nokta, inç veya milimetre cinsinden istediğiniz boyuta ayarlayın.

**S: Aspose.CAD için geçici lisanslar mevcut mu?**  
C: Evet, [Temporary License](https://purchase.aspose.com/temporary-license/) adresini ziyaret ederek Aspose.CAD için geçici lisans alabilirsiniz.

**S: Ek destek veya topluluk tartışmalarını nerede bulabilirim?**  
C: Uzman yardımı ve eş‑eş danışmanlık için [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) adresine gidin.

**S: Aspose.CAD'in ücretsiz deneme sürümü var mı?**  
C: Evet, [free trial](https://releases.aspose.com/) adresine erişerek Aspose.CAD'in özelliklerini keşfedebilirsiniz.

## Sonuç

Artık Aspose.CAD for .NET kullanarak **PDF sayfa boyutunu ayarlamak** ve **3D CAD görüntülerinden PDF dışa aktarmak** için eksiksiz, üretime hazır bir yönteme sahipsiniz. Rasterleştirme seçeneklerini ayarlayarak çözünürlük, sayfa düzeni ve 3‑D varlık renderlamasını istediğiniz belge gereksinimlerine göre ince ayar yapabilirsiniz. Farklı DPI ayarları ve sayfa boyutlarıyla deney yaparak dosya boyutu ile görsel doğruluk arasında mükemmel dengeyi yakalayın.

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Belirli Düzenleri PDF'ye Dışa Aktarma - Aspose.CAD Kılavuzu](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [DWG'yi PDF veya Raster Görüntülere Dışa Aktarma - Aspose.CAD Kılavuzu](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Aspose.CAD for .NET'te DGN'yi PDF'ye Dışa Aktarma](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Last Updated:** 2026-07-04  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose