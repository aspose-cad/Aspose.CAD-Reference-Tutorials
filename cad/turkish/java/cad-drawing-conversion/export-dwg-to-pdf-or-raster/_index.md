---
date: 2026-10-14
description: Java CAD library Aspose.CAD for Java'in DWG'yi PDF'ye veya raster görüntülere
  hızlı ve doğru bir şekilde dışa aktarabildiğini öğrenin.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: DWG PDF ve raster görüntüleri dışa aktar
og_description: Aspose.CAD for Java ile DWG PDF'yi hızlı bir şekilde dışa aktarın.
  Bu adım adım rehberde yüksek kaliteli PDF dönüşümü, raster seçenekleri ve lisanslama
  hakkında bilgi edinin.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: Java CAD library Aspose.CAD kullanarak DWG PDF ve raster görüntüleri dışa
  aktar
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: Java CAD library Aspose.CAD kullanarak DWG PDF ve raster görüntüleri dışa aktar
url: /tr/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java CAD Kütüphanesi Aspose.CAD Kullanarak DWG PDF ve Raster Görüntüleri Dışa Aktarma

## Giriş

DWG'yi PDF'ye dönüştürmek, mühendisler, mimarlar ve yerel dosya formatını ortaya çıkarmadan CAD çizimlerini paylaşması gereken herkes için sık bir gereksinimdir. **Aspose.CAD for Java** ile sadece birkaç satır Java kodu kullanarak **export dwg pdf** — veya raster görüntüler — yapabilir, vektör bütünlüğünü ve düzen hassasiyetini koruyabilirsiniz. Bu öğretici, bir DWG dosyasını yükleme, rasterleştirme ayarlarını yapılandırma ve sonucu yüksek‑kaliteli bir PDF veya görüntü olarak kaydetme sürecini adım adım gösterir. Ayrıca Aspose.CAD'in güvenilir, çok platformlu dönüşüm için tercih edilen Java CAD kütüphanesi olduğunu göreceksiniz.

Sadece PDF dönüşümü üzerine odaklanmış bir kılavuz için, [DWG'yi PDF'ye Dışa Aktarma Öğreticisi](/java/cad-drawing-conversion/export-dwg-to-pdf/) adresine bakın.

## Hızlı Yanıtlar
- **Bu öğretici neyi kapsıyor?** Aspose.CAD for Java kullanarak DWG dosyalarını PDF veya raster görüntülerine dışa aktarma.  
- **Bir lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz geçici bir lisans mevcuttur; üretim için tam lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** En son Aspose.CAD Java API'si, Java 8+ çalışma zamanının herhangi bir sürümüyle çalışır.  
- **DWG'yi diğer görüntü formatlarına dönüştürebilir miyim?** Evet – aynı rasterleştirme seçenekleri PNG, JPEG, BMP vb. formatlarda çıktı almanıza olanak tanır.  
- **Dönüşüm ne kadar sürer?** Standart çizimler için genellikle bir saniyenin altında; daha büyük dosyalar birkaç saniye sürebilir.

## Java CAD Kütüphanesi, DWG Dönüşümü İçin En İyi Seçim Neden?

Aspose.CAD for Java, yerel DLL'lere ihtiyaç duymayan saf Java uygulaması sunması, metrik veya imparatorluk birimlerini otomatik olarak algılaması, 1200 DPI'ye kadar raster çıktı sağlaması ve harici bağımlılıklar olmadan vektör koruyan PDF'ler oluşturması nedeniyle en iyi seçimdir. Kütüphane ayrıca geçici bir lisansla başlayıp kurumsal kullanıma ölçeklendirebileceğiniz esnek bir lisans modeli sunar.

## “export dwg to pdf” nedir?

`Export dwg pdf`, yerel bir DWG çizim dosyasını vektör verilerini, katmanları ve ölçeklemeyi koruyarak bir PDF belgesine dönüştürme sürecidir. Bu dönüşüm, AutoCAD'e ihtiyaç duymadan herhangi bir platformda görüntülenebilen cihaz bağımsız bir dosya üretir. PDF vektör bilgilerini koruduğu için metin aranabilir kalır ve grafikler herhangi bir yakınlaştırma seviyesinde net kalır; bu da belgeleme, müşteri incelemesi ve arşivleme için idealdir.

## Bu Dönüşüm İçin Aspose.CAD Java Neden Kullanılmalı?

Aspose.CAD Java'yı kullanmalısınız çünkü kütüphane birim dönüşümünü, rasterleştirmeyi ve PDF gömülmesini dahili olarak yönetir; bu da üçüncü taraf araçlara veya karmaşık komut satırı zincirlerine ihtiyaç duymadan yapılabilir. API'si geliştiriciler için tasarlanmıştır: tek bir `Image` nesnesi çizimi temsil eder ve birkaç yapılandırma nesnesi DPI, sayfa boyutu ve sıkıştırmayı ince ayarlamanıza olanak tanır. Sonuç, Windows, Linux ve macOS ortamlarında tutarlı, tekrarlanabilir bir çıktı sağlar.

## Önkoşullar

- Java programlaması hakkında temel bilgi.  
- Aspose.CAD for Java kütüphanesi yüklü. Henüz indirmediyseniz, **[download Aspose.CAD for Java](https://releases.aspose.com/cad/java/)** adresinden edinin.  
- Test için bir DWG dosyası – bu kılavuzda örnek **Bottom_plate.dwg** kullanılmıştır.

## Ad Alanlarını İçe Aktarma

In your Java project, import the necessary classes to kick‑start the conversion:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Adım Adım Rehber

### Adım 1: DWG Dosyasını Yükleme

İlk olarak, `Image` sınıfını kullanarak DWG çiziminizi yükleyin. Bu, Aspose.CAD'in çalışabileceği bellek içi bir temsil oluşturur.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Adım 2: Birim Tipini Belirleme

Çizimin metrik mi yoksa imparatorluk birimlerini mi kullandığını anlamak, doğru ölçekleme için gereklidir. Yardımcı metod `IsMetric` (kısa tutmak için uygulanması atlanmıştır) bir boolean değer döndürür.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Adım 3: Rasterleştirme Seçeneklerini Ayarlama

`CadRasterizationOptions` sınıfı DPI, sayfa boyutu ve birim dönüşümü gibi rasterleştirme parametrelerini tanımlar. Birim sistemine göre sayfa boyutunu, ölçeklemeyi ve hedef birim tipini yapılandırın. Bu seçenekler, DWG'nin PDF'ye dönüştürülmeden önce nasıl rasterleştirileceğini belirler.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Adım 4: PDF Seçeneklerini Yapılandırma (pdf options cad)

`PdfOptions` sınıfı sıkıştırma ve meta veriler dahil PDF'ye özgü ayarları belirtir. Bir `PdfOptions` örneği oluşturun ve rasterleştirme ayarlarını ekleyin. Bu, Aspose.CAD'e rasterleştirilmiş içeriği nihai PDF'ye nasıl gömeceğini söyler.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Adım 5: PDF Olarak Kaydetme

`save` metodu, verilen dosya yoluna sağlanan seçeneklerle görüntüyü yazar. Son olarak, çizimi bir PDF dosyasına dışa aktarın. `save` metodu çıktı yolunu ve yapılandırılmış `PdfOptions` nesnesini alır.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Kod tamamlandığında, `DWGDrawings` klasörünüzde **Saved.pdf** dosyasını bulacaksınız; dağıtım veya arşivleme için hazır.

## Java CAD Kütüphanesi ile DWG Raster Görüntülerini Nasıl Dönüştürürüm?

`PdfOptions` yerine `PngOptions` veya `JpegOptions` gibi raster‑özel bir seçenek sınıfı kullanarak DWG'yi raster formatlara dönüştürebilirsiniz. Aynı `CadRasterizationOptions` örneğini yeniden kullanın, çıktı formatını ayarlayın ve `save` metodunu yeni seçenek nesnesiyle çağırın. Bu yaklaşım, tek bir satır değişikliğiyle PNG, JPEG, BMP veya TIFF dosyaları oluşturmanıza olanak tanır ve iş akışını tutarlı tutar.

## PDF Options CAD Kullanarak PDF DWG Nasıl Oluşturulur?

Yukarıdaki örnek zaten **pdf dwg** çıktısı **oluşturur**. PDF boyutunu ince ayarlamak için `pdfOptions.setCompress(true)` çağrısı yaparak sıkıştırmayı etkinleştirebilirsiniz. Ayrıca özel meta verileri gömebilir, PDF sürümünü ayarlayabilir veya ek `PdfOptions` özellikleriyle şifre koruması ekleyebilirsiniz. Bu ayarlamalar, Java kod tabanından çıkmadan nihai PDF üzerinde tam kontrol sağlar.

## Yaygın Sorunlar ve İpuçları

- **Yanlış sayfa boyutu** – Birim dönüşüm mantığını iki kez kontrol edin; uyumsuz katsayılar aşırı büyük sayfalar üretebilir.  
- **Eksik yazı tipleri veya çizgi kalınlıkları** – Dönüşümden önce DWG'nin dış kaynaklara referans verdiğinden emin olun.  
- **Büyük çizimlerde performans** – Yüksek kalite gerektiğinde yalnızca `CadRasterizationOptions` içinde `DPI` ayarını artırın; daha düşük DPI işlemeyi hızlandırır.  
- **Lisans endişeleri** – Değerlendirme için **geçici bir Aspose lisansı** kullanabilirsiniz; üretim dağıtımları için tam lisans gereklidir.

## Sık Sorulan Sorular

**S: Aspose.CAD for Java'yı diğer Java çerçeveleriyle kullanabilir miyim?**  
C: Evet, Aspose.CAD for Java, Spring, Jakarta EE ve Android gibi popüler Java çerçeveleriyle sorunsuz bir şekilde entegre olur.

**S: Aspose.CAD for Java için geçici bir lisans mevcut mu?**  
C: Evet, **[geçici bir lisans edinin](https://purchase.aspose.com/temporary-license/)** adresinden geçici bir lisans alabilirsiniz.

**S: Aspose.CAD for Java için destek nereden bulabilirim?**  
C: Topluluk ve Aspose mühendislerinden yardım almak için **[Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19)** ziyaret edin.

**S: Aspose.CAD for Java için lisans nasıl satın alınır?**  
C: **[Lisans satın alabilirsiniz](https://purchase.aspose.com/buy)**.

**S: Aspose.CAD for Java hangi birimleri destekliyor?**  
C: Aspose.CAD for Java, metrik ve imparatorluk birimlerini destekler ve çizimin birim sistemini otomatik olarak algılar.

**S: Aynı API'yi kullanarak DWG'yi diğer görüntü formatlarına (ör. PNG, JPEG) dönüştürebilir miyim?**  
C: Kesinlikle. `PdfOptions` yerine uygun raster görüntü seçeneklerini (ör. `PngOptions`) kullanın ve aynı `CadRasterizationOptions` nesnesini yeniden kullanın.

## Sonuç

Bu öğretici, **java cad library** Aspose.CAD for Java kullanarak **export dwg pdf** ve raster görüntüleri nasıl dışa aktaracağınızı gösterdi. Adım adım rehberi izleyerek, belgeleme için PDF'lere veya web gösterimi için raster görüntülere ihtiyacınız olsun, güvenilir CAD dönüşümünü herhangi bir Java uygulamasına entegre edebilirsiniz. Kütüphanenin saf Java yapısı, yüksek kaliteli çıktısı ve esnek lisanslama modeli, hem küçük yardımcı programlar hem de büyük ölçekli kurumsal hatlar için sağlam bir seçim olmasını sağlar.

**Son Güncelleme:** 2026-10-14  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.10  
**Yazar:** Aspose

## İlgili Öğreticiler

- [DWG'yi PDF'ye Dışa Aktarma: Aspose.CAD for Java ile Belirli Düzen](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Java'da DWG'yi PDF'ye Dışa Aktarma – Aspose.CAD ile PDF Sayfa Boyutunu Ayarlama](/cad/java/cad-export-options/export-to-pdf/)
- [Gizli Çizgilerle DWG'yi PDF'ye Dışa Aktarma – Aspose.CAD for Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}