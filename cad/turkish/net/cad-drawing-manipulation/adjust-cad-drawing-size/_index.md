---
title: Aspose.CAD for .NET'te CAD Çizim Boyutunu Ayarlama
linktitle: CAD Çizim Boyutunu Ayarlama
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD'i kullanarak .NET'te CAD çizim boyutlarını zahmetsizce nasıl ayarlayabileceğinizi öğrenin. Sorunsuz yeniden boyutlandırma için adım adım kılavuzumuzu izleyin.
type: docs
weight: 10
url: /tr/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## giriiş

.NET uygulamalarınızda CAD çizimlerinin boyutunu sorunsuz bir şekilde ayarlamak mı istiyorsunuz? Aspose.CAD for .NET, CAD çiziminin yeniden boyutlandırılmasını zahmetsizce gerçekleştirmenize olanak tanıyan sağlam bir çözüm sunar. Bu eğitimde, Aspose.CAD kullanarak CAD çizimlerini yeniden boyutlandırmanın inceliklerini kavramanızı sağlamak için her adımı ayrıntılı olarak anlatarak süreç boyunca size rehberlik edeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

- Aspose.CAD for .NET Library: Kütüphaneyi şuradan indirip yükleyin:[Aspose.CAD for .NET indirme sayfası](https://releases.aspose.com/cad/net/).
- Örnek CAD Çizimi: Belge dizininizde örnek bir CAD çizim dosyanızın (örneğin, "sample.dwg") bulunduğundan emin olun.

## Ad Alanlarını İçe Aktar

Gerekli ad alanlarını .NET uygulamanıza aktararak başlayın. Bu adım, Aspose.CAD for .NET tarafından sağlanan işlevlere erişmek için çok önemlidir.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Adım 1: CAD Çizimini Yükleyin

CAD çizimini Aspose.CAD.Image sınıfının bir örneğine yükleyerek başlayın. Örnek çiziminiz için doğru dosya yoluna sahip olduğunuzdan emin olun.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Görüntü örneğine bir CAD çizimi yükleme
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Kodunuz burada...
}
```

## Adım 2: BmpOptions'ı oluşturun

CAD çizimini BMP dosyası olarak kaydederken seçeneklerin belirlenmesinden sorumlu olan BmpOptions sınıfının bir örneğini oluşturun.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Adım 3: CadRasterizationOptions'ı ayarlayın

CadRasterizationOptions sınıfını oluşturun ve vektör rasterleştirme için özelliklerini yapılandırın.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Adım 4: UnitType Özelliğini Ayarlayın

Yeniden boyutlandırma için birim türünü belirtmek üzere CadRasterizationOptions'ın UnitType özelliğini ayarlayın. Bu örnekte Santimetre olarak ayarlanmıştır.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Adım 5: Düzenler Özelliğini Ayarlayın

Düzenler özelliğini ayarlayarak, yeniden boyutlandırılan çizime dahil etmek istediğiniz düzenleri belirtin.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Adım 6: BMP'ye aktarın

Son olarak, yeniden boyutlandırılan düzeni Kaydet yöntemini kullanarak BMP dosyası olarak kaydedin.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Artık Aspose.CAD for .NET'i kullanarak CAD çiziminizin boyutunu başarıyla ayarladınız!

## Çözüm

Bu eğitimde Aspose.CAD kullanarak .NET'te CAD çizimlerini yeniden boyutlandırma sürecini inceledik. Bu adımları takip ederek bu işlevselliği sorunsuz bir şekilde uygulamalarınıza entegre ederek sorunsuz bir kullanıcı deneyimi sağlayabilirsiniz.

## SSS

### S1: Aspose.CAD for .NET tüm CAD formatlarıyla uyumlu mudur?

 Cevap1: Aspose.CAD for .NET, DWG, DXF, DWF ve daha fazlasını içeren çok çeşitli CAD formatlarını destekler. Kontrol edin[dokümantasyon](https://reference.aspose.com/cad/net/) tam liste için.

### S2: Birden fazla düzeni aynı anda yeniden boyutlandırabilir miyim?

C2: Evet, CadRasterizationOptions'taki düzenler dizisini ayarlayarak birden çok düzeni yeniden boyutlandırabilirsiniz.

### S3: Aspose.CAD for .NET desteğini nereden alabilirim?

 A3: Ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) Toplumsal destek ve yardım için.

### S4: Ücretsiz deneme sürümü mevcut mu?

 A4: Evet, keşfedebilirsiniz[ücretsiz deneme](https://releases.aspose.com/) Aspose.CAD for .NET'in özelliklerini değerlendirmek.

### S5: Aspose.CAD for .NET için nasıl geçici lisans alabilirim?

 Cevap5: Test amaçlı geçici bir lisans edinin[Burada](https://purchase.aspose.com/temporary-license/).