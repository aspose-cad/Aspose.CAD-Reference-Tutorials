---
title: Aspose.CAD for Java ile Dinamik PDF'ler Oluşturma
linktitle: Farklı Düzenlere Sahip Tek PDF
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java'yı kullanarak CAD çizimlerinden çeşitli düzenlerle etkileyici PDF'ler oluşturun. Java geliştiricileri için kolay entegrasyon ve güçlü özellikler.
type: docs
weight: 16
url: /tr/java/other-cad-operations/single-pdf-different-layouts/
---
## giriiş

Geliştiricilerin CAD çizimlerini zahmetsizce değiştirmesine olanak tanıyan güçlü bir kütüphane olan Aspose.CAD for Java dünyasına hoş geldiniz. Bu eğitimde Aspose.CAD for Java'yı kullanarak farklı düzenlere sahip tek PDF'ler oluşturmayı ele alacağız. İster deneyimli bir geliştirici olun ister yeni başlıyor olun, bu adım adım kılavuz süreç boyunca size yol gösterecektir.

## Önkoşullar

Bu yolculuğa çıkmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:
- Java Ortamı: Makinenizde Java'nın kurulu olduğundan emin olun.
-  Aspose.CAD Kütüphanesi: Java için Aspose.CAD kütüphanesini şuradan indirip yükleyin:[İndirme: {link](https://releases.aspose.com/cad/java/).
- Belge Dizini: DWG çizimleriniz için bir dizin oluşturun.

## Paketleri İçe Aktar

Java projenizde gerekli paketleri içe aktarın:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Adım 1: CAD Çizimini Yükleyin

 CAD çiziminizi bir dosyaya yükleyerek başlayın.`CadImage` nesne:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Adım 2: Rasterleştirme Seçeneklerini Yapılandırın

CAD görüntüsü için rasterleştirme seçeneklerini ayarlayın:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## 3. Adım: Düzen Sayfası Boyutlarını Özelleştirin

CAD çizimindeki çeşitli düzenler için özel boyutlar tanımlayın:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## 4. Adım: PDF Seçeneklerini Ayarlayın

Rasterleştirme ayarlarını birleştirerek PDF seçeneklerini yapılandırın:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 5. Adım: PDF olarak kaydedin

İşlenen CAD görüntüsünü PDF olarak kaydedin:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Tebrikler! Aspose.CAD for Java'yı kullanarak farklı düzenlere sahip tek bir PDF'yi başarıyla oluşturdunuz.

## Çözüm

Bu eğitimde, Aspose.CAD for Java'nın CAD çizimlerinden çeşitli düzenlere sahip PDF'ler oluşturmak için kusursuz entegrasyonunu araştırdık. Kitaplığın esnekliği ve sağlam özellikleri, onu CAD manipülasyon görevleri için tercih edilen bir seçenek haline getiriyor.

## SSS'ler

### S1: Aspose.CAD for Java'yı diğer Java kütüphaneleriyle birlikte kullanabilir miyim?

C1: Evet, Aspose.CAD for Java, diğer Java kitaplıklarıyla sorunsuz bir şekilde entegre olacak ve kapsamlı işlevsellik sağlayacak şekilde tasarlanmıştır.

### S2: Deneme sürümü mevcut mu?

 A2: Kesinlikle! Ücretsiz deneme sürümüne erişebilirsiniz[Burada](https://releases.aspose.com/).

### S3: Ek desteği nerede bulabilirim?

 A3: Ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği ve tartışmalar için.

### S4: Geçici lisansı nasıl edinebilirim?

 Cevap4: Geçici bir lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Tam sürümü nereden satın alabilirim?

Cevap5: Aspose.CAD for Java'nın tam sürümünü satın alın[Burada](https://purchase.aspose.com/buy).