---
title: Aspose.CAD for .NET'te DGN V7 desteği
linktitle: DGN V7 desteği
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET'in DGN V7'ye yönelik kusursuz desteğini keşfedin. Adım adım rehberlikle DGN dosyalarını zahmetsizce taramalı görüntülere dönüştürün.
type: docs
weight: 19
url: /tr/net/cad-features-and-support/support-for-dgn-v7/
---
## giriiş

.NET geliştirme alanında Aspose.CAD, Bilgisayar Destekli Tasarım (CAD) dosyalarını işlemek için güçlü bir kütüphane olarak öne çıkıyor. Bu eğitimde Aspose.CAD for .NET'in belirli bir özelliği olan DGN V7 dosyaları desteği ele alınmaktadır. Tasarım'ın kısaltması olan DGN, CAD alanında yaygın olarak kullanılan bir dosya formatıdır. Aspose.CAD, DGN V7 dosyalarıyla çalışma sürecini basitleştirerek geliştiricilere kusursuz bir deneyim sunar.

## Önkoşullar

Uygulamaya geçmeden önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.CAD for .NET: Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. adresinden indirebilirsiniz.[İnternet sitesi](https://releases.aspose.com/cad/net/).

- Geliştirme Ortamı: Visual Studio veya tercih edilen herhangi bir IDE dahil, çalışan bir .NET geliştirme ortamı kurun.

Artık önkoşulları sıraladığımıza göre, Aspose.CAD for .NET'te DGN V7 desteğinden nasıl yararlanılacağını inceleyelim.

## Ad Alanlarını İçe Aktar

Aspose.CAD'in işlevselliğine erişmek için gerekli ad alanlarını içe aktararak başlayın:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Adım 1: DGN Dosyasını Yükleyin

 Mevcut bir DGN dosyasını bir dosya olarak yükleyerek başlayın.`CadImage` Yer değiştirmek`"Your Document Directory"` Ve`"Nikon_D90_Camera.dgn"` uygun dizin yolu ve dosya adı ile.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Daha sonraki adımlar için kod buraya gelecek...
}
```

## Adım 2: Rasterleştirme Seçeneklerini Yapılandırın

 Oluşturmak`CadRasterizationOptions` Rasterleştirmeyle ilgili çeşitli özellikleri tanımlamak ve ayarlamak için nesne.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Adım 3: Vektör Rasterleştirme Seçeneklerini Ayarlayın

 Oluşturmak`JpegOptions` DGN dosyasını JPEG'e dönüştürmeyi planladığımız için nesneyi kullanacağız. Daha önce oluşturulanları atayın`CadRasterizationOptions` buna itiraz edin.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Adım 4: Rasterleştirilmiş Görüntüyü Kaydetme

 Ara`Save` yöntemi`CadImage` DGN dosyasını bir raster görüntüye, bu durumda bir JPEG'e aktarmak için sınıf nesnesini kullanın.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Bu adımlar tamamlandıktan sonra DGN dosyası başarılı bir şekilde taramalı görüntüye aktarılır.

## Çözüm

Bu eğitimde Aspose.CAD for .NET'te DGN V7'nin kusursuz desteğini araştırdık. Geliştiriciler, adım adım kılavuzu izleyerek DGN dosyalarını zahmetsizce raster görüntülere dönüştürebilir ve .NET uygulamalarının yeteneklerini genişletebilirler.

## SSS'ler

### S1: Aspose.CAD en son DGN V7 spesifikasyonlarıyla uyumlu mu?

Cevap1: Evet, Aspose.CAD, DGN V7 dosyalarını sorunsuz bir şekilde işleyecek ve en yeni spesifikasyonlarla uyumluluğu sağlayacak şekilde tasarlanmıştır.

### S2: DGN dosya dönüşümü için rasterleştirme seçeneklerini özelleştirebilir miyim?

 A2: Kesinlikle. Eğitimde nasıl oluşturulacağı ve yapılandırılacağı gösterilmektedir`CadRasterizationOptions` dönüşüm sürecini uyarlamak için.

### S3: JPEG dışında desteklenen başka çıktı formatları var mı?

Cevap3: Evet, Aspose.CAD çeşitli çıktı formatlarını destekler. Kapsamlı bir liste için belgeleri inceleyebilirsiniz.

### S4: Aspose.CAD ile ilgili sorgular için nasıl destek alabilirim?

 A4: Ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği ve tartışmalar için.

### S5: Aspose.CAD for .NET'in ücretsiz deneme sürümü mevcut mu?

 C5: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).