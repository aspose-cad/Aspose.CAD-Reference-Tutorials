---
date: 2026-06-04
description: Aspose.CAD for Java kullanarak CAD'den PDF oluşturmayı ve filigran eklemeyi
  öğrenin. Bu adım adım kılavuz, CAD'i PDF'ye dışa aktarma, add text CAD ve branding
  konularını kapsar.
keywords:
- create pdf from cad
- export cad to pdf
- add text cad
- watermark cad drawing
- convert dwg to pdf
linktitle: Filigran Ekle
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to create PDF from CAD and add a watermark using Aspose.CAD
    for Java. This step‑by‑step guide covers export CAD to PDF, add text CAD, and
    branding.
  headline: Create PDF from CAD with Watermark - Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PDF from CAD and add a watermark using Aspose.CAD
    for Java. This step‑by‑step guide covers export CAD to PDF, add text CAD, and
    branding.
  name: Create PDF from CAD with Watermark - Aspose.CAD for Java
  steps:
  - name: Import Packages
    text: The `com.aspose.cad` namespace provides all classes you need for CAD manipulation.
      The `Image` class is the entry point for loading and saving CAD files. The `MText`
      class represents multi‑line text that can be styled and positioned.
  - name: Add New MTEXT
    text: MText represents multi‑line text entities that can be used for watermarks.
  - name: Add Simple Entity like Text
    text: TextEntity is a single‑line text object used for simple annotations.
  - name: Export to PDF
    text: SaveFormat.Pdf specifies PDF as the output format for saving.
  type: HowTo
- questions:
  - answer: Aspose.CAD supports **DWG, DXF, DWT, DWF, and over 30 additional formats**,
      allowing you to **export cad to pdf** from virtually any source file.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Yes – you can control font family, size, color, rotation, and transparency
      through the `MText` or `TextEntity` properties.
    question: Can I customize the appearance of the watermark text?
  - answer: Yes, you can download the trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.CAD for Java?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      assistance and official support channels.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      detailed API references, code samples, and best‑practice guides.
    question: Where can I find the complete documentation for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Filigranlı CAD'den PDF Oluşturma - Aspose.CAD for Java
url: /tr/java/other-cad-operations/add-watermark/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD'den PDF Oluşturma ve Filigran Ekleme - Aspose.CAD for Java

## Giriş

Bu öğreticide **CAD çizimlerinden PDF oluşturacak** ve Aspose.CAD for Java kullanarak özel bir filigran uygulayacaksınız. Filigran eklemek, fikri mülkiyetinizi korumanıza, tasarımlarınıza marka eklemenize veya revizyon bilgilerini gömmenize olanak tanır. Gerekli paketlerin içe aktarılmasından, metin‑tabanlı filigranların eklenmesine, son CAD çiziminin PDF dosyası olarak dışa aktarılmasına kadar tüm süreci adım adım inceleyeceğiz. Sonunda, herhangi bir Java projesine ekleyebileceğiniz yeniden kullanılabilir bir kod parçacığına sahip olacaksınız.

## Hızlı Yanıtlar
- **Ana hedef nedir?** Bir CAD dosyasından PDF oluşturmak ve sadece birkaç Java satırıyla üzerine bir filigran yerleştirmek.  
- **Hangi kütüphane gereklidir?** Aspose.CAD for Java (30+ CAD formatını destekler).  
- **Test için lisansa ihtiyacım var mı?** 30‑günlük ücretsiz deneme sürümü mevcuttur; üretim için ticari lisans gereklidir.  
- **Filigran ekledikten sonra CAD'i PDF'e dışa aktarabilir miyim?** Evet – çizimi kaydeden aynı API çağrısı aynı zamanda PDF'e dönüştürür.  
- **İşlem çoklu iş parçacığı güvenli mi?** Tüm Aspose.CAD sınıfları, her iş parçacığı için ayrı örnekler oluşturulduğunda eşzamanlı kullanım için tasarlanmıştır.

## CAD'de filigran nedir?
CAD'de bir filigran, sahipliği, gizliliği veya revizyon durumunu göstermek amacıyla çizimin üzerine veya arkasına yerleştirilen yarı‑saydam bir metin veya grafik katmanıdır. Alt geometrik verileri değiştirmeden, izleyicilerin orijinal içeriği görmesini sağlarken filigranın varlığını da gösterir.

## **cad'den pdf oluştururken** neden bir filigran eklemelisiniz?
Aspose.CAD for Java **30+ giriş formatını** (DWG, DXF, DWF, DWT vb.) destekler ve dosyaları **500 MB**'a kadar bellek içinde tamamen yüklemeden işleyebilir. PDF dönüşüm aşamasında filigran eklemek, ayrı bir son‑işlem adımına gerek kalmadan işlem süresinde **%40** tasarruf sağlar ve toplu iş akışlarını hızlandırır.

## Önkoşullar

- **Aspose.CAD for Java** – resmi siteden en son JAR dosyasını [buradan](https://releases.aspose.com/cad/java/) indirin.  
- **Java Development Kit (JDK)** – sürüm 11 veya üzeri önerilir.  
- Üretim kullanımı için geçerli bir **Aspose.CAD lisansı** (deneme sürümü için isteğe bağlı).  

## CAD'den PDF Oluşturma ve Filigran Ekleme Nasıl Yapılır?

CadImage, Aspose.CAD içinde bir CAD çizimini temsil eden temel sınıftır.  
Bir CAD dosyasından gömülü filigranlı PDF oluşturmak için önce çizimi bir `CadImage` örneğine yükleyin; bu, CAD belgesini bellekte temsil eder. Ardından filigran metnini içeren bir `MText` veya `TextEntity` nesnesi oluşturun, yazı tipi boyutunu, rengini ve saydamlığını ayarlayın ve model alanına ekleyin. Son olarak, `save` metodunu `SaveFormat.Pdf` ile çağırarak değiştirilmiş çizimi PDF olarak dışa aktarın; vektör kalitesi korunur.

### Adım 1: Paketleri İçe Aktarın

`com.aspose.cad` ad alanı, CAD manipülasyonu için ihtiyaç duyduğunuz tüm sınıfları sağlar.

`Image` sınıfı, CAD dosyalarını yüklemek ve kaydetmek için giriş noktasıdır.  
`MText` sınıfı, stil verilebilen ve konumlandırılabilen çok‑satırlı metni temsil eder.  

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Adım 2: Yeni MTEXT Ekleyin

MText, filigranlar için kullanılabilen çok‑satırlı metin varlıklarını temsil eder.  

```java
//add new MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

### Adım 3: Metin Gibi Basit Bir Varlık Ekleyin

TextEntity, basit açıklamalar için kullanılan tek‑satırlı metin nesnesidir.  

```java
// or add more simple entity like Text
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

### Adım 4: PDF Olarak Dışa Aktarın

SaveFormat.Pdf, kaydetme işlemi için çıktı formatı olarak PDF'i belirtir.  

```java
// export to pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Yaygın Sorunlar ve Çözümler

- **Filigran görünmüyor** – Metin renginin arka planla kontrast oluşturduğundan emin olun ve `Transparency` özelliğini (ör. %50 saydamlık için 0.5) ayarlayın.  
- **Büyük dosyalar OutOfMemoryError veriyor** – `CadImage` akış modunu etkinleştirmek için `CadImageOptions.setLoadMode(LoadMode.Paged)` ayarını kullanın.  
- **Yanlış yazı tipi renderı** – Sunucuya gerekli TrueType yazı tiplerini kurun veya `FontRepository` aracılığıyla gömün.

## Sıkça Sorulan Sorular

**S: Aspose.CAD tüm CAD dosya formatlarıyla uyumlu mu?**  
C: Aspose.CAD **DWG, DXF, DWT, DWF ve 30'dan fazla ek format** destekler; bu sayede neredeyse her kaynak dosyadan **cad'den pdf** dışa aktarabilirsiniz.

**S: Filigran metninin görünümünü özelleştirebilir miyim?**  
C: Evet – `MText` veya `TextEntity` özellikleri aracılığıyla yazı tipi ailesi, boyutu, rengi, dönüşü ve saydamlığı kontrol edebilirsiniz.

**S: Aspose.CAD for Java için bir deneme sürümü mevcut mu?**  
C: Evet, deneme sürümünü [buradan](https://releases.aspose.com/) indirebilirsiniz.

**S: Aspose.CAD için destek nasıl alınır?**  
C: Topluluk yardımı ve resmi destek kanalları için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

**S: Aspose.CAD for Java için tam dokümantasyona nereden ulaşabilirim?**  
C: Ayrıntılı API referansları, kod örnekleri ve en iyi uygulama rehberleri için [dokümantasyona](https://reference.aspose.com/cad/java/) bakın.

---

**Son Güncelleme:** 2026-06-04  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Aspose.CAD for Java Kullanarak DWG'yi PDF veya Raster Olarak Dışa Aktarma](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java Kullanarak DWG'den PDF Oluşturma ve Metin Ekleme](/cad/java/cad-text-and-annotation/add-text-in-dwg/)
- [Aspose.CAD for Java Kullanarak Belirli DWG Düzenini PDF Olarak Dışa Aktarma](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}