---
date: 2026-01-07
description: Aspose.CAD for Java ile CAD'i SVG'ye nasıl dışa aktaracağınızı öğrenin.
  Bu adım adım rehber, DWG'yi SVG'ye dönüştürmeyi, SVG renk modunu ayarlamayı ve kütüphaneyi
  Java projenize entegre etmeyi gösterir.
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java kullanarak CAD'i SVG'ye dışa aktar
url: /tr/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java Kullanarak CAD'i SVG Olarak Dışa Aktarma

## Giriiş

Aspose.CAD for Java hoş geldiniz, geliştiricilerin CAD çizimlerini kolayca manipüle etmelerini sağlayan güçlü bir kütüphane. Programın bir geliştiricisi olun ister CAD performansının yeni adım atıyor olun, bu özet kılavuzu **CAD'i SVG'ye aktarın** işlem adım adım adım gösterimi DWG'yi SVG'ye nasıl dönüştüreceğinizi, SVG renk modunu nasıl ayarlayacağınızı ve API'yi Java projenize nasıl entegre edeceğini anlatacak.

## Hızlı Yanıtlar
- **“CAD'i SVG'ye aktar” ne anlaşılıyor?** Bir CAD çizimini (ör. DWG) tarayıcılarda görüntülenebilen Ölçeklenebilir Vektör Grafikleri dosyasına kaydedilebilir.
- **Dönüşümü hangi paketi gerçekleştiriyor?** Aspose.CAD for Java bu görev için basit bir API sağlar.
- **Geliştirme için lisansa ihtiyacınız var mı?** Test için ücretsiz deneme sürümü yeterlidir; üretim için ticari lisans gereklidir.
- **SVG renk çıkışını kontrol edebilir miyim?** Evet, SVG renk modunu (ör.gri tonlama) ayarlayabilirsiniz.
- **Ek bir yazılım gerekiyor mu?** Yalnızca bir Java runtime ve Aspose.CAD JAR dosyası yeterlidir.

## Önkoşullar

Bu eğitimi almadan önce aşağıdaki önkoşulları karşıladığınızdan emin olun:

- Java Geliştirme Ortamı: Sisteminizde Java yüklü olduğundan emin olun.
- Aspose.CAD Kütüphanesi: Aspose.CAD for Java kütüphanesini [indirme bağlantısı](https://releases.aspose.com/cad/java/) adresinden indirilir ve yüklenir.
- Belge Dizini: CAD çizimleriniz için bir dizin oluşturma ve yol edinmeyin.

## Ad Alanlarını İçe Aktar

Bu sürenin uzatılması, Aspose.CAD yolculuğumuza başlamak için gerekli reklam alanlarını (ad alanlarını) içeri aktaracağız. Aşağıdaki adımları izleyin:

### Adım 1: Java Projenizi Açın
Seçtiğiniz IDE'de Java projenizi açın.

### Adım 2: Aspose.CAD Kitaplığını Ekleyin
Aspose.CAD kütüphanesini projenize ekleyin. Bunu, JAR kredilerinizi projenizin ilişkilerine dahil ederek yapabilirsiniz.

### 3. Adım: Ad Alanlarını İçe Aktarın
Java sınıfınızda gerekli ad alanlarını içe aktarın:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## CAD Dosyasını SVG'ye Aktarma

Artık sahneyi hazırladığımıza göre, Aspose.CAD for Java kullanarak **export CAD to SVG** işleminin adım adım sürecine dalalım.

### Adım 1: Kaynak Dizinini Belirtin
CAD çizimlerinizin bulunduğu kaynak dizinin yolunu tanımlayın:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Adım 2: CAD Çizimini Yükleyin
Aspose.CAD kütüphanesini kullanarak CAD çizimini yükleyin:

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Adım 3: SVG Dışa Aktarma Seçeneklerini Yapılandırın
SVG dışa aktarma seçeneklerini özelleştirerek çıktıyı yapılandırın. Burada **set SVG color mode** ayarını grayscale (gri tonlamalı) olarak belirliyor ve metni şekillere dönüştürmesini sağlıyoruz:

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### Adım 4: SVG Olarak Kaydedin
CAD çizimini bir SVG dosyası olarak kaydedin:

```java
image.save(dataDir + "meshes.svg");
```

> **İpucu:** Renkleri koru **convert DWG to SVG** yapılması gerekiyorsa, `SvgColorMode.Grayscale` değeri `SvgColorMode.FullColor` olarak onaylanmıştır.

Tebrikler! Aspose.CAD for Java kullanarak bir CAD çizimini başarıyla SVG olarak düzenlediniz.

## CAD'yi SVG'ye Aktarmak için Neden Aspose.CAD Kullanılmalı?
- **Yüksek doğruluk:** Vektör verileri korunur, böylece SVG orijinal CAD çizimiyle tam olarak aynı görünür.
- **Dışa bağımlılık yok:** Dönüşüm tamamen Java içinde gerçekleşiyor, ek araçlara ihtiyaç duyulmuyor.
- **Özelleştirilebilir çıktı:** `setColorType` gibi seçeneklerle SVG'nin gri tonlamalı mı yoksa tam renkli mi genişlemeyi kontrol edebilirsiniz.

## Yaygın Sorunlar ve Çözümler
- **Dosya bulunamadı:** `dataDir` değişkeninin doğru klasörde işaretlendiğini ve DWG dosyası adının eşleştiğini doğrulayın.
- **Boş SVG çıktısı:** Çizimde metin şekli olarak görünmesi ise `options.setTextAsShapes(true)` ayarını yaptığınızdan emin olun.
- **Desteklenmeyen CAD formatı:** Aspose.CAD DWG, DXF, DWF ve birkaç başka formatı desteklemek; tam liste için belgeleri inceleyin.

## Çözüm

Bu öğreticide, Aspose.CAD for Java kullanarak **export CAD to SVG** sürecini sorunsuz bir şekilde nasıl gerçekleştireceğinizi inceledik. Sezgisel API'si ve güçlü özellikleri sayesinde Aspose.CAD, karmaşık görevleri basitleştirerek geliştiricilere çok yönlü bir CAD manipülasyon aracı sunar.

## Sıkça Sorulan Sorular

**S: Aynı kodu kullanarak bir DXF dosyasını SVG'ye dönüştürebilir miyim?**  
C: Evet, dosya adını bir DXF dosyasıyla değiştirmeniz yeterlidir; API her iki formatı da işler.

**S: Çıktıyı tam renkli SVG olarak nasıl değiştiririm?**  
C: Kaydetmeden önce `options.setColorType(SvgColorMode.FullColor);` satırını ekleyin.

**S: Oluşturulan SVG'ye fontları gömmek mümkün mü?**  
C: Aspose.CAD şu anda metni şekillere dönüştürür; font gömme gereksinimi yoktur.

**S: Kütüphane Linux ve macOS'ta çalışıyor mu?**  
C: Java kütüphanesi platform bağımsızdır ve uyumlu bir JVM bulunduğu her yerde çalışır.

**S: Bu öğreticide hangi Aspose.CAD sürümü kullanıldı?**  
C: Örnek, Aspose.CAD for Java 24.10 sürümü ile test edilmiştir.

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
