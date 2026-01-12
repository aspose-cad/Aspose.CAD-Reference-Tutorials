---
date: 2026-01-12
description: Aspose.CAD for Java kullanarak DWG dosyalarında otomatik kod sayfası
  algılamasını geçersiz kılarak CAD'i PDF'ye nasıl dışa aktaracağınızı öğrenin. Kodlama
  ve bozuk CIF/MIF dosyalarını ele alır.
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: CAD'yi PDF'ye Dışa Aktar – DWG Dosyalarında Otomatik Kod Sayfası Algılamasını
  Java ile Geçersiz Kıl
url: /tr/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD'yi PDF'ye Dışa Aktarma – DWG Dosyalarında Otomatik Kod Sayfası Algılamasını Java ile Geçersiz Kılma

## Giriş

Bu kapsamlı rehberde, DWG dosyalarındaki metni bozabilen otomatik kod sayfası algılamasını geçersiz kılarak **CAD'yi PDF'ye nasıl dışa aktaracağınızı** keşfedeceksiniz. Aspose.CAD for Java, kodlamayı ince ayar yapmanıza olanak tanır, bozuk CIF/MIF verilerini kurtarmanızı ve güvenilir PDF çıktısı üretmenizi sağlar. İster bir toplu dönüştürücü oluşturuyor olun, ister CAD işleme işlevini daha büyük bir Java uygulamasına entegre ediyor olun, aşağıdaki adımlar tüm iş akışını size gösterecektir.

## Hızlı Yanıtlar
- **“Kod sayfasını geçersiz kıl” ne anlama gelir?** Aspose.CAD'in tahmin etmek yerine belirli bir karakter kodlamasını kullanmasını zorlar.
- **DWG'yi doğrudan PDF'ye dışa aktarabilir miyim?** Evet – doğru kod sayfasını ayarladıktan sonra CAD görüntüsünü PDF olarak kaydedebilirsiniz.
- **Japonca metin için hangi kodlama çalışır?** `CodePages.Japanese` ve `MifCodePages.Japanese` doğru seçimlerdir.
- **Üretim kullanımı için lisansa ihtiyacım var mı?** Ticari bir lisans gereklidir; test için geçici bir lisans mevcuttur.
- **Hangi Aspose.CAD sürümü gerekiyor?** `LoadOptions` ve `PdfOptions` destekleyen herhangi bir yeni sürüm.

## “CAD'yi PDF'ye dışa aktarma” nedir?
CAD'yi PDF'ye dışa aktarmak, vektör tabanlı CAD çizimlerini geniş çapta desteklenen, sabit düzenli bir belge formatına dönüştürür. Oluşan PDF, çizgi çalışmasını, katmanları ve metni korurken çizimi paylaşmayı, yazdırmayı veya diğer uygulamalara gömmeyi kolaylaştırır.

## Otomatik kod sayfası algılamasını neden geçersiz kılmalıyız?
DWG dosyaları genellikle metni eski kod sayfalarıyla depolar. Aspose.CAD'in otomatik algılaması bu baytları yanlış yorumlayabilir ve bozuk karakterlere yol açabilir. Kod sayfasını manuel olarak belirleyerek, özellikle Japonca, Kiril veya Arapça gibi Latin dışı yazı sistemleri için, metnin dışa aktarılan PDF'de tam olarak istediğiniz gibi görünmesini sağlarsınız.

## Ön Koşullar
- **Java Geliştirme Ortamı** – JDK 8+ ve tercih ettiğiniz IDE.
- **Aspose.CAD for Java** – Kütüphaneyi resmi siteden [buradan](https://releases.aspose.com/cad/java/) indirin.
- **DWG Örnek Dosyası** – Sağlanan `SimpleEntities.dwg` dosyasını veya dönüştürmek istediğiniz herhangi bir DWG dosyasını kullanın.

## Paketleri İçe Aktarma
Java projenizde, gerekli Aspose.CAD sınıflarını içe aktarın:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Adım‑Adım Kılavuz

### Adım 1: Java Projesini Kurun
Yeni bir Maven veya Gradle projesi oluşturun ve Aspose.CAD JAR dosyasını sınıf yoluna ekleyin. Bu adım, IDE'nin içe aktarılan sınıfları çözümleyebilmesini sağlar.

### Adım 2: Belirtilen Kod Sayfası ile DWG Dosyasını Yükleyin
Aspose.CAD'e hangi kodlamayı kullanacağını ve bozuk CIF/MIF verilerinin kurtarılmaya çalışılıp çalışılmayacağını söyleyin.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Adım 3: CAD Görüntüsünü PDF'ye Dışa Aktarın
Doğru kod sayfası uygulandığında, çizimi güvenle dışa aktarabilirsiniz. `PdfOptions` nesnesi, PDF çıktısını (sıkıştırma, rasterleştirme vb.) ince ayar yapmanıza olanak tanır.

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Adım 4: Başarıyı Doğrulayın
Basit bir konsol mesajı, işlemin istisna olmadan tamamlandığını doğrular.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Bu adımları birden fazla DWG dosyası için tekrarlayabilir, kaynak yolunu ve çıktı adını gerektiği gibi ayarlayabilirsiniz.

## Yaygın Sorunlar ve Çözümler
- **Garbage karakterler hâlâ görünüyor:** `specifiedEncoding`'in orijinal DWG'nin kod sayfasıyla eşleştiğini iki kez kontrol edin. Gerekirse farklı bir `CodePages` enum'u kullanın.
- **`cadImage.save` üzerinde `NullPointerException`:** DWG dosyasının doğru yüklendiğinden emin olun; yolu ve dosya izinlerini doğrulayın.
- **PDF boyutu büyük:** `PdfOptions` içinde sıkıştırmayı etkinleştirin (ör. `pdfOptions.setCompress(true)`).

## Sıkça Sorulan Sorular

**Q1: Aspose.CAD tüm DWG dosyası sürümleriyle uyumlu mu?**  
A1: Aspose.CAD, AutoCAD 2018 ve daha önceki sürümler dahil olmak üzere geniş bir DWG sürüm yelpazesini destekler.

**Q2: Aspose.CAD'i ticari projelerde kullanabilir miyim?**  
A2: Evet, üretim kullanımı için ticari bir lisans gereklidir. Lisansı [buradan](https://purchase.aspose.com/buy) edinebilirsiniz.

**Q3: Ücretsiz deneme sürümünde herhangi bir sınırlama var mı?**  
A3: Deneme sürümü boyut ve özellik kısıtlamaları getirir; ayrıntılar için resmi belgelere bakın.

**Q4: Aspose.CAD için destek nasıl alabilirim?**  
A4: Yardım ve tartışmalar için topluluk [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

**Q5: Test amaçları için geçici bir lisans mevcut mu?**  
A5: Evet, geçici bir lisans [buradan](https://purchase.aspose.com/temporary-license/) istenebilir.

---

**Son Güncelleme:** 2026-01-12  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.11 (yazım sırasında en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}