---
title: Aspose.CAD for .NET'te DGN'yi PDF'ye aktarın
linktitle: DGN'yi PDF'ye aktar
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET ile DGN dosyalarını zahmetsizce PDF'ye nasıl aktaracağınızı öğrenin. Kusursuz CAD dosyası manipülasyonu için adım adım kılavuz.
weight: 12
url: /tr/net/cad-export-formats/export-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET'te DGN'yi PDF'ye aktarın

## giriiş

.NET geliştirme dünyasında Aspose.CAD, CAD dosyalarının işlenmesini ve dönüştürülmesini kolaylaştıran güçlü bir kütüphanedir. Geliştiricilerin sıklıkla karşılaştığı ortak görevlerden biri, DGN dosyalarını PDF formatına aktarmaktır. Bu eğitimde Aspose.CAD for .NET'i kullanarak süreci adım adım anlatacağız.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdakilerin yerinde olduğundan emin olun:

- C# ve .NET çerçevesi hakkında çalışma bilgisi.
-  Aspose.CAD for .NET kütüphanesi kuruldu. İndirebilirsin[Burada](https://releases.aspose.com/cad/net/).
- Bu eğitim için örnek bir DGN dosyası, örneğin "Nikon_D90_Camera.dgn".

## Ad Alanlarını İçe Aktar

C# projenizde gerekli ad alanlarını içe aktararak başlayın:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Adım 1: DGN Dosyasını Yükleyin

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Kodunuz burada...
}
```

## Adım 2: Rasterleştirme Seçeneklerini Yapılandırın

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 3. Adım: PDF Seçenekleri Oluşturun

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 4. Adım: PDF olarak kaydedin

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Çözüm

Tebrikler! Aspose.CAD for .NET kullanarak bir DGN dosyasını başarıyla PDF'ye aktardınız. Bu eğitim, DGN dosyasının yüklenmesinden rasterleştirme seçeneklerinin yapılandırılmasına ve çıktının PDF olarak kaydedilmesine kadar temel adımları kapsıyordu.

## SSS'ler

### S1: Aspose.CAD for .NET'i önceden CAD bilgisi olmadan kullanabilir miyim?

A1: Kesinlikle! Aspose.CAD, karmaşık CAD görevlerini basitleştirerek farklı geçmişlere sahip geliştiricilerin erişebilmesini sağlar.

### S2: Aspose.CAD için daha fazla örnek ve belgeyi nerede bulabilirim?

 A2: Keşfedin[dokümantasyon](https://reference.aspose.com/cad/net/) Kapsamlı kılavuzlar ve örnekler için.

### S3: Aspose.CAD için ücretsiz deneme sürümü mevcut mu?

A3: Evet, ücretsiz deneme sürümünden yararlanabilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.CAD için nasıl geçici lisans alabilirim?

 Cevap4: Geçici lisanslar alın[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Yardıma mı ihtiyacınız var veya sorularınız mı var?

A5: ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
