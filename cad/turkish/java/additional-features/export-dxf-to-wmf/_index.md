---
date: 2026-06-09
description: Aspose.CAD for Java ile DXF'yi WMF'ye nasıl dönüştüreceğinizi öğrenin,
  ücretsiz deneme, Java 8+ desteği ve isteğe bağlı PDF dışa aktarma dahil. Adım adım
  kod örnekli rehber.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: DXF'yi WMF Formatına Java ile Dışa Aktar
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: DXF'yi WMF'ye Aspose.CAD ile Java'da Dönüştür
url: /tr/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD ile Java’da DXF’yi WMF’ye Dönüştürme

## Giriş

Bu öğreticide, Aspose.CAD for Java ile **DXF'yi WMF'ye dönüştürmeyi** keşfedeceksiniz. CAD çizimlerini Windows tabanlı bir rapora yerleştirmeniz, Office belgeleri için hafif vektör grafikler oluşturmanız veya toplu dönüşümleri otomatikleştirmeniz gerekse, DXF'yi WMF'ye dönüştürmek mühendislik ve raporlama süreçlerinde sıkça ihtiyaç duyulan bir işlemdir. DXF çizimini yükleme, rasterleştirme seçeneklerini yapılandırma, sonucu WMF olarak kaydetme ve isteğe bağlı olarak aynı çizimi PDF olarak dışa aktarma adımlarını birlikte inceleyeceğiz.

## Hızlı Yanıtlar
- **DXF'yi WMF'ye ücretsiz deneme ile dönüştürebilir miyim?** Evet – Aspose tam işlevsel 30 günlük bir deneme sunar.  
- **Hangi Java sürümü gereklidir?** Java 8 veya daha yenisi.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Üretim için lisans gereklidir; deneme sürümü geliştirme ve test için çalışır.  
- **Dönüşüm kayıpsız mı?** Vektör verileri korunur; rasterleştirme seçenekleri çözünürlüğü kontrol etmenizi sağlar.  
- **Aynı çizimi PDF olarak da dışa aktarabilir miyim?** Kesinlikle – aşağıdaki “PDF’ye Dışa Aktar” adımına bakın.

## “DXF'yi WMF'ye dönüştürme” nedir?

DXF'yi WMF'ye dönüştürmek, yaygın olarak kullanılan bir CAD formatı olan Drawing Exchange Format (DXF) dosyasını alıp Windows Metafile (WMF) formatına çevirmek anlamına gelir. WMF, Microsoft Office, Windows uygulamaları ve birçok raporlama aracıyla sorunsuz bir şekilde bütünleşen bir vektör görüntü formatıdır.

## Neden Aspose.CAD for Java Kullanılmalı?

Aspose.CAD for Java, yerel DLL gerektirmeyen saf Java motoru sunar ve CAD dosyalarını **%99'dan fazla vektör doğruluğu** ile dönüştürür; katmanlar, renkler, çizgi stilleri ve tarama desenleri korunur. **50+ giriş ve çıkış formatını** destekler — DXF, DWG, DGN, PDF, PNG, SVG ve WMF dahil — ve yerleşik rasterleştirme seçenekleriyle sayfa boyutu, DPI ve arka plan rengini ince ayar yapmanıza olanak tanır. Aynı API, PDF, PNG ve SVG dışa aktarmalarını da yönetir, böylece birden fazla kütüphane kullanmanıza gerek kalmaz.

### Temel avantajlar
- **Harici bağımlılık yok** – saf Java, Java çalıştıran herhangi bir işletim sisteminde çalışır.  
- **Yüksek doğruluklu render** – çizgi kalınlığı, renk ve tarama detaylarını korur.  
- **Yerleşik rasterleştirme** – sayfa boyutları, çözünürlük ve arka planı kontrol eder.  
- **Tek durak dönüşüm** – aynı sınıflar WMF, PDF, PNG, SVG vb. formatlara dışa aktarır.

## Önkoşullar

Başlamadan önce, aşağıdakilere sahip olduğunuzdan emin olun:

- **Aspose.CAD for Java** projenize entegre edilmiş. Resmi siteden indirin: [Aspose.CAD Java indirme](https://releases.aspose.com/cad/java/).  
- **Belge dizini** DXF dosyalarınızın saklandığı yer (örnek: `Your Document Directory/DXFDrawings/`).  

## Ad Alanlarını İçe Aktarma

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

## Adım‑Adım Kılavuz

### Java’da DXF'yi WMF’ye nasıl dönüştürürüm?

DXF dosyanızı `Image.load("yourFile.dxf")` ile yükleyin, istenen sayfa boyutu ve DPI için `CadRasterizationOptions` yapılandırın, ardından `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))` çağrısını yapın. Bu üç adımlı desen, vektör kalitesini koruyarak tam dönüşümü gerçekleştirir ve sadece birkaç satır kod gerektirir.

#### Adım 1: DXF Çizimini Yükle

Image.load, DXF dosyasını bir Aspose.CAD Image nesnesine okur.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Adım 2: Rasterleştirme Seçeneklerini Yapılandır

CadRasterizationOptions, CAD çizimini rasterleştirirken sayfa boyutu, çözünürlük ve arka planı belirler.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Adım 3: WMF Olarak Kaydet

SaveFormat.WMF ile kullanılan ImageSaveOptions, Aspose.CAD'e çıktıyı bir Windows Metafile olarak yazmasını söyler.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Adım 4: Kaynakları Serbest Bırak

`image.close()` çağrısı, Aspose.CAD Image nesnesi tarafından kullanılan yerel kaynakları serbest bırakır.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Adım 5: İsteğe Bağlı – PDF’ye Dışa Aktar

PdfOptions, görüntüyü PDF belgesi olarak kaydederken PDF’ye özgü ayarları yapılandırır.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Aynı `CadRasterizationOptions` nesnesini bir `PdfOptions` örneğine geçirerek PDF dışa aktarımında yeniden kullanabilirsiniz; bu, birkaç satır ayarı size kazandırır.

## Aspose CAD Java ile DXF'yi PDF’ye nasıl dışa aktarırım?

PDF’ye dışa aktarma, aynı yükleme ve rasterleştirme adımlarını izler; sadece WMF kaydetme formatını PDF ile değiştirin. `new ImageSaveOptions(SaveFormat.Pdf)` kullanın ve isteğe bağlı olarak sıkıştırma seviyesi veya yazar meta verileri gibi PDF’ye özgü ayarları belirleyin. Bu tek satırlık dönüşüm, orijinal CAD düzenini yansıtan, aranabilir ve sayfa doğruluğunda bir PDF üretir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | Değişken `cadImage` tanımlı değil (`image` olmalı). | `cadImage`'i `image` ile değiştirin veya değişkeni tutarlı şekilde yeniden adlandırın. |
| **Output WMF is blank** | Rasterleştirme sayfa boyutu çok küçük veya arka plan rengi şeffaf olarak ayarlanmış. | `PageWidth`/`PageHeight` değerlerini artırın veya `rasterizationOptions.setBackgroundColor(Color.WHITE);` ile bir arka plan rengi ayarlayın. |
| **License exception** | Üretimde geçerli bir Aspose lisansı olmadan çalıştırılıyor. | Uygulama başlangıcında lisans dosyasını uygulayın: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Sonuç

Artık Aspose.CAD for Java kullanarak **DXF'yi WMF'ye dönüştürmek** için eksiksiz, üretim‑hazır bir iş akışına sahipsiniz; aynı zamanda **çizimi PDF’ye dışa aktarma** adımı da isteğe bağlıdır. Bu yaklaşım, Windows tabanlı raporlama ve dokümantasyon araçlarıyla sorunsuz bir şekilde bütünleşen yüksek kaliteli vektör çıktısı sağlar ve kod tabanınızı basit ve bağımlılıklardan arındırır.

## SSS

### S1: Aspose.CAD dokümantasyonunu nereden bulabilirim?
C1: Dokümantasyona [buradan](https://reference.aspose.com/cad/java/) ulaşabilirsiniz.

### S2: Aspose.CAD for Java’yı nasıl indiririm?
C2: Kütüphaneyi [buradan](https://releases.aspose.com/cad/java/) indirebilirsiniz.

### S3: Ücretsiz deneme mevcut mu?
C3: Evet, ücretsiz denemeyi [buradan](https://releases.aspose.com/) alabilirsiniz.

### S4: Geçici lisans seçeneklerine mi ihtiyacınız var?
C4: Geçici lisansları [buradan](https://purchase.aspose.com/temporary-license/) inceleyebilirsiniz.

### S5: Destek nereden alınır?
C5: Aspose.CAD destek forumunu [buradan](https://forum.aspose.com/c/cad/19) ziyaret edebilirsiniz.

## Sıkça Sorulan Sorular

**S: Büyük DXF dosyalarını (yüzlerce MB) bellek tükenmeden dönüştürebilir miyim?**  
C: Evet. Dosyayı bir try‑with‑resources bloğunda yükleyin ve `Image` nesnesini hemen serbest bırakın. Bellek kullanımını düşük tutmak için `CadRasterizationOptions.setPageWidth/Height` değerlerini makul bir boyuta ayarlayın.

**S: WMF çıktısı katman bilgilerini korur mu?**  
C: WMF düz bir vektör formatıdır, bu yüzden katman hiyerarşisi düzleştirilir, ancak çizgi stilleri, renkler ve tarama desenleri korunur.

**S: WMF için özel bir DPI ayarlamak mümkün mü?**  
C: Kaydetmeden önce DPI'yi tanımlamak için `rasterizationOptions.setResolution(300);` kullanın.

**S: Tek bir çalıştırmada birden fazla DXF dosyasını toplu olarak dönüştürebilir miyim?**  
C: Kesinlikle. Bir dizin içinde döngü kurarak her dosyayı yükleyin ve aynı rasterleştirme ve kaydetme mantığını uygulayın.

**S: Hangi Java sürümleri destekleniyor?**  
C: Aspose.CAD for Java, Java 8 ve sonrası sürümleri destekler; Java 11, 17 ve daha yeni LTS sürümler dahil.

---

**Last Updated:** 2026-06-09  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## İlgili Öğreticiler

- [CAD'den PDF Oluştur – Aspose.CAD for Java ile DXF'yi PDF’ye Dışa Aktar](/cad/java/additional-features/export-dxf-to-pdf/)
- [DXF'den PDF Oluştur: Katmanı Aspose.CAD for Java ile Dışa Aktar](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [DXF Düzenini JPEG Görüntüsüne Dönüştürme – Aspose.CAD ile Java’da](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}