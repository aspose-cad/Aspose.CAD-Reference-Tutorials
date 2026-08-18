---
date: 2026-03-05
description: Bu adım adım öğreticide, DWG'yi PDF'ye nasıl dışa aktaracağınızı, gizli
  hatları nasıl etkinleştireceğinizi ve Aspose.CAD for Java ile DWG'yi PDF'ye nasıl
  dönüştüreceğinizi öğrenin.
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: DWG'yi Gizli Çizgilerle PDF'ye Dışa Aktar – Aspose.CAD for Java
url: /tr/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi Gizli Çizgilerle PDF'ye Dışa Aktarma – Aspose.CAD for Java

## Giriş

Bu öğreticide, Aspose.CAD for Java kullanarak gizli çizgileri koruyarak **dwg'yi pdf'ye dışa aktarmayı** öğreneceksiniz. **DWG'yi PDF'ye dönüştürmeniz**, **dwg to pdf tutorial**‑stil bir kılavuz oluşturmanız veya sadece **DWG'yi PDF olarak kaydetmeniz** gizli‑çizgi desteğiyle olsun, her adımı sizinle paylaşacağız. Sonunda, herhangi bir Java projesine ekleyebileceğiniz hazır bir çözüm elde edeceksiniz.

## Hızlı Yanıtlar
- **Bu öğreticinin kapsamı nedir?** Aspose.CAD for Java ile DWG'yi PDF'ye dışa aktarırken gizli‑çizgi renderlamasını etkinleştirmek.  
- **Hangi ana işlem gerçekleştirilir?** `export dwg to pdf`.  
- **Lisans gerekli mi?** Test için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.  
- **Önkoşullar nelerdir?** Java geliştirme ortamı, Aspose.CAD for Java kütüphanesi ve DWG dosyaları.  
- **Uygulama ne kadar sürer?** Temel bir kurulum için yaklaşık 10‑15 dakika.

## “export dwg to pdf” nedir?
DWG dosyasını PDF'ye dışa aktarmak, vektör‑tabanlı CAD çizimini katmanları, çizgi tiplerini ve isteğe bağlı gizli‑çizgi renderlamasını koruyarak taşınabilir belge formatına dönüştürür. Bu sayede CAD yazılımı olmayan paydaşlarla CAD tasarımlarını kolayca paylaşabilirsiniz.

## DWG'yi PDF'ye Dışa Aktarırken Gizli Çizgileri Nasıl Etkinleştirirsiniz
Gizli çizgiler, rasterizasyon seçeneklerindeki düzen ayarıyla kontrol edilir. **Model** düzenini seçerek, Aspose.CAD renderlayıcıya gizli kenarları görünmez olarak ele almasını söyler ve 3‑D modelin temiz bir 2‑D temsilini elde edersiniz.

## Dışa Aktarırken neden gizli çizgileri etkinleştirirsiniz?
Gizli çizgiler, karmaşık 3‑D modellerin 2‑D sayfada daha net bir görsel temsilini sağlar; yalnızca görünen kenarlar vurgulanır. Bu, okunabilirliği artırır ve mühendislik dokümantasyonu için sıkça gereklidir.

## Önkoşullar

1. **Aspose.CAD for Java** – Kütüphaneyi resmi siteden [buradan](https://releases.aspose.com/cad/java/) indirin.  
2. **DWG dosyaları** – kaynak DWG çizimlerini bilinen bir dizinde saklayın.  
3. **Java geliştirme ortamı** – JDK 8+ ve tercih ettiğiniz IDE (Eclipse, IntelliJ vb.).  

Şimdi kurulum tamam, koda dalalım.

## Ad Alanlarını İçe Aktarma

CAD görüntüleri ve PDF seçenekleriyle çalışabilmek için gerekli sınıfları içe aktararak başlayın.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Adım 1: Projenizi Kurun

Bir Java projesi oluşturun ve Aspose.CAD JAR dosyasını derleme yolunuza ekleyin. Ardından DWG dosyalarınızı tutan dizini tanımlayın.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro ipucu:** Mutlak bir yol kullanın veya projenizin kaynak klasörüne göre göreceli bir yol yapılandırın.

## Adım 2: DWG Dosyasını Yükleyin

Kaynak DWG dosyasını bir `CadImage` nesnesine yükleyin, böylece üzerinde işlem yapabilirsiniz.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Adım 3: Rasterizasyon Seçeneklerini Yapılandırın

Dahil etmek istediğiniz katmanları seçin ve sayfa boyutunu orijinal çizime göre ayarlayın. Burada, düzeni belirterek gizli‑çizgi renderlamasını etkinleştiriyoruz.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Adım 4: PDF Seçeneklerini Ayarlayın

Aspose.CAD'e vektör verilerini PDF'ye rasterleştirmesini söyleyin, gizli çizgileri gizli tutmak için “Model” düzenini kullanın.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Adım 5: Sonucu Kaydedin

Son olarak, DWG'yi bir PDF dosyası olarak dışa aktarın. Gizli çizgiler, belirlediğiniz düzene göre saygı gösterilecektir.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Yaygın Hata:** Layout'u `"Model"` olarak ayarlamayı unutmak, tüm çizgilerin (gizli olanlar dahil) PDF'de katı görünmesine neden olur.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Nasıl Düzeltilir |
|-------|--------------|-------------------|
| PDF tüm çizgileri katı gösterir | Layout **Model** olarak ayarlanmamış | Kaydetmeden önce `rasterizationOptions.setLayouts(new String[] { "Model" });` çağrıldığından emin olun. |
| Çıktıda katmanlar eksik | Yanlış katman adları | DWG dosyasındaki katman adlarını kontrol edin ve `list` içinde tam olarak eşleştiğinden emin olun. |
| Büyük dosyalarda bellek dışı hatası | Büyük rasterizasyon boyutu | Sayfa boyutlarını küçültün veya mümkünse çizimi parçalara bölerek işleyin. |

## Sıkça Sorulan Sorular

### S1: Aspose.CAD for Java'yi diğer CAD dosya formatlarıyla kullanabilir miyim?
A1: Evet, Aspose.CAD DWG, DXF, DWF ve daha fazlası gibi çeşitli CAD formatlarını destekler.

### S2: Aspose.CAD for Java için ücretsiz deneme mevcut mu?
A2: Evet, ücretsiz denemeyi [burada](https://releases.aspose.com/) bulabilirsiniz.

### S3: Aspose.CAD for Java için desteği nasıl alabilirim?
A3: Topluluk desteği için Aspose.CAD forumunu [burada](https://forum.aspose.com/c/cad/19) ziyaret edin.

### S4: Aspose.CAD for Java için ayrıntılı belgeleri nerede bulabilirim?
A4: Belgeleri [burada](https://reference.aspose.com/cad/java/) bulabilirsiniz.

### S5: Aspose.CAD for Java için geçici lisans satın alabilir miyim?
A5: Evet, geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

### S6: Bu yöntem, başsız sunucu ortamında DWG'yi PDF'ye dönüştürmek için de çalışır mı?
A6: Kesinlikle. Kod yalnızca Aspose.CAD API'sini kullandığı için herhangi bir UI bağımlılığı olmadan çalışır ve sunucu‑tarafı otomasyon için idealdir.

## Sonuç

Artık Aspose.CAD for Java kullanarak gizli‑çizgi desteğiyle **dwg'yi pdf'ye dışa aktarma** için eksiksiz, üretim‑hazır bir yönteme sahipsiniz. Bu yaklaşım, toplu işleme araçlarına, web servislerine veya masaüstü uygulamalara entegre edilerek CAD‑to‑PDF dönüşümünü otomatikleştirebilir.

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}