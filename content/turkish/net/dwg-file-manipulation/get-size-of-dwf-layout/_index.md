---
title: C#'ta DWG Dosyalarıyla Çalışma - DWF Düzeninin Boyutunu Alma
linktitle: C#'ta DWG Dosyalarıyla Çalışma - DWF Düzeninin Boyutunu Alma
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: DWG dosyalarını işlemede Aspose.CAD for .NET'in gücünü keşfedin. C# kullanarak DWF düzeni boyutlarını zahmetsizce çıkarmayı öğrenin.
type: docs
weight: 10
url: /tr/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## giriiş

Bilgisayar destekli tasarım (CAD) ve .NET geliştirme alanında Aspose.CAD, DWG dosyalarını yönetmek için güçlü bir araç olarak duruyor. Bu eğitim, C# dilinde DWG dosyalarıyla çalışma ve bir DWF düzeninin boyutunu çıkarma sürecinde size rehberlik edecektir. Kodlara dalmadan önce, bu yolculuğa çıkmak için her şeyin ayarlandığından emin olalım.

## Önkoşullar

Bu öğreticiyi sorunsuz bir şekilde takip etmek için aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

-  Aspose.CAD for .NET: Aspose.CAD for .NET'in kurulu olduğundan emin olun. adresinden indirebilirsiniz.[Aspose.CAD for .NET indirme sayfası](https://releases.aspose.com/cad/net/).

Artık gerekli araçlara sahip olduğunuza göre kodlama alanına geçelim.

## Ad Alanlarını İçe Aktar

Kodla çalışmaya başlamadan önce gerekli ad alanlarını içe aktaralım:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Bu ad alanları, C# uygulamanızda Aspose.CAD ile CAD dosyalarını işlemek için gerekli sınıfları ve yöntemleri sağlayacaktır.

## 1. Adım: Ortamınızı Kurun

Projeniz için doğru ortamın kurulduğundan emin olarak başlayın. C# projenizde Aspose.CAD kütüphanesine başvurun.

## 2. Adım: Dosya Yollarını Tanımlayın

DWG dosyanızın yollarını ve oluşturulan JPG dosyalarının çıktı dizinini tanımlayın:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## 3. Adım: DWF Görüntüsünü Yükleyin

Aspose.CAD'i kullanarak DWF görüntüsünü yükleyin:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Daha sonraki adımların kodu buraya gelecek
}
```

## Adım 4: Sayfalar Arasında Yineleme Yapın

DWF görüntüsünün sayfalarını yineleyin:

```csharp
foreach (var page in image.Pages)
{
    // Daha sonraki adımların kodu buraya gelecek
}
```

## Adım 5: Düzen Bilgilerini Alın

Her sayfadan düzen bilgilerini alın:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Adım 6: JPG Seçeneklerini Ayarlayın

Düzeni JPG dosyası olarak kaydetme seçeneklerini ayarlayın:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Daha sonraki adımların kodu buraya gelecek
}
```

## Adım 7: Sayfa Boyutunu Belirleyin

DWF düzeninin boyutunu belirleyin:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Daha sonraki adımların kodu buraya gelecek
```

## Adım 8: Sayfa Boyutlarını Ayarlayın

Birim türüne göre sayfa boyutlarını ayarlayın:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Adım 9: JPG Dosyasını Kaydedin

JPG dosyasını belirtilen seçeneklerle kaydedin:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Artık C# dilinde Aspose.CAD'i kullanarak DWF düzeninin boyutunu DWG dosyasından başarıyla çıkardınız. Aspose.CAD'in .NET geliştirme için sunduğu daha fazla özellik ve işlevi keşfetmekten çekinmeyin.

## Çözüm

Bu eğitimde Aspose.CAD kullanarak C#'ta DWG dosyalarıyla çalışma sürecini anlattık. Bu adımları takip ederek yalnızca DWF düzeninin boyutunu elde etmekle kalmaz, aynı zamanda .NET projelerinizde Aspose.CAD'in CAD ile ilgili çeşitli görevlerinden de yararlanabilirsiniz.

## SSS'ler

### S1: Aspose.CAD en yeni DWG dosya formatlarıyla uyumlu mu?

 Cevap1: Aspose.CAD, en son sürümler de dahil olmak üzere çeşitli DWG dosya formatlarını destekler. Bakın[dokümantasyon](https://reference.aspose.com/cad/net/) belirli uyumluluk ayrıntıları için.

### S2: Aspose.CAD'i hem ticari hem de kişisel projeler için kullanabilir miyim?

C2: Evet, Aspose.CAD hem ticari hem de kişisel kullanım için esnek lisanslama seçenekleri sunuyor. Ziyaret edin[satın alma sayfası](https://purchase.aspose.com/buy) daha fazla ayrıntı için.

### S3: Aspose.CAD için nasıl geçici lisans alabilirim?

 Cevap 3: Geçici lisansı şu adresten alabilirsiniz:[Burada](https://purchase.aspose.com/temporary-license/) değerlendirme amaçlı.

### S4: Aspose.CAD desteğini nerede bulabilirim?

 A4: Sorularınız veya yardım için şu adresi ziyaret edin:[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19).

### S5: Aspose.CAD'in ücretsiz deneme sürümü mevcut mu?

 Cevap5: Evet, Aspose.CAD'in ücretsiz deneme sürümüne erişebilirsiniz.[Burada](https://releases.aspose.com/).