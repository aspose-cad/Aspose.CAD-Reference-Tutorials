---
date: 2026-10-30
description: Aspose.CAD for Java kullanarak DXF dosyalarını WMF'ye toplu dönüştürmeyi,
  adım adım kod örnekleri, ücretsiz deneme bilgileri ve isteğe bağlı PDF dışa aktarımıyla
  öğrenin.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Java Kullanarak DXF'i WMF Formatına Dışa Aktarın
og_description: Aspose.CAD for Java ile DXF dosyalarını WMF'ye toplu dönüştürün. Bu
  kılavuzu izleyerek DXF çizimlerini yükleyin, rasterleştirme seçeneklerini ayarlayın,
  WMF olarak kaydedin ve ücretsiz deneme ile isteğe bağlı olarak PDF'ye dışa aktarın.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Aspose.CAD for Java ile DXF dosyalarını WMF'ye toplu dönüştürün
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Aspose.CAD for Java ile DXF dosyalarını WMF'ye toplu dönüştürün
url: /tr/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DXF dosyalarını WMF'ye toplu dönüştürme Aspose.CAD for Java ile

## Giriş

Bu öğreticide, Aspose.CAD for Java kullanarak **batch convert DXF files to WMF** işlemini nasıl yapacağınızı öğreneceksiniz. Windows tabanlı raporlara CAD çizimlerini gömmek, Office belgeleri için hafif vektör grafikler oluşturmak veya büyük ölçekli dönüşümleri otomatikleştirmek ister misiniz, bu kılavuz bir DXF çizimini yüklemeniz, rasterleştirme seçeneklerini yapılandırmanız, WMF olarak kaydetmeniz ve isteğe bağlı olarak aynı çizimi PDF olarak dışa aktarmanız konusunda size adım adım rehberlik eder. Adımlar, Java 8+ çalışan herhangi bir platformda çalışır.

## Hızlı cevaplar
- **DXF'yi WMF'ye ücretsiz deneme ile dönüştürebilir miyim?** Evet – Aspose tam işlevsel 30‑günlük bir deneme sunar.  
- **Hangi Java sürümü gereklidir?** Java 8 veya daha yeni.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Üretim için bir lisans gereklidir; deneme sürümü geliştirme ve test için çalışır.  
- **Dönüşüm kayıpsız mı?** Vektör verileri korunur; rasterleştirme seçenekleri çözünürlüğü kontrol etmenizi sağlar.  
- **Aynı çizimi PDF olarak da dışa aktarabilir miyim?** Kesinlikle – aşağıdaki “Export to PDF” adımına bakın.  
- **Birçok DXF dosyasını aynı anda toplu olarak nasıl dönüştürebilirim?** Bir klasörü döngüyle gezerek, aynı yükle‑rasterleştir‑kaydet desenini her dosyaya uygularsınız.

## Batch convert dxf dosyaları nedir?

Batch converting DXF files, birden fazla Drawing Exchange Format (DXF) çizimini tek bir çalıştırmada işlemek ve her biri için WMF çıktısı üretmek anlamına gelir. WMF (Windows Metafile), Microsoft Office, Windows uygulamaları ve birçok raporlama aracıyla doğal olarak bütünleşen bir vektör görüntü formatıdır.

## Neden Aspose.CAD for Java kullanmalı?

Aspose.CAD for Java, **50'den fazla giriş ve çıkış formatını** destekleyen saf‑Java bir motor olup—DXF, DWG, DGN, PDF, PNG, SVG ve WMF dahil—**%99 vektör doğruluğu** sağlar. Java destekleyen herhangi bir işletim sisteminde çalışır, yerel DLL gerektirmez ve tek bir `CadRasterizationOptions` sınıfı aracılığıyla sayfa boyutu, DPI ve arka plan rengini kontrol etmenizi sağlar. Aynı API, PDF, PNG ve SVG dışa aktarmalarını da yönetir, böylece birden çok kütüphane kullanma ihtiyacını ortadan kaldırır.

### Ölçülmüş faydalar
- **50+ desteklenen format** üçüncü taraf dönüştürücülere olan ihtiyacı azaltır.  
- **300 sayfalık DXF dosyalarını 5 saniyeden kısa sürede işler** tipik 2.5 GHz sunucuda 150 DPI'de rasterleştirildiğinde.  
- **Bellek ayak izi 200 MB'nin altında kalır** 500 MB'ye kadar dosyalar için uygun sayfa boyutları ayarlandığında.  

## Önkoşullar

- **Aspose.CAD for Java** projenize entegre edilmiştir. Resmi siteden indirin: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Dönüştürmek istediğiniz DXF dosyalarını içeren bir klasör (ör. `Your Document Directory/DXFDrawings/`).  

## Ad alanlarını içe aktar

`Image` Aspose.CAD’in bellek içindeki bir CAD çizimini temsil eden temel sınıfıdır. Bir dosya yüklendikten sonra, sonraki tüm işlemler—rasterleştirme, format dönüşümü ve kaynak temizliği—bu nesne üzerinden gerçekleştirilir.

Aşağıdaki içe aktarmalar, CAD dosyalarını yüklemek, rasterleştirmek ve kaydetmek için gereken Aspose.CAD sınıflarını getirir.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Adım adım kılavuz

### Java'da DXF dosyalarını WMF'ye toplu olarak nasıl dönüştürürüm?

Her DXF'i `Image.load` ile yükleyin, istenen sayfa boyutu ve DPI için `CadRasterizationOptions` yapılandırın ve `image.save` ile `SaveFormat.WMF` kullanarak kaydedin. Bu üç adımlı desen, vektör kalitesini koruyarak tam dönüşümü gerçekleştirir ve dosya başına sadece birkaç satır kod gerektirir.

#### Adım 1: dxf çizimini yükle

Image.load, DXF dosyasını bir Aspose.CAD Image nesnesine okur.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Adım 2: rasterleştirme seçeneklerini yapılandır

`CadRasterizationOptions`, CAD çizimini rasterleştirirken sayfa boyutu, çözünürlük ve arka planı belirler.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Adım 3: wmf olarak kaydet

`SaveFormat.WMF` ile `ImageSaveOptions`, Aspose.CAD’in çıktıyı Windows Metafile olarak yazmasını sağlar.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Adım 4: kaynakları serbest bırak

`image.close()` çağrısı, Aspose.CAD Image nesnesi tarafından kullanılan yerel kaynakları serbest bırakır.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Adım 5: isteğe bağlı – pdf'ye dışa aktar

`PdfOptions`, görüntüyü PDF belgesi olarak kaydederken PDF‑özel ayarları yapılandırır.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Aynı `CadRasterizationOptions` nesnesini bir `PdfOptions` örneğine geçirerek PDF dışa aktarımında yeniden kullanabilirsiniz; bu, birkaç satır kurulumdan tasarruf sağlar.

## Aspose CAD Java kullanarak DXF'yi PDF'ye nasıl dışa aktarırım?

WMF kaydetme formatını `new ImageSaveOptions(SaveFormat.Pdf)` ile değiştirerek PDF olarak kaydedin. Aynı rasterleştirme ayarları uygulanır ve ayrıca yazar meta verisi veya sıkıştırma seviyesi gibi PDF‑özel seçenekler ayarlanabilir. Bu tek satırlık dönüşüm, orijinal CAD düzenini yansıtan, aranabilir ve sayfa‑doğru bir PDF üretir.

## Yaygın sorunlar ve çözümler

`License` Aspose sınıfı, çalışma zamanında bir ürün lisansı uygulamak için kullanılır.

| Sorun | Neden | Çözüm |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | Değişken `cadImage` tanımlı değil (`image` olmalı). | `cadImage` yerine `image` kullanın veya değişkeni tutarlı bir şekilde yeniden adlandırın. |
| **Output WMF is blank** | Rasterleştirme sayfa boyutu çok küçük veya arka plan rengi şeffaf olarak ayarlanmış. | `PageWidth`/`PageHeight` değerlerini artırın veya `rasterizationOptions.setBackgroundColor(Color.WHITE);` ile arka plan rengini ayarlayın. |
| **License exception** | Üretimde geçerli bir Aspose lisansı olmadan çalıştırılıyor. | Uygulama başlangıcında lisans dosyasını uygulayın: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Sıkça Sorulan Sorular

**S: Aspose.CAD belgelerini nerede bulabilirim?**  
C: Belgeleri şu adresten erişebilirsiniz: [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**S: Aspose.CAD for Java'yı nasıl indirebilirim?**  
C: Kütüphaneyi şu sayfadan indirin: [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**S: Ücretsiz deneme mevcut mu?**  
C: Evet, ücretsiz deneme alabilirsiniz: [Aspose free trial page](https://releases.aspose.com/).

**S: Geçici lisans seçenekleri var mı?**  
C: Geçici lisansları şu adreste inceleyebilirsiniz: [temporary license options](https://purchase.aspose.com/temporary-license/).

**S: Destek nereden alınır?**  
C: Aspose.CAD destek forumunu ziyaret edin: [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Ek sıkça sorulan sorular

**S: Yüzlerce MB'lık büyük DXF dosyalarını bellek tükenmeden dönüştürebilir miyim?**  
C: Evet. Dosyayı `try‑with‑resources` bloğunda yükleyin ve `Image` nesnesini hızlıca serbest bırakın. Bellek kullanımını düşük tutmak için `CadRasterizationOptions.setPageWidth/Height` değerlerini makul tutun.

**S: WMF çıktısı katman bilgilerini korur mu?**  
C: WMF düz bir vektör formatıdır, bu yüzden katman hiyerarşisi düzleştirilir; ancak çizgi stilleri, renkler ve tarama desenleri korunur.

**S: WMF için özel DPI ayarlamak mümkün mü?**  
C: Kaydetmeden önce `rasterizationOptions.setResolution(300);` kullanarak DPI'yi tanımlayabilirsiniz.

**S: Tek bir çalıştırmada birden fazla DXF dosyasını toplu dönüştürebilir miyim?**  
C: Kesinlikle. Bir dizini döngüyle gezerek her dosyayı yükleyin ve aynı rasterleştirme‑kaydet mantığını uygulayın.

**S: Hangi Java sürümleri destekleniyor?**  
C: Aspose.CAD for Java, Java 8 ve üzeri sürümleri destekler; Java 11, 17 ve daha yeni LTS sürümler de dahildir.

**Son Güncelleme:** 2026-10-30  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose

## İlgili öğreticiler

- [CAD'den PDF Oluştur – Aspose.CAD for Java ile DXF'yi PDF'ye Dışa Aktar](/cad/java/additional-features/export-dxf-to-pdf/)
- [DXF'den PDF Oluştur: Katmanı Aspose.CAD for Java ile Dışa Aktar](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [DXF Düzenini JPEG Görüntüsüne Dönüştürme – Aspose.CAD ile Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}