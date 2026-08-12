---
date: 2026-08-12
description: DWG'den metin çıkarın ve belirli bir DWG'yi .NET için Aspose.CAD kullanarak
  C#'ta görüntüye dönüştürün. Adım adım kod örnekleriyle öğrenin.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Belirli bir DWG'yi C#'ta Görüntüye Dönüştürme
og_description: DWG'den metin çıkarın ve belirli bir DWG'yi Aspose.CAD ile C#'ta görüntüye
  dönüştürün. Hızlı uygulama için bu özlü kılavuzu izleyin.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: DWG'den metin çıkarın ve belirli bir DWG'yi C#'ta görüntüye dönüştürün
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: DWG'den metin çıkarın ve belirli bir DWG'yi C#'ta görüntüye dönüştürün
url: /tr/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#'ta belirli DWG'yi görüntüye dönüştürme - Aspose.CAD rehberi

## Giriş

Modern mühendislik uygulamalarında, genellikle **DWG'den metin çıkarma** ve **belirli DWG'yi görüntüye dönüştürme** formatları raporlama veya görselleştirme için gerekir. Aspose.CAD for .NET, dış CAD yazılımı gerektirmeden bu iki görevi de yöneten tam özellikli bir API sunar. Bu öğreticide, bir DWG'yi nasıl yükleyeceğinizi, metin varlıklarını nasıl filtreleyeceğinizi, çizimi rasterleştireceğinizi ve sonunda sonucu PDF görüntüsü olarak nasıl kaydedeceğinizi—temiz C# kodu ile öğreneceksiniz.

## Hızlı cevaplar

- **İlk adım nedir?** Load the DWG file with `new CadImage("file.dwg")`.  
- **Hangi sınıf metni filtreler?** Use `CadEntityFilter` to select `Text` entities.  
- **Görüntü boyutunu nasıl tanımlarsınız?** Set `Width` and `Height` on `CadRasterizationOptions`.  
- **Hangi çıktı formatı kullanılıyor?** The example saves to PDF, which embeds the raster image.  
- **Üretim için lisansa ihtiyacım var mı?** Yes – a commercial Aspose.CAD license removes evaluation limits.

## DWG'den metin nasıl çıkarılır?

DWG'yi yükleyin, yalnızca metin varlıklarını seçen bir filtre uygulayın ve ardından her varlığın `TextString` özelliğini okuyun. Bu yaklaşım, çizimde mevcut olan tüm açıklama, etiket veya ölçü metinlerini döndürür ve bunları arama, indeksleme veya raporlama için yeniden kullanmanıza olanak tanır.

## Neden belirli dwg'yi görüntüye dönüştürürsünüz?

Bir DWG'yi raster görüntüye dönüştürmek, çizimi yerel CAD formatlarını render edemeyen belgeler, web sayfaları veya mobil uygulamalara yerleştirmenizi sağlar. Aspose.CAD **50+ CAD formatının** üzerinde işlem yapar ve çok sayfalı (yüzlerce sayfa) çizimleri 200 MB'den az bellek kullanarak rasterleştirebilir; bu da yüksek verimli sunucu senaryoları için uygundur.

## Önkoşullar

- C# projelerini derlemek ve çalıştırmak için Visual Studio (herhangi bir yeni sürüm).  
- Aspose.CAD for .NET – kütüphanenin yüklü olduğundan emin olun. İndirme bağlantısını **[Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/)** adresinde bulabilirsiniz.  
- Üzerinde çalışmak istediğiniz bir DWG dosyası; örnek dosya *visualization_-_conference_room.dwg* kod parçacıklarında kullanılmıştır.

## Ad alanlarını içe aktar

Aşağıdaki ad alanları, temel CAD sınıflarına, rasterleştirme seçeneklerine ve PDF çıktı yardımcılarına erişim sağlar:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Adım 1: dwg dosyasını yükleyin

`CadImage` örneğini, DWG dosyanızın yolunu geçirerek oluşturun. `CadImage` nesnesi, tüm çizimi bellekte temsil eder ve katmanlarına, varlıklarına ve meta verilerine erişim sağlar.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Adım 2: varlıkları filtrele

`CadEntityFilter`, yalnızca ihtiyacınız olan varlıkları seçmenizi sağlar. Bu rehberde, **metin** nesnelerini tutacak şekilde yapılandırıyoruz; çizgileri, daireleri ve son görüntüde istemediğiniz diğer geometrileri dışarı atıyoruz.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Adım 3: rasterleştirme seçeneklerini ayarla

`CadRasterizationOptions`, çizimin bitmap'e nasıl dönüştürüleceğini kontrol eder. Çıktı boyutunu, arka plan rengini ve çözünürlüğü (DPI) tanımlayabilirsiniz. Aşağıdaki tanım bağlantısı sınıfı tanıtır:

`CadRasterizationOptions` sınıfı, CAD çizimlerini raster formatlara dönüştürmek için görüntü boyutlarını, çözünürlüğü ve render ayarlarını belirtir.  

Seçenekleri PDF dışa aktarıcıya geçirmeden önce istenen genişlik, yükseklik ve arka plan rengini ayarlayın.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Adım 4: PDF seçeneklerini ayarla

`PdfOptions`, rasterleştirme ayarlarını sıkıştırma gibi PDF‑özelliği özelliklerle birleştirir. Bu sınıfın tanım bağlantısı ilk olarak görülür:

`PdfOptions`, PDF oluşturma parametrelerini kapsar; rasterleştirme seçenekleri, CAD verilerinin PDF belgesi içinde nasıl render edildiğini belirler.  

Önceden oluşturulan `CadRasterizationOptions` örneğini `VectorRasterizationOptions` özelliğine atayın.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Adım 5: PDF olarak kaydet

Son olarak, `CadImage` nesnesinin `Save` metodunu çağırın, hedef dosya adını ve yapılandırılmış `PdfOptions`'ı geçirin. PDF, filtrelenmiş çizimin yüksek kaliteli bir görüntüsünü içerecektir.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Yaygın sorunlar ve hata ayıklama

- **Filtreleme sonrası eksik metin** – DWG'nin gerçekten `Text` varlıkları içerdiğinden emin olun; bazı çizimler açıklamaları `MText` olarak saklar. Gerekirse filtreyi `MText` içerecek şekilde ayarlayın.  
- **Boş çıktı görüntüsü** – Rasterleştirme DPI'sının yeterince yüksek (300 DPI güvenli bir varsayılandır) olduğunu ve PDF'yi görüntülerken arka plan renginin şeffaf olarak ayarlanmadığını doğrulayın.  
- **Büyük dosyalarda bellek yetersizliği hataları** – Akışı etkinleştiren `LoadOptions` aşırı yüklemesini kullanın; bu, tüm dosyanın bir kerede belleğe yüklenmesini önler.

## Sıkça sorulan sorular

**Q: Aspose.CAD tüm DWG dosyası sürümleriyle uyumlu mu?**  
A: Aspose.CAD, AutoCAD 2000'den en yeni 2024 sürümüne kadar DWG sürümlerini destekler ve alanda oluşturulan dosyaların %90'ından fazlasını kapsar.

**Q: Farklı çıktılar için rasterleştirme seçeneklerini özelleştirebilir miyim?**  
A: Evet – çözünürlüğü, görüntü formatını, anti‑aliasing'i ve arka plan rengini PNG, JPEG veya PDF hedeflerine göre değiştirebilirsiniz.

**Q: Ek örnekler ve belgeler nerede bulunabilir?**  
A: Daha fazla kod örneği ve API detayları için kapsamlı [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) adresini inceleyin.

**Q: Aspose.CAD için ücretsiz deneme sürümü mevcut mu?**  
A: Kesinlikle – **[Aspose trial download page](https://releases.aspose.com/)** adresinden bir deneme sürümü indirebilir ve 30 gün boyunca tüm özellikleri kısıtlama olmadan değerlendirebilirsiniz.

**Q: Destek nasıl alabilirim veya toplulukla nasıl iletişime geçebilirim?**  
A: Geliştiricilerin çözümler paylaştığı ve Aspose ekibinin soruları yanıtladığı aktif [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) forumuna katılın.

---

**Son Güncelleme:** 2026-08-12  
**Test Edilen:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose

## İlgili Öğreticiler

- [C# ile DWG Dosyalarında Metin Arama - Aspose.CAD Öğreticisi](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [.NET için Aspose.CAD'de CAD Çizimini Raster Görüntüye Dönüştürme](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [C# ile DWG Belgelerini Render Etme - Aspose.CAD Rehberi](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}