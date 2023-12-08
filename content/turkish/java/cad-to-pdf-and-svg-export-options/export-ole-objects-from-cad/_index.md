---
title: Aspose.CAD for Java Kullanarak OLE Nesnelerini CAD'den Dışa Aktarma
linktitle: OLE Nesnelerini CAD'den Dışa Aktarma
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java'nın potansiyelini ortaya çıkarın. OLE nesnelerini CAD dosyalarından zahmetsizce dışa aktarın. Kusursuz CAD veri yönetimi için hemen indirin.
type: docs
weight: 10
url: /tr/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---
## giriiş

Bilgisayar Destekli Tasarımın (CAD) dinamik dünyasında, OLE (Nesne Bağlama ve Gömme) nesnelerini verimli bir şekilde yönetmek ve çıkarmak çok önemlidir. Aspose.CAD for Java, OLE nesnelerini CAD dosyalarından dışa aktarmak için güçlü bir çözüm sunar. Bu adım adım kılavuz, süreç boyunca size yol gösterecek ve bu aracın tüm potansiyelinden yararlanmanızı sağlayacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Java Ortamı: Makinenizde bir Java geliştirme ortamının kurulu olduğundan emin olun.
-  Aspose.CAD for Java: Aspose.CAD for Java kütüphanesini indirip yükleyin. Kütüphaneyi şu adreste bulabilirsiniz:[İndirme: {link](https://releases.aspose.com/cad/java/).
- CAD Dosyaları: Dışa aktarmak istediğiniz OLE nesnelerini içeren CAD dosyalarını hazırlayın.

## Ad Alanlarını İçe Aktar

Başlamak için gerekli ad alanlarını Java projenize aktarın. Bu ad alanları, Aspose.CAD kullanarak CAD dosyalarıyla çalışmak için gereken temel sınıfları ve işlevleri sağlar.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Şimdi OLE nesnelerini CAD'den dışa aktarma sürecini birden çok adıma ayıralım:

## 1. Adım: Belge Dizininizi Ayarlayın

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

"Belge Dizininiz"i, CAD dosyalarınızı içeren dizinin yoluyla değiştirdiğinizden emin olun.

## Adım 2: CAD Dosya Adlarını Tanımlayın

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

 İşlemek istediğiniz CAD dosyalarının adlarını belirtin.`files` sıralamak.

## 3. Adım: PNG Dışa Aktarma Seçeneklerini Ayarlayın

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Vektör rasterleştirme ve düzen ayarları da dahil olmak üzere PNG dışa aktarma seçeneklerini yapılandırın.

## Adım 4: CAD Dosyalarını Yineleyin

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Belirtilen her CAD dosyasını yineleyin, Aspose.CAD kullanarak yükleyin ve OLE nesnelerini PNG görüntüleri olarak kaydedin.

## Çözüm

Bu basit ama güçlü adımlarla Aspose.CAD for Java'yı kullanarak OLE nesnelerini CAD dosyalarından sorunsuz bir şekilde dışa aktarabilirsiniz. Bu çok yönlü araç, geliştiricilerin CAD verilerini verimli bir şekilde yönetmelerine olanak tanır ve CAD uygulama geliştirmede yeni olanakların önünü açar.

## SSS'ler

### S1: Aspose.CAD tüm CAD dosya formatlarıyla uyumlu mudur?

 Cevap1: Aspose.CAD, DWG, DXF ve DGN dahil olmak üzere çeşitli CAD formatlarını destekler. Bakın[dokümantasyon](https://reference.aspose.com/cad/java/) tam liste için.

### S2: OLE nesnelerinin dışa aktarma ayarlarını özelleştirebilir miyim?

Cevap2: Evet, Aspose.CAD, dışa aktarma ayarlarını özelleştirmek için kapsamlı seçenekler sunarak çıktıyı özel gereksinimlerinize göre uyarlamanıza olanak tanır.

### S3: Aspose.CAD için ücretsiz deneme sürümü mevcut mu?

 Cevap3: Evet, Aspose.CAD'in yeteneklerini ücretsiz deneme sürümünü edinerek keşfedebilirsiniz.[Burada](https://releases.aspose.com/).

### S4: Aspose.CAD için topluluk desteğini nereden alabilirim?

 Cevap4: Aspose.CAD topluluğuna katılın[forum](https://forum.aspose.com/c/cad/19) yardım istemek ve deneyimlerinizi paylaşmak için.

### S5: Aspose.CAD lisansını nasıl satın alabilirim?

A5: ziyaret edin[satın alma sayfası](https://purchase.aspose.com/buy) Geliştirme ihtiyaçlarınıza uygun bir lisans almak için.