---
title: Farklı Düzenlerle Tek PDF Oluşturma - Aspose.CAD Guide
linktitle: Farklı Düzenlerle Tek PDF Oluşturma
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET'i kullanarak farklı düzenlerle tek bir PDF oluşturun. Sorunsuz entegrasyon ve verimli PDF oluşturma için adım adım kılavuzumuzu izleyin.
weight: 13
url: /tr/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Farklı Düzenlerle Tek PDF Oluşturma - Aspose.CAD Guide

## giriiş

Aspose.CAD for .NET'i kullanarak farklı düzenlere sahip bir CAD çiziminden tek bir PDF belgesi mi oluşturmak istiyorsunuz? Bu adım adım kılavuz, süreç boyunca size yol göstererek kusursuz entegrasyona ve etkili PDF oluşturmaya ulaşmanıza yardımcı olacaktır. Aspose.CAD for .NET, CAD çizimlerini programlı olarak yönetmek için güçlü özellikler sağlar ve bu eğitimde, farklı düzenlerle tek bir PDF oluşturmaya odaklanacağız.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

-  Aspose.CAD for .NET: Aspose.CAD for .NET'in kurulu olduğundan emin olun. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/cad/net/).

- Geliştirme Ortamı: Bir .NET geliştirme ortamı kurun ve C# programlama konusunda temel bir anlayışa sahip olun.

## Ad Alanlarını İçe Aktar

Aspose.CAD for .NET'in işlevselliklerinden yararlanmak için C# projenize gerekli ad alanlarını ekleyin:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Adım 1: CAD Görüntüsünü Yükleyin

```csharp
// Belgeler dizininin yolu.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // 1. Adım kodunuz buraya gelecek
}
```

## Adım 2: Rasterleştirme Seçeneklerini Özelleştirin

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Çeşitli düzenler için özel boyutlar
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## 3. Adım: PDF Seçeneklerini Tanımlayın

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## 4. Adım: PDF olarak kaydedin

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Artık Aspose.CAD for .NET'i kullanarak farklı düzenlere sahip tek bir PDF belgesini başarıyla oluşturdunuz. Daha fazla özelliği keşfetmekten ve kodu özel gereksinimlerinize göre özelleştirmekten çekinmeyin.

## Çözüm

Bu eğitimde Aspose.CAD for .NET'i kullanarak farklı düzenlere sahip bir CAD çiziminden tek bir PDF oluşturma sürecini ele aldık. Bu güçlü kitaplık, CAD manipülasyon görevlerini basitleştirir ve çeşitli senaryolar için esneklik sunar.

## SSS'ler

### S1: Aspose.CAD for .NET'i diğer CAD formatlarıyla kullanabilir miyim?

Cevap1: Evet, Aspose.CAD for .NET DWG, DXF, DGN ve daha fazlası gibi çeşitli CAD formatlarını destekler.

### S2: Ücretsiz deneme sürümü var mı?

 A2: Evet, ücretsiz deneme sürümünü keşfedebilirsiniz[Burada](https://releases.aspose.com/).

### S3: Aspose.CAD for .NET desteğini nasıl alabilirim?

 A3: Ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği için.

### S4: Ayrıntılı belgeleri nerede bulabilirim?

 Cevap4: Belgelere bakın[Burada](https://reference.aspose.com/cad/net/).

### S5: Aspose.CAD for .NET lisansını satın alabilir miyim?

 A5: Evet, lisans satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
