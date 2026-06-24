---
date: 2026-03-02
description: Aspise.CAD for .NET kullanarak farklı düzenlere sahip tek bir PDF nasıl
  oluşturulur, CAD'i PDF'ye dönüştürme, DWG'yi PDF'ye dışa aktarma ve CAD'i PDF olarak
  verimli bir şekilde kaydetme konusunda bilgi edinin.
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Farklı Düzenlerle Tek PDF Nasıl Oluşturulur - Aspose.CAD Rehberi
url: /tr/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Farklı Düzenlerle Tek PDF Oluşturma - Aspose.CAD Rehberi

## Introduction

Eğer **tek pdf** dosyaları oluşturmanız ve bu dosyaların içinde birden fazla CAD düzeni bulunması gerekiyorsa doğru yerdesiniz. Bu öğreticide, CAD çizimlerini tek bir PDF belgesine dönüştürmek için gereken adımları, birden çok düzeni aynı anda işleyerek adım adım göstereceğiz. Aspose.CAD for .NET'in **CAD to PDF** dönüşümünü, **DWG to PDF** dışa aktarmayı ve **CAD as PDF** kaydetmeyi sadece birkaç C# satırıyla nasıl kolaylaştırdığını göreceksiniz.

## Quick Answers
- **Bu öğreticide ne anlatılıyor?** Birden fazla CAD düzeni içeren tek bir PDF oluşturulması.  
- **Hangi kütüphane kullanılıyor?** Aspose.CAD for .NET.  
- **Lisans gerekli mi?** Değerlendirme için ücretsiz deneme sürümü yeterli; üretim ortamı için lisans gereklidir.  
- **Desteklenen CAD formatları?** DWG, DXF, DGN ve daha birçok format.  
- **Tipik uygulama süresi?** Temel bir dönüşüm için yaklaşık 10‑15 dakika.

## What is “create single pdf” in a CAD context?

Tek bir PDF oluşturmak, içinde birden fazla düzen tanımı (paper space) barındıran bir CAD kaynak dosyasını alıp, her bir düzeni tek PDF belgesinin ayrı sayfalarına birleştirmek anlamına gelir. Bu, mimari planlar, mühendislik şemaları veya müşterinin tek bir PDF paketi beklediği her senaryo için özellikle faydalıdır.

## Why use Aspose.CAD for this task?

- **Harici bağımlılık yok** – saf .NET, AutoCAD kurulumu gerekmez.  
- **Rasterizasyon üzerinde tam kontrol** – sayfa boyutu, DPI ve özel düzen boyutlarını ayarlayabilirsiniz.  
- **Yüksek doğruluklu render** – mümkün olduğunda vektör verileri korunur, net bir çıktı sağlar.  
- **Batch‑ready** – aynı kod bir döngü içinde yerleştirildiğinde birçok çizimi otomatik olarak işleyebilir.

## Prerequisites

- Aspose.CAD for .NET: Aspose.CAD for .NET'in kurulu olduğundan emin olun. İndirmek için [buraya](https://releases.aspose.com/cad/net/) tıklayın.  
- Development Environment: Bir .NET geliştirme ortamı kurun ve C# programlamaya temel bir anlayışa sahip olun.

## Import Namespaces

C# projenizde, Aspose.CAD for .NET işlevselliğinden yararlanmak için gerekli ad alanlarını ekleyin:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Step‑by‑step guide

### Step 1: Load the CAD Image

Öncelikle kaynak CAD dosyasını (örneğin bir DWG çizimi) yükleyin. `CadImage` sınıfı, dosya içindeki tüm düzenlere erişim sağlar.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### Step 2: Customize Rasterization Options

Her bir düzenin nasıl rasterize edileceğini tanımlayın. Varsayılan bir sayfa boyutu ayarlayabilir ve ardından `LayoutPageSizes` kullanarak belirli düzenler için bunu geçersiz kılabilirsiniz.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **Pro tip:** Detaylı çizimler için daha yüksek çözünürlük istiyorsanız DPI (`rasterizationOptions.Resolution`) değerini artırın.

### Step 3: Define PDF Options

Rasterizasyon ayarlarını bir `PdfOptions` nesnesi içinde paketleyin. Bu, Aspose.CAD'in CAD verilerini doğrudan bir PDF akışına render etmesini sağlar.

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### Step 4: Save as PDF

Son olarak, `CadImage` örneği üzerinde `Save` metodunu çağırarak hedef PDF dosya adını ve hazırlanmış seçenekleri geçin. Kütüphane, yapılandırdığınız her bir düzen için bir sayfa içeren tek bir PDF oluşturur.

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Bu çağrıdan sonra, “ANSI C Plot” ve “8.5 x 11 Plot” düzenlerini tek bütünleşik belgede birleştiren bir PDF elde edeceksiniz.

## Common pitfalls & troubleshooting

| Issue | Reason | Fix |
|-------|--------|-----|
| PDF'de düzenler eksik | `LayoutPageSizes` bir düzen adı için tanımlı değil | CAD dosyasındaki tam düzen adlarını (büyük/küçük harf duyarlı) doğrulayın. |
| Düşük kalite çıktı | Varsayılan DPI 96 | Kaydetmeden önce `rasterizationOptions.Resolution = 300` (veya daha yüksek) ayarlayın. |
| Dosya bulunamadı | Yanlış `MyDir` yolu | Platform bağımsız yollar oluşturmak için `Path.Combine` kullanın. |

## Frequently Asked Questions

### Q1: Aspose.CAD for .NET'i diğer CAD formatlarıyla kullanabilir miyim?

A1: Evet, Aspose.CAD for .NET DWG, DXF, DGN ve daha birçok CAD formatını destekler.

### Q2: Ücretsiz deneme sürümü mevcut mu?

A2: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) inceleyebilirsiniz.

### Q3: Aspose.CAD for .NET için destek nasıl alınır?

A3: Topluluk desteği için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

### Q4: Ayrıntılı dokümantasyonu nereden bulabilirim?

A4: Dokümantasyona [buradan](https://reference.aspose.com/cad/net/) ulaşabilirsiniz.

### Q5: Aspose.CAD for .NET için lisans satın alabilir miyim?

A5: Evet, lisansı [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

**Additional Q&A**

**S:** Özel sayfa boyutlarıyla **DWG to PDF** dışa aktarmak nasıl yapılır?  
**C:** `CadRasterizationOptions.LayoutPageSizes` kullanarak her DWG düzenini istediğiniz PDF sayfa boyutlarına eşleyin; adım 2'de gösterildiği gibi.

**S:** Vektör verilerini rasterize etmeden **CAD as PDF** kaydetmek mümkün mü?  
**C:** Aspose.CAD PDF oluştururken her zaman rasterize eder, ancak görsel doğruluğu korumak için DPI'yi artırabilirsiniz.

## Conclusion

Bu rehberde, Aspose.CAD for .NET kullanarak birden fazla düzen içeren CAD çizimlerinden **tek pdf** dosyaları oluşturmayı gösterdik. Artık **CAD to PDF**, **DWG to PDF** ve **CAD as PDF** işlemlerini tek bir otomatik iş akışında gerçekleştirecek temel bileşenlere sahipsiniz. Projenizin kalite gereksinimlerine uygun rasterizasyon ayarlarıyla deneyler yapın ve bu kodu daha büyük batch‑işleme hatlarına entegre edin.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

---