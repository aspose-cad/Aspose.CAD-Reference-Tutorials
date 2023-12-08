---
title: İhracatta Kalem Desteği
linktitle: İhracatta Kalem Desteği
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java ile CAD dışa aktarımında kalem özelleştirmesinde uzmanlaşın. Sorunsuz entegrasyon için adım adım kılavuzumuzu izleyin.
type: docs
weight: 13
url: /tr/java/advanced-cad-features/pen-support-in-export/
---
## giriiş

Sürekli gelişen CAD (Bilgisayar Destekli Tasarım) dönüşüm ortamında Aspose.CAD for Java, CAD dosyalarını işlemek için kapsamlı yetenekler sunan güçlü bir araç olarak ortaya çıkıyor. Çok yönlü özellikleri arasında, dışa aktarma sırasında kalem özelleştirme desteği öne çıkıyor ve kullanıcıların dışa aktarılan görüntülerin görünümünü uyarlamasına olanak tanıyor. Bu eğitim, Java kullanarak pratik uygulamaya odaklanarak dışa aktarma işlevinde kalem desteğinden yararlanma sürecinde size yol gösterecektir.

## Önkoşullar

Eğiticiye başlamadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Java Geliştirme Ortamı: Makinenizde işlevsel bir Java geliştirme ortamının kurulu olduğundan emin olun.

-  Aspose.CAD Kütüphanesi: Aspose.CAD kütüphanesini indirin ve Java projenize entegre edin. Kütüphaneyi bulabilirsiniz[Burada](https://releases.aspose.com/cad/java/).

Şimdi eğitime geçelim ve CAD dışa aktarımı sırasında kalem desteğini kullanma adımlarını inceleyelim.

## Ad Alanlarını İçe Aktar

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## 1. Adım: Belge Dizininizi Tanımlayın

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

"Belge Dizininiz"i CAD belgelerinizin gerçek yolu ile değiştirdiğinizden emin olun.

## Adım 2: CAD Dosyasını Yükleyin

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

Bu adım, Aspose.CAD kütüphanesini kullanarak CAD dosyasının (bu durumda "conic_pyramid.dxf") yüklenmesini içerir.

## 3. Adım: Rasterleştirme Seçeneklerini Yapılandırın

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

Sayfa genişliğini ve yüksekliğini özel gereksinimlerinize göre ayarlayın. Bu değerler dışa aktarılan görüntünün boyutlarını belirler.

## Adım 4: Kalem Seçeneklerini Özelleştirin

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

Kalemlerin başlangıç ve bitiş kapaklarını gerektiği gibi özelleştirin. Bu özelleştirme, CadImage nesnesini çeşitli görüntü formatlarına aktarırken geçerlidir.

## 5. Adım: PDF Dışa Aktarma Seçeneklerini Yapılandırın

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Önceden yapılandırılmış rasterleştirme seçenekleri de dahil olmak üzere vektör rasterleştirme seçeneklerini belirtin.

## Adım 6: Dışa Aktarılan PDF'yi Kaydedin

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Dışa aktarılan PDF'yi belirtilen dosya adı (bu örnekte "9LHATT-A56_geneated.pdf") ve yapılandırılmış seçeneklerle kaydedin.

## Çözüm

Sonuç olarak, Aspose.CAD for Java ile CAD dışa aktarımı sırasında kalem desteğinden yararlanmak, kullanıcılara dışa aktarılan görüntülerin görünümünü özelleştirme olanağı sağlar. Bu adım adım kılavuzu izleyerek kalem özelleştirmesini CAD dönüştürme iş akışınıza sorunsuz bir şekilde nasıl entegre edeceğinizi öğrendiniz.

## SSS'ler

### S1: PDF dışındaki formatlar için kalem seçeneklerini özelleştirebilir miyim?

Cevap1: Evet, bu eğitimde gösterilen kalem özelleştirmesi PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF ve WMF dahil olmak üzere çeşitli görüntü formatlarına uygulanabilir.

### S2: Kalemler için farklı başlangıç ve bitiş kapaklarını nasıl kullanabilirim?

 A2: Kullanın`PenOptions` İstenilen başlangıç ve bitiş sınırlarını ayarlamak için sınıf, çizgilerin görünümünü tanımlamada esneklik sunar.

### S3: Kalem seçeneklerini belirtmezsem ne olur?

Cevap3: Kalem seçenekleri açıkça ayarlanmamışsa sistem, farklı bağlamlarda farklılık gösterebilecek varsayılan kalemlerini kullanır.

### S4: Rasterleştirme seçenekleriyle ilgili özel hususlar var mı?

Cevap4: Dışa aktarılan görüntünün boyutlarını kontrol etmek için rasterleştirme seçeneklerinde sayfa genişliğini ve yüksekliğini ayarlayın.

### S5: Ek desteği veya topluluk tartışmalarını nerede bulabilirim?

 Cevap5: Aspose.CAD topluluk forumunu şu adreste keşfedin:[Burada](https://forum.aspose.com/c/cad/19) Destek ve tartışmalar için.