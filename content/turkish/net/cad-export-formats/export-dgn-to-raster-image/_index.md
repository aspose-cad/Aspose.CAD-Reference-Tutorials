---
title: Aspose.CAD for .NET'te DGN'yi Raster Görüntüye Aktar
linktitle: DGN'yi Raster Görüntüye Aktar
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET'i kullanarak DGN'yi taramalı görüntülere zahmetsizce dönüştürün. Adım adım kılavuzu keşfedin ve CAD dosya işlemede .NET'in gücünü açığa çıkarın.
type: docs
weight: 13
url: /tr/net/cad-export-formats/export-dgn-to-raster-image/
---
## giriiş

.NET geliştirmenin dinamik alanında Aspose.CAD, Bilgisayar Destekli Tasarım (CAD) dosyalarını işlemek için güçlü bir araç olarak ortaya çıkıyor. Bu eğitimde Aspose.CAD for .NET kullanarak DGN dosyalarını raster görüntülere aktarma süreci ayrıntılı olarak ele alınmaktadır. DGN dosyalarınızı görsel olarak ilgi çekici raster görüntülere sorunsuz bir şekilde dönüştürme konusunda istekliyseniz, doğru yerdesiniz.

## Önkoşullar

Bu yolculuğa çıkmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.CAD for .NET: .NET projenizde Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. Kütüphaneyi ve ilgili belgeleri şu adreste bulabilirsiniz:[İnternet sitesi](https://reference.aspose.com/cad/net/).

- Örnek DGN Dosyası: Dönüştürme için hazır bir DGN dosyası bulundurun. Örneğimizde "Nikon_D90_Camera.dgn" kullanacağız.

Şimdi adım adım kılavuza geçelim.

## Ad Alanlarını İçe Aktar

.NET projenize Aspose.CAD için gerekli ad alanlarını içe aktararak başlayın. Bu adım, DGN'nin taramalı görüntü dönüştürmesi için gereken sınıflara ve yöntemlere erişmenizi sağlar.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Adım 1: DGN Dosyasını Yükleyin

 DGN dosyasını bir`CadImage` nesne. Bu daha sonraki operasyonlar için bir temel sağlar.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Daha ileri işlemler için kodunuz buraya gelecek
}
```

## Adım 2: Rasterleştirme Seçeneklerini Tanımlayın

 Oluşturmak`CadRasterizationOptions` Nesneyi seçin ve rasterleştirme işlemini gereksinimlerinize göre özelleştirmek için çeşitli özellikleri ayarlayın.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 3. Adım: JpegOptions Nesnesi Oluşturun

 DGN dosyasını JPEG'e dönüştürmeyi hedeflediğimiz için`JpegOptions` nesneyi seçin ve önceden tanımlanmış olanı atayın`CadRasterizationOptions` ona.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Adım 4: Raster Görüntüyü Kaydedin

 Kullanın`Save` yöntemi`CadImage` DGN dosyasını istenen formatta bir raster görüntüye, bu durumda JPEG'e aktarmak için sınıf.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Çözüm

Tebrikler! Aspose.CAD for .NET kullanarak bir DGN dosyasını raster görüntüye aktarma adımlarını başarıyla tamamladınız. Bu eğitim, bu işlevselliği .NET projelerinize zahmetsizce entegre etmeniz için sizi temel bilgilerle donattı.

## SSS'ler

### S1: DGN dosyalarını JPEG dışındaki formatlara aktarabilir miyim?

Cevap1: Evet, Aspose.CAD for .NET çeşitli çıktı formatlarını destekler. Seçenekleri uygun şekilde 3. Adımda değiştirebilirsiniz.

### S2 Dönüştürme işlemi sırasında istisnaları nasıl ele alabilirim?

C2: Olası sorunları çözmek için, sağlanan kodda gösterildiği gibi, uygun istisna yönetimine sahip olduğunuzdan emin olun.

### S3: Aspose.CAD for .NET'in deneme sürümü mevcut mu?

 C3: Evet, ürünü ücretsiz deneme sürümüyle keşfedebilirsiniz. Ziyaret etmek[Burada](https://releases.aspose.com/) daha fazla bilgi için.

### S4: Aspose.CAD for .NET ile ilgili nereden yardım alabilirim veya sorunları tartışabilirim?

 A4: Şuraya gidin:[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği ve tartışmalar için.

### S5: Aspose.CAD for .NET için geçici lisansı nasıl edinebilirim?

 A5: Ziyaret edin[bu bağlantı](https://purchase.aspose.com/temporary-license/)Geliştirme ihtiyaçlarınız için geçici bir lisans almak için.