---
date: 2025-12-19
description: Aspose.CAD for Java kullanarak AutoCAD PDF dışa aktarmayı öğrenin. Bu
  adım adım kılavuz, DWG'yi PDF'ye nasıl dönüştüreceğinizi, CAD'i PDF olarak nasıl
  kaydedeceğinizi ve lisanslamayı nasıl yöneteceğinizi gösterir.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: AutoCAD PDF Dışa Aktar - Aspose.CAD for Java ile AutoCAD Görüntülerini PDF'ye
  Dışa Aktarma Öğreticisi
url: /tr/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# AutoCAD PDF'yi Dışa Aktar - Aspose.CAD for Java ile AutoCAD Görüntülerini PDF'ye aktarın

## Giriiş

Java kullanarak **AutoCAD PDF aktarmayı** istiyor musunuz? Daha fazla aramanıza gerek yok yok! Bu öğreticide, Aspose.CAD for Java ile AutoCAD görüntülerini PDF’ye dönüştürmeyi adım adım gösteriyoruz; bu güçlü depolama **DWG'yi PDF'ye dönüştürme** süreci zahmetsiz hâle getirir. Sonunda **CAD’i PDF olarak kaydetme**, özel rasterleştirme ayarları uygulaması ve üretim kullanımı için bir Aspose.CAD lisansı ile çalışma konularını anlayacaksınız.

## Hızlı Yanıtlar
- **Java ile DWG'yi PDF'ye dönüştürebilir miyim?** Evet, Aspose.CAD for Java DWG, DXF ve birçok diğer formatı destekleme.
- **Bir lisansa ihtiyaç var mı?** Sınırsız kullanım için bir **Aspose CAD lisansı** gereklidir; Değerlendirme için geçici bir lisans mevcuttur.
- **Hangi Java sürümü destekleniyor mu?** Java8+ (kütüphane tüm modern JDK'larla uyumludur).
- **PDF sayfa ilişkilerini özelleştirebilir miyim?** Kesinlikle – rasterleştirme seçeneklerinde `pageWidth` ve `pageHeight` ayarlarını ayarlar.
- **3‑B rasterleştirme mümkün mü?** Evet, tam 3‑B render için `TypeOfEntities.Entities3D`yi etkinleştirin.

## **autocad pdf'sini dışa aktarma** nedir?
AutoCAD PDF'yi dışa aktarma, vektör CAD çizimlerini (DWG, DXF, DWF vb.) katmanları, çizgilerini koruyarak ve doğal olarak 3‑B geometrisini de kullanılabilir şekilde taşınabilir bir PDF belgesine dönüştürebilir gelir. Bu, renklerle renkleri paylaşmak, arşivlemek veya CAD yazılımı gerektirmeden yazdırmak faydalıdır.

## **autocad pdf'sini dışa aktarmak** için neden Aspose.CAD for Java kullanmalısınız?
- **Tam format desteği** – DWG, DXF, DWF ve daha fazlası kullanılabilir.
- **Harici ilişkiler yok** – saf Java kütüphanesi, yerel DLL dosyasıdır.
- **Yüksek kaliteli rasterleştirme** – DPI, sayfa boyutu ve yerleşim üzerinde kontrol sağlar.
- **Lisans sunar** – ücretsiz deneme ile kalıcı kalıcı bir **Aspose CAD lisansı**na yükseltilebilir.

## Önkoşullar

Başlamadan önce programın kuruluşunun olduğundan emin olun:

- **Java Geliştirme Ortamı** – JDK8 veya üzeri yüklü.
- **Aspose.CAD for Java Kütüphanesi** – [indirme bağlantısı](https://releases.aspose.com/cad/java/) üzerinden indirin.
- **Belge Dizini** – kaynak CAD dosyalarının ve oluşturulacak PDF'lerin bulunacağı bir dizüstü bilgisayar.

## Ad Alanlarını İçe Aktar

Java projenizde Aspose.CAD ile çalışmak için gerekli sınıfları içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Şimdi kodu adım adım inceleyelim.

## Adım Adım Kılavuz

### Adım 1: Kaynak Dizini Yolunu Ayarlayın

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **İpucu:** `"Your Document Directory"` ifadesini, ön koşullarda oluşturduğunuz klasörün mutlak yolu ile değiştirin.

### Adım 2: CAD Görüntüsünü Yükleyin

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Neden önemli:** CAD dosyasını bir `Image` nesnesine yüklemek, Aspose.CAD’in rasterleştirme motoruna tam erişim sağlar.

### Adım 3: Rasterleştirme Seçeneklerini Ayarlayın

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Çıktı PDF’nin boyutunu değiştirmek için `pageWidth` ve `pageHeight` değerlerini ayarlayın.  
- 3‑B varlıklar için **java convert cad pdf** ihtiyacınız varsa `setTypeOfEntities` satırının yorumunu kaldırın.  
- `setLayouts` çağrısı, render edilecek düzeni (Model, Layout1 vb.) seçer.

### Adım 4: PDF Seçeneklerini Yapılandırın

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Bu, rasterleştirme ayarlarını PDF çıktısına bağlayarak vektör verisinin doğru şekilde dönüştürülmesini sağlar.

### Adım 5: PDF'yi Kaydedin

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Ortaya çıkan dosya `Export3DImagestoPDF_out_.pdf`, orijinal AutoCAD çiziminizin bir **save cad as pdf** temsilidir.

## Yaygın Sorunlar ve Çözümler

| Belirti | Muhtemel Neden | Çözüm |
|-----------|-----|------|
| Boş PDF çıktısı | Rasterleştirme seçenekleri ayarlanmamış veya düzenli eşleşmiyor | `setLayouts`un CAD dosyanızdaki düzeniyle aynı olduğundan emin olun. |
| Düşük verim görüntü | `pageWidth`/`pageHeight` çok küçük | Boyutları artırın veya `rasterizationOptions.setResolution(...)` ile daha yüksek DPI ayarlayın. |
| Lisans istisnası | ürünün lisansı uygulanmamış | Bir **Aspose CAD lisansı** modu veya test için geçici lisans kullanın. |

## Sıkça Sorulan Sorular

### S1: Aspose.CAD for Java ile diğer CAD dosya formatlarını da kullanabilir miyim?
A1: Evet, Aspose.CAD DWG, DWF, DGN ve daha fazlası dahil olmak üzere geniş bir format aralığını sağlar, bu da projelerinizin esnekliğini sağlar.

### S2: Aspose.CAD for Java için geçici bir lisans nasıl alınır?
A2: Değerlendirme amaçlı geçici lisans almak için [burayı](https://purchase.aspose.com/temporary-license/) ziyaret edin.

### S3: Rasterleştirme için herhangi bir düzen seçeneği var mı?
A3: Evet, `setLayouts` yöntemiyle (ör. `"Model"`, `"Layout1"`) hangi görünümün renderını gizliliğini özelleştirebilirsiniz.

### S4: Çıktı PDF dosyalarının bozulmalarını özelleştirebilir miyim?
A4: elbette! Rasterleştirme seçeneklerinde `pageWidth` ve `pageHeight` parametrelerini istediğiniz boyutlara göre ayarlayın.

### S5: Aspose.CAD for Java ile ilgili yardım almak veya sorunları tartışmak için Nereden desteklenirim?
A5: Ayrı destek ve topluluk tartışmaları için [Aspose.CAD forumuna](https://forum.aspose.com/c/cad/19) göz atın.

---

**Son Güncelleme:** 2025-12-19
**Şunlarla Test Edildi:** Java 24.10 için Aspose.CAD
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}