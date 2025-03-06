---
title: Aspose.CAD for Java ile DGN'yi DWG'ye aktarın
linktitle: DGN'yi DWG'nin bir parçası olarak dışa aktarın
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java kullanarak DWG'nin bir parçası olarak DGN'yi nasıl dışa aktaracağınızı keşfedin. Verimli CAD dosyası manipülasyonu için adım adım kılavuzumuzu izleyin.
weight: 10
url: /tr/java/dgn-export-options/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java ile DGN'yi DWG'ye aktarın

## giriiş

Bu eğitimde, bir DGN (MicroStation Design) dosyasını bir DWG (AutoCAD Çizimi) dosyasının parçası olarak dışa aktarmak için Aspose.CAD for Java'nın nasıl kullanılacağını keşfedeceğiz. Aspose.CAD, CAD dosya formatlarıyla çalışmak için kapsamlı işlevsellik sağlayan güçlü bir kütüphanedir. Bu adım adım kılavuz, Java kullanarak DWG'nin bir parçası olarak DGN'yi dışa aktarma sürecini anlamanıza yardımcı olacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
1. Aspose.CAD Kütüphanesi: Java için Aspose.CAD kütüphanesini indirip yükleyin. Kütüphaneyi bulabilirsiniz[Burada](https://releases.aspose.com/cad/java/).
2. Java Geliştirme Kiti (JDK): Sisteminizde Java'nın kurulu olduğundan emin olun.
3. Entegre Geliştirme Ortamı (IDE): Daha sorunsuz bir geliştirme deneyimi için Eclipse veya IntelliJ gibi bir Java IDE seçin.

## Paketleri İçe Aktar

CAD dosyası manipülasyonunu etkinleştirmek için Java projenizde gerekli Aspose.CAD paketlerini içe aktarın. İşte bir örnek:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## 1. Adım: Dosya Yollarını Ayarlayın

 DWG dosyası için giriş ve çıkış dosyası yollarını tanımlayın. Güncelleme`dataDir`, `fileName` , Ve`outPath` buna göre değişkenler.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Adım 2: PdfOptions Örneği Oluşturun

 Bir örneğini oluşturun`PdfOptions` DWG dosyasını PDF formatına aktardığımız için sınıf.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Adım 3: DWG Dosyasını Yükleyin

 Mevcut DWG dosyasını resim olarak yükleyin ve`CadImage` tip.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Adım 4: Varlıklar Arasında Yineleme Yapın

DWG dosyasındaki her varlığı gözden geçirin ve bunun bir görüntü tanımı olup olmadığını kontrol edin. Öyleyse, nesnenin dış referansını alın.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Adım 5: Rasterleştirme Seçeneklerini Tanımlayın

 için ayarları tanımlayın`CadRasterizationOptions`sayfa genişliği, yükseklik, düzenler ve arka plan rengi dahil olmak üzere nesne.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Adım 6: Vektör Rasterleştirme Seçeneklerini Ayarlayın

Dışa aktarma için vektör rasterleştirme seçeneklerini ayarlayın.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Adım 7: DWG'yi PDF'ye aktarın

 Son olarak, DWG'yi çağırarak PDF'ye aktarın.`save` yöntem.

```java
cadImage.save(outPath, exportOptions);
```

## Çözüm

Tebrikler! Aspose.CAD for Java kullanarak bir DGN dosyasını bir DWG dosyasının parçası olarak nasıl dışa aktaracağınızı başarıyla öğrendiniz. Bu güçlü kitaplık, CAD dosyalarıyla çalışmak için kapsamlı yetenekler sunarak CAD dosyası işleme görevlerinizi verimli ve basit hale getirir.

## SSS'ler

### S1: Aspose.CAD for Java belgelerini nerede bulabilirim?

 A1: Belgeler bulunabilir[Burada](https://reference.aspose.com/cad/java/).

### S2: Java için Aspose.CAD kütüphanesini nasıl indirebilirim?

 Cevap2: Kütüphaneyi şuradan indirebilirsiniz:[bu bağlantı](https://releases.aspose.com/cad/java/).

### S3: Aspose.CAD for Java'nın ücretsiz deneme sürümü mevcut mu?

 A3: Evet, ücretsiz deneme sürümünü bulabilirsiniz[Burada](https://releases.aspose.com/).

### S4: Aspose.CAD for Java için nereden geçici lisans alabilirim?

 Cevap4: Geçici bir lisans edinin[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Yardıma mı ihtiyacınız var veya sorularınız mı var?

 Cevap5: Aspose.CAD topluluk destek forumunu ziyaret edin[Burada](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
