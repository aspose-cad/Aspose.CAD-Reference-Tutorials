---
title: CAD Çizimlerine Filigran Ekleme - Aspose.CAD Guide
linktitle: CAD Çizimlerine Filigran Ekleme
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET'i kullanarak CAD çizimlerinizi profesyonel filigranlarla geliştirin. Kişiselleştirilmiş ve ilgi çekici tasarımlar için adım adım kılavuzumuzu izleyin.
type: docs
weight: 11
url: /tr/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## giriiş

Profesyonel filigranlar ekleyerek CAD çizimlerinizi geliştirmek mi istiyorsunuz? Aspose.CAD for .NET, filigranları CAD dosyalarınıza sorunsuz bir şekilde entegre etmek için güçlü bir çözüm sunar. Bu adım adım kılavuzda, Aspose.CAD kullanarak filigran ekleme sürecinde size yol göstereceğiz, böylece çizimlerinizin yalnızca kritik bilgileri iletmesini değil, aynı zamanda benzersiz işaretinizi de taşımasını sağlayacağız.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdakilere sahip olduğunuzdan emin olun:
-  Aspose.CAD for .NET: Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/cad/net/).
- Belge Dizininiz: CAD çizimlerinizi saklamak için bir dizin ayarlayın.
Şimdi CAD çizimlerinize filigran eklemeye başlayalım!

## Ad Alanlarını İçe Aktar

Gerekli ad alanlarını .NET projenize aktararak başlayın:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Adım 1: CAD Çizimini Yükleyin

```csharp
// Belgeler dizininin yolu.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Adım 2: Filigranı MTEXT olarak ekleyin

```csharp
// Yeni MTEXT ekle
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## 3. Adım: Veya Metin Olarak Filigran Ekleyin

```csharp
// Alternatif olarak Metin gibi daha basit bir varlık ekleyin
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## 4. Adım: PDF'ye aktarın

```csharp
// Filigranlı CAD çizimini PDF'ye aktarın
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Farklı çizimler için bu adımları tekrarlayın; kısa sürede profesyonel görünümlü filigranlı CAD dosyalarına sahip olacaksınız!

## Çözüm

Tebrikler! Aspose.CAD for .NET'i kullanarak CAD çizimlerinize nasıl filigran ekleyeceğinizi başarıyla öğrendiniz. Bu basit ama güçlü süreç, teknik çizimlerinizin bütünlüğünü korurken tasarımlarınızı kişiselleştirmenize olanak tanır.

## SSS'ler

### S1: Filigranın görünümünü özelleştirebilir miyim?

Cevap1: Evet, filigranın metnini, yazı tipini, boyutunu ve konumunu tercihlerinize göre özelleştirebilirsiniz.

### S2: Aspose.CAD farklı CAD dosya formatlarıyla uyumlu mudur?

Cevap2: Aspose.CAD, DWG ve DXF dahil olmak üzere çeşitli CAD dosya formatlarını destekleyerek geniş uyumluluk sağlar.

### S3: Tek bir CAD çizimine birden fazla filigran ekleyebilir miyim?

A3: Kesinlikle! Farklı kullanım durumları için esneklik sağlayacak şekilde gerektiği kadar filigran ekleyebilirsiniz.

### S4: Aspose.CAD ücretsiz deneme sunuyor mu?

Cevap4: Evet, Aspose.CAD'in özelliklerini ücretsiz denemeyle keşfedebilirsiniz. Anla[Burada](https://releases.aspose.com/).

### S5: Aspose.CAD desteğini nerede bulabilirim?

 A5: Herhangi bir sorunuz veya yardım için şu adresi ziyaret edin:[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19).