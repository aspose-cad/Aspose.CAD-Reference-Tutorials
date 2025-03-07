---
title: Aspose.CAD for Java Kullanarak CAD Çizim Boyutunu Otomatik Ayarlama
linktitle: CAD Çizim Boyutunun Otomatik Ayarlanması
second_title: Aspose.CAD Java API'si
description: Aspose.CAD'i kullanarak Java'da CAD çizim boyutlarını otomatik olarak ayarlamanın kusursuz sürecini keşfedin. Verimli CAD dosyası manipülasyonu için adım adım kılavuzumuzu izleyin.
weight: 13
url: /tr/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java Kullanarak CAD Çizim Boyutunu Otomatik Ayarlama

## giriiş

CAD (Bilgisayar Destekli Tasarım) dünyasında çizim boyutlarını ayarlamak ortak bir gerekliliktir ve Aspose.CAD for Java ile bu sorunsuz bir süreç haline gelir. Bu güçlü kitaplık, Java uygulamalarında CAD dosyalarının işlenmesi için kapsamlı araçlar sağlar. Bu eğitimde, Aspose.CAD'i kullanarak CAD çizim boyutlarını otomatik olarak ayarlama sürecini adım adım inceleyeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

1.  Java Geliştirme Ortamı: Makinenizde Java'nın kurulu olduğundan emin olun. İndirebilirsin[Burada](https://www.java.com/en/download/).

2.  Aspose.CAD Kütüphanesi: Java için Aspose.CAD kütüphanesini şu adresten indirip yükleyin:[Burada](https://releases.aspose.com/cad/java/).

3. Örnek CAD Dosyası: Belge dizininizde örnek bir CAD dosyası (örn. sample.dwg) bulundurun.

## Ad Alanlarını İçe Aktar

Aspose.CAD işlevselliğini kullanmak için Java uygulamanıza gerekli ad alanlarını ekleyin. İşte bir örnek:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Şimdi CAD çizim boyutlarını otomatik olarak ayarlama sürecini yönetilebilir adımlara ayıralım.

## Adım 1: CAD Çizimini Yükleyin

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

Bu adım, CAD çiziminin belirtilen dosya yolundan yüklenmesini içerir.

## Adım 2: BmpOptions'ı oluşturun

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Örnekleyin`BmpOptions` BMP formatı için çeşitli seçenekleri ayarlamak için kullanılacak olan sınıf.

## Adım 3: CadRasterizationOptions'ı oluşturun

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Bir örneğini oluşturun`CadRasterizationOptions` CAD dosyası için rasterleştirme ayarlarını özelleştirmek için.

## Adım 4: Düzenler Özelliğini Ayarlayın

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

Çıktıya dahil etmek istediğiniz düzenleri belirtin. Bu durumda "Model" düzenini kullanıyoruz.

## Adım 5: BMP Formatına Aktarın

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

Son olarak, ayarlanan CAD çizimini BMP formatında belirtilen çıktı yoluna kaydedin.

Java uygulamanızda bu adımları tekrarlayın; Aspose.CAD for Java'yı kullanarak CAD çizim boyutunu başarıyla otomatik olarak ayarlamış olacaksınız.

## Çözüm

Bu eğitimde Aspose.CAD for Java'yı kullanarak CAD çizim boyutlarını otomatik olarak ayarlama sürecini anlattık. Bu kitaplık, CAD dosyası manipülasyonunu basitleştirerek geliştiriciler için sağlam bir çözüm sunar.

## SSS'ler

### S1: Aspose.CAD farklı CAD dosya formatlarıyla uyumlu mudur?

Cevap1: Evet, Aspose.CAD, DWG, DXF, DGN ve daha fazlası dahil olmak üzere çeşitli CAD formatlarını destekler.

### S2: Aspose.CAD'i ticari projeler için kullanabilir miyim?

 A2: Kesinlikle! Ziyaret etmek[Burada](https://purchase.aspose.com/buy) Lisanslama seçeneklerini keşfetmek için.

### S3: Test amaçlı geçici lisansları nasıl alabilirim?

 Cevap 3: Geçici bir lisans edinin[Burada](https://purchase.aspose.com/temporary-license/) Test ve değerlendirme için.

### S4: Aspose.CAD desteğini nerede bulabilirim?

 Cevap4: Aspose.CAD topluluğuna katılın[forum](https://forum.aspose.com/c/cad/19) Yardım ve tartışmalar için.

### S5: Aspose.CAD for Java'nın ücretsiz deneme sürümü mevcut mu?

 C5: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/) Kütüphanenin yeteneklerini keşfetmek için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
