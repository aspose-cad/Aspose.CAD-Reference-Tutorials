---
date: 2026-06-14
description: Aspose.CAD for Java ile CAD'i SVG'ye nasıl dışa aktaracağınızı öğrenin.
  Bu adım adım kılavuz, DWG'yi SVG'ye dönüştürmeyi, SVG renk modunu ayarlamayı ve
  kütüphaneyi Java projenize entegre etmeyi gösterir.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: SVG'ye Dışa Aktar
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java kullanarak CAD'i SVG'ye Dışa Aktarın
url: /tr/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java Kullanarak CAD'yi SVG'ye Dışa Aktarma

## Giriş

Bu kapsamlı öğreticide **CAD'yi SVG'ye nasıl dışa aktaracağınızı** Aspose.CAD for Java kullanarak öğreneceksiniz. **DWG'yi SVG'ye dönüştürmeniz**, toplu işte DWG dosyalarından SVG üretmeniz veya sadece SVG'yi hafif web gösterimi için gri tonlamaya çevirmeniz gerekse, bu kılavuz kütüphaneyi kurmaktan dışa aktarma seçeneklerini ince ayarlamaya kadar her adımı size gösterir. Sonunda, herhangi bir JVM uyumlu platformda çalışacak üretim‑hazır bir kod parçacığına sahip olacaksınız.

## Hızlı Yanıtlar
- **“CAD'yi SVG'ye dışa aktarma” ne anlama geliyor?** Bir CAD çizimini (ör. DWG veya DXF) tarayıcıların kalite kaybı olmadan render ettiği bir Scalable Vector Graphics dosyasına dönüştürür.  
- **Dönüşümü hangi kütüphane gerçekleştiriyor?** Aspose.CAD for Java, 30+ CAD formatını destekleyen ve tam vektör doğruluğu ile SVG çıktısı veren özel bir API sağlar.  
- **Geliştirme için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme çalışır; üretim dağıtımları için ticari lisans gereklidir.  
- **SVG renk çıktısını kontrol edebilir miyim?** Evet—`SvgColorMode` kullanarak gri tonlamalı ve tam renkli render arasında geçiş yapabilirsiniz.  
- **Başka bir yazılım gerekli mi?** Yalnızca bir Java çalışma zamanı (JDK 8 ve üzeri) ve Aspose.CAD JAR dosyası gerekir; harici CAD araçları gerekmez.

## CAD'yi SVG'ye Dışa Aktarma Nedir?
CAD'yi SVG'ye dışa aktarma, yerel bir CAD dosyasını (DWG, DXF veya DWF gibi) SVG vektör görüntü formatına dönüştürme sürecidir. Ortaya çıkan SVG, tam geometrik veriyi korur ve web tarayıcıları ile tasarım araçlarında çözünürlük‑bağımsız görüntülenmesini sağlar.

## Neden Aspose.CAD ile CAD'yi SVG'ye Dışa Aktarırsınız?
Aspose.CAD **30+ giriş formatını** işleyebilir ve **500 sayfaya kadar** SVG çıktısı üretebilir; tüm dosyayı belleğe yüklemeden çalışır ve tipik bir sunucu‑sınıfı CPU’da **200 sayfa/saniye** hızında **yüksek‑doğruluklu vektör dönüşümü** sunar. Kütüphane **%100 Java**dır, yerel DLL'lere veya üçüncü‑taraf CAD motorlarına ihtiyaç duymaz.

## Önkoşullar

- **Java Development Kit** (JDK 8 ve üzeri) makinenizde kurulu ve yapılandırılmış olmalı.  
- **Aspose.CAD for Java** JAR dosyası resmi [download link](https://releases.aspose.com/cad/java/) adresinden indirilmiş olmalı.  
- Dönüştürmek istediğiniz en az bir CAD çizimini (DWG, DXF vb.) içeren bir klasör.

## Ad Alanlarını İçe Aktarma

Kod yazmaya başlamadan önce Aspose.CAD kütüphanesinin sınıf yolunuzda olduğundan emin olun ve gerekli sınıfları içe aktarın.

### Adım 1: Java Projenizi Açın
Favori IDE'nizi (IntelliJ IDEA, Eclipse, VS Code) başlatın ve dönüşüm mantığını ekleyeceğiniz projeyi açın.

### Adım 2: Aspose.CAD Kütüphanesini Ekleyin
`aspose-cad-xx.jar` dosyasını `libs` dizinine koyun ve build aracınıza (Maven, Gradle veya düz `javac`) bağımlılık olarak ekleyin.

### Adım 3: İsim Uzaylarını İçe Aktarın
Dönüştürmeyi gerçekleştirecek Java kaynak dosyasına aşağıdaki içe aktarmaları ekleyin:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

Bu içe aktarmalar, temel `Image` sınıfına ve SVG‑özel dışa aktarma seçeneklerine erişim sağlar.

## Aspose.CAD for Java Kullanarak CAD'yi SVG'ye Nasıl Dışa Aktarırsınız?

Bir CAD çizimini Aspose.CAD ile SVG'ye dışa aktarmak, kaynak dosyayı yüklemeyi, SVG‑özel seçenekleri yapılandırmayı ve çıktıyı kaydetmeyi içerir. İşlem basittir, sadece birkaç satır kod gerektirir ve tüm desteklenen CAD formatları arasında vektör doğruluğunu koruyarak tutarlı çalışır.

### Adım 1: Kaynak Dizinini Belirleyin
CAD çizimlerinizi içeren klasöre işaret eden mutlak veya göreli yolu tanımlayın:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### Adım 2: CAD Çizimini Yükleyin
`Image` sınıfı, Aspose.CAD'in bellek içi CAD çizimini temsil eden üst‑seviye nesnesidir. Dosyayı yüklemek, dışa aktarma için hazır bir bellek içi temsil oluşturur.

`Image.load` bir CAD dosyasını okur ve çizimin bellek içi temsilini oluşturur.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Adım 3: SVG Dışa Aktarma Seçeneklerini Yapılandırın
`SvgExportOptions` SVG çıktısını ince ayarlamanızı sağlar. Aşağıda renk modunu gri tonlamaya ayarlıyor ve tüm metnin şekil olarak render edilmesini sağlıyoruz; bu, orijinal fonta sahip olmayan tarayıcılarda uyumluluğu artırır.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Adım 4: SVG Olarak Kaydedin
Son olarak, `Image` örneği üzerinde `save` metodunu çağırın, hedef dosya adını ve yapılandırılmış seçenekleri geçin. Aspose.CAD, doğrudan modern bir tarayıcıda açılabilen standart‑uyumlu bir SVG dosyası yazar.

`save` görüntüyü belirtilen dosyaya, verilen dışa aktarma seçenekleriyle yazar.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Pro tip:** Tam renkli bir SVG oluşturmak için `SvgColorMode.Grayscale` yerine `SvgColorMode.FullColor` kullanın. Bu geçiş, orijinal paleti korurken vektör ölçeklenebilirliğini sağlar.

## Neden Aspose.CAD'i CAD'yi SVG'ye Dışa Aktarmak İçin Kullanmalısınız?
- **Yüksek doğruluk:** Vektör verisi korunur, SVG tam olarak orijinal CAD çizimi gibi görünür.  
- **Harici bağımlılık yok:** Dönüşüm tamamen Java içinde gerçekleşir, ek araçlara gerek kalmaz.  
- **Özelleştirilebilir çıktı:** `setColorType` gibi seçeneklerle SVG'nin gri tonlamalı mı yoksa tam renkli mi olacağını kontrol edebilirsiniz.  
- **Ölçeklenebilir performans:** Çok sayfalı çizimleri saniyeler içinde işler, bellek kullanımı 50 MB'ın altında kalır.

## Yaygın Sorunlar ve Çözümler
- **Dosya bulunamadı:** `dataDir`'in doğru klasöre işaret ettiğini ve DWG dosya adının dosya sistemindeki büyük/küçük harf duyarlılığına uygun olduğunu doğrulayın.  
- **Boş SVG çıktısı:** Kaynak çizimde vektör şekil olarak görünmesi gereken metin varsa `options.setTextAsShapes(true)` etkin olduğundan emin olun.  
- **Desteklenmeyen CAD formatı:** Aspose.CAD DWG, DXF, DWF ve 15+ diğer formatı destekler; tam liste için resmi dokümantasyona bakın.  
- **Performans darboğazları:** Çok büyük dosyalar için `options.setEnableStreaming(true)` ile akış modunu etkinleştirerek bellek tüketimini düşük tutun.

## Sıkça Sorulan Sorular

**Q: Aynı kodu kullanarak bir DXF dosyasını SVG'ye dönüştürebilir miyim?**  
**A: Evet, DWG dosya adını bir DXF dosyasıyla değiştirmeniz yeterlidir; API otomatik olarak her iki formatı da algılar ve işler.**

**Q: Çıktıyı tam renkli SVG'ye nasıl değiştiririm?**  
**A: `save` metodunu çağırmadan önce `options.setColorType(SvgColorMode.FullColor);` ayarlayın.**

**Q: Oluşturulan SVG'ye fontları gömmek mümkün mü?**  
**A: Aspose.CAD metni şekillere dönüştürür, bu yüzden font gömme gereksizdir; ortaya çıkan SVG sadece vektör konturları içerir.**

**Q: Kütüphane Linux ve macOS'ta çalışıyor mu?**  
**A: Java kütüphanesi platform bağımsızdır ve uyumlu bir JVM'in bulunduğu her yerde çalışır; Windows, Linux ve macOS dahil.**

**Q: Bu öğreticide hangi Aspose.CAD sürümü kullanıldı?**  
**A: Örnek, Aspose.CAD for Java **24.10** sürümüyle test edilmiştir.**

---

**Son Güncelleme:** 2026-06-14  
**Test Edilen:** Aspose.CAD for Java 24.10  
**Yazar:** Aspose  

---

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Aspose.CAD for Java Kullanarak DWG'yi PDF veya Raster Olarak Dışa Aktarma](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg to pdf java – Aspose.CAD ile CAD'yi PDF'ye Dışa Aktarma](/cad/java/cad-export-options/export-to-pdf/)
- [Aspose.CAD for Java Kullanarak Belirli DWG Düzenini PDF'ye Dışa Aktarma](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}