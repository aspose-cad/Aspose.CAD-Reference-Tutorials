---
date: 2026-09-29
description: Aspose.CAD for .NET kullanarak çizimlerinize Aspose CAD filigranı eklemeyi
  öğrenin. CAD dosyalarınızı kişiselleştirmek ve korumak için bu adım adım kılavuzu
  izleyin.
keywords:
- aspose cad watermark
- convert dwg to pdf
- generate pdf with watermark
- how to watermark cad
- add watermark to dwg
lastmod: 2026-09-29
linktitle: CAD Çizimlerine Filigran Ekleme
og_description: Aspose.CAD for .NET kullanarak çizimlerinize Aspose CAD filigranı
  eklemeyi öğrenin. Bu adım adım kılavuz, önkoşulları, dosya yüklemeyi, MTEXT veya
  metin filigranlarını uygulamayı ve PDF olarak dışa aktarmayı kapsar.
og_image_alt: Screenshot of Aspose.CAD watermarking tutorial for .NET
og_title: Aspose CAD filigranını çizimlerinize ekleyin – hızlı .NET kılavuzu
schemas:
- author: Aspose
  dateModified: '2026-09-29'
  description: Learn how to add an Aspose CAD watermark to your drawings using Aspose.CAD
    for .NET. Follow this step‑by‑step guide to personalize and protect your CAD files.
  headline: How to add an Aspose CAD watermark to drawings
  type: TechArticle
- questions:
  - answer: Yes, you can set text, font family, size, color, rotation angle, and opacity
      directly on the MTEXT or Text entity.
    question: Can I customize the appearance of the watermark?
  - answer: Aspose.CAD supports more than 30 input and output formats, including DWG,
      DXF, DWF, DGN, and IFC.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Call the watermark‑adding method multiple times with different
      positions or content.
    question: Can I add multiple watermarks to a single CAD drawing?
  - answer: Yes, you can explore Aspose.CAD's features with a free trial. Download
      **Aspose.CAD** [here](https://releases.aspose.com/).
    question: Does Aspose.CAD offer a free trial?
  - answer: For any queries or assistance, visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: Where can I find support for Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- cad watermark
- .net drawing
- dwg to pdf
- cad automation
title: Aspose CAD filigranını çizimlere nasıl eklenir
url: /tr/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD filigranını çizimlere ekleme

## Giriş

Bir **aspose cad watermark** eklemek, fikri mülkiyetinizi korumanıza ve paylaştığınız her çizime markanızı eklemenize olanak tanır. Aspose.CAD for .NET ile DWG, DXF veya diğer desteklenen CAD formatlarına doğrudan filigran gömebilir, orijinal tasarım yazılımına ihtiyaç duymadan çalışabilirsiniz. Bu öğreticide, filigranların neden önemli olduğunu, hangi formatların desteklendiğini ve adım adım nasıl uygulanacağını göreceksiniz.

## Hızlı cevaplar
- **Hangi kütüphane gerekiyor?** Aspose.CAD for .NET (resmi siteden indirin).  
- **Hangi dosya türlerine filigran ekleyebilirim?** DWG, DXF, DWF ve DGN dahil olmak üzere 30’dan fazla CAD/BIM formatı.  
- **Sonucu PDF olarak dışa aktarabilir miyim?** Evet – aynı API tek bir satırda filigranlı çizimi PDF olarak kaydetmenizi sağlar.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme test için yeterlidir; üretim için ticari lisans gereklidir.  
- **Kod .NET 6 ile uyumlu mu?** Kesinlikle – Aspose.CAD .NET Framework 4.5+, .NET Core 3.1+, .NET 5+ ve .NET 6+ sürümlerini destekler.

## Aspose CAD filigranı nedir?
Bir **Aspose CAD watermark**, Aspose.CAD'in bir CAD çiziminin model alanına eklediği metin veya MTEXT varlığıdır; dosyayla birlikte hareket eden yarı saydam bir katman olarak görüntülenir. Çizimi korur ve standart CAD görüntüleyicilerinde düzenlenebilir kalır.

## Neden Aspose.CAD filigran için kullanılmalı?
Aspose.CAD **30+** CAD ve BIM formatını işleyebilir ve **1.000 sayfaya kadar** dosyaları tüm belgeyi belleğe yüklemeden yönetebilir. Bu ölçülebilir yetenek, büyük mühendislik arşivlerini toplu olarak verimli bir şekilde işleyerek sunucu bellek kullanımını **%70** kadar azaltır.

## Önkoşullar

Başlamadan önce aşağıdakilerin kurulu olduğundan emin olun:

- Aspose.CAD for .NET yüklü – **Aspose.CAD for .NET** [buradan](https://releases.aspose.com/cad/net/) indirebilirsiniz.  
- Filigran eklemek istediğiniz CAD çizimlerini içeren bir klasör.  
- Geçerli bir Aspose lisansı (deneme çalıştırmaları için isteğe bağlı).

Şimdi, filigran ekleme sürecine göz atalım.

## Bir CAD çizimine nasıl filigran eklerim?

CAD dosyasını yükleyip bir filigran varlığı (MTEXT veya Text) oluşturur, model alanına eklersiniz ve ardından istenen formatta (ör. PDF) kaydedersiniz. Bu yöntem, desteklenen herhangi bir CAD formatı için çalışır ve toplu işleme için scriptlenebilir.

## Adım 1: CAD çizimini yükle

`CadImage` sınıfı, belleğe yüklenmiş bir CAD çizimini temsil eder ve varlıklarına erişim sağlar.  
```markdown
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
```

## Adım 2: Filigranı MTEXT olarak ekle

`CadMText`, çok satırlı metin ve biçimlendirme içeren bir varlık olup filigran mesajları için uygundur.  
```markdown
```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```
```

## Adım 3: Veya filigranı düz metin olarak ekle

`CadText`, çizimin model alanına yerleştirilebilen tek satırlı bir metin varlığıdır.  
```markdown
```csharp
// Add new MTEXT
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```
```

## Adım 4: PDF olarak dışa aktar

`CadRasterizationOptions` bir CAD çiziminin rasterleştirilme şeklini tanımlarken, `PdfOptions` PDF çıktı ayarlarını belirler.  
```markdown
```csharp
// Alternatively, add a simpler entity like Text
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```
```

Bu adımları koleksiyonunuzdaki her çizim için tekrarlayın; dağıtıma hazır, profesyonel filigranlı CAD dosyaları elde edeceksiniz.

## Yaygın sorunlar ve çözümler

- **Filigran dışa aktarma sonrası görünmüyor** – MTEXT veya Text varlığının `Opacity` özelliğinin 0.3 ile 0.7 arasında ayarlandığından emin olun; bu aralığın dışındaki değerler tamamen opak ya da görünmez olabilir.  
- **Büyük dosyalar bellek dalgalanmalarına neden oluyor** – `Image.Load` metodunu `LoadOptions` parametresiyle kullanarak akış (streaming) etkinleştirin, bu bellek kullanımını düşük tutar.  
- **Yanlış font render'ı** – Sunucuda çizim oluşturulurken kullanılan aynı TrueType fontlarını kurun veya `MText.Font` aracılığıyla yedek bir font ekleyin.

## Sıkça sorulan sorular

**S: Filigranın görünümünü özelleştirebilir miyim?**  
C: Evet, MTEXT veya Text varlığı üzerinde metin, yazı tipi, boyut, renk, döndürme açısı ve opaklık gibi özellikleri doğrudan ayarlayabilirsiniz.

**S: Aspose.CAD farklı CAD dosya formatlarıyla uyumlu mu?**  
C: Aspose.CAD, DWG, DXF, DWF, DGN ve IFC dahil olmak üzere 30’dan fazla giriş ve çıkış formatını destekler.

**S: Tek bir CAD çizimine birden fazla filigran ekleyebilir miyim?**  
C: Kesinlikle. Farklı konumlar veya içeriklerle filigran ekleme metodunu birden çok kez çağırabilirsiniz.

**S: Aspose.CAD ücretsiz deneme sunuyor mu?**  
C: Evet, Aspose.CAD'in özelliklerini ücretsiz deneme ile keşfedebilirsiniz. **Aspose.CAD** [buradan](https://releases.aspose.com/) indirebilirsiniz.

**S: Aspose.CAD için desteği nereden bulabilirim?**  
C: Her türlü soru ve yardım için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

---

**Son Güncelleme:** 2026-09-29  
**Test Edilen:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose  








```csharp
// Export the CAD drawing with watermark to PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

## İlgili Eğitimler

- [DWG'yi PDF'ye Dönüştür ve C#'ta Metin Ekle – Aspose.CAD Eğitimi](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Aspose.CAD for .NET ile CAD Çizimlerini PDF'ye Dönüştür ve Dışa Aktar – Eğitim](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)
- [Aspose.CAD for .NET ile Mesh Desteği Kullanarak DWG'yi PDF'ye Dönüştür](/cad/net/cad-features-and-support/mesh-support/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}