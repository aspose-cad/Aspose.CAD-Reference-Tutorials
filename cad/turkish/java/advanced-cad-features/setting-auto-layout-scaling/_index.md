---
title: Aspose.CAD for Java ile Otomatik Mizanpaj Ölçeklendirmesini Ayarlama
linktitle: Otomatik Düzen Ölçeklendirmeyi Ayarlama
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java ile CAD iş akışınızı geliştirin. Bu adım adım kılavuzda, optimum görüntü ve verimlilik sağlayan Otomatik Düzen Ölçeklendirme tanıtılmaktadır. Kütüphaneyi indirin, öğreticiyi takip edin ve CAD projelerinizde devrim yaratın.
type: docs
weight: 17
url: /tr/java/advanced-cad-features/setting-auto-layout-scaling/
---
## giriiş

Bilgisayar destekli tasarımın (CAD) dinamik dünyasında verimlilik çok önemlidir. Aspose.CAD for Java, CAD iş akışınızı geliştirmek için güçlü bir araç seti sağlar. Öne çıkan özelliklerden biri, düzenlerinizin en iyi görüntü için kusursuz bir şekilde ayarlanmasını sağlayan bir işlevsellik olan Otomatik Düzen Ölçeklendirme'dir. Bu eğitimde, Aspose.CAD for Java'yı kullanarak Otomatik Mizanpaj Ölçeklendirmenin adım adım nasıl uygulanacağını keşfedeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

1.  Aspose.CAD for Java Library: Aspose.CAD for Java kütüphanesinin kurulu olduğundan emin olun. Değilse, adresinden indirebilirsiniz.[indirme sayfası](https://releases.aspose.com/cad/java/).

2.  Kaynak Dizini: CAD belgelerinizi depolamak için bir dizin ayarlayın. Yer değiştirmek`"Your Document Directory"` sağlanan kod pasajındaki gerçek yolla.

3. CAD Dosyası: Test için hazır bir CAD dosyası bulundurun. Bu eğitimde "conic_pyramid.dxf" adlı örnek bir dosya kullanacağız.

## Ad Alanlarını İçe Aktar

Aspose.CAD işlevselliği için gerekli ad alanlarını Java kodunuza aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Adım 1: CAD Dosyasını Yükleyin

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Adım 2: Rasterleştirme Seçenekleri Oluşturun

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## 3. Adım: Otomatik Düzen Ölçeklendirmesini Ayarlayın

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## 4. Adım: PDF Seçenekleri Oluşturun

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 5. Adım: PDF'ye aktarın

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Otomatik Düzen Ölçeklendirmenin CAD projelerinize kusursuz entegrasyonu için bu adımları tekrarlayın.

## Çözüm

Aspose.CAD for Java, Otomatik Düzen Ölçeklendirmenin uygulanmasını basitleştirerek CAD düzenlerinizin uyarlanabilirliğini artırır. Bu adım adım kılavuzu takip ederek bu özelliği projelerinize sorunsuz bir şekilde entegre ederek optimum görüntü ve verimliliği sağlayabilirsiniz.

## SSS'ler

### S1: Aspose.CAD for Java tüm CAD dosya formatlarıyla uyumlu mudur?

Cevap1: Aspose.CAD for Java, DWG, DXF ve DWF dahil olmak üzere çeşitli CAD formatlarını destekler.

### S2: Ölçeklendirme seçeneklerini daha da özelleştirebilir miyim?

 A2: Evet,`CadRasterizationOptions` class, ölçeklendirmenin ve diğer ayarların ince ayarı için çeşitli özellikler sağlar.

### S3: Aspose.CAD for Java için ek belgeleri nerede bulabilirim?

 A3: Bkz.[dokümantasyon](https://reference.aspose.com/cad/java/) Ayrıntılı bilgi ve örnekler için.

### S4: Aspose.CAD for Java'nın ücretsiz deneme sürümü mevcut mu?

 A4: Evet, keşfedebilirsiniz[ücretsiz deneme](https://releases.aspose.com/) Aspose.CAD for Java'nın yeteneklerini deneyimlemek için.

### S5: Aspose.CAD for Java hakkında nasıl yardım isteyebilirim veya tartışmalara nasıl katılabilirim?

A5: ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) toplulukla bağlantı kurmak ve destek aramak.