---
date: 2026-03-26
description: Aspose.CAD for .NET kullanarak CAD'den PDF oluşturmayı ve DXF'yi PDF'ye
  dönüştürmeyi öğrenin. PDF, PNG, BMP ve daha fazlasında çarpıcı görseller için kalem
  seçeneklerini özelleştirin.
linktitle: Pen Support in Export
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Özel Kalem Seçenekleriyle CAD'den PDF Oluşturma – Aspose.CAD for .NET
url: /tr/net/cad-features-and-support/pen-support-in-export/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET'te Özel Kalem Seçenekleriyle CAD Dışa Aktarmayı Geliştirin

## Introduction

CAD dosyalarından **PDF oluşturmak** istiyorsanız ve bunu hızlı bir şekilde, tam görsel kontrolle yapmak istiyorsanız, Aspose.CAD for .NET tam da bunu sağlar. Kütüphanenin kalem‑destek özelliğini kullanarak başlangıç ve bitiş uçlarını, çizgi birleşimlerini ve diğer çizim özelliklerini tanımlayabilir, istediğiniz gibi görünen PDF'ler üretebilirsiniz. Bu öğretici, DXF dosyasını yüklemekten cilalı bir PDF dışa aktarmaya kadar tüm süreci adım adım gösterir; ayrıca aynı ayarların **CAD'yi PNG olarak dışa aktarma** veya **CAD görüntüsünü rasterleştirme** gibi diğer formatlar için nasıl yeniden kullanılabileceğini de gösterir.

## Quick Answers
- **“CAD'den PDF oluşturmak” ne anlama geliyor?** Vektör tabanlı CAD çizimlerini (ör. DXF) geometri ve stilini koruyarak bir PDF belgesine dönüştürür.  
- **Hangi formatlar kalem seçeneklerini destekler?** PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF ve WMF.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Diğer formatlar için çizgi uçlarını değiştirebilir miyim?** Evet—kalem seçenekleri Aspose.CAD tarafından desteklenen herhangi bir rasterleştirme hedefine uygulanır.  
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## What is pen support in CAD export?

Kalem desteği, bir CAD çizimi rasterleştirildiğinde veya vektör‑rasterleştirildiğinde çizgilerin nasıl çizileceğini özelleştirmenizi sağlar. `StartCap`, `EndCap`, `LineJoin` ve `DashStyle` gibi özellikleri ayarlayabilirsiniz. Bu ayarlar, dışa aktarılan görüntünün veya PDF'in son görünümünü etkiler ve görsel kalite üzerinde ayrıntılı kontrol sağlar.

## Why use custom pen options when you **create PDF from CAD**?

- **Tutarlı marka kimliği** – tüm belgelerde kurumsal çizgi stillerini eşleştirin.  
- **Gelişmiş okunabilirlik** – daha kalın uçlar ve birleşimler, teknik çizimleri ekranda ve basımda daha net hale getirir.  
- **Çapraz format esnekliği** – aynı kalem yapılandırması PNG, BMP ve diğer raster formatlarda da çalışır, zaman kazandırır.

## Prerequisites

- Aspose.CAD for .NET yüklü (indir: [release page](https://releases.aspose.com/cad/net/)).  
- DXF (Drawing Exchange Format) hakkında temel bilgi.  
- C# programlamaya aşina olmak.

## Import Namespaces

Başlamak için, C# projenizde gerekli ad alanlarını (namespaces) içe aktardığınızdan emin olun:

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

## Step 1: Set Up Your Document Directory

Kaynak CAD dosyasını içeren klasörü tanımlayın:

```csharp
string MyDir = "Your Document Directory";
```

## Step 2: Load the CAD Image

CAD çizimini (örneğin bir DXF dosyası) `Aspose.CAD.Image` nesnesine yükleyin:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Step 3: Configure Rasterization Options

Rasterleştirme ve PDF seçenekleri nesnelerini oluşturun. Bu nesneler, CAD verisinin raster görüntüye veya PDF sayfasına nasıl dönüştürüleceğini kontrol etmenizi sağlar:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Step 4: Customize Pen Options

İşte çizgileri çizen **kalemi özelleştirdiğiniz** yer. Başlangıç ve bitiş uçlarını `Flat`, `Round`, `Square` vb. olarak ayarlayabilirsiniz. Bu, ihtiyacınız olan görsel stil ile “CAD nasıl dışa aktarılır” sorusunun özüdür:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

*Pro ipucu:* `LineCap.Round` ile **CAD'yi PNG olarak dışa aktardığınızda** daha pürüzsüz çizgi uçları elde edebilirsiniz.

## Step 5: Apply Vector Rasterization Options

Rasterleştirme ayarlarını PDF seçeneklerine ekleyin, böylece dışa aktarma süreci hangi kalem yapılandırmasını kullanacağını bilir:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Step 6: Save the Exported PDF

Son olarak, PDF dosyasını oluşturun. Bu adım, **CAD'den PDF oluşturur** ve özel kalem ayarlarını uygular:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

`PdfOptions` yerine `PngOptions`, `BmpOptions` vb. nesneleri kullanarak aynı kalem yapılandırmasını koruyarak **CAD'yi PNG olarak dışa aktarabilir** veya diğer raster formatlara dönüştürebilirsiniz.

## Common Use Cases

- **Teknik dokümantasyon** – mühendislik PDF'lerine hassas çizgi stilleri ekleyin.  
- **Otomatik rapor oluşturma** – tek bir kalem profiliyle birçok DXF dosyasını toplu olarak PDF'ye dönüştürün.  
- **Web servisleri** – yüklenen DXF dosyalarını anında PDF'ye dönüştüren bir API sunun, tutarlı stil sağlanır.

## Troubleshooting & Common Pitfalls

| Sorun | Sebep | Çözüm |
|-------|--------|----------|
| Dışa aktarılan çizgiler beklenenden daha kalın görünüyor | DPI amaçlanandan yüksek | `rasterizationOptions.PageWidth` / `PageHeight` ayarlayın veya `Resolution` değerini değiştirin. |
| Kalem seçenekleri PNG çıktısında göz ardı ediliyor | `ImageOptions` yerine `VectorRasterizationOptions` kullanılıyor | Kaydetmeden önce `rasterizationOptions.PenOptions` atadığınızdan emin olun. |
| PDF dosyası boş | Kaynak DXF yolu hatalı veya dosya bozuk | `sourceFilePath`'i doğrulayın ve DXF'in istisna olmadan yüklendiğinden emin olun. |

## FAQ's

### Q1: Bu kalem seçeneklerini PDF dışındaki diğer görüntü formatları için kullanabilir miyim?

A1: Evet, kalem seçenekleri PNG, BMP, GIF, JPEG ve daha fazlası gibi çeşitli görüntü formatlarına uygulanabilir.

### Q2: Aspose.CAD for .NET için ek belgeleri nerede bulabilirim?

A2: Kapsamlı bilgi ve örnekler için [documentation](https://reference.aspose.com/cad/net/) sayfasına bakın.

### Q3: Aspose.CAD for .NET için ücretsiz deneme sürümü mevcut mu?

A3: Evet, ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

### Q4: Aspose.CAD for .NET için geçici lisansları nasıl alabilirim?

A4: Geçici lisans seçenekleri için [temporary license page](https://purchase.aspose.com/temporary-license/) sayfasını ziyaret edin.

### Q5: Aspose.CAD for .NET için topluluk desteği nereden alınabilir?

A5: Toplulukla [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) üzerinden etkileşime geçin.

## Additional Frequently Asked Questions

**S: **DXF'yi PDF'ye** programlı olarak nasıl dönüştürürüm?**  
C: DXF'i `Image.Load` ile yükleyin, `CadRasterizationOptions` ve `PdfOptions` yapılandırın, ardından yukarıdaki adımlarda gösterildiği gibi `Save` çağırın.

**S: PDF oluşturmadan bir CAD görüntüsünü rasterleştirebilir miyim?**  
C: Evet—`PngOptions`, `BmpOptions` veya başka bir raster format sınıfını kullanın ve aynı `rasterizationOptions`'ı atayarak yüksek kaliteli rasterleştirme elde edin.

**S: CAD'den PDF oluştururken çizgi kalınlığını değiştirmek mümkün mü?**  
C: Kaydetmeden önce `rasterizationOptions.CustomLineWidth`'ı ayarlayın veya `PenOptions.Width` özelliğini değiştirin.

**S: Kütüphane 3D DXF dosyalarını destekliyor mu?**  
C: Aspose.CAD 2D vektör verilerine odaklanır; 3D varlıklar rasterleştirme sırasında yok sayılır.

**S: Bu özellikler için hangi Aspose.CAD sürümü gerekiyor?**  
C: Kalem desteği 20.9 sürümünden itibaren mevcuttur; daha yeni bir sürüm yeterlidir.

---

**Son Güncelleme:** 2026-03-26  
**Test Edilen:** Aspose.CAD for .NET 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}