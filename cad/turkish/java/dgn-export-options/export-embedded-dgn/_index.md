---
date: 2026-01-07
description: Aspose.CAD for Java kullanarak CAD'i PDF'ye nasıl dışa aktaracağınızı
  ve DGN'yi PDF'ye nasıl dönüştüreceğinizi öğrenin. Java geliştiricileri için adım
  adım rehber.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: CAD'yi PDF'ye Dışa Aktar – Aspose.CAD for Java ile Gömülü DGN'yi Dışa Aktar
url: /tr/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD'yi PDF'ye Dışa Aktarma – Aspose.CAD for Java ile Gömülü DGN'yi Dışa Aktarma

## Giriş

Bu öğreticide **CAD'yi PDF'ye nasıl dışa aktaracağınızı** keşfedecek ve gömülü bir DGN dosyasını yüksek kalitede bir PDF belgesine dönüştüreceksiniz. Aspose.CAD, Java geliştiricilerine CAD dosyası manipülasyonu üzerinde tam kontrol sağlayan güçlü bir kütüphanedir; ister **DGN'yi PDF'ye dönüştürme**, ister **DWG'yi PDF'ye dönüştürme**, ya da CAD çizimlerini diğer formatlarda render etme ihtiyacınız olsun. Aşağıdaki adım‑adım kılavuzu izleyin, dakikalar içinde bu yeteneği uygulamalarınıza entegre edebileceksiniz.

## Hızlı Yanıtlar
- **“CAD'yi PDF'ye dışa aktarma” ne demektir?** CAD çizimlerini (DWG, DGN vb.) vektör kalitesini koruyarak PDF dosyalarına dönüştürür.  
- **Hangi kütüphane kullanılıyor?** Aspose.CAD for Java.  
- **Lisans gerekli mi?** Üretim ortamları için lisans gerekir; ücretsiz deneme sürümü mevcuttur.  
- **Ana önkoşullar nelerdir?** Java geliştirme ortamı ve Aspose.CAD for Java JAR dosyası.  
- **Çıktıyı özelleştirebilir miyim?** Evet – düzenleri seçebilir, rasterizasyon seçeneklerini ayarlayabilir ve PDF ayarlarını kontrol edebilirsiniz.

## “CAD'yi PDF'ye dışa aktarma” nedir?
CAD'yi PDF'ye dışa aktarmak, yerel bir CAD dosyasını (DWG veya DGN gibi) orijinal geometriyi eksiksiz yansıtan bir PDF belgesine dönüştürmek anlamına gelir. PDF, herhangi bir platformda CAD yazılımına ihtiyaç duymadan görüntülenebilir; bu da paylaşım, baskı veya arşivleme için idealdir.

## Aspose.CAD for Java ile DGN'yi PDF'ye dönüştürmek neden tercih edilmeli?
- **Harici bağımlılık yok** – tamamen Java içinde çalışır.  
- **Vektör verisini korur** – PDF'ler herhangi bir yakınlaştırmada net kalır.  
- **İnce ayar kontrolü** – belirli düzenleri seçebilir, rasterizasyon DPI'sını ayarlayabilir ve yazı tiplerini gömebilirsiniz.  
- **Kurumsal düzeyde** – büyük dosyaları, toplu işleme ve lisans seçeneklerini destekler.

## Önkoşullar

Başlamadan önce aşağıdakilerin kurulu olduğundan emin olun:

- **Java Geliştirme Ortamı** – JDK 8 veya üzeri yüklü ve yapılandırılmış.  
- **Aspose.CAD for Java** – En son JAR dosyasını [buradan](https://releases.aspose.com/cad/java/) indirin.  

## Paketleri İçe Aktarma

Projeye başlamak için gerekli sınıfları içe aktarmanız gerekir. Aşağıdaki import satırlarını kaynak dosyanıza ekleyin:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Aspose.CAD for Java ile DGN'yi PDF'ye nasıl dışa aktarılır?

Aşağıda, gömülü bir DGN dosyasını (DWG içinde saklanan) PDF'ye dönüştürmek için adım adım bir rehber bulacaksınız.

### Adım 1: Giriş ve Çıkış Yollarını Ayarlama

Kaynak dosyanızın bulunduğu dizini tanımlayın ve gömülü DGN'yi içeren DWG dosyasını belirtin.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Adım 2: DWG Dosyasını Yükleme

DWG dosyasını bir `Image` nesnesine yükleyin. Aspose.CAD, gömülü DGN verisini otomatik olarak algılar.

```java
Image objImage = Image.load(fileName);
```

### Adım 3: Rasterizasyon Seçeneklerini Yapılandırma

PDF'ye dahil etmek istediğiniz düzen(ler)i seçin. Bu örnekte yalnızca **Model** düzenini dışa aktarıyoruz.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Adım 4: PDF Seçeneklerini Yapılandırma

Rasterizasyon ayarlarını PDF dışa aktarma seçeneklerine ekleyin.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Adım 5: PDF Dosyasını Kaydetme

Son olarak, yapılandırılmış seçenekleri kullanarak PDF'yi diske yazın.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## DWG'yi PDF'ye Dönüştürme – Ek İpucu

Kaynak dosyanız gömülü bir DGN içermeyen düz bir DWG ise, aynı kodu yeniden kullanabilirsiniz – sadece `fileName` değişkenini dönüştürmek istediğiniz DWG'ye yönlendirin. Rasterizasyon ve PDF seçenekleri aynı kalır, böylece tutarlı bir **DWG'yi PDF'ye dönüştürme** iş akışı elde edersiniz.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Sebep | Çözüm |
|-------|--------|----------|
| **Boş PDF çıktısı** | Düzen adı uyuşmazlığı | `setLayouts` metoduna verilen düzen adının kaynak dosyadaki adla (büyük‑küçük harf duyarlı) tam olarak eşleştiğini doğrulayın. |
| **Lisans istisnası** | Lisans olmadan deneme sürümü kullanılıyor | Görüntüyü yüklemeden önce geçerli bir Aspose.CAD lisansı uygulayın (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Dosya bulunamadı** | `dataDir` yolu hatalı | Mutlak bir yol kullanın veya göreceli yolun proje çalışma dizinine göre doğru olduğundan emin olun. |
| **Düşük çözünürlüklü grafikler** | Varsayılan rasterizasyon DPI'sı düşük | DPI'ı artırmak için `rasterizationOptions.setPageWidth/Height` veya `setResolution` metodlarını kullanın. |

## Sık Sorulan Sorular

**S: Aspose.CAD for Java'yı ticari bir projede kullanabilir miyim?**  
C: Evet, Aspose.CAD for Java ticari bir kütüphanedir. Lisansı [buradan](https://purchase.aspose.com/buy) temin edebilirsiniz.

**S: Ücretsiz deneme sürümü mevcut mu?**  
C: Evet, Aspose.CAD for Java için ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

**S: Aspose.CAD for Java için destek nasıl alınır?**  
C: Aspose.CAD topluluğu üzerinden [forumda](https://forum.aspose.com/c/cad/19) destek alabilirsiniz.

**S: Geçici bir lisansa ihtiyacım olursa?**  
C: Geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

**S: Dokümantasyonu nereden bulabilirim?**  
C: Dokümantasyon [burada](https://reference.aspose.com/cad/java/) mevcuttur.

## Sonuç

Artık **CAD'yi PDF'ye dışa aktarmayı**, özellikle **DGN'yi PDF'ye dönüştürmeyi** ve **DWG'yi PDF'ye dönüştürmeyi** Aspose.CAD for Java kullanarak nasıl yapacağınızı öğrendiniz. Yukarıdaki adımları izleyerek, ek CAD yazılımına ihtiyaç duymadan yüksek kaliteli PDF'leri kullanıcılarınıza sunabilecek bir CAD‑to‑PDF dönüşümünü herhangi bir Java tabanlı çözüme entegre edebilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-01-07  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose