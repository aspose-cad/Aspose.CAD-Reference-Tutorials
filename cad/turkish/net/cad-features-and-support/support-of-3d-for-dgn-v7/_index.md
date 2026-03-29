---
date: 2026-03-29
description: Aspose.CAD for .NET kullanarak CAD rasterleştirme seçeneklerini nasıl
  yapılandıracağınızı ve DGN'yi 3D desteğiyle PDF'ye nasıl dışa aktaracağınızı öğrenin.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DGN V7 3D için CAD Rasterleştirme Seçeneklerini Yapılandır
url: /tr/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD Rasterizasyon Seçeneklerini DGN V7 3D için Yapılandırma

## Giriş

Bu kapsamlı öğreticide, Aspose.CAD for .NET kullanarak 3‑B DGN V7 dosyasını PDF'ye dışa aktarmak için **CAD rasterizasyon seçeneklerini nasıl yapılandıracağınızı** öğreneceksiniz. Bir CAD görüntüleyici, raporlama aracı veya otomatik dönüşüm hattı oluşturuyor olsanız da, bu ayarları ustalaşmak sayfa boyutu, düzen ölçeklendirme, arka plan renkleri ve render etmek istediğiniz belirli görünümler üzerinde kesin kontrol sağlar. Süreci adım adım inceleyelim.

## Hızlı Yanıtlar
- **“configure CAD rasterization options” ne anlama geliyor?**  
  Bu, bir CAD dosyasını raster formatına (ör. PDF) dönüştürmeden önce sayfa boyutları, ölçekleme, arka plan rengi ve düzen seçimi gibi özellikleri ayarlamayı ifade eder.
- **3‑D desteğiyle DGN'yi PDF'ye nasıl dışa aktarılır?**  
  DGN'yi `DgnImage` ile yükleyin, `PdfOptions` + `CadRasterizationOptions` tanımlayın ve ardından `Save` metodunu çağırın.
- **Üretim kullanımında lisansa ihtiyacım var mı?**  
  Evet – dağıtım için ticari bir lisans gereklidir; ücretsiz deneme sürümü mevcuttur.
- **Hangi .NET sürümleri destekleniyor?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Dışa aktarılacak belirli görünümleri seçebilir miyim?**  
  Kesinlikle – rasterizasyon seçeneklerinde `Layouts` dizisini ayarlayın.

## “configure CAD rasterization options” nedir?

CAD rasterizasyon seçeneklerini yapılandırmak, bir CAD çiziminin nasıl rasterleştirileceğini (vektörden bitmap'e veya PDF'e dönüştürülmesini) özelleştirmek anlamına gelir. Bu ayarları değiştirerek ortaya çıkan belgenin görsel çıktısını, performansını ve dosya boyutunu kontrol edersiniz.

## 3‑D DGN V7 dışa aktarımı için Aspose.CAD neden kullanılmalı?

- **Full .NET integration** – COM veya yerel DLL'lere gerek yok.  
- **Supports 3‑D geometry** – PDF'ye render ederken derinlik bilgisini korur.  
- **Fine‑grained control** – tam düzenleri, ölçeklemeyi ve arka plan renklerini seçin.  
- **Cross‑platform** – .NET Core ile Windows, Linux ve macOS'ta çalışır.

## Ön Koşullar

Başlamadan önce şunların olduğundan emin olun:

- **Aspose.CAD for .NET** – [buradan](https://releases.aspose.com/cad/net/) indirin.  
- **Visual Studio** veya uyumlu bir .NET IDE.  
- **Bir örnek DGN dosyası** – bu kılavuz için `Nikon_D90_Camera.dgn` dosyasını kullanacağız (Aspose örnek paketinde dahil).

Her şey hazır olduğuna göre, koda dalalım.

## Ad Alanlarını İçe Aktarma

.NET projenizde, gerekli ad alanlarını içe aktarın:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Adım 1: Belge Dizinini Ayarlama

Kaynak DGN dosyanızın ve çıktı dosyalarınızın bulunacağı klasöre işaret eden bir değişken oluşturun.

```csharp
string MyDir = "Your Document Directory";
```

## Adım 2: DGN Dosyasını Yükleme

`DgnImage` olarak DGN dosyasını yükleyin. Bu nesne, CAD verilerine ve rasterizasyon işlem hattına erişim sağlar.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Adım 3: PDF Dışa Aktarma Seçeneklerini Yapılandırma (CAD Rasterizasyon Seçeneklerini Yapılandırma)

Burada **CAD rasterizasyon seçeneklerini** yapılandırıyoruz; bu seçenekler 3‑D modelin PDF'ye nasıl render edileceğini belirler. Sayfa boyutunu ayarlayabilir, otomatik düzen ölçeklendirmeyi etkinleştirebilir, bir arka plan rengi belirleyebilir ve dışa aktarmak istediğiniz tam düzenleri (görünümleri) seçebilirsiniz.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Adım 4: Raster Görüntüyü Kaydetme

Son olarak, az önce yapılandırdığınız seçenekleri kullanarak DGN'yi bir PDF dosyasına dışa aktarın.

```csharp
dgnImage.Save(outFile, options);
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **Boş PDF çıktısı** | `Layouts` dizisinin DGN dosyasında bulunan doğru görünüm tanımlayıcılarını içerdiğini doğrulayın. |
| **Yanlış renkler** | `BackgroundColor`'ın istenen değere ayarlandığından emin olun; açık bir arka plan için `Color.White` kullanın. |
| **Büyük dosyalarda performans darboğazı** | `AutomaticLayoutsScaling`'i etkinleştirin ve daha düşük bir raster çözünürlüğü için `PageWidth/PageHeight` değerlerini azaltmayı düşünün. |
| **Lisans istisnası** | Deneme filigranlarından kaçınmak için resmi bir Aspose.CAD lisansını görüntüyü yüklemeden önce kurun. |

## Sıkça Sorulan Sorular

**Q: Aspose.CAD for .NET'i diğer CAD dosya formatlarıyla kullanabilir miyim?**  
A: Evet, Aspose.CAD DWG, DXF, DWF, DGN ve daha birçok formatı destekler.

**Q: Aspose.CAD ile çalışırken istisnaları nasıl ele alabilirim?**  
A: Kodunuzu bir `try‑catch` bloğuna sarın ve ayrıntılı hata bilgileri için `Aspose.CAD.CADException`'ı inceleyin.

**Q: Aspose.CAD ticari projeler için uygun mu?**  
A: Kesinlikle. Bir lisans satın alabilirsiniz [buradan](https://purchase.aspose.com/buy).

**Q: Satın almadan önce Aspose.CAD for .NET'i deneyebilir miyim?**  
A: Evet, ücretsiz bir deneme sürümü mevcuttur [buradan](https://releases.aspose.com/).

**Q: Aspose.CAD için topluluk desteğini nerede bulabilirim?**  
A: Tartışma forumuna katılın [buradan](https://forum.aspose.com/c/cad/19).

**Son Güncelleme:** 2026-03-29  
**Test Edilen Versiyon:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}