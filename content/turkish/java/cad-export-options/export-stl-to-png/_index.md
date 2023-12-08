---
title: Aspose.CAD for Java ile STL'yi PNG'ye aktarın
linktitle: STL'yi PNG'ye aktar
second_title: Aspose.CAD Java API'si
description: Aspose.CAD ile STL dosyalarını Java'da PNG'ye aktarmanın kusursuz sürecini keşfedin. İş akışınızı basitleştirin ve Java projelerinizi zahmetsizce geliştirin.
type: docs
weight: 20
url: /tr/java/cad-export-options/export-stl-to-png/
---
## giriiş

Java kullanarak STL dosyalarını PNG'ye aktarmak mı istiyorsunuz? Aspose.CAD for Java ihtiyacınız olan çözüm! Bu eğitimde size süreç boyunca adım adım rehberlik edeceğiz. Uzman bir SEO yazarı olarak içeriğin yalnızca bilgilendirici olmasını değil aynı zamanda arama motorları için optimize edilmesini de sağlayacağım.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Makinenizde Java Geliştirme Kiti (JDK) yüklü.
-  Aspose.CAD for Java kütüphanesi indirildi. Alabilirsin[Burada](https://releases.aspose.com/cad/java/).
-  Geçerli bir lisans veya geçici bir lisans[Burada](https://purchase.aspose.com/temporary-license/).

## Ad Alanlarını İçe Aktar

Java projenizde gerekli ad alanlarını içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Şimdi örneği birden çok adıma ayıralım.

## 1. Adım: Projenizi Kurun

Yeni bir Java projesi oluşturun ve Aspose.CAD for Java kütüphanesini projenizin bağımlılıklarına ekleyin.

## Adım 2: STL Dosyanızı Belirleyin

STL dosyanızın yolunu tanımlayın. Örneğin:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## Adım 3: STL Dosyasını Yükleyin

 STL dosyasını kullanarak yükleyin.`Image.load` yöntem:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## Adım 4: Rasterleştirme Seçeneklerini Yapılandırın

Vektörleştirme için rasterleştirme seçeneklerini ayarlayın:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## Adım 5: PNG Seçeneklerini Yapılandırın

PNG dışa aktarma seçeneklerini belirtin:

```java
PngOptions pngOptions = new PngOptions();
// Vektör rasterleştirme seçeneklerini ayarlamak istiyorsanız aşağıdaki satırın açıklamasını kaldırın
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## Adım 6: PNG olarak kaydedin

CAD görüntüsünü PNG dosyası olarak kaydedin:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

Tebrikler! Aspose.CAD for Java'yı kullanarak bir STL dosyasını başarıyla PNG'ye aktardınız.

## Çözüm

Bu eğitimde, STL dosyalarını PNG'ye zahmetsizce aktarmak için Aspose.CAD for Java'dan nasıl yararlanılacağını araştırdık. Bu güçlü kitaplık, karmaşık görevleri basitleştirerek onu Java projeleriniz için değerli bir varlık haline getirir.

## SSS'ler

### S1: Aspose.CAD for Java tüm STL dosya sürümleriyle uyumlu mudur?

Cevap1: Aspose.CAD for Java, çeşitli STL dosya sürümlerini destekleyerek en yaygın formatlarla uyumluluk sağlar.

### S2: Aspose.CAD for Java'yı ticari bir projede kullanabilir miyim?

 A2: Evet, yapabilirsin. Geçerli bir lisans almanız yeterli[Burada](https://purchase.aspose.com/buy).

### S3: Ücretsiz deneme için geçici bir lisansa ihtiyacım var mı?

 C3: Hayır, ücretsiz deneme için geçici lisansa gerek yoktur. Deneme sürümüne hemen başlayabilirsiniz[Burada](https://releases.aspose.com/).

### S4: Nerede ek destek bulabilirim veya soru sorabilirim?

 Cevap4: Aspose.CAD forumunu ziyaret edin[Burada](https://forum.aspose.com/c/cad/19) herhangi bir destek veya sorularınız için.

### S5: Kapsamlı bir belge mevcut mu?

 A5: Evet, belgeler bulunabilir[Burada](https://reference.aspose.com/cad/java/).