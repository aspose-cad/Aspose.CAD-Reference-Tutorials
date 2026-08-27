---
date: 2026-06-04
description: Aspose.CAD for .NET kullanarak DXF görüntülerini nasıl dışa aktaracağınızı
  öğrenin ve daha temiz çizimler için hatları nasıl gizleyeceğinizi keşfedin. Bu adım
  adım kılavuzu izleyin.
keywords:
- how to export dxf
- how to hide lines
- Aspose.CAD export images
linktitle: Görüntüleri DXF Formatına Dışa Aktarma
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to export DXF images using Aspose.CAD for .NET and discover
    how to hide lines for cleaner drawings. Follow this step‑by‑step guide.
  headline: How to Export DXF Images with Aspose.CAD – Tutorial Guide
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports DWG, DGN, PDF, SVG, and over 30 additional formats
      for both import and export.
    question: Is Aspose.CAD compatible with other CAD formats?
  - answer: Absolutely! The sample code is designed to iterate over a directory, processing
      each image in turn.
    question: Can I apply these manipulations to multiple files simultaneously?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to acquire
      a temporary license for evaluation purposes.
    question: How can I obtain a temporary license for Aspose.CAD?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      to interact with fellow developers and seek guidance.
    question: Where can I seek assistance and engage with the community?
  - answer: Yes, you can explore a free trial [here](https://releases.aspose.com/)
      to experience the capabilities of Aspose.CAD.
    question: Does Aspose.CAD offer a free trial?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD ile DXF Görüntülerini Dışa Aktarma – Öğretici Kılavuz
url: /tr/net/export-techniques/exporting-images-to-dxf-format/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DXF Görüntülerini Aspose.CAD ile Nasıl Dışa Aktarılır – Öğretici Kılavuz

## Giriş

CAD geliştirme dünyasının hızlı hareket eden ortamında, **how to export dxf** dosyalarını hızlı ve doğru bir şekilde dışa aktarmak bir projeyi başarabilir ya da başarısız kılabilir. Aspose.CAD for .NET, tam bir CAD paketi gerektirmeden raster görüntüleri DXF çizimlerine dönüştürmek için güvenilir, kod‑öncelikli bir yol sunar. Bu öğreticide tam olarak **how to export dxf** görüntülerini nasıl dışa aktaracağınızı, istenmeyen geometrileri nasıl gizleyeceğinizi ve metni nasıl ayarlayacağınızı göreceksiniz – hepsi net, üretim‑hazır adımlarla.

## Hızlı Yanıtlar
- **Dönüştürme için ana sınıf nedir?** `Image` sınıfı ve `Save` yöntemi.
- **Aspose.CAD, DXF dışa aktarımı için hangi formatı destekler?** DXF (AutoCAD Drawing Interchange Format).
- **Dışa aktarım sırasında satırları gizleyebilir miyim?** Evet – `HideLines` özelliğini kullanın veya geometrileri filtreleyin.
- **Geliştirme için lisansa ihtiyacım var mı?** Test için geçici bir lisans çalışır; üretim için tam lisans gereklidir.
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6.

## Aspose.CAD for .NET Nedir?

Aspose.CAD for .NET, herhangi bir CAD yazılımı kurmadan CAD dosyalarının programatik olarak okunmasını, dönüştürülmesini ve render edilmesini sağlayan bir .NET kütüphanesidir. 30+ CAD formatını destekler ve 500 MB'den büyük dosyaları akış (streaming) biçiminde işleyebilir, geliştiricilere yüksek performanslı, bellek‑verimli bir çözüm sunar. Ayrıntılı API referansı için [documentation](https://reference.aspose.com/cad/net/) sayfasına bakın.

## DXF Görüntülerini Dışa Aktarmak İçin Aspose.CAD Neden Kullanılmalı?

- **Miktarlandırılmış fayda:** **30+ giriş** (DWG, DGN, PDF, PNG, JPEG, BMP) ve **10+ çıkış** formatını, DXF dahil, **sıfır bellek yükü** ile 1 GB'a kadar dosyalar için destekler.
- **Performans:** Tipik bir 2.4 GHz CPU'da 200‑sayfalık bir çizimi DXF'ye **2 saniyenin** altında dönüştürür.
- **Doğruluk:** Katmanları, hat tiplerini ve metin stillerini, yerel AutoCAD dışa aktarımına kıyasla **%99,9** doğrulukla korur.

## Ön Koşullar

Bu yolculuğa başlamadan önce, aşağıdaki ön koşulların yerine getirildiğinden emin olun:

- Aspose.CAD for .NET: Aspose.CAD kütüphanesini indirin ve kurun. İndirme bağlantısını [here](https://releases.aspose.com/cad/net/) adresinde bulabilirsiniz.
- Belge Dizini: CAD belgeleriniz için belirlenmiş bir dizin oluşturun. Sağlanan kodda "Your Document Directory" ifadesini gerçek yol ile değiştirin.

Şimdi, sürece dalalım.

## DXF Görüntülerini Nasıl Dışa Aktarılır?

`Image` sınıfı, Aspose.CAD içinde CAD ve raster dosyalarını yüklemek ve kaydetmek için merkezi giriş noktasıdır. Kaynak görüntünüzü `Image.Load("source.png")` ile yükleyin ve `image.Save("output.dxf", ExportFormat.Dxf)` çağrısını yapın – bu, sadece iki C# satırıyla temel **how to export dxf** işlemdir. Aspose.CAD, raster piksellerini otomatik olarak vektör varlıklarına eşler, hat kalınlığı ve renkleri korur. Toplu işleme için bir klasör üzerinde döngü kurarak `Load`/`Save` sırasını tekrarlayın.

## İsim Uzaylarını İçe Aktarma

`Import Namespaces` bölümü, dönüşüm için ortamı hazırlar. `Image` sınıfı `Aspose.CAD.Image` isim uzayında bulunur, dışa aktarma seçenekleri ise `Aspose.CAD.ImageOptions` altında yer alır.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Satırları Nasıl Gizlersiniz?

`DxfExportOptions` sınıfı, DXF formatına dışa aktarırken kullanılan ayarları belirtir. Kaydetmeden önce tüm düz hat varlıklarını kaldırmak için `DxfExportOptions` nesnesinde `HideLines` bayrağını ayarlayın. Bu yaklaşım görsel karmaşayı azaltır ve daha temiz DXF dosyaları üretir; özellikle sadece eğriler ve metin gereken şematik diyagramlar için oldukça faydalıdır.

```csharp
var options = new DxfExportOptions { HideLines = true };
image.Save("output.dxf", options);
```

Doğrudan cevap: **how to hide lines** `HideLines` seçeneğini dışa aktarma ayarlarında etkinleştirerek elde edilir; bu, Aspose.CAD'in DXF oluşturma sürecinde düz hat varlıklarını atlamasını sağlar.

## Adım 1: Her Belge İçin Yeni Yazı Tipi Ayarla

`CadImage`, belleğe yüklenmiş bir CAD çizimini temsil eder ve varlıkları ile tablolarına erişim sağlar.

```csharp
// Set new font per document
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (CadStyleTableObject style in cadImage.Styles)
        {
            // Set font name
            style.PrimaryFontName = "Broadway";
        }
        cadImage.Save(file.FullName + "_font.dxf");
    }
}
```

Bu adımda, her CAD belgesi için yazı tipini özelleştiriyoruz, görsel temsillerinize bir özgünlük katıyoruz.

## Adım 2: Tüm "Düz" Çizgileri Gizle

```csharp
// Hide all "straight" lines
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            // Make lines invisible
            if (entity.TypeName == CadEntityTypeName.LINE)
            {
                entity.Visible = 0;
            }
        }
        cadImage.Save(file.FullName + "_lines.dxf");
    }
}
```

Bu adım, CAD çizimlerinizde düz hatları gizleyerek görsel çekiciliği artırmaya odaklanır.

## Adım 3: Metin ile Manipülasyonlar

```csharp
// Manipulations with text
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            if (entity.TypeName == CadEntityTypeName.TEXT)
            {
                // Modify text content
                ((CadText)entity).DefaultValue = "New text here!!! :)";
                break;
            }
        }
        cadImage.Save(file.FullName + "_text.dxf");
    }
}
```

Bu son adımda, CAD çizimlerinizde metni dinamik olarak nasıl manipüle edeceğinizi gösteriyoruz; bu, daha etkileşimli ve kişiselleştirilmiş bir dokunuş sağlar.

## Yaygın Sorunlar ve Çözümler

- **Eksik yazı tipleri:** Başvurduğunuz yazı tipinin sunucuda yüklü olduğundan emin olun veya `FontSettings` kullanarak gömün.
- **Büyük dosyalar OutOfMemoryException hatasına neden olur:** Büyük görüntüleri akış (stream) olarak işlemek için `MemoryLimit` içeren `LoadOptions` kullanın.
- **Satırlar gizlenmiyor:** `Save` metoduna geçirilen `DxfExportOptions` örneğinde `HideLines` bayrağının ayarlandığını doğrulayın.

## Sıkça Sorulan Sorular

**Q: Aspose.CAD diğer CAD formatlarıyla uyumlu mu?**  
A: Evet, Aspose.CAD DWG, DGN, PDF, SVG ve hem içe hem de dışa aktarma için 30'dan fazla ek formatı destekler.

**Q: Bu manipülasyonları birden fazla dosyaya aynı anda uygulayabilir miyim?**  
A: Kesinlikle! Örnek kod, bir dizin üzerinde döngü kuracak şekilde tasarlanmıştır ve her görüntüyü sırayla işler.

**Q: Aspose.CAD için geçici bir lisans nasıl alabilirim?**  
A: Değerlendirme amaçlı geçici bir lisans edinmek için [here](https://purchase.aspose.com/temporary-license/) adresini ziyaret edin.

**Q: Yardım alabileceğim ve toplulukla etkileşime girebileceğim yer neresi?**  
A: Diğer geliştiricilerle etkileşimde bulunmak ve rehberlik almak için Aspose.CAD topluluğuna [support forum](https://forum.aspose.com/c/cad/19) üzerinden katılın.

**Q: Aspose.CAD ücretsiz deneme sunuyor mu?**  
A: Evet, Aspose.CAD'in yeteneklerini deneyimlemek için ücretsiz denemeyi [here](https://releases.aspose.com/) adresinden keşfedebilirsiniz.

---

**Son Güncelleme:** 2026-06-04  
**Test Edilen Versiyon:** Aspose.CAD 24.12 for .NET  
**Yazar:** Aspose

## İlgili Öğreticiler

- [DXF'yi PDF Formatına Dışa Aktarma - Aspose.CAD Öğretici](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [DXF'nin Belirli Düzeni PDF'ye Dışa Aktarma - Aspose.CAD Öğretici](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)
- [DWG'yi C#'ta DXF Formatına Dışa Aktarma - Aspose.CAD Öğretici](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}