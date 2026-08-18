---
date: 2026-02-23
description: Aspose.CAD for Java kullanarak DWFX'i PDF'e dönüştürmeyi ve CAD'i PDF
  olarak kaydetmeyi öğrenin. DWFX dosyalarını açmak ve PDF oluşturmak için hızlı rehber.
linktitle: Open DWFX File
second_title: Aspose.CAD Java API
title: DWFX'i Java için Aspose.CAD ile PDF'ye Dönüştür
url: /tr/java/cad-file-manipulation/open-dwfx-file/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWFX'i PDF'e Aspose.CAD for Java ile Dönüştür

## Giriş

Günümüzün hızlı tempolu tasarım dünyasında, geliştiriciler genellikle **DWFX'i PDF'e dönüştürmek** zorundadır, böylece CAD çizimleri teknik olmayan paydaşlarla paylaşılabilir. Aspose.CAD for Java bu görevi basitleştirir; bir DWFX dosyasını açmanıza, rasterleştirmenize ve **CAD'i PDF olarak kaydetmenize** sadece birkaç satır kodla olanak tanır. Bu öğreticide, ortamınızı kurmaktan son PDF'yi doğrulamaya kadar tüm süreci adım adım inceleyeceğiz, böylece Java uygulamalarınızda DWFX dosyalarını güvenle işleyebilirsiniz.

## Hızlı Yanıtlar
- **Bu kılavuzun temel amacı nedir?** Aspose.CAD for Java kullanarak DWFX'i PDF'e nasıl dönüştüreceğinizi göstermek.  
- **Hangi kütüphane gereklidir?** Aspose.CAD for Java (resmi Aspose sitesinden indirin).  
- **Lisans almam gerekir mi?** Geliştirme için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.  
- **DWFX dosyalarını doğrudan açabilir miyim?** Evet, DWFX dosyalarını açmak için `Image.load` kullanın.  
- **Örnek hangi çıktı formatını üretir?** Belirtilen çıktı dizinine kaydedilen bir PDF dosyası.

## “DWFX'i PDF'e dönüştürmek” nedir?

DWFX'i PDF'e dönüştürmek, Autodesk ürünlerinde yaygın olarak kullanılan vektör tabanlı bir DWFX çizimini, taşınabilir ve geniş çapta desteklenen bir PDF belgesine render etmektir. Bu, alıcının tarafında CAD yazılımı gerektirmeden kolay görüntüleme, yazdırma ve paylaşma imkanı sağlar.

## Neden Aspose.CAD for Java ile **CAD'i PDF olarak kaydet**?

- **Harici bağımlılık yok:** Saf Java API, yerel CAD motorlarına ihtiyaç duymaz.  
- **Yüksek doğrulukta render:** Çizgi kalınlıklarını, renkleri ve katmanları korur.  
- **Toplu işleme dostu:** Sunucu tarafı otomasyon veya bulut hizmetleri için idealdir.  
- **Çapraz platform:** Windows, Linux ve macOS üzerinde çalışır.

## Önkoşullar

Kodlamaya başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Aspose.CAD for Java Library** – [Aspose.CAD for Java indirme sayfasından](https://releases.aspose.com/cad/java/) indirin.  
- **Java Geliştirme Ortamı** – JDK 8 veya daha yeni bir sürüm, tercih ettiğiniz IDE veya derleme aracı ile.  
- **DWFX Dosyası** – Dönüşümü test etmek için bir örnek DWFX dosyası (ör. `Tyrannosaurus.dwfx`).

## İsim Uzaylarını İçe Aktarın

İhtiyacımız olan sınıfları önce içe aktaralım:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Aspose.CAD for Java ile DWFX'i PDF'e Dönüştürme

Aşağıda adım adım bir açıklama yer almaktadır. Her adım kısa bir açıklama ve ardından çalıştıracağınız tam kodu içerir.

### Adım 1: DWFX Dosyasını Yükle  

```java
String SourceDir = Utils.getDataDir_DWFXDrawings();
String OutputDir = Utils.getDataDir_Output();
String filePath = SourceDir + "Tyrannosaurus.dwfx";

Image cadImageDwf = Image.load(filePath);
```

`Image.load` yöntemi DWFX dosyasını belleğe okur ve rasterleştirme için hazır bir `CadImage` nesnesi sağlar.

### Adım 2: Rasterleştirme Seçeneklerini Ayarla  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImageDwf.getSize().getWidth());
rasterizationOptions.setPageHeight(cadImageDwf.getSize().getHeight());
```

Bu seçenekler çıktı sayfa boyutunu tanımlar, PDF'in orijinal çizim boyutlarıyla eşleşmesini sağlar.

### Adım 3: PDF Seçeneklerini Yapılandır  

```java
PdfOptions CADf = new PdfOptions();
CADf.setVectorRasterizationOptions(rasterizationOptions);
```

Burada rasterleştirme ayarlarını PDF dışa aktarma yapılandırmasına bağlarız.

### Adım 4: PDF Olarak Kaydet  

```java
cadImageDwf.save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

`save` metodunu çağırmak, render edilen görüntüyü çıktı klasöründeki bir PDF dosyasına yazar.

### Adım 5: Başarıyı Doğrula  

```java
System.out.println("OpenDwfxFile executed successfully");
```

Basit bir konsol mesajı, dönüşümün hatasız tamamlandığını onaylar.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Muhtemel Neden | Çözüm |
|-------|----------------|-------|
| **Boş PDF çıktısı** | Rasterleştirme genişliği/yüksekliği 0 olarak ayarlandı | Seçenekleri ayarlamadan önce `cadImageDwf.getSize()` geçerli boyutlar döndürdüğünden emin olun. |
| **Bellek yetersiz hatası** | Çok büyük DWFX dosyası | JVM yığın boyutunu (`-Xmx2g`) artırın veya dosyayı daha küçük bölümlerde işleyin. |
| **Eksik yazı tipleri** | Yazı tipi kaynak DWFX içinde gömülü değil | Gerekli yazı tiplerini sunucuya kurun veya yedek bir yazı tipi belirtmek için `CadRasterizationOptions.setFontName` kullanın. |

## Sıkça Sorulan Sorular

### Q1: Aspose.CAD for Java'yi diğer CAD dosya formatlarıyla kullanabilir miyim?  
A1: Evet, Aspose.CAD for Java geniş bir CAD formatı yelpazesini destekler ve geliştiriciler için çok yönlü bir çözüm sunar.

### Q2: Aspose.CAD for Java için ücretsiz deneme mevcut mu?  
A2: Evet, Aspose.CAD for Java'nun yeteneklerini ücretsiz deneme ile keşfedebilirsiniz. Başlamak için [bu bağlantıyı](https://releases.aspose.com/) ziyaret edin.

### Q3: Aspose.CAD for Java için destek nasıl alınır?  
A3: Yardım ve iş birliği için Aspose.CAD topluluğuna [destek forumunda](https://forum.aspose.com/c/cad/19) katılın.

### Q4: Aspose.CAD for Java için geçici lisanslar mevcut mu?  
A4: Evet, Aspose.CAD for Java için geçici bir lisans alabilirsiniz. Daha fazla bilgi için [bu bağlantıyı](https://purchase.aspose.com/temporary-license/) ziyaret edin.

### Q5: Aspose.CAD for Java dokümantasyonunu nerede bulabilirim?  
A5: Kapsamlı dokümantasyon [burada](https://reference.aspose.com/cad/java/) mevcuttur.

**Son Güncelleme:** 2026-02-23  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}