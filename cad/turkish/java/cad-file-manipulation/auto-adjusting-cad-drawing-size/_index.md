---
date: 2025-12-22
description: Aspose.CAD ile Java'da CAD çizimlerini dışa aktarmayı ve DWG'yi BMP'ye
  dönüştürmeyi öğrenin. Verimli CAD dosyası manipülasyonu için bu adım adım kılavuzu
  izleyin.
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java kullanarak CAD Çizimini BMP'ye Dışa Aktarma
url: /tr/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspise.CAD for Java Kullanarak CAD Çizimini BMP Olarak Dışa Aktarma

## Giriş

Java'dan **how to export cad** dosyalarını dışa aktarmanın net ve güvenilir bir yolunu arıyorsanız, doğru yerdesiniz. Aspose.CAD for Java ile sadece birkaç satır kodla çizim boyutlarını otomatik ayarlamakla kalmaz, aynı zamanda **DWG'yi BMP'ye dönüştürür**sünüz. Bu öğretici, ortamınızı kurmaktan orijinal CAD düzenini koruyan bir BMP görüntüsü üretmeye kadar tüm süreci adım adım gösterir.

## Hızlı Yanıtlar
- **“how to export cad” ne anlama geliyor?** CAD dosyalarını (DWG, DXF vb.) BMP, PNG veya PDF gibi başka bir formata dönüştürmeyi ifade eder.  
- **Hangi kütüphane dönüşümü gerçekleştirir?** Bu görev için Aspose.CAD for Java basit bir API sağlar.  
- **Bir lisansa ihtiyacım var mı?** Test için geçici bir lisans yeterlidir; üretim için tam lisans gereklidir.  
- **Birden fazla düzeni aynı anda dışa aktarabilir miyim?** Evet – `Layouts` özelliğini ayarlayarak hangi düzenlerin render edileceğini belirtebilirsiniz.  
- **BMP tek çıktı formatı mı?** Hayır – PNG, JPEG, TIFF ve daha fazlasına da dışa aktarabilirsiniz.

## Aspose.CAD ile “how to export cad” nedir?
CAD dışa aktarma, yerel bir CAD çizimini (ör. bir DWG dosyası) raster görüntüye veya başka bir vektör formatına dönüştürmek anlamına gelir. Aspose.CAD tüm zorlu süreci yönetir: CAD yapısını ayrıştırma, vektör varlıklarını rasterleştirme ve sonucu seçtiğiniz görüntü formatına yazma.

## Java için Aspose.CAD'i **DWG'yi BMP'ye dönüştürmek** için neden kullanmalısınız?
- **Harici bağımlılık yok** – saf Java, yerel DLL'ler yok.  
- **DWG, DXF, DGN ve diğer formatlar için tam destek**.  
- **İnce ayarlı kontrol** rasterleştirme seçenekleri üzerinde, örneğin düzen seçimi, ölçekleme ve arka plan rengi.  
- **Yüksek performans** sunucularda toplu işleme için uygundur.

## Ön Koşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit** – bunu [buradan](https://www.java.com/en/download/) indirin.  
2. **Aspose.CAD for Java kütüphanesi** – en son JAR dosyasını [buradan](https://releases.aspose.com/cad/java/) edinin.  
3. **Örnek CAD dosyası** – projenizin belge dizinine yerleştirilmiş bir DWG dosyası (ör. `sample.dwg`).

## İsim Uzaylarını İçe Aktarma

Java uygulamanızda, Aspose.CAD işlevselliğini kullanmak için gerekli isim uzaylarını ekleyin. İşte bir örnek:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Şimdi, **how to export cad** sürecini yönetilebilir adımlara ayıralım.

## Adım‑Adım Kılavuz

### Adım 1: CAD Çizimini Yükleyin

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

Kaynak DWG dosyasını bir `Image` nesnesine yüklüyoruz; bu nesne sonraki tüm işlemler için giriş noktasıdır.

### Adım 2: `BmpOptions` Oluşturun

```java
BmpOptions bmpOptions = new BmpOptions();
```

### Adım 3: Rasterleştirme Ayarlarını Yapılandırın

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Burada rasterleştirme seçeneklerini BMP seçeneklerine bağlayarak CAD varlıklarının nasıl render edileceğini kontrol edebiliyoruz.

### Adım 4: Dışa Aktarılacak Düzen(leri) Ayarlayın

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

`Layouts` özelliği Aspose.CAD'e hangi çizim düzenlerinin dahil edileceğini söyler. Çoğu durumda, dönüştürmek istediğiniz ana düzen `"Model"`'dir.

### Adım 5: BMP Formatına Dışa Aktarın

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

Yapılandırılmış `BmpOptions` ile `save` metodunu çağırmak BMP dosyasını diske yazar. Bu, **DWG'yi BMP'ye dönüştürme** iş akışını tamamlar.

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| Çıktı resmi boş | Yanlış düzen adı veya eksik düzen | Düzen adının CAD dosyasıyla eşleştiğini doğrulayın (ör. `"Model"`). |
| Düşük çözünürlük | Varsayılan DPI düşük | Kaydetmeden önce `cadRasterizationOptions.setResolution(300);` ayarlayın. |
| Büyük dosyalar için bellek yetersizliği hatası | Büyük çizimler daha fazla heap gerektirir | JVM heap boyutunu (`-Xmx2g`) artırın veya sayfaları tek tek işleyin. |

## Sıkça Sorulan Sorular

**S: Aspose.CAD farklı CAD dosya formatlarıyla uyumlu mu?**  
C: Evet, Aspose.CAD DWG, DXF, DGN ve birçok diğer formatı destekler.

**S: Aspose.CAD'i ticari projelerde kullanabilir miyim?**  
C: Kesinlikle. Üretim kullanımı için bir lisans satın alın [buradan](https://purchase.aspose.com/buy).

**S: Test için geçici bir lisans nasıl alabilirim?**  
C: Geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

**S: Topluluk desteğini nereden bulabilirim?**  
C: Aspose.CAD topluluk forumuna [forum](https://forum.aspose.com/c/cad/19) adresinden katılın.

**S: Aspose.CAD for Java için ücretsiz deneme mevcut mu?**  
C: Evet, ücretsiz denemeyi [buradan](https://releases.aspose.com/) indirebilirsiniz.

 Sonuç

Bu rehberde Java'dan **how to export cad** dosyalarını ve Aspose.CAD kullanarak **DWG'yi BMP'ye dönüştürmeyi** gösterdik. Yukarıdaki beş adımı izleyerek CAD‑görüntü dönüşümünü herhangi bir Java uygulamasına entegre edebilirsiniz; ister masaüstü aracı, ister web servisi, ister toplu işleme hattı olsun. Seçenek sınıfını değiştirerek diğer çıktı formatlarını (PNG, JPEG, PDF) keşfedin ve tüm CAD manipülasyon ihtiyaçlarınızı karşılamak için Aspose.CAD'in zengin özellik setinden yararlanın.

---

**Son Güncelleme:** 2025-12-22  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}