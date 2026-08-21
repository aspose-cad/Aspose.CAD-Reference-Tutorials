---
date: 2026-04-23
description: Aspose.CAD for Java kullanarak DWG'yi PNG'ye dönüştürmeyi ve CAD'i PNG
  olarak kaydetmeyi öğrenin; DWG, DXF ve diğer CAD dosyalarını verimli bir şekilde
  raster görüntülere dönüştürün.
keywords:
- convert dwg to png
- save cad as png
- cad to png conversion
linktitle: CAD Çizimini Raster Görüntü Formatına Dönüştür
second_title: Aspose.CAD Java API
title: DWG'yi PNG'ye Dönüştür – Aspose.CAD for Java Kullanarak CAD'i PNG Olarak Kaydet
url: /tr/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi PNG'ye Dönüştür – Aspose.CAD for Java Kullanarak CAD'i PNG Olarak Kaydet

## Giriş

Bu öğreticide, Aspose.CAD for Java kullanarak **convert DWG to PNG** nasıl yapılacağını öğreneceksiniz. CAD çizimlerini PNG gibi raster görüntü formatlarına dönüştürmek, web ön izlemeleri, dokümantasyon ve raporlama için sıkça ihtiyaç duyulan bir gereksinimdir. Aspose.CAD, DWG, DXF, DWF ve birçok diğer CAD dosya türü için **cad to png conversion** sağlam bir, yüksek performanslı bir yol sunar.

## Hızlı Yanıtlar
- **Dönüşümü hangi kütüphane yönetir?** Aspose.CAD for Java.  
- **DWG'yi PNG'ye dönüştürebilir miyim?** Evet – aynı API DWG, DXF ve diğer formatlar için çalışır.  
- **Üretim için lisansa ihtiyacım var mı?** Değerlendirme dışı kullanım için ticari bir lisans gereklidir.  
- **Raster boyutu yapılandırılabilir mi?** Kesinlikle – sayfa genişliği, yüksekliği ve DPI'yi rasterizasyon seçenekleriyle ayarlayabilirsiniz.  
- **Dönüşüm ne kadar sürer?** Standart çizimler için genellikle bir saniyenin altında; daha büyük dosyalar daha uzun sürebilir.

## Aspose.CAD Kullanarak DWG'yi PNG'ye Nasıl Dönüştürülür

CAD'i PNG olarak kaydetmek, vektör tabanlı CAD verilerini piksel tabanlı bir görüntüye (PNG) rasterleştirmek anlamına gelir. Bu süreç, genellikle **convert dwg to raster** olarak adlandırılır, görsel doğruluğu korurken web sayfalarına, e-postalara veya raporlara kolayca yerleştirilebilen bir format oluşturur.

## Aspose.CAD for Java Neden Kullanılmalı?

- **Geniş format desteği** – DWG, DXF, DWF ve daha fazlası ile çalışır.  
- **Harici bağımlılık yok** – saf Java, yerel DLL'ler yok.  
- **İnce ayarlı kontrol** – çözünürlüğü, arka plan rengini ve render kalitesini özelleştirin.  
- **Ölçeklenebilir performans** – toplu işleme veya anlık dönüşüm için uygundur.  
- **CAD'i nasıl kaydedilir** – API, sadece birkaç satır kodla **save CAD as PNG** yapmanıza olanak tanır.

## Önkoşullar

Öğreticiye başlamadan önce, aşağıdaki önkoşulların yerine getirildiğinden emin olun:

1. **Java Development Environment** – çalışan bir JDK (8 veya daha yeni) ve seçtiğiniz bir IDE veya derleme aracı.  
2. **Aspose.CAD Library** – Aspose.CAD for Java kütüphanesini projenize indirin ve entegre edin. Kütüphaneyi [here](https://releases.aspose.com/cad/java/) adresinde bulabilirsiniz.

## Ad Alanlarını İçe Aktarın

Java kodunuzda, Aspose.CAD for Java işlevlerini etkili bir şekilde kullanmak için gerekli ad alanlarını içe aktarın. Bu adım, gerekli sınıflara ve yöntemlere erişim için kritiktir.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Şimdi, bir CAD çizimini raster görüntüye dönüştürme sürecini ayrıntılı adımlara ayıralım:

## Adım 1: CAD Çizimini Yükle

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Bu adımda, belirtilen dosya yolundan `Image.load()` yöntemiyle CAD çizimini yüklüyoruz.

## Adım 2: Rasterizasyon Seçeneklerini Ayarla

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

`CadRasterizationOptions` sınıfının bir örneğini oluşturun ve rasterleştirilmiş görüntü için sayfa genişliğini ve yüksekliğini ayarlayın.

## Adım 3: Görüntü Seçeneklerini Oluştur

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

Sonuç görüntüsü için bir `PngOptions` örneği oluşturun ve vektör rasterizasyon seçeneklerini ayarlayın.

## Adım 4: Raster Görüntüyü Kaydet

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

`image.save()` yöntemiyle oluşan raster görüntüyü belirtilen dizine kaydedin.

Bu adımları belirli CAD dosyalarınız için tekrarlayın ve **converted CAD drawing image** başarıyla PNG'ye dönüştürülmüş olacaktır.

## Ortak Kullanım Senaryoları ve İpuçları

- **Web ön izleme oluşturma** – Büyük DWG dosyalarını hızlı tarayıcı gösterimi için hafif PNG küçük resimlerine dönüştürün.  
- **Rapor gömme** – Vektör CAD dosyalarının desteklenmediği PDF veya Word raporlarında PNG çıktısını kullanın.  
- **Toplu dönüşüm** – Bir klasördeki CAD dosyaları üzerinde döngü yaparak tutarlı çıktı için aynı rasterizasyon ayarlarını uygulayın.  
- **Pro ipucu:** Yüksek çözünürlüklü baskılar için DPI'yi artırmak amacıyla `rasterizationOptions.setResolution()`'ı ayarlayın.  
- **DWG'yi nasıl dönüştürürsünüz** – aynı rasterizasyon ayarlarını koruyarak `PngOptions`'ı diğer görüntü seçenekleriyle (ör. `JpegOptions`) değiştirerek çıktı formatını da değiştirebilirsiniz.

## Sonuç

Yukarıdaki adımları izleyerek, kolayca **convert DWG to PNG**, **save CAD as PNG** yapabilir veya ihtiyacınız olan herhangi bir **cad to png conversion** gerçekleştirebilirsiniz. Aspose.CAD for Java API, süreci basitleştirir ve çözünürlük, arka plan rengi ve çıktı formatı üzerinde tam kontrol sağlar—web ön izlemeleri, dokümantasyon veya toplu işleme hatları için mükemmeldir.

## Sıkça Sorulan Sorular

**S: DWG dosyasını özel bir arka plan rengiyle PNG'ye nasıl dönüştürürüm?**  
Cevap: `PngOptions` örneğini oluşturmadan önce `CadRasterizationOptions` üzerindeki `backgroundColor` özelliğini ayarlayın.

**S: Birden fazla CAD dosyasını tek bir toplu işlemde dönüştürmek mümkün mü?**  
Cevap: Evet—yükleme, rasterizasyon ve kaydetme adımlarını dosya koleksiyonunuz üzerinde dönen bir döngü içinde sarın.

**S: Varsayılan ayarlardan hangi görüntü kalitesini bekleyebilirim?**  
Cevap: Varsayılan DPI (96) ekran kalitesinde PNG'ler üretir; baskı kalitesinde sonuçlar için DPI'yi artırın.

**S: Aspose.CAD, PNG çıktısında şeffaf arka planları destekliyor mu?**  
Cevap: Kesinlikle. Varsayılan olarak PNG'ler alfa kanalıyla kaydedilir; rasterizasyon seçeneklerinde şeffaf bir arka plan da belirtebilirsiniz.

**S: CAD dosyalarını JPEG veya BMP gibi diğer raster formatlara dönüştürebilir miyim?**  
Cevap: Evet—aynı rasterizasyon ayarlarını koruyarak `PngOptions`'ı `JpegOptions` veya `BmpOptions` ile değiştirin.

---

**Son Güncelleme:** 2026-04-23  
**Test Edilen:** Aspose.CAD for Java 24.12 (latest)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}