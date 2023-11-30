---
title: Aspose.CAD for .NET'te Kanvas Boyutunu ve Modunu Ayarlama
linktitle: Kanvas Boyutunu ve Modunu Ayarlama
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET'te tuval boyutunu ve modunu ayarlamaya ilişkin adım adım kılavuzu keşfedin. Bu kapsamlı eğitimi kullanarak CAD oluşturma işleminizi kolaylıkla optimize edin.
type: docs
weight: 16
url: /tr/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## giriiş

Aspose.CAD for .NET'in tüm potansiyelini ortaya çıkarmaya ve CAD işleme deneyiminizde devrim yaratmaya hazır mısınız? Bu adım adım eğitimde, güçlü Aspose.CAD kütüphanesini kullanarak tuval boyutunu ve modunu ayarlamanın inceliklerini inceleyeceğiz. İster deneyimli bir geliştirici olun ister yeni başlıyor olun, bu kılavuz süreç boyunca size yol gösterecek ve Aspose.CAD'in yeteneklerinden etkili bir şekilde yararlanmanızı sağlayacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.CAD Kütüphanesi: Aspose.CAD kütüphanesini şuradan indirip yükleyin:[Aspose.CAD web sitesi](https://releases.aspose.com/cad/net/).

- Geliştirme Ortamı: Makinenizde bir .NET geliştirme ortamının kurulu olduğundan emin olun.

-  Örnek CAD Dosyası: Bu eğitim için örnek bir DXF dosyası kullanacağız. İçinde bir tane bulabilirsin[Aspose.CAD belgeleri](https://reference.aspose.com/cad/net/).

## Ad Alanlarını İçe Aktar

Başlamak için .NET uygulamanızın başlangıcında gerekli ad alanlarını içe aktarın:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Adım 1: CAD Dosyasını Yükleyin

Aşağıdaki kodu kullanarak CAD dosyasını yükleyerek başlayın:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Daha sonraki adımlara ilişkin kodunuz buraya gelecek
}
```

## Adım 2: CadRasterizationOptions'ı oluşturun

 Bir örneğini oluşturun`CadRasterizationOptions` ve özelliklerini ayarlayın:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## 3. Adım: PdfOptions Oluşturun

 Bir örneğini oluşturun`PdfOptions` ve onu ayarla`VectorRasterizationOptions` mülk:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 4. Adım: PDF'ye aktarın

Yapılandırılmış seçenekleri kullanarak CAD dosyasını PDF'ye aktarın:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Adım 5: TiffOptions'ı oluşturun

 Bir örneğini oluşturun`TiffOptions` ve onu ayarla`VectorRasterizationOptions` mülk:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Adım 6: TIFF'e aktarın

Yapılandırılmış seçenekleri kullanarak CAD dosyasını TIFF'e aktarın:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Çözüm

Tebrikler! Aspose.CAD for .NET'te tuval boyutunu ve modunu başarıyla ayarladınız. Bu güçlü özellik, CAD oluşturma için bir olasılıklar dünyasının kapılarını açar. Farklı seçenekleri deneyin ve .NET uygulamalarınızda Aspose.CAD'in tüm potansiyelini keşfedin.

## SSS'ler

### S1: Aspose.CAD'i diğer .NET kütüphaneleriyle kullanabilir miyim?

Cevap1: Evet, Aspose.CAD diğer .NET kitaplıklarıyla sorunsuz bir şekilde bütünleşerek CAD manipülasyonu için gelişmiş yetenekler sağlar.

### S2: Aspose.CAD için ücretsiz deneme sürümü mevcut mu?

 Cevap2: Evet, Aspose.CAD'in özelliklerini ücretsiz deneme sürümüyle keşfedebilirsiniz. Ziyaret etmek[Burada](https://releases.aspose.com/) başlamak.

### S3: Aspose.CAD için nasıl destek alabilirim?

 Cevap 3: Destek ve tartışmalar için şu adresi ziyaret edin:[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19).

### S4: Aspose.CAD için kapsamlı belgeleri nerede bulabilirim?

 A4: Bkz.[Aspose.CAD belgeleri](https://reference.aspose.com/cad/net/) detaylı bilgi ve örnekler için.

### S5: Aspose.CAD for .NET'i nasıl satın alabilirim?

 Cevap5: Aspose.CAD'i satın almak için şu adresi ziyaret edin:[satın alma sayfası](https://purchase.aspose.com/buy).