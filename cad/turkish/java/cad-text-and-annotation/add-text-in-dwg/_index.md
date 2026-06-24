---
date: 2026-02-28
description: DWG'den PDF oluşturmayı, DWG'yi PDF olarak kaydetmeyi ve Aspose.CAD for
  Java ile DWG çizimlerine metin eklemeyi adım adım öğrenin—rehber.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: DWG'den PDF Oluşturun ve Aspose.CAD for Java Kullanarak Metin Ekleyin
url: /tr/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'den PDF Oluşturma ve Aspose.CAD for Java Kullanarak Metin Ekleme

## Giriş

Eğer **DWG dosyalarından PDF oluşturmak** ve aynı zamanda özel metin eklemek istiyorsanız doğru yerdesiniz. Bu öğreticide tüm süreci adım adım inceleyeceğiz—DWG çizimini yükleme, bir metin açıklaması ekleme ve son olarak sonucu Aspose.CAD for Java kullanarak PDF olarak kaydetme. Sonunda **DWG'yi PDF olarak kaydetmeyi**, metin yüksekliğini özelleştirmeyi ve temel açıklamalar eklemeyi öğreneceksiniz.

## Hızlı Yanıtlar
- **Java'da DWG'yi PDF'ye dönüştürebilir miyim?** Evet, Aspose.CAD for Java basit bir API sağlar.  
- **Üretim kullanımında lisansa ihtiyacım var mı?** Ticari bir lisans gereklidir; ücretsiz deneme sürümü mevcuttur.  
- **DWG'ye metin ekleyen yöntem hangisidir?** `CadText` nesnesini kullanın ve model alanına ekleyin.  
- **Metin yüksekliğini ayarlayabilir miyim?** Kesinlikle—`CadText` örneği üzerinde `setTextHeight()` kullanın.  
- **Çıktı vektör tabanlı mı?** Rasterleştirme seçenekleri `UseObjectColor` olarak ayarlandığında PDF yüksek kaliteli vektör verisini korur.

## DWG'den PDF Oluşturma Nedir?
DWG çiziminden PDF oluşturmak, yerel CAD formatını geniş çapta desteklenen, yalnızca okunabilir bir belgeye dönüştürmek ve orijinal geometrinin korunmasını sağlamak anlamına gelir. Bu dönüşüm, CAD yazılımı olmayan paydaşlarla tasarımları paylaşmanız gerektiğinde hayati öneme sahiptir.

## DWG'yi PDF'ye Dönüştürmek İçin Neden Aspose.CAD for Java Kullanmalı?
Aspose.CAD, harici bir CAD kurulumuna ihtiyaç duymayan saf Java çözümü sunar. **DWG'yi PDF'ye dönüştürme** özelliğini destekler, vektör bütünlüğünü korur ve dönüşümden önce metin, ölçü veya özel grafikler gibi açıklamaları programlı olarak eklemenize olanak tanır.

## Önkoşullar

Öğreticiye başlamadan önce aşağıdaki önkoşulların sağlandığından emin olun:

- Aspose.CAD for Java Library: Kütüphaneyi [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/) adresinden indirin ve kurun.

- Java Development Kit (JDK): Sisteminizde en son JDK'nın yüklü olduğundan emin olun.

- DWG Çizimi: Metin eklemek istediğiniz bir DWG dosyası hazırlayın.

## Ad Alanlarını İçe Aktarma

Java kodunuzda Aspose.CAD için gerekli ad alanlarını içe aktarın:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Şimdi, sağlanan kod parçacığını birden fazla adıma ayıralım:

## Adım 1: Belge Dizinini ve DWG Dosya Yolunu Ayarlama

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Adım 2: DWG Görüntüsünü Yükleme

```java
Image image = Image.load(dwgPathToFile);
```

## Adım 3: CadText Nesnesi Oluşturma (DWG'ye Metin Ekleme)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Adım 4: CadImage'ye Metin Ekleme (Açıklama Ekleme)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Adım 5: PDF Seçeneklerini Ayarlama (DWG'den PDF Oluşturmak İçin Hazırlık)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Adım 6: CadRasterizationOptions'ı Yapılandırma (PDF Oluşturmayı Kontrol Etme)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Adım 7: Değiştirilmiş DWG'yi PDF Olarak Kaydetme (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Bu adımları izleyerek **DWG'den PDF oluşturabilir**, özel metin ekleyebilir ve metin yüksekliğini kontrol edebilirsiniz—hepsi sadece birkaç satır Java kodu ile.

## Java'da DWG'yi PDF'ye Ölçekli Olarak Nasıl Dönüştürürüm?
**DWG PDF** dosyalarını toplu olarak dönüştürmeniz gerekiyorsa, yukarıdaki kodu bir klasördeki DWG çizimlerini döngüyle işleyen bir yapı içine yerleştirin. `pageHeight`/`pageWidth` değerlerini yalnızca gerektiğinde ayarlayın, böylece bellek kullanımı düşük kalır ve her dosya için aynı `PdfOptions` örneğini yeniden kullanarak performansı artırırsınız.

## Yaygın Sorunlar ve İpuçları

- **Metin görünmüyor mu?** X/Y koordinatlarının çizim sınırları içinde olduğundan ve katmanın görünür olduğundan emin olun.  
- **Yanlış metin yüksekliği?** `setTextHeight()` değerini ayarlayın; değer çizimin birim sisteminde ifade edilir.  
- **PDF rasterleştirilmiş görünüyor mu?** Vektör bilgisini korumak için `CadDrawTypeMode.UseObjectColor` ayarının yapıldığını kontrol edin.  
- **Büyük dosyalarda performans?** `pageHeight`/`pageWidth` değerlerini yalnızca ihtiyaç duyulduğunda artırın; daha büyük değerler daha fazla bellek tüketir.

## Sık Sorulan Sorular

**S: Aspose.CAD tüm DWG sürümleriyle uyumlu mu?**  
C: Aspose.CAD, çeşitli DWG sürümlerini destekler ve geniş bir CAD yazılım yelpazesiyle uyumluluk sağlar.

**S: Eklenen metnin fontunu ve biçimini özelleştirebilir miyim?**  
C: Evet, Aspose.CAD kullanarak DWG dosyalarına eklenen metnin fontunu, stilini ve diğer biçimlendirme seçeneklerini özelleştirebilirsiniz.

**S: Aspose.CAD for Java için ücretsiz deneme mevcut mu?**  
C: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) alarak Aspose.CAD özelliklerini keşfedebilirsiniz.

**S: Aspose.CAD for Java için ayrıntılı belgeleri nereden bulabilirim?**  
C: Derinlemesine bilgi ve örnekler için belgeleri [burada](https://reference.aspose.com/cad/java/) inceleyin.

**S: Aspose.CAD ile ilgili destek veya yardım nasıl alınır?**  
C: Yardım almak ve toplulukla iletişime geçmek için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

---

**Last Updated:** 2026-02-28  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}