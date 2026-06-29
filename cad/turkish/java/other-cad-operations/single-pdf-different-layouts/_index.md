---
date: 2026-06-29
description: Aspose.CAD for Java kullanarak DWG'den PDF oluşturmayı ve PDF düzenini
  özelleştirmeyi öğrenin. Java geliştiricileri için kolay entegrasyon.
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: Farklı Düzenlere Sahip Tek PDF
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java ile DWG'den PDF Oluşturun
url: /tr/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'den PDF Oluşturma Aspose.CAD for Java ile

## Giriş

Bu öğreticide **DWG'den PDF oluşturma** dosyalarını oluşturacak ve Aspose.CAD for Java kullanarak çeşitli sayfa‑boyutu düzenleri uygulayacaksınız. İster inşaat planları, mühendislik şemaları ya da pazarlama‑hazır PDF'ler üretmeniz gerekse, aşağıdaki adımlar CAD çizimlerini PDF'ye dönüştürmeyi, her düzenin boyutlarını özelleştirmeyi ve tek bir çok‑sayfalı belge üretmeyi—Java ortamınızdan çıkmadan—gösterir.

## Hızlı Yanıtlar
- **Bu öğreticinin kapsamı nedir?** DWG çizimini birden çok sayfa boyutlu tek bir PDF'ye dönüştürmek.  
- **Hangi kütüphane gereklidir?** Aspose.CAD for Java (en son sürüm).  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Diğer formatlara dışa aktarabilir miyim?** Evet – API ayrıca PNG, JPEG ve SVG dışa aktarmayı destekler.  
- **Java 8 yeterli mi?** Kütüphane Java 8 ve daha yeni çalışma zamanlarıyla çalışır.

## “DWG'den PDF oluşturma” nedir?

**DWG'den PDF oluşturma**, yerel bir AutoCAD DWG dosyasını vektör doğruluğu, katmanlar ve çizgi kalınlıkları korunarak bir PDF belgesine dönüştürmek ve düzen özelleştirmesine izin vermek anlamına gelir. Aspose.CAD bu dönüşümü tamamen bellek içinde gerçekleştirir, bu yüzden harici bir CAD yazılımına ihtiyaç yoktur ve ortaya çıkan PDF doğrudan düzenlenebilir veya yazdırılabilir.

## DWG'den PDF düzenini neden özelleştirirsiniz?

Aspose.CAD **30'dan fazla CAD formatını** destekler ve dosyanın tamamını belleğe yüklemeden **500 MB**'a kadar PDF oluşturabilir. Her düzen için ayrı sayfa boyutları tanımlayarak ISO, ANSI veya özel ölçülere uyan yazdırılabilir sayfalar üretebilir—zaman kazandıran ve manuel sonrası işleme ihtiyacı ortadan kaldıran ölçülebilir bir fayda.

## Önkoşullar

- Java Ortamı: Makinenizde Java yüklü olduğundan emin olun.  
- Aspose.CAD Kütüphanesi: Aspose.CAD kütüphanesini Java için [download link](https://releases.aspose.com/cad/java/) adresinden indirin ve kurun.  
- Belge Dizini: DWG çizimleriniz için bir dizin oluşturun.

## Paketleri İçe Aktarma

`CadImage` sınıfı, Aspose.CAD'in bellekte bir CAD çizimini temsil eden temel nesnesidir. Başlamadan önce gerekli ad alanlarını içe aktarın:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Adım 1: CAD Çizimini Yükleme

`CadImage` DWG dosyasını yükler ve vektör verilerine erişim sağlar. CAD çiziminizi bir `CadImage` nesnesine yükleyerek başlayın:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Adım 2: Rasterleştirme Seçeneklerini Yapılandırma

`RasterizationOptions`, CAD vektörlerinin PDF'ye yerleştirilmeden önce nasıl rasterleştirileceğini tanımlar. CAD görüntüsü için rasterleştirme seçeneklerini ayarlayın:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Adım 3: Düzen Sayfa Boyutlarını Özelleştirme

`PdfOptions`, DWG içindeki her düzen için farklı sayfa boyutları atamanıza olanak tanır. CAD çizimi içinde birkaç düzen için özel boyutlar tanımlayın:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Adım 4: PDF Seçeneklerini Ayarlama

`PdfOptions`, rasterleştirme ayarları ve düzen tanımlarını birleştiren kapsayıcıdır. Rasterleştirme ayarlarını dahil ederek PDF seçeneklerini yapılandırın:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Adım 5: PDF Olarak Kaydetme

`PdfSaveOptions`, dönüşümü tamamlar ve çıktı dosyasını yazar. İşlenmiş CAD görüntüsünü PDF olarak kaydedin:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Tebrikler! Aspose.CAD for Java kullanarak farklı sayfa boyutlarıyla **DWG'den PDF oluşturma** işlemini başarıyla tamamladınız.

## Yaygın Sorunlar ve Çözümler

- **Çıktı PDF'sinde boş sayfalar** – `PageSize` değerlerinin DWG dosyasındaki gerçek düzen boyutlarıyla eşleştiğinden emin olun.  
- **Büyük çizimlerde bellek hataları** – Dosyayı tamamen yüklemek yerine akış olarak işlemek için `CadImage.load(..., LoadOptions)` ve `LoadOptions.setLoadMode(LoadMode.Memory)` kullanın.  
- **Yanlış ölçekleme** – İstenen DPI'ye (inç başına nokta) uygun olması için `RasterizationOptions.setPageWidth` ve `setPageHeight` ayarlarını düzenleyin.

## Sık Sorulan Sorular

**S: Aspose.CAD for Java'ı diğer Java kütüphaneleriyle kullanabilir miyim?**  
C: Evet, Aspose.CAD for Java Apache POI, Jackson veya Spring Boot gibi kütüphanelerle sorunsuz bir şekilde bütünleşir.

**S: Deneme sürümü mevcut mu?**  
C: Kesinlikle! Ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) erişebilirsiniz.

**S: Ek destek nereden bulunabilir?**  
C: Topluluk desteği ve tartışmalar için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

**S: Geçici bir lisans nasıl alınır?**  
C: Geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

**S: Tam sürüm nereden satın alınır?**  
C: Aspose.CAD for Java tam sürümünü [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

**Son Güncelleme:** 2026-06-29  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.10  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.CAD for Java Kullanarak DWG'yi PDF veya Raster Olarak Dışa Aktar](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java ile CAD Düzenlerini PDF'ye Dışa Aktar](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Aspose.CAD for Java Kullanarak Belirli DWG Düzenini PDF'ye Dışa Aktar](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}