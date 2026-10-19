---
date: 2026-10-19
description: Aspose.CAD for Java kullanarak AutoCAD çizimlerini özel PDF sayfa boyutu
  ile PDF'ye nasıl dışa aktaracağınızı öğrenin. Bu adım adım rehber, DWG'den PDF'ye
  dönüştürme, rasterleştirme seçenekleri ve lisanslama konularını kapsar.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: AutoCAD Görüntülerini PDF'ye Dışa Aktar
og_description: Aspose.CAD for Java kullanarak AutoCAD çizimlerini PDF'ye dışa aktarırken
  özel bir PDF sayfa boyutu ayarlayın. DWG'den PDF'ye dönüşüm, rasterleştirme ayarları
  ve lisanslama hakkında dakikalar içinde bilgi edinin.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Aspose.CAD ile AutoCAD dışa aktarımında özel PDF sayfa boyutu ayarlayın
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Aspose.CAD ile AutoCAD dışa aktarımında özel PDF sayfa boyutu ayarlayın
url: /tr/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# AutoCAD PDF Dışa Aktarma - Aspose.CAD for Java ile AutoCAD görüntülerini PDF olarak dışa aktar

## Giriş

DWG'yi **PDF'ye dönüştürmeniz** ve çıktı dosyasının tam boyutlarını kontrol etmeniz gerekiyorsa, doğru yerdesiniz. Bu öğreticide, Aspose.CAD for Java ile AutoCAD görüntülerini PDF olarak dışa aktarırken **özel PDF sayfa boyutu** nasıl ayarlanacağını gösteriyoruz. Kılavuzun sonunda, bir DWG'yi nasıl yükleyeceğinizi, DPI ve sayfa genişliği/yüksekliği gibi rasterleştirme seçeneklerini nasıl yapılandıracağınızı, bir lisans uygulayacağınızı ve üretime hazır bir PDF oluşturacağınızı öğreneceksiniz.

## Hızlı cevaplar
- **Java ile DWG'yi PDF'ye dönüştürebilir miyim?** Evet – Aspose.CAD for Java, DWG, DXF, DWF ve birçok diğer CAD formatını yerel olarak destekler.  
- **Üretim kullanımında lisansa ihtiyacım var mı?** Tam bir Aspose.CAD lisansı tüm değerlendirme sınırlamalarını kaldırır; test için geçici bir lisans mevcuttur.  
- **Hangi Java sürümleri uyumludur?** Kütüphane Java 8 ve sonraki tüm JDK'larla çalışır.  
- **PDF sayfa boyutlarını nasıl değiştiririm?** `PdfOptions.getRasterizationOptions()` üzerindeki `pageWidth` ve `pageHeight` değerlerini istediğiniz boyuta ayarlayın.  
- **3‑B renderleme destekleniyor mu?** Evet – 3‑B varlıkları rasterleştirmek için `TypeOfEntities.Entities3D` özelliğini etkinleştirin.

## AutoCAD PDF Dışa Aktarma Nedir?
AutoCAD PDF dışa aktarma, vektör tabanlı CAD çizimlerini (DWG, DXF, DWF vb.) katmanları, hat kalınlıklarını ve isteğe bağlı 3‑B geometrisini koruyarak taşınabilir bir PDF belgesine dönüştürmek anlamına gelir. Bu, tasarımları müşterilerle paylaşmanızı, çizimleri arşivlemenizi veya CAD yazılımı kurmadan yazdırmanızı sağlar.

## DWG'yi PDF'ye dönüştürmek için neden Aspose.CAD for Java kullanılmalı?
Aspose.CAD for Java, DWG'yi PDF'ye dönüştürmek için idealdir çünkü geniş format desteği sunar, yerel bağımlılıklar olmadan saf Java üzerinde çalışır, DPI ve sayfa boyutu üzerinde tam kontrol sağlayan yüksek çözünürlüklü rasterleştirme sunar ve deneme sürümüyle başlayıp üretime ölçeklendirebileceğiniz esnek bir lisanslama içerir.

- **Geniş format kapsamı** – DWG, DXF, DWF, DGN ve PDF dahil olmak üzere 50+ giriş ve çıkış formatını destekler.  
- **Saf Java uygulaması** – yerel DLL'ler veya dış bağımlılıklar yoktur, bu yüzden dağıtım herhangi bir platformda basittir.  
- **Yüksek çözünürlüklü rasterleştirme** – DPI, sayfa boyutu ve düzeni belirtebilir, sonuçta **özel PDF sayfa boyutu** üzerinde tam kontrol sağlar.  
- **Ölçeklenebilir lisanslama** – ücretsiz bir deneme ile başlayın, ardından kalıcı bir **Aspose CAD lisansı**na yükseltin.  

## Önkoşullar

- **Java Development Kit** – Makinenizde JDK 8 veya daha yeni bir sürüm yüklü olmalıdır.  
- **Aspose.CAD for Java** – En son JAR'ı [download link](https://releases.aspose.com/cad/java/) adresinden indirin.  
- **Çalışma dizini** – kaynak DWG dosyalarını içeren ve oluşturulan PDF'lerin kaydedileceği bir klasör.  

## Ad alanlarını içe aktar

`Image` sınıfı, Aspose.CAD'ın bellekte bir CAD çizimini temsil eden çekirdek nesnesidir. Kodlamaya başlamadan önce gerekli paketleri içe aktarın.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Şimdi kodu adım adım inceleyelim.

## DWG'yi PDF'ye dışa aktarırken özel PDF sayfa boyutu nasıl ayarlanır?

DWG'nizi yükleyin, istenen sayfa genişliğini ve yüksekliğini tanımlayın ve ardından sonucu PDF olarak kaydedin – özel bir sayfa boyutuna sahip PDF oluşturmak için ihtiyacınız olan tek şey bu. Aşağıdaki adımlar tam sıralamayı ve gereken minimum kodu gösterir.

### Adım 1: kaynak dizin yolunu ayarla

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro ipucu:** `"Your Document Directory"` ifadesini önkoşullarda oluşturduğunuz klasörün mutlak yolu ile değiştirin.

### Adım 2: CAD görüntüsünü yükle

`Image` sınıfı CAD dosyasını yükler ve Aspose.CAD'ın rasterleştirme motoruna erişim sağlar.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Neden önemli:** CAD dosyası yüklendikten sonra PDF'ye render etmeden önce rasterleştirme seçeneklerini manipüle edebilirsiniz.

### Adım 3: rasterleştirme seçeneklerini ayarla

`CadRasterizationOptions` sınıfı, CAD çiziminin PDF olarak kaydedilmeden önce nasıl rasterleştirileceğini belirler. **Özel PDF sayfa boyutu** tanımlamak için `pageWidth` ve `pageHeight` değerlerini ayarlayın. Ayrıca `setTypeOfEntities` satırının yorumunu kaldırarak 3‑B renderlemeyi etkinleştirebilirsiniz.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – piksel cinsinden ölçülür; bu değerleri A4, Letter veya herhangi bir özel boyuta uyacak şekilde değiştirin.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – gerektiğinde 3‑B varlıkları render eder.  
- `setLayouts` – rasterleştirilecek düzeni (Model, Layout1 vb.) seçer.

### Adım 4: PDF seçeneklerini yapılandır

`PdfOptions` sınıfı PDF'ye özgü ayarları tutar ve rasterleştirme seçeneklerini çıktı dosyasına bağlayarak özel sayfa boyutlarının doğru şekilde uygulanmasını sağlar.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Adım 5: PDF'yi kaydet

`save` yöntemi render edilen görüntüyü belirtilen PDF dosyasına yazar.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Ortaya çıkan dosya, `Export3DImagestoPDF_out_.pdf`, orijinal AutoCAD çiziminizin **save cad as pdf** temsili olup, belirttiğiniz tam sayfa boyutlarına sahiptir.

## Yaygın sorunlar ve çözümler

| Semptom | Muhtemel neden | Çözüm |
|---------|----------------|-------|
| Boş PDF çıktısı | Rasterleştirme seçenekleri ayarlanmamış veya düzen eşleşmiyor | CAD dosyanızdaki düzen adıyla `setLayouts`'in eşleştiğini doğrulayın. |
| Düşük çözünürlüklü görüntü | `pageWidth`/`pageHeight` çok küçük veya DPI düşük | Boyutları artırın veya daha yüksek DPI ile `rasterizationOptions.setResolution(...)` çağırın. |
| Lisans istisnası | Geçerli bir lisans uygulanmadı | Kalıcı bir Aspose.CAD lisansı uygulayın veya test için geçici bir lisans kullanın. |

## Sıkça sorulan sorular

**Q: Aspose.CAD for Java'yi diğer CAD dosya formatlarıyla kullanabilir miyim?**  
**A:** Evet, kütüphane DWG, DXF, DWF, DGN ve daha fazlasını destekler, projelerinizde esneklik sağlar.

**Q: Aspose.CAD for Java için geçici bir lisans nasıl alabilirim?**  
**A:** Değerlendirme amaçlı zaman sınırlı bir lisans talep etmek için [temporary license page](https://purchase.aspose.com/temporary-license/) adresini ziyaret edin.

**Q: Rasterleştirme için düzen seçenekleri var mı?**  
**A:** Kesinlikle. Hangi görünümün render edileceğini kontrol etmek için `setLayouts("Model")` kullanın veya diğer düzen adlarını belirtin.

**Q: Çıktı PDF dosyasının boyutunu özelleştirebilir miyim?**  
**A:** Evet – rasterleştirme seçeneklerinde `pageWidth` ve `pageHeight` değerlerini ihtiyacınız olan herhangi bir boyuta değiştirin.

**Q: Aspose.CAD for Java ile ilgili yardım alabileceğim veya sorunları tartışabileceğim yer neresi?**  
**A:** Ayrı bir [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) topluluk desteği ve Aspose ekibinden resmi yanıtlar sunar.

## Ek SSS (AI‑dostu format)

**Q: Aspose.CAD Windows veya Linux'ta herhangi bir yerel kütüphane gerektiriyor mu?**  
**A:** Hayır. Aspose.CAD for Java saf‑Java bir kütüphanedir, bu yüzden ek yerel DLL'ler olmadan JDK'yı destekleyen herhangi bir platformda çalışır.

**Q: Kütüphane ne kadar büyük bir DWG dosyasını işleyebilir?**  
**A:** Kütüphane, akış mimarisi sayesinde tüm dosyayı belleğe yüklemeden çok sayfalı çizimleri (500 MB'a kadar) işleyebilir.

**Q: Tek bir çalıştırmada birçok DWG dosyasını PDF'ye toplu olarak dönüştürmek mümkün mü?**  
**A:** Evet. Bir dizin üzerinde döngü kurarak, her dosyayı `Image.load()` ile yükleyin, aynı rasterleştirme seçeneklerini uygulayın ve her çıktı PDF için `save()` çağırın.

**Q: Tipik bir sunucuda ne tür bir performans bekleyebilirim?**  
**A:** Standart 2.5 GHz CPU'da 300 DPI'de 100 sayfalık bir DWG'yi dönüştürmek, Aspose'un benchmark testlerine göre yaklaşık 12 saniye sürer.

**Q: Kütüphane PDF'de katman bilgilerini korur mu?**  
**A:** Çıktı rasterleştirilmiş olsa da, katmanların, hat kalınlıklarının ve renklerin görsel görünümü eksiksiz olarak yeniden üretilir.

---

**Son Güncelleme:** 2026-10-19  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.10  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.CAD Java ile DWG'yi PDF'ye Dışa Aktar ve İzlemeyi Etkinleştir](/cad/java/additional-features/enable-tracking/)
- [Aspose.CAD Java Kullanarak DWG'yi PDF'ye Dışa Aktar: Belirli Düzen](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Aspose.CAD for Java ile DWG'yi BMP'ye Dışa Aktar ve Birim Tipi Kullanarak CAD Boyutunu Ayarla](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}