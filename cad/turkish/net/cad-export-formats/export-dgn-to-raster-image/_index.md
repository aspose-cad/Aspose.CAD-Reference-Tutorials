---
date: 2026-03-24
description: Aspose.CAD for .NET kullanarak dgn'yi png'ye dönüştürmeyi ve cad'i jpeg
  olarak kaydetmeyi öğrenin – CAD'den görüntüye dönüşüm için hızlı bir rehber.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET'te DGN'yi PNG'ye Nasıl Dönüştürülür
url: /tr/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN'yi PNG'ye Dönüştürme Aspose.CAD for .NET'te

Modern .NET geliştirmede, **convert dgn to png** web üzerinde CAD çizimlerini görüntülemek veya raporlara gömmek istediğinizde yaygın bir gereksinimdir. Aspose.CAD for .NET bu dönüşümü basitleştirir, bir DGN dosyasını sadece birkaç kod satırıyla yüksek kaliteli bir raster görüntüsüne dönüştürmenizi sağlar. Bu rehberde projeyi kurmaktan son PNG (veya JPEG) dosyasını kaydetmeye kadar tüm süreci adım adım inceleyeceğiz.

## Hızlı Yanıtlar
- **Can I convert DGN to PNG with Aspose.CAD?** Evet – sadece rasterleştirme seçeneklerini yapılandırın ve PNG veya JPEG çıktısını seçin.  
- **Do I need a license for production use?** Üretim ortamı için geçerli bir Aspose.CAD lisansı gereklidir, deneme sürümü dışındaki dağıtımlar için.  
- **Which .NET versions are supported?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **What image formats are available?** PNG, JPEG, BMP, GIF, TIFF ve daha fazlası.  
- **Is exception handling necessary?** Kesinlikle – dosya erişim sorunlarını ele almak için dönüşümü try/catch bloğuna alın.

## “convert dgn to png” nedir?
Bir DGN (MicroStation) dosyasını PNG'ye dönüştürmek, vektörel CAD verilerini piksel tabanlı bir görüntüye rasterleştirmek anlamına gelir. Bu, önizleme oluşturma, çizimleri HTML e-postalarına gömme veya belge yönetim sistemleri için küçük resimler (thumbnail) oluşturma gibi durumlarda faydalıdır.

## CAD'den görüntüye dönüşümde neden Aspose.CAD kullanmalı?
- **No external dependencies** – tamamen yönetilen kodda çalışır.  
- **High fidelity** – çizgi kalınlıklarını, katmanları ve renkleri korur.  
- **Flexible output** – tek bir seçeneği değiştirerek PNG, JPEG, BMP vb. arasında geçiş yapabilirsiniz.  
- **Performance‑optimized** – rasterleştirme büyük çizimler için bile hızlıdır.

## Önkoşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

- Projenizde **Aspose.CAD for .NET** yüklü olduğundan emin olun. [website](https://reference.aspose.com/cad/net/) adresinden indirebilirsiniz.  
- Bilinen bir dizine yerleştirilmiş örnek bir DGN dosyası (ör. `Nikon_D90_Camera.dgn`).

## Ad Alanlarını (Namespaces) İçe Aktarın

Aspose.CAD sınıflarına erişebilmek için gerekli `using` ifadelerini ekleyerek başlayın.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Adım 1: DGN Dosyasını Yükleyin

Kaynak DGN dosyasını bir `CadImage` nesnesine yükleyin. Bu nesne, bellek içindeki CAD çizimini temsil eder ve rasterleştirme için kaynak olacaktır.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Adım 2: Rasterleştirme Seçeneklerini Tanımlayın

CAD çiziminin nasıl rasterleştirileceğini yapılandırın. Burada görüntü boyutunu, ölçeklemeyi ve arka plan rengini kontrol edebilirsiniz.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Adım 3: Çıktı Formatını Seçin (PNG veya JPEG)

Rehber PNG üzerine odaklansa da **save cad as jpeg** isteyebilirsiniz. Uygun görüntü seçenekleri nesnesini oluşturun ve rasterleştirme ayarlarını ekleyin.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** PNG dosyası oluşturmak için `new JpegOptions()` ifadesini `new PngOptions()` ile değiştirin.

## Adım 4: Raster Görüntüyü Kaydedin

Son olarak, yapılandırdığınız dosya adı ve seçenek nesnesini sağlayarak `CadImage` örneği üzerinde `Save` metodunu çağırın.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

`PngOptions`'a geçiş yaptıysanız, dosya `ExportDGNToRasterImage_out.png` olarak kaydedilecektir.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Neden | Çözüm |
|-------|-------|-----|
| **Boş çıktı görüntüsü** | `NoScaling` hatalı ayarlandığında veya düzen seçilmediğinde | `AutomaticLayoutsScaling = true` olarak ayarlayın veya istenen düzeni belirtin. |
| **Büyük dosyalar için bellek yetersizliği** | Akış (streaming) kullanılmadan büyük DGN dosyasının yüklenmesi | `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })` kullanın. |
| **Desteklenmeyen DGN sürümü** | Eski MicroStation sürümleri | Eski formatları destekleyen en son Aspose.CAD sürümüne sahip olduğunuzdan emin olun. |

## Sıkça Sorulan Sorular

**Q: JPEG dışındaki formatlara DGN dosyalarını dışa aktarabilir miyim?**  
A: Evet, Aspose.CAD for .NET PNG, BMP, GIF, TIFF ve daha fazlasını destekler – sadece seçenek sınıfını değiştirin (ör. `new PngOptions()`).

**Q: Dönüşüm sırasında istisnaları nasıl ele almalı?**  
A: Dönüşüm kodunu bir `try/catch` bloğuna alın ve ayrıntılı hata bilgileri için `Aspose.CAD.CadException` kaydedin.

**Q: Aspose.CAD for .NET için bir deneme sürümü mevcut mu?**  
A: Evet, ürünü ücretsiz deneme ile inceleyebilirsiniz. Daha fazla bilgi için [burayı](https://releases.aspose.com/) ziyaret edin.

**Q: Aspose.CAD for .NET ile ilgili yardım almak veya sorunları tartışmak için nereye başvurabilirim?**  
A: Topluluk desteği ve tartışmalar için [Aspose.CAD forumuna](https://forum.aspose.com/c/cad/19) göz atın.

**Q: Aspose.CAD for .NET için geçici bir lisans nasıl alabilirim?**  
A: Geliştirme ihtiyaçlarınız için geçici lisans edinmek üzere [bu linki](https://purchase.aspose.com/temporary-license/) ziyaret edin.

## Sonuç

Artık Aspose.CAD for .NET kullanarak **convert dgn to png** (veya JPEG) nasıl yapılacağını öğrendiniz. Rasterleştirme seçeneklerini ayarlayarak ve görüntü‑seçenekleri sınıfını değiştirerek çıktıyı herhangi bir proje gereksinimine uyacak şekilde özelleştirebilirsiniz. Uygulamanız için mükemmel raster görüntüyü elde etmek amacıyla farklı sayfa boyutları, DPI ayarları ve dosya formatlarıyla denemeler yapmaktan çekinmeyin.

---

**Son Güncelleme:** 2026-03-24  
**Test Edilen Versiyon:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}