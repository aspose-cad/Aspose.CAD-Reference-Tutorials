---
date: 2026-02-20
description: Aspose.CAD for Java kullanarak STL'yi PNG'ye nasıl dönüştüreceğinizi
  öğrenin. Bu adım adım kılavuz, STL dosyalarını verimli bir şekilde dışa aktarmayı
  gösterir.
linktitle: Export STL to PNG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java ile STL'yi PNG'ye Dönüştürme
url: /tr/java/cad-export-options/export-stl-to-png/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# STL'yi PNG'ye Dönüştürme Aspose.CAD for Java ile

## Giriş

Java uygulamasında **STL'yi PNG'ye dönüştürmeniz** gerekiyorsa, Aspose.CAD for Java işi hızlı ve güvenilir bir şekilde halleder. Bu öğreticide, projenizi kurmaktan son PNG görüntüsünü kaydetmeye kadar tüm süreci adım adım göstereceğiz—böylece STL dönüşümünü iş akışınıza güvenle entegre edebilirsiniz.

## Hızlı Yanıtlar
- **Kütüphane ne yapar?** CAD formatlarını (STL dahil) PNG gibi raster görüntülere dönüştürür.  
- **Hangi dil kullanılıyor?** Java, Aspose.CAD API ile.  
- **Lisans gerekli mi?** Üretim kullanımı için geçici ya da tam lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir dönüşüm için yaklaşık 10‑15 dakika.  
- **Görüntü boyutunu özelleştirebilir miyim?** Evet, `CadRasterizationOptions` aracılığıyla.

## STL'yi PNG'ye Dönüştürmek Nedir?

STL'yi PNG'ye dönüştürmek, bir 3‑B mesh dosyasını (STL) 2‑B raster görüntüye (PNG) çevirir. Bu, hızlı bir görsel önizleme, küçük resim oluşturma ya da modeli 3‑B görüntüleyici gerektirmeden web sayfalarına yerleştirme ihtiyacınız olduğunda faydalıdır.

## Neden Aspose.CAD for Java Kullanmalı?

- **Tam özellikli API** – Sadece STL değil, birçok CAD formatını işler.  
- **Harici bağımlılık yok** – Saf Java, herhangi bir Maven/Gradle projesine eklemesi kolay.  
- **Yüksek kaliteli raster çıktısı** – Çözünürlük, arka plan ve anti‑aliasing üzerinde kontrol.  
- **“STL nasıl dışa aktarılır” senaryolarını destekler** – Toplu işleme veya anlık dönüşümler için idealdir.

## Önkoşullar

Başlamadan önce, aşağıdakilere sahip olduğunuzdan emin olun:

- Makinenizde Java Development Kit (JDK) kurulu.  
- Aspose.CAD for Java kütüphanesini indirin. Bunu [buradan](https://releases.aspose.com/cad/java/) alabilirsiniz.  
- Geçerli bir lisans ya da geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) edinin.

## İsim Uzaylarını İçe Aktarma

Java projenizde gerekli sınıfları içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Şimdi, örneği birden fazla adıma ayıralım.

## Adım 1: Projenizi Kurun

Yeni bir Java projesi oluşturun ve Aspose.CAD for Java kütüphanesini projenizin bağımlılıklarına ekleyin (Maven, Gradle veya manuel JAR ekleme).

## Adım 2: STL Dosyanızı Belirleyin

Dönüştürmek istediğiniz STL dosyasının yolunu tanımlayın:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## Adım 3: STL Dosyasını Yükleyin

`Image.load` yöntemiyle STL dosyasını yükleyin. Bu, rasterleştirebileceğiniz bir **CAD image** nesnesi oluşturur:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## Adım 4: Rasterleştirme Seçeneklerini Yapılandırın

Çıktı PNG'nin boyut ve kalitesini kontrol etmek için rasterleştirme seçeneklerini ayarlayın. Bu seçenekler **cad image to png** dönüşüm sürecinin bir parçasıdır:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## Adım 5: PNG Seçeneklerini Yapılandırın

`PngOptions` örneği oluşturun. Rasterleştirme ayarlarını uygulamak istiyorsanız, aşağıdaki satırın yorumunu kaldırın:

```java
PngOptions pngOptions = new PngOptions();
// Uncomment the line below if you want to set vector rasterization options
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## Adım 6: PNG Olarak Kaydedin

Son olarak, CAD görüntüsünü bir PNG dosyasına dışa aktarın—bu **save PNG Java** adımıdır:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

> **Pro ipucu:** Daha hızlı işleme için `PageWidth` ve `PageHeight` değerlerini istediğiniz küçük resim boyutlarına göre ayarlayın.

Tebrikler! Aspose.CAD for Java kullanarak bir STL dosyasını başarıyla **PNG'ye dönüştürdünüz**.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Sebep | Çözüm |
|-------|-------|-------|
| Boş PNG çıktısı | Rasterleştirme seçenekleri ayarlanmamış | `pngOptions.setVectorRasterizationOptions(vectorOptions);` satırının yorumunu kaldırın veya bir arka plan rengi belirtin |
| Büyük STL dosyalarında OutOfMemoryError | Yetersiz yığın (heap) belleği | JVM yığınını artırın (`-Xmx2g`) veya dosyayı parçalara bölerek işleyin |
| LicenseException | Geçerli lisans yok | Görüntüyü yüklemeden önce geçici ya da satın alınmış bir lisans uygulayın |

## Sıkça Sorulan Sorular

### Q1: Aspose.CAD for Java tüm STL dosya sürümleriyle uyumlu mu?
A1: Aspose.CAD for Java çeşitli STL dosya sürümlerini destekler, çoğu yaygın formatla uyumluluğu sağlar.

### Q2: Aspose.CAD for Java'ı ticari bir projede kullanabilir miyim?
A2: Evet, kullanabilirsiniz. Tek yapmanız gereken [buradan](https://purchase.aspose.com/buy) geçerli bir lisans almaktır.

### Q3: Ücretsiz deneme için geçici lisansa ihtiyacım var mı?
A3: Hayır, ücretsiz deneme için geçici lisans gerekmez. Deneme sürümüyle hemen başlayabilirsiniz [buradan](https://releases.aspose.com/).

### Q4: Ek destek nereden bulabilirim ya da soru sorabilirim?
A4: Herhangi bir destek veya soru için Aspose.CAD forumunu [buradan](https://forum.aspose.com/c/cad/19) ziyaret edin.

### Q5: Kapsamlı bir dokümantasyon mevcut mu?
A5: Evet, dokümantasyonu [buradan](https://reference.aspose.com/cad/java/) bulabilirsiniz.

## Sonuç

Bu rehberde, Aspose.CAD for Java kullanarak **STL'yi PNG'ye** verimli bir şekilde nasıl dönüştüreceğinizi gösterdik. Yukarıdaki adımları izleyerek, STL‑to‑PNG dönüşümünü herhangi bir Java tabanlı iş akışına entegre edebilirsiniz; ister bir masaüstü yardımcı programı, bir web servisi ya da otomatik raporlama aracı geliştirin.

---

**Son Güncelleme:** 2026-02-20  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}