---
date: 2026-01-22
description: Aspose.CAD for Java kullanarak CAD'i PDF olarak kaydederken zaman aşımını
  nasıl ayarlayacağınızı öğrenin. Bu adım adım rehberle performansı artırın.
linktitle: Put Timeout on Save
second_title: Aspose.CAD Java API
title: Aspose.CAD ile CAD Kaydetme İşlemine Zaman Aşımı Nasıl Ayarlanır
url: /tr/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD ile CAD Kaydetme İşleminde Zaman Aşımı

## Giriş

Aspose.CAD for Java kullanarak CAD çizimlerini kaydederken **zaman aşımını nasıl ayarlayacağınızı** anlatan öğreticiye hoş geldiniz. Bu rehberde, kaydetme işlemi için zaman aşımı yapılandırma sürecini adım adım göstereceğiz; bu, uygulamanızın yanıt vermesini sağlar ve genel performansı artırır. Aspose.CAD for Java, CAD dosyalarıyla sorunsuz çalışmanızı sağlayan güçlü bir kütüphanedir.

## Hızlı Yanıtlar
- **Zaman aşımı ne işe yarar?** Belirtilen süreyi aşarsa kaydetme işlemini iptal eder, uzun süren takılmaları önler.  
- **Örnekte hangi format kullanılıyor?** CAD çizimi PDF dosyası olarak kaydedilir.  
- **Lisans gerekli mi?** Üretim ortamında geçici veya kalıcı bir Aspose.CAD lisansı gereklidir.  
- **Hangi Java sürümü destekleniyor?** Kod Java 8 ve üzeri sürümlerle çalışır.  
- **Zaman aşımı süresini ayarlayabilir miyim?** Evet—`TimeUnit.SECONDS.sleep(...)` değerini değiştirmeniz yeterlidir.

## Kaydetme İşleminde Zaman Aşımı Nasıl Ayarlanır

### Aspose.CAD bağlamında zaman aşımı nedir?
Zaman aşımı, uzun süren rasterleştirme veya dönüştürme işlemini durduran bir güvenlik önlemidir. Bir `InterruptionTokenSource` sağlayarak, kütüphaneye belirli bir süreden sonra işlemi iptal etmesini söyleyebilir ve uygulamanızın yanıt vermeye devam etmesini sağlayabilirsiniz.

### CAD'i PDF olarak kaydederken neden zaman aşımı ayarlamalıyız?
Büyük veya karmaşık CAD çizimlerini kaydetmek önemli miktarda CPU ve bellek tüketebilir. Zaman aşımı eklemek:
- Uygulamanın donmasını önler.
- Uzun süren görevleri sorunsuz bir şekilde yönetmenizi sağlar.
- Özellikle web veya UI‑odaklı ortamlarda genel kullanıcı deneyimini iyileştirir.

## Ön Koşullar

- **Aspose.CAD for Java Kütüphanesi** – Kütüphanenin projenize entegre edildiğinden emin olun. Kütüphaneyi [web sitesinden](https://releases.aspose.com/cad/java/) indirebilirsiniz.  
- **Geliştirme Ortamı** – JDK 8+ yüklü bir Java IDE'si (IntelliJ, Eclipse vb.).

## Paketleri İçe Aktarma

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Şimdi, örnek kodu adım adım talimatlara ayıralım:

## Adım 1: Kaynak ve Çıktı Dizinlerini Ayarlama

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

CAD çizimleriniz için doğru kaynak ve çıktı dizinlerine sahip olduğunuzdan emin olun.

## Adım 2: Interruption Token Source Oluşturma

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Kaydetme işlemi sırasında kesintileri yönetmek için bir interruption token source başlatın.

## Adım 3: CAD Çizimini Yükleme

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

CAD çizimini bir `CadImage` nesnesine yükleyin.

## Adım 4: Rasterleştirme Seçeneklerini Yapılandırma

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

CAD çizimi için rasterleştirme seçeneklerini yapılandırın.

## Adım 5: PDF Seçeneklerini Yapılandırma

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Vektör rasterleştirme seçenekleri ve interruption token ile PDF seçeneklerini ayarlayın.

## Adım 6: Zaman Aşımıyla Çizimi Kaydetme

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

CAD çizimini belirtilen zaman aşımıyla bir PDF dosyasına kaydedin.

## Adım 7: Kesintiyi Yönetme

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

Kaydetme işlemini yönetmek için bir thread oluşturun ve belirtilen zaman aşımından sonra kesintiye uğratın.

## Yaygın Tuzaklar ve Sorun Giderme

- **Zaman aşımı çok kısa** – Çizim büyükse, çok kısa bir zaman aşımı işlemi bitmeden iptal edebilir. Uyku süresini artırın veya rasterleştirme ayarlarını değiştirin.  
- **Lisans eksik** – Geçerli bir lisans olmadan çalıştırmak bir istisna fırlatır. Kodu çalıştırmadan önce geçici veya kalıcı bir lisans uygulayın.  
- **Yanlış yollar** – `SourceDir` ve `OutputDir` mevcut klasörlere işaret ettiğinden emin olun; aksi takdirde `Image.load` veya `save` başarısız olur.

## Sıkça Sorulan Sorular

**S: Aspose.CAD for Java'ı nasıl indirebilirim?**  
C: [sürümler sayfasından](https://releases.aspose.com/cad/java/) indirebilirsiniz.

**S: Aspose.CAD for Java belgelerini nerede bulabilirim?**  
C: Kapsamlı bilgi için [belgelere](https://reference.aspose.com/cad/java/) bakın.

**S: Ücretsiz deneme mevcut mu?**  
C: Evet, [bu linkten](https://releases.aspose.com/) ücretsiz deneme alabilirsiniz.

**S: Geçici bir lisans nasıl alabilirim?**  
C: Geçici lisans detayları için [burayı](https://purchase.aspose.com/temporary-license/) ziyaret edin.

**S: Yardıma ihtiyacınız var mı ya da sorularınız mı var?**  
C: Topluluk desteği için [Aspose.CAD forumuna](https://forum.aspose.com/c/cad/19) gidin.

## Sonuç

Tebrikler! Artık Aspose.CAD for Java kullanarak CAD çizimlerini PDF'ye dönüştürürken kaydetme işlemlerinde **zaman aşımını nasıl ayarlayacağınızı** biliyorsunuz. Bu zaman aşımını uygulamak, CAD ile ilgili uygulamalarınızın güvenilirliğini ve yanıt verebilirliğini artırır.

---

**Son Güncelleme:** 2026-01-22  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.11 (latest)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}