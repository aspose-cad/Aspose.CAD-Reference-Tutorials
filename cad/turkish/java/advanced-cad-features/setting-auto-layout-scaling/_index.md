---
date: 2026-08-29
description: Aspose.CAD for Java kullanarak özel bir pdf sayfa boyutu ayarlamayı ve
  CAD'den PDF oluşturmayı öğrenin. Bu adım adım rehber, Auto Layout Scaling ile CAD'den
  PDF dışa aktarımını kapsar.
keywords:
- custom pdf page size
- create pdf from cad
- dwg to pdf java
- custom page size pdf
- java convert cad pdf
lastmod: 2026-08-29
linktitle: Auto Layout Scaling'i Ayarlama
og_description: Aspose.CAD for Java ile CAD dosyalarını PDF'ye dönüştürürken özel
  bir pdf sayfa boyutu ayarlayın. Auto Layout Scaling'i kullanmak ve mükemmel düzen
  sonuçları elde etmek için adım adım rehberi izleyin.
og_image_alt: 'Tutorial: set custom pdf page size for CAD to PDF conversion using
  Aspose.CAD Java'
og_title: CAD PDF dışa aktarımı için özel pdf sayfa boyutu ayarlayın – Aspose.CAD
  Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  headline: How to set custom pdf page size for CAD PDF export
  type: TechArticle
- description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  name: How to set custom pdf page size for CAD PDF export
  steps:
  - name: load the CAD file
    text: Loading the source file is the first step in **how to export CAD** to a
      PDF document.
  - name: create rasterization options
    text: The `CadRasterizationOptions` class defines how the CAD drawing is rasterized
      and which page dimensions to use. It also lets you control DPI, background color,
      and other rendering details.
  - name: set auto layout scaling
    text: Enable the automatic scaling feature. This is the core of **how to set scaling**
      for a CAD‑to‑PDF conversion.
  - name: create PDF options
    text: Link the rasterization settings to the PDF export options.
  - name: export to PDF
    text: Finally, save the rendered image as a PDF file. This step completes the
      **convert dxf to pdf** workflow. Repeat the steps above for any additional CAD
      files you need to process, whether they are **DWG**, **DWF**, or other supported
      formats.
  type: HowTo
- questions:
  - answer: Aspose.CAD for Java supports a broad range of formats, including DWG,
      DXF, DWF, and more than 30 additional CAD types.
    question: Is Aspose.CAD for Java compatible with all CAD file formats?
  - answer: Yes, the `CadRasterizationOptions` class provides properties for fine‑tuning
      scaling, DPI, background color, and other rasterization settings.
    question: Can I customize the scaling options further?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      in‑depth information and examples.
    question: Where can I find additional documentation for Aspose.CAD for Java?
  - answer: Yes, you can explore a [free trial](https://releases.aspose.com/) to experience
      the capabilities of Aspose.CAD for Java.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect
      with the community and seek support.
    question: How can I seek assistance or engage in discussions about Aspose.CAD
      for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
title: CAD PDF dışa aktarımı için özel pdf sayfa boyutu nasıl ayarlanır
url: /tr/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Özel PDF sayfa boyutu ayarla – CAD'den otomatik yerleşim ölçeklendirme ile PDF oluştur

## Giriş

Özel bir **set a custom pdf page size** ... **create PDF from CAD** ... dosyalarını hızlı ve mükemmel ölçeklendirme ile yapmak istediğinizde, Aspose.CAD for Java ihtiyacınızı karşılar. Auto Layout Scaling, CAD yerleşimlerini hedef sayfa boyutlarına otomatik olarak yeniden boyutlandırarak, ortaya çıkan PDF'nin kaynak çizime bakılmaksızın istenen sayfa boyutuyla eşleşmesini sağlar. Bu öğreticide, DXF dosyasını yüklemekten PDF'ye dışa aktarmaya kadar tam süreci adım adım inceleyecek, kütüphanenin **export CAD to PDF** yeteneklerini vurgulayacak ve ayrıca **convert DWG to PDF** veya **increase PDF resolution** gibi işlemleri nasıl yapabileceğinizi göstereceğiz.

## Hızlı cevaplar
- **What does Auto Layout Scaling do?** Rasterleştirirken, CAD yerleşimlerini hedef sayfa boyutlarına otomatik olarak yeniden boyutlandırır.  
- **Which CAD formats can I convert?** Aspose.CAD tarafından desteklenen herhangi bir format (ör. DXF, DWG, DWF) PDF'ye dönüştürülebilir.  
- **Do I need a license for production?** Evet, değerlendirme dışı kullanım için ticari bir lisans gereklidir.  
- **How long does a typical conversion take?** Modern donanımlarda standart bir dosya bir saniyeden kısa sürede dönüştürülür.  
- **Can I change the page size?** Kesinlikle – özel sayfa boyutlarını ayarlamak için `CadRasterizationOptions` kullanın.

## “CAD'den PDF oluşturma” nedir?

CAD'den PDF oluşturmak, vektör tabanlı bir mühendislik çizimini (DXF, DWG vb.) alıp bir PDF belgesine rasterleştirmek anlamına gelir. PDF, orijinal çizimin görsel doğruluğunu korurken, herhangi bir platformda geniş çapta görüntülenebilir ve yerel CAD formatlarını desteklemeyen cihazlarda da açılabilir.

## Neden otomatik yerleşim ölçeklendirmesi kullanılır?

Auto Layout Scaling, her yerleşimin PDF sayfasını manuel hesaplamalar olmadan tamamen doldurulmasını garanti eder, zaman kazandırır ve ölçekleme hatalarını ortadan kaldırır. Ayrıca, çizgi kalınlıkları ve renklerin farklı çıktı boyutları arasında doğru bir şekilde korunmasını sağlar. Onlarca CAD dosyasında tutarlı, yüksek kaliteli çıktı sunar ve büyük projeler için toplu işleme desteği verir.

## Önkoşullar

1. **Aspose.CAD for Java Library** – en son sürümü [download page](https://releases.aspose.com/cad/java/) adresinden indirin.  
2. **Resource directory** – makinenizde CAD dosyalarını saklamak için bir klasör oluşturun; kodda `"Your Document Directory"` ifadesini bu yol ile değiştirin.  
3. **Sample CAD file** – bu kılavuz için `conic_pyramid.dxf` dosyasını kullanacağız; bu dosya Aspose örnek veri setine dahildir.

## Ad alanlarını içe aktar

İlk olarak, gerekli sınıfları içe aktarın. Bu, görüntü yükleme, rasterleştirme ve PDF dışa aktarma özelliklerine erişim sağlar.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## CAD'den PDF için özel sayfa boyutu nasıl ayarlanır

Adım adım koda geçmeden önce, özel sayfa boyutlarının neden önemli olduğunu açıklayalım. **custom pdf page size** ayarlamak, endüstri standardı kağıt boyutları (A4, A1, Letter) ile eşleşmenizi veya özel bir tuval tanımlamanızı sağlar; bu, düzenleyici başvurular, teknik kılavuzlar veya yüksek çözünürlüklü baskı işleri için gereklidir.

### Adım 1: CAD dosyasını yükle

Kaynak dosyayı yüklemek, **how to export CAD** bir PDF belgesine dönüştürme sürecinin ilk adımıdır.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Adım 2: rasterleştirme seçeneklerini oluştur

`CadRasterizationOptions` sınıfı, CAD çiziminin nasıl rasterleştirileceğini ve hangi sayfa boyutlarının kullanılacağını tanımlar. Ayrıca DPI, arka plan rengi ve diğer render detaylarını kontrol etmenizi sağlar.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Adım 3: otomatik yerleşim ölçeklendirmesini ayarla

Otomatik ölçeklendirme özelliğini etkinleştirin. Bu, CAD‑to‑PDF dönüşümü için **how to set scaling** özelliğinin çekirdeğidir.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Adım 4: PDF seçeneklerini oluştur

Rasterleştirme ayarlarını PDF dışa aktarma seçeneklerine bağlayın.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Adım 5: PDF'ye dışa aktar

Son olarak, işlenen görüntüyü bir PDF dosyası olarak kaydedin. Bu adım **convert dxf to pdf** iş akışını tamamlar.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

İşlemeniz gereken ek CAD dosyaları için yukarıdaki adımları tekrarlayın; dosyalar **DWG**, **DWF** veya diğer desteklenen formatlarda olabilir.

## Yaygın kullanım senaryoları

| Senaryo | Neden özel bir sayfa boyutu ayarlansın? |
|----------|----------------------------------------|
| **Construction drawing submission** | PDF'yi düzenleyici kurumların talep ettiği standart A1/A2 kağıt boyutlarıyla hizalar. |
| **Embedding in technical manuals** | Çizimin, ek ölçekleme olmadan kılavuzun önceden tanımlı düzenine sığmasını garanti eder. |
| **High‑resolution printing** | Sayfa boyutlarını tutarlı tutarken DPI'yi artırmanıza (ör., `rasterizationOptions.setResolution(300)`) izin verir. |

## Yaygın sorunlar ve sorun giderme

| Belirti | Muhtemel neden | Çözüm |
|---------|----------------|-------|
| Boş PDF çıktısı | Rasterleştirme seçenekleri ayarlanmamış veya dosya yolu hatalı | `srcFile` yolunu doğrulayın ve `setPageWidth/Height` değerlerinin sıfır olmadığından emin olun |
| Bozulmuş ölçekleme | `setAutomaticLayoutsScaling` false olarak bırakılmış | Otomatik ölçeklendirmeyi etkinleştirin veya ölçek faktörünü manuel olarak hesaplayın |
| Eksik katmanlar | Kaynak DXF desteklenmeyen varlıklar içeriyor | Desteklenen varlık tipleri için Aspose.CAD sürüm notlarını kontrol edin |

Aspose.CAD, **30+ CAD formats** dönüşümünü destekler ve **500 MB**'a kadar dosyaları belgenin tamamını belleğe yüklemeden işleyebilir, kurumsal iş yükleri için hızlı, bellek‑verimli dönüşümler sunar.

## Sıkça Sorulan Sorular

**Q: Aspose.CAD for Java tüm CAD dosya formatlarıyla uyumlu mu?**  
A: Aspose.CAD for Java, DWG, DXF, DWF ve 30'dan fazla ek CAD türü dahil olmak üzere geniş bir format yelpazesini destekler.

**Q: Ölçeklendirme seçeneklerini daha da özelleştirebilir miyim?**  
A: Evet, `CadRasterizationOptions` sınıfı, ölçeklendirme, DPI, arka plan rengi ve diğer rasterleştirme ayarlarını ince ayar yapabilmeniz için özellikler sunar.

**Q: Aspose.CAD for Java için ek belgeleri nerede bulabilirim?**  
A: Derinlemesine bilgi ve örnekler için [documentation](https://reference.aspose.com/cad/java/) adresine bakın.

**Q: Aspose.CAD for Java için ücretsiz deneme mevcut mu?**  
A: Evet, Aspose.CAD for Java'un yeteneklerini deneyimlemek için bir [free trial](https://releases.aspose.com/) keşfedebilirsiniz.

**Q: Aspose.CAD for Java hakkında yardım almak veya tartışmalara katılmak nasıl mümkün?**  
A: Toplulukla bağlantı kurmak ve destek almak için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

**Ek yaygın sorular**

**Q: DXF yerine DWG dosyasını PDF'ye nasıl dönüştürebilirim?**  
A: Aynı kod çalışır; sadece `srcFile` içindeki dosya uzantısını `.dwg` olarak değiştirin.

**Q: Daha yüksek çözünürlüklü PDF'ler için özel DPI ayarlayabilir miyim?**  
A: Evet, `rasterizationOptions.setResolution(300);` (veya ihtiyacınız olan herhangi bir DPI) kullanın.

**Q: Oluşturulan PDF'ye fontları gömmek mümkün mü?**  
A: Aspose.CAD çizimi rasterleştirir, bu yüzden fontlar vektör olarak işlenir; ayrı bir font gömme gerekli değildir.

## Sonuç

Bu kılavuzu izleyerek artık Aspose.CAD for Java ile Auto Layout Scaling kullanarak **set custom pdf page size** ve **create PDF from CAD** dosyalarını nasıl yapacağınızı biliyorsunuz. İşlem, **export CAD to PDF** iş akışını basitleştirir, tutarlı ölçeklendirme sağlar ve değerli geliştirme zamanınızı tasarruf eder. Proje ihtiyaçlarınıza uygun olarak farklı sayfa boyutları, çözünürlükler ve CAD formatlarıyla denemeler yapmaktan çekinmeyin; ister **converting DWG to PDF**, **increasing PDF resolution**, ister **java CAD to PDF** toplu işlemci oluşturuyor olun.

---

**Son güncelleme:** 2026-08-29  
**Test edildiği sürüm:** Aspose.CAD for Java 24.12 (latest)  
**Yazar:** Aspose

## İlgili Öğreticiler

- [Aspose.CAD for Java kullanarak CAD Render İşleminde PDF Sayfa Boyutu Ayarlama ve İzleme Etkinleştirme](/cad/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/)
- [PDF Sayfa Boyutunu Ayarla – CAD'yi PDF'ye Dönüştür (Java)](/cad/java/advanced-cad-features/set-canvas-size-and-mode/)
- [Java CAD kütüphanesi Aspose.CAD for Java kullanarak DWG'yi PDF'ye veya Raster'e Hızlıca Dışa Aktar](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}