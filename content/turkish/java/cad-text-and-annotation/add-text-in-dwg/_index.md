---
title: Aspose.CAD for Java Kullanarak DWG'ye Metin Ekleme
linktitle: DWG'ye Metin Ekle
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java ile DWG çizimlerinizi zahmetsizce geliştirin. Adım adım kılavuzumuzla sorunsuz bir şekilde metin ekleyin.
type: docs
weight: 10
url: /tr/java/cad-text-and-annotation/add-text-in-dwg/
---
## giriiş

Bilgisayar destekli tasarım (CAD) alanında Aspose.CAD for Java, DWG çizimlerini değiştirmek ve dönüştürmek için güçlü bir araç olarak öne çıkıyor. Kullanışlı özelliklerinden biri, DWG dosyalarına sorunsuz bir şekilde metin ekleyebilme yeteneğidir. Bu eğitimde, Aspose.CAD for Java'yı kullanarak DWG çizimlerinize metin ekleme sürecinde size rehberlik edeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.CAD for Java Library: Kütüphaneyi şuradan indirip yükleyin:[Aspose.CAD for Java sayfası](https://releases.aspose.com/cad/java/).

- Java Geliştirme Kiti (JDK): Sisteminizde en son JDK'nın kurulu olduğundan emin olun.

- DWG Çizimi: Metin eklemek istediğiniz yere bir DWG çizim dosyası hazırlayın.

## Ad Alanlarını İçe Aktar

Aspose.CAD için gerekli ad alanlarını Java kodunuzda içe aktarın:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Şimdi sağlanan kod pasajını birden çok adıma ayıralım:

## 1. Adım: Belge Dizinini ve DWG Dosya Yolunu Ayarlayın

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Adım 2: DWG Görüntüsünü Yükleyin

```java
Image image = Image.load(dwgPathToFile);
```

## Adım 3: CadText Nesnesi Oluşturun

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);
cadText.setScaleX(0);
```

## Adım 4: CadImage'a Metin Ekleme

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Adım 5: PDF Seçeneklerini Ayarlayın

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Adım 6: CadRasterizationOptions'ı yapılandırın

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Adım 7: Değiştirilen DWG'yi PDF olarak kaydedin

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Bu adımları izleyerek Aspose.CAD for Java'yı kullanarak DWG çizimlerinize sorunsuz bir şekilde metin ekleyebileceksiniz.

## Çözüm

Aspose.CAD for Java, geliştiricilerin DWG çizimlerini programlı olarak geliştirmelerine ve değiştirmelerine olanak tanır. Bu eğitim, Aspose.CAD'in basitliğini ve gücünü sergileyen, DWG dosyalarınıza metin ekleme konusunda adım adım anlaşılır bir kılavuz sağladı.

## SSS'ler

### S1: Aspose.CAD, DWG dosyalarının tüm sürümleriyle uyumlu mudur?

Cevap1: Aspose.CAD, DWG dosyalarının çeşitli versiyonlarını destekleyerek geniş bir CAD yazılımı yelpazesiyle uyumluluk sağlar.

### S2: Eklenen metnin yazı tipini ve formatını özelleştirebilir miyim?

Cevap2: Evet, Aspose.CAD'i kullanarak DWG dosyalarına eklenen metnin yazı tipini, stilini ve diğer formatlama seçeneklerini özelleştirebilirsiniz.

### S3: Aspose.CAD for Java'nın ücretsiz deneme sürümü mevcut mu?

 C3: Evet, Aspose.CAD'in özelliklerini ücretsiz deneme sürümünü edinerek keşfedebilirsiniz.[Burada](https://releases.aspose.com/).

### S4: Aspose.CAD for Java'nın ayrıntılı belgelerini nerede bulabilirim?

 Cevap4: Belgelere bakın[Burada](https://reference.aspose.com/cad/java/) Ayrıntılı bilgi ve örnekler için.

### S5: Aspose.CAD ile nasıl destek alabilirim veya yardım alabilirim?

A5: ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) yardım almak ve toplulukla bağlantı kurmak için.