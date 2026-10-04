---
date: 2026-10-04
description: Aspose.CAD for Java kullanarak DWG'yi PNG'ye hızlı bir şekilde dönüştürmeyi
  ve CAD'i PNG ya da diğer raster formatlarına dışa aktarmayı öğrenin. Yüksek kaliteli
  sonuçları hızlıca elde edin.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: CAD Düzenini Raster Görüntü Formatına Dönüştürün
og_description: Aspose.CAD for Java ile DWG'yi PNG'ye hızlı bir şekilde dönüştürün.
  CAD'i PNG, JPEG, TIFF ve diğer formatlara dışa aktarmayı adım adım öğrenin.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Aspose.CAD for Java kullanarak DWG'yi PNG ve diğer raster formatlarına dönüştürün
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Aspose.CAD for Java kullanarak DWG'yi PNG ve diğer raster formatlarına dönüştürün
url: /tr/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java kullanarak DWG'yi PNG ve diğer raster formatlarına dönüştürme

## Giriş

`Aspose.CAD for Java` bir kütüphanedir ve CAD dosyalarını PNG, JPEG ve TIFF gibi raster görüntülere programlı olarak dönüştürmeyi sağlar. DWG'yi PNG'ye (veya diğer raster görüntü formatlarına) dönüştürmek, CAD görüntüleyicisi olmayan ekip arkadaşlarıyla CAD çizimlerini paylaşmanız, tasarımları belgelerde gömmeniz veya web galerileri için küçük resimler oluşturmanız gerektiğinde yaygın bir gereksinimdir. Bu rehberde, tam bir çizim dosyasıyla ya da sadece belirli bir yerleşimle çalışsanız da dwg'yi png'ye hızlı ve güvenilir bir şekilde nasıl dönüştüreceğinizi öğreneceksiniz. Ayrıca web ön izlemeleri, raporlama araçları veya mobil uygulamalar için **CAD'yi rastera dönüştürmeniz** gerekebilir.

## Hızlı cevaplar
- **DWG'yi PNG'ye işleyen kütüphane nedir?** Aspose.CAD for Java dönüşüm motorunu sağlar.  
- **Hangi raster formatlarını dışa aktarabilirim?** PNG, JPEG, TIFF, PDF, BMP ve 30'dan fazla ek format.  
- **Test için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.  
- **Belirli bir yerleşim seçebilir miyim?** Evet – `setLayouts` kullanarak “Model”, “Layout1”, vb. hedefleyebilirsiniz.  
- **Yüksek çözünürlüklü çıktı mümkün mü?** Kesinlikle – DPI'yi kontrol etmek için `setPageWidth` ve `setPageHeight` (veya `setResolution`) ayarlayın.

## “convert dwg to png” nedir?

“Convert dwg to png”, DWG vektör çizimini herhangi bir standart görüntü görüntüleyicisi tarafından görüntülenebilen piksel tabanlı bir PNG görüntüsüne dönüştürmek anlamına gelir. Bu süreç, vektör öğelerini rasterleştirir, çizgi kalınlığı, renkler ve katmanları korurken sabit çözünürlüklü bir bitmap'e dönüştürür. Sonuç, PDF'lere, Word belgelerine veya vektör desteğinin sınırlı olduğu web sayfalarına gömmek için idealdir.

## CAD'i PNG (veya diğer raster formatları) olarak dışa aktarmak neden önemlidir?

CAD'i PNG olarak dışa aktarmak, evrensel uyumluluk, hızlı yükleme ve tüm büyük platformlarda kolay gömme sağlar. Raster görüntüler, ağır bir DWG dosyasını açmaya kıyasla anında yüklenir ve PNG'nin kayıpsız sıkıştırması görsel doğruluğu temin eder. Çözünürlük, arka plan rengi ve yerleşimi kontrol ederek, dosya masaüstü, mobil cihaz veya tarayıcı içinde görüntülense bile her paydaşı aynı görünümü görür.

## Yaygın kullanım senaryoları

| Senaryo | Raster çıktının faydası |
|----------|------------------------|
| **Proje dokümantasyonu** | PNG'leri PDF'lere veya Word belgelerine gömmek, inceleyenlerin CAD yazılımına ihtiyaç duymasını önler. |
| **Web portalları** | DWG dosyalarından oluşturulan küçük resimler anında yüklenir ve kullanıcı deneyimini iyileştirir. |
| **Mobil uygulamalar** | Raster görüntüler, CAD görüntüleyicisi olmayan cihazlarda doğru şekilde görüntülenir. |
| **Otomatik raporlama** | Grafiklere veya panolara eklemek için birden fazla yerleşimi toplu olarak PNG/JPEG'e dönüştürün. |

## Önkoşullar

1. **Java geliştirme ortamı** – JDK 8 veya daha yeni bir sürüm yüklü ve yapılandırılmış.  
2. **Aspose.CAD for Java** – En son JAR'ı [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/) adresinden indirin.  

## Ad alanlarını içe aktar

`com.aspose.cad.Image`, bellekte herhangi bir CAD dosyasını temsil eden temel sınıftır. `com.aspose.cad.imageoptions.*`, her raster formatı için seçenek nesneleri sağlar. Çizimi yüklemek, rasterleştirmeyi yapılandırmak ve çıktıyı kaydetmek için ihtiyacınız olan sınıfları içe aktarın.

> **Pro tip:** TIFF yerine **CAD'i PNG olarak dışa aktarmayı** planlıyorsanız, `TiffOptions` yerine `PngOptions` ( `com.aspose.cad.imageoptions.PngOptions` içinde bulunur) kullanın.

## Adım adım kılavuz

### Adım 1: kaynak dizinini ayarla

"Your Document Directory" ifadesini CAD dosyalarınızın bulunduğu mutlak yol ile değiştirin. Bu dizin, giriş ve çıkış dosyaları için kullanılacaktır.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Adım 2: CAD dosyasını yükle

`Image.load`, kaynak dosyayı ayrıştırır ve rasterleştirebileceğiniz bellek içi bir temsil oluşturur. Desteklenen herhangi bir formatı (DWG, DXF, DGN, vb.) yükleyebilirsiniz – bu **cad nasıl dönüştürülür** kısmıdır.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Adım 3: rasterleştirme seçeneklerini yapılandır

`CadRasterizationOptions`, vektör verisinin piksellere nasıl dönüştürüleceğini tanımlar. `setPageWidth` ve `setPageHeight`, çıktı çözünürlüğünü kontrol eder (daha büyük değerler = daha yüksek DPI). `setLayouts`, belirli yerleşimler için **CAD'i rastera dönüştürmenizi** sağlar; tüm çizimi rasterleştirmek için bunu atlayın.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Adım 4: görüntü seçeneklerini ayarla

`TiffOptions` (PNG için `PngOptions`), Aspose'a hangi raster formatının üretileceğini söyler ve sıkıştırma, renk derinliği ve diğer format‑özel ayarları ince ayar yapmanıza olanak tanır. İstediğiniz çıktıya uygun seçenek sınıfını seçin.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Adım 5: ortaya çıkan görüntüyü kaydet

`Image` örneği üzerinde `save` metodunu çağırın, çıktı dosya adını ve seçenek nesnesini geçirin. Dosya uzantısını `.png` olarak değiştirin (ve `PngOptions` kullanın) **CAD'i PNG olarak kaydetmek** için. Aynı desen JPEG, BMP veya PDF için de çalışır.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Yaygın tuzak:** Dosya uzantısını seçenek sınıfıyla eşleştirmeyi unutmak `UnsupportedFormatException` hatasına yol açar. Her zaman uyumlu tutun.

## Yaygın sorunlar ve çözümler

| Sorun | Çözüm |
|-------|----------|
| **Boş çıktı görüntüsü** | `setLayouts` içindeki yerleşim adlarının kaynak CAD dosyasındaki adlarla tam olarak eşleştiğini doğrulayın. |
| **Düşük çözünürlüklü PNG** | `setPageWidth` / `setPageHeight` değerlerini artırın veya rasterleştirme seçeneklerinde `setResolution` ayarlayın. |
| **Desteklenmeyen DWG sürümü** | En son Aspose.CAD sürümünü kullandığınızdan emin olun; eski sürümler yeni DWG sürümlerini desteklemeyebilir. |
| **Büyük dosyalarda bellek hataları** | Sayfaları tek tek işleyin veya JVM yığın boyutunu artırın (`-Xmx2g`). |

## Sıkça sorulan sorular

**Q: Aspose.CAD farklı CAD dosya formatlarıyla uyumlu mu?**  
A: Evet, DWG, DXF, DGN ve SVG dahil olmak üzere 30'dan fazla CAD ve raster formatını destekler.

**Q: Çıktı raster görüntüsünün çözünürlüğünü özelleştirebilir miyim?**  
A: Kesinlikle. İstenen DPI'yi elde etmek için `CadRasterizationOptions` içinde `setPageWidth`, `setPageHeight` veya `setResolution` ayarlarını değiştirin.

**Q: Tek bir çalıştırmada birden fazla CAD yerleşimini nasıl dönüştürebilirim?**  
A: `setLayouts` metoduna tüm yerleşim adlarını içeren bir dizi sağlayın, örneğin `new String[]{"Model","Layout1","Layout2"}`.

**Q: TIFF dışındaki çıktı formatları destekleniyor mu?**  
A: Evet—PNG, JPEG, BMP, PDF ve daha fazlası ilgili `*Options` sınıfları aracılığıyla mevcuttur.

**Q: Aspose.CAD ile ilgili yardım alabileceğim veya deneyimlerimi paylaşabileceğim yer neresi?**  
A: Topluluk desteği ve resmi yardım için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

## Sonuç

Bu adımları izleyerek **DWG'yi PNG'ye dönüştürebilir**, **CAD'i PNG olarak dışa aktarabilir**, **CAD'i JPEG olarak kaydedebilir** veya ihtiyacınız olan herhangi bir raster formatı oluşturabilirsiniz. Aspose.CAD for Java ağır işleri halleder, yüksek kaliteli görüntüleri uygulamalarınıza, belgelere veya web portallarına entegre etmeye odaklanmanızı sağlar. Kütüphanenin 30'dan fazla formatı desteklemesi ve çok sayfalı çizimleri tüm dosyayı belleğe yüklemeden işleyebilmesi, onu kurumsal düzeyde CAD rasterleştirme için sağlam bir seçenek yapar.

---

**Son Güncelleme:** 2026-10-04  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## İlgili Eğitimler

- [Java CAD kütüphanesi Aspose.CAD for Java kullanarak DWG'yi PDF veya Raster olarak hızlıca dışa aktar](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java ile DWG'yi BMP'ye dönüştür](/cad/java/cad-export-options/export-to-bmp/)
- [Aspose.CAD for Java kullanarak DWG'yi PDF'ye dışa aktar: Belirli Yerleşim](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}