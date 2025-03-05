---
title: Aspose.CAD Eğitimi ile Java DGN'den JPEG'e Dönüştürme
linktitle: AutoCAD Formatındaki DGN'yi Raster Görüntü Formatına Aktarma
second_title: Aspose.CAD Java API'si
description: Aspose.CAD kullanarak DGN dosyalarını Java'da JPEG görüntülere nasıl aktaracağınızı öğrenin. Bu adım adım eğitim, süreç boyunca size zahmetsizce rehberlik eder.
type: docs
weight: 13
url: /tr/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## giriiş

Aspose.CAD for Java kullanarak DGN (Tasarım) dosyalarını Raster Görüntü Formatına aktarmaya ilişkin bu kapsamlı eğitime hoş geldiniz. Aspose.CAD, Java geliştiricilerinin CAD dosyalarıyla sorunsuz bir şekilde çalışmasını sağlayan güçlü bir kütüphanedir. Bu eğitimde, DGN dosyalarını JPEG görüntülerine dönüştürme sürecinde size adım adım talimatlar ve kod örnekleri sunarak rehberlik edeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:
1.  Aspose.CAD Kütüphanesi: Aspose.CAD for Java kütüphanesinin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/cad/java/).
2. Java Geliştirme Kiti (JDK): Makinenizde Java'nın kurulu olduğundan emin olun.
3. Entegre Geliştirme Ortamı (IDE): IntelliJ veya Eclipse gibi Java uyumlu bir IDE kullanın.

## Paketleri İçe Aktar

Aspose.CAD için gerekli paketleri Java projenize aktarın. Kodunuza aşağıdaki satırları ekleyin:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Adım 1: DGN Dosyasını Yükleyin

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Adım 2: JpegOptions Nesnesi Oluşturun

```java
ImageOptionsBase options = new JpegOptions();
```

## 3. Adım: Rasterleştirme Seçeneklerini Atayın

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Adım 4: Dönüştürülen Görüntüyü Kaydedin

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Dosya yollarını uygun şekilde ayarlayarak bu adımları belirli DGN dosyalarınız için tekrarlayın.

## Çözüm

Tebrikler! Aspose.CAD for Java kullanarak DGN dosyalarını Raster Görüntü Formatına nasıl aktaracağınızı başarıyla öğrendiniz. Bu eğitim sizi bu işlevselliği Java uygulamalarınıza dahil etme bilgisiyle donattı.

## SSS'ler

### S1: Aspose.CAD for Java'yı diğer CAD dosya formatlarıyla kullanabilir miyim?

Cevap1: Evet, Aspose.CAD çeşitli CAD formatlarını destekleyerek Java geliştiricileri için çok yönlü bir çözüm sunar.

### S2: Aspose.CAD for Java'nın ücretsiz deneme sürümü mevcut mu?

 C2: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S3: Aspose.CAD for Java belgelerini nerede bulabilirim?

 A3: Belgelere bakın[Burada](https://reference.aspose.com/cad/java/).

### S4: Aspose.CAD for Java desteğini nasıl alabilirim?

 Cevap4: Destek forumunu ziyaret edin[Burada](https://forum.aspose.com/c/cad/19).

### S5: Aspose.CAD for Java lisansını nereden satın alabilirim?

 A5: Bir lisans satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).