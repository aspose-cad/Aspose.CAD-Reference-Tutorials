---
title: CAD Çizimlerine Filigran Ekleme - Aspose.CAD for Java Eğitimi
linktitle: Filigran ekle
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java'yı kullanarak CAD çizimlerinizi kişiselleştirilmiş filigranlarla geliştirin. Sorunsuz entegrasyon için adım adım kılavuzumuzu izleyin.
type: docs
weight: 12
url: /tr/java/other-cad-operations/add-watermark/
---
## giriiş

Aspose.CAD for Java kullanarak CAD çizimlerine filigran eklemeye ilişkin bu kapsamlı kılavuza hoş geldiniz. Bu eğitimde, filigranları verimli bir şekilde nasıl entegre edeceğinizi, CAD belgelerinizi kişiselleştirilmiş mesajlarla veya markalamayla nasıl geliştireceğinizi öğreneceksiniz. Aspose.CAD for Java, filigran ekleme sürecini kolaylaştıran güçlü bir dizi özellik sunar.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

-  Aspose.CAD for Java: Java ortamınızda Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/cad/java/).
- Java Geliştirme Kiti (JDK): Sisteminizde JDK'nın en son sürümünün yüklü olduğundan emin olun.

## Paketleri İçe Aktar

Başlamak için Java projenize gerekli Aspose.CAD paketlerini içe aktarın:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 1. Adım: Yeni MTEXT Ekleyin

```java
//yeni MTEXT ekle
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Adım 2: Metin Gibi Basit Varlık Ekleme

Ayrıca metin gibi daha basit bir varlık da ekleyebilirsiniz:

```java
// veya Metin gibi daha basit bir varlık ekleyin
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## 3. Adım: PDF'ye aktarın

Eklenen filigranı içeren CAD çizimini bir PDF dosyasına aktarın:

```java
// pdf'e aktar
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Çözüm

Tebrikler! Aspose.CAD for Java'yı kullanarak CAD çizimlerinize filigranları başarıyla eklediniz. Bu basit ama güçlü süreç, tasarımlarınızı kişiselleştirmenize veya markalamayla korumanıza olanak tanır.

## SSS'ler

### S1: Aspose.CAD tüm CAD dosya formatlarıyla uyumlu mudur?

Cevap1: Aspose.CAD, DWG, DXF, DWT ve DWF dahil olmak üzere çeşitli CAD formatlarını destekler.

### S2: Filigran metninin görünümünü özelleştirebilir miyim?

C2: Evet, metin boyutu, renk ve konum da dahil olmak üzere filigranın görünümü üzerinde tam kontrole sahipsiniz.

### S3: Aspose.CAD for Java'nın deneme sürümü mevcut mu?

 A3: Evet, deneme sürümünü indirebilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.CAD için nasıl destek alabilirim?

 A4: Ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği için.

### S5: Aspose.CAD for Java belgelerinin tamamını nerede bulabilirim?

 A5: Bkz.[dokümantasyon](https://reference.aspose.com/cad/java/) detaylı bilgi için.