---
date: 2025-12-18
description: Aspose.CAD kullanarak Java'da dwg'yi pdf veya raster görüntülere nasıl
  dışa aktaracağınızı keşfedin. Bu adım adım rehber, DWG dosyalarının hassas, verimli
  ve kolay dönüşümünü sağlar.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java kullanarak DWG'yi PDF veya Raster formatına dışa aktar
url: /tr/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi PDF veya Raster Olarak Aspose.CAD for Java Kullanarak Dışa Aktarma

## Giriş

Bilgisayar destekli tasarım (CAD) dünyasında, çizimlerin verimli bir şekilde işlenmesi hayati öneme sahiptir. **Aspose.CAD for Java** ile **dwg'yi pdf'ye dışa aktarabilir** — veya raster görüntülere — sadece birkaç satır kodla bunu yapabilirsiniz. Bu öğretici, bir DWG dosyasını yüklemekten yüksek kaliteli bir PDF üretmeye kadar tüm süreci adım adım gösterirken, Aspose.CAD Java’nın CAD dönüşüm görevleri için neden tercih edilen kütüphane olduğunu vurgular.

## Hızlı Yanıtlar
- **Bu öğreticide ne ele alınıyor?** Aspose.CAD for Java kullanarak DWG dosyalarını PDF veya raster görüntülere dışa aktarma.  
- **Lisans gerekli mi?** Değerlendirme için ücretsiz geçici bir lisans mevcuttur; üretim için tam lisans gereklidir.  
- **Hangi Java sürümü destekleniyor?** En yeni Aspose.CAD Java API’si, Java 8+ çalışma zamanı ile uyumludur.  
- **DWG'yi başka görüntü formatlarına dönüştürebilir miyim?** Evet – aynı rasterleştirme seçenekleri PNG, JPEG, BMP vb. formatlarda çıktı almanızı sağlar.  
- **Dönüşüm ne kadar sürer?** Standart çizimler için genellikle bir saniyenin altında; daha büyük dosyalar birkaç saniye sürebilir.

## “export dwg to pdf” ne demektir?
DWG'yi PDF’ye dışa aktarmak, yerel bir AutoCAD çizimini taşınabilir, cihaz bağımsız bir PDF belgesine dönüştürmek anlamına gelir. Oluşan PDF, vektör verilerini, katmanları ve ölçeklemeyi korur; bu da paylaşım, baskı veya arşivleme için idealdir.

## Aspose.CAD Java’yı bu dönüşüm için neden kullanmalıyım?
- **Harici bağımlılık yok** – saf Java, yerel DLL gerektirmez.  
- **Doğru birim yönetimi** – metrik ya da imperial birimleri otomatik olarak dikkate alır.  
- **Yüksek kaliteli raster çıktısı** – DPI ve sayfa boyutu kontrolü ince ayarlarla yapılabilir.  
- **Tam PDF desteği** – ek kütüphanelere ihtiyaç duymadan vektör korumalı PDF üretimi.

## Önkoşullar

Koda geçmeden önce şunların hazır olduğundan emin olun:

- Java programlama temelleri.  
- Aspose.CAD for Java kütüphanesi yüklü. Henüz indirmediyseniz **[buradan](https://releases.aspose.com/cad/java/)** edinebilirsiniz.  
- Test amaçlı bir DWG dosyası – bu rehberde örnek **Bottom_plate.dwg** kullanılmaktadır.

## İsim Uzaylarını İçe Aktarma

Java projenizde dönüşümü başlatmak için gerekli sınıfları içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Adım Adım Kılavuz

### Adım 1: DWG Dosyasını Yükleyin

İlk olarak, `Image` sınıfını kullanarak DWG çiziminizi yükleyin. Bu, Aspose.CAD’nin çalışabileceği bellek içi bir temsil oluşturur.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Adım 2: Birim Tipini Belirleyin

Çizimin metrik mi yoksa imperial mi olduğunu anlamak, doğru ölçekleme için kritiktir. Yardımcı metod `IsMetric` (uygulama detayı burada verilmemiştir) bir boolean değer döndürür.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Adım 3: Rasterleştirme Seçeneklerini Ayarlayın

Birim sistemine göre sayfa boyutu, ölçekleme ve hedef birim tipini yapılandırın. Bu seçenekler, DWG rasterleştirilmeden önce PDF’ye nasıl sarmalanacağını belirler.

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

### Adım 4: PDF Seçeneklerini Yapılandırın

Bir `PdfOptions` örneği oluşturun ve rasterleştirme ayarlarını ekleyin. Bu, Aspose.CAD’ye rasterleştirilmiş içeriği son PDF’e nasıl gömeceğini söyler.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Adım 5: PDF Olarak Kaydedin

Son olarak, çizimi bir PDF dosyasına dışa aktarın. `save` metodu çıktı yolunu ve yapılandırılmış `PdfOptions` nesnesini alır.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Kod tamamlandığında, `DWGDrawings` klasörünüzde **Saved.pdf** dosyasını bulacaksınız; dağıtım veya arşivleme için hazırdır.

## Yaygın Sorunlar ve İpuçları

- **Yanlış sayfa boyutu** – Birim dönüşüm mantığını iki kez kontrol edin; uyumsuz katsayılar aşırı büyük sayfalara yol açabilir.  
- **Eksik yazı tipleri veya çizgi kalınlıkları** – Dönüşümden önce DWG’nin dış kaynakları referans ettiğinden emin olun.  
- **Büyük çizimlerde performans** – `CadRasterizationOptions` içindeki `DPI` ayarını yalnızca yüksek kalite gerektiğinde artırın; düşük DPI işleme süresini hızlandırır.

## Sık Sorulan Sorular

**S: Aspose.CAD for Java’yı diğer Java çerçeveleriyle kullanabilir miyim?**  
C: Evet, Aspose.CAD for Java Spring, Jakarta EE ve Android gibi popüler Java çerçeveleriyle sorunsuz entegrasyon sağlar.

**S: Aspose.CAD for Java için geçici bir lisans mevcut mu?**  
C: Evet, geçici lisansı **[buradan](https://purchase.aspose.com/temporary-license/)** alabilirsiniz.

**S: Aspose.CAD for Java için destek nereden alınır?**  
C: **[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19)** üzerinden topluluk ve Aspose mühendislerinden yardım alabilirsiniz.

**S: Aspose.CAD for Java lisansı nasıl satın alınır?**  
C: Lisansı **[buradan](https://purchase.aspose.com/buy)** satın alabilirsiniz.

**S: Aspose.CAD for Java hangi birimleri destekliyor?**  
C: Aspose.CAD for Java, hem metrik hem de imperial birimleri destekler ve çizimin birim sistemini otomatik olarak algılar.

**S: Aynı API ile DWG'yi diğer görüntü formatlarına (ör. PNG, JPEG) dönüştürebilir miyim?**  
C: Kesinlikle. `PdfOptions` yerine uygun raster görüntü seçeneklerini (ör. `PngOptions`) kullanın ve aynı `CadRasterizationOptions` ayarlarını yeniden değerlendirin.

## Sonuç

Bu öğreticide **dwg'yi pdf'ye ve raster görüntülere dışa aktarma** işlemini Aspose.CAD for Java kullanarak gösterdik. Adım adım kılavuzu izleyerek, PDF belgeleri için ya da web gösterimi için raster görüntüler üretmek istediğiniz her Java uygulamasına güvenilir bir CAD dönüşümünü entegre edebilirsiniz.

---

**Son Güncelleme:** 2025-12-18  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.10  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}