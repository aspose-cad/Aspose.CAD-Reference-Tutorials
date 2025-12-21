---
date: 2025-12-21
description: Aspose.CAD for Java kullanarak belirli bir DWG düzenini PDF'ye dışa aktararak
  DWG'yi PDF'ye nasıl dönüştüreceğinizi öğrenin. CAD iş akışınızı hızlandırmak için
  bu adım adım DWG'den PDF'ye öğreticisini izleyin.
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: DWG'yi PDF'ye Dönüştür – Aspose.CAD for Java ile Düzeni Dışa Aktar
url: /tr/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi PDF'ye Dönüştür – Aspose.CAD for Java Kullanarak Belirli Düzeni Dışa Aktar

## Giriş

Bilgisayar Destekli Tasarım (CAD) dünyasının dinamik ortamında, **convert DWG to PDF** (DWG'yi PDF'ye dönüştürmek) müşteriler, müteahhitler veya teknik olmayan paydaşlarla çizimleri paylaşırken sıkça ihtiyaç duyulan bir gereksinimdir. Aspose.CAD for Java bu dönüşümü zahmetsiz hâle getirir ve çoklu düzen içeren bir DWG dosyasından tek bir düzen seçmenize bile olanak tanır. Bu öğreticide, **DWG'ye özgü düzenleri** PDF'ye nasıl dışa aktaracağınızı adım adım göstereceğiz, böylece projenizin tam olarak ihtiyacı olanı ekstra sayfalar veya manuel kırpma olmadan sunabilirsiniz.

## Hızlı Yanıtlar
- **convert DWG to PDF** ne anlama geliyor? DWG çizimini PDF belgesine dönüştürür, vektör verilerini ve düzen bütünlüğünü korur.  
- **Hangi kütüphane dönüşümü gerçekleştirir?** Aspose.CAD for Java, kullanıma hazır bir API sunar.  
- **Üretim ortamında lisansa ihtiyacım var mı?** Evet, ticari bir lisans gereklidir; değerlendirme için ücretsiz deneme sürümü kullanılabilir.  
- **Tek bir düzen seçebilir miyim?** Kesinlikle – `Layouts` özelliğini istediğiniz düzen adıyla ayarlayın.  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri tamamen uyumludur.

## Ön Koşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- **Java Geliştirme Ortamı** – JDK 8+ ve tercih ettiğiniz IDE.  
- **Aspose.CAD Kütüphanesi** – En son JAR dosyasını resmi siteden **[buradan](https://releases.aspose.com/cad/java/)** indirin.  
- **DWG Dosyası** – En az bir düzen içeren bir çizim (ör. *visualization_-_conference_room.dwg*).  

## Neden Belirli Bir DWG Düzenini PDF'ye Dışa Aktaralım?

Birçok DWG dosyası birden fazla kağıt alanı (düzen) içerir. Tüm dosyayı dışa aktarmak, istenmeyen sayfalarla dolu büyük bir PDF oluşturabilir. Tek bir düzen seçmek:

- Dosya boyutunu azaltır.  
- Görüşmenin dikkatini ilgili çizim sayfasına odaklar.  
- Proje dokümantasyon standartlarıyla uyumlu olur.  

## Adım Adım Kılavuz

### Adım 1: Proje Ortamını Kurun

Yeni bir Java projesi (Maven, Gradle veya basit bir IDE) oluşturun ve Aspose.CAD JAR dosyasını sınıf yolunuza ekleyin. **[Buradan](https://releases.aspose.com/cad/java/)** indirebilirsiniz.

### Adım 2: Gerekli Paketleri İçe Aktarın

Gerekli Aspose.CAD ad alanlarını Java sınıfınıza ekleyin.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Adım 3: DWG Dosyasını Yükleyin

Dönüştürmek istediğiniz DWG dosyasını işaret edin ve bir `Image` nesnesine yükleyin.

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### Adım 4: Rasterizasyon Seçeneklerini Yapılandırın

Sayfa boyutunu ve özellikle dışa aktarmak istediğiniz düzeni tanımlayın.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### Adım 5: PDF Dışa Aktarma Seçeneklerini Ayarlayın

Rasterizasyon ayarlarını PDF dışa aktarıcısına bağlayın.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Adım 6: DWG'yi PDF'ye Dışa Aktarın

Sonucu bir PDF dosyası olarak kaydedin. Çıktı yalnızca **Layout1** içerecek ve temiz bir **convert DWG to PDF** işlemi sağlayacaktır.

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|--------------|-------|
| **Layout not found** | Düzen adı yanlış yazılmış veya DWG içinde mevcut değil. | Mevcut düzenleri listelemek için `image.getLayoutNames()` kullanın, ardından doğru olanı seçin. |
| **Low resolution PDF** | `PageWidth`/`PageHeight` çok küçük. | Boyutları artırın (ör. 2000 × 2000) veya `rasterizationOptions.setResolution(300);` ayarlayın. |
| **License exception** | Deneme dışı bir ortamda geçerli lisans olmadan çalıştırmak. | Görüntüyü yüklemeden önce Aspose.CAD lisansınızı uygulayın: `License license = new License(); license.setLicense("Aspose.CAD.lic");`. |

## Sık Sorulan Sorular

**S1: Aspose.CAD for Java'yı diğer Java tabanlı CAD kütüphaneleriyle kullanabilir miyim?**  
C: Aspose.CAD for Java bağımsız bir kütüphanedir ancak genişletilmiş işlevsellik için diğer Java tabanlı kütüphanelerle entegre edilebilir.

**S2: Aspose.CAD için lisans seçenekleri var mı?**  
C: Evet, lisans seçeneklerini inceleyebilir ve satın alma detaylarını **[buradan](https://purchase.aspose.com/buy)** görebilirsiniz.

**S3: Aspose.CAD için geçici bir lisans nasıl alabilirim?**  
C: Geçici lisans talep etmek için **[bu linki](https://purchase.aspose.com/temporary-license/)** ziyaret edin.

**S4: Aspose.CAD desteğini nereden bulabilirim?**  
C: Herhangi bir soru veya yardım için **[Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19)** ziyaret edin.

**S5: Aspose.CAD için ücretsiz deneme mevcut mu?**  
C: Evet, ücretsiz denemeye **[buradan](https://releases.aspose.com/)** ulaşabilirsiniz.

## Sonuç

Bu **dwg to pdf öğreticisi**'ni izleyerek, artık tek bir düzeni hedefleyerek **convert DWG to PDF** yapmanın güvenilir bir yoluna sahipsiniz. Bu yaklaşım depolamayı tasarruf eder, belge paylaşımını hızlandırır ve CAD iş akışınızı düzenli tutar. Farklı rasterizasyon ayarlarıyla denemeler yapmaktan veya projeniz ilerledikçe birden fazla düzeni tek bir PDF'de birleştirmekten çekinmeyin.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2025-12-21  
**Test Edilen:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose