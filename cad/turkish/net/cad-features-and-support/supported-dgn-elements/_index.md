---
title: Aspose.CAD for .NET'te desteklenen DGN Elementleri
linktitle: Desteklenen DGN Öğeleri
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET'in DGN dosyalarını işlemeye yönelik güçlü özelliklerini keşfedin. 2D ve 3D öğelerle sorunsuz bir şekilde çalışmak için adım adım kılavuzumuzu izleyin.
type: docs
weight: 18
url: /tr/net/cad-features-and-support/supported-dgn-elements/
---
## giriiş

DGN dosyalarıyla sorunsuz bir şekilde çalışmak isteyen bir .NET geliştiricisi misiniz? Aspose.CAD for .NET, DGN dosyalarını verimli bir şekilde yönetmek için güçlü bir çözüm sunar. Bu eğitimde, desteklenen DGN öğelerini inceleyerek Aspose.CAD for .NET ile çalışma sürecinde size yol göstereceğiz.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- .NET programlamaya ilişkin temel bilgiler.
- Makinenizde Visual Studio yüklü.
-  İndirebileceğiniz Aspose.CAD for .NET kütüphanesi[Burada](https://releases.aspose.com/cad/net/).

## Ad Alanlarını İçe Aktar

Projenizi başlatmak için gerekli ad alanlarını .NET uygulamanıza aktarın. Bu adım, Aspose.CAD for .NET tarafından sağlanan işlevlere erişmenizi sağlar.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Adım 1: DGN Dosyasını Yükleyin

Mevcut bir DGN dosyasını .NET uygulamanıza CadImage olarak yükleyerek başlayın.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Kodunuz burada
}
```

## Adım 2: DGN Öğeleri Üzerinden Yineleme Yapın

Bir foreach döngüsü kullanarak DGN öğelerini yineleyin. Aspose.CAD for .NET üzerinde çalışabileceğiniz çeşitli DGN eleman türleri sağlar.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Kodunuz burada
}
```

## 3. Adım: Önceden Desteklenen Varlıkları İşleyin

Daha önce desteklenen ve artık 3B için de desteklenen 2B varlıkları işleyin.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Ek durumlar
        {
            // Kodunuz burada
            break;
        }
}
```

## 4. Adım: Desteklenen 3B Varlıkları İşleyin

Aspose.CAD for .NET tarafından sağlanan desteklenen 3D varlıkları yönetin.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Kodunuz burada
            break;
        }
}
```

## Adım 5: Dışa Aktarın ve Kaydedin

Son olarak, değiştirilen DGN dosyasını taramalı bir görüntüye aktarın ve belirtilen dizine kaydedin.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Çözüm

Bu eğitimde Aspose.CAD for .NET'in DGN dosyalarını işleme ve işleme konusundaki yeteneklerini araştırdık. Adım adım kılavuzu izleyerek, ister 2B ister 3B varlıklar olsun, desteklenen DGN öğeleriyle verimli bir şekilde çalışabilirsiniz. Aspose.CAD for .NET, DGN dosya işlemeyi .NET uygulamalarınıza sorunsuz bir şekilde entegre etmenizi sağlar.

## SSS'ler

### S1: Aspose.CAD for .NET belgelerini nerede bulabilirim?

 A1: Belgeleri bulabilirsiniz[Burada](https://reference.aspose.com/cad/net/).

### S2: Aspose.CAD for .NET'i nasıl indirebilirim?

 A2: Kütüphaneyi indirebilirsiniz[Burada](https://releases.aspose.com/cad/net/).

### S3: Aspose.CAD for .NET'in ücretsiz deneme sürümü mevcut mu?

 C3: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.CAD for .NET için geçici lisansları nereden alabilirim?

 Cevap4: Geçici lisanslar mevcut[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Yardıma mı ihtiyacınız var veya sorularınız mı var?

 Cevap5: Aspose.CAD for .NET topluluğunu ziyaret edin[destek Forumu](https://forum.aspose.com/c/cad/19).