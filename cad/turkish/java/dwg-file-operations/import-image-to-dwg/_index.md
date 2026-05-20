---
date: 2026-05-20
description: Aspose.CAD for Java kullanarak DWG dosyalarına görüntü eklemeyi ve DWG'yi
  PDF'ye dönüştürmeyi öğrenin. Verimli geliştirme için adım adım rehberimizi izleyin.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Java kullanarak DWG dosyasına görüntü aktarın
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD Java kullanarak DWG dosyalarına görüntüyü zahmetsizce ekleyin
url: /tr/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG Dosyalarına Görüntü Eklemek Aspose.CAD Java ile Kolayca

Modern Java uygulamalarında, **DWG'ye görüntü eklemek** yaygın bir gereksinimdir—ister bir CAD görüntüleyici oluşturuyor olun, ister çizim güncellemelerini otomatikleştiriyor olun ya da dokümantasyon üretiyor olun. Aspose.CAD for Java, raster görüntüleri doğrudan DWG çizimlerine tam bir CAD motoruna ihtiyaç duymadan eklemenizi sağlayan basit ve yüksek performanslı bir yol sunar. Bu öğreticide, DWG'yi yüklemekten sonucu PDF olarak dışa aktarmaya kadar tüm süreci adım adım gösterecek ve ayrıca **dwg'ye görüntü içe aktarma** ve **dwg'yi pdf'ye dönüştürme** işlemlerini tek bir iş akışında nasıl yapacağınızı ele alacağız.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.CAD for Java  
- **PDF olarak da dışa aktarabilir miyim?** Evet – `PdfOptions` ile `CadRasterizationOptions` kullanın  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri  
- **Uygulama ne kadar sürer?** Temel bir görüntü içe aktarma için yaklaşık 10‑15 dakika  

## “dwg'ye görüntü ekleme” nedir?
DWG dosyasına bir görüntü eklemek, raster bir resim (PNG, JPEG vb.) **CadRasterImage** varlığı olarak çizimin model alanına gömmek anlamına gelir; bu sayede diğer CAD nesneleri gibi konumlandırılabilir, ölçeklendirilebilir ve isteğe bağlı olarak kırpılabilir. Görüntü, çizimin nesne tablosunda depolanır ve standart CAD görüntüleyiciler tarafından gösterilir.

## DWG'ye görüntü eklemek için Aspose.CAD for Java neden kullanılmalı?
Üçüncü taraf bir CAD yazılımı kurmadan DWG dosyalarına raster grafikler gömebilirsiniz ve API, ekleme noktası, ölçek vektörleri ve kırpma sınırları üzerinde piksel düzeyinde kontrol sağlar. Aspose.CAD, 2 GB'a kadar dosyaları işleyebilir, **50+ giriş ve çıkış formatını** destekler ve Windows, Linux ve macOS üzerinde çalışır; bu sayede CAD manipülasyonunu herhangi bir Java tabanlı arka uçta entegre edebilirsiniz.

## Önkoşullar
- **Aspose.CAD for Java** – resmi siteden en yeni JAR'ı **[buradan](https://releases.aspose.com/cad/java/)** indirin.  
- **Java Development Kit** – JDK 8 veya daha yeni bir sürüm, tercih ettiğiniz IDE (IntelliJ IDEA, Eclipse, VS Code vb.) ile.  
- Üretim kullanımı için geçerli bir **Aspose.CAD lisansı** (deneme sürümü deneyler için çalışır).  

## Paketleri İçe Aktarma
Aşağıdaki içe aktarmalar, görüntü işleme ve PDF dönüşümü için kullanılan temel Aspose.CAD sınıflarını getirir.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Adım Adım Kılavuz

### Adım 1: DWG Dosyasını Yükle
İlk olarak, DWG çiziminizin bulunduğu klasöre işaret edin ve `Image.load` ile yükleyin.  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Adım 2: Raster Görüntü Tanımını Belirle
`CadRasterImageDef` sınıfı, çizime gömülecek harici raster görüntü kaynağını tanımlar.  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Adım 3: Ekleme Noktasını ve Ölçek Vektörlerini Ayarla
Ekleme noktası, görüntünün sol‑alt köşesinin nerede görüneceğini belirler. **U** ve **V** vektörleri yatay ve dikey ölçeklemeyi kontrol eder.  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Adım 4: CadRasterImage Nesnesini Oluştur
`CadRasterImage` varlığı, DWG model alanına yerleştirilen bir raster resmi temsil eder.  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Adım 5: Görüntüyü Model Alanına Ekle
Raster görüntüyü `*Model_Space` bloğuna ekleyin, ardından tanımın kaydedilmesi için çizimin nesne koleksiyonunu güncelleyin.  
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### Adım 6: PDF Dışa Aktarma Seçeneklerini Yapılandır (İsteğe Bağlı)
`PdfOptions`, bir CAD çizimini PDF dosyası olarak kaydetmek için ayarları belirtir. `CadRasterizationOptions` ise PDF dönüşümü sırasında CAD içeriğinin nasıl rasterleştirileceğini tanımlar.  
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Adım 7: Oluşan PDF'yi Kaydet
Son olarak, değiştirilmiş çizimi PDF dosyası olarak dışa aktarın. Aynı `image` örneği kullanıldığı için PDF, yeni eklenen raster görüntüyü yansıtır.  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Bu adımları izleyerek **dwg'ye görüntü ekleyebilir** ve gerektiğinde **dwg'yi pdf olarak kaydedebilirsiniz**, tek bir kompakt rutin içinde en yaygın **dwg dosya işlemlerini** kapsar.

## Yaygın Sorunlar ve Çözümler
- **Görüntü görünmüyor** – Görüntü dosya yolunun (`road‑sign‑custom.png`) doğru olduğundan ve görüntü boyutlarının `CadRasterImageDef`'e verilen değerlerle eşleştiğinden emin olun.  
- **Yanlış ölçekleme** – U ve V vektörlerini ayarlayın; bunlar piksel başına çizim birimlerini temsil eder.  
- **PDF boş görünüyor** – `CadRasterizationOptions.setDrawType`'ın `UseObjectColor` veya başka uygun bir moda ayarlandığından emin olun.  

## Sıkça Sorulan Sorular

**Q: Aspose.CAD for Java tüm Java geliştirme ortamlarıyla uyumlu mu?**  
**A:** Evet, Aspose.CAD for Java, JDK 8+ destekleyen herhangi bir IDE ile çalışır; IntelliJ IDEA, Eclipse ve VS Code dahil.

**Q: Aspose.CAD for Java'yi ticari projelerde kullanabilir miyim?**  
**A:** Evet, Aspose.CAD for Java'yi ticari projelerde kullanabilirsiniz. Lisans detayları için **[buradan](https://purchase.aspose.com/buy)** ziyaret edin.

**Q: Aspose.CAD for Java için ücretsiz deneme mevcut mu?**  
**A:** Evet, ücretsiz deneme sürümüne **[buradan](https://releases.aspose.com/)** ulaşabilirsiniz.

**Q: Aspose.CAD for Java için destek nasıl alabilirim?**  
**A:** **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** üzerinden destek alabilirsiniz.

**Q: Aspose.CAD for Java için geçici bir lisans alabilir miyim?**  
**A:** Evet, geçici lisansı **[buradan](https://purchase.aspose.com/temporary-license/)** alabilirsiniz.

**Son Güncelleme:** 2026-05-20  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [DWG'yi PDF veya Raster Olarak Aspose.CAD for Java ile Dışa Aktar](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java ile DWG Dosyalarına Özel Özellikler Ekle](/cad/java/additional-features/add-custom-properties/)
- [CAD'i PNG Olarak Kaydet – Aspose.CAD for Java ile CAD Çizimini Raster Görüntü Formatına Dönüştür](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}