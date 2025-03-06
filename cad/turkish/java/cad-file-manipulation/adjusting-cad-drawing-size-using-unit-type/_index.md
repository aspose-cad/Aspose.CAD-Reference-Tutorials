---
title: Aspose.CAD for Java ile Birim Tipini Kullanarak CAD Çizim Boyutunu Ayarlama
linktitle: Birim Tipini Kullanarak CAD Çizim Boyutunu Ayarlama
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java'nın CAD çizim boyutlarını zahmetsizce ayarlama konusundaki gücünü keşfedin. Hassasiyet ve uyarlanabilirlik için adım adım kılavuzumuzu izleyin.
weight: 14
url: /tr/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java ile Birim Tipini Kullanarak CAD Çizim Boyutunu Ayarlama

## giriiş

Sürekli gelişen Bilgisayar Destekli Tasarım (CAD) alanında hassasiyet ve uyarlanabilirlik çok önemlidir. Yaygın gereksinimlerden biri, CAD çizimlerinin boyutunun belirli birim türlerine göre ayarlanmasıdır. Aspose.CAD for Java, CAD dosyalarının programlı olarak işlenmesi için kusursuz yetenekler sağlayan güçlü bir müttefik olarak ortaya çıkıyor.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Java Geliştirme Ortamı: Makinenizde işlevsel bir Java geliştirme ortamının kurulu olduğundan emin olun.

-  Aspose.CAD for Java Library: Aspose.CAD kütüphanesini indirin ve Java projenize entegre edin. Kütüphaneyi edinebilirsiniz[Burada](https://releases.aspose.com/cad/java/).

## Ad Alanlarını İçe Aktar

Aspose.CAD işlevlerine erişmek için Java kodunuza gerekli ad alanlarını ekleyin. Aşağıdaki içe aktarmaları ekleyin:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Şimdi, birim türünü kullanarak CAD çizim boyutunu ayarlama sürecini yönetilebilir adımlara ayıralım:

## 1. Adım: Veri Dizinini Tanımlayın

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

CAD dosyalarınızın bulunduğu dizinin yolunu ayarlayın.

## Adım 2: CAD Çizimini Yükleyin

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Aspose.CAD'i kullanarak CAD çizimini yükleyin`Image` sınıf.

## 3. Adım: BMP Seçenekleri Oluşturun

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Örnekleyin`BmpOptions` CAD düzenini BMP formatına aktarmak için sınıf.

## Adım 4: Rasterleştirme Seçeneklerini Yapılandırın

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Bir örneğini oluşturun`CadRasterizationOptions` ve bunu şununla ilişkilendirin:`BmpOptions` vektör rasterleştirmesi için.

## Adım 5: Birim Türünü Ayarlayın

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

CAD çizimi için istenen birim tipini belirtin. Bu örnekte bunu Santimetre olarak ayarladık.

## Adım 6: Düzenleri Ayarlayın

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Dışa aktarma sırasında dikkate alınacak düzenleri tanımlayın. Bu durumda "Model" düzenini seçtik.

## Adım 7: BMP'ye aktarın

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Son olarak değiştirilen CAD çizimini BMP formatında kaydedin.

## Çözüm

Aspose.CAD for Java ile CAD çizim boyutlarını ayarlamak artık çok kolay. Bu eğitim, kesin sonuçlara ulaşmada her adımın önemini vurgulayarak size süreç boyunca yol gösterdi.

## SSS'ler

### S1: Aspose.CAD for Java'yı diğer programlama dilleriyle birlikte kullanabilir miyim?

Cevap1: Aspose.CAD öncelikle Java'yı destekler ancak .NET gibi diğer diller için de versiyonlar mevcuttur.

### S2: Aspose.CAD için herhangi bir lisanslama seçeneği var mı?

 Cevap2: Evet, lisanslama seçeneklerini inceleyebilir ve Aspose.CAD'i satın alabilirsiniz.[Burada](https://purchase.aspose.com/buy).

### S3: Aspose.CAD için ücretsiz deneme sürümü mevcut mu?

 Cevap3: Kesinlikle ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.CAD for Java desteğini nasıl alabilirim?

 Cevap4: Aspose.CAD forumunu ziyaret edin[Burada](https://forum.aspose.com/c/cad/19) kapsamlı destek için.

### S5: Aspose.CAD için geçici bir lisans alabilir miyim?

 Cevap5: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
