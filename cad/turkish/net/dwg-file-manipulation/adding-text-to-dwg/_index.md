---
date: 2026-04-06
description: C# ve Aspose.CAD kullanarak DWG'yi PDF'ye dönüştürmeyi ve özel metin
  eklemeyi öğrenin. Bu adım adım kılavuz, DWG'den PDF oluşturmayı, bir metin varlığı
  eklemeyi ve DWG metin fontunu değiştirmeyi kapsar.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: C#'ta DWG Dosyalarına Metin Ekleme
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG'yi PDF'ye Dönüştür ve C#'ta Metin Ekle – Aspose.CAD Öğreticisi
url: /tr/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi PDF'ye Dönüştürme ve C#'ta Metin Ekleme – Aspose.CAD Öğreticisi

## Giriş

CAD ve .NET geliştirme dünyasının hızlı hareket eden ortamında, **DWG'yi PDF'ye dönüştürme** ve özel açıklamalar ekleme sıkça karşılaşılan bir gereksinimdir. Müşteriler için yazdırılabilir çizimler oluşturmanız ya da dinamik notları doğrudan bir DWG'ye gömmeniz gerekse, Aspose.CAD işi basitleştirir. Bu öğreticide, C# kullanarak **DWG'yi PDF'ye dönüştürmeyi**, **bir metin varlığı eklemeyi** ve hatta **DWG metin yazı tipini değiştirmeyi** öğreneceksiniz.

## Hızlı Yanıtlar
- **DWG‑to‑PDF dönüşümü için en iyi kütüphane hangisidir?** Aspose.CAD for .NET  
- **Dönüştürürken özel metin ekleyebilir miyim?** Evet – bir `CadText` varlığı oluşturun ve kaydetmeden önce ekleyin.  
- **Üretim kullanımında lisansa ihtiyacım var mı?** Ticari bir lisans gereklidir; ücretsiz deneme mevcuttur.  
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Metin yazı tipini değiştirmek mümkün mü?** Evet, `CadText` özelliklerini, örneğin `StyleType` ve `TextHeight` gibi, ayarlayın.

## DWG'yi PDF'ye dönüştürmek nedir?

DWG dosyasını PDF'ye dönüştürmek, vektör tabanlı bir CAD çizimini geniş çapta paylaşılabilir, cihaz bağımsız bir belgeye dönüştürür. PDF, orijinal geometriyi ve katmanları korurken, açıklamalar, metin veya diğer meta verileri gömmenize olanak tanır. Aspose.CAD, rasterleştirme ve vektör renderlamasını otomatik olarak yönetir, bu yüzden sunucuda üçüncü taraf CAD yazılımına ihtiyacınız yoktur.

## Dönüştürmeden önce bir DWG'ye metin eklemek neden önemlidir?

Metni doğrudan DWG'ye gömmek, konumlandırma, stil ve katman ataması üzerinde tam kontrol sağlar. Dosya daha sonra PDF'ye dönüştürüldüğünde, metin tam olarak yerleştirdiğiniz yerde görünür, tasarım amacını korur ve PDF editöründe son işlem yapma ihtiyacını ortadan kaldırır.

## Önkoşullar

Başlamadan önce şunlara sahip olduğunuzdan emin olun:

- **Aspose.CAD Library** – indirmek için [download link](https://releases.aspose.com/cad/net/) adresini kullanın.  
- **Çalışan bir .NET ortamı** (Visual Studio 2022, .NET 6 veya uyumlu herhangi bir sürüm).  
- **Test dosyalarınız için bir klasör** – kılavuz boyunca `MyDir` olarak adlandıracağız.

Şimdi, süreci adım adım inceleyelim.

## Ad Alanlarını İçe Aktarın

Gerekli `using` ifadelerini ekleyin, böylece Aspose.CAD sınıflarına erişebilirsiniz.

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
using Aspose.CAD.ImageOptions;
```

## Adım 1: DWG Dosyasını Yükleyin

Kaynak DWG dosyanızı bir `Image` nesnesine yükleyin. Bu nesne, temel CAD varlıklarına erişim sağlar.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Adım 2: CadText Nesnesi Oluşturun (Metin Varlığını Ekle)

`CadText` sınıfı, bir DWG'deki tek satır metni temsil eder. Burada stilini, değerini, rengini, katmanını ve konumunu ayarlarız. **DWG metin yazı tipini değiştirmek** için `StyleType` veya `TextHeight` değerlerini ayarlayın.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Adım 3: Metin Varlığını Model Alanına Ekleyin

DWG model alanı, çoğu çizim varlığını tutar. `CadText` nesnemizi `*Model_Space` bloğuna ekleyerek, metin çizimin bir parçası haline gelir.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Adım 4: PDF Seçeneklerini Yapılandırın (DWG'den PDF Oluştur)

DWG'nin PDF'ye nasıl renderlanacağını kontrol eden rasterleştirme seçeneklerini ayarlayın. Sayfa boyutunu, çizim tipini ve düzeni ayarlayabilirsiniz.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Adım 5: Değiştirilmiş DWG'yi PDF Olarak Kaydedin

Son olarak, değiştirilmiş çizimi dışa aktarın. Oluşan PDF, yeni eklenen metni içerir.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Pro ipucu:** Daha yüksek çözünürlüklü bir PDF'ye ihtiyacınız varsa, `PageHeight` ve `PageWidth` değerlerini orantılı olarak artırın.

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| Metin PDF'de görünmüyor | Yanlış katman veya renk kimliği | `LayerName`'in mevcut olduğundan ve `ColorId`'nin görünür bir renge (ör. beyaz için 7) ayarlandığından emin olun. |
| Metin yanlış konumda | Yanlış hizalama koordinatları | Çizimin birimlerine göre `FirstAlignment.X/Y` değerlerini doğrulayın. |
| PDF boş | Rasterleştirme seçenekleri ayarlanmamış | `DrawType`'ı `UseObjectColor` veya `UseObjectLineWeight` olarak ayarlayın. |

## Sıkça Sorulan Sorular (Mevcut)

### Q1: Aspose.CAD tüm DWG dosya sürümleriyle uyumlu mu?
A1: Aspose.CAD, çeşitli DWG dosya sürümlerini geniş bir yelpazede destekler ve farklı CAD yazılımlarıyla uyumluluğu sağlar.

### Q2: Aspose.CAD kullanarak tek bir DWG dosyasına birden fazla metin varlığı ekleyebilir miyim?
A2: Evet, öğreticide açıklanan adımları tekrarlayarak bir DWG dosyasına birden fazla metin varlığı ekleyebilirsiniz.

### Q3: Aspose.CAD'de metin yazı tipini ve stilini nasıl değiştirebilirim?
A3: Metin yazı tipini ve stilini değiştirmek için, `CadText` nesnesinin özelliklerini DWG dosyasına eklemeden önce ayarlayın.

### Q4: Aspose.CAD'i ticari bir projede kullanırken lisans konuları var mı?
A5: Evet, Aspose.CAD lisans koşullarına uyduğunuzdan emin olun. Ayrıntılar için [Aspose.CAD Purchase](https://purchase.aspose.com/buy) adresine bakın.

### Q5: Aspose.CAD ile ilgili sorular için nereden yardım alabilir veya tartışabilirim?
A5: Toplulukla bağlantı kurmak ve destek almak için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

## Ek SSS

**S: Metin eklemeden DWG'den PDF nasıl oluştururum?**  
C: `CadText` oluşturma adımını atlayın ve `image.Save(...)` çağırmadan önce doğrudan `PdfOptions` yapılandırın.

**S: Metin rengini programlı olarak değiştirebilir miyim?**  
C: Evet, `cadText.ColorId`'yi belirli bir ACI renk numarasına (ör. kırmızı için 1) ayarlayın.

**S: Çok satırlı metin eklemek mümkün mü?**  
C: Çok satırlı metin blokları için `CadMText` kullanın; yaklaşım `CadText` ile benzer.

**S: Aspose.CAD birden fazla DWG dosyasının toplu dönüşümünü destekliyor mu?**  
C: Kesinlikle – bir DWG dosyaları dizini üzerinden döngü kurarak aynı adımları uygulayın ve her birini PDF olarak kaydedin.

## Sonuç

Artık C# ve Aspose.CAD kullanarak **DWG'yi PDF'ye dönüştürmek**, **özel metin eklemek** ve **metin görünümünü özelleştirmek** için eksiksiz, üretim‑hazır bir iş akışına sahipsiniz. Bu teknik, otomatik çizim üretimi, raporlama hatları veya CAD dosyalarını anında zenginleştirmeniz gereken herhangi bir senaryo için idealdir.

---

**Son Güncelleme:** 2026-04-06  
**Test Edilen Versiyon:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}