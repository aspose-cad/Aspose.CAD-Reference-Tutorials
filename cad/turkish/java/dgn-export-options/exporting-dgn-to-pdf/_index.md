---
date: 2026-05-04
description: Aspose.CAD for Java kullanarak DGN'yi AutoCAD PDF'ye dışa aktararak CAD
  PDF dosyalarını nasıl dönüştüreceğinizi öğrenin. Özelleştirilebilir PDF boyutu ve
  seçenekleriyle adım adım rehber.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: AutoCAD formatında DGN'yi PDF'ye dışa aktarma
second_title: Aspose.CAD Java API
title: CAD PDF'yi Dönüştür – Aspose.CAD for Java ile DGN'den AutoCAD PDF'ye Kolay
  Dışa Aktarım
url: /tr/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD PDF'yi Dönüştürün: Aspose.CAD for Java ile DGN'den AutoCAD PDF'ye Kolay Dışa Aktarım

## Giriş

DGN kaynaklarından doğrudan **convert CAD PDF** dosyalarını dönüştürmeniz gerekiyorsa, doğru yerdesiniz. Bu öğreticide, Aspose.CAD for Java kullanarak DGN dosyalarını AutoCAD uyumlu bir PDF'ye dışa aktarmayı adım adım göstereceğiz. Özel sayfa boyutlarını nasıl ayarlayacağınızı, belirli düzenleri nasıl seçeceğinizi ve PDF çıktısını nasıl ince ayar yapacağınızı göreceksiniz — kendi projenize ekleyebileceğiniz net, adım adım kodlarla.

## Hızlı Yanıtlar
- **convert CAD PDF** ne anlama geliyor? Bu, CAD kaynak dosyalarını (ör. DGN) vektör verilerini ve düzen doğruluğunu koruyan bir PDF'ye dönüştürmeyi ifade eder.  
- **Which library handles the conversion?** Aspose.CAD for Java bu görev için güvenilir, lisans‑sız bir deneme sürümü sunar.  
- **Do I need a license for development?** Test için ücretsiz deneme yeterlidir; üretim kullanımı için ticari lisans gereklidir.  
- **Can I customize the PDF size?** Evet – `CadRasterizationOptions` sayfa genişliği, yüksekliği ve ölçeklemeyi ayarlamanıza izin verir.  
- **How many lines of code are required?** PDF'yi yüklemek, yapılandırmak ve kaydetmek için 20 satırdan az Java kodu yeterlidir.  

## “convert CAD PDF” nedir?
CAD PDF'yi dönüştürmek, yerel bir CAD çizimini (ör. DGN) alıp, orijinal vektör grafikleri, katmanları ve düzen bilgilerini koruyan bir PDF üretmek anlamına gelir. Oluşan PDF, CAD yazılımına ihtiyaç duymadan herhangi bir cihazda görüntülenebilir; bu da paylaşım, baskı veya arşivleme için idealdir.

## CAD PDF'yi dönüştürmek için Aspose.CAD for Java neden kullanılmalı?
- **Full format support** – DGN, DWG, DXF ve daha birçok format.  
- **No external dependencies** – saf Java, yerel DLL'ler yok.  
- **Fine‑grained control** – hangi düzenlerin dışa aktarılacağını seçebilir, özel sayfa boyutları ayarlayabilir ve rasterleştirme kalitesini kontrol edebilirsiniz.  
- **Scalable for batch jobs** – döngü içinde onlarca dosyayı minimum ek yükle yükleyip kaydedebilirsiniz.

## Önkoşullar
İlerlemeye başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Aspose.CAD Library** – [buradan](https://releases.aspose.com/cad/java/) indirin.  
- **Document Directory** – giriş DGN dosyalarının ve çıktı PDF'lerin bulunacağı bilgisayarınızdaki bir klasör.

## Paketleri İçe Aktar
Java projenizde, Aspose.CAD işlevlerine erişmek için gerekli paketleri içe aktarın:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Şimdi, örnek kodu birden fazla adıma ayıralım:

## Adım 1: Dosya Yollarını Tanımla (dgn nasıl dışa aktarılır)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

`Your Document Directory` ifadesini dosyalarınızın bulunduğu gerçek yol ile değiştirdiğinizden emin olun.

## Adım 2: DGN Görüntüsünü Yükle

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Aspose.CAD kullanarak DGN dosyasını yükleyin.

## Adım 3: PDF Dışa Aktarım Seçeneklerini Ayarla (pdf boyutunu özelleştir, pdf seçeneklerini ayarla)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Burada PDF dışa aktarım seçeneklerini tanımlıyoruz; sayfa boyutları, otomatik ölçekleme ve son PDF'ye dahil etmek istediğiniz belirli DGN düzenleri (görünümler) yer alıyor.

## Adım 4: PDF Dosyasını Kaydet

```java
objImage.save(outFile, options);
```

Dışa aktarılan PDF dosyasını kaydedin. `save` metodu, bir önceki adımda yapılandırdığınız tüm seçenekleri uygular.

Dönüştürmek istediğiniz ek DGN dosyaları için bu adımları tekrarlayın. Tebrikler! Aspose.CAD for Java kullanarak DGN dosyalarını AutoCAD formatında PDF'ye dışa aktararak **convert CAD PDF** işlemini başarıyla gerçekleştirdiniz.

## Yaygın Sorunlar ve Çözümler
| Sorun | Neden Oluşur | Çözüm |
|-------|----------------|-----|
| **File not found** | Yanlış `dataDir` yolu | Klasör yolunu tekrar kontrol edin ve DGN dosyasının mevcut olduğundan emin olun. |
| **Blank pages in PDF** | `AutomaticLayoutsScaling` `false` olarak ayarlanmış veya eksik düzen kimlikleri | `setAutomaticLayoutsScaling(true)` tutun ve düzen adlarını (`"1","2",…`) doğrulayın. |
| **Low‑resolution output** | Varsayılan rasterleştirme DPI'si düşük | Kaliteyi artırmak için `vectorOptions.setResolution(300);` kullanın (`setVectorRasterizationOptions`'dan önce ekleyin). |
| **License exception** | Üretimde geçerli bir lisans olmadan çalıştırmak | Aspose belgelerinde açıklandığı gibi geçici veya satın alınmış bir lisans uygulayın. |

## Sıkça Sorulan Sorular (Ek)

**S: Çoklu‑düzen DGN dosyasından yalnızca tek bir düzeni dışa aktarabilir miyim?**  
C: Evet – istenen düzen kimliklerini `vectorOptions.setLayouts(new String[] { "2" });` içinde belirtebilirsiniz.

**S: Oluşan PDF'ye fontları gömmek mümkün mü?**  
C: Aspose.CAD, vektör verileri rasterleştirildiğinde gerekli fontları otomatik olarak gömer; gerektiğinde `PdfOptions` aracılığıyla font gömme kontrolü de yapabilirsiniz.

**S: Birçok DGN dosyasını toplu olarak nasıl işleyebilirim?**  
C: Adımları, dosya adları listesini yineleyen bir `for` döngüsü içinde sarın ve her yineleme için aynı `PdfOptions` örneğini yeniden kullanın.

**S: Kütüphane şifre korumalı PDF'leri destekliyor mu?**  
C: Evet – `PdfOptions` nesnesine `options.setPassword("yourPassword");` ile bir şifre atayabilirsiniz.

**S: Daha fazla örnek nerede bulunabilir?**  
C: Resmi Aspose.CAD dokümantasyonu ve örnek deposu birçok ek senaryo içerir.

## SSS'ler (Orijinal)

### Q1: Aspose.CAD tüm CAD dosya formatlarıyla uyumlu mu?
A1: Evet, Aspose.CAD geniş bir CAD formatı yelpazesini destekler, çeşitli dosya türlerini işleme konusunda çok yönlülük sağlar.

### Q2: PDF dışa aktarım ayarlarını özelleştirebilir miyim?
A2: Kesinlikle. Öğreticide gösterildiği gibi, sayfa boyutları ve düzenler gibi seçenekleri gereksinimlerinize göre ayarlayabilirsiniz.

### Q3: Ek destek veya yardım nereden bulunur?
A3: Topluluk desteği ve tartışmalar için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

### Q4: Ücretsiz deneme mevcut mu?
A4: Evet, ücretsiz denemeye [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

### Q5: Geçici bir lisans nasıl alınır?
A5: Geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) edinebilirsiniz.

## Sonuç

Bu öğreticide, Aspose.CAD for Java'ı kullanarak **convert CAD PDF** dosyalarını nasıl dönüştüreceğimizi inceledik. Sadece birkaç satır kodla bir DGN çizimini yükleyebilir, PDF dışa aktarım seçeneklerini ince ayar yapabilir ve paylaşım veya arşivleme için yüksek kaliteli PDF'ler oluşturabilirsiniz. Projenizin ihtiyaçlarına göre farklı sayfa boyutları, düzenler veya toplu işleme denemekten çekinmeyin.

---

**Last Updated:** 2026-05-04  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}