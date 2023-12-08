---
title: Java'da Aspose.CAD ile Belirli DXF Düzenini Görüntüye Aktarın
linktitle: Belirli DXF Düzenini Java ile Görüntüye Aktarma
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java kullanarak belirli bir DXF düzenini bir görüntüye nasıl aktaracağınızı öğrenin. Sorunsuz entegrasyon için adım adım kılavuzumuzu izleyin.
type: docs
weight: 16
url: /tr/java/additional-features/export-specific-layout-to-image/
---
## giriiş

Belirli bir DXF düzenini Java kullanarak bir görüntüye dönüştürmek mi istiyorsunuz? Aspose.CAD for Java ile bu görevi sorunsuz bir şekilde gerçekleştirebilirsiniz. Bu adım adım kılavuzda, her aşama için net talimatlar ve örnekler sunarak belirli bir DXF düzenini bir görüntüye aktarma sürecinde size yol göstereceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.CAD for Java: Aspose.CAD for Java kütüphanesinin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/cad/java/).

## Ad Alanlarını İçe Aktar

Başlamak için gerekli ad alanlarını Java projenize aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.fileformats.dwf.whip.objects.DwfWhipLayer;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dwf.DwfImage;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

Şimdi her adımı ayrıntılı olarak ele alalım.

## 1. Adım: Kaynak Dizinini Ayarlayın

Java projenizdeki kaynak dizininin yolunu tanımlayın. Bu dizin dönüştürmek istediğiniz DXF çizimini içermelidir.

```java
String dataDir = "Your Document Directory" + "DXFDrawings\\";
```

"Belge Dizininiz"i gerçek yolla değiştirdiğinizden emin olun.

## Adım 2: DXF Görüntüsünü Yükleyin

Aspose.CAD kütüphanesini kullanarak DXF görüntüsünü yükleyin.

```java
String srcFile = dataDir + "for_layers_test.dwf";
DwfImage image = (DwfImage) Image.load(srcFile);
```

"for_layers_test.dwf" ifadesini DXF dosyanızın adıyla değiştirin.

## 3. Adım: Katman Adlarını Alın

DXF görüntüsünde bulunan katmanların adlarını alın.

```java
List<String> layersNames = image.getLayers().getLayersNames();
```

Bu adım, mevcut katmanların bir listesine sahip olmanızı sağlar.

## Adım 4: Rasterleştirme Seçeneklerini Ayarlayın

 Bir örneğini oluşturun`CadRasterizationOptions` ve sayfa genişliği ve yüksekliği gibi gerekli özellikleri ayarlayın.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

Sayfa boyutlarını gereksinimlerinize göre ayarlayın.

## Adım 5: Katmanları Belirleyin

Katman adları listesini rasterleştirme seçeneklerine uygun bir formata dönüştürün.

```java
String[] stringArray = Arrays.copyOf(layersNames.toArray(), layersNames.toArray().length, String[].class);
List<String> stringList = Arrays.asList(stringArray);
rasterizationOptions.setLayers(stringList);
```

Bu adım, dışa aktarma işlemine yalnızca istediğiniz katmanları dahil etmenizi sağlar.

## Adım 6: JPEG Seçeneklerini Yapılandırın

 Bir örneğini oluşturun`JpegOptions` ve vektör rasterleştirme seçeneklerini ayarlayın.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Bu, görüntüyü JPEG formatında kaydetme seçeneklerini hazırlar.

## Adım 7: DXF'yi Görüntüye Aktarın

Çıkış yolunu belirtin ve DXF görüntüsünü JPEG olarak kaydedin.

```java
String output = dataDir + "for_layers_test.jpg";
image.save(output, jpegOptions);
```

Çıkış yolunu ve dosya adını tercihlerinize göre ayarlayın.

Bu adımlarla, Aspose.CAD for Java kullanarak belirli bir DXF düzenini başarıyla bir görüntüye aktardınız.

## Çözüm

Bu eğitimde, Aspose.CAD for Java kullanarak belirli bir DXF düzenini bir görüntüye aktarma sürecini ele aldık. Ayrıntılı adımları izleyerek ve verilen kod parçacıklarını kullanarak bu işlevselliği Java projelerinize sorunsuz bir şekilde entegre edebilirsiniz.

## SSS'ler

### S1: Birden fazla DXF düzenini tek seferde dışa aktarabilir miyim?

C1: Evet, birden çok düzeni işleyecek şekilde, bunlar arasında yineleyerek ve her birini ayrı ayrı dışa aktararak kodu değiştirebilirsiniz.

### S2: Aspose.CAD for Java farklı Java sürümleriyle uyumlu mudur?

Cevap2: Aspose.CAD for Java, çeşitli Java sürümleriyle uyumlu olacak şekilde tasarlanmıştır. Belirli uyumluluk ayrıntıları için belgelere bakın.

### S3: DXF'den görüntüye dönüştürme işlemi sırasındaki hataları nasıl halledebilirim?

Cevap 3: Dönüştürme sırasında oluşabilecek olası istisnaları yakalamak ve yönetmek için try-catch bloklarını kullanarak hata işlemeyi uygulayabilirsiniz.

### S4: JPEG dışında desteklenen başka çıktı formatları var mı?

Cevap4: Evet, Aspose.CAD for Java PNG, BMP, TIFF ve daha fazlası dahil olmak üzere çeşitli çıktı formatlarını destekler. Kodu buna göre ayarlayabilirsiniz.

### S5: Rasterleştirme seçeneklerini daha da özelleştirebilir miyim?

 A5: Kesinlikle,`CadRasterizationOptions` sınıf özelleştirme için çeşitli özellikler sağlar. Ek seçenekler için belgeleri inceleyin.