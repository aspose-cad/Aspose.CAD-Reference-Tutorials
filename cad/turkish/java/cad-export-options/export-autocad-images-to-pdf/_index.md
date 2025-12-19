---
date: 2025-12-19
description: Aspose.CAD for Java kullanarak AutoCAD PDF dışa aktarmayı öğrenin. Bu
  adım adım kılavuz, DWG'yi PDF'ye nasıl dönüştüreceğinizi, CAD'i PDF olarak nasıl
  kaydedeceğinizi ve lisanslamayı nasıl yöneteceğinizi gösterir.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: AutoCAD PDF Dışa Aktar - Aspose.CAD for Java ile AutoCAD Görüntülerini PDF'ye
  Dışa Aktarma Öğreticisi
url: /tr/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export AutoCAD PDF - Export AutoCAD Images to PDF with Aspose.CAD for Java

## Introduction

Java kullanarak **AutoCAD PDF dışa aktarmak** istiyor musunuz? Daha fazla aramanıza gerek yok! Bu öğreticide, Aspose.CAD for Java ile AutoCAD görüntülerini PDF’ye dönüştürmeyi adım adım göstereceğiz; bu güçlü kütüphane **DWG'yi PDF’ye dönüştürme** sürecini zahmetsiz hâle getirir. Sonunda **CAD’i PDF olarak kaydetme**, özel rasterleştirme ayarları uygulama ve üretim kullanımı için bir Aspose.CAD lisansı ile çalışma konularını anlayacaksınız.

## Quick Answers
- **Java ile DWG'yi PDF’ye dönüştürebilir miyim?** Evet, Aspose.CAD for Java DWG, DXF ve birçok diğer formatı destekler.  
- **Bir lisansa ihtiyacım var mı?** Sınırsız kullanım için bir **Aspose CAD lisansı** gereklidir; değerlendirme için geçici bir lisans mevcuttur.  
- **Hangi Java sürümü destekleniyor?** Java 8+ (kütüphane tüm modern JDK'larla uyumludur).  
- **PDF sayfa boyutunu özelleştirebilir miyim?** Kesinlikle – rasterleştirme seçeneklerinde `pageWidth` ve `pageHeight` değerlerini ayarlayın.  
- **3‑B rasterleştirme mümkün mü?** Evet, tam 3‑B render için `TypeOfEntities.Entities3D` etkinleştirin.

## What is **export autocad pdf**?
Exporting AutoCAD PDF, vektör tabanlı CAD çizimlerini (DWG, DXF, DWF vb.) katmanları, çizgi kalınlıklarını koruyarak ve isteğe bağlı olarak 3‑B geometrisini de içerecek şekilde taşınabilir bir PDF belgesine dönüştürmek anlamına gelir. Bu, tasarımları müşterilerle paylaşmak, arşivlemek veya CAD yazılımı gerektirmeden yazdırmak için faydalıdır.

## Why use Aspose.CAD for Java to **export autocad pdf**?
- **Tam format desteği** – DWG, DXF, DWF ve daha fazlasıyla çalışır.  
- **Harici bağımlılık yok** – saf Java kütüphanesi, yerel DLL gerektirmez.  
- **Yüksek‑kaliteli rasterleştirme** – DPI, sayfa boyutu ve yerleşim üzerinde kontrol sağlar.  
- **Lisans esnekliği** – ücretsiz deneme ile başlayıp kalıcı bir **Aspose CAD lisansı**na yükseltebilirsiniz.  

## Prerequisites

Başlamadan önce şunların kurulu olduğundan emin olun:

- **Java Geliştirme Ortamı** – JDK 8 veya üzeri yüklü.  
- **Aspose.CAD for Java Kütüphanesi** – [indirme bağlantısı](https://releases.aspose.com/cad/java/) üzerinden indirin.  
- **Belge Dizini** – kaynak CAD dosyalarının ve oluşturulacak PDF'lerin bulunacağı bir klasör.

## Import Namespaces

Java projenizde Aspose.CAD ile çalışmak için gerekli sınıfları içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Şimdi kodu adım adım inceleyelim.

## Step‑by‑Step Guide

### Step 1: Set the Resource Directory Path

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **İpucu:** `"Your Document Directory"` ifadesini, ön koşullarda oluşturduğunuz klasörün mutlak yolu ile değiştirin.

### Step 2: Load the CAD Image

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Neden önemli:** CAD dosyasını bir `Image` nesnesine yüklemek, Aspose.CAD’in rasterleştirme motoruna tam erişim sağlar.

### Step 3: Set Rasterization Options

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Çıktı PDF’nin boyutunu değiştirmek için `pageWidth` ve `pageHeight` değerlerini ayarlayın.  
- 3‑B varlıklar için **java convert cad pdf** ihtiyacınız varsa `setTypeOfEntities` satırının yorumunu kaldırın.  
- `setLayouts` çağrısı, render edilecek düzeni (Model, Layout1 vb.) seçer.

### Step 4: Configure PDF Options

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Bu, rasterleştirme ayarlarını PDF çıktısına bağlayarak vektör verisinin doğru şekilde dönüştürülmesini sağlar.

### Step 5: Save the PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Ortaya çıkan dosya `Export3DImagestoPDF_out_.pdf`, orijinal AutoCAD çiziminizin bir **save cad as pdf** temsilidir.

## Common Issues & Solutions

| Belirti | Muhtemel Neden | Çözüm |
|---------|----------------|-------|
| Boş PDF çıktısı | Rasterleştirme seçenekleri ayarlanmamış veya düzen eşleşmiyor | `setLayouts` değerinin CAD dosyanızdaki düzen adıyla aynı olduğundan emin olun. |
| Düşük çözünürlüklü görüntü | `pageWidth`/`pageHeight` çok küçük | Boyutları artırın veya `rasterizationOptions.setResolution(...)` ile daha yüksek DPI ayarlayın. |
| Lisans istisnası | Geçerli lisans uygulanmamış | Bir **Aspose CAD lisansı** uygulayın veya test için geçici lisans kullanın. |

## Frequently Asked Questions

### Q1: Aspose.CAD for Java ile diğer CAD dosya formatlarını da kullanabilir miyim?
A1: Evet, Aspose.CAD DWG, DWF, DGN ve daha fazlası dahil olmak üzere geniş bir format yelpazesini destekler, bu da projelerinizde esneklik sağlar.

### Q2: Aspose.CAD for Java için geçici bir lisans nasıl alınır?
A2: Değerlendirme amaçlı geçici lisans almak için [burayı](https://purchase.aspose.com/temporary-license/) ziyaret edin.

### Q3: Rasterleştirme için herhangi bir düzen seçeneği var mı?
A3: Evet, `setLayouts` yöntemiyle (ör. `"Model"`, `"Layout1"`) hangi görünümün render edileceğini özelleştirebilirsiniz.

### Q4: Çıktı PDF dosyasının boyutunu özelleştirebilir miyim?
A4: Kesinlikle! Rasterleştirme seçeneklerinde `pageWidth` ve `pageHeight` parametrelerini istediğiniz boyutlara göre ayarlayın.

### Q5: Aspose.CAD for Java ile ilgili yardım almak veya sorunları tartışmak için nereden destek bulabilirim?
A5: Ayrı destek ve topluluk tartışmaları için [Aspose.CAD forumuna](https://forum.aspose.com/c/cad/19) göz atın.

---

**Last Updated:** 2025-12-19  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}