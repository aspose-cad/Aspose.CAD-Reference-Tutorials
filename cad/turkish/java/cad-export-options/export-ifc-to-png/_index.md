---
date: 2026-10-19
description: Aspose.CAD for Java ile sadece birkaç satır kodla PNG küçük resim IFC
  dosyaları oluşturmayı öğrenin.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: IFC'yi PNG'ye Dışa Aktar
og_description: Aspose.CAD for Java kullanarak PNG küçük resim IFC dosyalarını zahmetsizce
  oluşturun. Bu adım adım rehber, IFC modellerini yükleme, rasterleştirme ve yüksek
  kaliteli PNG görüntüleri olarak kaydetme sürecini gösterir.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Aspose.CAD for Java ile PNG küçük resim IFC oluşturun
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Aspose.CAD for Java ile PNG küçük resim IFC oluşturma
url: /tr/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# IFC'yi PNG'ye Dışa Aktarma – Aspose.CAD for Java ile

## Giriş

Bu öğreticide Aspose.CAD for Java ile **PNG küçük resim IFC oluştur** dosyaları oluşturmayı öğreneceksiniz. BIM portalı için hızlı ön izlemelere, belge yönetim sistemi için küçük resimler oluşturmaya veya toplu dönüşümleri otomatikleştirmeye ihtiyacınız olsun, aşağıdaki adımlar birkaç satır Java kodu ile 3‑D IFC modelini net bir 2‑D PNG görüntüsüne rasterlemenizi sağlar.

## Hızlı Yanıtlar
- **Gerekli kütüphane nedir?** Aspose.CAD for Java.  
- **Birkaç satır kodla PNG küçük resim IFC oluşturabilir miyim?** Evet – tüm iş akışı 20 satırın altında.  
- **Üretim için lisansa ihtiyacım var mı?** Test için geçici bir lisans çalışır; ticari dağıtım için tam lisans gereklidir.  
- **Çıktı ölçeklenebilir mi?** Herhangi bir piksel boyutu ayarlayabilirsiniz, böylece PNG ihtiyacınız olan herhangi bir boyuta ölçeklenir.  
- **Hangi Java sürümü destekleniyor?** Java 8 veya üzeri.

## “IFC'yi PNG'ye dönüştürmek” nedir?
IFC (Industry Foundation Classes) dosyasını PNG'ye dönüştürmek, 3‑D bina modelini 2‑D bitmap görüntüsüne rasterleştirmek anlamına gelir. Bu süreç, tam bir CAD görüntüleyiciye ihtiyaç duymadan tarayıcılarda, raporlarda veya mobil uygulamalarda görüntülenebilen görsel bir küçük resim oluşturur.

## Neden Aspose.CAD for Java kullanmalı?
Aspose.CAD, **30+ CAD ve BIM formatını** destekler; bunlar arasında IFC, DWG, DXF ve DGN bulunur ve **2 GB**'a kadar dosyaları bellek içine tüm belgeyi yüklemeden işleyebilir. Kütüphane saf Java'dır, **sıfır dış bağımlılığı** vardır ve Windows, Linux ve macOS'ta çalışır, bu da sunucu‑tarafı görüntü üretimi için idealdir.  
Yüksek‑performanslı rasterleştirme, geniş format desteği ve Java uygulamalarına kolay entegrasyon sağlar.

## Önkoşullar

- **Aspose.CAD Kütüphanesi** – en son JAR'ı [indirme bağlantısından](https://releases.aspose.com/cad/java/) indirin.  
- **Java Development Kit** – JDK 8 veya daha yeni bir sürüm makinenizde kurulu.  
- **IFC kaynak dosyası** – dosyayı kodunuzdan referans alabileceğiniz bir klasöre yerleştirin.

## Ad alanlarını içe aktar

`com.aspose.cad` paketi ihtiyacınız olan tüm sınıfları sağlar. `CadImage`, CAD dosyalarını yüklemek için giriş noktasıdır, `PngOptions` ise rasterleştirme ayarlarını yapılandırır.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Java'da PNG küçük resim IFC nasıl oluşturulur?

IFC dosyasını yükleyin, rasterleştirme seçeneklerini tanımlayın ve sonucu PNG görüntüsü olarak kaydedin – bu tam dönüşüm iş akışıdır. Aşağıdaki bölümler her adımı ayrıntılı olarak açıklar, böylece kod parçacıklarını projenize kopyalayıp hemen çalıştırabilirsiniz.

### Adım 1: IFC dosyasını yükle
İlk olarak, IFC dosyanızın bulunduğu klasöre işaret edin ve `CadImage.load` ile yükleyin.  
`CadImage.load`, bir CAD dosyasını okur ve rasterleştirilebilecek bir görüntü nesnesi döndürür.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Neden önemli:** Dosyayı `CadImage` olarak yüklemek, çözünürlük, arka plan rengi ve çizgi kalınlığını kontrol eden vektör‑raster dönüşüm seçeneklerine erişim sağlar.

### Adım 2: rasterleştirme seçeneklerini ayarla
Çıktı boyutlarını ve diğer vektör‑ile‑ilgili ayarları `VectorRasterizationOptions` aracılığıyla tanımlayın.  
`VectorRasterizationOptions`, çıktı boyutunu, arka plan rengini ve diğer rasterleştirme parametrelerini belirlemenizi sağlar.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> `PageWidth` ve `PageHeight` değerlerini ayarlayarak son PNG çözünürlüğünü kontrol edin; bu, yüksek kalite baskılar veya web küçük resimleri için **PNG java** dosyalarını kaydederken önemlidir.

### Adım 3: PNG seçeneklerini yapılandır
Rasterleştirme seçeneklerini bir `PngOptions` örneği oluşturarak PNG dışa aktarıcısına bağlayın.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Adım 4: görüntüyü PNG olarak kaydet
Son olarak, rasterleştirilmiş görüntüyü `save` yöntemiyle diske yazın.  
`save`, rasterleştirilmiş görüntüyü seçilen formatta belirtilen dosya yoluna yazar.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Bu adımı tamamladıktan sonra **PNG küçük resim IFC** dosyasını başarıyla oluşturmuş olursunuz ve ortaya çıkan `example.png` dosyasını raster görüntüye ihtiyaç duyduğunuz her yerde kullanabilirsiniz.

## Yaygın kullanım senaryoları
- **BIM modelleri için web portalında küçük resimler oluşturma**.  
- **Kat planı anlık görüntülerini** PDF veya Word raporlarına yerleştirme.  
- **Arşivleme veya taşıma projeleri için büyük IFC kütüphanelerinin otomatik toplu dönüşümü**.

## Sorun Giderme ve İpuçları
- **Bellek sorunları:** Çok büyük IFC dosyaları için JVM yığınını (`-Xmx2g` veya daha yüksek) artırın.  
- **Eksik dokular:** IFC dosyasının dış kaynaklarının `dataDir` üzerinden erişilebilir olduğundan emin olun.  
- **Pro ipucu:** Varsayılan şeffaf PNG yerine beyaz arka plan tercih ediyorsanız `vectorOptions.setBackgroundColor(Color.getWhite())` kullanın.

## SSS

### S1: Aspose.CAD tüm IFC dosya sürümleriyle uyumlu mu?
C1: Aspose.CAD çeşitli IFC sürümlerini destekler. Ayrıntılı uyumluluk bilgileri için [belgelere](https://reference.aspose.com/cad/java/) bakın.

### S2: Rasterleştirme seçeneklerini daha da özelleştirebilir miyim?
C2: Kesinlikle! DPI kontrolü, anti‑aliasing ve çizgi kalınlığı gibi gelişmiş ayarlar için [belgelere](https://reference.aspose.com/cad/java/) göz atın.

### S3: Deneme sürümü mevcut mu?
C3: Evet, ücretsiz deneme sürümünü [Aspose.CAD ücretsiz deneme](https://releases.aspose.com/) üzerinden indirebilirsiniz.

### S4: Test için geçici lisans nasıl alınır?
C4: [Aspose.CAD geçici lisans sayfasından](https://purchase.aspose.com/temporary-license/) geçici bir lisans edinin.

### S5: Sorular sorabilir veya sorunları nerede bildirebilirim?
C5: Aspose mühendisleri ve diğer geliştiricilerden destek almak için [Aspose.CAD forumuna](https://forum.aspose.com/c/cad/19) katılın.

## Sıkça Sorulan Sorular

**S: Bu yaklaşımı diğer CAD formatlarını PNG'ye dönüştürmek için kullanabilir miyim?**  
C: Evet, Aspose.CAD birçok formatı (DWG, DXF, DGN vb.) destekler. Sadece dosya uzantısını değiştirin ve uygun görüntü sınıfını yükleyin.

**S: Kütüphane özel bir DPI ayarlamama izin veriyor mu?**  
C: DPI, `PageWidth`/`PageHeight` aracılığıyla dolaylı olarak kontrol edilir. İstenen fiziksel boyuta göre bu değerleri ayarlayarak gerekli DPI'yi elde edebilirsiniz.

**S: PNG çıktısı kayıpsız mı?**  
C: PNG kayıpsız bir formattır, bu yüzden rasterleştirilmiş görüntü orijinal vektör verisinin tam görsel bütünlüğünü korur.

## Sonuç

Artık Aspose.CAD for Java kullanarak **PNG küçük resim IFC** dosyaları oluşturmak için eksiksiz, üretim‑hazır bir yönteme sahipsiniz. Bu adımları masaüstü araçlarına, sunucu‑tarafı hizmetlerine veya bulut fonksiyonlarına entegre ederek BIM görselleştirme süreçlerini otomatikleştirebilir ve son kullanıcılara hızlı, yüksek‑kaliteli küçük resimler sunabilirsiniz.

---

**Son Güncelleme:** 2026-10-19  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.CAD for Java ile STL'yi PNG'ye Dönüştürme](/cad/java/cad-export-options/export-stl-to-png/)
- [DWG'yi PNG'ye Dönüştür – Aspose.CAD for Java Kullanarak CAD'yi PNG Olarak Kaydet](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [Java'da DWG'yi PDF'ye Dışa Aktar – Aspose.CAD ile PDF Sayfa Boyutunu Ayarla](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}