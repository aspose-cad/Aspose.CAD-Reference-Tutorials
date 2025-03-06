---
title: Aspose.CAD for Java ile Gömülü DGN'yi PDF'ye aktarın
linktitle: Gömülü DGN'yi Dışa Aktar
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java kullanarak gömülü DGN dosyalarını PDF'ye aktarmaya ilişkin adım adım kılavuzu keşfedin. Sorunsuz CAD dosya işlemeyle Java uygulamalarınızı geliştirin.
weight: 11
url: /tr/java/dgn-export-options/export-embedded-dgn/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java ile Gömülü DGN'yi PDF'ye aktarın

## giriiş

Aspose.CAD for Java kullanarak gömülü DGN dosyalarını dışa aktarmaya ilişkin bu kapsamlı eğitime hoş geldiniz. Aspose.CAD, Java geliştiricilerinin CAD dosyalarıyla sorunsuz bir şekilde çalışmasını sağlayan güçlü bir kütüphanedir. Bu eğitimde, adım adım talimatları kullanarak gömülü DGN dosyalarını PDF'ye aktarma sürecinde size rehberlik edeceğiz. İster deneyimli bir geliştirici olun ister yeni başlıyor olun, bu eğitim Aspose.CAD'in özelliklerinden yararlanarak Java uygulamalarınızı geliştirmenize yardımcı olacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:
- Java Geliştirme Ortamı: Makinenizde bir Java geliştirme ortamının kurulu olduğundan emin olun.
-  Aspose.CAD for Java: Aspose.CAD for Java kütüphanesini şu adresten indirip yükleyin:[Burada](https://releases.aspose.com/cad/java/).

## Paketleri İçe Aktar

Başlamak için gerekli paketleri Java projenize aktarmanız gerekir. Aşağıdaki içe aktarma ifadelerini kodunuza ekleyin:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Şimdi örnek kodu birden çok adıma ayıralım:

## 1. Adım: Giriş ve Çıkış Yollarını Ayarlayın

Belgenizin bulunduğu dizin yolunu tanımlayın ve giriş DWG dosya adını belirtin.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Adım 2: DWG Dosyasını Yükleyin

 DWG dosyasını bir`Image` Aspose.CAD kullanarak nesneyi oluşturun.

```java
Image objImage = Image.load(fileName);
```

## 3. Adım: Rasterleştirme Seçeneklerini Yapılandırın

Dışa aktarmaya dahil edilecek düzenler gibi rasterleştirme seçeneklerini yapılandırın.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## 4. Adım: PDF Seçeneklerini Yapılandırın

Vektör rasterleştirme seçenekleri de dahil olmak üzere PDF seçeneklerini ayarlayın.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Adım 5: PDF Dosyasını Kaydet

PDF dosyasını yapılandırılmış seçeneklerle kaydedin.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Çözüm

Tebrikler! Gömülü bir DGN dosyasını Aspose.CAD for Java kullanarak başarıyla PDF'ye aktardınız. Bu eğitimde, verimli CAD dosyası manipülasyonu için Aspose.CAD'i Java uygulamanıza entegre etmek için gerekli adımlar anlatıldı.

## SSS'ler

### S1: Aspose.CAD for Java'yı ticari bir projede kullanabilir miyim?

 Cevap1: Evet, Aspose.CAD for Java ticari bir kütüphanedir. adresinden lisans alabilirsiniz.[Burada](https://purchase.aspose.com/buy).

### S2: Ücretsiz deneme sürümü mevcut mu?

 Cevap2: Evet, Aspose.CAD for Java'nın ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S3: Aspose.CAD for Java desteğini nasıl alabilirim?

Cevap3: Aspose.CAD topluluğundan destek alabilirsiniz.[forum](https://forum.aspose.com/c/cad/19).

### S4: Geçici bir lisansa ihtiyacım olursa ne olur?

 Cevap4: Geçici bir lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Belgeleri nerede bulabilirim?

 A5: Belgeler mevcut[Burada](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
