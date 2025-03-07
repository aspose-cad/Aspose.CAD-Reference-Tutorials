---
title: Aspose.CAD for Java'yı kullanarak DWG'yi PDF'ye veya Raster'a aktarın
linktitle: DWG'yi PDF'ye veya Raster'a aktarın
second_title: Aspose.CAD Java API'si
description: Aspose.CAD'i kullanarak DWG dosyalarını PDF'ye veya Java'daki raster görüntülere aktarmanın kusursuz sürecini keşfedin. Bu adım adım kılavuz, hassasiyet ve verimlilik sağlar.
weight: 13
url: /tr/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java'yı kullanarak DWG'yi PDF'ye veya Raster'a aktarın

## giriiş

Bilgisayar destekli tasarımın (CAD) dinamik dünyasında, çizimlerin verimli şekilde işlenmesi çok önemlidir. Aspose.CAD for Java, DWG dosyalarını PDF'ye veya taramalı görüntülere aktarmak için güçlü bir çözüm sunar. Bu eğitim size süreç boyunca rehberlik edecek ve Aspose.CAD for Java'nın tüm potansiyelinden yararlanmanızı sağlayacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- Java programlamanın temel anlayışı.
-  Aspose.CAD for Java kütüphanesi kuruldu. Değilse indirin[Burada](https://releases.aspose.com/cad/java/).
- Test amaçlı bir DWG dosyası. Sağlanan "Bottom_plate.dwg" dosyasını kullanabilirsiniz.

## Ad Alanlarını İçe Aktar

Süreci başlatmak için Java projenizde gerekli ad alanlarını içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Adım 1: DWG Dosyasını Yükleyin

 Aspose.CAD'i kullanarak DWG dosyanızı yükleyerek başlayın`Image` sınıf:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Adım 2: Birim Türünü Belirleyin

Ardından yüklenen DWG dosyasının birim türünü kontrol edin:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## 3. Adım: Rasterleştirme Seçeneklerini Ayarlayın

Birim türüne bağlı olarak rasterleştirme seçeneklerini yapılandırın:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metrik birimler
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // İmparatorluk birimleri
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## 4. Adım: PDF Seçeneklerini Yapılandırın

PDF dışa aktarma seçeneklerini ayarlayın:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## 5. Adım: PDF olarak kaydedin

Son olarak DWG dosyasını PDF olarak kaydedin:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

İşte buyur! Aspose.CAD for Java'yı kullanarak bir DWG dosyasını başarıyla PDF'ye aktardınız.

## Çözüm

Bu eğitimde, DWG dosyalarını PDF'ye veya taramalı görüntülere aktarmak için Aspose.CAD for Java'dan yararlanma konusunda adım adım bir kılavuz sağlandı. Bu kitaplık süreci basitleştirerek Java uygulamalarınızdaki CAD çizimlerini verimli bir şekilde yönetmenize olanak tanır.

## SSS'ler

### S1: Aspose.CAD for Java'yı diğer Java çerçeveleriyle kullanabilir miyim?

Cevap1: Evet, Aspose.CAD for Java, popüler Java çerçeveleriyle sorunsuz bir şekilde bütünleşir.

### S2: Aspose.CAD for Java için geçici bir lisans mevcut mu?

 Cevap2: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

### S3: Aspose.CAD for Java desteğini nerede bulabilirim?

 A3: Ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluktan yardım almak için.

### S4: Aspose.CAD for Java lisansını nasıl satın alabilirim?

 Cevap4: Bir lisans satın alabilirsiniz[Burada](https://purchase.aspose.com/buy).

### S5: Aspose.CAD for Java hangi birimleri destekliyor?

Cevap5: Aspose.CAD for Java hem metrik hem de İngiliz ölçü birimlerini destekler.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
