---
date: 2026-01-12
description: Aspose.CAD for Java kullanarak DWG dosyalarına nasıl resim ekleyeceğinizi
  ve DWG'yi PDF'ye nasıl dönüştüreceğinizi öğrenin. Verimli geliştirme için adım adım
  rehberimizi izleyin.
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: Aspose.CAD Java Kullanarak DWG Dosyalarına Görüntüyü Zahmetsizce Ekleyin
url: /tr/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD Java Kullanarak DWG Dosyalarına Görüntü Eklemeyi Kolayca Yapın

## Hızlı Yanıtlar
- **Hangi kütüphaneye ihtiyacım var?** Aspose.CAD for Java  
- **PDF olarak da dışa aktarabilir miyim?** Evet – `PdfOptions` ile `CadRasterizationOptions` kullanın  
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme sürümü yeterlidir; üretim için ticari lisans gereklidir  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri  
- **Uygulama ne kadar sürer?** Temel bir görüntü içe aktarma için yaklaşık 10‑15 dakika

## “add image to dwg” nedir?
DWG dosyasına görüntü eklemek, bir raster resim (PNG, JPEG vb.) nin `CadRasterImage` nesnesi olarak çizimin model alanına yerleştirilmesi anlamına gelir. Görüntü, CAD varlık ağacının bir parçası haline gelir ve diğer CAD nesneleri gibi konumlandırılabilir, ölçeklenebilir ve kırpılabilir.

## Aspose.CAD for Java ile dwg’ye görüntü eklemek neden tercih edilmeli?
- **CAD yazılımı gerekmez** – API, DWG ayrıştırmasını dahili olarak gerçekleştirir.  
- **İnce ayar kontrolü** – ekleme noktası, ölçek vektörleri ve kırpma üzerinde hassas kontrol.  
- **Yerleşik PDF dönüşümü** – aynı iş akışında yazdırılabilir bir PDF oluşturabilirsiniz.  
- **Çapraz platform** – Windows, Linux ve macOS’ta çalışır.

## Önkoşullar
- Aspose.CAD for Java: Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. İndirmek için [buraya](https://releases.aspose.com/cad/java/) tıklayın.  
- Java Geliştirme Ortamı: JDK 8+ ve tercih ettiğiniz IDE (IntelliJ, Eclipse, VS Code vb.).

## Paketleri İçe Aktarın
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Adım‑Adım Kılavuz

### Adım 1: DWG Dosyasını Yükleyin
İlk olarak, DWG çiziminizin bulunduğu klasöre işaret edin ve `Image.load` ile yükleyin.
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Adım 2: Raster Görüntü Tanımını Belirleyin
Gömmek istediğiniz dış PNG dosyasına referans veren bir `CadRasterImageDef` oluşturun. Yapıcı, görüntü dosya adını ve piksel boyutlarını alır.
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Adım 3: Ekleme Noktasını ve Ölçek Vektörlerini Ayarlayın
Ekleme noktası, görüntünün sol‑alt köşesinin nerede görüneceğini belirler. **U** ve **V** vektörleri, yatay ve dikey ölçeklemeyi kontrol eder.
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Adım 4: CadRasterImage Nesnesini Oluşturun
Tanımı, ekleme noktasını ve vektörleri bir `CadRasterImage` içinde birleştirin. Görüntünün yalnızca bir kısmının görünmesini istiyorsanız kırpma sınırlarını da ayarlayabilirsiniz.
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Adım 5: Görüntüyü Model Alanına Ekleyin
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

### Adım 6: PDF Dışa Aktarma Seçeneklerini Yapılandırın (İsteğe Bağlı)
Eğer çizimin bir PDF sürümüne de ihtiyacınız varsa, `PdfOptions` ile `CadRasterizationOptions`’ı yapılandırın. Bu adım, **convert dwg to pdf** işlemini aynı akışta gösterir.
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Adım 7: Oluşturulan PDF’yi Kaydedin
Son olarak, değiştirilmiş çizimi bir PDF dosyası olarak dışa aktarın. Aynı `image` örneği kullanıldığı için PDF, yeni eklenen raster görüntüyü yansıtır.
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Bu adımları izleyerek **add image to dwg** dosyalarını hızlıca ekleyebilir ve gerektiğinde **save dwg as pdf** yapabilirsiniz.

## Yaygın Sorunlar ve Çözümleri
- **Görüntü görünmüyor** – Görüntü dosya yolunun (`road-sign-custom.png`) doğru olduğundan ve görüntü boyutlarının `CadRasterImageDef`’e verilen değerlerle eşleştiğinden emin olun.  
- **Ölçekleme hatalı** – U ve V vektörlerini ayarlayın; bunlar piksel başına çizim birimlerini temsil eder.  
- **PDF boş görünüyor** – `CadRasterizationOptions.setDrawType` değerinin `UseObjectColor` veya uygun bir moda ayarlandığını kontrol edin.

## Sık Sorulan Sorular

**S: Aspose.CAD for Java tüm Java geliştirme ortamlarıyla uyumlu mu?**  
C: Evet, Aspose.CAD for Java çoğu Java geliştirme ortamıyla uyumludur.

**S: Aspose.CAD for Java’yı ticari projelerde kullanabilir miyim?**  
C: Evet, Aspose.CAD for Java’yı ticari projelerde kullanabilirsiniz. Lisans detayları için [buraya](https://purchase.aspose.com/buy) bakın.

**S: Aspose.CAD for Java için ücretsiz deneme mevcut mu?**  
C: Evet, ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

**S: Aspose.CAD for Java için destek nasıl alınır?**  
C: Destek için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edebilirsiniz.

**S: Aspose.CAD for Java için geçici bir lisans alabilir miyim?**  
C: Evet, geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

---

**Son Güncelleme:** 2026-01-12  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}