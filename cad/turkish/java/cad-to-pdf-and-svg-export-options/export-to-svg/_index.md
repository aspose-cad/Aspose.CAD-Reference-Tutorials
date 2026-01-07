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

## Introduction

Aspose.CAD for Java dünyasına hoş geldiniz, geliştiricilerin CAD çizimlerini kolayca manipüle etmelerini sağlayan güçlü bir kütüphane. İster deneyimli bir geliştirici olun ister CAD dünyasına yeni adım atıyor olun, bu kapsamlı kılavuz **export CAD to SVG** işlemini adım adım göstererek DWG'yi SVG'ye nasıl dönüştüreceğinizi, SVG renk modunu nasıl ayarlayacağınızı ve API'yi Java projenize nasıl entegre edeceğinizi anlatacak.

## Quick Answers
- **“export CAD to SVG” ne anlama geliyor?** Bir CAD çizimini (ör. DWG) tarayıcılarda görüntülenebilen Scalable Vector Graphics dosyasına dönüştürür.  
- **Dönüşümü hangi kütüphane gerçekleştiriyor?** Aspose.CAD for Java bu görev için basit bir API sağlar.  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü yeterlidir; üretim için ticari lisans gereklidir.  
- **SVG renk çıktısını kontrol edebilir miyim?** Evet, SVG renk modunu (ör. grayscale) ayarlayabilirsiniz.  
- **Ek bir yazılım gerekiyor mu?** Sadece bir Java runtime ve Aspose.CAD JAR dosyası yeterlidir.

## Prerequisites

Bu öğreticiye başlamadan önce aşağıdaki önkoşulları karşıladığınızdan emin olun:

- Java Geliştirme Ortamı: Sisteminizde Java yüklü olduğundan emin olun.  
- Aspose.CAD Kütüphanesi: Aspose.CAD for Java kütüphanesini [download link](https://releases.aspose.com/cad/java/) adresinden indirin ve kurun.  
- Belge Dizini: CAD çizimleriniz için bir dizin oluşturun ve yolunu not edin.

## Import Namespaces

Bu adımda, Aspose.CAD yolculuğumuza başlamak için gerekli ad alanlarını (namespaces) içe aktaracağız. Aşağıdaki adımları izleyin:

### Step 1: Open Your Java Project
Seçtiğiniz IDE'de Java projenizi açın.

### Step 2: Add Aspose.CAD Library
Aspose.CAD kütüphanesini projenize ekleyin. Bunu, JAR dosyasını projenizin bağımlılıklarına dahil ederek yapabilirsiniz.

### Step 3: Import Namespaces
Java sınıfınızda gerekli ad alanlarını içe aktarın:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## Export CAD to SVG

Artık sahneyi hazırladığımıza göre, Aspose.CAD for Java kullanarak **export CAD to SVG** işleminin adım adım sürecine dalalım.

### Step 1: Specify the Resource Directory
CAD çizimlerinizin bulunduğu kaynak dizinin yolunu tanımlayın:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Step 2: Load the CAD Drawing
Aspose.CAD kütüphanesini kullanarak CAD çizimini yükleyin:

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Step 3: Configure SVG Export Options
SVG dışa aktarma seçeneklerini özelleştirerek çıktıyı yapılandırın. Burada **set SVG color mode** ayarını grayscale (gri tonlamalı) olarak belirliyor ve metni şekillere dönüştürmesini sağlıyoruz:

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### Step 4: Save as SVG
CAD çizimini bir SVG dosyası olarak kaydedin:

```java
image.save(dataDir + "meshes.svg");
```

> **İpucu:** Renkleri koruyarak **convert DWG to SVG** yapmanız gerekiyorsa, `SvgColorMode.Grayscale` değerini `SvgColorMode.FullColor` olarak değiştirin.

Tebrikler! Aspose.CAD for Java kullanarak bir CAD çizimini başarıyla SVG olarak dışa aktardınız.

## Why Use Aspose.CAD to Export CAD to SVG?
- **High fidelity:** Vektör verileri korunur, böylece SVG orijinal CAD çizimiyle tam olarak aynı görünür.  
- **No external dependencies:** Dönüşüm tamamen Java içinde gerçekleşir, ek araçlara ihtiyaç duyulmaz.  
- **Customizable output:** `setColorType` gibi seçeneklerle SVG'nin gri tonlamalı mı yoksa tam renkli mi olacağını kontrol edebilirsiniz.

## Common Issues and Solutions
- **File not found:** `dataDir` değişkeninin doğru klasöre işaret ettiğini ve DWG dosya adının eşleştiğini doğrulayın.  
- **Blank SVG output:** Çizimde metin şekil olarak görünmeli ise `options.setTextAsShapes(true)` ayarını yaptığınızdan emin olun.  
- **Unsupported CAD format:** Aspose.CAD DWG, DXF, DWF ve birkaç başka formatı destekler; tam liste için belgeleri inceleyin.

## Conclusion

Bu öğreticide, Aspose.CAD for Java kullanarak **export CAD to SVG** sürecini sorunsuz bir şekilde nasıl gerçekleştireceğinizi inceledik. Sezgisel API'si ve güçlü özellikleri sayesinde Aspose.CAD, karmaşık görevleri basitleştirerek geliştiricilere çok yönlü bir CAD manipülasyon aracı sunar.

## SSS

### Q1: Aspose.CAD for Java'yi diğer CAD formatlarıyla da kullanabilir miyim?

A1: Evet, Aspose.CAD DWG, DXF, DWF ve daha fazlası dahil olmak üzere çeşitli CAD formatlarını destekler.

### Q2: Aspose.CAD hem yeni başlayanlar hem de deneyimli geliştiriciler için uygun mu?

A2: Kesinlikle! Aspose.CAD kullanıcı dostu bir API sunar; bu sayede yeni başlayanlar rahatça kullanabilir, deneyimli geliştiriciler ise gelişmiş özelliklerden faydalanabilir.

### Q3: Ek destek veya topluluk tartışmalarını nerede bulabilirim?

A3: Destek ve tartışmalar için [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

### Q4: Ücretsiz bir deneme sürümü mevcut mu?

A4: Evet, bir [free trial](https://releases.aspose.com/) ile Aspose.CAD'i keşfedebilirsiniz.

### Q5: Aspose.CAD for Java için lisans nasıl satın alınır?

A5: Lisansı [purchase page](https://purchase.aspose.com/buy) üzerinden satın alabilirsiniz.

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

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose