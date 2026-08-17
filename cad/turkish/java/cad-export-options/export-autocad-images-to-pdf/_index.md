---
date: 2026-02-20
description: Aspose.CAD for Java kullanarak AutoCAD PDF dışa aktarmayı öğrenin. Bu
  adım adım kılavuz, **DWG'yi PDF'ye dönüştürmeyi**, **CAD'i PDF olarak kaydetmeyi**
  ve lisanslamayı nasıl yöneteceğinizi gösterir.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: DWG'yi PDF'ye Dönüştür - AutoCAD Görüntülerini Aspose.CAD for Java ile PDF'ye
  Aktar
url: /tr/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# AutoCAD PDF'yi Dışa Aktar - AutoCAD Görüntülerini PDF'ye Aspose.CAD for Java ile Dışa Aktar

## Giriş

Java kullanarak **DWG'yi PDF'ye dönüştürmek** mi istiyorsunuz? Daha fazla aramayın! Bu öğreticide, **DWG'yi PDF'ye dönüştür** sürecini zahmetsiz hale getiren güçlü bir kütüphane olan Aspose.CAD for Java ile AutoCAD görüntülerini PDF'ye dönüştürmeyi adım adım göstereceğiz. Sonunda **CAD'i PDF olarak kaydet**, özel rasterleştirme ayarları uygula ve üretim kullanımı için bir Aspose.CAD lisansı ile çalışmayı anlayacaksınız.

## Hızlı Yanıtlar
- **Java ile DWG'yi PDF'ye dönüştürebilir miyim?** Evet, Aspose.CAD for Java DWG, DXF ve birçok diğer formatı destekler.  
- **Bir lisansa ihtiyacım var mı?** **Aspose CAD lisansı**, sınırsız kullanım için gereklidir; değerlendirme için geçici bir lisans mevcuttur.  
- **Hangi Java sürümü destekleniyor?** Java 8+ (kütüphane tüm modern JDK'larla uyumludur).  
- **PDF sayfa boyutunu özelleştirebilir miyim?** Kesinlikle – rasterleştirme seçeneklerinde `pageWidth` ve `pageHeight` değerlerini ayarlayın.  
- **3‑B rasterleştirme mümkün mü?** Evet, tam 3‑B render için `TypeOfEntities.Entities3D` özelliğini etkinleştirin.

## **export autocad pdf** nedir?
AutoCAD PDF dışa aktarma, vektör tabanlı CAD çizimlerini (DWG, DXF, DWF vb.) katmanları, çizgi kalınlıklarını koruyarak ve isteğe bağlı olarak 3‑B geometriyi dahil ederek taşınabilir bir PDF belgesine dönüştürmek anlamına gelir. Bu, tasarımları müşterilerle paylaşmak, arşivlemek veya CAD yazılımı gerektirmeden yazdırmak için kullanışlıdır.

## Neden Aspose.CAD for Java ile DWG'yi PDF'ye Dönüştürmeliyim?
- **Tam format desteği** – DWG, DXF, DWF ve daha fazlası ile çalışır.  
- **Harici bağımlılık yok** – saf Java kütüphanesi, yerel DLL'ler gerektirmez.  
- **Yüksek kaliteli rasterleştirme** – DPI, sayfa boyutu ve düzen üzerinde kontrol sağlar, böylece **PDF sayfa boyutunu özelleştirebilir** ve proje gereksinimlerinize uyarlayabilirsiniz.  
- **Lisans esnekliği** – ücretsiz deneme ile başlayıp ardından kalıcı bir **Aspose CAD lisansı** alabilirsiniz.  

## Önkoşullar

Başlamadan önce şunların yüklü olduğundan emin olun:

- **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm.  
- **Aspose.CAD for Java Kütüphanesi** – [indirme bağlantısı](https://releases.aspose.com/cad/java/) üzerinden indirin.  
- **Belge Dizini** – kaynak CAD dosyalarının ve oluşturulan PDF'lerin bulunacağı makinenizde bir klasör.

## İsim Uzaylarını İçeri Aktarın

Java projenizde Aspose.CAD ile çalışmak için gerekli sınıfları içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Şimdi kodu adım adım inceleyelim.

## Aspose.CAD for Java ile DWG'yi PDF'ye Nasıl Dönüştürülür

### Adım 1: Kaynak Dizin Yolunu Ayarla

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **İpucu:** `"Your Document Directory"` ifadesini, önkoşullarda oluşturduğunuz klasörün mutlak yolu ile değiştirin.

### Adım 2: CAD Görüntüsünü Yükle

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Neden önemli:** CAD dosyasını bir `Image` nesnesine yüklemek, Aspose.CAD’in rasterleştirme motoruna tam erişim sağlar.

### Adım 3: Rasterleştirme Seçeneklerini Ayarla

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` ve `pageHeight` değerlerini **PDF sayfa boyutunu özelleştirmek** için ayarlayın.  
- 3‑B varlıklar için **java convert cad pdf** ihtiyacınız varsa `setTypeOfEntities` satırının yorumunu kaldırın.  
- `setLayouts` çağrısı, render edilecek düzeni (Model, Layout1 vb.) seçer.

### Adım 4: PDF Seçeneklerini Yapılandır

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Bu, rasterleştirme ayarlarını PDF çıktısına bağlayarak vektör verilerinin doğru şekilde dönüştürülmesini sağlar.

### Adım 5: PDF'yi Kaydet

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Ortaya çıkan dosya, `Export3DImagestoPDF_out_.pdf`, orijinal AutoCAD çiziminizin **save cad as pdf** temsilidır.

## Yaygın Sorunlar ve Çözümler

| Semptom | Muhtemel Neden | Çözüm |
|---------|----------------|-------|
| Boş PDF çıktısı | Rasterleştirme seçenekleri ayarlanmamış veya düzen eşleşmiyor | `setLayouts` değerinin CAD dosyanızdaki düzen adıyla aynı olduğundan emin olun. |
| Düşük çözünürlüklü görüntü | `pageWidth`/`pageHeight` çok küçük | Boyutları artırın veya `rasterizationOptions.setResolution(...)` ile daha yüksek DPI ayarlayın. |
| Lisans istisnası | Geçerli bir lisans uygulanmamış | **Aspose CAD lisansı** uygulayın veya test için geçici bir lisans kullanın. |

## Sık Sorulan Sorular

### S1: Aspose.CAD for Java'yi diğer CAD dosya formatlarıyla kullanabilir miyim?
C1: Evet, Aspose.CAD DWG, DWF, DGN ve daha fazlası dahil olmak üzere geniş bir format yelpazesini destekler, bu da projelerinizde esneklik sağlar.

### S2: Aspose.CAD for Java için geçici bir lisans nasıl alınır?
C2: Değerlendirme amaçlı geçici lisans almak için [burayı](https://purchase.aspose.com/temporary-license/) ziyaret edin.

### S3: Rasterleştirme için herhangi bir düzen seçeneği var mı?
C3: Evet, `setLayouts` yöntemi aracılığıyla (ör. `"Model"`, `"Layout1"`) hangi görünümün render edileceğini kontrol ederek düzenleri özelleştirebilirsiniz.

### S4: Çıktı PDF dosyasının boyutunu özelleştirebilir miyim?
C4: Kesinlikle! İstediğiniz boyutlara uyması için rasterleştirme seçeneklerinde `pageWidth` ve `pageHeight` parametrelerini ayarlayın.

### S5: Aspose.CAD for Java ile ilgili yardım almak veya sorunları tartışmak için nereye başvurabilirim?
C5: Ayrı destek ve topluluk tartışmaları için [Aspose.CAD forumuna](https://forum.aspose.com/c/cad/19) göz atın.

---

**Son Güncelleme:** 2026-02-20  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.10  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}