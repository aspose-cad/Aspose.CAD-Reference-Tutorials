---
title: Aspose.CAD for Java ile IFC'yi PNG'ye aktarın
linktitle: IFC'yi PNG'ye aktar
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java ile IFC'yi zahmetsizce PNG'ye dönüştürün. Adım adım eğitimimizi takip edin.
type: docs
weight: 18
url: /tr/java/cad-export-options/export-ifc-to-png/
---
## giriiş

Aspose.CAD for Java kullanarak IFC'yi (Industry Foundation Classes) PNG'ye aktarmaya ilişkin bu adım adım eğitime hoş geldiniz. Aspose.CAD, IFC formatı da dahil olmak üzere CAD dosyalarıyla çalışmak için kapsamlı yetenekler sağlayan güçlü bir Java kütüphanesidir. Bu eğitimde, her adımda ayrıntılı açıklamalarla bir IFC dosyasını PNG görüntüsüne dönüştürme sürecinde size rehberlik edeceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.CAD Kütüphanesi: Java için Aspose.CAD kütüphanesini şuradan indirip yükleyin:[İndirme: {link](https://releases.aspose.com/cad/java/).

- Doküman Dizini: Sisteminizde IFC dosyanızın bulunduğu bir dizin hazırlayın.

## Ad Alanlarını İçe Aktar

Java projenizde gerekli ad alanlarını aşağıda gösterildiği gibi içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Adım 1: IFC Dosyasını Yükleyin

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Bu adım, Aspose.CAD kullanarak IFC dosyasının yüklenmesini içerir.

## Adım 2: Vektör Seçeneklerini Ayarlayın

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Sayfa genişliğini ve yüksekliğini belirterek rasterleştirme için vektör seçeneklerini yapılandırın.

## 3. Adım: PNG Seçeneklerini Ayarlayın

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Vektör rasterleştirme seçenekleri dahil PNG seçeneklerini ayarlayın.

## 4. Adım: PNG olarak kaydedin

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

İşlenen görüntüyü PNG formatında kaydedin.

## Çözüm

Tebrikler! Aspose.CAD for Java'yı kullanarak bir IFC dosyasını başarıyla PNG'ye dönüştürdünüz. Bu eğitimde, bu işlevselliği projelerinize sorunsuz bir şekilde entegre edebilmenizi sağlayan kapsamlı bir kılavuz sağlanmıştır.

## SSS'ler

### S1: Aspose.CAD, IFC dosyalarının tüm sürümleriyle uyumlu mudur?

 Cevap1: Aspose.CAD, IFC dosyalarının çeşitli sürümlerini destekler. Bakın[dokümantasyon](https://reference.aspose.com/cad/java/) uyumluluk ayrıntıları için.

### S2: Rasterleştirme seçeneklerini daha da özelleştirebilir miyim?

 A2: Kesinlikle! Keşfedin[dokümantasyon](https://reference.aspose.com/cad/java/) Gelişmiş özelleştirme seçenekleri için.

### S3: Deneme sürümü mevcut mu?

Cevap3: Evet, ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.CAD için nasıl geçici lisans alabilirim?

 Cevap4: Geçici bir lisans alın[bu bağlantı](https://purchase.aspose.com/temporary-license/).

### S5: Nereden yardım isteyebilirim veya sorunları tartışabilirim?

A5: ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği için.
