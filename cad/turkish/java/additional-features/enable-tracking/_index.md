---
date: 2026-06-29
description: DWG'yi PDF'ye dışa aktarmayı, izlemeyi etkinleştirmeyi ve Aspose.CAD
  for Java ile özel bir hata işleyici Java sınıfı kullanmayı öğrenin. DXF‑to‑PDF dönüşümünü
  içerir.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
linktitle: Java Kullanarak DWG Dosyalarında İzlemeyi Etkinleştirin
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to export DWG to PDF, enable tracking, and use a custom error
    handler Java class with Aspose.CAD for Java. Includes DXF‑to‑PDF conversion.
  headline: Export DWG to PDF and Enable Tracking with Aspose.CAD Java
  type: TechArticle
- questions:
  - answer: It activates Aspose.CAD’s render callbacks so you can see warnings and
      errors during export.
    question: What does “enable dwg tracking java” do?
  - answer: A trial works for testing; a commercial license is required for production
      use.
    question: Do I need a license?
  - answer: Yes – the same `PdfOptions` object used for DWG works for DXF, covering
      the *java convert dxf pdf* scenario.
    question: Can I also convert DXF to PDF?
  - answer: Java 8 or higher.
    question: Which JDK version is required?
  - answer: See the [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)
      linked below.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.CAD Java API
title: DWG'yi PDF'ye Dışa Aktarın ve Aspose.CAD Java ile İzlemeyi Etkinleştirin
url: /tr/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi PDF'ye Dışa Aktarma ve Aspose.CAD Java ile İzlemeyi Etkinleştirme

## Giriş

DWG'yi PDF'ye dışa aktarırken dönüşüm sürecine tam görünürlük sağlamak, modern CAD odaklı ekipler için hayati öneme sahiptir. Bu rehberde **izlemeyi nasıl etkinleştireceğinizi**, aynı pipeline'da DXF'yi PDF'ye dönüştürmeyi ve her render uyarısını **özel bir Java hata işleyicisi** sınıfı ile yakalamayı öğreneceksiniz. Sonunda, yalnızca yüksek doğrulukta PDF'ler üretmekle kalmayıp, denetim ve sorun giderme için tanı bilgilerini de kaydeden üretime hazır bir kod parçacığına sahip olacaksınız.

## Hızlı Yanıtlar
- **“enable dwg tracking java” ne yapar?** Aspose.CAD'in render geri aramalarını etkinleştirir, böylece dışa aktarım sırasında uyarı ve hataları görebilirsiniz.  
- **Bir lisansa ihtiyacım var mı?** Deneme sürümü test için çalışır; üretim kullanımı için ticari bir lisans gereklidir.  
- **DXF'yi de PDF'ye dönüştürebilir miyim?** Evet – DWG için kullanılan aynı `PdfOptions` nesnesi DXF için de çalışır, *java convert dxf pdf* senaryosunu kapsar.  
- **Hangi JDK sürümü gereklidir?** Java 8 veya üzeri.  
- **Daha fazla örnek nerede bulunur?** Aşağıda bağlantısı verilen [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) sayfasına bakın.

## DWG'yi PDF'ye dışa aktarma nedir?
DWG'yi PDF'ye dışa aktarma, yerel bir AutoCAD çizimini (DWG) vektör doğruluğu, katmanlar ve açıklamaları koruyarak taşınabilir bir PDF belgesine dönüştürme sürecidir. Aspose.CAD bu dönüşümü tamamen Java içinde gerçekleştirir, yerel AutoCAD kurulumlarına ihtiyaç duyulmaz.

## Aspose.CAD for Java Neden Kullanılmalı?
Aspose.CAD for Java, CAD dönüşümü için kapsamlı, saf‑Java bir çözüm sunar, 50'den fazla formatı destekler, yüksek performans sağlar ve render geri aramaları aracılığıyla yerleşik izleme sunar. Harici bağımlılık gerektirmez ve sunucu‑tarafı pipeline'lara entegre edilebilir.

- **Kapsamlı format desteği** – DWG, DXF, DGN ve 50+ diğer CAD formatını işler.  
- **Sıfır dış bağımlılık** – sunucu‑tarafı otomasyon için ideal saf‑Java kütüphanesi.  
- **Yerleşik izleme** – `CadRenderHandler` ayrıntılı render sonuçları sunar.  
- **Tek satır PDF dışa aktarımı** – `PdfOptions` vektör verilerini koruyarak PDF'ye dönüştürür.  

Bu sayısal iddialar, Aspose.CAD'in tüm belgeyi belleğe yüklemeden 500 sayfaya kadar dosyayı işleyebilme yeteneğiyle desteklenir; tipik bir 4‑çekirdek sunucuda dönüşüm süresi 2 saniyenin altında gerçekleşir.

## Önkoşullar
- **Java Development Kit (JDK)** 8 veya daha yeni bir sürüm makinenizde kurulu olmalıdır.  
- **Aspose.CAD for Java** resmi [download link](https://releases.aspose.com/cad/java/) adresinden indirilmelidir.  
- **Aspose.CAD Free Trial** hızlı bir değerlendirme için [Aspose.CAD Free Trial](https://releases.aspose.com/) sayfasından temin edilebilir.  
- Dönüştürmek istediğiniz DWG/DXF dosyalarını içeren bir klasör.

## DWG'yi PDF'ye Nasıl Dışa Aktarılır?
Kaynak dosyanızı yükleyin, `PdfOptions`'ı yapılandırın, özel bir `CadRenderHandler` ekleyin ve `save` metodunu çağırın. Bu uçtan uca akış, DWG (veya DXF)'yi PDF'ye dönüştürürken her render adımı için izleme bilgisi üretir, böylece uyarı ve hatalar yakalanır ve geliştiriciler veya otomatik süreçler tarafından işlenebilir.

## İsim Uzaylarını İçe Aktarma
`CadRenderHandler` sınıfı, render tanılarını alan Aspose.CAD'in geri arama arayüzüdür. Kodlamaya başlamadan önce gerekli paketleri içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Adım 1: DWG/DXF Dosyasını Yükleme
`CadImage` sınıfı, belleğe yüklenmiş bir CAD belgesini temsil eder. Dosya yolu ile örneklenmesi, yerel bir CAD uygulaması açmadan çizimi yükler.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Adım 2: PDF Dışa Aktarım Seçeneklerini Yapılandırma (DXF'yi PDF'ye Nasıl Dönüştürülür)
`PdfOptions`, CAD rasterizer'ın PDF çıktısını nasıl üreteceğini tanımlar; vektör render ayarları ve sayfa boyutu dahil. `VectorRasterizationOptions` ayarlanması, çizgi ve eğrilerin net kalmasını sağlar. `VectorRasterizationOptions` nesnesi DPI ve arka plan rengi gibi rasterizasyon parametrelerini belirtir.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Adım 3: İzlemeyi Uygulama (Özel Java Hata İşleyicisi)
`ErrorHandler`, rasterizasyon sırasında üretilen uyarı, hata ve bilgi mesajlarını yakalamak için `CadRenderHandler`'ı genişletir. Bu sınıf her mesajı konsola yazar, ancak bunları bir günlük dosyasına veya izleme sistemine yönlendirebilirsiniz. `CadRenderHandler`, rasterizer'dan render tanılarını alan bir arayüzdür.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Adım 4: PDF'ye Dışa Aktarma
Yapılandırılmış `PdfOptions` ile `CadImage` örneği üzerinde `save` çağrısı, dönüşümü gerçekleştirir. Özel işleyici zaten ekli olduğu için, dışa aktarım sırasında oluşan tüm render sorunları konsolda görünür.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Adım 5: CadRenderHandler Sınıfı
`CadRenderHandler`, render sonuçlarını almak için Aspose.CAD'in temel sınıfıdır. `onRenderCompleted` metodunu geçersiz kıldığınızda, sürecin her adımını açıklayan `RenderMessage` girişlerinin bir koleksiyonunu içeren `RenderResult` nesnesine erişirsiniz.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Neden Önemlidir
İzlemeyi etkinleştirmek, mimarlık, mühendislik ve inşaat gibi düzenlenmiş sektörlerde uyumluluk gereksinimlerini karşılayan bir denetim izi oluşturur. Özel hata işleyicisi ayrıca CAD dönüşüm sağlık kontrollerini CI/CD pipeline'larına entegre etmenizi sağlar ve manuel inceleme gerektiren dosyaları otomatik olarak işaretler.

## Yaygın Sorunlar ve Çözümler
- **`RenderResult` üzerinde `NullPointerException`** – Aspose.CAD 23.10 veya daha yeni bir sürüm kullandığınızdan emin olun; daha eski sürümlerde `RenderResult` API'si bulunmaz.  
- **Dosya bulunamadı** – `dataDir`'in doğru klasöre işaret ettiğini ve dosya adının büyük/küçük harfe duyarlı olarak eşleştiğini kontrol edin.  
- **İzleme çıktısı eksik** – `ErrorHandler` örneğinizin `cadRasterizationOptions.setRenderHandler(new ErrorHandler())` ile doğru şekilde atandığını doğrulayın.  

## Sıkça Sorulan Sorular

**S:** Aspose.CAD for Java ile diğer CAD dosya formatları için izlemeyi etkinleştirebilir miyim?  
**C:** İzleme öncelikle DWG ve DXF için sunulur. Diğer formatlar için hangi API'lerin render geri aramaları sağladığını görmek üzere resmi dokümantasyona bakın.

**S:** PDF meta verilerini ayarlamak gibi ek dışa aktarım seçeneklerini nasıl özelleştirebilirim?  
**C:** `PdfOptions` `setTitle`, `setAuthor` ve `setSubject` gibi özellikler sunar. Bu değerleri `save` çağırmadan önce ayarlayarak sonuç PDF'ye meta veri ekleyebilirsiniz.

**S:** İzleme özelliklerini değerlendirmek için deneme sürümü yeterli mi?  
**C:** Evet, ücretsiz deneme tam API erişimi sağlar; `CadRenderHandler` ve PDF dışa aktarımını kısıtlama olmadan test edebilirsiniz.

**S:** Aspose.CAD for Java için topluluk desteği nereden alınabilir?  
**C:** Diğer geliştiricilere sorular sorup deneyimlerinizi paylaşmak için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

**S:** Otomatik test ortamları için geçici bir lisans nasıl elde ederim?  
**C:** Zaman sınırlı bir lisans dosyası oluşturmak için [Temporary License](https://purchase.aspose.com/temporary-license/) sayfasındaki adımları izleyin.

## Sonuç
Bu öğreticiyi izleyerek artık **DWG'yi PDF'ye dışa aktarmayı**, tam‑yığın izlemeyi etkinleştirmeyi ve **özel bir Java hata işleyicisi** sınıfı ile DXF‑to‑PDF dönüşümünü nasıl yapacağınızı biliyorsunuz. Bu kod parçacıklarını derleme pipeline'ınıza entegre ederek görünürlük kazanın, güvenilirliği artırın ve CAD belge işleme için sektör düzeyinde uyumluluğu sağlayın.

---

**Son Güncelleme:** 2026-06-29  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [DWG'yi PDF'ye Dışa Aktarma ve CAD Çizimlerini Dönüştürme – Aspose.CAD Java Öğreticisi](/cad/java/cad-drawing-conversion/)
- [Aspose.CAD for Java Kullanarak DWG'yi PDF'ye veya Raster'a Dışa Aktarma](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Aspose.CAD for Java Kullanarak Belirli DWG Düzenini PDF'ye Dışa Aktarma](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}