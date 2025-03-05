---
title: Aspose.CAD for Java Kullanarak DWG'deki Düzenleri Listeleme
linktitle: DWG'deki Düzenleri Listeleme
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java'yı keşfedin ve DWG dosyalarındaki düzenleri zahmetsizce listeleyin. Güçlü CAD işlevselliğini Java uygulamalarınıza entegre edin.
type: docs
weight: 12
url: /tr/java/cad-file-manipulation/list-layouts-in-dwg/
---
## giriiş

DWG dosyalarındaki düzenleri listelemek için Aspose.CAD for Java'yı kullanmayla ilgili adım adım kılavuzumuza hoş geldiniz. Aspose.CAD, geliştiricilerin CAD dosyalarıyla programlı olarak çalışmasını sağlayan güçlü bir kütüphanedir. Bu eğitimde belirli bir göreve odaklanacağız: Bir DWG dosyasındaki düzenleri listelemek. Bu kılavuzun sonunda, bu işlevselliği Java uygulamalarınıza sorunsuz bir şekilde entegre edebileceksiniz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.CAD for Java Library: Aspose.CAD for Java kütüphanesinin kurulu olduğundan emin olun. adresinden indirebilirsiniz.[İnternet sitesi](https://releases.aspose.com/cad/java/).

- Java Geliştirme Ortamı: Makinenizde bir Java geliştirme ortamı kurun.

## Ad Alanlarını İçe Aktar

Aspose.CAD'i kullanmak için Java uygulamanızda gerekli ad alanlarını içe aktarmanız gerekir. Java dosyanızın başına aşağıdaki satırları ekleyin:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## 1. Adım: Belge Dizininizi Kurun

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

"Belge Dizininiz"i, CAD dosyalarınızın depolandığı dizinin yolu ile değiştirdiğinizden emin olun.

## Adım 2: DWG Dosyasını Yükleyin

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

Belirtilen dosya yolunu kullanarak DWG dosyasını yükleyin.

## 3. Adım: Düzenleri Alın ve Adları Yazdırın

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

Düzenleri DWG dosyasından alın ve adlarını konsola yazdırın.

## Çözüm

 Tebrikler! Aspose.CAD for Java kullanarak mizanpajları bir DWG dosyasında başarıyla listelediniz. Bu eğitim, ortamınızı ayarlamaktan düzen adlarını yazdırmaya kadar temel adımları kapsıyordu. Aspose.CAD for Java'nın diğer özelliklerini keşfetmekten çekinmeyin.[dokümantasyon](https://reference.aspose.com/cad/java/).

## SSS'ler

### S1: Aspose.CAD for Java'yı diğer CAD dosya formatlarıyla kullanabilir miyim?

Cevap1: Evet, Aspose.CAD, DWG, DXF, DWF ve daha fazlası dahil olmak üzere çeşitli CAD formatlarını destekler.

### S2: Aspose.CAD for Java'nın ücretsiz deneme sürümü mevcut mu?

 C2: Evet, şu adresten ücretsiz deneme sürümü edinebilirsiniz:[Burada](https://releases.aspose.com/).

### S3: Aspose.CAD for Java için topluluk desteğini nereden alabilirim?

 A3: Ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği için.

### S4: Aspose.CAD for Java lisansını nasıl satın alabilirim?

 Cevap4: Lisansı şuradan satın alabilirsiniz:[satın alma sayfası](https://purchase.aspose.com/buy).

### S5: Geçici lisansı test amacıyla kullanabilir miyim?

 Cevap5: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).