---
title: Kanvas Boyutunu ve Modunu Ayarlama
linktitle: Kanvas Boyutunu ve Modunu Ayarlama
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java'nın gücünü tuval boyutunu ve modunu ayarlamaya ilişkin adım adım kılavuzumuzla keşfedin. CAD dosyalarını zahmetsizce PDF ve TIFF formatlarına dönüştürün.
type: docs
weight: 16
url: /tr/java/advanced-cad-features/set-canvas-size-and-mode/
---
## giriiş

CAD dönüştürme sürecinizi geliştirmek için Aspose.CAD for Java'nın gücünden yararlanmak mı istiyorsunuz? Bu kapsamlı kılavuz, Aspose.CAD for Java'yı kullanarak tuval boyutunu ve modunu ayarlama adımlarında size yol gösterecektir. İster deneyimli bir geliştirici olun ister yeni başlıyor olun, bu eğitim size ihtiyacınız olan bilgileri sağlayacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

-  Aspose.CAD for Java: Java ortamınızda Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/cad/java/).

- Belge Dizini: CAD dosyalarınızı depolamak için bir belge dizini ayarlayın. Bu dizine eğitim adımlarında başvurulacaktır.

Şimdi adım adım kılavuza başlayalım.

## Ad Alanlarını İçe Aktar

Bu adımda Aspose.CAD projenizi başlatmak için gerekli ad alanlarını içe aktaracağız.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Adım 1: Aspose.CAD Sınıflarını İçe Aktarın

```java
// Kaynak dizininin yolu.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 Bu kod parçasında, kaynak dizininin yolunu ayarlıyoruz ve Aspose.CAD'i kullanarak bir DXF dosyası yüklüyoruz.`Image` sınıf.

## Adım 2: CadRasterizationOptions Özelliklerini Ayarlayın

```java
// Bir CadRasterizationOptions örneği oluşturun ve çeşitli özelliklerini ayarlayın
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Burada bir örneğini oluşturuyoruz`CadRasterizationOptions` ve sayfa genişliği, sayfa yüksekliği ve ölçeklendirme seçenekleri gibi özellikleri yapılandırın.

## 3. Adım: PdfOptions Oluşturun ve VectorRasterizationOptions'ı Ayarlayın

```java
// PdfOptions'ın bir örneğini oluşturun
PdfOptions pdfOptions = new PdfOptions();

// VectorRasterizationOptions özelliğini ayarlayın
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Şimdi bir tane oluşturuyoruz`PdfOptions` örneğini seçin ve ayarlayın`VectorRasterizationOptions` önceden yapılandırılmış olanın özelliği`CadRasterizationOptions`.

## 4. Adım: PDF'ye aktarın

```java
// CAD'yi PDF'ye aktar
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Son olarak CAD görüntüsünü belirtilen seçenekleri kullanarak PDF dosyasına kaydediyoruz.

## Adım 5: TiffOptions Oluşturun ve VectorRasterizationOptions'ı Ayarlayın

```java
// TiffOptions'ın bir örneğini oluşturun
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// VectorRasterizationOptions özelliğini ayarlayın
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Bu adımda bir kurulum gerçekleştiriyoruz.`TiffOptions` örneği ve yapılandırmasını yapın`VectorRasterizationOptions` mülk.

## Adım 6: TIFF'e aktarın

```java
// CAD'yi TIFF'e aktar
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Son olarak CAD görüntüsünü belirtilen seçenekleri kullanarak TIFF dosyasına kaydediyoruz.

## Çözüm

 Tebrikler! Aspose.CAD for Java'yı kullanarak tuval boyutunu ve modunu başarıyla ayarladınız. Bu eğitim, CAD dönüştürme projeleriniz için sağlam bir temel sağlar. Daha fazla özellik ve olasılığı keşfedin[Aspose.CAD belgeleri](https://reference.aspose.com/cad/java/).

## SSS'ler

### S1: Aspose.CAD for Java'yı diğer Java çerçeveleriyle kullanabilir miyim?

Cevap1: Evet, Aspose.CAD çeşitli Java çerçeveleriyle sorunsuz bir şekilde entegre olacak şekilde tasarlanmıştır.

### S2: Aspose.CAD için geçici bir lisans mevcut mu?

 Cevap2: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

### S3: Aspose.CAD için topluluk desteğini nereden alabilirim?

 A3: Ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği ve tartışmalar için.

### S4: Aspose.CAD'i ücretsiz deneyebilir miyim?

 Cevap4: Kesinlikle! Bedava deneme sürümünü al[Burada](https://releases.aspose.com/).

### S5: Aspose.CAD for Java'yı nasıl satın alabilirim?

 A5: Ürünü satın alın[Burada](https://purchase.aspose.com/buy).