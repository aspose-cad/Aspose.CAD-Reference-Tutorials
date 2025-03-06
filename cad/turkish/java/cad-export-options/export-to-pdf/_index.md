---
title: Aspose.CAD for Java ile PDF'ye aktarın
linktitle: PDF'ye aktar
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java ile CAD dosyalarını zahmetsizce PDF'ye nasıl aktaracağınızı öğrenin. Sorunsuz entegrasyon için adım adım kılavuzumuzu izleyin.
weight: 13
url: /tr/java/cad-export-options/export-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java ile PDF'ye aktarın

## giriiş

Aspose.CAD for Java kullanarak CAD dosyalarını PDF'ye aktarmaya ilişkin bu kapsamlı eğitime hoş geldiniz. CAD çizimlerinizi sorunsuz bir şekilde yaygın olarak desteklenen PDF formatına dönüştürmek istiyorsanız doğru yerdesiniz. Bu adım adım kılavuzda, başarılı bir PDF dışa aktarımı elde etmek için her adımı anlamanızı sağlayacak şekilde süreci ayrıntılı olarak anlatacağız.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

-  Aspose.CAD for Java: Java ortamınızda Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/cad/java/).

- Kaynak Dizini: CAD dosyalarınızın depolandığı bir dizin ayarlayın. Sağlanan kod pasajındaki "Belge Dizininiz"i gerçek yolla değiştirin.

Şimdi ana adımlara geçelim.

## Ad Alanlarını İçe Aktar

Aspose.CAD işlevlerinin kullanımını etkinleştirmek için Java projenizde gerekli ad alanlarını içe aktararak başlayın.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//com.aspose.cad.imageoptions.TypeOfEntities'i içe aktar;
```

## Adım 1: CAD Dosyasını Yükleyin

CAD dosyanızı Aspose.CAD Image nesnesine yükleyin. "site.dwf"yi gerçek CAD dosya adınızla değiştirin.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## 2. Adım: PDF Seçeneklerini Yapılandırın

Sayfa yüksekliği, genişlik ve düzenler gibi vektör rasterleştirme seçenekleri de dahil olmak üzere PDF dışa aktarma seçeneklerini ayarlayın.

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## 3. Adım: PDF'ye aktarın

Oluşturulan PDF dosyası için çıktı yolunu belirtin ve görüntüyü yapılandırılmış PDF seçenekleriyle kaydedin.

```java
String outPath = dataDir + "site.pdf";
image.save(outPath, pdfOptions);
```

Tebrikler! Aspose.CAD for Java'yı kullanarak CAD dosyanızı başarıyla PDF'ye aktardınız.

## Çözüm

Bu eğitimde, Aspose.CAD for Java kullanarak CAD dosyalarını PDF'ye aktarmanın adım adım sürecini inceledik. Bu basit ama etkili adımları izleyerek bu işlevselliği Java uygulamalarınıza sorunsuz bir şekilde entegre edebilirsiniz.

## SSS'ler

### S1: Aspose.CAD tüm CAD dosya formatlarıyla uyumlu mudur?

Cevap1: Evet, Aspose.CAD çok çeşitli CAD formatlarını destekleyerek çeşitli tasarım yazılımlarıyla uyumluluk sağlar.

### S2: PDF çıktı ayarlarını özelleştirebilir miyim?

A2: Kesinlikle. Öğretici, özelleştirme seçeneklerine kısa bir bakış sağlar, ancak çıktıyı ihtiyaçlarınıza göre uyarlamak için daha fazlasını keşfedebilirsiniz.

### S3: Aspose.CAD için ek desteği nerede bulabilirim?

 C3: Her türlü soru veya sorun için şu adresi ziyaret edin:[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) toplumdan yardım istemek.

### S4: Ücretsiz deneme sürümü mevcut mu?

 Cevap4: Evet, Aspose.CAD'in ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S5: Aspose.CAD için nasıl geçici lisans alabilirim?

 Cevap5: Geçici lisanslama için şu adresi ziyaret edin:[bu bağlantı](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
