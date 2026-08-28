---
date: 2026-06-14
description: Aspose.CAD for Java kullanarak CAD'i PDF'ye dışa aktarmayı ve DGN'yi
  PDF'ye dönüştürmeyi öğrenin. Java geliştiricileri için adım adım kılavuz.
keywords:
- export cad to pdf
- convert dwg to pdf
- convert dgn to pdf
- java convert cad pdf
- batch convert dgn pdf
linktitle: Gömülü DGN'yi Dışa Aktar
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  headline: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  name: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  steps:
  - name: Set Up Input and Output Paths
    text: Define the directory that contains your source file and specify the DWG
      that holds the embedded DGN.
  - name: Load DWG File
    text: '`Image` loads the DWG and automatically detects any embedded DGN data,
      exposing it for further processing.'
  - name: Configure Rasterization Options
    text: Select which layout(s) you want to include in the PDF. In this example we
      export only the **Model** layout, which is the most common view for engineering
      drawings.
  - name: Configure PDF Options
    text: Attach the rasterization settings to the PDF export options so that the
      final document respects the chosen layout and DPI.
  - name: Save PDF File
    text: Finally, write the PDF to disk using the configured options. The `save`
      method writes the configured image to the target file format on disk.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java is a commercial library. You can obtain a license
      from [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Yes, you can access a free trial of Aspose.CAD for Java [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: You can seek support from the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: What if I need a temporary license?
  - answer: The documentation is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the official documentation?
  type: FAQPage
second_title: Aspose.CAD Java API
title: CAD'i PDF'ye Dışa Aktar – Aspose.CAD for Java ile Gömülü DGN'yi Dışa Aktar
url: /tr/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD'yi PDF'ye Dışa Aktar – Aspose.CAD for Java ile Gömülü DGN'yi Dışa Aktar

## Giriş

Bu öğreticide **CAD'yi PDF'ye nasıl dışa aktarılır** konusunu keşfedecek, gömülü bir DGN dosyasını Aspose.CAD for Java ile yüksek kaliteli bir PDF belgesine dönüştüreceksiniz. Aspose.CAD, Java geliştiricilerine CAD dosyası manipülasyonu üzerinde tam kontrol sağlayan güçlü bir kütüphanedir; **DGN'yi PDF'ye dönüştür**, **DWG'yi PDF'ye dönüştür** ya da CAD çizimlerini başka formatlarda render etmeniz gerektiğinde kullanılabilir. Aşağıdaki adım‑adım kılavuzu izleyin, böylece bu yeteneği dakikalar içinde uygulamalarınıza entegre edebileceksiniz.

## Hızlı Yanıtlar
- **“export CAD to PDF” ne anlama geliyor?** CAD çizimlerini (DWG, DGN, vb.) vektör kalitesini koruyarak PDF dosyalarına dönüştürür.  
- **Hangi kütüphane kullanılıyor?** Aspose.CAD for Java.  
- **Bir lisansa ihtiyacım var mı?** Üretim için bir lisans gereklidir; ücretsiz deneme sürümü mevcuttur.  
- **Ana önkoşullar nelerdir?** Java geliştirme ortamı ve Aspose.CAD for Java JAR dosyası.  
- **Çıktıyı özelleştirebilir miyim?** Evet – düzenleri seçebilir, rasterleştirme seçeneklerini ayarlayabilir ve PDF ayarlarını kontrol edebilirsiniz.

## “export CAD to PDF” nedir?

Export CAD to PDF, yerel bir CAD çizimini (DWG, DGN, vb.) orijinal vektör geometrisini, katmanlarını ve düzenini koruyan bir PDF dosyasına dönüştürür; bu sayede herkes CAD yazılımı olmadan tasarımı görüntüleyebilir, yazdırabilir veya paylaşabilir. Bu dönüşüm, herhangi bir yakınlaştırma seviyesinde aynı görünüme sahip, platform bağımsız bir belge üretir ve iş birliği ile arşivleme için idealdir.

## DGN'yi PDF'ye dönüştürmek için Aspose.CAD for Java neden kullanılmalı?

Aspose.CAD for Java, harici CAD araçlarına ihtiyaç duymayan saf‑Java bir çözüm sunar, ortaya çıkan PDF'lerde tam vektör doğruluğu sağlar ve düzen seçimi, DPI kontrolü, yazı tipi gömme gibi kapsamlı yapılandırma seçenekleri sunar; bu da hem basit hem de kurumsal ölçekli dönüşüm görevleri için mükemmeldir.

- **Harici bağımlılık yok** – herhangi bir işletim sisteminde tamamen Java ile çalışır.  
- **Vektör verisini korur** – PDF'ler herhangi bir yakınlaştırma seviyesinde net kalır.  
- **İnce ayarlı kontrol** – belirli düzenleri seçin, rasterleştirme DPI'sını ayarlayın ve yazı tiplerini gömün.  
- **Kurumsal hazır** – **2 GB**'a kadar dosyaları destekler, binlerce çizimin toplu işlenmesini ve esnek lisanslamayı sağlar.  

## Önkoşullar

İlerlemeye başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Java Geliştirme Ortamı** – JDK 8 veya daha üstü yüklü ve yapılandırılmış.  
- **Aspose.CAD for Java** – en son JAR'ı [buradan](https://releases.aspose.com/cad/java/) indirin.  

## Paketleri İçe Aktar

`import` ifadeleri, gerekli Aspose.CAD sınıflarını kapsam içine getirir.  
`Image`, rasterleştirilebilen herhangi bir CAD dosyasını temsil eden temel sınıftır; `PdfOptions` ve `RasterizationOptions` PDF çıktısını ince ayarlamanızı sağlar.  
`CadRasterizationOptions`, CAD render'ı için DPI, sayfa boyutu ve düzen gibi rasterleştirme parametrelerini belirler.

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Aspose.CAD for Java kullanarak CAD'yi PDF'ye nasıl dışa aktarılır?

İşlem, gömülü DGN içeren DWG dosyasını yükleyerek, çıktı çözünürlüğü ve düzenini tanımlayan rasterleştirme parametrelerini ayarlamayı, bu parametreleri bir PdfOptions nesnesine eklemeyi ve son olarak PDF'yi oluşturmak için kaydetme metodunu çağırmayı içerir. Bu yaklaşım, minimum kodla yüksek kaliteli, vektör‑koruyucu sonuçlar sağlar.

Aşağıda, gömülü DGN dosyasını (DWG içinde saklanan) PDF'ye dönüştürmenin adım‑adım bir açıklaması yer almaktadır.

### Adım 1: Giriş ve Çıkış Yollarını Ayarla

Kaynak dosyanızın bulunduğu dizini tanımlayın ve gömülü DGN'i barındıran DWG dosyasını belirtin.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Adım 2: DWG Dosyasını Yükle

`Image`, DWG'yi yükler ve otomatik olarak gömülü DGN verisini algılar, böylece sonraki işlemler için kullanılabilir hâle getirir.

```java
Image objImage = Image.load(fileName);
```

### Adım 3: Rasterleştirme Seçeneklerini Yapılandır

PDF'ye dahil etmek istediğiniz düzen(ler)i seçin. Bu örnekte, mühendislik çizimleri için en yaygın görünüm olan **Model** düzenini dışa aktarıyoruz.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Adım 4: PDF Seçeneklerini Yapılandır

Rasterleştirme ayarlarını PDF dışa aktarma seçeneklerine ekleyin; böylece nihai belge seçilen düzeni ve DPI'yi dikkate alır.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Adım 5: PDF Dosyasını Kaydet

Son olarak, yapılandırılmış seçenekleri kullanarak PDF'yi diske yazın. `save` metodu, yapılandırılmış görüntüyü hedef dosya formatına diske yazar.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## DWG'yi PDF'ye Dönüştür – ek bir ipucu

Kaynak dosyanız gömülü DGN içermeyen sade bir DWG ise, aynı kodu yeniden kullanabilirsiniz – sadece `fileName` değişkenini dönüştürmek istediğiniz DWG'ye yönlendirin. Rasterleştirme ve PDF seçenekleri aynı kalır, böylece tutarlı bir **DWG'yi PDF'ye dönüştür** iş akışı elde edersiniz.

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|--------|----------|
| **Boş PDF çıktısı** | Düzen adı uyuşmazlığı | `setLayouts` metoduna geçirilen düzen adının kaynak dosyadaki düzenle tam olarak (büyük/küçük harf duyarlı) eşleştiğini doğrulayın. |
| **Lisans istisnası** | Lisans olmadan deneme sürümü kullanmak | Görüntüyü yüklemeden önce geçerli bir Aspose.CAD lisansı uygulayın (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Dosya bulunamadı** | `dataDir` yolu hatalı | Mutlak bir yol kullanın veya göreli yolun proje çalışma dizinine göre doğru olduğundan emin olun. |
| **Düşük çözünürlüklü grafikler** | Varsayılan rasterleştirme DPI'sı düşük | `rasterizationOptions.setResolution(300)` ayarlayın veya DPI'yi artırmak için `setPageWidth/Height` değerlerini değiştirin. |

## Sıkça Sorulan Sorular

**Q: Aspose.CAD for Java'ı ticari bir projede kullanabilir miyim?**  
**A:** Evet, Aspose.CAD for Java ticari bir kütüphanedir. Lisansı [buradan](https://purchase.aspose.com/buy) alabilirsiniz.

**Q: Ücretsiz bir deneme sürümü mevcut mu?**  
**A:** Evet, Aspose.CAD for Java için ücretsiz bir deneme sürümüne [buradan](https://releases.aspose.com/) erişebilirsiniz.

**Q: Aspose.CAD for Java için destek nasıl alınır?**  
**A:** Aspose.CAD topluluğundan [forum](https://forum.aspose.com/c/cad/19) üzerinden destek alabilirsiniz.

**Q: Geçici bir lisansa ihtiyacım olursa ne yapmalıyım?**  
**A:** Geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

**Q: Resmi dokümantasyonu nereden bulabilirim?**  
**A:** Dokümantasyon [burada](https://reference.aspose.com/cad/java/) mevcuttur.

## Sonuç

Artık **CAD'yi PDF'ye dışa aktarmayı**, özellikle **DGN'yi PDF'ye dönüştürmeyi** ve **DWG'yi PDF'ye dönüştürmeyi** Aspose.CAD for Java kullanarak nasıl yapacağınızı öğrendiniz. Yukarıdaki adımları izleyerek, ek CAD yazılımına ihtiyaç duymadan herhangi bir Java tabanlı çözümde sorunsuz CAD‑to‑PDF dönüşümünü entegre edebilir, kullanıcılarınıza yüksek kaliteli PDF'ler sunabilirsiniz.

---

**Son Güncelleme:** 2026-06-14  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose

{{< blocks/products/products-backtop-button >}}

## İlgili Eğitimler

- [Aspose.CAD for Java ile DGN'yi DWG'ye Dışa Aktar – Eğitim](/cad/java/dgn-export-options/)
- [Aspose.CAD for Java ile DGN'den AutoCAD PDF'ye Kolay Dışa Aktarım](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [dwg to pdf java – Aspose.CAD ile CAD'yi PDF'ye Dışa Aktar](/cad/java/cad-export-options/export-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}