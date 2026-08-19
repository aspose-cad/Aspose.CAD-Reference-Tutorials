---
date: 2026-03-16
description: Aspose.CAD for .NET ile DWG'yi PDF veya raster görüntülere nasıl dönüştüreceğinizi
  öğrenin. Bu adım adım CAD‑den‑PDF öğreticisi, DWG'yi PNG gibi görüntü formatlarına
  dışa aktarmayı kapsar ve DWG'yi görüntü dosyalarına verimli bir şekilde dışa aktarmanın
  yollarını gösterir.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET kullanarak DWG'yi PDF ve Raster Görüntülere Dönüştürme
url: /tr/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

, Why it Happens, How to Fix headings and cells.

FAQ: translate questions and answers, but keep URLs unchanged.

Also bullet list under Quick Answers: translate each bullet but keep code names.

Make sure to preserve markdown formatting.

Let's produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi PDF veya Raster Görüntülere Dönüştürme - Aspose.CAD Kılavuzu

## Giriş

Eğer bir .NET uygulamasından **DWG'yi PDF'ye** (veya PNG gibi raster formatlara) doğrudan dönüştürmeniz gerekiyorsa doğru yerdesiniz. Bu öğreticide Aspose.CAD for .NET kullanarak dönüşümün tam adımlarını gösterecek, kütüphanenin neden sağlam bir tercih olduğunu açıklayacak ve sadece birkaç satır kodla PDF ve görüntü çıktısını nasıl yöneteceğinizi göstereceğiz.

## Hızlı Yanıtlar
- **DWG dönüşümünü hangi kütüphane yönetir?** Aspose.CAD for .NET  
- **DWG'yi PNG olarak da PDF'ye dışa aktarabilir miyim?** Evet – aynı rasterleştirme seçenekleri her iki format için de çalışır.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü yeterlidir; üretim için ticari lisans gereklidir.  
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Birim dönüşümü otomatik olarak yapılır mı?** Kodda gösterildiği gibi birim sistemini (metrik veya imperial) manuel olarak tanımlayabilirsiniz.

## “DWG'yi PDF'ye dönüştürmek” ne demektir?
DWG'yi PDF'ye dönüştürmek, bir CAD çizimini (DWG) taşınabilir, yalnızca görüntülenebilir bir belgeye (PDF) render etmektir. Bu, CAD yazılımı olmayan paydaşlarla tasarımları paylaşmak, yazdırılabilir dokümantasyon oluşturmak veya çizimleri evrensel olarak okunabilir bir formatta arşivlemek için kullanışlıdır.

## Bu dönüşüm için neden Aspose.CAD kullanılmalı?
- **Harici bağımlılık yok** – kütüphane tamamen yönetilen kod içinde çalışır.  
- **Yüksek doğruluk** – katmanları, hat kalınlıklarını ve düzen bilgilerini korur.  
- **Yerleşik raster seçenekleri** – tek bir yapılandırma nesnesiyle PNG, JPEG, BMP vb. formatlara dışa aktarım sağlar.  
- **Çapraz platform** – .NET Core ile Windows, Linux ve macOS'ta çalışır.

## Önkoşullar

Öğreticiye başlamadan önce aşağıdakilerin hazır olduğundan emin olun:

- .NET programlamaya temel bir anlayış.  
- Aspose.CAD for .NET kütüphanesi yüklü. Yüklü değilse, [buradan](https://releases.aspose.com/cad/net/) indirebilirsiniz.  
- .NET geliştirme için tercih ettiğiniz bütünleşik geliştirme ortamı (IDE) kurulmuş.

## Ad Alanlarını İçe Aktarın

.NET projenizde gerekli ad alanlarını içe aktararak işe başlayalım. Bu, kodunuzda Aspose.CAD işlevselliğine erişmenizi sağlar.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Adım 1: DWG Dosyasını Yükle

Dönüştürmek istediğiniz DWG dosyasını yükleyin. `"Your Document Directory"` ifadesini DWG dosyanızın yolu ile değiştirin.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Adım 2: PDF Dışa Aktarımını Ayarla (DWG'yi PDF'ye nasıl dışa aktarılır)

Şimdi PDF dışa aktarım ayarlarını yapılandıralım. Bu örnek, düzeni ayarlamayı ve birim dönüşümlerini ele almayı gösterir.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Adım 3: PDF'ye Dışa Aktar

Yapılandırılmış ayarları kullanarak PDF'ye dışa aktarımı gerçekleştirin.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Adım 4: Raster Görüntülere Dışa Aktar (dwg'yi görüntüye dışa aktar)

Fonksiyonu PNG gibi raster görüntülere dışa aktarım yapacak şekilde genişletin.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Nasıl Düzeltilir |
|-------|--------------|-------------------|
| **PDF'de boş sayfalar** | Düzen doğru belirtilmemiş | `rasterizationOptions.Layouts` içinde doğru düzen adının (ör. `"Model"`) bulunduğundan emin olun. |
| **Yanlış boyutlar** | DPI veya sayfa boyutu uyuşmazlığı | `CadRasterizationOptions` içinde `PageHeight`, `PageWidth` ve DPI değerlerini ayarlayın. |
| **Birimler hatalı** | Birim dönüşümü tanımlanmamış | `DefineUnitSystem` kullanarak `currentUnitIsMetric` ve `currentUnitCoefficient` değerlerini `cadImage.UnitType` temelinde ayarlayın. |
| **Lisans istisnası** | Deneme sürümü sınırlamaları | `Image.Load` çağrısından önce geçici veya kalıcı bir lisans uygulayın. |

## Sık Sorulan Sorular

### S1: Aspose.CAD for .NET'i ticari projelerimde kullanabilir miyim?
C1: Evet, kullanabilirsiniz. Lisans detayları için [purchase.aspose.com/buy](https://purchase.aspose.com/buy) adresini ziyaret edin.

### S2: Ücretsiz bir deneme sürümü mevcut mu?
C2: Kesinlikle! Ücretsiz denemenizi [buradan](https://releases.aspose.com/) alabilirsiniz.

### S3: Aspose.CAD for .NET için destek nasıl alabilirim?
C3: Topluluk desteği için [Aspose.CAD forumuna](https://forum.aspose.com/c/cad/19) göz atın.

### S4: Test amaçlı geçici bir lisans alabilir miyim?
C4: Evet, geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

### S5: Ayrıntılı belgeleri nerede bulabilirim?
C5: Dokümantasyon [Aspose.CAD](https://reference.aspose.com/cad/net/) adresinde mevcuttur.

### S6: **CAD'i PNG olarak yüksek kaliteyle nasıl kaydederim?**
C6: `CadRasterizationOptions` içinde `PageHeight` ve `PageWidth` değerlerini istediğiniz piksel boyutlarına ayarlayın ve DPI'yi 300 veya daha yüksek bir değere belirleyin.

### S7: Kaynak dosya birden fazla düzen içerdiğinde **dwg nasıl dönüştürülür** en iyi yol nedir?
C7: Dışa aktarmak istediğiniz tüm düzen adlarını `rasterizationOptions.Layouts` içine ekleyin, ardından her bir düzen için döngü oluşturup `Save` metodunu ilgili çıktı formatı ile çağırın.

---

**Son Güncelleme:** 2026-03-16  
**Test Edilen Versiyon:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}