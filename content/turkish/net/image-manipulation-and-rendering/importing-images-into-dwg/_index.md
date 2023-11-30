---
title: Görüntüleri C# ile DWG Dosyalarına Aktarma - Aspose.CAD Guide
linktitle: C# ile Görüntüleri DWG Dosyalarına Aktarma
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET ile C# kullanarak görüntüleri DWG dosyalarına aktarmayı öğrenin. Sorunsuz entegrasyon için adım adım kılavuzumuzu izleyin.
type: docs
weight: 11
url: /tr/net/image-manipulation-and-rendering/importing-images-into-dwg/
---
## giriiş

Bilgisayar destekli tasarım (CAD) alanında, görüntüleri DWG dosyalarına dahil etmek yaygın ve önemli bir görevdir. Aspose.CAD for .NET, bu süreci kolaylaştırmak için güçlü bir araç seti sağlayarak C# geliştiricilerinin erişimini sağlar. Bu eğitimde, görüntüleri adım adım DWG dosyalarına nasıl aktaracağımızı keşfedeceğiz.

## Önkoşullar

Kılavuza dalmadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- Temel C# programlama bilgisi.
-  Aspose.CAD for .NET kuruldu. İndirebilirsin[Burada](https://releases.aspose.com/cad/net/).
- Bir geliştirme ortamı oluşturuldu.

## Ad Alanlarını İçe Aktar

C# projenize gerekli ad alanlarını eklediğinizden emin olun:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 1. Adım: Belge Dizininizi Kurun

```csharp
string MyDir = "Your Document Directory";
```

## Adım 2: DWG Dosyasını Yükleyin

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## 3. Adım: Görüntü Özelliklerini Tanımlayın

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## Adım 4: Ekleme Noktasını ve Vektörleri Ayarlayın

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## Adım 5: Raster Görüntüyü Oluşturun ve Yapılandırın

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## Adım 6: DWG Dosyasına Resim Ekleme

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## Adım 7: PDF olarak kaydedin

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Çözüm

Görüntüleri C# ve Aspose.CAD for .NET kullanarak DWG dosyalarına entegre etmek kusursuz bir süreçtir ve geliştiricilere CAD projelerini görsel öğelerle zahmetsizce geliştirme olanağı sağlar.

## SSS'ler

### S1: Aspose.CAD for .NET'i diğer programlama dilleriyle birlikte kullanabilir miyim?

Cevap1: Aspose.CAD öncelikle .NET için tasarlanmıştır, ancak Aspose çeşitli programlama dilleri için kütüphaneler sağlar.

### S2: Aspose.CAD for .NET'in ücretsiz deneme sürümü mevcut mu?

 A2: Evet, ücretsiz deneme sürümünü keşfedebilirsiniz[Burada](https://releases.aspose.com/).

### S3: Aspose.CAD için ayrıntılı belgeleri nerede bulabilirim?

 A3: Belgeler mevcut[Burada](https://reference.aspose.com/cad/net/).

### S4: Aspose.CAD for .NET için nasıl geçici lisans alabilirim?

 A4: Ziyaret edin[bu bağlantı](https://purchase.aspose.com/temporary-license/) geçici lisans almak için.

### S5: Aspose.CAD desteği için topluluk forumları var mı?

 C5: Evet, destek arayabilir ve toplulukla etkileşime geçebilirsiniz[Burada](https://forum.aspose.com/c/cad/19).