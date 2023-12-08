---
title: OLE Nesnelerini DWG Dosyalarından Dışa Aktarma - Aspose.CAD Eğitimi
linktitle: OLE Nesnelerini DWG Dosyalarından Dışa Aktarma
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET kullanarak OLE nesnelerini DWG dosyalarından dışa aktarmaya ilişkin adım adım kılavuzu keşfedin. CAD dosyası işleme becerilerinizi zahmetsizce geliştirin.
type: docs
weight: 12
url: /tr/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---
## giriiş

OLE nesnelerini DWG dosyalarından kolaylıkla çıkarmak mı istiyorsunuz? Aspose.CAD for .NET, süreci sizin için kolaylaştırmak için burada. Bu öğreticide, OLE nesnelerini adım adım dışa aktarma konusunda size rehberlik ederek bu güçlü .NET kitaplığından en iyi şekilde yararlanmanızı sağlayacağız. 

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.CAD for .NET Library: Kütüphanenin kurulu olduğundan emin olun. adresinden indirebilirsiniz.[Aspose.CAD for .NET indirme sayfası](https://releases.aspose.com/cad/net/).

-  Belge Dizini: DWG dosyalarınızın depolandığı bir dizin ayarlayın. Yer değiştirmek`"Your Document Directory"` sağlanan kod pasajında gerçek yolla birlikte.

## Ad Alanlarını İçe Aktar

.NET projenizde Aspose.CAD işlevselliklerinden yararlanmak için gerekli ad alanlarını içe aktarmanız gerekecektir. Aşağıdaki kod parçacığını kullanın:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 1. Adım: Belge Dizinini Ayarlayın

```csharp
string MyDir = "Your Document Directory";
```

 Yer değiştirmek`"Your Document Directory"` DWG dosyalarınızın bulunduğu yolla.

## Adım 2: DWG Dosyalarını Belirleyin

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Dizi içinde işlemek istediğiniz DWG dosyalarını listeleyin.

## 3. Adım: Dışa Aktarma Seçeneklerini Yapılandırın

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Dışa aktarma seçeneklerini gereksinimlerinize göre özelleştirin. Bu örnekte PNG dışa aktarımını belirli bir düzen ile yapılandırıyoruz.

## Adım 4: Dosyaları Yineleyin ve Dışa Aktarın

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Belirtilen DWG dosyalarını yineleyin, her birini yükleyin ve dışa aktarılan PNG dosyasını tanımlanan seçeneklerle kaydedin.

## Çözüm

Tebrikler! Aspose.CAD for .NET'i kullanarak OLE nesnelerini DWG dosyalarından başarıyla dışa aktardınız. Bu güçlü kütüphane, karmaşık görevleri basitleştirerek CAD dosyası manipülasyonunda verimlilik ve esneklik sağlar.

## SSS'ler

### S1: Aspose.CAD for .NET hem alt hem de üst düzey CAD dosyaları için uygun mudur?

Cevap1: Evet, Aspose.CAD for .NET çok yönlüdür ve hem alt hem de üst düzey versiyonlar da dahil olmak üzere çok çeşitli CAD dosyalarını işleyebilir.

### S2: Farklı düzenler için dışa aktarma seçeneklerini özelleştirebilir miyim?

A2: Kesinlikle! Öğreticide gösterildiği gibi, düzenler de dahil olmak üzere dışa aktarma seçeneklerini özel ihtiyaçlarınıza göre uyarlayabilirsiniz.

### S3: Aspose.CAD for .NET'in ayrıntılı belgelerini nerede bulabilirim?

 A3: Keşfedin[Aspose.CAD for .NET belgeleri](https://reference.aspose.com/cad/net/) Ayrıntılı bilgi ve örnekler için.

### S4: Ücretsiz deneme sürümü mevcut mu?

 Cevap4: Evet, Aspose.CAD for .NET'in özelliklerini ücretsiz denemeyle deneyimleyebilirsiniz. Ziyaret etmek[bu bağlantı](https://releases.aspose.com/) başlamak.

### S5: Nasıl destek alabilirim veya toplulukla nasıl bağlantı kurabilirim?

 Cevap5: Destek ve topluluk katılımı için şu adresi ziyaret edin:[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19).