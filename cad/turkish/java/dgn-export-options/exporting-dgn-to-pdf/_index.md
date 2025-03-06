---
title: Aspose.CAD for Java ile DGN'den AutoCAD PDF'ye Zahmetsiz Dışa Aktarma
linktitle: AutoCAD Formatındaki DGN'yi PDF'ye Aktarma
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java kullanarak DGN dosyalarını AutoCAD formatına PDF olarak aktarmaya ilişkin adım adım kılavuzu keşfedin. Java uygulamanızın CAD işleme yeteneklerini zahmetsizce yükseltin.
weight: 12
url: /tr/java/dgn-export-options/exporting-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java ile DGN'den AutoCAD PDF'ye Zahmetsiz Dışa Aktarma

## giriiş

AutoCAD formatındaki DGN dosyalarını PDF'ye aktarmak için Aspose.CAD for Java'nın kullanılmasıyla ilgili bu kapsamlı eğitime hoş geldiniz. Java uygulamanızın CAD dosyalarını işleme yeteneğini geliştirmek istiyorsanız Aspose.CAD mükemmel bir seçimdir. Bu eğitimde, DGN dosyalarını dışa aktarma sürecinde size adım adım rehberlik edeceğiz.


## Önkoşullar
Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:
-  Aspose.CAD Kütüphanesi: Java için Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/cad/java/).
- Belge Dizini: Giriş ve çıkış dosyalarınızın saklanacağı bir belge dizini ayarlayın.

## Paketleri İçe Aktar

Aspose.CAD işlevlerine erişmek için Java projenize gerekli paketleri içe aktarın:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Şimdi örnek kodu birden çok adıma ayıralım:

## 1. Adım: Dosya Yollarını Tanımlayın

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

"Belge Dizininiz"i dosyalarınızın bulunduğu gerçek yolla değiştirdiğinizden emin olun.

## 2. Adım: DGN Görüntüsünü Yükleyin

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Aspose.CAD'i kullanarak DGN dosyasını yükleyin.

## 3. Adım: PDF Dışa Aktarma Seçeneklerini Ayarlayın

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Belirli görünümleri dışa aktar
options.setVectorRasterizationOptions(vectorOptions);
```

Sayfa boyutları ve düzen tercihleri de dahil olmak üzere PDF dışa aktarma seçeneklerini tanımlayın.

## Adım 4: PDF Dosyasını Kaydet

```java
objImage.save(outFile, options);
```

Dışa aktarılan PDF dosyasını kaydedin.

Dönüştürmek istediğiniz ek DGN dosyaları için bu adımları tekrarlayın. Tebrikler! Aspose.CAD for Java'yı kullanarak DGN dosyalarını başarıyla PDF formatında AutoCAD formatına aktardınız.

## Çözüm

Bu eğitimde, uygulamanızın CAD dosya işleme yeteneklerini geliştirmek için Aspose.CAD for Java'dan nasıl yararlanabileceğinizi araştırdık. Takip edilmesi kolay adımlar ve kod örnekleriyle artık DGN dosyalarını PDF formatında sorunsuz bir şekilde AutoCAD formatına aktarabilirsiniz.

## SSS'ler

### S1: Aspose.CAD tüm CAD dosya formatlarıyla uyumlu mudur?

Cevap1: Evet, Aspose.CAD çok çeşitli CAD formatlarını destekleyerek çeşitli dosya türlerinin işlenmesinde çok yönlülük sağlar.

### S2: PDF dışa aktarma ayarlarını özelleştirebilir miyim?

A2: Kesinlikle. Öğreticide gösterildiği gibi sayfa boyutları ve düzenleri gibi seçenekleri gereksinimlerinize uyacak şekilde ayarlayabilirsiniz.

### S3: Nerede ek destek veya yardım bulabilirim?

 A3: Ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği ve tartışmalar için.

### S4: Ücretsiz deneme sürümü mevcut mu?

 Cevap4: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S5: Geçici lisansı nasıl alabilirim?

 Cevap5: Geçici bir lisans alın[Burada](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
