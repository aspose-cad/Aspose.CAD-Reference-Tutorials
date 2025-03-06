---
title: DWG'yi PDF veya Raster Görüntülere Aktarma - Aspose.CAD Guide
linktitle: DWG'yi PDF'ye veya Raster Görüntülere Aktarma
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET kullanarak DWG'yi PDF'ye veya taramalı görüntülere aktarmaya ilişkin kapsamlı kılavuzu keşfedin. Adımları ve önkoşulları öğrenin ve bu güçlü kitaplığı kullanmaya başlayın.
weight: 11
url: /tr/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi PDF veya Raster Görüntülere Aktarma - Aspose.CAD Guide

## giriiş

.NET uygulamanızda DWG dosyalarını sorunsuz bir şekilde PDF'ye veya taramalı görüntülere dönüştürmeyi mi istiyorsunuz? Başka yerde arama! Bu adım adım kılavuz, güçlü Aspose.CAD for .NET kütüphanesini kullanarak süreç boyunca size yol gösterecektir. İster deneyimli bir geliştirici olun ister yeni başlıyor olun, bu eğitim tüm beceri düzeylerine hitap etmektedir.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdakilerin mevcut olduğundan emin olun:

- .NET programlamanın temel anlayışı.
-  Aspose.CAD for .NET kütüphanesi kuruldu. Değilse indirin[Burada](https://releases.aspose.com/cad/net/).
- .NET geliştirme için en sevdiğiniz entegre geliştirme ortamı (IDE) kurulumu.

## Ad Alanlarını İçe Aktar

.NET projenize gerekli ad alanlarını içe aktararak işe başlayalım. Bu, kodunuzdaki Aspose.CAD işlevselliğine erişmenizi sağlar.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Adım 1: DWG Dosyasını Yükleyin

Dönüştürmek istediğiniz DWG dosyasını yükleyerek başlayın. "Belge Dizininiz"i DWG dosyanızın yolu ile değiştirin.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // DWG yükleme kodunuz buraya gelecek
}
```

## 2. Adım: PDF Dışa Aktarmayı Ayarlayın

Şimdi PDF dışa aktarma ayarlarını yapılandıralım. Bu örnek, düzenin nasıl ayarlanacağını ve birim dönüşümlerinin nasıl işleneceğini gösterir.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Birim sistemini kontrol edin ve tanımlayın
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// PDF dışa aktarmayı ayarlama kodunuz buraya gelir
```

## 3. Adım: PDF'ye aktarın

Yapılandırılmış ayarları kullanarak PDF'ye aktarma işlemini gerçekleştirin.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Adım 4: Raster Görüntülere Dışa Aktarma

PNG gibi taramalı görüntülere dışa aktarma işlevini genişletin.

```csharp
// 300 DPI'da A4 boyutu - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Çözüm

Tebrikler! DWG dosyalarını hem PDF hem de raster görüntülere aktarmak için Aspose.CAD for .NET'i nasıl kullanacağınızı başarıyla öğrendiniz. Bu güçlü kitaplık süreci kolaylaştırarak verimli ve geliştirici dostu hale getirir.

## SSS'ler

### S1: Aspose.CAD for .NET'i ticari projelerimde kullanabilir miyim?

 A1: Evet, yapabilirsin. Ziyaret etmek[satın alma.aspose.com/buy](https://purchase.aspose.com/buy) lisans ayrıntıları için.

### S2: Ücretsiz deneme sürümü var mı?

 A2: Kesinlikle! Ücretsiz denemenizi alın[Burada](https://releases.aspose.com/).

### S3: Aspose.CAD for .NET desteğini nasıl alabilirim?

 A3: Şuraya gidin:[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği için.

### S4: Test amacıyla geçici bir lisans alabilir miyim?

 Cevap4: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Ayrıntılı belgeleri nerede bulabilirim?

 A5: Belgeler şu adreste mevcuttur:[Aspose.CAD](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
