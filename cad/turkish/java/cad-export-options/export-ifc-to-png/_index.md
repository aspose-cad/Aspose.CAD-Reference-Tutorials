---
date: 2025-12-21
description: Aspose.CAD for Java ile IFC'yi PNG'ye zahmetsizce dönüştürün. Adım adım
  öğreticimizi izleyin.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java ile IFC'yi PNG'ye Dönüştür
url: /tr/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java ile IFC'yi PNG'ye Dönüştürme

## Giriş

Bu öğreticide, güçlü Aspose.CAD Java kütüphanesini kullanarak **IFC'yi PNG'ye nasıl dönüştüreceğinizi** öğreneceksiniz. İster bir BIM görüntüleyici oluşturuyor olun, ister bir inşaat portalı için küçük resimler üretiyor olun ya da belgeleme hatlarını otomatikleştiriyor olun, IFC (Industry Foundation Classes) dosyalarını raster görüntülere dönüştürmek yaygın bir gereksinimdir. Her adımı adım adım inceleyecek, ayarların arkasındaki mantığı açıklayacak ve en iyi görsel sonuçları elde etmeniz için ipuçları vereceğiz.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.CAD for Java (ücretsiz deneme mevcut).  
- **Desteklenen IFC sürümleri?** Çoğu IFC 2x3 ve IFC4 dosy işlenir.  
- **Tipik dönüşüm süresi?** Standart modeller için birkaç saniye; dosya boyutuna bağlıdır.  
- **Lisans gerekiyor mu?** Üretim kullanımında geçici bir lisans gereklidir.  
- **Görüntü boyutunu özelleştirebilir miyim?** Evet – genişlik ve yüksekliği ayarlamak `CadRasterizationOptions` kullanın.

## “IFC'yi PNG'ye dönüştürmek” nedir?
IFC'yi PNG'ye dönüştürmek, 3‑B boyutlu bir bina modelini (IFC) 2‑B bitmap görüntüsü (PNG) haline rasterleştirmek anlamına gelir. Bu süreç geometrileri düzleştirir, varsayılan görsel stilleri uygular ve bir CAD görüntüleyiciye ihtiyaç duymadan tarayıcılarda, raporlarda veya mobil uygulamalarda görüntülenebilen taşınabilir bir resim üretir.

## Neden Aspose.CAD for Java kullanmalı?
- **Harici CAD yazılımı gerekmez** – saf Java API, herhangi bir platformda çalışır.  
- **Yüksek doğruluklu render** – hat kalınlıklarını, renkleri ve katmanları korur.  
- **Tam kontrol** – rasterleştirme seçenekleri çözünürlük, arka plan ve daha fazlasını tanımlamanıza olanak verir.  
- **Kolay lisanslama** – deneme ve geçici lisanslar değerlendirmeyi basitleştirir.

## Önkoşullar

Başlamadan önce, aşağıdakilere sahip olduğunuzdan emin olun:

- **Aspose.CAD Kütüphanesi** – [download link](https://releases.aspose.com/cad/java/) adresinden indirip kurun.  
- **Java Development Kit (JDK)** – sürüm 8 veya üzeri.  
- **Bir klasör** içinde dönüştürmek istediğiniz IFC dosyasını bulundurun.

## İsim Uzaylarını İçe Aktarma

Java projenizde gerekli sınıfları içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Adım‑Adım Kılavuz

### Adım 1: IFC Dosyasını Yükleyin

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Burada kaynak IFC dosyasını bir `IfcImage` nesnesine yüklüyoruz. Aspose.CAD, IFC yapısını otomatik olarak ayrıştırır ve rasterleştirme için hazırlar.

### Adım 2: Vektör (Rasterleştirme) Seçeneklerini Ayarlayın

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

`CadRasterizationOptions`, 3‑B geometrisinin nasıl düzleştirileceğini kontrol eder. İstenen PNG çözünürlüğüne uygun olması için `PageWidth` ve `PageHeight` değerlerini ayarlayın. Daha büyük değerler daha yüksek detaylı görüntüler üretir ancak bellek kullanımını artırır.

### Adım 3: PNG Dışa Aktarma Ayarlarını Yapılandırın

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

`PngOptions`, Aspose.CAD'e bir PNG dosyası üretmesini söyler ve önceki adımda tanımlanan rasterleştirme ayarlarını bağlar.

### Adım 4: Görüntüyü PNG Olarak Kaydedin

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

`save` metodu rasterleştirilmiş görüntüyü diske yazar. Bu satır çalıştıktan sonra, `example.png` dosyasını kaynak IFC dosyanızla aynı dizinde bulacaksınız.

## Yaygın Sorunlar ve Çözümler

| Issue | Why it Happens | Fix |
|-------|----------------|-----|
| **Boş PNG çıktısı** | Rasterleştirme seçeneklerinde genişlik/yükseklik 0 veya çok küçük olarak ayarlandığında. | `PageWidth` ve `PageHeight` değerlerinin pozitif tam sayılar olduğundan emin olun (ör. 1500). |
| **Eksik katmanlar veya renkler** | Varsayılan görünüm bazı katmanları gizleyebilir. | `vectorOptions.setRenderMode(CadRenderMode.Wireframe)` kullanın veya gerektiğinde API aracılığıyla katman görünürlüğünü ayarlayın. |
| **Büyük IFC dosyaları için bellek yetersizliği hataları** | Çok yüksek çözünürlük çok fazla RAM tüketir. | Çözünürlüğü düşürün veya modeli bölümler halinde işleyin. |

## SSS'ler

### S1: Aspose.CAD tüm IFC dosya sürümleriyle uyumlu mu?
A1: Aspose.CAD, çeşitli IFC dosya sürümlerini destekler. Uyumluluk detayları için [documentation](https://reference.aspose.com/cad/java/) adresine bakın.

### S2: Rasterleştirme seçeneklerini daha da özelleştirebilir miyim?
A2: Kesinlikle! Gelişmiş özelleştirme seçenekleri için [documentation](https://reference.aspose.com/cad/java/) adresini inceleyin.

### S3: Deneme sürümü mevcut mu?
A3: Evet, ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

### S4: Aspose.CAD için geçici lisans nasıl alınır?
A4: [Bu linkten](https://purchase.aspose.com/temporary-license/) geçici bir lisans edinin.

### S5: Yardım almak veya sorunları tartışmak için nereden ulaşabilirim?
A5: Topluluk desteği için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

## Sıkça Sorulan Sorular (Ek)

**S: Birden fazla IFC dosyasını toplu olarak dönüştürebilir miyim?**  
C: Evet. Yükleme ve kaydetme mantığını, dosya yolu listesi üzerinde dönen bir döngü içinde sarın.

**S: PNG'nin arka plan rengini nasıl değiştiririm?**  
C: `PngOptions` oluşturulmadan önce `vectorOptions.setBackgroundColor(Color.getWhite())` (veya herhangi bir `java.awt.Color`) ayarlayın.

**S: JPEG veya BMP gibi diğer raster formatlarına dışa aktarmak mümkün mü?**  
C: Kesinlikle. `PngOptions` yerine `JpegOptions` veya `BmpOptions` kullanın ve format‑özel ayarları gerektiği gibi düzenleyin.

**S: Dönüştürmeden sonra kaynakları serbest bırakmam gerekiyor mu?**  
C: İşiniz bittiğinde yerel belleği serbest bırakmak için `cadImage.dispose()` çağırın.

---

**Son Güncelleme:** 2025-12-21  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12 (yazım anındaki en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}