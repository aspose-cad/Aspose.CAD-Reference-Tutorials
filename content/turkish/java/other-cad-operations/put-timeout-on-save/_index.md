---
title: Aspose.CAD ile CAD için Kaydetmede Zaman Aşımı
linktitle: Kaydetmeye Zaman Aşımı koy
second_title: Aspose.CAD Java API'si
description: Aspose.CAD ile Java uygulamanızın performansını nasıl artıracağınızı öğrenin. CAD çizimlerini kaydetmeye zaman aşımı koyun. Adım adım kılavuzumuzu takip edin.
type: docs
weight: 15
url: /tr/java/other-cad-operations/put-timeout-on-save/
---
## giriiş

Aspose.CAD for Java kullanarak kaydetmeye zaman aşımı koyma eğitimine hoş geldiniz. Bu kılavuzda, uygulamanızın performansını artırmak amacıyla CAD çizimlerini kaydetmek için zaman aşımı ayarlama sürecinde size yol göstereceğiz. Aspose.CAD for Java, Java uygulamalarınızdaki CAD dosyalarıyla sorunsuz bir şekilde çalışmanıza olanak tanıyan güçlü bir kütüphanedir.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:
-  Aspose.CAD for Java Library: Aspose.CAD for Java kütüphanesinin projenize entegre olduğundan emin olun. Kütüphaneyi adresinden indirebilirsiniz.[İnternet sitesi](https://releases.aspose.com/cad/java/).
- Geliştirme Ortamı: Gerekli tüm araç ve bağımlılıklarla Java geliştirme ortamınızı kurun.

## Paketleri İçe Aktar

Başlamak için gerekli paketleri Java projenize aktarın. Java dosyanızın başına aşağıdaki satırları ekleyin:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Şimdi örnek kodu adım adım talimatlara ayıralım:

## Adım 1: Kaynak ve Çıkış Dizinlerini Ayarlayın

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

CAD çizimleriniz için doğru kaynak ve çıktı dizinlerine sahip olduğunuzdan emin olun.

## Adım 2: Kesinti Belirteci Kaynağı Oluşturun

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Kaydetme işlemi sırasında kesintileri yönetmek için bir kesinti belirteci kaynağı başlatın.

## Adım 3: CAD Çizimini Yükleyin

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 CAD çizimini bir`CadImage` nesne.

## Adım 4: Rasterleştirme Seçeneklerini Yapılandırın

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

CAD çizimi için rasterleştirme seçeneklerini yapılandırın.

## Adım 5: PDF Seçeneklerini Yapılandırın

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Vektör rasterleştirme seçenekleri ve kesinti belirteciyle PDF seçeneklerini ayarlayın.

## Adım 6: Çizimi Zaman Aşımı ile Kaydet

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

CAD çizimini belirtilen zaman aşımı süresiyle bir PDF dosyasına kaydedin.

## Adım 7: Kesintiyi Önleyin

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Kaydetme işlemini gerçekleştirecek bir iş parçacığı oluşturun ve belirli bir zaman aşımından sonra işlemi kesintiye uğratın.

## Çözüm

Tebrikler! Aspose.CAD for Java'yı kullanarak kaydetmeye nasıl zaman aşımı koyacağınızı başarıyla öğrendiniz. Bu özellik CAD ile ilgili uygulamalarınızın verimliliğini büyük ölçüde artırabilir.

## SSS'ler

### S1: Aspose.CAD for Java'yı nasıl indirebilirim?

 A1: Bunu şuradan indirebilirsiniz:[sürümler sayfası](https://releases.aspose.com/cad/java/).

### S2: Aspose.CAD for Java belgelerini nerede bulabilirim?

 A2: Bkz.[dokümantasyon](https://reference.aspose.com/cad/java/) kapsamlı bilgi için.

### S3: Ücretsiz deneme sürümü mevcut mu?

C3: Evet, şu adresten ücretsiz deneme alabilirsiniz:[bu bağlantı](https://releases.aspose.com/).

### S4: Geçici lisansı nasıl edinebilirim?

 A4: Ziyaret edin[Burada](https://purchase.aspose.com/temporary-license/) geçici lisans ayrıntıları için.

### S5: Yardıma mı ihtiyacınız var veya sorularınız mı var?

 A5: Şuraya gidin:[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği için.