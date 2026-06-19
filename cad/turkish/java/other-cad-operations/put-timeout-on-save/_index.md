---
date: 2026-06-19
description: Aspose.CAD for Java ile CAD çizimlerini kaydederken timeout nasıl ayarlanacağını
  öğrenin. Performansı artırın, takılmaları önleyin ve CAD'i PDF'ye verimli bir şekilde
  dışa aktarın.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: Kaydetme İşlemine Timeout Ekle
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Aspose.CAD ile CAD Kaydetme İşlemine Timeout Nasıl Ayarlanır
url: /tr/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD ile CAD Kaydetme İşleminde Zaman Aşımını Ayarlama

## Giriş

Bu kapsamlı rehberde, Aspose.CAD for Java kullanarak CAD çizimlerini kaydederken **zaman aşımını nasıl ayarlayacağınızı** öğreneceksiniz. Zaman aşımı uygulamak, uzun süren kaydetme işlemlerinin uygulamanızı kilitlemesini önler; bu, **CAD'i PDF olarak dışa aktarmanız** veya **DWG'yi PDF'ye dönüştürmeniz** gerektiğinde toplu iş senaryolarında özellikle önemlidir. Aspose.CAD for Java, 50'den fazla CAD formatını destekler ve tüm belgeyi belleğe yüklemeden çok sayfalı dosyaları işleyebilir, böylece öngörülebilir performans ve kaynak kullanımı sağlar.

## Hızlı Yanıtlar
- **Zaman aşımı ne işe yarar?** Belirtilen süreden sonra kaydetme işlemini iptal eder, iş parçacığını serbest bırakır ve kaynak sızıntılarını önler.  
- **Zaman aşımını kontrol eden sınıf hangisidir?** `InterruptionTokenSource`, kaydetme rutininde kullanılan iptal tokenını sağlar.  
- **Zaman aşımından sonra hâlâ CAD'i PDF olarak dışa aktarabilir miyim?** Evet – kesinti istisnasını yakalayabilir, yeniden deneyebilir veya hatayı kaydedebilirsiniz.  
- **Özel bir lisansa ihtiyacım var mı?** Normal bir Aspose.CAD lisansı yeterlidir; zaman aşımı özelliği yerleşiktir.  
- **Bu yaklaşım iş parçacığı güvenli mi?** Evet, her kaydetme kendi iş parçacığında ve kendi tokenı ile çalıştığında güvenlidir.

## CAD Kaydetme İşlemlerinde Zaman Aşımı Nedir?
Zaman aşımı, aşıldığında kaydetme sürecini durduran ve bir kesinti istisnası yükselten yapılandırılabilir bir zaman sınırıdır. Bu, karmaşık çizimler veya I/O darboğazları nedeniyle Java uygulamanızın süresiz olarak takılmasını önler.

## CAD Dosyalarını Kaydederken Neden Zaman Aşımı Ayarlamalısınız?
Aspose.CAD, tipik çizimler için **DWG'yi PDF'ye dönüştürme** ve **CAD'i PDF olarak dışa aktarma** işlemlerini bir saniyeden kısa sürede gerçekleştirebilir, ancak aşırı büyük veya bozuk dosyalar dakikalar sürebilir. Bir zaman aşımı tanımlayarak, örneğin 30 saniyeyi aşmayacağını garanti eder ve toplu iş verimliliğini istikrarlı tutar, iş parçacığı açlığını önlersiniz.

## Ön Koşullar

Öğreticiye başlamadan önce aşağıdaki ön koşulların yerine getirildiğinden emin olun:
- **Aspose.CAD for Java Library** – Projenize Aspose.CAD for Java kütüphanesini entegre ettiğinizden emin olun. Kütüphaneyi [website](https://releases.aspose.com/cad/java/) adresinden indirebilirsiniz.  
- **Development Environment** – Gerekli tüm araç ve bağımlılıklarla Java geliştirme ortamınızı kurun.

## Paketleri İçe Aktarma

Başlamak için gerekli paketleri Java projenize içe aktarın. Java dosyanızın başına aşağıdaki satırları ekleyin:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Şimdi örnek kodu adım adım talimatlara ayıralım:

## CAD Çizimlerini Kaydederken Zaman Aşımını Nasıl Ayarlarsınız?

CAD dosyanızı yükleyin, istediğiniz zaman aşımıyla bir `InterruptionTokenSource` oluşturun ve tokenı PDF kaydetme seçeneklerine geçirin. İşlem zaman aşımını aşarsa, Aspose.CAD bir `OperationCanceledException` fırlatır; bu istisnayı yakalayarak hatayı nazikçe işleyebilirsiniz.

### Adım 1: Kaynak ve Çıktı Dizinlerini Ayarlama

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

CAD çizimleriniz için doğru kaynak ve çıktı dizinlerine sahip olduğunuzdan emin olun.

### Adım 2: Kesinti Token Kaynağı Oluşturma

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Kaydetme işlemi sırasında kesintileri yönetmek için bir kesinti token kaynağı başlatın.

### Adım 3: CAD Çizimini Yükleme

`CadImage` sınıfı, Aspose.CAD'in bellek içindeki bir CAD çizimini temsil eden temel nesnesidir; render ve dönüşüm metodları sunar.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### Adım 4: Rasterleştirme Seçeneklerini Yapılandırma

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

CAD çizimi için rasterleştirme seçeneklerini yapılandırın.

### Adım 5: PDF Seçeneklerini Yapılandırma

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Vektör rasterleştirme seçenekleri ve kesinti tokenı ile PDF seçeneklerini ayarlayın.

### Adım 6: Çizimi Zaman Aşımıyla Kaydetme

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Belirtilen zaman aşımıyla CAD çizimini bir PDF dosyasına kaydedin.

### Adım 7: Kesintiyi İşleme

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

Kaydetme işlemini yönetecek bir iş parçacığı oluşturun ve belirtilen zaman aşımından sonra kesintiye uğratın.

## Yaygın Sorunlar ve Çözümler

- **Zaman Aşımı Çok Kısa** – Sık sık kesintiler alıyorsanız, daha büyük çizimler için zaman aşımı değerini artırın.  
- **InterruptedException Yakalanmadı** – Uygulamanın çökmesini önlemek için kaydetme çağrısını her zaman `OperationCanceledException` için bir try‑catch bloğuna sarın.  
- **Bellek Tüketimi** – Tüm dosyayı belleğe yüklemek yerine çıktıyı akış olarak göndermek için `PdfOptions.setVectorRasterizationOptions` kullanın.

## Sıkça Sorulan Sorular

**S: Bu özelliği toplu işte DWG'yi PDF'ye dönüştürmek için kullanabilir miyim?**  
C: Evet, her dönüşümü ayrı bir iş parçacığında ve ayrı bir kesinti tokenı ile sararak dosya başına zaman sınırları uygulayabilirsiniz.

**S: Zaman aşımı tüm çıktı formatlarında çalışıyor mu?**  
C: Zaman aşımı mekanizması `InterruptionTokenSource` ile ilişkilidir ve PDF, PNG, SVG gibi tokenı tanıyan tüm formatlarla çalışır.

**S: Zaman aşımından sonra kısmen yazılmış dosyalar ne olur?**  
C: Aspose.CAD eksik çıktıyı otomatik olarak siler, böylece bozuk PDF dosyalarıyla karşılaşmazsınız.

**S: Üretim ortamında lisans gerekli mi?**  
C: Evet, ticari dağıtımlar için geçerli bir Aspose.CAD lisansı gerekir; değerlendirme için ücretsiz deneme sürümü mevcuttur.

**S: Kesinti tokenlarıyla ilgili daha fazla örnek nerede bulunur?**  
C: Resmi Aspose.CAD belgeleri ek kod parçacıkları ve en iyi uygulama yönergeleri sunar.

## Ek Kaynaklar

- [releases page](https://releases.aspose.com/cad/java/) – En son Aspose.CAD for Java sürümlerinin doğrudan indirme sayfası.  
- [documentation](https://reference.aspose.com/cad/java/) – Tam API referansı ve geliştirici kılavuzları.  
- [this link](https://releases.aspose.com/) – Genel Aspose ürün sürümleri.  
- [here](https://purchase.aspose.com/temporary-license/) – Test için geçici lisans alın.  
- [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) – Topluluk desteği ve tartışmalar.

## Sonuç

Artık Aspose.CAD for Java ile CAD çizimlerini kaydederken **zaman aşımını nasıl ayarlayacağınızı** öğrendiniz. İş akışınıza bir `InterruptionTokenSource` entegre ederek **CAD'i PDF olarak dışa aktarma** veya **DWG'yi PDF'ye dönüştürme** işlemlerini uzun süren takılma riskine maruz kalmadan güvenilir bir şekilde gerçekleştirebilir, uygulamanızın yanıt verebilirliğini ve ölçeklenebilirliğini koruyabilirsiniz.

---

**Last Updated:** 2026-06-19  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Eğitimler

- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Export Specific DWG Layout to PDF Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Convert DWG to PNG and Other Raster Formats Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}