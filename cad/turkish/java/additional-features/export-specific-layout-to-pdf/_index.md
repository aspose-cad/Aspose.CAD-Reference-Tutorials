---
date: 2026-06-24
description: Aspose.CAD for Java kullanarak dxf'den pdf oluşturmayı, dxf'yi pdf'ye
  dışa aktarmayı, pdf sayfa boyutunu ayarlamayı ve cad'den pdf'yi hassas kontrol ile
  üretmeyi öğrenin.
keywords:
- create pdf from dxf
- export dxf to pdf
- set pdf page size
- convert dwg to pdf
- export cad drawing pdf
linktitle: Java ile Belirli DXF Layout'ı PDF'ye Dışa Aktar
schemas:
- author: Aspose
  dateModified: '2026-06-24'
  description: Learn how to create pdf from dxf and export dxf to pdf using Aspose.CAD
    for Java, set pdf page size, and generate pdf from cad with precise control.
  headline: Create pdf from dxf Layout to PDF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create pdf from dxf and export dxf to pdf using Aspose.CAD
    for Java, set pdf page size, and generate pdf from cad with precise control.
  name: Create pdf from dxf Layout to PDF with Aspose.CAD for Java
  steps:
  - name: Set the Resource Directory
    text: Define the folder that contains your DXF files. Replace the placeholder
      with the actual path on your machine. > **Pro tip:** Use `System.getProperty("user.dir")`
      to build a relative path that works across environments.
  - name: Load the DXF File
    text: Load the source DXF using `Image.load()`. `Image.load()` reads a CAD file
      and returns an `Image` object representing its contents. The `Image.load()`
      method parses the DXF structure and creates an in‑memory representation that
      can be rasterized or saved directly.
  - name: Configure Rasterization Options (Set PDF Page Width in Java)
    text: Here we create `CadRasterizationOptions` and define the output page size.
      `CadRasterizationOptions` specifies how CAD data is rasterized, including page
      size, DPI, and layout selection. `CadRasterizationOptions` controls how the
      CAD data is rendered—page size, DPI, background color, and which layout
  - name: Create PDF Options (Java Convert CAD PDF)
    text: Link the rasterization settings to a `PdfOptions` instance. `PdfOptions`
      tells Aspose.CAD to generate a PDF file using the provided rasterization settings.
      `PdfOptions` is the container that tells the library to produce a PDF file,
      applying the rasterization settings defined earlier.
  - name: Export DXF to PDF (Create PDF from DXF)
    text: Finally, save the image as a PDF. `Image.save()` writes the rendered content
      to a file in the format specified by the options. The `save` call writes the
      rendered content to disk using the PDF options, producing a vector‑preserving
      PDF. After execution, you’ll find `conic_pyramid_layout_out_.pdf` in
  type: HowTo
- questions:
  - answer: Absolutely. The API is straightforward for newcomers while offering deep
      customization for power users.
    question: Is Aspose.CAD for Java suitable for both beginners and experienced developers?
  - answer: Yes. Adjust `CadRasterizationOptions` (page size, DPI, background color)
      per layout as needed.
    question: Can I customize the rasterization options for different layouts?
  - answer: Detailed docs are available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find comprehensive documentation for Aspose.CAD for Java?
  - answer: Yes, you can download a trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Visit the support forum [here](https://forum.aspose.com/c/cad/19) for
      community and staff assistance.
    question: How can I get support for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java ile dxf Layout'tan PDF oluşturma
url: /tr/java/additional-features/export-specific-layout-to-pdf/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF'yi dxf Düzeninden PDF'ye Aspose.CAD for Java ile Oluşturma

## Giriş

CAD çizimleriyle çalışan bir Java geliştiricisiyseniz, **dxf dosyalarını nasıl dışa aktaracağınız**ın projeyi başarıya taşıyabileceğini ya da başarısızlığa sürükleyebileceğini biliyorsunuzdur. Mühendislik raporları oluşturuyor, tasarımları müşterilerle paylaşıyor ya da toplu dönüşümleri otomatikleştiriyor olun, güvenilir bir Java PDF dönüşüm kütüphanesi şarttır. Bu öğreticide **dxf düzen dosyalarından pdf oluşturma** sürecini, sayfa boyutlarını kontrol etmeyi ve vektör kalitesini korumayı **Aspose.CAD for Java** ile adım adım göstereceğiz.

## Hızlı Yanıtlar
- **Birincil kütüphane nedir?** Aspose.CAD for Java, CAD için özel bir Java PDF dönüşüm kütüphanesidir.
- **Belirli bir düzen seçebilir miyim?** Evet – `CadRasterizationOptions.setLayouts()` kullanarak bir düzen adını hedefleyebilirsiniz.
- **Sayfa boyutunu nasıl ayarlarım?** Rasterizasyon seçeneklerinde `setPageWidth()` ve `setPageHeight()` metodlarını ayarlayın (ör. 1600 × 1600).
- **Üretim için lisansa ihtiyacım var mı?** Üretim kullanımında ticari bir lisans gereklidir; ücretsiz bir deneme sürümü mevcuttur.
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri (JDK 1.8+).

## create pdf from dxf nedir?
DXF formatında saklanan bir CAD çizimini PDF belgesine dönüştürmek, vektör verilerini, katmanları ve düzen bilgilerini korumak anlamına gelir. **Aspose.CAD for Java**, ara raster adımlarına ihtiyaç duymadan bu dönüşümü tek bir çağrı ile gerçekleştirir.

## Neden Aspose.CAD for Java kullanmalı?
Aspose.CAD for Java, dış bağımlılıklar olmadan 30'dan fazla formatı destekleyen kapsamlı bir CAD desteği sunar ve DPI, sayfa boyutu ve düzen seçimi gibi özelleştirilebilir rasterizasyon seçenekleri sağlar. Yüksek performanslı motoru, vektör bütünlüğünü korurken hızlı toplu dönüşümlere olanak tanır; bu da sunucu‑tarafı ve bulut dağıtımları için idealdir.

- **Tam özellikli CAD desteği** – **30'dan fazla** CAD formatını, DWG, DXF, DWF, DGN ve DWT dahil, işler.
- **Harici bağımlılık yok** – Saf Java, yerel DLL gerektirmez; bu da Linux, Windows veya konteyner ortamlarında dağıtımı basitleştirir.
- **Kesin rasterizasyon** – Vektör ya da raster çıktı seçin, DPI, sayfa boyutu ve düzeni ayarlayın. Örneğin, kütüphane standart 2 çekirdekli bir sunucuda 500 sayfalık bir DXF'i 5 saniyeden kısa sürede işleyebilir.
- **Yüksek performans** – Toplu işleme için optimize edilmiştir; tek bir iş parçacığında 1.000 dosyayı 200 MB'den az heap kullanımıyla dönüştürebilir.
- **Export dxf to pdf** tek bir kod satırıyla yapılabilir, bu da **java convert cad pdf** iş akışları için idealdir.

## Önkoşullar

Başlamadan önce şunlara sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – Java 8 veya üzeri. İndir: [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2. **Aspose.CAD for Java** – En son JAR dosyasını [Aspose.CAD indirme sayfasından](https://releases.aspose.com/cad/java/) alın.
3. Projenizin sınıf yoluna Aspose.CAD JAR'ını eklemek için bir IDE veya yapı aracı (Maven/Gradle).

## İsim Uzaylarını İçe Aktarma

İhtiyacınız olan sınıfları içe aktarın. Bu importlar, görüntü yükleme, rasterizasyon seçenekleri ve PDF çıktı ayarlarına erişim sağlar.

`Image` sınıfı, Aspose.CAD'in bellekte bir CAD dosyasını temsil eden temel nesnesidir. İçeriği çeşitli formatlarda render etme ve kaydetme metodlarını sunar.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Adım‑Adım Kılavuz

### Adım 1: Kaynak Dizinini Ayarla

DXF dosyalarınızı içeren klasörü tanımlayın. Yer tutucuyu makinenizdeki gerçek yol ile değiştirin.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

> **Pro tip:** `System.getProperty("user.dir")` kullanarak ortamlar arasında çalışan bir göreli yol oluşturabilirsiniz.

### Adım 2: DXF Dosyasını Yükle

Kaynak DXF'i `Image.load()` ile yükleyin.  
`Image.load()` bir CAD dosyasını okur ve içeriğini temsil eden bir `Image` nesnesi döndürür.

`Image.load()` metodu DXF yapısını ayrıştırır ve rasterize edilebilecek ya da doğrudan kaydedilebilecek bir bellek içi temsil oluşturur.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile); 
```

### Adım 3: Rasterizasyon Seçeneklerini Yapılandır (Java'da PDF Sayfa Genişliğini Ayarla)

Burada `CadRasterizationOptions` oluşturup çıktı sayfa boyutunu tanımlıyoruz.  
`CadRasterizationOptions`, CAD verilerinin rasterize edilme şeklini, sayfa boyutu, DPI ve düzen seçimini belirler.

`CadRasterizationOptions`, CAD verilerinin nasıl render edileceğini kontrol eder – sayfa boyutu, DPI, arka plan rengi ve rasterize edilecek düzen(ler).

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);   
rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `setPageWidth` / `setPageHeight` – PDF için **sayfa genişliğini** (ve yüksekliğini) kontrol eder.
- `setLayouts` – Hangi düzen(lerin) render edileceğini belirtir; `"Model"` çoğu DXF dosyasında varsayılan model alanıdır.

### Adım 4: PDF Seçeneklerini Oluştur (Java CAD PDF Dönüştürme)

Rasterizasyon ayarlarını bir `PdfOptions` örneğine bağlayın.  
`PdfOptions`, Aspose.CAD'in sağlanan rasterizasyon ayarlarıyla bir PDF dosyası üretmesini söyler.

`PdfOptions`, kütüphanenin daha önce tanımlanan rasterizasyon ayarlarını uygulayarak bir PDF dosyası üretmesini sağlayan kapsayıcıdır.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Adım 5: DXF'yi PDF'ye Dışa Aktar (DXF'den PDF Oluştur)

Son olarak görüntüyü PDF olarak kaydedin.  
`Image.save()` render edilen içeriği, seçeneklerde belirtilen formata göre bir dosyaya yazar.

`save` çağrısı, PDF seçeneklerini kullanarak render edilen içeriği diske yazar ve vektör bütünlüğünü koruyan bir PDF üretir.

```java
image.save(dataDir + "conic_pyramid_layout_out_.pdf", pdfOptions);
```

Çalıştırdıktan sonra aynı dizinde **conic_pyramid_layout_out_.pdf** dosyasını bulacaksınız; bu dosya yalnızca **Model** düzenini belirlediğiniz boyutlarda içerir.

## Yaygın Kullanım Senaryoları

| Senaryo | Bu yöntemin neden yardımcı olduğu |
|----------|-----------------------|
| **Otomatik rapor oluşturma** | Her çizimin aynı sayfa boyutuyla dışa aktarılmasını garanti eder, toplu PDF'leri tutarlı hâle getirir. |
| **Müşteri odaklı tasarım ön izlemeleri** | Tek bir düzen (ör. “Model” veya “Sheet1”) dışa aktararak dosya boyutunu azaltır ve vektör doğruluğunu korur. |
| **Eski DWG'den PDF'ye geçiş** | Bu örnek DXF kullansa da aynı API, **convert dwg to pdf** işlemi için minimal kod değişikliğiyle çalışır. |
| **Web portalına CAD çizimi gömme** | Oluşturulan PDF, ek dönüşüm araçlarına ihtiyaç duymadan doğrudan tarayıcılara akış olarak gönderilebilir. |

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|--------|-----|
| **Boş PDF** | Düzen adı uyuşmazlığı | DXF'teki tam düzen adını kontrol edin (bir CAD görüntüleyici kullanın). |
| **Yanlış sayfa boyutu** | `setPageWidth/Height` uygulanmamış | Rasterizasyon seçeneklerini **PdfOptions** oluşturulmadan önce ayarladığınızdan emin olun. |
| **Büyük dosyalarda bellek yetersizliği** | DXF bellekte tamamen yüklendi | Akış (streaming) kullanın veya JVM heap'ini artırın (`-Xmx2g`). |
| **Eksik yazı tipleri** | Metin öğeleri mevcut olmayan yazı tiplerini kullanıyor | Sunucuya gerekli yazı tiplerini kurun veya `CadRasterizationOptions` ile gömün. |
| **Birden fazla düzen dışa aktarmak gerekiyor** | Tek düzen çağrısı | `setLayouts` metoduna bir dizi düzen adı verin ve her biri için `save` adımını tekrarlayın. |

## Sıkça Sorulan Sorular

**S: Aspose.CAD for Java, yeni başlayanlar ve deneyimli geliştiriciler için uygun mu?**  
C: Kesinlikle. API, yeni başlayanlar için anlaşılırken, ileri düzey kullanıcılar için derin özelleştirme imkanı sunar.

**S: Farklı düzenler için rasterizasyon seçeneklerini özelleştirebilir miyim?**  
C: Evet. `CadRasterizationOptions` (sayfa boyutu, DPI, arka plan rengi) her düzen için ihtiyaç duyulduğu gibi ayarlanabilir.

**S: Aspose.CAD for Java için kapsamlı belgeleri nerede bulabilirim?**  
C: Ayrıntılı dokümantasyon [burada](https://reference.aspose.com/cad/java/) mevcuttur.

**S: Aspose.CAD for Java için ücretsiz bir deneme sürümü var mı?**  
C: Evet, deneme sürümünü [buradan](https://releases.aspose.com/) indirebilirsiniz.

**S: Aspose.CAD for Java desteğini nasıl alabilirim?**  
C: Topluluk ve çalışan desteği için destek forumuna [buradan](https://forum.aspose.com/c/cad/19) ulaşabilirsiniz.

## Sonuç

Bu rehberde **dxf düzenlerinden pdf oluşturma** sürecini Aspose.CAD for Java kullanarak, ortam kurulumundan sayfa boyutu ince ayarına kadar adım adım gösterdik. Bu **java pdf conversion library** sayesinde CAD‑to‑PDF iş akışlarını otomatikleştirebilir, vektör bütünlüğünü koruyabilir ve Java uygulamalarınıza sorunsuz PDF üretimini entegre edebilirsiniz. **export dxf to pdf**, **convert dwg to pdf** ya da **generate pdf from cad** gibi senaryolar için yukarıdaki adımlar sağlam bir temel sunar.

---

**Son Güncelleme:** 2026-06-24  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12 (yazım zamanı en güncel)  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Create PDF from CAD – Export DXF to PDF with Aspose.CAD for Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Create PDF from DXF: Export Layer with Aspose.CAD for Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Convert CAD to PDF – Set Canvas Size & Mode (Java)](/cad/java/advanced-cad-features/set-canvas-size-and-mode/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}