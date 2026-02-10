---
date: 2026-02-04
description: Aspose.CAD for Java kullanarak dxf'ten pdf oluşturmayı ve dxf'i pdf'ye
  dışa aktarmayı, pdf sayfa genişliğini ayarlamayı ve cad'den kesin kontrolle pdf
  üretmeyi öğrenin.
linktitle: Export Specific DXF Layout to PDF with Java
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java kullanarak dxf Layout'tan PDF oluştur
url: /tr/java/additional-features/export-specific-layout-to-pdf/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java ile dxf Düzeninden PDF Oluşturma

## Introduction

CAD çizimleriyle çalışan bir Java geliştiricisiyseniz, **dxf dosalarını nasıl dışa aktaracağınızı** doğru bir şekilde bilmenin bir projeyi başarabilir ya da başarısız kılabileceğini biliyorsunuz. İster mühendislik raporları oluşturuyor olun, ister tasarımları müşterilerle paylaşıyor olun, ister toplu dönüşümleri otomatikleştiriyor olun, güvenilir bir Java PDF dönüşüm kütüphanesi şarttır. Bu öğreticide **dxf düzeninden pdf oluşturma** sürecini, sayfa boyutlarını kontrol etmeyi ve **Aspose.CAD for Java** ile vektör kalitesini korumayı adım adım göstereceğiz.

## Quick Answers
- **Birincil kütüphane nedir?** Aspose.CAD for Java, CAD için özel bir Java pdf dönüşüm kütüphanesidir.
- **Belirli bir düzen seçebilir miyim?** Evet – belirli bir düzen adını hedeflemek için `CadRasterizationOptions.setLayouts()` kullanın.
- **Sayfa boyutunu nasıl ayarlarım?** Rasterizasyon seçeneklerinde `setPageWidth()` ve `setPageHeight()` metodlarını ayarlayın (ör. 1600 × 1600).
- **Üretim için lisansa ihtiyacım var mı?** Üretim kullanımında ticari bir lisans gereklidir; ücretsiz deneme sürümü mevcuttur.
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri (JDK 1.8+).

## dxf Düzeninden pdf Nasıl Oluşturulur?

Bir DXF dosyasını dışa aktarmak, vektör verilerini başka bir formata—genellikle PDF—dönüştürmek anlamına gelir; bu işlem sırasında katmanlar, çizgi kalınlıkları ve düzen bilgileri korunur. Aspose.CAD bu zorluğu üstlenir, böylece düşük seviyeli dosya ayrıştırmasıyla uğraşmak yerine iş mantığınıza odaklanabilirsiniz.

## Why use Aspose.CAD for Java?

- **Tam özellikli CAD desteği** – DWG, DXF, DWF ve daha fazlasını işler.
- **Harici bağımlılık yok** – Saf Java, yerel DLL'ler yok.
- **Kesin rasterizasyon** – Vektör veya raster çıktı seçin, DPI, sayfa boyutu ve düzeni ayarlayın.
- **Yüksek performans** – Toplu işleme ve sunucu tarafı senaryoları için optimize edilmiştir.
- **dxf'yi pdf'ye dışa aktar** tek bir kod satırıyla, **java convert cad pdf** iş akışları için ideal hâle getirir.

## Prerequisites

Başlamadan önce, aşağıdakilere sahip olduğunuzdan emin olun:

1. **Java Development Kit (JDK)** – Java 8 veya daha yeni bir sürüm. [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html) adresinden indirin.
2. **Aspose.CAD for Java** – En son JAR dosyasını [Aspose.CAD indirme sayfasından](https://releases.aspose.com/cad/java/) alın.
3. Projenizin sınıf yoluna Aspose.CAD JAR'ını eklemek için bir IDE veya yapı aracı (Maven/Gradle).

## Import Namespaces

İlk olarak, ihtiyacınız olan sınıfları içe aktarın. Bu importlar, görüntü yükleme, rasterizasyon seçenekleri ve PDF çıktı ayarlarına erişmenizi sağlar.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Step‑by‑Step Guide

### Step 1: Set the Resource Directory

DXF dosyalarınızı içeren klasörü tanımlayın. Yer tutucuyu, makinenizdeki gerçek yol ile değiştirin.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

> **Pro ipucu:** Ortamlar arasında çalışan bir göreli yol oluşturmak için `System.getProperty("user.dir")` kullanın.

### Step 2: Load the DXF File

`Image.load()` kullanarak kaynak DXF dosyasını yükleyin. Bu yöntem, CAD dosyasını bir Aspose.CAD `Image` nesnesine okur.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile); 
```

### Step 3: Configure Rasterization Options (Set PDF Page Width in Java)

Burada `CadRasterizationOptions` oluşturuyor ve çıktı sayfa boyutunu tanımlıyoruz. İstenen PDF boyutlarına uyması için genişlik/yüksekliği ayarlayın.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);   
rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `setPageWidth` / `setPageHeight` – PDF için **sayfa genişliğini** (ve yüksekliğini) kontrol eder.
- `setLayouts` – hangi düzen(ler)in render edileceğini belirtir; çoğu DXF dosyasında `"Model"` varsayılan model alanıdır.

### Step 4: Create PDF Options (Java Convert CAD PDF)

Rasterizasyon ayarlarını bir `PdfOptions` örneğine bağlayın. Bu, Aspose.CAD'e raster görüntü yerine PDF çıkışı vermesini söyler.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 5: Export DXF to PDF (Create PDF from DXF)

Son olarak, görüntüyü PDF olarak kaydedin. Çıktı dosya adı, düzen‑özgü dönüşümü göstermek için `_layout_out_.pdf` ile biter.

```java
image.save(dataDir + "conic_pyramid_layout_out_.pdf", pdfOptions);
```

Çalıştırdıktan sonra, aynı dizinde `conic_pyramid_layout_out_.pdf` dosyasını bulacaksınız; bu dosya yalnızca belirlediğiniz boyutlarda render edilmiş **Model** düzenini içerir.

## Common Use Cases

| Senaryo | Bu yöntemin faydası |
|----------|-----------------------|
| **Otomatik rapor oluşturma** | Her çizimin aynı sayfa boyutuyla dışa aktarılmasını garanti eder, toplu PDF'leri tutarlı hâle getirir. |
| **Müşteri odaklı tasarım ön izlemeleri** | Tek bir düzeni (ör. “Model” veya “Sheet1”) dışa aktarmak dosya boyutunu azaltır ve vektör doğruluğunu korur. |
| **Eski DWG'den PDF'ye geçiş** | Bu örnek DXF kullansa da aynı API, **convert dwg to pdf** için minimal kod değişikliğiyle çalışır. |
| **CAD çizimlerini web portalına gömme** | Oluşturulan PDF, ek dönüşüm araçları olmadan doğrudan tarayıcılara akıtılabilir. |

## Common Issues and Solutions

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| **Boş PDF** | Düzen adı uyuşmazlığı | DXF'teki tam düzen adını doğrulayın (bir CAD görüntüleyici kullanın). |
| **Yanlış sayfa boyutu** | `setPageWidth/Height` uygulanmadı | `PdfOptions` oluşturulmadan önce rasterizasyon seçeneklerini **ayarlandığınızdan** emin olun. |
| **Büyük dosyalarda bellek yetersizliği** | Büyük DXF'in belleğe yüklenmesi | Akış (streaming) kullanın veya JVM yığınını artırın (`-Xmx2g`). |
| **Eksik yazı tipleri** | Metin öğeleri mevcut olmayan yazı tiplerini kullanıyor | Sunucuda gerekli yazı tiplerini kurun veya `CadRasterizationOptions` aracılığıyla gömün. |
| **Birden fazla düzen dışa aktarmak gerekiyor** | Sadece tek düzen çağrısı | `setLayouts`'i düzen adları dizisiyle çağırın ve her biri için `save` adımını tekrarlayın. |

## Frequently Asked Questions

**S: Aspose.CAD for Java hem yeni başlayanlar hem de deneyimli geliştiriciler için uygun mu?**  
C: Kesinlikle. API, yeni başlayanlar için anlaşılırken, ileri düzey kullanıcılar için derin özelleştirme imkanı sunar.

**S: Farklı düzenler için rasterizasyon seçeneklerini özelleştirebilir miyim?**  
C: Evet. Gerektiği gibi her düzen için `CadRasterizationOptions` (sayfa boyutu, DPI, arka plan rengi) ayarlayabilirsiniz.

**S: Aspose.CAD for Java için kapsamlı belgeleri nerede bulabilirim?**  
C: Ayrıntılı dokümantasyon [burada](https://reference.aspose.com/cad/java/) mevcuttur.

**S: Aspose.CAD for Java için ücretsiz deneme sürümü var mı?**  
C: Evet, deneme sürümünü [buradan](https://releases.aspose.com/) indirebilirsiniz.

**S: Aspose.CAD for Java için destek nasıl alabilirim?**  
C: Topluluk ve personel yardımı için destek forumunu [buradan](https://forum.aspose.com/c/cad/19) ziyaret edin.

## Conclusion

Bu rehberde, Aspose.CAD for Java kullanarak **dxf düzenlerinden pdf oluşturma** sürecini, ortam kurulumundan sayfa boyutlarını ince ayarlamaya kadar tüm adımlarla gösterdik. Bu **java pdf conversion library**'yi kullanarak CAD‑to‑PDF iş akışlarını otomatikleştirebilir, vektör doğruluğunu koruyabilir ve Java uygulamalarınıza sorunsuz PDF üretimini entegre edebilirsiniz. İster **dxf'yi pdf'ye dışa aktarmanız**, ister **dwg'yi pdf'ye dönüştürmeniz** veya **cad'den pdf oluşturmanız** gerekse, yukarıdaki adımlar sağlam bir temel sağlar.

---

**Son Güncelleme:** 2026-02-04  
**Test Edilen:** Aspose.CAD for Java 24.12 (yazım zamanındaki en yeni sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}