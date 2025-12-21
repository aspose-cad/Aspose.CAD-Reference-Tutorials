---
date: 2025-12-21
description: Aspose.CAD for Java kullanarak CAD düzenlerini PDF'ye nasıl dışa aktaracağınızı
  öğrenin – CAD dosyalarından PDF oluşturmanın hızlı ve güvenilir bir yolu.
linktitle: Export CAD Layouts to PDF
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java ile CAD Düzenlerini PDF'ye Nasıl Dışa Aktarılır
url: /tr/java/cad-export-options/export-cad-layouts-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD Düzenlerini PDF'e Aspose.CAD for Java ile Nasıl Dışa Aktarılır

## Giriş

Bu öğreticide, **CAD** düzenlerini Aspose.CAD for Java kullanarak PDF'e nasıl dışa aktaracağınızı göstereceğiz. DWG, DXF veya diğer CAD formatlarıyla çalışıyor olun, bu kılavuz CAD dosyalarından hızlı ve güvenilir bir şekilde PDF oluşturmak için temiz, programatik bir yaklaşımı adım adım anlatır.

## Hızlı Yanıtlar
- **Kütüphane ne işe yarar?** CAD çizimlerini (DWG, DXF, DWF vb.) PDF, raster görüntüler ve diğer formatlara dönüştürür.  
- **Hangi dil kullanılıyor?** Java – kod, herhangi bir JVM‑uyumlu platformda çalışır.  
- **Lisans gerekli mi?** Ücretsiz deneme sürümü mevcuttur; üretim için ticari lisans gereklidir.  
- **Java'da DWG'yi PDF'e dönüştürebilir miyim?** Evet – aynı API **dwg to pdf java** dönüşümlerini destekler.  
- **Ana adımlar nelerdir?** CAD dosyasını yükleyin, rasterleştirme seçeneklerini ayarlayın, PDF seçeneklerini yapılandırın ve sonucu kaydedin.

## Önkoşullar

Öğreticiye başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

- Aspose.CAD for Java: Kütüphanenin yüklü olduğundan emin olun. Aspose web sitesinden [buradan](https://releases.aspose.com/cad/java/) indirebilirsiniz.

- Java Geliştirme Ortamı: Makinenizde bir Java geliştirme ortamı kurulu olmalı.

Her şey kurulduysa, öğreticiye başlayalım.

## “how to export cad” nedir?

CAD dışa aktarma, yerel CAD çizim verilerini (DWG, DXF veya DWF gibi) PDF gibi daha evrensel bir formatta okunabilir hâle getirmektir. Bu süreç, CAD yazılımı olmayan paydaşlarla tasarımları paylaşmak için gereklidir.

## Neden Aspose.CAD for Java ile CAD'i PDF'e Dışa Aktarmalısınız?

- **Yüksek doğruluk** – vektör grafikleri korunur ve rasterleştirme seçenekleri kaliteyi ince ayar yapmanıza olanak tanır.  
- **Harici bağımlılık yok** – saf Java, yerel DLL veya COM bileşeni gerektirmez.  
- **Çoklu format desteği** – DWG, DWF veya diğer formatlarda oluşturulmuş **generate pdf from cad** dosyalarından da PDF üretebilirsiniz.  
- **Toplu işler için ölçeklenebilir** – sunucu‑tarafı otomasyon, CI boru hatları veya masaüstü yardımcı programlar için idealdir.

## İsim Uzaylarını İçe Aktarma

Java kodunuzda, gerekli sınıflara erişim sağlamak için aşağıdaki isim uzaylarını içe aktarın.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Adım 1: CAD Dosyasını Yükleme

`Image.load` yöntemiyle CAD dosyasını Java uygulamanıza yükleyin. `"conic_pyramid.dxf"` ifadesini CAD dosyanızın yolu ile değiştirin.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Adım 2: Rasterleştirme Seçeneklerini Ayarlama

CAD varlıklarının nasıl rasterleştirileceğini tanımlamak için bir `CadRasterizationOptions` örneği oluşturun. Sayfa genişliği, sayfa yüksekliği ve düzen ölçeklendirme gibi parametreleri ihtiyacınıza göre ayarlayın.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## Adım 3: PDF Seçeneklerini Ayarlama

Bir `PdfOptions` örneği oluşturun ve rasterleştirme seçenekleriyle ilişkilendirin. Ayrıca PDF dışa aktarımı için grafik seçeneklerini, örneğin yumuşatma modu, metin render ipucu ve interpolasyon modunu ayarlayın.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## Adım 4: PDF'e Dışa Aktarma

Son olarak, `cadImage` nesnesinin `save` yöntemiyle CAD düzenlerini bir PDF dosyasına dışa aktarın.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| **Boş PDF çıktısı** | Rasterleştirme seçenekleri doğru ayarlanmamış (ör. düzen adı uyuşmazlığı) | `rasterizationOptions.setLayouts()` değerinin CAD dosyanızdaki düzen adlarıyla eşleştiğini doğrulayın. |
| **Düşük çözünürlüklü görüntüler** | `PageWidth`/`PageHeight` çok küçük | Sayfa boyutlarını artırın veya `rasterizationOptions.setResolution()` ile daha yüksek DPI ayarlayın. |
| **Desteklenmeyen CAD sürümü** | Eski DWG/DXF sürümleri daha yeni bir Aspose.CAD sürümü gerektirebilir | Aspose sitesinden en son kütüphane sürümünü indirin. |

## Sık Sorulan Sorular

### S1: Aspose.CAD for Java'yı diğer CAD dosya formatlarıyla kullanabilir miyim?

C1: Evet, Aspose.CAD DWG, DXF, DWF ve daha fazlası dahil olmak üzere çeşitli CAD formatlarını destekler. Tam liste için belgeleri [burada](https://reference.aspose.com/cad/java/) inceleyin.

### S2: Aspose.CAD for Java için ücretsiz bir deneme sürümü var mı?

C2: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) keşfedebilirsiniz.

### S3: Aspose.CAD for Java için destek nasıl alınır?

C3: Topluluk desteği için Aspose.CAD forumunu [burada](https://forum.aspose.com/c/cad/19) ziyaret edin. Premium destek için bir lisans satın almayı [buradan](https://purchase.aspose.com/buy) değerlendirin.

### S4: Otomatik ve manuel düzen ölçeklendirme arasındaki fark nedir?

C4: Otomatik düzen ölçeklendirme, sayfa boyutlarına göre düzen boyutunu ayarlar; manuel ölçeklendirme ise özel ölçek değerleri belirlemenize olanak tanır.

### S5: Dışa aktarılan PDF dosyalarının görünümünü özelleştirebilir miyim?

C5: Evet, kod içinde grafik seçeneklerini özelleştirerek PDF'in kalite ve görünümünü kontrol edebilirsiniz.

### S6: Aspose.CAD **dwg to pdf java** dönüşümünü doğrudan destekliyor mu?

C6: Kesinlikle. Aynı rasterleştirme ve PDF seçenekleri DWG dosyaları için de çalışır ve sorunsuz **dwg to pdf java** dönüşümleri sağlar.

### S7: **generate pdf from cad** işlemini bitmap rasterleştirmeden yapabilir miyim?

C7: `rasterizationOptions.setContentAsBitmap(false)` ayarını yaparak mümkün olduğunca vektör veriyi korur, böylece gerçek vektör‑tabanlı bir PDF elde edersiniz.

---

**Son Güncelleme:** 2025-12-21  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.10  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}