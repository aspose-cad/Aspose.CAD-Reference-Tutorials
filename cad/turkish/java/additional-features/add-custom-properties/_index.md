---
date: 2025-11-30
description: Aspose.CAD kullanarak Java’da dwg dosyalarına özel özellikler eklemeyi
  öğrenin. CAD çizimlerinde organizasyonu ve bilgi alımını zahmetsizce geliştirin.
linktitle: Add Custom Properties to DWG Files Using Java
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java Kullanarak DWG Dosyalarına Özel Özellikler Ekleyin
url: /tr/java/additional-features/add-custom-properties/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java Kullanarak DWG Dosyalarına Özel Özellikler Ekleme

CAD çizimlerini programlı olarak manipüle etmek, birçok Java geliştiricisinin günlük ihtiyacıdır. Bu öğreticide, güçlü Aspose.CAD for Java kütüphanesini kullanarak **dwg dosyalarına özel özellikler eklemeyi** keşfedeceksiniz. Kılavuzun sonunda, DWG dosyasının başlık kısmına doğrudan meta verileri enjekte eden yeniden kullanılabilir bir kod parçacığına sahip olacaksınız; bu sayede çizimlerinizin kataloglanması, aranması ve bakımı daha kolay olacak.

## Introduction

Aspose.CAD for Java, AutoCAD gerektirmeden geniş bir CAD formatı yelpazesini okumanıza, düzenlemenize ve yazmanıza olanak tanıyan tamamen yönetilen .NET‑free bir kütüphanedir. Bir DWG dosyasına özel özellikler eklemek, proje kodları, revizyon notları veya sahip bilgileri gibi ek bilgileri doğrudan çizim dosyasının içinde hafif bir şekilde depolamanızı sağlar.

## Quick Answers
- **“add custom properties dwg” ne anlama geliyor?** DWG dosyasının başlık meta verilerine kullanıcı tanımlı ad/değer çiftleri eklemek anlamına gelir.  
- **Hangi kütüphane bunu yönetir?** Aspose.CAD for Java, bu özellikleri okuma ve yazma için basit bir API sağlar.  
- **Uygulama ne kadar sürer?** Temel bir örnek için genellikle 5‑10 dakika.  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Diğer CAD formatlarıyla uyumlu mu?** Evet—DXF, DWF ve daha fazlası desteklenir.

## What is Adding Custom Properties to DWG Files?

Özel özellikler, DWG başlığında depolanan anahtar‑değer çiftleridir. Çizim geometrisinde gösterilmezler ancak herhangi bir CAD‑bilgili uygulama tarafından erişilebilir, daha iyi veri yönetimi, otomatik raporlama ve PLM sistemleriyle entegrasyon sağlar.

## Why Use Aspose.CAD for This Task?

- **AutoCAD bağımlılığı yok** – herhangi bir işletim sistemi veya CI hattında çalışır.  
- **Tam özellikli API** – doğruluk kaybı olmadan okuma, değiştirme ve kaydetme.  
- **Yüksek performans** – büyük çizimleri saniyeler içinde işler.  
- **Çapraz format desteği** – aynı kod DXF, DWF ve diğerleri için çalışır.

## Prerequisites

- **Java Development Kit (JDK) 8+** yüklü ve IDE'nizde yapılandırılmış.  
- **Aspose.CAD for Java** kütüphanesi – en son JAR dosyasını [Aspose.CAD indirme sayfasından](https://releases.aspose.com/cad/java/) indirin.  
- Deneyimlemek için bir **örnek DWG/DXF dosyası** (öğreticide `conic_pyramid.dxf` kullanılır).

## Import Namespaces

Aspose.CAD nesneleriyle çalışabilmeniz için Java sınıfınıza gerekli importları ekleyin.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;

import java.util.Map;
```

## Step‑by‑Step Guide

### Step 1: Set Up Your Project

Yeni bir Maven/Gradle projesi (veya basit bir IDE projesi) oluşturun ve Aspose.CAD JAR dosyasını sınıf yoluna (classpath) yerleştirin. Bu, `com.aspose.cad.*` paketlerinin derleme zamanında kullanılabilir olmasını sağlar.

### Step 2: Define File Paths

Kaynak çizimin nerede bulunduğunu ve değiştirilmiş dosyanın nereye yazılacağını belirtin.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
String outFile = dataDir + "AddCustomProperties_out.dxf";
```

### Step 3: Load the DWG File

Çizimi bir `CadImage` nesnesine okumak için statik `Image.load` metodunu kullanın.

```java
CadImage cadImage = (CadImage)Image.load(srcFile);
```

### Step 4: Add Custom Properties

Meta verilerinizi doğrudan çizim başlığına ekleyin. Her çağrı yeni bir ad/değer çifti ekler.

```java
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_1", "Custom property test 1");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_2", "Custom property test 2");
cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_3", "Custom property test 3");
```

> **İpucu:** Özellik adlarını kısa tutun (maksimum 31 karakter) ve eski CAD görüntüleyicilerle uyumluluğu korumak için boşluklardan kaçının.

### Step 5: Save the Modified DWG File

Değişiklikleri `save` metodunu çağırarak kalıcı hale getirin. Çıktı dosyası artık eklediğiniz özel özellikleri içeriyor.

```java
cadImage.save(outFile);
```

### Step 6: Execute the Code

Programı IDE'nizden veya komut satırından çalıştırın. Her şey doğru şekilde ayarlandıysa bir onay mesajı göreceksiniz.

```java
System.out.println("\nAddCustomProperties executed successfully.");
```

## Common Issues & Solutions

| Problem | Likely Cause | Fix |
|---------|--------------|-----|
| **`java.lang.NoClassDefFoundError: com/aspose/cad/Image`** | Aspose.CAD JAR sınıf yolunda (classpath) bulunmuyor | JAR'ı projenizin `libs` klasörüne ekleyin veya Maven/Gradle içinde bildirin. |
| **Kaydedilen dosyada özellikler görünmüyor** | Özel özellikleri desteklemeyen bir DWG sürümü kullanmak | DWG/DXF sürümünün 2000 veya daha yeni olduğundan emin olun; eski formatlar özel başlıkları yok sayabilir. |
| **`OutOfMemoryError` on large files** | Akış (streaming) kullanmadan çok büyük bir çizim yüklemek | `Image.load` metodunu, bellek‑verimli yüklemeyi etkinleştiren bir `LoadOptions` nesnesiyle kullanın. |

## Frequently Asked Questions

**S: Diğer CAD dosya formatlarına özel özellikler ekleyebilir miyim?**  
C: Evet. Aspose.CAD for Java DXF, DWF, DGN ve daha fazlasını destekler ve aynı `getHeader().getCustomProperties()` API'si bu formatlarda çalışır.

**S: Aspose.CAD for Java tüm büyük IDE'lerle uyumlu mu?**  
C: Kesinlikle. Eclipse, IntelliJ IDEA, NetBeans ve hatta basit komut‑satırı derlemeleriyle çalışır.

**S: Daha fazla örnek ve ayrıntılı belgeleri nerede bulabilirim?**  
C: Tam sınıf, metod ve örnek proje listesi için resmi [Aspose.CAD Java API Referansına](https://reference.aspose.com/cad/java/) ziyaret edin.

**S: Aspose.CAD for Java'ı satın almadan deneyebilir miyim?**  
C: Evet—[Aspose.CAD indirme sayfasından](https://releases.aspose.com/) ücretsiz 30‑günlük deneme sürümünü indirebilirsiniz.

**S: Zorluklarla karşılaşırsam nasıl destek alabilirim?**  
C: Aspose topluluk forumu ve özel [Aspose.CAD destek portalı](https://forum.aspose.com/c/cad/19), soru sormak ve çözümler paylaşmak için harika yerlerdir.

---

**Son Güncelleme:** 2025-11-30  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}