---
title: DWG'yi Uyumluluk PDF'sine Dönüştürme - Aspose.CAD Eğitimi
linktitle: DWG'yi Uyumluluk PDF'sine Dönüştürme
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET ile DWG'yi Uyumluluk PDF'sine dönüştürün. Adım adım rehberlik için eğitimimizi takip edin.
type: docs
weight: 13
url: /tr/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---
## giriiş

Aspose.CAD for .NET kullanarak DWG dosyalarını Uyumluluk PDF'sine dönüştürme hakkındaki adım adım eğitimimize hoş geldiniz. Aspose.CAD, geliştiricilerin CAD dosya formatlarıyla zahmetsizce çalışmasını sağlayan güçlü bir .NET API'sidir. Bu eğitimde, ayrıntılı örnekler ve açıklamalarla bir DWG dosyasını Uyumluluk PDF'sine dönüştürme sürecinde size rehberlik edeceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.CAD for .NET: Aspose.CAD kütüphanesinin .NET projenize entegre olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/cad/net/).

- Geliştirme Ortamı: Çalışan bir .NET geliştirme ortamını kurun ve doğru şekilde yapılandırıldığından emin olun.

- Örnek DWG Dosyası: Uyumluluk PDF'sine dönüştürmek istediğiniz örnek bir DWG dosyasını indirin.

## Ad Alanlarını İçe Aktar

Aspose.CAD işlevlerini kullanmak için .NET projenize gerekli ad alanlarını içe aktarın.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Şimdi bir DWG dosyasını Uyumluluk PDF'sine dönüştürme sürecini birden fazla adıma ayıralım.

## Adım 1: DWG Dosyasını Yükleyin

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## Adım 2: Rasterleştirme Seçeneklerini Ayarlayın

 Bir örneğini oluşturun`CadRasterizationOptions` ve arka plan rengi, sayfa genişliği ve sayfa yüksekliği gibi özelliklerini yapılandırın.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## 3. Adım: PDF Seçenekleri Oluşturun

 Bir örneğini oluşturun`PdfOptions` ve vektör rasterleştirme seçeneklerini ayarlayın.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## Adım 4: PDF olarak kaydedin (A1a Uyumluluğu)

CAD görüntüsünü A1a uyumluluğuyla Uyumluluk PDF'si olarak kaydedin.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## Adım 5: PDF olarak kaydedin (A1b Uyumluluğu)

Uyumluluk türünü A1b olarak değiştirin ve CAD görüntüsünü Uyumluluk PDF'si olarak kaydedin.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## Çözüm

Tebrikler! Aspose.CAD for .NET'i kullanarak bir DWG dosyasını başarıyla Uyumluluk PDF'sine dönüştürdünüz. Bu eğitim, CAD dönüştürme yeteneklerini uygulamalarına entegre etmek isteyen geliştiriciler için kapsamlı bir kılavuz sağlar.

## SSS'ler

### S1: Aspose.CAD'i kullanarak diğer CAD formatlarını Uyumluluk PDF'sine dönüştürebilir miyim?

Cevap1: Evet, Aspose.CAD çeşitli CAD formatlarını destekleyerek Uyumluluk PDF'sine dönüştürmeyi mümkün kılar.

### S2: Aspose.CAD .NET Core ile uyumlu mu?

Cevap2: Evet, Aspose.CAD hem .NET Framework hem de .NET Core ile uyumludur.

### S3: Aspose.CAD için herhangi bir lisanslama seçeneği var mı?

 C3: Evet, lisanslama seçeneklerini keşfedebilirsiniz[Burada](https://purchase.aspose.com/buy).

### S4: Ücretsiz deneme sürümü mevcut mu?

 A4: Evet, ücretsiz deneme sürümünden yararlanabilirsiniz[Burada](https://releases.aspose.com/).

### S5: Aspose.CAD için nereden destek alabilirim?

 A5: ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) Destekle ilgili tüm sorularınız için.