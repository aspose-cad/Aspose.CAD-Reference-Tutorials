---
title: Aspose.CAD for Java Kullanarak CAD Katmanını Raster Görüntü Formatına Dönüştürün
linktitle: CAD Katmanını Raster Görüntü Formatına Dönüştür
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java ile CAD katmanlarını zahmetsizce raster görüntülere nasıl dönüştüreceğinizi öğrenin. Sorunsuz belge görselleştirmesi için adım adım kılavuzumuzu izleyin.
type: docs
weight: 11
url: /tr/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
---
## giriiş

Bilgisayar Destekli Tasarım (CAD) alanında, CAD katmanlarını sorunsuz bir şekilde raster görüntü formatlarına dönüştürme yeteneği, belge manipülasyonu ve görselleştirmenin çok önemli bir yönüdür. Aspose.CAD for Java, bu dönüştürme sürecini kolaylaştırmak için sayısız işlevsellik sunan güçlü bir araç olarak ortaya çıkıyor. Bu adım adım kılavuz süreç boyunca size yol gösterecek ve Aspose.CAD for Java'nın tüm potansiyelinden yararlanmanızı sağlayacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Java Geliştirme Ortamı: Makinenizde bir Java geliştirme ortamının kurulu olduğundan emin olun.

-  Aspose.CAD Kütüphanesi: Java için Aspose.CAD kütüphanesini şuradan indirip yükleyin:[İndirme: {link](https://releases.aspose.com/cad/java/).

## Ad Alanlarını İçe Aktar

Bu adımda süreci başlatmak için gerekli ad alanlarını içe aktaracağız.

### Aspose.CAD Sınıflarını İçe Aktar

Aşağıdaki içe aktarma ifadelerini kullanarak Aspose.CAD sınıflarını Java kodunuza ekleyin:

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## CAD Katmanını Raster Görüntü Formatına Dönüştür

Şimdi sorunsuz bir dönüşüm süreci sağlamak için öğreticiyi birden fazla adıma ayıralım.

### Adım 1: CAD Dosyasını Ayarlayın

CAD dosyanızın yolunu belirleyip onu Image sınıfının bir örneğine yükleyerek başlayın.

```java
// Kaynak dizininin yolu.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Adım 2: Rasterleştirme Seçeneklerini Yapılandırın

Rasterleştirme ayarlarını tanımlamak için bir CadRasterizationOptions örneği oluşturun.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### Adım 3: CAD Katmanlarını Belirleyin

İstediğiniz CAD katmanını/katmanlarını rasterleştirme seçeneklerine ekleyin.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### 4. Adım: JPEG Seçeneklerini Ayarlayın

JpegOptions'ın (veya raster formatları için herhangi bir ImageOptions'ın) bir örneğini oluşturun ve bunu CadRasterizationOptions'a bağlayın.

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### 5. Adım: JPEG'e aktarın

Son olarak, her katmanı JPEG formatına aktarın.

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

Ek katmanlar için bu adımları tekrarlayın veya ayarları gereksinimlerinize göre özelleştirin.

## Çözüm

Bu kapsamlı kılavuzu takip ederek Aspose.CAD for Java'nın CAD katmanlarını taramalı görüntü formatlarına dönüştürme yeteneklerinden başarıyla yararlandınız. Bu araç, belge görselleştirmesini ve manipülasyonunu kolaylıkla geliştirmenizi sağlar.

## SSS'ler

### S1: Aspose.CAD for Java'yı diğer programlama dilleriyle birlikte kullanabilir miyim?

Cevap1: Aspose.CAD öncelikle Java'yı destekler ancak .NET gibi diğer diller için de versiyonlar mevcuttur.

### S2: Nerede ek destek veya yardım bulabilirim?

 A2: Sorularınız veya yardım için şu adresi ziyaret edin:[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19).

### S3: Ücretsiz deneme sürümü mevcut mu?

 C3: Evet, Aspose.CAD'i ücretsiz deneme sürümünü edinerek keşfedebilirsiniz.[Burada](https://releases.aspose.com/).

### S4: Aspose.CAD için nasıl geçici lisans alabilirim?

 Cevap4: Geçici bir lisans edinin[bu bağlantı](https://purchase.aspose.com/temporary-license/).

### S5: Aspose.CAD for Java'ya özel sistem gereksinimleri var mı?

Cevap5: Uyumlu bir Java geliştirme ortamına sahip olduğunuzdan emin olun; ayrıntılı gereksinimler için belgelere bakın.