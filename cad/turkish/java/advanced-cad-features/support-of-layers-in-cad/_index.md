---
date: 2025-12-13
description: Aspose.CAD kullanarak Java'da CAD'i JPEG olarak kaydetmeyi, birden fazla
  katman eklemeyi ve hassas görüntü dönüşümü için CAD boyutlarını ayarlamayı öğrenin.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Java'da Katman Desteğiyle CAD'yi JPEG Olarak Kaydet
url: /tr/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da Katman Desteğiyle CAD'i JPEG Olarak Kaydet

## Giriş

Bu öğreticide, Aspose.CAD for Java'da katman desteğinden tam olarak yararlanarak **CAD'i JPEG olarak kaydetmeyi** keşfedeceksiniz. Katmanlar, bir çizimin belirli bölümlerini izole etmenizi sağlar ve yalnızca ihtiyacınız olanı dışa aktarmayı kolaylaştırır. Ortamı kurmaktan, seçtiğiniz katmanları içeren bir JPEG dışa aktarmaya kadar her adımı adım adım inceleyeceğiz.

## Hızlı Yanıtlar
- **“save CAD as JPEG” ne anlama geliyor?** Bir CAD çizimini raster JPEG görüntüsüne dönüştürür.  
- **Sadece seçili katmanları ekleyebilir miyim?** Evet – hangi katmanların render edileceğini belirtmek için `setLayers` metodunu kullanın.  
- **Görüntü boyutunu nasıl değiştiririm?** `CadRasterizationOptions` içinde `setPageWidth` ve `setPageHeight` ayarlarını değiştirin.  
- **Bu sadece Java çözümü mü?** Örnek Aspose.CAD for Java kullanıyor, ancak aynı kavramlar diğer dillerde de geçerlidir.  
- **Lisans gerekir mi?** Test için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.

## Önkoşullar

İlerlemeye başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Aspose.CAD for Java Kütüphanesi** – [website](https://releases.aspose.com/cad/java/) adresinden indirin. Kurulum kılavuzunu izleyerek JAR dosyalarını projenizin sınıf yoluna ekleyin.  
2. **Java Geliştirme Ortamı** – makinenizde yüklü bir JDK (8 veya daha yeni).

Artık kurulum tamam, **CAD'i JPEG olarak kaydetmek** için seçici katman render'ı sağlayan kodu inceleyelim.

## İçe Aktarma Ad Alanları

Gerekli Aspose.CAD sınıflarını ve standart Java yardımcılarını içe aktararak başlayın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Adım‑Adım Kılavuz

### Adım 1: Dosya Yollarını Ayarlama

Kaynak DWF dosyasının nerede bulunduğunu ve çıktının JPEG olarak nereye yazılacağını tanımlayın.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Adım 2: DWF Görüntüsünü Yükleme

Aspose.CAD’in `Image.load` metodunu kullanarak CAD çizimini okuyun.

```java
Image image = Image.load(srcFile);
```

### Adım 3: Rasterizasyon Seçeneklerini Yapılandırma (CAD Boyutlarını Ayarlama)

Bir `CadRasterizationOptions` örneği oluşturun ve istenen çıktı boyutunu ayarlayın. Bu değerleri değiştirmek, son JPEG için **CAD boyutlarını ayarlamanızı** sağlar.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Adım 4: Katmanları Belirtme (Birden Çok Katman Ekleme)

Birden fazla katman render etmek istiyorsanız, isimlerini listeye eklemeniz yeterlidir. Burada “LayerA” adlı tek bir katmanla başlıyoruz.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Pro ipucu:* **Birden çok katman eklemek** için `Arrays.asList` çağrısını genişletin, örn. `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Adım 5: JPEG Seçeneklerini Yapılandırma (Java CAD Görüntüsünü Dönüştürme)

Rasterizasyon ayarlarını JPEG çıktı formatına bağlayın.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Adım 6: JPG Olarak Dışa Aktarma (CAD'i JPEG Olarak Kaydet)

Son olarak, görüntüyü diske yazın. Bu adım **seçili katmanları içeren CAD çizimini JPEG dosyası olarak kaydeder**.

```java
image.save(outFile, jpegOptions);
```

Bu adımları izleyerek, hangi katmanların görüneceğini kontrol ederken ve görüntü boyutlarını özelleştirirken **CAD'i JPEG olarak başarıyla kaydetmiş** olacaksınız.

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **Katmanlar görünmüyor** | Katman adlarının DWF dosyasında saklananlarla tam olarak eşleştiğinden emin olun (büyük/küçük harfe duyarlı). |
| **Çıktı resmi boş** | `setPageWidth` ve `setPageHeight` değerlerinin çizimin kapsamı için yeterince büyük olduğundan emin olun. |
| **Lisans istisnası** | Test için deneme lisansı kullanın; üretim ortamları için tam lisans edinin. |

## Sıkça Sorulan Sorular

**S: Rasterizasyon seçeneklerine birden çok katman ekleyebilir miyim?**  
C: Kesinlikle. `stringList`i ek katman adlarıyla genişletin, örn. `Arrays.asList("LayerA", "LayerB")`.

**S: Aspose.CAD diğer CAD formatlarıyla uyumlu mu?**  
C: Evet, DWG, DXF, DWF ve daha birçok formatı destekler.

**S: Çıktı görüntüsü boyutlarını nasıl değiştirebilirim?**  
C: `CadRasterizationOptions` örneğinde `setPageWidth` ve `setPageHeight` ayarlarını değiştirin.

**S: Aspose.CAD için lisans nereden satın alınabilir?**  
C: Lisans seçeneklerini [burada](https://purchase.aspose.com/buy) inceleyebilirsiniz.

**S: Topluluk desteği nereden alınabilir?**  
C: Yardım ve tartışmalar için Aspose.CAD topluluğuna [forum](https://forum.aspose.com/c/cad/19) üzerinden katılabilirsiniz.

---

**Son Güncelleme:** 2025-12-13  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}