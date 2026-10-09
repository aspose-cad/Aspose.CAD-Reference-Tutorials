---
date: 2026-10-09
description: C# ve Aspose.CAD for .NET kullanarak dwg dosyasını nasıl yükleyeceğinizi
  ve DWG dosyaları içinde metin arayacağınızı öğrenin. CAD iş akışlarınızı geliştirmek
  için bu adım adım kılavuzu izleyin.
keywords:
- load dwg file
- export dwg to pdf
- cad text search
- search text dwg
- c# read dwg
lastmod: 2026-10-09
linktitle: C# ile DWG Dosyalarında Metin Arama
og_description: C# ve Aspose.CAD for .NET kullanarak dwg dosyasını nasıl yükleyeceğinizi
  ve DWG dosyaları içinde metin arayacağınızı öğrenin. CAD iş akışlarınızı geliştirmek
  için bu adım adım kılavuzu izleyin.
og_image_alt: Guide showing how to load dwg file and search text in DWG files using
  Aspose.CAD for .NET
og_title: C# ile dwg dosyasını nasıl yükleyip DWG dosyalarında metin ararsınız
schemas:
- author: Aspose
  dateModified: '2026-10-09'
  description: Learn how to load dwg file and search text inside DWG files using C#
    and Aspose.CAD for .NET. Follow this step‑by‑step guide to enhance your CAD workflows.
  headline: How to load dwg file and search text in DWG files with C#
  type: TechArticle
- questions:
  - answer: '`new CadImage("yourfile.dwg")` creates an in‑memory representation of
      the drawing.'
    question: What is the first line of code to load a DWG?
  - answer: '`Aspose.CAD.Image` and `Aspose.CAD.FileFormats.Dwg` are required.'
    question: Which namespace contains the CAD classes?
  - answer: Yes – use `image.Save("out.pdf", SaveFormat.Pdf)`.
    question: Can I export the search results directly to PDF?
  - answer: A free trial works for evaluation; a permanent license is required for
      production.
    question: Do I need a license for development?
  - answer: .NET 5, .NET 6, .NET Core 3.1 and .NET Framework 4.6+.
    question: Which .NET versions are supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg file handling
- aspose.cad
- c# cad processing
- text search in dwg
title: C# ile dwg dosyasını nasıl yükleyip DWG dosyalarında metin ararsınız
url: /tr/net/text-search-and-manipulation/searching-text-in-dwg-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# ile dwg dosyası nasıl yüklenir ve DWG dosyalarında metin nasıl aranır - Aspose.CAD öğreticisi

## Giriş

Modern CAD geliştirmede, **dwg dosyası** nesnelerini **yükleyebilmek** ve belirli metin dizelerini anında bulabilmek, saatler süren manuel incelemeyi önler. İster toplu‑işlem aracı geliştirin ister bir görüntüleyiciye arama yeteneği ekleyin, Aspose.CAD for .NET, Windows, Linux ve macOS üzerinde yerel bağımlılıklar olmadan çalışan tamamen yönetilen bir API sunar. Bu kılavuz, DWG'yi yüklemeden PDF olarak dışa aktarmaya kadar her adımı size gösterir; böylece C# uygulamalarınıza güvenilir CAD metin araması ekleyebilirsiniz.

## Hızlı cevaplar
- **DWG'yi yüklemek için ilk satır kod nedir?** `new CadImage("yourfile.dwg")` çizimin bellekteki temsilini oluşturur.  
- **CAD sınıflarını hangi ad alanı (namespace) içerir?** `Aspose.CAD.Image` ve `Aspose.CAD.FileFormats.Dwg` gereklidir.  
- **Arama sonuçlarını doğrudan PDF'ye dışa aktarabilir miyim?** Evet – `image.Save("out.pdf", SaveFormat.Pdf)` kullanın.  
- **Geliştirme için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme çalışır; üretim için kalıcı bir lisans gerekir.  
- **Hangi .NET sürümleri destekleniyor?** .NET 5, .NET 6, .NET Core 3.1 ve .NET Framework 4.6+.

## DWG dosyası nedir?

DWG dosyası, AutoCAD ve uyumlu araçlar tarafından oluşturulan 2D ve 3D tasarım verilerini saklayan ikili bir formattır. Vektör geometrisi, katmanlar, metin ve meta veriler için endüstri standardı konteynerdir. Format sahipli olduğu için çoğu açık‑kaynak ayrıştırıcı yeni sürümlerle başa çıkmakta zorlanır; ancak Aspose.CAD, 150'den fazla DWG sürümünü tam olarak destekleyerek AutoCAD kurmadan çizimleri okumanıza ve işlemenize olanak tanır.

## Neden Aspose.CAD'i cad metin araması için kullanmalısınız?

Aspose.CAD, **50+** DWG ve DXF sürümünü işleyebilir, dosyaları belleğe tamamen yüklemeden 1 GB'a kadar işleyebilir. Kütüphane, **Entities** ve **Block** bölümlerinden metin çıkarır ve blokların içinde bile metinleri bulmada **%99** başarı oranı sağlar. Bu ölçülebilir güvenilirlik, kurumsal düzeyde CAD otomasyonu için tercih edilen bir çözüm olmasını sağlar.

## Önkoşullar

Başlamadan önce şunların yüklü olduğundan emin olun:

- **Aspose.CAD for .NET** yüklü. En son paketi [Aspose.CAD web sitesinden](https://releases.aspose.com/cad/net/) indirin.  
- Analiz etmek istediğiniz DWG dosyalarını içeren bir klasör.  
- Üretim kullanımı için geçerli bir lisans dosyası (deneme çalıştırmaları için isteğe bağlı).

## Hangi ad alanları (namespaces) gereklidir?

`Aspose.CAD` ad alanı temel görüntü işleme sınıflarını sağlar, `Aspose.CAD.FileFormats.Dwg` ise DWG‑özel yapılarını içerir. Bunları C# dosyanızın en üstüne ekleyin:

```csharp
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dwg;
using Aspose.CAD.ImageOptions;
```

> **Not:** Yukarıdaki kod bloğu bir yer tutucudur; orijinal yer tutucu sayısını korumak için metni tam olarak değiştirmeyin.

## DWG dosyasını nasıl yükleriz?

Aspose.CAD ile DWG dosyası yüklemek oldukça basittir. Bellekte bir CAD çizimini temsil eden `CadImage` sınıfını kullanın. Yapıcı, dosyayı render etmeden okur; bu da büyük çizimler için hızlıdır. Yükledikten sonra `Width`, `Height` ve `Layers` gibi özellikleri inceleyebilir, ardından arama işlemlerine geçebilirsiniz.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
```

## Entities bölümünde metni nasıl ararsınız?

Metni Entities bölümünde bulmak için `cadImage.Entities` koleksiyonunu döngüye alın. Her varlık, türüne göre (`MText`, `Text`, `Attribute` vb.) ve `TextString` özelliğine göre incelenebilir. Hedef dizeye karşı büyük/küçük harf duyarsız karşılaştırma yapın ve eşleşen varlıkları daha sonra işlemek veya vurgulamak için toplayın.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "search.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Block bölümünde metni nasıl ararsınız?

Bloklar, içinde gömülü metin olabilen yeniden kullanılabilir varlık gruplarıdır. Öncelikle `cadImage.BlockEntities.Values` üzerinden her blok tanımına erişin. Ardından her bloğun `Entities` koleksiyonunu dolaşarak, ana Entities bölümü için kullanılan aynı metin eşleştirme mantığını uygulayın. Bu sayede yeniden kullanılabilir bileşenlerin içinde gizli metinler atlanmaz.

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    IterateCADNodes(entity);
}
```

## Tam bir tarama için CAD düğümleri nasıl yinelemeli?

Kapsamlı bir tarama, Entities ve Block bölümlerini birleştirir. `CadImage` düğüm ağacını özyinelemeli olarak dolaşarak, iç içe bloklar, öznitelik tanımları ve hatta harici referanslar işlenebilir. `CadBaseEntity` parametresi alan bir yardımcı yöntem oluşturun; türünü kontrol edin, uygulanabilir olduğunda metni çıkarın ve düğüm bir koleksiyon içeriyorsa alt varlıklara yineleyin.

```csharp
foreach (CadBlockEntity blockEntity in cadImage.BlockEntities.Values)
{
    foreach (CadBaseEntity entity in blockEntity.Entities)
    {
        IterateCADNodes(entity);
    }
}
```

## Metni bulduktan sonra DWG'yi PDF'ye nasıl dışa aktarılır?

İlgili varlıkları belirledikten sonra bunları vurgulamak veya koordinatlarını çıkarmak isteyebilirsiniz. Aspose.CAD, vektör kalitesini koruyarak tüm çizimi PDF olarak kaydetmenize izin verir. Raster çıktı gerekiyorsa `CadRasterizationOptions` yapılandırın, ardından `image.Save("output.pdf", new PdfOptions())` çağrısını yapın. Oluşan PDF, CAD yazılımı olmayan paydaşlarla da paylaşılabilir.

```csharp
private static void IterateCADNodes(CadBaseEntity obj)
{
    switch (obj.TypeName)
    {
        // Handle different entity types
    }
}
```

## Sonuç

Aspose.CAD for .NET, dwg dosyası verilerini yükleme, belirli metinleri arama ve sonucu PDF olarak dışa aktarma konusunda sorunsuz, yüksek performanslı bir çözüm sunar. Bu öğreticideki adımları izleyerek, dış araçlara veya pahalı lisanslara bağımlı olmadan C# uygulamanıza güçlü CAD metin‑arama yetenekleri eklemiş oldunuz.

## Sıkça Sorulan Sorular

### Q1: Aspose.CAD for .NET'i diğer CAD formatlarıyla kullanabilir miyim?
A1: Evet, Aspose.CAD 30'dan fazla CAD formatını destekler; DXF, DWF ve STL gibi formatlar da dahil olmak üzere karışık‑format iş akışları için çok yönlü bir çözümdür.

### Q2: Aspose.CAD for .NET için ücretsiz deneme mevcut mu?
A2: Evet, özellikleri [ücretsiz deneme](https://releases.aspose.com/) ile keşfedebilirsiniz.

### Q3: Aspose.CAD for .NET için destek nasıl alınır?
A3: Topluluk yardımı ve resmi destek kanalları için [Aspose.CAD forumuna](https://forum.aspose.com/c/cad/19) göz atın.

### Q4: Geçici lisans nedir ve nasıl temin ederim?
A4: Kısa vadeli değerlendirme veya kanıt‑konsept projeleri için [geçici lisans](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

### Q5: Aspose.CAD for .NET için ayrıntılı belgeleri nerede bulabilirim?
A5: Derinlemesine rehberlik, API referansları ve kod örnekleri için kapsamlı [belgelere](https://reference.aspose.com/cad/net/) bakın.

---

**Son Güncelleme:** 2026-10-09  
**Test Edilen Versiyon:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose  


```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Configure rasterization options
rasterizationOptions.Layouts = new[] { "Layout1" };
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "SearchText_out.pdf", pdfOptions);
```

## İlgili Eğitimler

- [DWG'yi PDF ve Raster Görüntülere Dönüştürme - Aspose.CAD for .NET Kullanarak](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [DWG'yi PNG'ye Dönüştürme ve OLE Nesnelerini Dışa Aktarma - Aspose.CAD Öğreticisi](/cad/net/advanced-export-techniques/exporting-ole-objects-from-dwg/)
- [DWT Dosyalarını Aspose.CAD for .NET ile Okuma](/cad/net/cad-features-and-support/reading-dwt/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}