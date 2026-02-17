---
date: 2026-02-17
description: Java CAD kütüphanesi Aspose.CAD for Java'nin DWG'yi PDF'ye veya raster
  görüntülere hızlı ve doğru bir şekilde nasıl dışa aktarabileceğini öğrenin.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Java CAD kütüphanesi Aspose.CAD for Java ile DWG'yi PDF veya Raster formatına
  dışa aktar
url: /tr/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# java cad library Aspose.CAD for Java kullanarak DWG'yi PDF veya Raster olarak dışa aktarma

## Giriş

Bilgisayar destekli tasarım (CAD) dünyasında, çizimlerin verimli bir şekilde işlenmesi çok önemlidir. **java cad library** **Aspose.CAD for Java** ile sadece birkaç satır kodla **export dwg to pdf** — veya raster görüntüler — yapabilirsiniz. Bu öğretici, bir DWG dosyasını yüklemekten yüksek kaliteli bir PDF oluşturulana kadar tüm süreci adım adım gösterir ve Aspose.CAD Java'nın CAD dönüşüm görevleri için neden tercih edilen kütüphane olduğunu vurgular.

## Hızlı Yanıtlar
- **Bu öğretici neyi kapsıyor?** Aspose.CAD for Java kullanarak DWG dosyalarını PDF veya raster görüntülere dışa aktarma.  
- **Bir lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz geçici bir lisans mevcuttur; üretim için tam lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** En yeni Aspose.CAD Java API'si, Java 8+ çalışma zamanlarıyla çalışır.  
- **DWG'yi diğer görüntü formatlarına dönüştürebilir miyim?** Evet – aynı rasterleştirme seçenekleri PNG, JPEG, BMP vb. formatlarda çıktı almanıza olanak tanır.  
- **Dönüşüm ne kadar sürer?** Standart çizimler için genellikle bir saniyenin altında; daha büyük dosyalar birkaç saniye sürebilir.

## Neden java cad library DWG dönüşümü için en iyi seçimdir?

- **Pure Java implementation** – yerel DLL'ler veya harici araçlar yok.  
- **Accurate unit handling** – metrik ve imparatorluk birimleri otomatik olarak algılanır.  
- **High‑quality raster output** – ince ayarlı DPI ve sayfa boyutu kontrolü.  
- **Full PDF support** – ek bağımlılıklar olmadan vektör korumalı PDF oluşturma.  
- **Flexible licensing** – test için **temporary license aspose** ile başlayın, ardından yayına alırken yükseltin.

## “export dwg to pdf” nedir?

DWG'yi PDF'ye dışa aktarmak, yerel bir AutoCAD çizimini taşınabilir, cihaz bağımsız bir PDF belgesine dönüştürmek anlamına gelir. Oluşan PDF, vektör verilerini, katmanları ve ölçeklemeyi korur; bu da paylaşım, baskı veya arşivleme için idealdir.

## Bu dönüşüm için Aspose.CAD Java neden kullanılmalı?

Çünkü **java cad library**, birim dönüşümünden rasterleştirmeye kadar her şeyi dahili olarak yönetir; bu sayede üçüncü‑taraf araçların karmaşıklığından kaçınır ve platformlar arasında tutarlı sonuçlar elde edersiniz.

## Önkoşullar

Kodun içine girmeden önce şunların olduğundan emin olun:

- Java programlama temelleri bilgisi.  
- Aspose.CAD for Java kütüphanesi yüklü. Henüz indirmediyseniz **[buradan](https://releases.aspose.com/cad/java/)** edinebilirsiniz.  
- Test için bir DWG dosyası – bu rehberde örnek **Bottom_plate.dwg** kullanılmıştır.

## İsim Uzaylarını İçe Aktarma

Java projenizde, dönüşümü başlatmak için gerekli sınıfları içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Adım Adım Kılavuz

### Adım 1: DWG Dosyasını Yükleyin

İlk olarak, `Image` sınıfını kullanarak DWG çiziminizi yükleyin. Bu, Aspose.CAD'nin çalışabileceği bellek içi bir temsil oluşturur.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Adım 2: Birim Tipini Belirleyin

Çizimin metrik mi yoksa imparatorluk birimlerini mi kullandığını anlamak, doğru ölçekleme için gereklidir. Yardımcı metod `IsMetric` (kısa bir açıklama için uygulanması atlanmıştır) bir boolean değer döndürür.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Adım 3: Rasterleştirme Seçeneklerini Ayarlayın

Birim sistemine göre sayfa boyutunu, ölçeklemeyi ve hedef birim tipini yapılandırın. Bu seçenekler, DWG'nin PDF'ye gömülmeden önce nasıl rasterleştirileceğini belirler.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Adım 4: PDF Seçeneklerini Yapılandırın (pdf options cad)

`PdfOptions` örneği oluşturun ve rasterleştirme ayarlarını ekleyin. Bu, Aspose.CAD'ye rasterleştirilmiş içeriği son PDF'ye nasıl gömeceğini söyler.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Adım 5: PDF Olarak Kaydedin

Son olarak, çizimi bir PDF dosyasına dışa aktarın. `save` metodu çıktı yolunu ve yapılandırılmış `PdfOptions` nesnesini alır.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Kod tamamlandığında, `DWGDrawings` klasörünüzde **Saved.pdf** dosyasını bulacaksınız; dağıtım veya arşivleme için hazır.

## java cad library ile dwg raster görüntülerini nasıl dönüştürürüm

PDF yerine raster görüntülere ihtiyacınız varsa, `PdfOptions`'ı uygun raster görüntü seçenekleriyle (ör. `PngOptions`, `JpegOptions`) değiştirmeniz yeterlidir. Aynı `CadRasterizationOptions` örneği yeniden kullanılabilir; bu sayede **convert dwg raster** dosyalarını minimum kod değişikliğiyle dönüştürebilirsiniz.

## pdf options cad kullanarak pdf dwg nasıl oluşturulur

Yukarıdaki örnek zaten **generates pdf dwg** çıktısı üretir. `pdfOptions`'ı ayarlayarak—örneğin `pdfOptions.setCompress(true)` ayarı—PDF boyutunu ve kalitesini kontrol edebilirsiniz. Bu, **pdf options cad** API'sinin esnekliğini gösterir.

## Yaygın Sorunlar ve İpuçları

- **Incorrect page size** – Birim dönüşüm mantığını iki kez kontrol edin; uyumsuz katsayılar aşırı büyük sayfalara neden olabilir.  
- **Missing fonts or lineweights** – Dönüşümden önce DWG'nin dış kaynaklara referans verdiğinden emin olun.  
- **Performance on large drawings** – `CadRasterizationOptions` içinde `DPI` ayarını yalnızca daha yüksek kalite gerektiğinde artırın; düşük DPI işlemeyi hızlandırır.  
- **License concerns** – Değerlendirme için **temporary license aspose** kullanabilirsiniz; üretim dağıtımları için tam lisans gereklidir.

## Sıkça Sorulan Sorular

**S: Aspose.CAD for Java'yı diğer Java çerçeveleriyle kullanabilir miyim?**  
C: Evet, Aspose.CAD for Java, Spring, Jakarta EE ve Android gibi popüler Java çerçeveleriyle sorunsuz bir şekilde entegre olur.

**S: Aspose.CAD for Java için geçici bir lisans mevcut mu?**  
C: Evet, geçici bir lisansı **[buradan](https://purchase.aspose.com/temporary-license/)** alabilirsiniz.

**S: Aspose.CAD for Java için destek nereden bulunur?**  
C: Topluluk ve Aspose mühendislerinden yardım almak için **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** adresini ziyaret edin.

**S: Aspose.CAD for Java için lisans nasıl satın alınır?**  
C: Lisansı **[buradan](https://purchase.aspose.com/buy)** satın alabilirsiniz.

**S: Aspose.CAD for Java hangi birimleri destekliyor?**  
C: Aspose.CAD for Java, hem metrik hem de imparatorluk birimlerini destekler ve çizimin birim sistemini otomatik olarak algılar.

**S: Aynı API'yi kullanarak DWG'yi diğer görüntü formatlarına (ör. PNG, JPEG) dönüştürebilir miyim?**  
C: Kesinlikle. `PdfOptions`'ı uygun raster görüntü seçenekleriyle (ör. `PngOptions`) değiştirin ve aynı `CadRasterizationOptions`'ı yeniden kullanın.

## Sonuç

Bu öğreticide, **java cad library** Aspose.CAD for Java kullanarak **export dwg to pdf** ve raster görüntülerinin nasıl yapılacağı gösterildi. Adım adım kılavuzu izleyerek, belgeler için PDF'ye ya da web gösterimi için raster görüntülere ihtiyaç duyduğunuz her Java uygulamasına güvenilir CAD dönüşümünü entegre edebilirsiniz.

---

**Son Güncelleme:** 2026-02-17  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.10  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}