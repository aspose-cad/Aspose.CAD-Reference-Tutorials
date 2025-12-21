---
date: 2025-12-21
description: Aspose.CAD for Java kullanarak STL'yi PNG'ye nasıl dışa aktaracağınızı
  öğrenin – Java projelerinizde STL dosyalarını PNG'ye dönüştürmeyi basitleştiren
  adım adım bir rehber.
linktitle: Export STL to PNG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java ile STL'yi PNG'ye Dışa Aktar
url: /tr/java/cad-export-options/export-stl-to-png/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java ile STL'yi PNG'ye Dışa Aktarma

## Giriş

Java ortamında **stl'yi png'ye dışa aktarmanız** gerekiyorsa, Aspose.CAD for Java mükemmel bir araçtır. Bu öğreticide, projeyi kurmaktan yüksek kaliteli bir PNG görüntüsü kaydetmeye kadar ihtiyacınız olan her şeyi adım adım göstereceğiz; böylece 3‑B görsel varlıkları uygulamalarınıza güvenle entegre edebilirsiniz.

## Hızlı Yanıtlar
- **“export stl to png” ne anlama geliyor?** 3‑B STL modelini 2‑B raster PNG görüntüsüne dönüştürür.  
- **Dönüşümü hangi kütüphane gerçekleştiriyor?** Aspose.CAD for Java, STL ve PNG formatları için yerel destek sağlar.  
- **Lisans gerekiyor mu?** Üretim kullanımında geçici veya kalıcı bir Aspose.CAD lisansı gereklidir.  
- **Uygulama ne kadar sürer?** Temel bir dönüşüm betiği için yaklaşık 10‑15 dakika.  
- **Görüntü boyutunu ayarlayabilir miyim?** Evet – rasterleştirme seçenekleri, özel genişlik ve yükseklik ayarlamanıza izin verir.

## export stl to png nedir?

STL'yi PNG'ye dışa aktarmak, bir 3‑B ağ (STL) alıp düz bir görüntü (PNG) olarak render etmektir. Bu, ön izlemeler göstermek, küçük resimler oluşturmak veya modelleri raporlara gömmek istediğinizde, bir 3‑B görüntüleyiciye ihtiyaç duymadan faydalıdır.

## Neden Java'da STL'yi PNG'ye Dönüştürmeliyiz?

- **Çapraz platform uyumluluğu** – PNG, tarayıcılarda, mobil uygulamalarda ve masaüstü GUI'lerde çalışır.  
- **Performans** – Statik bir görüntünün render edilmesi, tam bir 3‑B modelin yüklenmesinden çok daha hızlıdır.  
- **Basitlik** – Aspose.CAD, karmaşık rasterleştirme sürecini soyutlayarak iş mantığına odaklanmanızı sağlar.  

## Önkoşullar

Başlamadan önce, aşağıdakilere sahip olduğunuzdan emin olun:

- Makinenizde Java Development Kit (JDK) yüklü.  
- Aspose.CAD for Java kütüphanesini indirin. Bunu [buradan](https://releases.aspose.com/cad/java/) edinebilirsiniz.  
- Geçerli bir lisans veya [buradan](https://purchase.aspose.com/temporary-license/) geçici bir lisans.

## İsim Uzaylarını İçe Aktarma

Java kaynak dosyanıza gerekli Aspose.CAD sınıflarını ekleyin:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Bu importlar, görüntü yükleme, rasterleştirme ve PNG‑özel seçeneklerine erişmenizi sağlar.

## Adım Adım Kılavuz

### Adım 1: Projenizi Kurun

Seçtiğiniz IDE ile yeni bir Java projesi oluşturun ve Aspose.CAD JAR dosyasını projenin sınıf yoluna ekleyin.

### Adım 2: STL Dosyanızı Belirleyin (stl nasıl yüklenir)

Dönüştürmek istediğiniz STL modelini içeren klasörü tanımlayın:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

> **Pro ipucu:** Yol sorunlarından kaçınmak için STL dosyalarınızı ayrı bir kaynak klasöründe tutun.

### Adım 3: STL Dosyasını Yükleyin (stl'yi png'ye dönüştür)

`Image.load` metodunu kullanarak STL dosyasını bir `CadImage` nesnesine okuyun:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

Bu noktada 3‑B geometri rasterleştirme için hazır.

### Adım 4: Rasterleştirme Seçeneklerini Yapılandırın (3d stl png dönüştürme)

Çıktı boyutlarını ve diğer raster ayarlarını belirleyin. Genişlik/yüksekliği istediğiniz PNG çözünürlüğüne göre ayarlayın:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Burada ayrıca arka plan rengini, çizgi kalınlığını veya anti‑aliasing'i ayarlayabilirsiniz.

### Adım 5: PNG Seçeneklerini Yapılandırın (java stl png dönüştürme)

`PngOptions` örneği oluşturun ve (isteğe bağlı olarak) rasterleştirme seçeneklerini ekleyin:

```java
PngOptions pngOptions = new PngOptions();
// Uncomment the line below if you want to set vector rasterization options
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Satırı yorumlu bırakarak varsayılan raster ayarları kullanılır; bu ayarlar çoğu durum için yeterlidir.

### Adım 6: PNG Olarak Kaydedin

Son olarak, render edilen görüntüyü diske yazın:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

Artık orijinal STL modelinizin PNG temsiline sahipsiniz; bu UI bileşenlerinde, web sayfalarında veya belgelerde kullanılabilir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|-----|
| **Boş PNG çıktısı** | Rasterleştirme seçenekleri ayarlanmamış veya sıfır boyutta | `setPageWidth` ve `setPageHeight` değerlerinin pozitif olduğundan emin olun. |
| **OutOfMemoryError** | Çok büyük STL dosyaları | JVM yığın boyutunu (`-Xmx`) artırın veya görüntü boyutlarını küçültün. |
| **Lisans bulunamadı** | Eksik veya hatalı lisans dosyası | Lisans dosyasını sınıf yoluna yerleştirin ve herhangi bir Aspose çağrısından önce yükleyin. |

## Sonuç

Aspose.CAD for Java kullanarak **stl'yi png'ye dışa aktarmayı** başarıyla öğrendiniz. Bu iş akışı, herhangi bir STL modelinden yüksek kaliteli PNG ön izlemeleri oluşturmanızı sağlar ve Java tabanlı uygulamalardaki görselleştirme görevlerini kolaylaştırır.

## SSS

### Q1: Aspose.CAD for Java tüm STL dosya sürümleriyle uyumlu mu?
A1: Aspose.CAD for Java, çeşitli STL dosya sürümlerini destekler ve çoğu yaygın formatla uyumluluğu sağlar.

### Q2: Aspose.CAD for Java'yi ticari bir projede kullanabilir miyim?
A2: Evet, kullanabilirsiniz. Tek yapmanız gereken [buradan](https://purchase.aspose.com/buy) geçerli bir lisans almaktır.

### Q3: Ücretsiz deneme için geçici bir lisansa ihtiyacım var mı?
A3: Hayır, ücretsiz deneme için geçici bir lisans gerekmez. Deneme sürümüyle hemen başlayabilirsiniz [buradan](https://releases.aspose.com/).

### Q4: Ek destek nereden bulabilirim veya sorular sorabilirim?
A4: Herhangi bir destek veya soru için Aspose.CAD forumunu [buradan](https://forum.aspose.com/c/cad/19) ziyaret edin.

### Q5: Kapsamlı bir dokümantasyon mevcut mu?
A5: Evet, dokümantasyonu [buradan](https://reference.aspose.com/cad/java/) bulabilirsiniz.

## Sık Sorulan Sorular

**S: Dışa aktarılan PNG'nin arka plan rengini nasıl kontrol ederim?**  
C: `pngOptions`'a atamadan önce `vectorOptions.setBackgroundColor(Color.getWhite())` kullanın.

**S: Bir toplu işlemde birden fazla STL dosyasını dışa aktarabilir miyim?**  
C: Kesinlikle – dönüşüm mantığını dosya yolu listesini dönen bir döngü içinde yerleştirin.

**S: PNG şeffaflığı korur mu?**  
C: Evet, PNG alfa kanalını destekler; gerekirse `pngOptions.setTransparent(true)` ile etkinleştirebilirsiniz.

**S: Diğer raster formatlara (ör. JPEG, BMP) dışa aktarmak mümkün mü?**  
C: Aspose.CAD birçok raster formatı destekler; `PngOptions` yerine `JpegOptions`, `BmpOptions` vb. kullanmanız yeterlidir.

**S: STL desteği için hangi Aspose.CAD sürümü gerekir?**  
C: STL desteği Aspose.CAD 20.x sürümünden beri mevcuttur; en son sürümü kullanmak tam uyumluluk sağlar.

---

**Son Güncelleme:** 2025-12-21  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}