---
date: 2026-01-10
description: Aspose.CAD for Java kullanarak DGN dosyalarından JPEG oluşturmayı öğrenin.
  Bu adım adım öğretici, DGN'yi JPEG'ye verimli bir şekilde nasıl dönüştüreceğinizi
  gösterir.
linktitle: Exporting DGN in AutoCAD Format to Raster Image Format
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java kullanarak DGN'den JPEG nasıl oluşturulur
url: /tr/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java kullanarak DGN'den JPEG oluşturma

## Giriş

Bu kapsamlı rehberde sadece birkaç satır Java kodu ile **DGN dosyalarından JPEG oluşturacaksınız**. İster toplu dönüşüm aracı geliştirin, ister CAD çizimlerini web‑dostu görüntüler olarak göstermeniz gereksin, DGN'yi JPEG'ye dönüştürmek birçok mühendislik ve tasarım iş akışı için yaygın bir gereksinimdir. Aspose.CAD kütüphanesini kurmaktan son raster görüntüyü kaydetmeye kadar her adımı adım adım göstereceğiz; böylece çözümü hemen kendi uygulamalarınıza entegre edebilirsiniz.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.CAD for Java  
- **Diğer CAD formatlarını JPEG'ye dönüştürebilir miyim?** Evet, Aspose.CAD birçok formatı destekler (ikincil anahtar kelime *convert cad to jpeg*).  
- **Üretim ortamında lisans gerekli mi?** Deneme dışı kullanım için ticari bir lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** Java 8 veya üzeri  
- **Tipik bir dönüşüm ne kadar sürer?** Standart‑boyutlu çizimler için genellikle bir saniyenin altında  

## “DGN'den JPEG oluşturma” nedir?
DGN dosyasından JPEG oluşturmak, vektör‑tabanlı DGN çizimini piksel‑tabanlı bir görüntüye (JPEG) rasterleştirmek anlamına gelir. Bu işlem görsel sadakati korurken, tarayıcılar, e‑postalar veya raporlar içinde CAD yazılımına ihtiyaç duymadan görüntülenebilen hafif bir dosya üretir.

## Neden DGN'yi JPEG'ye dönüştürmeliyiz?
- **Kolay paylaşım:** JPEG'ler herhangi bir cihazda evrensel olarak görüntülenebilir.  
- **Performans:** Raster görüntüler, web sayfalarında vektör CAD dosyalarından daha hızlı yüklenir.  
- **Uyumluluk:** Birçok sonraki araç (ör. raporlama motorları) yalnızca raster formatları kabul eder.  

## Önkoşullar

Başlamadan önce aşağıdakilerin kurulu olduğundan emin olun:

1. **Aspose.CAD Kütüphanesi** – Resmi siteden **[buradan](https://releases.aspose.com/cad/java/)** indirin.  
2. **Java Development Kit (JDK)** – Java 8 veya daha yeni bir sürüm makinenizde yüklü olmalı.  
3. **IDE** – IntelliJ IDEA, Eclipse gibi herhangi bir Java‑uyumlu IDE.

## Paketleri İçe Aktarma

Java sınıfınıza gerekli importları ekleyin:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Adım‑Adım Kılavuz

### Adım 1: DGN Dosyasını Yükleyin

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

*Açıklama:* `Image.load` yöntemi kaynak DGN dosyasını okur ve daha sonra rasterleştirebileceğimiz bir `DgnImage` nesnesi döndürür.

### Adım 2: Bir JpegOptions Nesnesi Oluşturun

```java
ImageOptionsBase options = new JpegOptions();
```

*Açıklama:* `JpegOptions`, Aspose.CAD'e çıktı formatının JPEG olacağını bildirir. Aynı zamanda rasterleştirme ayarlarını eklememizi sağlar.

### Adım 3: Rasterleştirme Ayarlarını Yapılandırın

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

*Açıklama:* Bu seçenekler, ortaya çıkan görüntünün boyutunu tanımlar ve ölçekleme davranışını kontrol eder. Hedef çözünürlüğünüze göre `PageWidth` ve `PageHeight` değerlerini ayarlayın.

### Adım 4: Dönüştürülmüş Görüntüyü Kaydedin

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

*Açıklama:* `save` yöntemi rasterleştirilmiş JPEG'i belirtilen çıktı akışına yazar. Bu adımdan sonra kullanıma hazır bir JPEG dosyanız olur.

> **Pro ipucu:** Dönüştürme kodunu bir try‑with‑resources bloğu içinde tutarak akışların otomatik olarak kapanmasını sağlayın.

## Ortak Kullanım Senaryoları

- **Küçük önizleme resimleri** oluşturma, CAD dosya tarayıcıları için.  
- **Çizimleri PDF raporlarına veya HTML sayfalara** gömme.  
- **Otomatik toplu işleme** ile tasarım arşivlerini dönüştürme.

## Sorun Giderme ve Yaygın Tuzaklar

| Sorun | Neden | Çözüm |
|-------|-------|------|
| Boş veya beyaz çıktı görüntüsü | Yanlış rasterleştirme seçenekleri (ör. `NoScaling` true ve sayfa boyutu uyumsuz) | `PageWidth`/`PageHeight` ayarlayın veya `NoScaling` değerini false yapın |
| Büyük DGN dosyalarında bellek hatası | Çok büyük dosyalar akışsız yüklendi | JVM yığın boyutunu (`-Xmx`) artırın veya dosyaları daha küçük parçalar halinde işleyin |
| JPEG kalitesi yetersiz | Varsayılan JPEG kalitesi düşük | Kaydetmeden önce `((JpegOptions)options).setQuality(100);` kullanın |

## Sık Sorulan Sorular

### S1: Aspose.CAD for Java'yi diğer CAD dosya formatlarıyla kullanabilir miyim?

C1: Evet, Aspose.CAD geniş bir format yelpazesini destekler; **CAD'ı JPEG'ye** ve birçok başka raster ya da vektör çıktısına dönüştürebilirsiniz.

### S2: Aspose.CAD for Java için ücretsiz bir deneme sürümü var mı?

C2: Evet, ücretsiz deneme sürümüne **[buradan](https://releases.aspose.com/)** ulaşabilirsiniz.

### S3: Aspose.CAD for Java belgelerine nereden ulaşabilirim?

C3: Belgeler **[burada](https://reference.aspose.com/cad/java/)** mevcuttur.

### S4: Aspose.CAD for Java için destek alabilir miyim?

C4: Destek forumuna **[buradan](https://forum.aspose.com/c/cad/19)** erişebilirsiniz.

### S5: Aspose.CAD for Java lisansını nereden satın alabilirim?

C5: Lisansı **[buradan](https://purchase.aspose.com/buy)** satın alabilirsiniz.

## Sonuç

Artık Aspose.CAD for Java kullanarak **DGN dosyalarından JPEG oluşturmayı** öğrendiniz. Yukarıdaki adımları izleyerek DGN‑to‑JPEG dönüşümünü herhangi bir Java uygulamasına sorunsuzca entegre edebilir, ister masaüstü araçları, web servisleri ya da otomatik işlem hatları için kullanabilirsiniz.

---

**Son Güncelleme:** 2026-01-10  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.11 (yazım anındaki en yeni sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}