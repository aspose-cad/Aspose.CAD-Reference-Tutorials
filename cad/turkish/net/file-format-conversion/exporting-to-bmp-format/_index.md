---
title: BMP Formatına Aktarma - Aspose.CAD Eğitimi
linktitle: BMP Formatına Aktarma
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET'i kullanarak BMP'ye 3D görüntü aktarımının kusursuz dünyasını keşfedin. Sorunsuz bir deneyim için eğitimimizi takip edin.
weight: 11
url: /tr/net/file-format-conversion/exporting-to-bmp-format/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# BMP Formatına Aktarma - Aspose.CAD Eğitimi

## giriiş

Yazılım geliştirmenin dinamik dünyasında Aspose.CAD for .NET, Bilgisayar Destekli Tasarım (CAD) dosyalarını işlemek için güçlü bir araç olarak öne çıkıyor. CAD görüntülerini yaygın olarak kullanılan BMP formatına aktarmak istiyorsanız bu eğitim başvurulacak kılavuzunuzdur. Bu adım adım anlatımda, Aspose.CAD for .NET kullanarak 3D görüntüleri BMP'ye aktarma sürecini inceleyeceğiz. Hadi dalalım!

## Önkoşullar

Bu eğitime başlamadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

-  Aspose.CAD for .NET: Aspose.CAD kütüphanesini şu adresten indirip yükleyin:[Burada](https://releases.aspose.com/cad/net/).
- Geliştirme Ortamı: Bir .NET geliştirme ortamı kurun.
- CAD Dosyası: Dışa aktarmaya hazır bir CAD dosyası bulundurun. Bu örnek için "18-12-11 9644 - site.dwf"yi kullanacağız.

## Ad Alanlarını İçe Aktar

.NET projenizde gerekli ad alanlarını içe aktardığınızdan emin olun:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Adım 1: CAD Görüntüsünü Yükleyin

CAD görüntüsünü projenize yükleyerek başlayın. "Belge Dizininiz"i gerçek dizin yolu ile değiştirin.

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    // Resmi yükleme kodunuz buraya gelecek
}
```

## Adım 2: BMP Dışa Aktarma Seçeneklerini Yapılandırma

CAD dosyaları için vektör rasterleştirme seçenekleri de dahil olmak üzere BMP dışa aktarma seçeneklerini ayarlayın.

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## 3. Adım: BMP'ye aktarın

BMP dosyasının çıkış yolunu belirterek dışa aktarma işlemini yürütün.

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## Çözüm

Tebrikler! Aspose.CAD for .NET'i kullanarak bir 3D görüntüyü başarıyla BMP'ye aktardınız. Bu eğitim Aspose.CAD'in çok yönlülüğüne bir bakış sunarak karmaşık görevlerin çok kolay olmasını sağlıyor.

## SSS'ler

### S1: Aspose.CAD for .NET'i herhangi bir CAD dosya formatıyla kullanabilir miyim?

Cevap1: Evet, Aspose.CAD çeşitli CAD dosya formatlarını destekleyerek projelerinizde esneklik sağlar.

### S2: Test amaçlı olarak geçici bir lisans mevcut mu?

 A2: Kesinlikle! Geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/) Evrim için.

### S3: Aspose.CAD için kapsamlı belgeleri nerede bulabilirim?

 A3: Belgelere bakın[Burada](https://reference.aspose.com/cad/net/) detaylı bilgi ve örnekler için.

### S4: Nasıl destek alabilirim veya toplulukla nasıl bağlantı kurabilirim?

 Cevap4: Aspose.CAD forumunu ziyaret edin[Burada](https://forum.aspose.com/c/cad/19) soru sormak ve toplulukla etkileşime geçmek.

### S5: Aspose.CAD for .NET'i satın alabilir miyim?

 Cevap5: Evet, Aspose.CAD'i satın alabilirsiniz[Burada](https://purchase.aspose.com/buy) Projeleriniz için tüm potansiyelini açığa çıkarmak için.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
