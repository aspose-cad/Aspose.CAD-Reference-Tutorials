---
date: 2026-10-25
description: Aspose.CAD for Java kullanarak DWG'yi PDF'ye dönüştürmeyi, CAD düzenlerini,
  BMP, IFC ve STL dosyalarını dışa aktarmayı öğrenin. Lisanslama notları, performans
  ipuçları ve gerçek dünya kullanım örneklerini içerir.
keywords:
- convert dwg to pdf
- cad layout pdf export
- generate pdf from dwg
- java convert cad pdf
- export stl to png
lastmod: 2026-10-25
linktitle: CAD Dışa Aktarma Seçenekleri
og_description: Aspose.CAD for Java ile DWG'yi PDF, BMP, IFC ve STL'ye dönüştürün.
  Adım adım öğrenin, performans rakamlarını görün ve bu 2026 rehberinde lisanslama
  rehberliğini alın.
og_image_alt: Screenshot of Aspose.CAD Java API converting DWG to PDF
og_title: DWG'yi PDF'ye ve Java'da diğer CAD dışa aktarma seçeneklerine dönüştürün
schemas:
- author: Aspose
  dateModified: '2026-10-25'
  description: Learn how to convert DWG to PDF, export CAD layouts, BMP, IFC, and
    STL files using Aspose.CAD for Java. Includes licensing notes, performance tips,
    and real‑world use cases.
  headline: How to convert DWG to PDF and other CAD export options in Java
  type: TechArticle
- questions:
  - answer: Load the IFC file with `Image.load("model.ifc")` and call `save("model.png",
      new PngOptions())`.
    question: How do I convert IFC to PNG using Aspose.CAD?
  - answer: Yes—Aspose.CAD treats layouts as images internally, so `save("layout.pdf",
      new PdfOptions())` handles it automatically.
    question: Can I export a CAD layout directly to PDF without converting to an image
      first?
  - answer: Exporting an AutoCAD drawing converts the entire drawing, while exporting
      a layout targets a specific paper‑space view, preserving its page settings.
    question: What is the difference between exporting AutoCAD to PDF and exporting
      a CAD layout to PDF?
  - answer: No inherent limit; each layout becomes a separate page in the resulting
      PDF.
    question: Is there a limit on the number of pages when exporting a multi‑sheet
      DWG to PDF?
  - answer: A single Aspose.CAD license covers all supported formats (PDF, PNG, BMP,
      etc.).
    question: Do I need a separate license for each export format?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg to pdf
- Aspose.CAD
- Java CAD conversion
- CAD export tutorials
title: DWG'yi PDF'ye ve Java'da diğer CAD dışa aktarma seçeneklerine nasıl dönüştürülür
url: /tr/java/cad-export-options/
weight: 30
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD dışa aktarma seçenekleri

## Giriş

Eğer hızlı ve güvenilir bir şekilde **DWG'yi PDF'ye dönüştürmeniz** gereken bir Java geliştiricisiyseniz, doğru yerdesiniz. Bu kılavuz, Aspose.CAD for Java’nın en yaygın dışa aktarma senaryolarını—AutoCAD görüntüleri, CAD düzenleri, BMP, PDF, IFC ve STL dosyalarını—adım adım inceler. Bu özelliklerin gerçek dünyadaki projelerde neden önemli olduğunu görecek, en iyi uygulama ipuçlarını öğrenecek ve kendi uygulamalarınız için kopyalamaya hazır kod parçacıklarını elde edeceksiniz.

## Hızlı cevaplar
- **AutoCAD'i PDF'ye dışa aktarmanın en basit yolu nedir?** Use `Image.save("output.pdf", new PdfOptions())` from Aspose.CAD.  
- **IFC dosyalarını hangi formatlara dönüştürebilirim?** PNG is fully supported; just load the IFC file and save as PNG.  
- **STL dosyalarını doğrudan PNG'ye dışa aktarabilir miyim?** Yes—load the STL model and call `save("image.png")`.  
- **Üretim kullanımında bir lisansa ihtiyacım var mı?** A commercial license is required for non‑trial deployments.  
- **Hangi Java sürümü gereklidir?** Java 8 or higher is recommended.

## AutoCAD PDF dışa aktarma nedir?

AutoCAD çizimlerini PDF'ye dışa aktarmak, vektör tabanlı DWG/DXF dosyalarını yaygın olarak kabul edilen, sayfa odaklı bir formata dönüştürmek anlamına gelir. PDF, katmanları, çizgi kalınlıklarını ve renkleri korur, bu da tasarımları müşteriler, inceleyiciler veya yerel CAD dosyalarını anlamayan alt sistemlerle paylaşmak için idealdir.

## Aspose.CAD for Java neden kullanılmalı?

Aspose.CAD for Java, **pure‑Java** bir kütüphanedir—yerel DLL'lere veya COM etkileşimine gerek yoktur. Geometriyi, metni ve raster verileri **high fidelity** ile yeniden üretir, binlerce dosyanın **batch processing**'ini destekler ve **over 60 input and output formats** (DWG, DXF, IFC, STL, BMP, PNG ve PDF dahil) işleyebilir. Kütüphanenin bellek‑verimli boru hattı, tüm dosyayı RAM'e yüklemeden çok sayfalı çizimleri işleyebilmenizi sağlar.

## Bunun önemi nedir

Anlık olarak **DWG'yi PDF'ye dönüştürebilmek**, rapor oluşturmayı otomatikleştirmenizi, müşteri hazır teslimatlar oluşturmanızı ve ham DWG dosyalarını ifşa etmeden CAD verilerini web portallarına gömmenizi sağlar. Aynı API, küçük resimler, hızlı görsel kontroller ve hafif ön izlemeler için görüntü‑tabanlı dışa aktarmalar (BMP, PNG) da oluşturur.

## Önkoşullar
- Java 8 veya daha yeni bir sürüm yüklü.  
- Aspose.CAD for Java kütüphanesi projenize eklenmiş (Maven, Gradle veya manuel JAR).  
- Üretim kullanımı için geçerli bir Aspose lisansı (değerlendirme için ücretsiz deneme mevcuttur).

## Java'da DWG'yi PDF'ye nasıl dönüştürülür

`Image`, bellekte bir CAD belgesini temsil eden temel Aspose.CAD sınıfıdır.  
`PdfOptions`, çözünürlük ve sıkıştırma gibi PDF‑özel çıktı ayarlarını yapılandırır.

`Image.load` ile DWG'yi (veya desteklenen herhangi bir CAD formatını) yükleyin, ardından bir `PdfOptions` örneği kullanarak `save` çağrısı yapın. Bu iki adımlı desen, vektör‑PDF dönüşümünü yönetir, katmanları korur ve DPI ya da sıkıştırma ayarlarını ayarlamanıza olanak tanır.

`Image` sınıfı, bellekteki herhangi bir desteklenen CAD belgesini temsil ederken, `PdfOptions` çıktı PDF'sini yapılandırır. Ek dönüşüm araçları veya dış yardımcı programlara gerek yoktur.

### Adım 1: DWG dosyasını yükle
```java
// Load a DWG file – the Image class is the entry point for all Aspose.CAD operations
com.aspose.cad.Image cadImage = com.aspose.cad.Image.load("sample.dwg");
```

### Adım 2: PDF seçeneklerini yapılandır (isteğe bağlı)
```java
// Create PDF options – you can set vector rasterization DPI, compression, etc.
com.aspose.cad.imageoptions.PdfOptions pdfOptions = new com.aspose.cad.imageoptions.PdfOptions();
pdfOptions.setVectorRasterizationOptions(
    new com.aspose.cad.imageoptions.VectorRasterizationOptions()
        .setPageWidth(2100)   // width in pixels (A4 at 300 DPI)
        .setPageHeight(2970)  // height in pixels
        .setResolution(300)   // 300 DPI for high‑quality output
);
```

### Adım 3: PDF olarak kaydet
```java
// Save the loaded DWG as a PDF file
cadImage.save("output.pdf", pdfOptions);

// Release resources – important when processing many files in a loop
cadImage.dispose();
```

Yukarıdaki üç satır, eksiksiz bir **DWG'yi PDF'ye dönüştürmek** iş akışını oluşturur. Bunları bir döngü içinde kullanarak çizimlerin bulunduğu bir dizini toplu‑işlem yapabilirsiniz.

## CAD düzenlerini PDF'ye dışa aktar

Belirli bir düzeni (paper‑space görünümü) dışa aktarmak aynı şekilde çalışır çünkü Aspose.CAD her düzeni dahili olarak bir görüntü olarak ele alır. DWG'yi basitçe yükleyin, gerekirse adıyla düzeni seçin ve `PdfOptions` ile `save` çağrısı yapın. Ek bir dönüşüm adımına gerek yoktur.

## BMP'ye dışa aktar

`BmpOptions`, bit derinliği ve çözünürlük gibi BMP‑formatı çıktı parametrelerini belirler. Raster küçük resimler veya bitmap varlıkları gerektiğinde `PdfOptions` yerine `BmpOptions` kullanın. Aynı `Image` nesnesi tek bir çağrı ile BMP olarak kaydedilebilir, kataloglar veya UI küçük resimleri için yüksek çözünürlüklü ön izlemeler oluşturmanıza olanak tanır.

## PDF'ye dışa aktar (genel CAD dosyaları)

DWG'nin ötesinde, kütüphane aynı kodla DXF, DWF ve diğer CAD formatlarını PDF'ye dönüştürebilir. `Image.load` içindeki dosya uzantısını değiştirmeniz yeterlidir. Temel dönüşüm motoru kaynak formatı otomatik olarak algılar.

## IFC'yi PNG'ye dışa aktar

`PngOptions`, sıkıştırma seviyesi gibi PNG‑formatı ayarlarını tanımlar. IFC (Industry Foundation Classes) dosyaları BIM iş akışlarında yaygındır. IFC'yi `Image.load` ile yükleyin ve `PngOptions` kullanarak PNG olarak kaydedin. Bu, web panolarına veya belgelere gömülebilen bir raster görüntü üretir.

## STL'yi PNG'ye dışa aktar

`PngOptions`, sıkıştırma seviyesi gibi PNG‑formatı ayarlarını tanımlar. STL dosyaları 3‑D ağları tanımlar. Aspose.CAD, bunları 2‑D bir görüntüye render eder; bu görüntüyü hızlı görsel kontroller veya ürün listeleri için PNG olarak dışa aktarabilirsiniz. Aynı `Image.save("model.png", new PngOptions())` deseni uygulanır.

## CAD dışa aktarma öğreticileri

### [AutoCAD görüntülerini PDF'ye dışa aktar - Aspose.CAD for Java öğreticisi](./export-autocad-images-to-pdf/)
Aspose.CAD for Java kullanarak AutoCAD görüntülerini PDF'ye zahmetsizce dışa aktarın. Sorunsuz entegrasyon için adım adım rehberimizi izleyin.

### [Aspose.CAD for Java ile CAD düzenlerini PDF'ye dışa aktar](./export-cad-layouts-to-pdf/)
Aspose.CAD for Java'yı keşfederek CAD düzenlerini PDF'ye zahmetsizce dışa aktarın. Verimli, güvenilir ve geliştirici‑dostu.

### [Aspose.CAD for Java ile BMP'ye dışa aktar](./export-to-bmp/)
Aspose.CAD for Java ile CAD'den BMP'ye sorunsuz dönüşümü keşfedin. Verimli ve kesin dışa aktarmalar için adım adım rehberimizi izleyin.

### [Aspose.CAD for Java ile PDF'ye dışa aktar](./export-to-pdf/)
Aspose.CAD for Java kullanarak CAD dosyalarını PDF'ye zahmetsizce dışa aktarmayı öğrenin. Sorunsuz entegrasyon için adım adım rehberimizi izleyin.

### [Aspose.CAD for Java ile IFC'yi PNG'ye dışa aktar](./export-ifc-to-png/)
Aspose.CAD for Java ile IFC'yi PNG'ye zahmetsizce dönüştürün. Adım adım öğreticimizi izleyin.

### [Aspose.CAD for Java ile STL'yi PNG'ye dışa aktar](./export-stl-to-png/)
Aspose.CAD ile Java'da STL dosyalarını PNG'ye sorunsuz bir şekilde dışa aktarma sürecini keşfedin. İş akışınızı basitleştirin ve Java projelerinizi zahmetsizce geliştirin.

## Ortak kullanım senaryoları
- **Müşteri teslimatları** – Kaynak DWG dosyalarını ifşa etmeden PDF formatında tasarım incelemeleri sağlayın.  
- **Otomatik raporlama** – Gösterge panelleri için IFC veya STL modellerinin PNG küçük resimlerini oluşturun.  
- **Toplu dönüşüm hatları** – Basit bir Java döngüsü kullanarak büyük CAD arşivlerini gece boyunca işleyin.

## İpuçları ve püf noktaları
- **Pro tip:** Raster‑tabanlı dışa aktarmalar için DPI'yi kontrol etmek ve dosya boyutlarını makul tutmak amacıyla `PdfOptions.setVectorRasterizationOptions().setResolution(300)` ayarlayın.  
- **Bellek dalgalanmalarını önleyin:** Call `Image.dispose()` after each `save` when processing many files.  
- **Sorun giderme:** Katmanlar kaybolursa, kaynak DWG'nin görünür katmanlara sahip olduğunu doğrulayın ve `PdfOptions.setCompress(true)` ile sıkıştırmayı etkinleştirin.

## Sıkça sorulan sorular

**Q: Aspose.CAD kullanarak IFC'yi PNG'ye nasıl dönüştürürüm?**  
A: IFC dosyasını `Image.load("model.ifc")` ile yükleyin ve `save("model.png", new PngOptions())` çağırın.

**Q: Bir CAD düzenini önce görüntüye dönüştürmeden doğrudan PDF'ye dışa aktarabilir miyim?**  
A: Evet—Aspose.CAD düzenleri dahili olarak görüntü olarak ele alır, bu yüzden `save("layout.pdf", new PdfOptions())` bunu otomatik olarak işler.

**Q: AutoCAD'i PDF'ye dışa aktarmak ile bir CAD düzenini PDF'ye dışa aktarmak arasındaki fark nedir?**  
A: AutoCAD çizimini dışa aktarmak tüm çizimi dönüştürürken, bir düzeni dışa aktarmak belirli bir paper‑space görünümünü hedefler ve sayfa ayarlarını korur.

**Q: Çok sayfalı bir DWG'yi PDF'ye dışa aktarırken sayfa sayısı için bir sınırlama var mı?**  
A: Yerleşik bir sınırlama yoktur; her düzen, ortaya çıkan PDF'de ayrı bir sayfa olur.

**Q: Her dışa aktarma formatı için ayrı bir lisansa ihtiyacım var mı?**  
A: Tek bir Aspose.CAD lisansı, tüm desteklenen formatları (PDF, PNG, BMP, vb.) kapsar.

**Son Güncelleme:** 2026-10-25  
**Test Edilen:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose

## İlgili Öğreticiler

- [CAD'yi PDF'ye dışa aktar: Aspose.CAD for Java ile CAD düzenlerini PDF'ye dışa aktar](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Java'da DWG'yi PDF'ye dışa aktar – PDF sayfa boyutunu Aspose.CAD ile ayarlayın](/cad/java/cad-export-options/export-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}