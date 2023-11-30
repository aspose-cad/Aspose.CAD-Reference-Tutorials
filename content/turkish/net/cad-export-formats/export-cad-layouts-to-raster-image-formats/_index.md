---
title: Aspose.CAD for .NET'te CAD Düzenlerini Raster Görüntü Formatlarına Aktarın
linktitle: CAD Düzenlerini Raster Görüntü Formatlarına Aktarma
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET kullanarak CAD düzenlerini taramalı görüntülere nasıl aktaracağınızı öğrenin. Sorunsuz dönüşüm için adım adım kılavuzumuzu izleyin.
type: docs
weight: 10
url: /tr/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---
## giriiş

Aspose.CAD for .NET'i kullanarak CAD düzenlerini verimli bir şekilde raster görüntü formatlarına dönüştürmek mi istiyorsunuz? Bu adım adım kılavuz, görevi kusursuz hale getirmek için ayrıntılı talimatlar ve kod parçacıkları sağlayarak süreç boyunca size yol gösterecektir. İster deneyimli bir geliştirici olun ister Aspose.CAD'e yeni başlayan biri olun, bu eğitim tüm uzmanlık seviyelerine hitap etmektedir.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdakilere sahip olduğunuzdan emin olun:

-  Aspose.CAD for .NET Library: Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. Değilse, adresinden indirebilirsiniz.[Aspose.CAD web sitesi](https://releases.aspose.com/cad/net/).

- CAD Çizim Dosyası: Raster görüntü formatlarına dönüştürmek istediğiniz bir CAD çizim dosyasını (örn. conic_pyramid.dxf) hazırlayın.

## Ad Alanlarını İçe Aktar

Aspose.CAD işlevselliklerinden yararlanmak için .NET projenize gerekli ad alanlarını içe aktarın. Kodunuzun başına aşağıdaki ad alanlarını ekleyin:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Adım 1: CAD Çizimini Yükleyin

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Görüntü örneğine bir CAD çizimi yükleme
using (var image = Image.Load(sourceFilePath))
{
    //CAD çizimini yükleme kodunuz buraya gelir
}
```

## Adım 2: CadRasterizationOptions'ı oluşturun

```csharp
// CadRasterizationOptions'ın bir örneğini oluşturun
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## 3. Adım: Katmanları Belirleyin

```csharp
// Katman adını CadRasterizationOptions'ın katman listesine ekleyin
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## 4. Adım: JpegOptions'ı oluşturun

```csharp
// JpegOptions'ın (veya raster formatları için herhangi bir ImageOptions'ın) bir örneğini oluşturun
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Adım 5: Jpeg Formatına Aktarın

```csharp
// Her katmanı Jpeg formatına aktarın
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Ek Adım: Tüm Katmanları Dönüştürün

Tüm katmanları dönüştürmek istiyorsanız aşağıdaki yöntemi kullanın:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Bu yöntem, CAD çizimindeki tüm katmanları yineler ve her katmanı ayrı bir Jpeg dosyasına aktarır.

## Çözüm

Tebrikler! Aspose.CAD for .NET'i kullanarak CAD düzenlerini raster görüntü formatlarına nasıl aktaracağınızı başarıyla öğrendiniz. Bu eğitim, CAD dönüşümü için verimli ve güvenilir çözümler arayan geliştiriciler için kapsamlı bir kılavuz sağlar.

## SSS'ler

### S1: Dışa aktarma için diğer görüntü formatlarını kullanabilir miyim?

 A1: Evet, yapabilirsin. Basitçe değiştirin`JpegOptions` İstenilen formatın seçenekleriyle, örneğin`PngOptions` veya`BmpOptions`.

### S2: Deneme sürümü mevcut mu?

 Cevap2: Evet, deneme sürümünü indirerek Aspose.CAD'in işlevselliğini keşfedebilirsiniz.[Burada](https://releases.aspose.com/).

### S3: Aspose.CAD için nasıl destek alabilirim?

 Cevap3: Aspose.CAD'i ziyaret edin[forum](https://forum.aspose.com/c/cad/19) topluluk desteği için veya özel destek için bir lisans satın almayı düşünün.

### S4: Geçici lisanslar mevcut mu?

 Cevap4: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Belgeleri nerede bulabilirim?

 A5: Ayrıntılı belgelere bakın[Burada](https://reference.aspose.com/cad/net/).