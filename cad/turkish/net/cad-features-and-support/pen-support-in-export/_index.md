---
title: Aspose.CAD for .NET'teki Özel Kalem Seçenekleri ile CAD Dışa Aktarmayı Geliştirin
linktitle: İhracatta Kalem Desteği
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET'i kullanarak CAD görüntü aktarımlarınızı nasıl geliştireceğinizi öğrenin. PDF, PNG, BMP ve daha fazlasında çarpıcı görseller için kalem seçeneklerini özelleştirin.
weight: 12
url: /tr/net/cad-features-and-support/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET'teki Özel Kalem Seçenekleri ile CAD Dışa Aktarmayı Geliştirin

## giriiş

Aspose.CAD for .NET, Bilgisayar Destekli Tasarım (CAD) dosyalarıyla çalışmak için güçlü bir araç seti sağlayarak geliştiricilerin CAD görüntülerini sorunsuz bir şekilde değiştirmesine ve dışa aktarmasına olanak tanır. Dikkate değer özelliklerden biri, dışa aktarma sırasında kalem desteği olup, kullanıcıların CAD görüntülerini PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF ve WMF gibi çeşitli formatlara dışa aktarırken kalemlerin başlangıç ve bitiş kapağı ayarlarını özelleştirmesine olanak tanır.

Bu eğitimde Aspose.CAD for .NET kullanarak dışa aktarmada kalem desteğinin ayrıntılarını inceleyeceğiz. Süreç boyunca size yol gösterecek net açıklamalar ve örnekler sunarak her adımı ayrıntılı olarak ele alacağız.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Aspose.CAD for .NET, geliştirme ortamınızda kuruludur. adresinden indirebilirsiniz.[yayın sayfası](https://releases.aspose.com/cad/net/).

- CAD dosya formatları, özellikle DXF (Çizim Değişim Formatı) hakkında temel bilgi.

- C# programlama dili hakkında çalışma bilgisi.

## Ad Alanlarını İçe Aktar

Başlamak için C# projenize gerekli ad alanlarını içe aktardığınızdan emin olun:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## 1. Adım: Belge Dizininizi Kurun

CAD belgenizin bulunduğu dizini tanımlayın:

```csharp
string MyDir = "Your Document Directory";
```

## Adım 2: CAD Görüntüsünü Yükleyin

Aspose.CAD'i kullanarak CAD görüntüsünü yükleyin:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## 3. Adım: Rasterleştirme Seçeneklerini Yapılandırın

Dışa aktarma işlemini özelleştirmek için rasterleştirme ve PDF seçenekleri oluşturun:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Adım 4: Kalem Seçeneklerini Özelleştirin

Kalemler için başlangıç ve bitiş kapağı seçeneklerini ayarlayın:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## Adım 5: Vektör Rasterleştirme Seçeneklerini Uygulayın

Rasterleştirme seçeneklerini PDF seçeneklerine uygulayın:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Adım 6: Dışa Aktarılan PDF'yi Kaydedin

CAD görüntüsünü özelleştirilmiş kalem seçenekleriyle PDF dosyası olarak kaydedin:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## Çözüm

Bu eğitimde Aspose.CAD for .NET'in dışa aktarma özelliğinde kalem desteğini inceledik. Adım adım kılavuzu takip ederek kalemlerin başlangıç ve bitiş kapağı ayarlarını kolayca özelleştirerek CAD görüntü aktarımlarınızın esnekliğini artırabilirsiniz.

Dışa aktarılan görsellerinizde istediğiniz görsel efektleri elde etmek için farklı kalem seçeneklerini denemekten çekinmeyin.

## SSS'ler

### S1: Bu kalem seçeneklerini PDF'nin yanı sıra diğer görüntü formatları için de kullanabilir miyim?

Cevap1: Evet, kalem seçenekleri PNG, BMP, GIF, JPEG ve daha fazlası gibi çeşitli görüntü formatlarına uygulanabilir.

### S2: Aspose.CAD for .NET için ek belgeleri nerede bulabilirim?

 A2: Bkz.[dokümantasyon](https://reference.aspose.com/cad/net/) Kapsamlı bilgi ve örnekler için.

### S3: Aspose.CAD for .NET'in ücretsiz deneme sürümü mevcut mu?

 C3: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.CAD for .NET için geçici lisansları nasıl alabilirim?

 A4: Ziyaret edin[geçici lisans sayfası](https://purchase.aspose.com/temporary-license/) Geçici lisanslama seçenekleri için.

### S5: Aspose.CAD for .NET için topluluk desteğini nereden alabilirim?

 A5: Toplulukla etkileşime geçin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
