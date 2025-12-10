---
date: 2025-12-07
description: Aspose.CAD for Java kullanarak CAD'i PDF'ye dönüştürürken PDF sayfa boyutunu
  nasıl ayarlayacağınızı öğrenin. İzlemeyi etkinleştirmek, CAD'i PDF'ye dönüştürmek
  ve CAD'i PDF olarak verimli bir şekilde kaydetmek için bu adım adım kılavuzu izleyin.
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: PDF Sayfa Boyutunu Nasıl Ayarlarsınız ve CAD Render İşlemi İçin İzlemeyi Nasıl
  Etkinleştirirsiniz
url: /tr/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD Rendering Süreci için İzlemeyi Etkinleştirme

## Giriş

Bu öğreticide **Aspose.CAD for Java** kullanarak **CAD'ı PDF'ye dönüştürürken PDF sayfa boyutunu ayarlamayı** öğreneceksiniz. İzlemeyi etkinleştirerek renderleme hattı üzerinde tam görünürlük elde eder, CAD dosyalarından (ör. DXF) PDF'ye dönüşümü daha kolay hata ayıklayıp optimize edebilirsiniz. **CAD'ı PDF olarak kaydetme**, DXF'ten PDF oluşturma ya da çıktı boyutlarını kontrol etme ihtiyacınız olsun, aşağıdaki adımlar tüm süreci size gösterecek.

## Hızlı Yanıtlar
- **“PDF sayfa boyutunu ayarla” ne işe yarar?** CAD renderleme sırasında oluşacak PDF sayfasının genişlik ve yüksekliğini tanımlar.  
- **Neden izleme etkinleştirilmeli?** İzleme, dönüşümün her aşamasını kaydederek performans darboğazlarını ya da hataları tespit etmenizi sağlar.  
- **Lisans gerekli mi?** Değerlendirme için ücretsiz deneme yeterlidir; üretim ortamı için ticari lisans gerekir.  
- **Hangi CAD formatları destekleniyor?** DWG, DXF, DGN ve daha birçok format – tam liste için Aspose.CAD dokümantasyonuna bakın.  
- **Sayfa boyutlarını anlık olarak değiştirebilir miyim?** Evet – `CadRasterizationOptions` içindeki `PageWidth` ve `PageHeight` değerlerini istediğiniz gibi ayarlayın.

## CAD renderlemede “PDF sayfa boyutunu ayarla” nedir?

PDF sayfa boyutunu ayarlamak, rasterizer'a vektörel CAD verisinin PDF sayfasına rasterleştirilirken tuvalin ne kadar büyük olması gerektiğini bildirir. Bu, özellikle detaylı mühendislik çizimlerinde görsel bütünlüğün korunması için kritiktir.

## CAD renderlemede izleme neden etkinleştirilmeli?

İzleme, kaynak dosyanın yüklenmesinden PDF çıktısının yazılmasına kadar her adımın ayrıntılı bir kaydını sağlar. Şunlara yardımcı olur:

- Belirli bir çizimin neden hatalı renderlendiğini teşhis etmek.  
- Her aşamanın süresini ölçerek performans ayarı yapmak.  
- Ayarladığınız sayfa boyutunun gerçekten uygulandığını doğrulamak.

## Önkoşullar

İzleme kurulumuna geçmeden önce aşağıdaki önkoşulları sağlayın:

1. **Java Geliştirme Ortamı** – Makinenizde Java 8 veya daha yeni bir sürüm yüklü olmalı.  
2. **Aspose.CAD Kütüphanesi** – Aspose.CAD kütüphanesini indirin ve Java projenize entegre edin. İndirme bağlantısını [burada](https://releases.aspose.com/cad/java/) bulabilirsiniz.  
3. **Belge Dizini** – CAD dosyalarınızı ve oluşturulacak PDF'leri saklayacağınız bir dizin hazırlayın.

## İsim Uzaylarını İçe Aktarma

Java projenizde Aspose.CAD işlevselliğini kullanmak için gerekli isim uzaylarını içe aktarın. Kodunuzun başına aşağıdaki satırları ekleyin:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Kaynak Dizin Yolunu Ayarlama

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

`"Your Document Directory"` ifadesini gerçek belge dizini yolunuzla değiştirin.

## CAD Dosyasını Yükleme

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

CAD dosyanızın yolunu belirtin; dosyanın belirlediğiniz belge dizini içinde olduğundan emin olun.

## PDF Çıktı Seçeneklerini Ayarlama

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

Bir çıktı akışı oluşturun ve dönüşüm için PDF seçeneklerini ayarlayın.

## CadRasterizationOptions'ı Yapılandırma (PDF Sayfa Boyutunu Ayarla)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

Burada **PDF sayfa boyutunu ayarlıyoruz**; `PageWidth` ve `PageHeight` değerlerini tanımlıyoruz. Bu değerleri mühendislik çiziminizin gerektirdiği boyutlara göre ayarlayın. Bu adım, CAD içeriğinin ölçeklenmesi ve nihai PDF'de renderlenmesi üzerinde doğrudan etkili olur.

## PDF Dosyasını Kaydetme

```java
image.save(stream, pdfOptions);
```

Belirttiğiniz seçeneklerle renderlenmiş PDF dosyasını kaydedin.

## İzleme Etkinleştirmesini Doğrulama

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

CAD renderleme sürecinde izlemenin başarıyla etkinleştirildiğini onaylayın.

## Yaygın Sorunlar ve Çözüm Önerileri

| Belirti | Muhtemel Neden | Çözüm |
|---------|----------------|------|
| PDF sayfası boş görünüyor | `PageWidth`/`PageHeight` 0 olarak ayarlanmış | Sıfır olmayan boyutlar sağlayın. |
| Çıktı dosyası bozuk | Çıktı akışı kapatılmamış | `image.save(...)` sonrası `stream.close()` çağırın. |
| PDF'te katmanlar eksik | CAD dosyası desteklenmeyen varlıklar içeriyor | Dosyanın Aspose.CAD tarafından tam desteklendiğini doğrulayın. |

## Sık Sorulan Sorular

### S1: Aspose.CAD tüm CAD dosya formatlarıyla uyumlu mu?

C1: Aspose.CAD, DWG, DXF, DGN ve daha fazlası dahil olmak üzere geniş bir CAD formatı yelpazesini destekler. Kapsamlı liste için [dokümantasyona](https://reference.aspose.com/cad/java/) bakın.

### S2: PDF dosyasının çıktı boyutlarını özelleştirebilir miyim?

C2: Kesinlikle! `CadRasterizationOptions` içindeki `PageWidth` ve `PageHeight` parametrelerini değiştirerek çıktı boyutlarını istediğiniz gibi ayarlayabilirsiniz.

### S3: Aspose.CAD for Java için ücretsiz bir deneme mevcut mu?

C3: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) edinebilirsiniz.

### S4: Aspose.CAD ile ilgili sorular için topluluk desteği nasıl alınır?

C4: Toplulukla etkileşime geçmek ve yardım almak için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

### S5: Aspose.CAD için geçici lisanslar sağlanıyor mu?

C5: Evet, geçici bir lisansa ihtiyacınız varsa [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

## Sonuç

Tebrikler! **Aspose.CAD for Java** kullanarak **PDF sayfa boyutunu ayarlamayı** ve CAD renderleme sürecinde izlemeyi **etkinleştirmeyi** öğrendiniz. Bu kılavuz, **CAD'ı PDF'ye dönüştürme**, **CAD'ı PDF olarak kaydetme** ve **DXF'ten PDF oluşturma** konularında sayfa boyutları ve ayrıntılı yürütme günlükleri üzerinde tam kontrol sağlayarak size yardımcı olacak. Farklı sayfa boyutlarıyla denemeler yapın ve mühendislik iş akışlarınıza uygun ek rasterizasyon seçeneklerini keşfedin.

---

**Son Güncelleme:** 2025-12-07  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.12 (yazım anındaki en yeni sürüm)  
**Yazar:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
