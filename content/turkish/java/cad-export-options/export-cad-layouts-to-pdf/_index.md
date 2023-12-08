---
title: Aspose.CAD for Java ile CAD Düzenlerini PDF'ye aktarın
linktitle: CAD Düzenlerini PDF'ye aktar
second_title: Aspose.CAD Java API'si
description: CAD düzenlerini zahmetsizce PDF'ye aktarmak için Aspose.CAD for Java'yı keşfedin. Verimli, güvenilir ve geliştirici dostu.
type: docs
weight: 11
url: /tr/java/cad-export-options/export-cad-layouts-to-pdf/
---
## giriiş

Sürekli gelişen bilgisayar destekli tasarım (CAD) alanında Aspose.CAD for Java, CAD dosyalarını işlemek ve dönüştürmek için güçlü bir araç olarak öne çıkıyor. Bu eğitimde, Aspose.CAD for Java kullanarak CAD düzenlerini PDF'ye aktarma sürecinde size rehberlik edeceğiz. İster tecrübeli bir geliştirici olun ister CAD dünyasına dalın, bu adım adım kılavuz bu çok yönlü Java kütüphanesinin tüm potansiyelinden yararlanmanıza yardımcı olacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.CAD for Java: Kütüphanenin kurulu olduğundan emin olun. Aspose web sitesinden indirebilirsiniz[Burada](https://releases.aspose.com/cad/java/).

- Java Geliştirme Ortamı: Makinenizde bir Java geliştirme ortamının kurulu olduğundan emin olun.

Artık her şeyi ayarladığınıza göre öğreticiye başlayalım.

## Ad Alanlarını İçe Aktar

Java kodunuzda gerekli ad alanlarını içe aktararak başlayın. Bu içe aktarmalar Aspose.CAD for Java ile çalışmak için gereken sınıflara ve yöntemlere erişim sağlar.

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

 CAD dosyasını Java uygulamanıza yükleyerek başlayın.`Image.load` yöntem. Yer değiştirmek`"conic_pyramid.dxf"` CAD dosyanızın yolu ile birlikte.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## Adım 2: Rasterleştirme Seçeneklerini Ayarlayın

 Bir örneğini oluşturun`CadRasterizationOptions` CAD varlıklarının nasıl rasterleştirilmesi gerektiğini tanımlamak için. Sayfa genişliği, sayfa yüksekliği ve sayfa düzeni ölçeklendirmesi gibi parametreleri gereksinimlerinize göre ayarlayın.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## 3. Adım: PDF Seçeneklerini Ayarlayın

 Bir örneğini oluşturun`PdfOptions` ve bunu rasterleştirme seçenekleriyle ilişkilendirin. Ek olarak, PDF dışa aktarımı için yumuşatma modu, metin oluşturma ipucu ve enterpolasyon modu gibi grafik seçeneklerini ayarlayın.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## 4. Adım: PDF'ye aktarın

 Son olarak, CAD düzenlerini kullanarak PDF dosyasına aktarın.`save` yöntemi`cadImage` nesne.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

Tebrikler! Aspose.CAD for Java'yı kullanarak CAD düzenlerini başarıyla PDF'ye aktardınız. CAD dosya işleme deneyiminizi geliştirmek için Aspose.CAD tarafından sunulan ek özellikleri ve işlevleri keşfetmekten çekinmeyin.

## Çözüm

Bu eğitimde, Aspose.CAD for Java kullanarak CAD düzenlerini PDF'ye aktarma sürecini anlattık. Aspose.CAD, güçlü özellikleri ve kullanımı kolay API'si ile geliştiricilerin Java uygulamalarında CAD dosyalarıyla verimli bir şekilde çalışmasını sağlar.

## SSS'ler

### S1: Aspose.CAD for Java'yı diğer CAD dosya formatlarıyla kullanabilir miyim?

 Cevap1: Evet, Aspose.CAD, DWG, DXF, DWF ve daha fazlası dahil olmak üzere çeşitli CAD formatlarını destekler. Belgeleri kontrol edin[Burada](https://reference.aspose.com/cad/java/) tam liste için.

### S2: Aspose.CAD for Java'nın ücretsiz deneme sürümü mevcut mu?

 Cevap2: Evet, Aspose.CAD'in özelliklerini ücretsiz deneme sürümüyle keşfedebilirsiniz[Burada](https://releases.aspose.com/).

### S3: Aspose.CAD for Java desteğini nasıl alabilirim?

 Cevap3: Aspose.CAD forumunu ziyaret edin[Burada](https://forum.aspose.com/c/cad/19) topluluk desteği için. Premium destek için bir lisans satın almayı düşünün[Burada](https://purchase.aspose.com/buy).

### S4: Otomatik ve manuel düzen ölçeklendirme arasındaki fark nedir?

Cevap4: Otomatik düzen ölçeklendirme, belirtilen sayfa boyutlarına göre düzen boyutunu ayarlar; manuel ölçeklendirme ise özel ölçeklendirme değerleri ayarlamanıza olanak tanır.

### S5: Dışa aktarılan PDF dosyalarının görünümünü özelleştirebilir miyim?

C5: Evet, dışa aktarılan PDF'nin kalitesini ve görünümünü kontrol etmek için koddaki grafik seçeneklerini özelleştirebilirsiniz.