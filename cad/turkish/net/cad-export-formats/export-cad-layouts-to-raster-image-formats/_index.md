---
date: 2026-03-21
description: Aspose.CAD for .NET kullanarak dxf'i png ve diğer raster formatlarına
  nasıl dönüştüreceğinizi öğrenin. Sorunsuz CAD katman ihracı için adım adım rehberimizi
  izleyin.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET ile DXF'yi PNG'ye Dönüştür
url: /tr/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET'te CAD Düzenlerini Raster Görüntü Biçimlerine Dışa Aktarma

## Giriş

Aspose.CAD for .NET kullanarak **convert dxf to png** ve diğer raster görüntü biçimlerini verimli bir şekilde dönüştürmek mi istiyorsunuz? Bu adım‑adım kılavuz, süreci size anlatacak, ayrıntılı talimatlar ve kod parçacıkları sağlayarak görevi sorunsuz hâle getirecek. İster deneyimli bir geliştirici olun, ister Aspose.CAD'e yeni başlayan biri, bu öğretici her seviyedeki uzmanlığa hitap eder.

### Hızlı Yanıtlar
- **Dönüşümü hangi kütüphane yönetir?** Aspose.CAD for .NET  
- **Kutudan çıkar çıkmaz desteklenen birincil format?** JPEG, PNG, BMP ve TIFF raster görüntüler  
- **Belirli CAD katmanlarını dışa aktarabilir miyim?** Evet – bireysel katmanları hedeflemek için `CadRasterizationOptions.Layers` kullanın  
- **Üretim için lisansa ihtiyacım var mı?** Deneme dışı kullanım için geçerli bir Aspose.CAD lisansı gereklidir  
- **Desteklenen .NET sürümleri?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## **convert dxf to png** nedir?

DXF (Drawing Exchange Format) dosyasını PNG'ye dönüştürmek, vektör tabanlı CAD verilerini piksel tabanlı bir görüntüye rasterleştirmek anlamına gelir. Bu, CAD çizimlerini web sayfalarına, raporlara veya yalnızca raster grafik destekleyen herhangi bir ortama yerleştirmeniz gerektiğinde faydalıdır.

## CAD katmanlarını ayrı ayrı dışa aktarmak neden önemlidir?

CAD katmanlarını ayrı ayrı dışa aktarmak, görsel çıktının ayrıntılı kontrolünü sağlar, her görüntünün dosya boyutunu azaltır ve katmana özgü stil veya son işleme uygulamanıza olanak tanır. Bu, yalnızca belirli bir izleyici kitlesi için ilgili katmanların bir alt kümesinin gerekli olduğu büyük mühendislik çizimleri için özellikle kullanışlıdır.

## Önkoşullar

Öğreticiye başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Aspose.CAD for .NET Kütüphanesi** – [Aspose.CAD web sitesinden](https://releases.aspose.com/cad/net/) indirin.  
- **CAD Çizim Dosyası** – raster biçimlerine dönüştürmek istediğiniz bir DXF dosyası (ör. `conic_pyramid.dxf`).  

## Ad Alanlarını İçe Aktarma

.NET projenizde, Aspose.CAD işlevlerini kullanmak için gerekli ad alanlarını içe aktarın. Aşağıdaki ad alanlarını kodunuzun başına ekleyin:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## **convert dxf to png** nasıl yapılır – Adım Adım Kılavuz

### Adım 1: CAD Çizimini Yükle

İlk olarak, DXF dosyasını bir `Image` nesnesine yükleyin. Bu nesne, tüm CAD çizimini bellekte temsil eder.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### Adım 2: `CadRasterizationOptions` Oluşturun

Çıktı boyutları ve çözünürlük gibi rasterleştirme ayarlarını yapılandırın. Bu seçenekler, vektör verisinin nasıl rasterleştirileceğini kontrol eder.

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### Adım 3: Katmanları Belirt (CAD Katmanlarını Dışa Aktar)

Yalnızca belirli bir katmana ihtiyacınız varsa, adını burada listeleyin. Bu, **export cad layers**'ı ayrı ayrı göstermektedir.

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### Adım 4: Bir Görüntü Biçimi Seç – CAD'i PNG (veya JPEG) Olarak Kaydet

Görüntü biçimine özgü bir seçenek nesnesi oluşturun. **save cad as png** yapmak istediğinizde `JpegOptions` yerine `PngOptions` kullanın.

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** PNG dosyaları oluşturmak için `JpegOptions` yerine `new PngOptions()` örneği oluşturmanız yeterlidir.

### Adım 5: JPEG (veya PNG) Biçimine Dışa Aktar

Son olarak, rasterleştirilmiş görüntüyü diske kaydedin. Dosya uzantısı çıktı biçimini belirler.

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

`JpegOptions` yerine `PngOptions` kullandığınızda, aynı kod **convert dxf to png** yapacak ve bir `.png` dosyası üretecektir.

### Ek Adım: Tüm Katmanları Dönüştür

Çizimdeki her katman için **convert cad to raster** yapmanız gerekiyorsa, aşağıdaki yardımcı yöntemi çağırın. Bu yöntem tüm katmanları döner ve her birini ayrı bir görüntü olarak kaydeder.

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *Not:* `ConvertAllLayersToRasterImageFormats` uygulaması tam Aspose.CAD örnek paketinin bir parçasıdır ve katmanların toplu işlenmesini gösterir.

## Yaygın Sorunlar ve Çözümleme

| Belirti | Muhtemel Neden | Çözüm |
|---------|----------------|------|
| Boş veya beyaz görüntü | Rasterleştirme seçenekleri ayarlanmamış (ör. `PageWidth`/`PageHeight` = 0) | `PageWidth` ve `PageHeight` değerlerinin pozitif olduğundan emin olun |
| Katmanlar eksik | `Layers` dizisinde yanlış katman adı | CAD dosyasındaki tam katman adını (büyük/küçük harfe duyarlı) doğrulayın |
| Düşük kaliteli PNG | Varsayılan DPI düşük | Daha yüksek kalite için `rasterizationOptions.Resolution = 300;` ayarlayın |

## Sıkça Sorulan Sorular (Orijinal)

### S1: Başka görüntü biçimlerini dışa aktarabilir miyim?
C1: Evet, yapabilirsiniz. `JpegOptions` yerine istediğiniz formatın seçeneklerini, örneğin `PngOptions` veya `BmpOptions` kullanarak değiştirin.

### S2: Deneme sürümü mevcut mu?
C2: Evet, Aspose.CAD işlevselliğini deneme sürümünü [buradan](https://releases.aspose.com/) indirerek keşfedebilirsiniz.

### S3: Aspose.CAD için destek nasıl alabilirim?
C3: Topluluk desteği için Aspose.CAD [forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin veya özel destek için bir lisans satın almayı düşünün.

### S4: Geçici lisanslar mevcut mu?
C4: Evet, geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) edinebilirsiniz.

### S5: Belgeleri nerede bulabilirim?
C5: Ayrıntılı belgeler için [buraya](https://reference.aspose.com/cad/net/) bakın.

## Ek SSS

**S: Tüm katmanları tek bir komutla dışa aktarabilir miyim?**  
C: Evet, yukarıda gösterilen `ConvertAllLayersToRasterImageFormats` yöntemini kullanın.

**S: Aspose.CAD SVG gibi vektör biçimlerini destekliyor mu?**  
C: Öncelikle raster biçimlerine yöneliktir, ancak vektör verisini koruyan PDF'ye dışa aktarabilirsiniz.

**S: Dışa aktarılan PNG'nin arka plan rengini nasıl kontrol ederim?**  
C: Kaydetmeden önce `rasterizationOptions.BackgroundColor` değerini istediğiniz `Color` olarak ayarlayın.

**S: Tüm çizim yerine tek bir düzeni dışa aktarmak mümkün mü?**  
C: Evet, rasterleştirmek istediğiniz düzen adı(ları)nı belirlemek için `rasterizationOptions.Layouts` yapılandırın.

## Sonuç

Artık Aspose.CAD for .NET kullanarak **convert dxf to png**, **export cad layers** ve **save cad as png** ya da JPEG yapmayı öğrendiniz. `CadRasterizationOptions` ayarlarını değiştirerek ve görüntü‑biçim seçeneklerini değiştirerek dönüşümü ihtiyacınız olan hemen hemen her raster çıktısına uyarlayabilirsiniz. CAD‑to‑raster iş akışınızı genişletmek için Aspose.CAD API'deki diğer biçim seçeneklerini keşfedin.

---

**Son Güncelleme:** 2026-03-21  
**Test Edilen Versiyon:** Aspose.CAD for .NET 24.11 (yazım anındaki en yeni sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}