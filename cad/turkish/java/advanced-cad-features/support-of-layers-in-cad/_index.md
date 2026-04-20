---
date: 2026-02-17
description: Aspose.CAD kullanarak Java'da DWG'yi JPEG olarak kaydetmeyi, birden fazla
  katman eklemeyi ve hassas görüntü dönüşümü için CAD boyutlarını ayarlamayı öğrenin.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Java'da Katman Desteğiyle DWG'yi JPEG Olarak Kaydet
url: /tr/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi Katman Desteğiyle Java'da JPEG Olarak Kaydet

## Giriş

Bu öğreticide **DWG'yi JPEG olarak kaydet**meyi ve Aspose.CAD for Java'da katman desteğinden tam olarak yararlanmayı öğreneceksiniz. Katmanlar, bir çizimin belirli bölümlerini izole etmenizi sağlar ve yalnızca ihtiyacınız olanı dışa aktarmayı kolaylaştırır. Ortamı kurmaktan, seçtiğiniz katmanları içeren bir JPEG dışa aktarmaya kadar her adımı adım adım inceleyeceğiz.

## Hızlı Yanıtlar
- **“DWG'yi JPEG olarak kaydet” ne anlama geliyor?** Bir DWG (veya diğer CAD) çizimini raster JPEG görüntüsüne dönüştürür.  
- **Yalnızca seçili katmanları ekleyebilir miyim?** Evet – hangi katmanların render edileceğini belirlemek için `setLayers` metodunu kullanın.  
- **Görüntü boyutunu nasıl değiştiririm?** `CadRasterizationOptions` içinde `setPageWidth` ve `setPageHeight` değerlerini ayarlayın.  
- **Bu sadece Java çözümü mü?** Örnek Aspose.CAD for Java kullanıyor, ancak aynı kavramlar diğer dillerde de uygulanabilir.  
- **Lisans gerekir mi?** Test için ücretsiz deneme sürümü yeterli; üretim için ticari bir lisans gereklidir.

## “DWG'yi JPEG olarak kaydet” nedir?
DWG'yi JPEG olarak kaydetmek, vektör tabanlı bir CAD dosyasını (DWG, DWF, DXF vb.) standart bir JPEG bitmapine rasterleştirmek anlamına gelir. Bu, CAD çizimlerini yalnızca raster görüntüleri destekleyen web sayfalarına, e‑postalara veya raporlara eklemeniz gerektiğinde kullanışlıdır.

## Katman‑bilinçli JPEG dönüşümünü neden kullanmalısınız?
- **İlgili verilere odaklanın:** İhtiyacınız olan katmanları dışa aktararak dosya boyutunu ve görsel karmaşayı azaltın.  
- **Tasarım amacını koruyun:** Katmanlar, nesnelerin mantıksal gruplamasını korur; böylece aynı kaynak dosyayı farklı çıktılar için yeniden kullanabilirsiniz.  
- **Boyutlar üzerinde tam kontrol:** Rasterleştirme seçeneklerini ayarlayarak yayın gereksinimlerinize uygun yüksek çözünürlüklü görüntüler üretebilirsiniz.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

1. **Aspose.CAD for Java Kütüphanesi** – [web sitesi](https://releases.aspose.com/cad/java/)'nden indirin. Kurulum kılavuzunu izleyerek JAR dosyalarını projenizin sınıf yoluna ekleyin.  
2. **Java Geliştirme Ortamı** – makinenizde yüklü bir JDK (8 veya daha yeni bir sürüm).

Şimdi ortamımız hazır, **DWG'yi JPEG olarak kaydet** ve seçici katman render'ı için gereken kodu inceleyelim.

## İsim Uzaylarını İçe Aktarma

Gerekli Aspose.CAD sınıflarını ve standart Java yardımcılarını içe aktarın:

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

Kaynak DWF dosyasının konumunu ve çıktının JPEG olarak yazılacağı yeri tanımlayın.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Adım 2: DWF Görüntüsünü Yükleme

CAD çizimini okumak için Aspose.CAD’in `Image.load` metodunu kullanın.

```java
Image image = Image.load(srcFile);
```

### Adım 3: Rasterleştirme Seçeneklerini Yapılandırma (CAD Boyutlarını Ayarlama)

Bir `CadRasterizationOptions` örneği oluşturun ve istenen çıktı boyutunu ayarlayın. Bu değerleri değiştirerek **CAD boyutlarını** nihai JPEG için **ayarlayabilirsiniz**.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Adım 4: Katmanları Belirtme (Birden Çok Katman Ekleme)

Birden fazla katman render etmek istiyorsanız, adlarını listeye ekleyin. Burada “LayerA” adlı tek bir katmanla başlıyoruz.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*İpucu:* **Birden çok katman eklemek** için `Arrays.asList` çağrısını genişletin, örneğin `Arrays.asList("LayerA", "LayerB", "LayerC")`. Bu sayede **belirli CAD katmanlarını** dönüşüm için seçebilirsiniz.

### Adım 5: JPEG Seçeneklerini Yapılandırma (Java CAD Görüntüsü Dönüştürme)

Rasterleştirme ayarlarını JPEG çıktı formatına bağlayın.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Adım 6: JPG Olarak Dışa Aktarma (DWG'yi JPEG Olarak Kaydet)

Son olarak görüntüyü diske yazın. Bu adım **CAD çizimini yalnızca seçili katmanları içeren bir JPEG dosyası** olarak kaydeder.

```java
image.save(outFile, jpegOptions);
```

Bu adımları izleyerek **DWG'yi JPEG olarak kaydet** ve hangi katmanların görüneceğini kontrol ederken görüntü boyutlarını da özelleştirmiş oldunuz.

## Katman Seçimiyle DWF'den JPEG'e Dönüştürme

Örnek DWF kaynağı kullanıyor olsa da aynı rasterleştirme hattı, desteklenen herhangi bir CAD formatı (DWG, DXF, DGN vb.) için çalışır. `srcFile` içindeki dosya uzantısını değiştirmeniz yeterlidir; kütüphane **DWF'yi JPEG'e dönüştürme** (veya başka bir formata) işlemini otomatik olarak gerçekleştirir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **Katmanlar görünmüyor** | Katman adlarının DWF dosyasında saklanan isimlerle tam olarak eşleştiğinden emin olun (büyük/küçük harf duyarlıdır). |
| **Çıktı görüntüsü boş** | `setPageWidth` ve `setPageHeight` değerlerinin çizimin kapsamına yeterli büyüklükte olduğundan emin olun. |
| **Lisans istisnası** | Test için deneme lisansı kullanın; üretim ortamları için tam lisans edinin. |

## Sık Sorulan Sorular

**S: Rasterleştirme seçeneklerine birden çok katman ekleyebilir miyim?**  
C: Kesinlikle. `stringList`i ek katman adlarıyla genişletin, örneğin `Arrays.asList("LayerA", "LayerB")`.

**S: Aspose.CAD diğer CAD formatlarıyla uyumlu mu?**  
C: Evet, DWG, DXF, DWF ve daha birçok formatı destekler.

**S: Çıktı görüntüsü boyutlarını nasıl değiştirebilirim?**  
C: `CadRasterizationOptions` örneğindeki `setPageWidth` ve `setPageHeight` metodlarını değiştirin.

**S: Aspose.CAD için lisans nereden satın alınır?**  
C: Lisans seçeneklerini [burada](https://purchase.aspose.com/buy) inceleyebilirsiniz.

**S: Topluluk desteği nereden alınır?**  
C: Yardım ve tartışmalar için Aspose.CAD topluluğuna [forum](https://forum.aspose.com/c/cad/19) üzerinden katılabilirsiniz.

---

**Son Güncelleme:** 2026-02-17  
**Test Edilen:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}