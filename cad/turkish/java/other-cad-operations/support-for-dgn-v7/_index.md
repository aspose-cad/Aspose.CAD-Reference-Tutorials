---
title: DGN'den PDF'ye Dönüştürme Kılavuzu - Aspose.CAD for Java
linktitle: DGN V7 desteği
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java'yı kullanarak DGN dosyalarını zahmetsizce PDF'ye dönüştürün. Sorunsuz entegrasyon ve verimli iş akışı için adım adım kılavuzumuzu izleyin.
type: docs
weight: 11
url: /tr/java/other-cad-operations/support-for-dgn-v7/
---
## giriiş

CAD'nin (Bilgisayar Destekli Tasarım) dinamik dünyasında, DGN (Tasarım) dosyalarının PDF'ye (Taşınabilir Belge Formatı) verimli bir şekilde dönüştürülmesi çok önemli bir gerekliliktir. Aspose.CAD for Java, kesintisiz entegrasyon ve sağlam yetenekler sunan güçlü bir çözüm olarak ortaya çıkıyor. Bu adım adım kılavuz, Aspose.CAD for Java kullanarak DGN dosyalarını PDF'ye aktarma sürecinde size yol göstererek sorunsuz ve verimli bir iş akışı sağlamayı amaçlamaktadır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:
-  Aspose.CAD for Java Library: Kütüphaneyi şuradan indirip yükleyin:[Java için Aspose.CAD İndirme sayfası](https://releases.aspose.com/cad/java/).
- Java Geliştirme Ortamı: Makinenizde bir Java geliştirme ortamının kurulu olduğundan emin olun.

## Paketleri İçe Aktar

Gerekli paketleri Java projenize aktararak başlayın:

## Adım 1: Gerekli Paketleri İçe Aktarın

Java projenizde Aspose.CAD for Java için gerekli paketleri içe aktarın.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## 2. Adım: Dosya Yollarını Ayarlayın

Giriş DGN dosyanızın ve çıktı PDF dosyanızın yollarını tanımlayın.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## 3. Adım: DGN Görüntüsünü Yükleyin

Aspose.CAD kütüphanesini kullanarak DGN görüntüsünü yükleyin.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## 4. Adım: PDF Dışa Aktarma Seçeneklerini Yapılandırın

Sayfa boyutları, otomatik düzen ölçeklendirme, arka plan rengi ve dışa aktarılacak belirli düzenler de dahil olmak üzere PDF'ye dışa aktarma seçeneklerini ayarlayın.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //yalnızca 4 (1,2,3 ve 9) görünümü dışa aktar
options.setVectorRasterizationOptions(vectorOptions);
```

## Adım 5: PDF Dosyasını Kaydet

DGN görüntüsünü belirtilen seçeneklerle PDF dosyası olarak kaydedin.

```java
objImage.save(outFile, options);
```

Dosya yollarını ve seçeneklerini gerektiği gibi ayarlayarak bu adımları farklı DGN dosyaları için tekrarlayın.

## Çözüm

Aspose.CAD for Java ile DGN dosyalarını PDF'ye dönüştürmek basit bir süreç haline geliyor. Bu kılavuz, kitaplığı Java projelerinize sorunsuz bir şekilde entegre etme bilgisiyle donatır ve verimli CAD dosya dönüştürmelerini kolaylaştırır.

## SSS'ler

### S1: Aspose.CAD for Java'yı diğer CAD dosya formatlarıyla kullanabilir miyim?

Cevap1: Evet, Aspose.CAD çeşitli CAD formatlarını destekleyerek DGN'den PDF'ye dönüştürmenin ötesinde çok yönlü işlevsellik sağlar.

### S2: Aspose.CAD for Java için geçici bir lisans mevcut mu?

 Cevap2: Evet, geçici lisans alabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/) test amaçlı.

### S3: Aspose.CAD for Java hakkında nasıl destek alabilirim veya soru sorabilirim?

 A3: Ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19)toplulukla bağlantı kurmak ve yardım istemek.

### S4: DGN'yi PDF'ye dönüştürürken hangi düzenleri dışa aktarabilirim?

 Cevap4: Dışa aktarılacak düzenleri özelleştirerek belirleyebilirsiniz.`setLayouts` koddaki dizi.

### S5: Aspose.CAD for Java'nın kapsamlı belgelerini nerede bulabilirim?

 A5: Bkz.[Java belgeleri için Aspose.CAD](https://reference.aspose.com/cad/java/) detaylı bilgi için.