---
title: Aspose.CAD for .NET'te Düzenleri Raster Görüntüye Dönüştürme
linktitle: Düzenleri Raster Görüntüye Dönüştür
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET'i kullanarak CAD düzenlerini zahmetsizce raster görüntülere dönüştürün. Güçlü CAD manipülasyon yetenekleriyle gelişiminizi geliştirin.
type: docs
weight: 12
url: /tr/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---
## giriiş

.NET uygulamalarınızda düzenleri zahmetsizce raster görüntülere dönüştürmeyi mi istiyorsunuz? Başka yerde arama! Bu adım adım kılavuz, Bilgisayar Destekli Tasarım (CAD) görevlerini basitleştiren güçlü bir kütüphane olan Aspose.CAD for .NET'i kullanarak süreç boyunca size yol gösterecektir.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

- Aspose.CAD for .NET Library: Kütüphaneyi şuradan indirip yükleyin:[Aspose.CAD for .NET indirme sayfası](https://releases.aspose.com/cad/net/).

- Geliştirme Ortamı: Makinenizde çalışan bir .NET geliştirme ortamının kurulu olduğundan emin olun.

- Dönüştürülecek Belge: Raster görüntülere dönüştürmek istediğiniz düzenleri içeren bir CAD belgesi hazırlayın.

- Belge Dizininiz: Koddaki "Belge Dizininiz" yer tutucusunu belge dizininizin yolu ile değiştirin.

## Ad Alanlarını İçe Aktar

İlk olarak Aspose.CAD işlevlerini kodunuzda erişilebilir hale getirmek için gerekli ad alanlarını içe aktaralım.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Adım 1: CAD Belgesini Yükleyin

Aspose.CAD kütüphanesini kullanarak CAD belgesini yükleyerek başlayın.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //Daha sonraki adımlara ilişkin kodunuz buraya gelecek
}
```

## Adım 2: Rasterleştirme Seçeneklerini Yapılandırın

 Bir örneğini oluşturun`CadRasterizationOptions` sayfa genişliğini ve yüksekliğini ayarlamak ve dönüştürmek istediğiniz düzenleri belirtmek için.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Adım 3: Ortaya Çıkan Görüntü için TiffOptions'ı Ayarlayın

 Bir örneğini oluşturun`TiffOptions`Ortaya çıkan görüntünün formatını tanımlamak için.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Adım 4: Ortaya Çıkan Görüntüyü Kaydedin

Çıkış yolunu belirtin ve dönüştürülen görüntüyü kaydedin.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Çözüm

Tebrikler! Aspose.CAD for .NET'i kullanarak CAD düzenlerini başarıyla taramalı görüntü formatına dönüştürdünüz. Olasılıklar çok geniştir ve bu kılavuz, CAD ile ilgili çalışmalarınız için bir başlangıç noktası görevi görür.

## SSS'ler

### S1: Aspose.CAD tüm CAD formatlarıyla uyumlu mudur?

 Cevap1: Aspose.CAD, DWG, DXF, DWF, STL ve daha fazlasını içeren çok çeşitli CAD formatlarını destekler. Kontrol edin[dokümantasyon](https://reference.aspose.com/cad/net/) kapsamlı bir liste için.

### S2: Aspose.CAD için nasıl geçici lisans alabilirim?

 A2: Ziyaret edin[geçici lisans sayfası](https://purchase.aspose.com/temporary-license/) Test ve değerlendirme amacıyla geçici bir lisans almak.

### S3: Aspose.CAD desteğini nerede bulabilirim?

 Cevap3: Forumlar yardım almak için harika bir yerdir. Ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) toplulukla bağlantı kurmak ve yardım almak için.

### S4: Aspose.CAD'i ücretsiz deneyebilir miyim?

 Cevap4: Kesinlikle! Tutun[ücretsiz deneme](https://releases.aspose.com/) Aspose.CAD'in özelliklerini ve yeteneklerini keşfetmek için.

### S5: Aspose.CAD lisansını nereden satın alabilirim?

 A5: Şuraya gidin:[satın alma sayfası](https://purchase.aspose.com/buy) bir lisans satın almak ve Aspose.CAD'in tüm potansiyelini açığa çıkarmak için.