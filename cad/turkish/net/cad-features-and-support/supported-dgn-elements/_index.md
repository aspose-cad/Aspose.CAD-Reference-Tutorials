---
date: 2026-03-29
description: Aspose.CAD for .NET kullanarak DGN'yi PNG'ye nasıl dönüştüreceğinizi
  öğrenin. Bu kılavuz ayrıca CAD dosya formatı desteğini ve desteklenen DGN öğelerinin
  tam setini kapsar.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET ile DGN'yi PNG'ye Dönüştür
url: /tr/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN'yi PNG'ye Dönüştürme Aspose.CAD for .NET

## Giriş

.NET geliştiricisi olarak **DGN'yi PNG'ye dönüştürmek** istiyor musunuz? Aspose.CAD for .NET, DGN dosyalarını verimli bir şekilde işlemek için sağlam bir çözüm sunar. Bu öğreticide, desteklenen DGN öğelerini inceleyecek, Aspose.CAD for .NET ile çalışma sürecinde size rehberlik edecek ve bu öğeleri PNG görüntülerine nasıl dışa aktaracağınızı tam olarak göstereceğiz.

## Hızlı Yanıtlar
- **Aspose.CAD ne yapar?** CAD/BIM dosyalarını (DGN dahil) okur, değiştirir ve PNG gibi raster formatlarına dönüştürür.  
- **2D ve 3D DGN öğelerini dönüştürebilir miyim?** Evet – hem 2‑D hem de 3‑D varlıklar desteklenir.  
- **Hangi .NET sürümleri gereklidir?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Test için lisansa ihtiyacım var mı?** Ücretsiz bir deneme sürümü mevcuttur; üretim için lisans gereklidir.  
- **Kütüphaneyi nereden alabilirim?** Resmi Aspose sitesinden indirebilirsiniz (aşağıdaki bağlantı).

## “DGN'yi PNG'ye dönüştürmek” nedir?
DGN'yi PNG'ye dönüştürmek, vektör tabanlı DGN çizimini (2‑D veya 3‑D) raster görüntü formatına (PNG) dönüştürmek anlamına gelir. Bu, CAD çizimlerini web üzerinde görüntülemek, raporlara eklemek veya bir CAD görüntüleyiciye ihtiyaç duymadan küçük resimler oluşturmak istediğinizde faydalıdır.

## Neden CAD dosya formatı desteği için Aspose.CAD for .NET kullanmalısınız?
- **Tam CAD dosya formatı desteği** – DGN, DWG, DXF, DWF ve daha fazlası.  
- **Harici bağımlılık yok** – saf .NET kütüphanesi, yerel CAD kurulumları gerektirmez.  
- **Yüksek doğruluklu render** – çizgi kalınlıklarını, renkleri ve 3‑D geometrileri korur.  
- **Toplu işleme** – sunucu tarafı uygulamada birçok dosyayı kolayca döngüye alabilirsiniz.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- .NET programlama temeline sahip olmak.  
- Makinenizde Visual Studio yüklü olması.  
- Aspose.CAD for .NET kütüphanesini [buradan](https://releases.aspose.com/cad/net/) indirebilirsiniz.

## Namespace'leri İçe Aktarın

Projenizi başlatmak için gerekli namespace'leri .NET uygulamanıza içe aktarın. Bu adım, Aspose.CAD for .NET tarafından sağlanan işlevlere erişmenizi sağlar.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## DGN'yi PNG'ye Nasıl Dönüştürülür

Aşağıda, bir DGN dosyasını yükleme, öğelerini yineleme, hem 2‑D hem de 3‑D varlıkları işleme ve sonunda sonucu PNG raster görüntüsü olarak dışa aktarma adımlarını adım adım gösteren bir rehber bulunmaktadır.

### Adım 1: DGN Dosyasını Yükleyin

.NET uygulamanızda mevcut bir DGN dosyasını `DgnImage` olarak yükleyerek başlayın.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Adım 2: DGN Öğeleri Üzerinde Döngü Yapın

`foreach` döngüsü kullanarak DGN öğeleri üzerinde yineleme yapın. Aspose.CAD for .NET, üzerinde çalışabileceğiniz çeşitli DGN öğesi tipleri sunar.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Adım 3: Önceden Desteklenen 2‑D Varlıkları İşleyin

Bu varlıklar artık 3‑D render için de desteklenmektedir. Switch ifadesi, öğe tipine göre mantığı dallandırmanıza olanak tanır.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Adım 4: Desteklenen 3‑D Varlıkları İşleyin

Aspose.CAD, çeşitli 3‑D DGN varlıkları için tam destek ekler. Gerekli olduğunda bunları işlemek için switch ifadesini genişletin.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Adım 5: PNG Olarak Dışa Aktarın ve Kaydedin

Gerekli tüm manipülasyonları yaptıktan sonra, DGN çizimini PNG raster görüntüsü olarak dışa aktarın ve belirtilen dizine kaydedin.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Pro ipucu:** Çözünürlüğü, arka plan rengini ve diğer PNG‑özel ayarları kontrol etmek için `Image.Save` metodunu `new PngOptions()` ile kullanın.

## CAD Dosya Formatı Desteği Genel Bakış

Aspose.CAD for .NET sadece DGN ile sınırlı değildir. DWG, DXF, DWF ve birçok diğer CAD formatını da destekleyerek, geniş bir mühendislik çizimi yelpazesini tek bir API ile yönetmenizi sağlar. Bu, birden fazla standarda **CAD dosya formatı desteği** gerektiren projeler için idealdir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|--------|-----|
| **Görüntü boş görünüyor** | Sıfır DPI ile dışa aktarıldı | `PngOptions` içinde `ResolutionX` ve `ResolutionY` değerlerini belirtin. |
| **3‑D geometri eksik** | Switch içinde öğe tipi işlenmedi | Eksik `DgnElementType` durumunu ekleyin ve uygun şekilde render edin. |
| **Büyük dosyalarda bellek yetersizliği** | Dosyanın tamamını bir kerede yüklemek | Öğeleri toplu olarak işleyin veya mümkün olduğunda akış (streaming) kullanın. |

## Sıkça Sorulan Sorular

### S1: Aspose.CAD for .NET belgelerini nerede bulabilirim?
A1: Belgeleri [burada](https://reference.aspose.com/cad/net/) bulabilirsiniz.

### S2: Aspose.CAD for .NET'i nasıl indirebilirim?
A2: Kütüphaneyi [buradan](https://releases.aspose.com/cad/net/) indirebilirsiniz.

### S3: Aspose.CAD for .NET için ücretsiz deneme sürümü var mı?
A3: Evet, ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) erişebilirsiniz.

### S4: Aspose.CAD for .NET için geçici lisansları nereden alabilirim?
A4: Geçici lisanslar [buradan](https://purchase.aspose.com/temporary-license/) temin edilebilir.

### S5: Yardıma mı ihtiyacınız var ya da sorularınız mı var?
A5: Aspose.CAD for .NET topluluğu [destek forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

---

**Son Güncelleme:** 2026-03-29  
**Test Edilen Versiyon:** Aspose.CAD for .NET 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}