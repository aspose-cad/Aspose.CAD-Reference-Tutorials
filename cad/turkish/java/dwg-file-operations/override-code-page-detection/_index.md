---
date: 2026-05-20
description: Aspose.CAD for Java kullanarak otomatik kod sayfası algılamasını geçersiz
  kılarak DWG'yi PDF'ye nasıl dönüştüreceğinizi öğrenin. DWG'den PDF'ye dışa aktarma
  adımları, kodlama ipuçları ve sorun giderme konularını içerir.
keywords:
- convert dwg pdf
- export dwg to pdf
- Aspose.CAD Java
linktitle: DWG Dosyalarında Otomatik Kod Sayfası Algılamasını Geçersiz Kıl
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  headline: Convert DWG to PDF – Override Code Page Detection in Java
  type: TechArticle
- description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  name: Convert DWG to PDF – Override Code Page Detection in Java
  steps:
  - name: Set Up the Java Project
    text: Create a Maven or Gradle project and add the Aspose.CAD JAR to the classpath.
      This ensures the IDE can resolve the imported classes and that the runtime can
      locate the library.
  - name: Load the DWG File with a Specified Code Page
    text: Tell Aspose.CAD which encoding to use and whether to attempt recovery of
      malformed CIF/MIF data.
  - name: Export the CAD Image to PDF
    text: With the correct code page applied, you can safely export the drawing. The
      `PdfOptions` object lets you fine‑tune the PDF output (compression, rasterization,
      etc.).
  - name: Verify Success
    text: A simple console message confirms that the process completed without exceptions.
      You can repeat these steps for multiple DWG files, adjusting the source path
      and output name as needed.
  type: HowTo
- questions:
  - answer: It forces Aspose.CAD to use a specific character encoding instead of guessing.
    question: What does “override code page” mean?
  - answer: Yes – after setting the correct code page, you can save the CAD image
      as PDF.
    question: Can I export DWG directly to PDF?
  - answer: '`CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.'
    question: Which encoding works for Japanese text?
  - answer: A commercial license is required; a temporary license is available for
      testing.
    question: Do I need a license for production use?
  - answer: Any recent version that supports `LoadOptions` and `PdfOptions`.
    question: What version of Aspose.CAD is needed?
  type: FAQPage
second_title: Aspose.CAD Java API
title: DWG'yi PDF'ye Dönüştür – Java'da Kod Sayfası Algılamasını Geçersiz Kıl
url: /tr/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi PDF'ye Dönüştür – Java'da Kod Sayfası Algılamasını Geçersiz Kıl

Bu kapsamlı öğreticide **DWG'yi PDF'ye nasıl dönüştüreceğinizi** öğreneceksiniz, metni bozabilen otomatik kod sayfası algılamasını geçersiz kılarak. Aspose.CAD for Java, karakter kodlaması üzerinde kesin kontrol sağlar, bozuk CIF/MIF verilerini kurtarmanıza ve güvenilir PDF çıktısı üretmenize olanak tanır. İster toplu bir dönüştürücü oluşturuyor olun, ister CAD işleme özelliğini daha büyük bir Java hizmetine ekliyor olun, aşağıdaki adımlar sizi proje kurulumundan doğrulamaya kadar tüm iş akışı boyunca yönlendirecek.

## Hızlı Yanıtlar
- **“override code page” ne anlama gelir?** Aspose.CAD'in tahmin etmek yerine belirli bir karakter kodlamasını kullanmasını zorlar.
- **DWG'yi doğrudan PDF'ye dışa aktarabilir miyim?** Evet – doğru kod sayfasını ayarladıktan sonra CAD görüntüsünü PDF olarak kaydedebilirsiniz.
- **Japonca metin için hangi kodlama çalışır?** `CodePages.Japanese` ve `MifCodePages.Japanese` doğru seçimlerdir.
- **Üretim kullanımı için lisansa ihtiyacım var mı?** Ticari bir lisans gereklidir; test için geçici bir lisans mevcuttur.
- **Hangi Aspose.CAD sürümü gerekiyor?** `LoadOptions` ve `PdfOptions` destekleyen herhangi bir yeni sürüm.

## “CAD'yi PDF'ye dışa aktarma” nedir?
CAD'yi PDF'ye dışa aktarmak, vektör tabanlı bir DWG çizimini evrensel olarak görüntülenebilir, sabit düzenli bir PDF belgesine dönüştürür. Dönüşüm, tüm geometrik varlıkları, çizgi çalışmaları, katmanları ve gömülü metni korurken, çizimi CAD yazılımı gerektirmeden kolayca paylaşılabilir, yazdırılabilir, arşivlenebilir veya diğer uygulamalara gömülebilir bir formata düzleştirir.

## Otomatik kod sayfası algılamasını neden geçersiz kılmalıyız?
Kod sayfasını manuel olarak belirtmek, metin baytlarının doğru yorumlanmasını garanti eder ve Aspose.CAD'in otomatik algılamasının yanlış eski kodlamayı tahmin etmesiyle sıkça ortaya çıkan bozuk karakterleri ortadan kaldırır. Bu, Japonca, Kiril veya Arapça gibi Latin dışı yazı sistemleri için hayati öneme sahiptir ve dışa aktarılan PDF'nin orijinal tasarımla eşleşmesini sağlar.

## Önkoşullar
- **Java Geliştirme Ortamı** – JDK 8+ ve tercih ettiğiniz IDE.  
- **Aspose.CAD for Java** – Kütüphaneyi resmi siteden [buradan](https://releases.aspose.com/cad/java/) indirin.  
- **DWG Örnek Dosyası** – Sağlanan `SimpleEntities.dwg` dosyasını veya dönüştürmek istediğiniz herhangi bir DWG dosyasını kullanın.

## Paketleri İçe Aktarma
`Document`, `LoadOptions` ve `PdfOptions` sınıfları dönüşüm sürecinin çekirdeğidir.

`Document` sınıfı, bellekte bir CAD çizimini temsil eder ve dosyayı çeşitli formatlarda yükleme, manipüle etme ve kaydetme yöntemleri sağlar.  
`LoadOptions` sınıfı, DWG dosyası yüklenirken kod sayfasını ve kurtarma seçeneklerini belirtmenizi sağlar.  
`PdfOptions` sınıfı, sıkıştırma, rasterleştirme ve meta veri gibi PDF'ye özgü ayarları kontrol eder.

Java projenizde, gerekli Aspose.CAD sınıflarını içe aktarın:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Kod sayfası geçersiz kılma ile DWG'yi PDF'ye nasıl dönüştürülür?
`LoadOptions` kullanarak DWG dosyasını yükleyin ve tam kod sayfasını belirtin, ardından yapılandırılmış bir `PdfOptions` örneğiyle elde edilen `CadImage` üzerinde `save` metodunu çağırın. Bu iki adımlı yaklaşım, metnin doğru yorumlanmasını ve oluşturulan PDF'nin orijinal çizimin doğruluğunu, katmanlarını ve vektör kalitesini korumasını sağlar.

### Adım 1: Java Projesini Kurun
Bir Maven veya Gradle projesi oluşturun ve Aspose.CAD JAR dosyasını sınıf yoluna ekleyin. Bu, IDE'nin içe aktarılan sınıfları çözümleyebilmesini ve çalışma zamanının kütüphaneyi bulabilmesini sağlar.

### Adım 2: Belirtilen Kod Sayfası ile DWG Dosyasını Yükleyin
Aspose.CAD'e hangi kodlamayı kullanacağını ve bozuk CIF/MIF verilerinin kurtarılmaya çalışılıp çalışılmayacağını söyleyin.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Adım 3: CAD Görüntüsünü PDF'ye Dışa Aktarın
Doğru kod sayfası uygulandığında, çizimi güvenle dışa aktarabilirsiniz. `PdfOptions` nesnesi, PDF çıktısını (sıkıştırma, rasterleştirme vb.) ince ayar yapmanıza olanak tanır.

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Adım 4: Başarıyı Doğrulayın
Basit bir konsol mesajı, işlemin istisna olmadan tamamlandığını doğrular.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Bu adımları birden fazla DWG dosyası için tekrarlayabilir, kaynak yolunu ve çıktı adını gerektiği gibi ayarlayabilirsiniz.

## Yaygın Sorunlar ve Çözümler
- **Garbage karakterler hâlâ görünüyor:** `specifiedEncoding`'in orijinal DWG'nin kod sayfasıyla eşleştiğini iki kez kontrol edin. Gerekirse farklı bir `CodePages` enum'u kullanın.  
- **`cadImage.save` sırasında `NullPointerException`:** DWG dosyasının doğru yüklendiğinden emin olun; yol ve dosya izinlerini doğrulayın.  
- **PDF boyutu büyük:** Kaliteden ödün vermeden dosya boyutunu azaltmak için `PdfOptions` içinde sıkıştırmayı etkinleştirin (örneğin, `pdfOptions.setCompress(true)`).

## Sıkça Sorulan Sorular

**S1: Aspose.CAD tüm DWG dosya sürümleriyle uyumlu mu?**  
C1: Aspose.CAD, AutoCAD 2018 ve daha eski sürümler dahil olmak üzere 30'dan fazla DWG sürümünü destekler.

**S2: Aspose.CAD'i ticari projelerde kullanabilir miyim?**  
C2: Evet, üretim kullanımı için ticari bir lisans gereklidir. Lisansı [buradan](https://purchase.aspose.com/buy) alabilirsiniz.

**S3: Ücretsiz deneme sürümünde herhangi bir sınırlama var mı?**  
C3: Deneme sürümü boyut ve özellik kısıtlamaları getirir; ayrıntılar için resmi belgeleri inceleyin.

**S4: Aspose.CAD için destek nasıl alabilirim?**  
C4: Yardım ve tartışmalar için topluluk [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

**S5: Test amaçlı geçici bir lisans mevcut mu?**  
C5: Evet, geçici bir lisans [buradan](https://purchase.aspose.com/temporary-license/) talep edilebilir.

---

**Son Güncelleme:** 2026-05-20  
**Test Edilen:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Yazar:** Aspose

## İlgili Öğreticiler

- [DWG'yi PDF'ye Dışa Aktar ve CAD Çizimlerini Dönüştür – Aspose.CAD Java Öğreticisi](/cad/java/cad-drawing-conversion/)
- [Aspose.CAD for Java Kullanarak Belirli DWG Düzenini PDF'ye Dışa Aktar](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Aspose.CAD for Java Kullanarak DWG'yi PDF'ye veya Raster'e Dışa Aktar](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}