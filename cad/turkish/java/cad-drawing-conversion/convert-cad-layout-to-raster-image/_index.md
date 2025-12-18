---
date: 2025-12-18
description: Aspose.CAD for Java ile DWG'yi PNG ve diğer raster görüntü formatlarına
  nasıl dönüştüreceğinizi öğrenin. CAD'i yüksek kaliteli sonuçlarla PNG olarak dışa
  aktarın.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: DWG'yi PNG ve Diğer Raster Formatlarına Aspose.CAD for Java ile Dönüştür
url: /tr/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi PNG ve Diğer Raster Formatlarına Aspose.CAD for Java Kullanarak Dönüştürme

## Giriş

## Hızlı Yanıtlar
- **DWG'yi PNG'ye dönüştüren kütüphane nedir?** Aspose.CAD for Java  
- **Hangi formatlar dışa aktarılabilir?** PNG, JPEG, TIFF, PDF, BMP ve daha fazlası  
- **Test için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme çalışır; üretim için lisans gereklidir  
- **Belirli bir yerleşim seçebilir miyim?** Evet, “Model”, “Layout1” vb. hedeflemek için `setLayouts` kullanın.  
- **Yüksek çözünürlüklü çıktı mümkün mü?** Kesinlikle—DPI'yi kontrol etmek için `setPageWidth` ve `setPageHeight` ayarlayın.  

## “convert dwg to png” nedir?

“convert dwg to png” ifadesi, vektör tabanlı bir DWG dosyasını (birçok CAD uygulamasının yerel formatı) piksel tabanlı bir PNG görüntüsüne rasterleştirme sürecini tanımlar. Raster görüntüler, web gösterimi, e-posta paylaşımı ve CAD dışı yazılımlara entegrasyon için idealdir.

## Neden CAD'i PNG (veya diğer raster formatları) olarak dışa aktaralım?

- **Evrensel Uyumluluk:** PNG ve JPEG, neredeyse tüm görüntü görüntüleyicileri ve tarayıcılar tarafından desteklenir.  
- **Hızlı Yükleme:** Raster görüntüler, büyük bir DWG dosyasını açmaya kıyasla anında yüklenir.  
- **Kolay Gömme:** PNG'leri doğrudan Word, PowerPoint veya HTML'e ekleyebilirsiniz; ekstra eklenti gerekmez.  
- **Tutarlı Görünüm:** Çözünürlük, arka plan ve yerleşimi kontrol edersiniz, böylece tüm paydaşlar aynı görseli görür.

## Önkoşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

1. **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm yüklü ve yapılandırılmış.  
2. **Aspose.CAD for Java** – En son JAR dosyasını [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/) adresinden indirin.  

## İsim Uzaylarını İçe Aktarma

İlk olarak, ihtiyaç duyacağınız sınıfları içe aktarın. Bu içe aktarmalar, görüntü yükleme, rasterleştirme seçenekleri ve TIFF/PNG çıktı ayarlarına erişim sağlar.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Pro tip:** PNG yerine TIFF dışa aktarmayı planlıyorsanız, `com.aspose.cad.imageoptions.PngOptions` içinde bulunan `PngOptions` ile `TiffOptions` yerine `PngOptions` kullanın.

## Adım Adım Kılavuz

### Adım 1: Kaynak Dizinini Ayarlama

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

`"Your Document Directory"` ifadesini CAD dosyalarınızın bulunduğu mutlak yol ile değiştirin.

### Adım 2: CAD Dosyasını Yükleme

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Desteklenen herhangi bir formatı (DWG, DXF, DGN vb.) yükleyebilirsiniz. Bu, **cad'i nasıl dönüştüreceğiniz** kısmıdır—dosyayı işaretleyin ve Aspose'un ayrıştırmasını sağlayın.

### Adım 3: Rasterleştirme Seçeneklerini Yapılandırma

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` çıktı çözünürlüğünü kontrol eder (daha büyük değerler = daha yüksek DPI).  
- `setLayouts` belirli yerleşimler için **cad'i rastere dönüştürmenizi** sağlar; tüm çizimi rasterleştirmek için bu ayarı atlayın.

### Adım 4: Görüntü Seçeneklerini Ayarlama

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

PNG tercih ediyorsanız, `TiffOptions` yerine `PngOptions` örneği oluşturun. İşte **cad'i png olarak dışa aktarma** burada gerçekleşir.

### Adım 5: Oluşan Görüntüyü Kaydetme

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Dosya uzantısını `.png` (ve seçenek nesnesini `PngOptions`) olarak değiştirerek **CAD'i JPEG/PNG olarak kaydedebilirsiniz**.

> **Yaygın Hata:** Dosya uzantısı ile seçenek sınıfının eşleşmemesi `UnsupportedFormatException` hatasına yol açar. Her zaman uyumlu tutun.

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **Boş çıktı görüntüsü** | `setLayouts` içinde kullanılan yerleşim adlarının kaynak CAD dosyasındaki adlarla tam olarak eşleştiğini doğrulayın. |
| **Düşük çözünürlüklü PNG** | `setPageWidth` / `setPageHeight` değerlerini artırın veya rasterleştirme seçeneklerinde `setResolution` ayarlayın. |
| **Desteklenmeyen DWG sürümü** | En yeni Aspose.CAD sürümünü kullandığınızdan emin olun; eski sürümler yeni DWG sürümlerini desteklemeyebilir. |
| **Büyük dosyalarda bellek hataları** | Sayfaları tek tek işleyin veya JVM yığın boyutunu (`-Xmx2g`) artırın. |

## Sık Sorulan Sorular

**S: Aspose.CAD farklı CAD dosya formatlarıyla uyumlu mu?**  
C: Evet, DWG, DXF, DGN ve daha birçok formatı destekler.

**S: Çıktı raster görüntüsünün çözünürlüğünü özelleştirebilir miyim?**  
C: Kesinlikle. `CadRasterizationOptions` içinde `setPageWidth`, `setPageHeight` veya `setResolution` ayarlarını değiştirin.

**S: Tek bir çalıştırmada birden fazla CAD yerleşimini nasıl dönüştürebilirim?**  
C: `setLayouts` metoduna tüm yerleşim adlarını içeren bir dizi verin, örneğin `new String[]{"Model","Layout1","Layout2"}`.

**S: TIFF dışındaki çıktı formatları destekleniyor mu?**  
C: Evet—PNG, JPEG, BMP, PDF ve daha fazlası ilgili `*Options` sınıfları aracılığıyla mevcuttur.

**S: Aspose.CAD ile ilgili yardım alabilir ya da deneyimlerimi paylaşabilir miyim?**  
C: Topluluk desteği ve resmi yardım için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

## Sonuç

Bu adımları izleyerek **DWG'yi PNG'ye dönüştürebilir**, **CAD'i PNG olarak dışa aktarabilir**, **CAD'i JPEG olarak kaydedebilir** veya ihtiyacınız olan diğer raster formatlarını üretebilirsiniz. Aspose.CAD for Java ağır işleri halleder, böylece yüksek kaliteli görüntüleri uygulamalarınıza, dokümantasyonlarınıza veya web portallarınıza entegre etmeye odaklanabilirsiniz.

---

**Son Güncelleme:** 2025-12-18  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}