---
title: Aspose.CAD for Java Kullanarak Arka Planı Ayarlama ve Çizim Rengi
linktitle: Arka Plan ve Çizim Rengini Ayarlama
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java'yı kullanarak CAD dosyalarını zahmetsizce PDF ve TIFF'e dönüştürün. Görsel olarak etkileyici sonuçlar için özel arka plan ve çizim renkleri ayarlayın.
type: docs
weight: 15
url: /tr/java/advanced-cad-features/setting-background-and-drawing-color/
---
## giriiş

Bilgisayar Destekli Tasarımın (CAD) dinamik dünyasında, verimli dosya dönüştürme, kusursuz işbirliği ve iletişim için çok önemlidir. Aspose.CAD for Java, CAD dosyalarını PDF ve TIFF formatlarına dönüştürmek için güçlü yetenekler sunan güçlü bir araç olarak ortaya çıkıyor. Bu eğitimde, Aspose.CAD for Java'yı kullanarak arka planı ayarlama ve çizim rengini oluşturma sürecini derinlemesine inceleyeceğiz ve size en iyi sonuçları elde etmek için adım adım bir kılavuz sunacağız.

## Önkoşullar

Bu yolculuğa çıkmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

-  Aspose.CAD for Java Library: Aspose.CAD for Java kütüphanesinin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/cad/java/).

-  Belge Dizini: CAD dosyalarınız için özel bir dizine sahip olun. Yer değiştirmek`"Your Document Directory" + "CADConversion/"` dizininizin yolu ile.

Şimdi sürece dalalım.

## Ad Alanlarını İçe Aktar

Aspose.CAD for Java'nın işlevselliklerinden yararlanmak için gerekli ad alanlarını içe aktardığınızdan emin olun. Örneğimizde aşağıdakileri kullanıyoruz:

```java
import java.awt.Color;
import java.awt.Image;

import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Adım 1: CAD Dosyasını Yükleyin

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(srcFile);
```

## Adım 2: Arka Planı ve Çizim Rengini Ayarlayın

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBeige());
rasterizationOptions.setDrawType(CadDrawTypeMode.UseDrawColor);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBlue());
```

## 3. Adım: PDF Oluşturun ve Kaydedin

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

## 4. Adım: TIFF Oluşturun ve Kaydedin

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Aspose.CAD for Java'yı kullanarak CAD'den PDF'ye ve TIFF dönüşümünde en iyi sonuçları elde etmek için bu adımları özenle izleyin.

## Çözüm

Aspose.CAD for Java, geliştiricilere CAD dosyası manipülasyonu için çok yönlü bir araç seti sağlar. Arka plan ve çizim rengini ayarlamanın inceliklerinde ustalaşarak, görsel olarak çekici ve doğru dönüşümler üretme yeteneğinizi geliştirirsiniz.

## SSS'ler

### S1: Aspose.CAD for Java toplu dönüşümler için uygun mudur?

A1: Kesinlikle! Aspose.CAD for Java, toplu dönüştürmelerde üstünlük sağlayarak verimlilik ve doğruluk sağlar.

### S2: Oluşturulan dosyalardaki arka plan rengini özelleştirebilir miyim?

Cevap2: Evet, eğitimde hem PDF hem de TIFF çıktıları için özel arka plan renklerinin nasıl ayarlanacağı gösterilmektedir.

### S3: Aspose.CAD for Java'nın kapsamlı belgelerini nerede bulabilirim?

 A3: Bkz.[dokümantasyon](https://reference.aspose.com/cad/java/) derinlemesine bilgiler ve örnekler için.

### S4: Ücretsiz deneme sürümü mevcut mu?

 A4: Evet, özellikleri şu şekilde keşfedin:[ücretsiz deneme](https://releases.aspose.com/).

### S5: Aspose.CAD for Java desteğini nasıl alabilirim?

A5: ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) yardım istemek ve toplulukla etkileşime geçmek.
