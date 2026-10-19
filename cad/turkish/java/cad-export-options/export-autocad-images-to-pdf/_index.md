---
date: 2026-10-19
description: Aspose.CAD ile Java'da DWG'yi PDF'ye nasıl dönüştüreceğinizi öğrenin.
  Bu adım adım rehber, AutoCAD PDF'yi dışa aktarmayı, CAD'i PDF olarak kaydetmeyi
  ve lisans uygulamayı gösterir.
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: AutoCAD Görüntülerini PDF'ye Dışa Aktar
og_description: Aspose.CAD ile Java'da DWG'yi PDF'ye nasıl dönüştüreceğinizi öğrenin.
  Bu rehber, AutoCAD PDF'yi dışa aktarmayı, CAD'i PDF olarak kaydetmeyi ve lisanslamayı
  adım adım anlatır.
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: Aspose.CAD kullanarak Java'da DWG'yi PDF'ye dönüştürün
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: Aspose.CAD kullanarak Java'da DWG'yi PDF'ye dönüştürün
url: /tr/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# AutoCAD PDF Dışa Aktarma – AutoCAD görüntülerini PDF olarak Aspose.CAD for Java ile dışa aktarın

## Giriş

Java'da **DWG'yi PDF'ye dönüştürmeniz** gerekiyorsa, doğru yerdesiniz. Bu öğreticide, Aspose.CAD for Java kullanarak AutoCAD görüntülerini PDF olarak dışa aktarmayı öğreneceksiniz; bu saf‑Java kütüphanesi, yerel bağımlılıklar olmadan DWG, DXF, DWF ve birçok diğer CAD formatını işleyebilir. Sonunda **CAD'i PDF olarak kaydedebilecek**, sayfa boyutu gibi rasterleştirme seçeneklerini ayarlayabilecek ve üretim kullanımı için **Aspose CAD lisansını** doğru şekilde uygulayabileceksiniz.

## Hızlı Yanıtlar
- **Java ile DWG'yi PDF'ye dönüştürebilir miyim?** Evet – Aspose.CAD for Java, DWG, DXF ve onlarca diğer CAD formatını yerel olarak destekler.  
- **Bir lisansa ihtiyacım var mı?** Kalıcı bir **Aspose CAD lisansı**, tüm değerlendirme kısıtlamalarını kaldırır; test için geçici bir lisans da mevcuttur.  
- **Hangi Java sürümleri destekleniyor?** Java 8 ve üzeri tam olarak desteklenir.  
- **PDF sayfa boyutlarını kontrol edebilir miyim?** Kesinlikle – rasterleştirme seçeneklerinde `pageWidth` ve `pageHeight` değerlerini ayarlayın.  
- **3‑B renderlama mümkün mü?** Evet – 3‑B varlıkları rasterleştirmek için `TypeOfEntities.Entities3D` özelliğini etkinleştirin.

## Export AutoCAD PDF nedir?
AutoCAD PDF dışa aktarma, vektör CAD çizimlerini taşınabilir bir PDF belgesine dönüştürme sürecidir. Katmanları, çizgi kalınlıklarını, renkleri ve isteğe bağlı olarak 3‑B geometrileri korur; böylece tasarımları müşterilerle paylaşmak veya CAD yazılımı gerektirmeden arşivlemek kolaylaşır.

## Neden Aspose.CAD for Java ile DWG'yi PDF'ye dönüştürmeliyim?
Aspose.CAD, **50+ giriş ve çıkış formatını** destekler, çok sayfalı çizimleri tüm dosyayı belleğe yüklemeden işler ve Java 8+ destekleyen herhangi bir platformda çalışır. Kütüphane, DPI, sayfa boyutu ve düzen üzerinde tam kontrol sağlar; böylece **PDF sayfa boyutunu** proje gereksinimlerine tam olarak uyduracak şekilde **özelleştirebilir**, tüm bunları yerel DLL'ler kurmadan yapabilirsiniz.

## Önkoşullar

- **Java Development Kit** – Çalışma istasyonunuzda JDK 8 veya daha yeni bir sürüm yüklü olmalıdır.  
- **Aspose.CAD for Java** – En son JAR dosyasını [download link](https://releases.aspose.com/cad/java/) adresinden indirin.  
- **Çalışma dizini** – kaynak DWG dosyalarınızın ve oluşturulan PDF'lerin saklanacağı bir klasör.

## Ad alanlarını içe aktar

`Image` sınıfı rasterleştirilebilir herhangi bir CAD çizimini temsil eder, `RasterizationOptions` ve `PdfOptions` ise dönüşümü ince ayar yapmanıza olanak tanır.

`Image` sınıfı, Aspose.CAD'in bellek içinde bir CAD çizimini tutan üst‑seviye nesnesidir.  
`RasterizationOptions` sınıfı, vektör verisinin PDF'ye yazılmadan önce nasıl rasterleştirileceğini tanımlar.  
`PdfOptions` sınıfı, rasterleştirme ayarlarını PDF'ye özgü çıktı parametreleriyle birleştirir.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Şimdi kodu adım adım inceleyelim.

## Aspose.CAD for Java ile DWG'yi PDF'ye nasıl dönüştürürüm?

Aspose.CAD for Java ile bir DWG dosyasını PDF'ye dönüştürmek için, çizimi `Image` sınıfı ile yükleyin, CadRasterizationOptions'ı (DPI, sayfa boyutu ve varlık tipleri gibi) yapılandırın, bu seçenekleri `PdfOptions` içinde paketleyin ve ardından .pdf uzantılı bir dosya adı belirterek `save` metodunu çağırın. Bu sıralama, vektör verisinin doğru şekilde rasterleştirilmesini ve ortaya çıkan PDF'nin düzen gereksinimlerinize uymasını sağlar.

### Adım 1: kaynak dizin yolunu ayarlayın

`"Your Document Directory"` ifadesini, önkoşullarda oluşturduğunuz klasörün mutlak yolu ile değiştirin.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro ipucu:** Farklı işletim sistemlerinde yol‑ile ilgili hatalardan kaçınmak için `Paths.get(...).toAbsolutePath()` kullanın.

### Adım 2: CAD görüntüsünü yükleyin

CAD dosyasını bir `Image` nesnesine yüklemek, Aspose.CAD'in rasterleştirme motoruna tam erişim sağlar.

`Image` sınıfı DWG dosyasını yükler ve dönüşüm için hazırlar.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Neden önemli:** Çizim belleğe alındıktan sonra, rasterleştirmeden önce düzenlerini, katmanlarını ve meta verilerini sorgulayabilirsiniz.

### Adım 3: rasterleştirme seçeneklerini ayarlayın

`pageWidth` ve `pageHeight` değerlerini **PDF sayfa boyutunu özelleştirmek** için ayarlayın. `setTypeOfEntities(TypeOfEntities.Entities3D)` özelliğini etkinleştirmek, gerektiğinde tam 3‑B renderlamayı sağlar.

`RasterizationOptions` nesnesi, çıktının DPI, sayfa boyutları ve varlık tiplerini kontrol eder.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` noktalar (point) cinsinden ölçülür (1 pt = 1/72 in).  
- 3‑B rasterleştirme için `setTypeOfEntities` satırının yorumunu kaldırın.  
- `setLayouts`, hangi düzenin (Model, Layout1, vb.) render edileceğini seçer.

### Adım 4: PDF seçeneklerini yapılandırın

Rasterleştirme ayarlarını PDF çıktısına bağlayarak, vektör verisinin doğru şekilde dönüştürülmesini sağlayın.

`PdfOptions` sınıfı, rasterleştirme yapılandırmasını son PDF dosyasıyla ilişkilendirir.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Adım 5: PDF'yi kaydedin

Oluşan dosya, `Export3DImagestoPDF_out_.pdf`, orijinal AutoCAD çiziminizin **CAD'i PDF olarak kaydet** temsilidır.

`save` metodu rasterleştirilmiş görüntüyü diskte bir PDF dosyasına yazar.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## Yaygın sorunlar ve çözümler

| Belirti | Muhtemel neden | Çözüm |
|---------|----------------|-------|
| Boş PDF çıktısı | Rasterleştirme seçenekleri ayarlanmamış veya düzen eşleşmiyor | `setLayouts` değerinin CAD dosyanızdaki düzen adıyla eşleştiğini doğrulayın. |
| Düşük çözünürlüklü görüntü | `pageWidth`/`pageHeight` çok küçük | Boyutları artırın veya `rasterizationOptions.setResolution(...)` ile daha yüksek DPI ayarlayın. |
| Lisans istisnası | Geçerli bir lisans uygulanmadı | Bir **Aspose CAD lisansı** uygulayın veya test için geçici bir lisans kullanın. |

## Sıkça Sorulan Sorular

**S: Aspose.CAD for Java'yu diğer CAD dosya formatlarıyla kullanabilir miyim?**  
C: Evet – kütüphane DWG, DXF, DWF, DGN ve 30'dan fazla ek formatı destekler, projeler arasında esneklik sağlar.

**S: Aspose.CAD for Java için geçici bir lisans nasıl alabilirim?**  
C: Değerlendirme amaçlı zaman sınırlı bir lisans talep etmek için [temporary license page](https://purchase.aspose.com/temporary-license/) adresini ziyaret edin.

**S: Rasterleştirme için düzen seçenekleri var mı?**  
C: Kesinlikle. PDF'ye hangi görünümün render edileceğini seçmek için `setLayouts("Model")`, `setLayouts("Layout1")` vb. kullanın.

**S: Çıktı PDF dosyasının boyutunu değiştirebilir miyim?**  
C: Evet – gerekli sayfa boyutlarına uyması için rasterleştirme seçeneklerinde `pageWidth` ve `pageHeight` değerlerini değiştirin.

**S: Sorun yaşarsam nereden yardım alabilirim?**  
C: Sorular sorabileceğiniz ve çözümler paylaşabileceğiniz [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresinde özel bir topluluk mevcuttur.

---

**Son Güncelleme:** 2026-10-19  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.10  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Java'da DWG'yi PDF'ye Dışa Aktar – PDF Sayfa Boyutunu Aspose.CAD ile Ayarla](/cad/java/cad-export-options/export-to-pdf/)
- [DWG'yi PDF'ye Dışa Aktar: Aspose.CAD for Java Kullanarak Belirli Düzen](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [DWG'yi PDF'ye Dışa Aktar ve Aspose.CAD Java ile İzlemeyi Etkinleştir](/cad/java/additional-features/enable-tracking/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}