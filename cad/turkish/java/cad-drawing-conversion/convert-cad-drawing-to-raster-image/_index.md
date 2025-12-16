---
date: 2025-12-16
description: Aspose.CAD for Java ile CAD'i PNG'ye nasıl dönüştüreceğinizi öğrenin;
  DWG'yi görüntüye dışa aktarma, CAD'i PNG olarak kaydetme ve CAD'i raster görüntü
  seçeneklerini kapsar.
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java Kullanarak CAD'i PNG'ye Dönüştürme
url: /tr/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java Kullanarak CAD'i PNG'ye Dönüştürme

## Hızlı Yanıtlar
- **Ana amaç nedir?** CAD çizimlerini PNG raster görüntülerine dönüştürmek.  
- **Hangi kütüphane kullanılıyor?** Aspose.CAD for Java.  
- **Lisans gerekli mi?** Ücretsiz deneme mevcuttur; üretim kullanımı için lisans gereklidir.  
- **Görüntü boyutunu özelleştirebilir miyim?** Evet, `CadRasterizationOptions` ile genişlik ve yükseklik ayarlanabilir.  
- **Desteklenen CAD formatları?** DWG, DXF, DWF ve daha fazlası.

## “CAD'i PNG'ye dönüştürmek” ne anlama geliyor?
CAD'i PNG'ye dönüştürmek, vektör tabanlı CAD içeriğini (DWG, DXF vb.) piksel tabanlı bir görüntü formatına rasterleştirmek demektir. PNG, şeffaflığı ve kayıpsız kalitesi sayesinde web ön izlemeleri, dokümantasyon ve raporlamalar için idealdir.

## Neden CAD'i PNG'ye (CAD'den raster görüntüye) dönüştürmeliyiz?
- **Evrensel görüntüleme:** PNG, özel CAD görüntüleyicileri olmadan herhangi bir cihazda çalışır.  
- **Hızlı yükleme:** Raster görüntüler web sayfalarında anında yüklenir.  
- **Kolay gömme:** PNG'leri PDF, Word belgeleri veya sunum slaytlarına ekleyin.  
- **Tutarlı görünüm:** Çizgi kalınlıkları, renkler ve katmanlar tasarlandığı gibi korunur.

## Önkoşullar
Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Geliştirme Ortamı** – JDK 8 ve üzeri yüklü ve yapılandırılmış.  
2. **Aspose.CAD Kütüphanesi** – Kütüphaneyi indirin ve projenize ekleyin. Kütüphaneyi **[burada](https://releases.aspose.com/cad/java/)** bulabilirsiniz.

## İsim Uzaylarını İçe Aktarın
Aspose.CAD nesneleriyle çalışabilmek için Java sınıfınıza gerekli içe aktarmaları ekleyin.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Adım Adım CAD'i PNG'ye Dönüştürme Kılavuzu

### Adım 1: CAD Çizimini Yükleyin
Öncelikle `Image.load()` kullanarak kaynak CAD dosyasını (DXF, DWG vb.) yükleyin.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

> **Pro ipucu:** Yol sorunlarından kaçınmak için CAD dosyalarınızı ayrı bir klasörde (ör. `CADConversion`) tutun.

### Adım 2: Rasterleştirme Seçeneklerini Ayarlayın (dwg'yi görüntüye dışa aktar)
Çıktı görüntü boyutunu ve diğer raster ayarlarını tanımlayın.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

İsterseniz burada arka plan rengini, çizgi render modunu ve DPI değerini de kontrol edebilirsiniz.

### Adım 3: Görüntü Seçeneklerini Oluşturun (cad'i png olarak kaydedin)
Bir `PngOptions` örneği oluşturun ve rasterleştirme ayarlarını ekleyin.

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### Adım 4: Raster Görüntüyü Kaydedin (cad dosyasını png'ye)
Son olarak PNG dosyasını diske yazın.

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

Oluşan `conic_pyramid_raster_image_out.png` dosyası, orijinal CAD çiziminizin yüksek çözünürlüklü PNG temsili olacaktır.

### Diğer Dosyalar İçin Tekrarlayın
Başka bir CAD dosyasına işaret etmek için sadece `srcFile` değerini değiştirin ve aynı adımları çalıştırın. Aynı kod DWG, DWF ve diğer desteklenen formatlar için de geçerlidir.

## Yaygın Sorunlar ve Çözümler
| Sorun | Çözüm |
|-------|----------|
| **Boş PNG çıktısı** | Kaynak CAD dosyasının doğru yüklendiğini doğrulayın (`Image.load()` bir hata atmamalı). |
| **Yanlış boyutlar** | `PageWidth` / `PageHeight` değerlerini ayarlayın veya DPI'yi `rasterizationOptions.setResolution(...)` ile belirleyin. |
| **Katmanlar eksik** | CAD dosyasının katmanlarının gizli olmadığından emin olun; `CadRasterizationOptions.setDrawType(CadDrawTypeMode.Vector);` kullanın. |
| **Lisans hataları** | Geçerli bir Aspose.CAD lisans dosyası kullanın (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |

## Sıkça Sorulan Sorular

**S1: Aspose.CAD tüm CAD formatlarıyla uyumlu mu?**  
C1: Aspose.CAD, DWG, DXF, DWF ve daha fazlası dahil olmak üzere geniş bir CAD formatı yelpazesini destekler. Tam liste için **[belgelere](https://reference.aspose.com/cad/java/)** bakın.

**S2: Rasterleştirme seçeneklerini özel ihtiyaçlarıma göre özelleştirebilir miyim?**  
C2: Evet, Aspose.CAD rasterleştirme seçeneklerini ayarlama esnekliği sunar; böylece çıktıyı boyut, DPI, arka plan rengi vb. gereksinimlerinize göre şekillendirebilirsiniz.

**S3: Aspose.CAD‑ile ilgili sorular için nereden destek alabilirim?**  
C3: Yardım almak ve toplulukla etkileşimde bulunmak için **[Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19)** ziyaret edin.

**S4: Aspose.CAD for Java için ücretsiz deneme mevcut mu?**  
C4: Evet, ücretsiz bir deneme **[buradan](https://releases.aspose.com/)** elde ederek Aspose.CAD özelliklerini keşfedebilirsiniz.

**S5: Aspose.CAD for Java nasıl satın alınır?**  
C5: Aspose.CAD for Java satın almak için **[satın alma sayfasını](https://purchase.aspose.com/buy)** ziyaret edin.

---

**Son Güncelleme:** 2025-12-16  
**Test Edilen:** Aspose.CAD for Java 24.11 (yazım anındaki en yeni sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}