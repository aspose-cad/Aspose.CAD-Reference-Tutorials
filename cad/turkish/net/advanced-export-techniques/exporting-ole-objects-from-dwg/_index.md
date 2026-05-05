---
description: Aspose.CAD for .NET kullanarak DWG'yi PNG'ye dönüştürmeyi ve DWG dosyalarından
  OLE nesnelerini çıkarmayı öğrenin – hızlı, kod odaklı bir rehber.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG'yi PNG'ye Dönüştür & OLE Nesnelerini Dışa Aktar - Aspose.CAD Öğreticisi
url: /tr/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

 keep blank lines as original.

Let's craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG Dosyalarından OLE Nesnelerini Dışa Aktarma - Aspose.CAD Öğreticisi

## Giriş

Eğer gömülü OLE nesnelerini çıkarırken **convert DWG to PNG** yapmak istiyorsanız, doğru yerdesiniz. Aspose.CAD for .NET bu iki adımlı süreci basitleştirir, birkaç C# satırıyla çıkarma ve rasterleştirmeyi otomatikleştirmenizi sağlar. Önümüzdeki birkaç dakikada ortamınızı kurmaktan, her DWG'yi çıkarılan OLE verilerini içeren bir PNG olarak kaydetmeye kadar tüm iş akışını adım adım göstereceğiz.

## Hızlı Yanıtlar
- **Bu öğretici neyi kapsıyor?** Aspose.CAD for .NET kullanarak DWG'yi PNG'ye dönüştürme ve OLE nesnelerini çıkarma.  
- **Bir lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Birden fazla DWG dosyasını aynı anda işleyebilir miyim?** Evet – örnek, dosya adları dizisi üzerinden döngü yapar.  
- **Daha fazla örnek nerede bulunur?** Aşağıdaki resmi Aspose.CAD dokümantasyonu ve forum bağlantılarına bakın.

## **convert DWG to PNG** nedir?
Bir DWG (AutoCAD çizimi) dosyasını PNG görüntüsüne dönüştürmek, vektör verilerini rasterleştirir ve DWG'yi doğal olarak desteklemeyen web sayfaları, raporlar veya diğer uygulamalara görüntüleme ya da gömme işlemini kolaylaştırır. OLE nesneleri mevcut olduğunda, dönüşüm sırasında ayrı varlıklar olarak çıkarılıp kaydedilebilir.

## CAD dosyalarından OLE nesnelerini neden çıkaralım?
Birçok DWG çizimi, elektronik tablolar, grafikler veya diğer Office belgelerini OLE nesneleri olarak gömer. Bunları çıkarmak, orijinal veriyi yeniden kullanmanıza, raporlamayı otomatikleştirmenize veya gömülü bilgiyi kaybetmeden içeriği daha yeni formatlara taşımanıza olanak tanır.

## Önkoşullar

- Aspose.CAD for .NET Kütüphanesi: Kütüphanenin kurulu olduğundan emin olun. [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) adresinden indirebilirsiniz.
- Belge Dizini: DWG dosyalarınızın saklandığı bir dizin oluşturun. Sağlanan kod parçacığındaki `"Your Document Directory"` ifadesini gerçek yol ile değiştirin.

## Ad Alanlarını İçe Aktarma

.NET projenizde, gerekli ad alanlarını içe aktarın:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Adım Adım Kılavuz

### Adım 1: Belge Dizini Ayarlama

```csharp
string MyDir = "Your Document Directory";
```

`"Your Document Directory"` ifadesini DWG dosyalarınızın bulunduğu yol ile değiştirin.

### Adım 2: İşlemek İstediğiniz DWG Dosyalarını Listeleyin

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Adım 3: PNG Dönüştürme İçin Dışa Aktarma Seçeneklerini Yapılandırın

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

`CadRasterizationOptions` (ör. `PageWidth`, `PageHeight`, `BackgroundColor`) ayarlarını istediğiniz çıktı çözünürlüğüne göre düzenleyebilirsiniz.

### Adım 4: Her DWG Üzerinde Döngü Oluşturup Dönüştürmeyi Gerçekleştirin

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Bu döngü sırasında kütüphane, her çizime gömülü **OLE nesnelerini** otomatik olarak çıkarır ve oluşturulan PNG'ye ekler. Ham OLE akışlarına ihtiyacınız varsa, `cadImage.OleObjects` koleksiyonuna erişebilirsiniz – programlı olarak **how to extract ole** verilerini almanın kullanışlı bir yolu.

## Yaygın Sorunlar ve Sorun Giderme

- **Eksik düzen adı** – Belirttiğiniz düzenin (`"Layout1"` örnekte) kaynak DWG'de mevcut olduğundan emin olun; aksi takdirde rasterleştirici varsayılan model alanına geri döner.
- **Büyük dosyalar bellek baskısı oluşturur** – Dosyaları tek tek işleyin (gösterildiği gibi) ve `using` ile `CadImage` nesnelerini hemen serbest bırakın.
- **Beklenmeyen renkler** – Şeffaflık gerekiyorsa `rasterizationOptions.BackgroundColor` değerini çizimin arka planına uygun şekilde ayarlayın.

## Sıkça Sorulan Sorular

### S1: Aspose.CAD for .NET hem junior hem senior CAD dosyaları için uygun mu?
A1: Evet, Aspose.CAD for .NET çok yönlüdür ve junior ve senior varyantlar dahil olmak üzere geniş bir CAD dosyası yelpazesini işleyebilir.

### S2: Farklı düzenler için dışa aktarma seçeneklerini özelleştirebilir miyim?
A2: Kesinlikle! Öğreticide gösterildiği gibi, dışa aktarma seçeneklerini, düzenler dahil, özel ihtiyaçlarınıza göre uyarlayabilirsiniz.

### S3: Aspose.CAD for .NET için ayrıntılı dokümantasyonu nerede bulabilirim?
A3: Derinlemesine bilgi ve örnekler için [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/) adresini inceleyin.

### S4: Ücretsiz deneme sürümü var mı?
A4: Evet, Aspose.CAD for .NET'in yeteneklerini ücretsiz deneme sürümüyle deneyebilirsiniz. Başlamak için [this link](https://releases.aspose.com/) adresini ziyaret edin.

### S5: Destek alabilir ya da toplulukla nasıl iletişime geçebilirim?
A5: Destek ve topluluk etkileşimi için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

### S6: PNG'ye dönüştürmeden **extract OLE from CAD** dosyalarından nasıl OLE çıkarırım?
A6: DWG'yi yükledikten sonra `CadImage.OleObjects` koleksiyonunu kullanın; her `OleObject` üzerinden döngü yaparak ham verisini bir dosyaya kaydedebilirsiniz.

## Sonuç

Artık Aspose.CAD for .NET kullanarak **convert DWG to PNG** yaparken **OLE nesnelerini** sorunsuz bir şekilde nasıl çıkaracağınızı gördünüz. Bu yaklaşım zaman kazandırır, manuel kopyala‑yapıştır adımlarını ortadan kaldırır ve otomatik iş akışlarına temiz bir şekilde entegre olur. Diğer raster formatları (JPEG, BMP) ile denemeler yapabilir veya Aspose'un sunduğu zengin CAD manipülasyon özelliklerini keşfedebilirsiniz.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}