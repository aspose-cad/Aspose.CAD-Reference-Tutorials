---
date: 2026-03-13
description: Aspose.CAD for .NET kullanarak CAD rasterleştirme seçeneklerini nasıl
  ayarlayacağınızı ve belirli DWG düzenlerini PDF'ye nasıl dışa aktaracağınızı öğrenin
  – CAD dosyasından PDF oluşturmak için kesin rehber.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD Rasterleştirme Seçeneklerini Ayarla – Belirli Düzenleri PDF'ye Dışa Aktar
  - Aspose.CAD Kılavuzu
url: /tr/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

Be careful to preserve code block placeholders as they are.

Also preserve blockquote > formatting.

Now craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Belirli Düzenleri PDF'ye Dışa Aktarma - Aspose.CAD Kılavuzu

## Introduction

Bu öğreticide **CAD rasterleştirme seçeneklerini nasıl ayarlayacağınızı** keşfedecek ve bir DWG dosyasından tek bir düzeni—veya birden fazla düzeni—doğrudan PDF olarak dışa aktarabileceksiniz. Aspose.CAD for .NET, *dwg to pdf conversion c#* sürecini basitleştirir ve sayfa boyutu, çözünürlük ve düzen seçimi üzerinde tam kontrol sağlar. Kılavuzun sonunda sadece birkaç satır kodla **CAD dosyasından PDF oluşturabileceksiniz**.

## Quick Answers
- **“set cad rasterization options” ne işe yarar?**  
  Aspose.CAD'e vektör verilerini (düzenler, katmanlar, hat kalınlıkları) rasterleştirilmiş PDF sayfalarına nasıl render edeceğini söyler.  
- **DWG düzenini PDF'e dışa aktaran yöntem hangisidir?**  
  `Image.Save` metodunu, içinde `CadRasterizationOptions` bulunan yapılandırılmış bir `PdfOptions` ile kullanın.  
- **Bir seferde birden fazla düzen dışa aktarabilir miyim?**  
  Evet – `Layouts` özelliğine düzen adlarının bir dizisini sağlayın.  
- **Üretim kullanımı için lisansa ihtiyacım var mı?**  
  Ticari bir lisans gereklidir; değerlendirme için ücretsiz bir deneme sürümü mevcuttur.  
- **Hangi .NET sürümleri destekleniyor?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 ve sonrası.

## What is “set cad rasterization options”?

`CadRasterizationOptions`, CAD varlıklarının PDF gibi raster‑tabanlı formatlara dönüştürülürken nasıl rasterleştirileceğini kontrol eden sınıftır. Sayfa boyutları, düzen seçimi, arka plan rengi vb. özelliklerini yapılandırarak **export dwg layout to pdf** işleminin görsel sonucunu belirlersiniz.

## Why set CAD rasterization options?
- **Precision** – Orijinal CAD çiziminde görülen hat kalınlıklarını ve ölçekleri tam olarak korur.  
- **Performance** – İhtiyacınız olan düzenleri yalnızca render ederek dosya boyutunu ve işlem süresini azaltır.  
- **Flexibility** – Sayfa genişliği/yüksekliği, DPI ve arka planı raporlama standartlarınıza göre ayarlamanızı sağlar.  

## Prerequisites

Kodlamaya başlamadan önce şunların yüklü olduğundan emin olun:

- **Aspose.CAD for .NET** yüklü olmalı. Bunu [buradan](https://releases.aspose.com/cad/net/) indirebilirsiniz.  
- Bir .NET geliştirme ortamı (Visual Studio, VS Code veya tercih ettiğiniz herhangi bir IDE).  
- En az bir düzen içeren bir DWG dosyası (burada kullanılan örnek dosya `visualization_-_conference_room.dwg`).

## Import Namespaces

.NET projenizde Aspose.CAD için gerekli ad alanlarını içe aktarın:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG file

DWG dosyasını yükleyin

İlk olarak, Aspose.CAD'i dönüştürmek istediğiniz kaynak DWG dosyasına yönlendirin.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Step 2: Set **CadRasterizationOptions**

CadRasterizationOptions ayarlayın

Burada PDF sayfa boyutu ve çözünürlüğünü belirleyen rasterleştirme ayarlarını yapılandırıyoruz.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Pro tip:** `PageWidth` ve `PageHeight` değerlerini hedef PDF düzeninizin boyutlarına göre ayarlayın. Daha büyük değerler detayları artırır ancak dosya boyutunu da büyütür.

### Step 3: Specify the layout name

Düzen adını belirtin

Aspose.CAD'e hangi düzen(ler)i render edeceğini söyleyin. `"Layout1"` ifadesini DWG dosyanızdaki düzenin tam adıyla değiştirin.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Neden önemli:** `Layouts` dizisini sınırlayarak istenmeyen sayfaların dışa aktarılmasını önler, **dwg to pdf conversion c#** işlemini hızlandırır ve ortaya çıkan PDF'i daha temiz hâle getirir.

### Step 4: Create `PdfOptions`

`PdfOptions` oluşturun

Rasterleştirme ayarlarını PDF dışa aktarma seçeneklerine bağlayın.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Step 5: Export to PDF

PDF olarak dışa aktarın

Son olarak, render edilen düzeni bir PDF dosyası olarak kaydedin.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Step 6: Display a success message

Başarı mesajını gösterin

Kısa bir konsol çıktısı işlemin başarılı olduğunu onaylar.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Common Issues & Solutions

| Sorun | Neden | Çözüm |
|-------|-------|-------|
| **PDF oluşturulmadı** | `Layouts` dizisi DWG içinde herhangi bir düzen adıyla eşleşmiyor. | Bir CAD görüntüleyici kullanarak düzen adlarını doğrulayın ve `Layouts` özelliğini güncelleyin. |
| **Boş sayfalar** | `PageWidth`/`PageHeight` 0 veya çok küçük bir değere ayarlanmış. | Gerçekçi boyutlar (ör. 1600 × 1600) kullanın veya bu özellikleri atlayarak Aspose'in otomatik hesaplamasına izin verin. |
| **Yanlış ölçekleme** | Yüksek çözünürlüklü çıktı gerektiğinde DPI ayarlanmamış. | Dışa aktarmadan önce `rasterizationOptions.Resolution = 300;` (veya istenen DPI) değerini ayarlayın. |

## Frequently Asked Questions

**S: Birden fazla düzeni aynı anda dışa aktarabilir miyim?**  
C: Evet, Step 3'teki `Layouts` dizisini tüm istenen düzen adlarını içerecek şekilde değiştirmeniz yeterlidir, ör. `new string[] { "Layout1", "Layout2" }`.

**S: Aspose.CAD diğer CAD dosya formatlarıyla uyumlu mu?**  
C: Kesinlikle. DWG, DXF, DWF, DGN ve daha birçok formatı destekler.

**S: PDF çıkış ayarlarını sayfa boyutunun ötesinde nasıl ayarlayabilirim?**  
C: `CadRasterizationOptions` sınıfının `Resolution`, `BackgroundColor` ve `DrawType` gibi ek özelliklerini inceleyerek sonucu ince ayar yapabilirsiniz.

**S: Ek Aspose.CAD belgelerine nereden ulaşabilirim?**  
C: Derinlemesine API referansları ve örnekler için [documentation](https://reference.aspose.com/cad/net/) sayfasını ziyaret edin.

**S: Ücretsiz bir deneme sürümü mevcut mu?**  
C: Evet, ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

## Conclusion

Artık **CAD rasterleştirme seçeneklerini** nasıl ayarlayacağınızı ve bunları **Aspose.CAD for .NET** ile **belirli DWG düzenlerini PDF'e dışa aktarmak** için nasıl kullanacağınızı öğrendiniz. Bu yaklaşım, dönüşüm süreci üzerinde kesin kontrol sağlar ve CAD‑to‑PDF işlevselliğini herhangi bir C# uygulamasına hızlı ve güvenilir bir şekilde entegre etmenize olanak tanır.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}