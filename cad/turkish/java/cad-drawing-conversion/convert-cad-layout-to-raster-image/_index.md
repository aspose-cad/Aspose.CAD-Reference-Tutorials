---
date: 2026-02-17
description: Aspose.CAD for Java kullanarak dwg'yi png'ye dönüştürmeyi ve cad'i png
  ya da diğer raster formatlarda dışa aktarmayı öğrenin. Yüksek kaliteli sonuçları
  hızlıca elde edin.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: DWG'yi PNG ve Diğer Raster Formatlarına Aspose.CAD for Java ile Dönüştür
url: /tr/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

 translate "Last Updated", "Tested With", "Author". Keep dates same.

Let's produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java ile DWG'yi PNG ve Diğer Raster Formatlarına Dönüştürme

## Giriş

DWG'yi PNG'ye (veya diğer raster görüntü formatlarına) dönüştürmek, CAD çizimlerini CAD görüntüleyicisi olmayan ekip arkadaşlarıyla paylaşmanız, tasarımları belgelerde gömmeniz veya web galerileri için küçük resimler oluşturmanız gerektiğinde yaygın bir gereksinimdir. **Bu rehberde DWG'yi PNG'ye hızlı ve güvenilir bir şekilde nasıl dönüştüreceğinizi öğreneceksiniz**, ister tam bir çizim dosyasıyla ister sadece belirli bir yerleşimle çalışıyor olun. Ayrıca **CAD'i rastera dönüştürmeniz** web ön izlemeleri, raporlama araçları veya mobil uygulamalar için gerekebilir. Aspose.CAD for Java bu dönüşümü basitleştirir ve çözünürlük, yerleşim seçimi ve çıktı formatı üzerinde tam kontrol sağlar.

## Hızlı Yanıtlar
- **DWG'yi PNG'ye hangi kütüphane işliyor?** Aspose.CAD for Java  
- **Hangi formatlar dışa aktarılabilir?** PNG, JPEG, TIFF, PDF, BMP ve daha fazlası  
- **Test için lisansa ihtiyacım var mı?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için lisans gereklidir  
- **Belirli bir yerleşim seçebilir miyim?** Evet, `setLayouts` kullanarak “Model”, “Layout1” vb. hedefleyebilirsiniz  
- **Yüksek çözünürlüklü çıktı mümkün mü?** Kesinlikle—DPI kontrolü için `setPageWidth` ve `setPageHeight` ayarlayın  

## “convert dwg to png” nedir?

“convert dwg to png” ifadesi, vektör tabanlı bir DWG dosyasını (birçok CAD uygulamasının yerel formatı) piksel tabanlı bir PNG görüntüsüne rasterleştirme sürecini tanımlar. Raster görüntüler, web gösterimi, e‑posta paylaşımı ve CAD dışı yazılımlara entegrasyon için idealdir.

## CAD'i PNG (veya diğer raster formatları) olarak dışa aktarmak neden?

- **Evrensel Uyumluluk:** PNG ve JPEG neredeyse tüm görüntü görüntüleyicileri ve tarayıcılar tarafından desteklenir.  
- **Hızlı Yükleme:** Raster görüntüler, ağır bir DWG dosyasını açmaya kıyasla anında yüklenir.  
- **Kolay Gömme:** PNG'leri doğrudan Word, PowerPoint veya HTML'e ekstra eklenti gerektirmeden ekleyebilirsiniz.  
- **Tutarlı Görünüm:** Çözünürlük, arka plan ve yerleşimi kontrol ederek her paydaşa aynı görseli sunarsınız.  

## Yaygın Kullanım Senaryoları

| Senaryo | Raster çıktının faydası |
|----------|------------------------|
| **Proje dokümantasyonu** | PNG'leri PDF veya Word belgelerine gömmek, inceleyenlerin CAD yazılımına ihtiyaç duymamasını sağlar. |
| **Web portalları** | DWG dosyalarından oluşturulan küçük resimler anında yüklenir ve kullanıcı deneyimini artırır. |
| **Mobil uygulamalar** | Raster görüntüler, CAD görüntüleyicisi olmayan cihazlarda doğru şekilde gösterilir. |
| **Otomatik raporlama** | Birden fazla yerleşimi toplu olarak PNG/JPEG'e dönüştürüp grafikler veya panolar içinde kullanabilirsiniz. |

## Ön Koşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

1. **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm yüklü ve yapılandırılmış.  
2. **Aspose.CAD for Java** – En son JAR dosyasını [Aspose.CAD for Java belgeleri](https://reference.aspose.com/cad/java/) üzerinden indirin.  

## İsim Uzaylarını İçe Aktarma

İhtiyacınız olan sınıfları ilk olarak içe aktarın. Bu import'lar, görüntü yükleme, rasterleştirme seçenekleri ve TIFF/PNG çıktı ayarlarına erişim sağlar.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **İpucu:** **CAD'i PNG olarak dışa aktarmak** istiyorsanız, `TiffOptions` yerine `com.aspose.cad.imageoptions.PngOptions` içinde bulunan `PngOptions` kullanın.

## Adım‑Adım Kılavuz

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

- `setPageWidth` / `setPageHeight` çıktı çözünürlüğünü kontrol eder (daha büyük değer = daha yüksek DPI).  
- `setLayouts` belirli yerleşimler için **CAD'i rastera dönüştürmenizi** sağlar; tüm çizimi rasterleştirmek için bu satırı atlayın.

### Adım 4: Görüntü Seçeneklerini Ayarlama

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

PNG tercih ediyorsanız, `TiffOptions` yerine `PngOptions` örneği oluşturun. Burada **CAD'i PNG olarak dışa aktarıyorsunuz**.

### Adım 5: Sonuç Görüntüyü Kaydetme

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Dosya uzantısını `.png` (ve seçenek nesnesini `PngOptions`) olarak değiştirerek **CAD'i JPEG/PNG olarak kaydedin**.

> **Yaygın Hata:** Dosya uzantısı ile seçenek sınıfının eşleşmemesi `UnsupportedFormatException` hatasına yol açar. Her zaman uyumlu tutun.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Çözüm |
|-------|----------|
| **Boş çıktı görüntüsü** | `setLayouts` içindeki yerleşim adlarının kaynak CAD dosyasındaki adlarla tam olarak eşleştiğini doğrulayın. |
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

**S: TIFF dışındaki çıktı formatları var mı?**  
C: Evet—PNG, JPEG, BMP, PDF ve daha fazlası ilgili `*Options` sınıflarıyla mevcuttur.

**S: Aspose.CAD ile ilgili yardım alabileceğim veya deneyimlerimi paylaşabileceğim yer neresi?**  
C: Topluluk desteği ve resmi yardım için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

## Sonuç

Bu adımları izleyerek **DWG'yi PNG'ye dönüştürebilir**, **CAD'i PNG olarak dışa aktarabilir**, **CAD'i JPEG olarak kaydedebilir** veya ihtiyacınız olan diğer raster formatlarını üretebilirsiniz. Aspose.CAD for Java ağır işleri üstlenir, böylece yüksek kaliteli görüntüleri uygulamalarınıza, belgelerinize veya web portallarınıza entegre etmeye odaklanabilirsiniz.

---

**Son Güncelleme:** 2026-02-17  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}