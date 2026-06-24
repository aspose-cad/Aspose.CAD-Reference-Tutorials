---
date: 2026-03-29
description: Bu adım adım rehberde, Aspose.CAD for .NET kullanarak CAD'den PDF oluşturmayı,
  tuval boyutunu ayarlamayı ve CAD'i PDF veya TIFF olarak dışa aktarmayı öğrenin.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'CAD''den PDF Oluşturma: Aspose.CAD for .NET''te Tuval Boyutunu ve Modunu Ayarlama'
url: /tr/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET'te Tuval Boyutu ve Modunu Ayarlama

## Giriş

Çıktı boyutlarını kontrol ederken **CAD'den PDF oluşturma** dosyalarına hazır mısınız? Bu öğreticide tuval boyutu ve modunu ayarlamayı, bir CAD dosyasını yüklemeyi ve Aspose.CAD for .NET ile PDF veya TIFF olarak dışa aktarmayı adım adım göstereceğiz. **DXF'yi PDF'ye dönüştürme**, yüksek çözünürlüklü çizimler oluşturma veya sadece rasterleştirme alanını ayarlama ihtiyacınız olsun, aşağıdaki adımlar size sağlam, üretime hazır bir çözüm sunacak.

## Hızlı Yanıtlar
- **“CAD'den PDF oluşturma” ne anlama gelir?** CAD çizimini (ör. DXF, DWG) vektör ve raster detaylarını koruyan bir PDF belgesine dönüştürmek.  
- **Hangi seçenek çıktı boyutunu kontrol eder?** `CadRasterizationOptions.PageWidth` ve `PageHeight` (tuval boyutu).  
- **TIFF olarak da dışa aktarabilir miyim?** Evet – aynı rasterleştirme ayarlarıyla `TiffOptions` kullanın.  
- **Üretim için lisansa ihtiyacım var mı?** Ticari bir lisans gereklidir; ücretsiz deneme sürümü mevcuttur.  
- **Desteklenen .NET sürümleri?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## “CAD'den PDF oluşturma” nedir?
CAD'den PDF oluşturmak, CAD çizimini sayfa‑odaklı bir formatta (PDF) işlemek anlamına gelir; bu sayede CAD yazılımına ihtiyaç duymadan görüntülenebilir, yazdırılabilir veya paylaşılabilir. Aspose.CAD, ağır işleri halleder ve size tuval boyutu, ölçekleme ve çıktı formatını tanımlama imkanı verir.

## CAD'den PDF oluştururken neden tuval boyutu ayarlamalısınız?
Tuval boyutunu ayarlamak, ortaya çıkan PDF veya TIFF'in çözünürlüğü ve boyutları üzerinde kesin kontrol sağlar. Bu özellikle şu durumlarda faydalıdır:
- Belirli kağıt boyutlarında baskı için çizimleri hazırlama.  
- Web önizlemesi için küçük resimler veya yüksek çözünürlüklü görüntüler oluşturma.  
- Birden fazla belge arasında tutarlı düzeni sağlama.

## Önkoşullar

- Aspose.CAD Kütüphanesi: Aspose.CAD kütüphanesini [Aspose.CAD web sitesinden](https://releases.aspose.com/cad/net/) indirip kurun.  
- Geliştirme Ortamı: Makinenizde bir .NET geliştirme ortamının kurulu olduğundan emin olun.  
- Örnek CAD Dosyası: Bu öğreticide bir örnek DXF dosyası kullanacağız. Bir tanesini [Aspose.CAD belgelerinde](https://reference.aspose.com/cad/net/) bulabilirsiniz.

## Ad Alanlarını İçe Aktarma

İlk olarak, CAD işleme için gerekli ad alanlarını içe aktarın:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Özel Tuval Boyutu ile CAD'den PDF Oluşturma

### Adım 1: CAD Dosyasını Yükle

İlk olarak **CAD dosyasını** (ör. bir DXF) bir `Image` nesnesine **yükleyerek** başlarız. Bu, CAD dosyasını belleğe **yüklediğiniz** noktadır.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Adım 2: CadRasterizationOptions Oluştur

`CadRasterizationOptions` bir örnek oluşturun ve tuval boyutunu tanımlayın. `PageWidth` ve `PageHeight` özellikleri, ihtiyacınız olan tam boyutları **tuval boyutu olarak ayarlamanıza** olanak tanır.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Adım 3: PdfOptions Oluştur (CAD'yi PDF'ye Dışa Aktar)

Rasterleştirme ayarlarını bir `PdfOptions` nesnesine bağlayın. Bu yapılandırma, tanımladığınız özel tuval ile **CAD'yi PDF'ye dışa aktarmanıza** olanak verir.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Adım 4: PDF'ye Dışa Aktar (DXF'yi PDF'ye Dönüştür)

Şimdi görüntüyü PDF olarak kaydedin. Bu adım, ayarladığımız seçenekleri kullanarak **CAD'den PDF oluşturur**.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Adım 5: TiffOptions Oluştur (CAD'yi TIFF'e Dışa Aktar)

Eğer ayrıca bir raster görüntüye ihtiyacınız varsa, `TiffOptions` yapılandırın. Aynı rasterleştirme seçenekleri yeniden kullanılır, böylece **CAD'yi TIFF'e dışa aktarma** tuval boyutuna saygı gösterir.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Adım 6: TIFF'e Dışa Aktar

Son olarak, çizimi bir TIFF dosyası olarak kaydedin.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Yaygın Sorunlar ve Çözümler

- **Tuval kırpılmış görünüyor** – Çizimin tuvalin içine sığacak şekilde ölçeklenmesi için `AutomaticLayoutsScaling` değerinin `true` ve `NoScaling` değerinin `false` olduğundan emin olun.  
- **Düşük çözünürlüklü PDF** – `PageWidth`/`PageHeight` değerlerini artırın veya `CadRasterizationOptions` üzerindeki `Resolution` ayarını yapın.  
- **Dosya bulunamadı hatası** – `MyDir`'in geçerli bir dizine işaret ettiğinden ve DXF dosya adının tam olarak eşleştiğinden emin olun.

## Sıkça Sorulan Sorular

### Q1: Aspose.CAD'i diğer .NET kütüphaneleriyle kullanabilir miyim?
A1: Evet, Aspose.CAD diğer .NET kütüphaneleriyle sorunsuz bir şekilde bütünleşir ve CAD manipülasyonu için gelişmiş yetenekler sunar.

### Q2: Aspose.CAD için ücretsiz deneme mevcut mu?
A2: Evet, Aspose.CAD'in özelliklerini ücretsiz bir deneme ile keşfedebilirsiniz. Başlamak için [burayı](https://releases.aspose.com/) ziyaret edin.

### Q3: Aspose.CAD için destek nasıl alabilirim?
A3: Destek ve tartışmalar için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

### Q4: Aspose.CAD için kapsamlı belgeleri nerede bulabilirim?
A4: Ayrıntılı bilgi ve örnekler için [Aspose.CAD belgelerine](https://reference.aspose.com/cad/net/) bakın.

### Q5: Aspose.CAD for .NET'i nasıl satın alabilirim?
A5: Aspose.CAD'i satın almak için [satın alma sayfasını](https://purchase.aspose.com/buy) ziyaret edin.

**S: Çok sayfalı bir CAD çizimini tek bir PDF'ye dışa aktarabilir miyim?**  
C: Evet. `CadRasterizationOptions` içinde `PageCount` ayarlayın, kütüphane sayfaları tek bir PDF'de birleştirir.

**S: Tuval boyutu vektör veri kalitesini etkiler mi?**  
C: Vektör verileri çözünürlükten bağımsız kalır; tuval boyutu yalnızca rasterleştirilmiş öğeleri ve görüntü çözünürlüğünü etkiler.

**Son Güncelleme:** 2026-03-29  
**Test Edilen Versiyon:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}