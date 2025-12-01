---
date: 2025-12-01
description: Aspose.CAD for Java kullanarak dxf dosyalarını görüntülere nasıl dışa
  aktaracağınızı öğrenin. Bu adım adım kılavuz, dxf'i görüntüye ve dwf'yi jpeg'e nasıl
  dönüştüreceğinizi gösterir.
language: tr
linktitle: Export Specific DXF Layout to Image with Java
second_title: Aspose.CAD Java API
title: Aspose.CAD ile Java'da DXF Düzenini Görüntüye Dışa Aktarma
url: /java/additional-features/export-specific-layout-to-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD ile Java'da DXF Düzenini Görüntü Olarak Dışa Aktarma

## Giriş

Java uygulamasında **how to export dxf** çizimlerini raster görüntüler olarak dışa aktarmanız gerekiyorsa, Aspose.CAD for Java bu süreci basitleştirir. Bu öğreticide, kaynak dosyadan belirli bir düzeni (katmanı) seçerek **convert dxf to image** (ve hatta **convert dwf to jpeg**) nasıl yapılacağını tam olarak göreceksiniz. Projeyi kurmaktan son JPEG'i kaydetmeye kadar her adımı adım adım anlatacağız, böylece çözümü kendi kod tabanınıza güvenle entegre edebilirsiniz.

## Hızlı Yanıtlar
- **Gerekli kütüphane nedir?** Aspose.CAD for Java (ücretsiz deneme mevcuttur).  
- **Hangi formatlar dışa aktarılabilir?** DXF, DWF, DWG → JPEG, PNG, BMP, TIFF, vb.  
- **Tek bir düzen/katı seçebilir miyim?** Evet – istediğiniz katmanları belirtmek için `CadRasterizationOptions.setLayers()` kullanın.  
- **Üretim için lisansa ihtiyacım var mı?** Değerlendirme dışı kullanım için ticari lisans gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir dönüşüm için yaklaşık 10‑15 dakika.

## DXF Düzenini Görüntü Olarak Dışa Aktarmak Ne Anlama Gelir?

DXF düzenini dışa aktarmak, bir vektör çizimini (DXF/DWF) JPEG gibi bir bitmap formatına rasterleştirmek anlamına gelir. Bu, çizimleri web sayfalarına gömmek, küçük resimler oluşturmak veya CAD yazılımı olmayan kullanıcılarla paylaşmak istediğinizde faydalıdır.

## Neden DXF'i Aspose.CAD ile Görüntüye Dönüştürmeliyim?

- **Harici CAD yazılımı gerekmez** – dönüşüm tamamen Java içinde çalışır.  
- **İnce ayarlı kontrol** – tek tek katmanları seçebilir, sayfa boyutunu, DPI'yi ve arka plan rengini ayarlayabilirsiniz.  
- **Geniş format desteği** – JPEG'in yanı sıra PNG, BMP, TIFF ve daha fazlasını çıktı olarak alabilirsiniz.  
- **Yüksek doğruluk** – kütüphane rasterleştirme sırasında çizgi kalınlıklarını, renkleri ve yazı tiplerini korur.

## Önkoşullar

- **Aspose.CAD for Java** – en son JAR dosyasını [Aspose.CAD indirme sayfasından](https://releases.aspose.com/cad/java/) indirin.  
- Bir **Java geliştirme ortamı** (JDK 8 veya üzeri).  
- Dönüştürmek istediğiniz **DXF/DWF dosyası** (örnek `for_layers_test.dwf` dosyasını kullanır).

## İsim Uzaylarını İçe Aktarma

First, import the classes you’ll need.  
```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.fileformats.dwf.whip.objects.DwfWhipLayer;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dwf.DwfImage;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

Now let’s break down the conversion process step by step.

## Adım 1: Kaynak Dizinini Ayarlama

Define the folder that contains your source DXF/DWF file.

```java
String dataDir = "Your Document Directory" + "DXFDrawings\\";
```

> **Pro ipucu:** `FileNotFoundException` hatasından kaçınmak için mutlak bir yol ya da projenizin köküne göre bir yol kullanın.

## Adım 2: DXF/DWF Görüntüsünü Yükleme

Load the drawing with Aspose.CAD. The example uses a DWF file, but the same code works for DXF.

```java
String srcFile = dataDir + "for_layers_test.dwf";
DwfImage image = (DwfImage) Image.load(srcFile);
```

> **Neden DWF?** Kütüphane DWF'yi DXF gibi işler, bu yüzden aynı rasterleştirme seçenekleri geçerlidir ve **convert dwf to jpeg** işlemini kolayca yapabilirsiniz.

## Adım 3: Katman İsimlerini Almak

Retrieve all layer names so you can pick the one you want to export.

```java
List<String> layersNames = image.getLayers().getLayersNames();
```

Artık her düzenin adını içeren bir `List<String>`'e sahipsiniz.

## Adım 4: Rasterleştirme Seçeneklerini Ayarlama

Configure the output image size, resolution, and other raster settings.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

`PageWidth` ve `PageHeight` değerlerini istediğiniz görüntü boyutlarına göre ayarlayın. DPI'yi `setResolution` ile de belirleyebilirsiniz.

## Adım 5: Katmanları Belirtme (Düzeni Seçme)

Convert the layer list to the format required by `setLayers()` and choose the layers you want to render.

```java
String[] stringArray = Arrays.copyOf(layersNames.toArray(), layersNames.toArray().length, String[].class);
List<String> stringList = Arrays.asList(stringArray);
rasterizationOptions.setLayers(stringList);
```

Yalnızca tek bir düzene ihtiyacınız varsa, `stringList`'i o belirli katman adını içeren bir listeyle değiştirin.

## Adım 6: JPEG Seçeneklerini Yapılandırma

Wrap the rasterization settings inside a `JpegOptions` object.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Gerekirse JPEG kalitesini (`jpegOptions.setQuality(90)`) de ayarlayabilirsiniz.

## Adım 7: DXF/DWF'yi Görüntü Olarak Dışa Aktarma

Finally, save the rasterized image to disk.

```java
String output = dataDir + "for_layers_test.jpg";
image.save(output, jpegOptions);
```

`for_layers_test.jpg` dosyası artık seçilen düzeni yüksek kaliteli bir JPEG olarak içeriyor.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|-------|
| **Boş çıktı görüntüsü** | Yanlış katman adı veya boş katman listesi | `layersNames`'in beklenen adları içerdiğini doğrulayın ve doğru listeyi `setLayers()`'a gönderin. |
| **Bellek yetersizliği hatası** | Çok büyük sayfa boyutları | `PageWidth/PageHeight` değerlerini azaltın veya JVM yığın boyutunu (`-Xmx`) artırın. |
| **Desteklenmeyen dosya formatı** | Eski bir Aspose.CAD sürümü kullanmak | Aspose'tan en son JAR dosyasına güncelleyin. |
| **Düşük görüntü kalitesi** | Varsayılan JPEG kalitesi düşük | Kaydetmeden önce `jpegOptions.setQuality(95)` çağırın. |

## Sıkça Sorulan Sorular

**S: Tek bir çalıştırmada birden fazla DXF düzenini dışa aktarabilir miyim?**  
C: Evet. İstenen katman adları üzerinde döngü kurun, her yineleme için `rasterizationOptions.setLayers()`'i güncelleyin ve benzersiz bir çıktı dosya adıyla `image.save()` çağırın.

**S: Aspose.CAD for Java tüm Java sürümleriyle uyumlu mu?**  
C: Kütüphane Java 8 ve üzeri sürümleri destekler. Sürüm notlarında sürüme özgü bilgiler için kontrol edin.

**S: Dönüşüm sırasında hataları nasıl yönetirim?**  
C: Dönüşüm kodunu bir `try‑catch` bloğuna alın ve `Exception` ya da belirli Aspose istisnalarını yakalayarak anlamlı mesajlar kaydedin veya gösterin.

**S: JPEG dışındaki hangi görüntü formatları mevcuttur?**  
C: `JpegOptions` yerine uygun sınıfı (`PngOptions`, `BmpOptions`, `TiffOptions` vb.) kullanarak bu formatları seçebilirsiniz.

**S: Arka plan rengini veya çizgi kalınlığını özelleştirebilir miyim?**  
C: Evet. `CadRasterizationOptions` `setBackgroundColor()` ve `setLineWeight()` gibi ince ayar özellikleri sunar.

**Son Güncelleme:** 2025-12-01  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.11 (yazım anındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}