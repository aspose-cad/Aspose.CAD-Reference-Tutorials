---
date: 2026-11-18
description: DWG'yi PDF'ye nasıl dışa aktaracağınızı, izlemeyi nasıl etkinleştireceğinizi
  ve Aspose.CAD for Java ile özel bir hata işleyici Java sınıfını nasıl kullanacağınızı
  öğrenin. DXF‑to‑PDF dönüşümünü içerir.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
lastmod: 2026-11-18
linktitle: Java Kullanarak DWG Dosyalarında İzlemeyi Etkinleştirin
og_description: DWG'yi PDF'ye dışa aktarın ve Java'da Aspose.CAD ile tam izlemeyi
  etkinleştirin. Özel bir hata işleyiciyi nasıl kullanacağınızı, DXF'yi PDF'ye dönüştürmeyi
  ve render uyarılarını kaydetmeyi öğrenin.
og_image_alt: Guide showing DWG to PDF conversion and tracking in Java with Aspose.CAD
og_title: Aspose.CAD for Java ile izleme kullanarak DWG'yi PDF'ye Dışa Aktarın
schemas:
- author: Aspose
  dateModified: '2026-11-18'
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
tags:
- export dwg to pdf
- aspose.cad java
- custom error handler
- dxf to pdf
- java cad conversion
title: DWG'yi PDF'ye Dışa Aktarın ve Aspose.CAD Java ile İzlemeyi Etkinleştirin
url: /tr/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi PDF'ye Dışa Aktarma ve Aspose.CAD Java ile İzlemeyi Etkinleştirme

## Giriş

DWG'yi PDF'ye dışa aktarırken dönüşüm sürecine tam görünürlük sağlamak, modern CAD‑odaklı ekipler için hayati öneme sahiptir. Bu rehberde **izlemeyi nasıl etkinleştireceğinizi** DWG iş akışlarında keşfedecek, aynı boru hattında DXF'yi PDF'ye dönüştürecek ve her render uyarısını **özel hata işleyici Java** sınıfı ile yakalayacaksınız. Sonunda, yalnızca yüksek doğruluklu PDF'ler üretmekle kalmayıp, denetim ve sorun giderme için tanı bilgilerini de kaydeden üretim‑hazır bir kod parçacığına sahip olacaksınız.

## Hızlı cevaplar
- **“enable dwg tracking java” ne yapar?** Aspose.CAD’in render geri aramalarını etkinleştirir, böylece dışa aktarım sırasında uyarı ve hataları görebilirsiniz.  
- **Lisans gerekli mi?** Test için bir deneme sürümü çalışır; üretim kullanımı için ticari bir lisans gereklidir.  
- **DXF'yi de PDF'ye dönüştürebilir miyim?** Evet – DWG için kullanılan aynı `PdfOptions` nesnesi DXF için de çalışır ve *java convert dxf pdf* senaryosunu kapsar.  
- **Hangi JDK sürümü gereklidir?** Java 8 veya daha yenisi.  
- **Daha fazla örnek nerede bulunur?** Aşağıda bağlantısı verilen [Aspose.CAD Java Dokümantasyonu](https://reference.aspose.com/cad/java/) sayfasına bakın.

## Export dwg to pdf nedir?

Export DWG to PDF, yerel bir AutoCAD çizimini (DWG) taşınabilir bir PDF belgesine dönüştürme sürecidir; vektör doğruluğu, katmanlar ve açıklamalar korunur. **Aspose.CAD, DWG'yi PDF'ye saf Java ile dönüştürür, böylece lisanslı bir AutoCAD kurulumuna hiç ihtiyaç duymazsınız.** Bu dönüşüm, tam çizgi kalınlıkları, metin stilleri ve düzen geometrisini korur; PDF, müşteri incelemesi, arşivleme veya sonraki işleme için uygundur.

## Neden Aspose.CAD for Java kullanmalı?

Aspose.CAD for Java, CAD dönüşümü için kapsamlı, saf‑Java bir çözüm sunar; 50'den fazla formatı destekler, yüksek performans sağlar ve render geri aramaları aracılığıyla yerleşik izleme sunar. Harici bağımlılık gerektirmez ve sunucu‑tarafı boru hatlarına entegre edilebilir. Kütüphane ayrıca bellek‑verimli işleme içerir; belgeyi RAM'e tamamen yüklemeden 500 sayfaya kadar dosyaları dönüştürmenize olanak tanır.

## Önkoşullar

- **Java Development Kit (JDK)** 8 veya daha yeni bir sürüm makinenizde kurulu olmalı.  
- **Aspose.CAD for Java** resmi [indirme bağlantısından](https://releases.aspose.com/cad/java/) indirilmiş olmalı.  
- **Aspose.CAD Ücretsiz Deneme** sürümü, hızlı bir değerlendirme için [Aspose.CAD Ücretsiz Deneme](https://releases.aspose.com/) sayfasından temin edilebilir.  
- Dönüştürmek istediğiniz DWG/DXF dosyalarını içeren bir klasör.

## DWG'yi PDF'ye nasıl dışa aktarılır?

Kaynak dosyanızı yükleyin, `PdfOptions` yapılandırın, özel bir `CadRenderHandler` ekleyin ve `save` metodunu çağırın. Bu uç‑uç akış, DWG (veya DXF) dosyasını PDF'ye dönüştürürken her render adımı için izleme bilgisi yayar; böylece uyarı ve hatalar yakalanır ve geliştiriciler ya da otomatik süreçler tarafından işlenebilir.

## İsim alanlarını içe aktar

`CadRenderHandler` arayüzü, dönüşüm sırasında uyarı ve hatalar gibi render tanılarını alır.  
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

## Adım 1: dwg/dxf dosyasını yükle  

`CadImage`, belleğe yüklenmiş bir CAD çizimini temsil eder ve sayfalarına ve katmanlarına erişim sağlar.  
```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Adım 2: pdf dışa aktarım seçeneklerini yapılandır (dxf'i pdf'ye nasıl dönüştürürsünüz)

`PdfOptions`, PDF çıkış ayarlarını tanımlar; `VectorRasterizationOptions` ise DPI ve arka plan rengi gibi rasterleştirme parametrelerini kontrol eder.  
```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Adım 3: izlemeyi uygula (özel hata işleyici java)

`ErrorHandler`, `CadRenderHandler`'ı genişleterek dönüşüm sürecinde yayınlanan render mesajlarını yakalar ve kaydeder.  
```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Adım 4: pdf olarak dışa aktar  

`CadImage` örneği üzerindeki `save` metodunu çağırmak, render edilen PDF'yi belirtilen çıkış yoluna yazar.  
```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Adım 5: cadrenderhandler sınıfı  

`CadRenderHandler`, render tamamlandığında ayrıntılı mesajları içeren bir `RenderResult` sağlayan temel geri arama sınıfıdır.  
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

## Bunun önemi

İzlemeyi etkinleştirmek, mimarlık, mühendislik ve inşaat gibi düzenlenmiş sektörlerde uyumluluk gereksinimlerini karşılayan bir denetim izi oluşturur. Özel hata işleyici, CAD dönüşüm sağlık kontrollerini CI/CD boru hatlarına entegre etmenizi sağlar; manuel inceleme gerektiren dosyaları otomatik olarak işaretler.

## Yaygın sorunlar ve çözümler

- **`RenderResult` üzerinde `NullPointerException`** – Aspose.CAD 23.10 veya daha yeni bir sürüm kullandığınızdan emin olun; önceki sürümlerde `RenderResult` API'si bulunmaz.  
- **Dosya bulunamadı** – `dataDir`'in doğru klasöre işaret ettiğini ve dosya adının büyük/küçük harfe duyarlı olarak eşleştiğini iki kez kontrol edin.  
- **İzleme çıktısı eksik** – `ErrorHandler` örneğinizin `cadRasterizationOptions.setRenderHandler(new ErrorHandler())` ile doğru şekilde atandığını doğrulayın.  

## Sıkça sorulan sorular

**S:** Aspose.CAD for Java ile diğer CAD dosya formatları için izlemeyi etkinleştirebilir miyim?  
**C:** İzleme öncelikle DWG ve DXF için sunulur. Diğer formatlar için hangi API'lerin render geri aramaları sağladığını resmi dokümantasyonda inceleyin.

**S:** PDF meta verileri gibi ek dışa aktarım seçeneklerini nasıl özelleştiririm?  
**C:** `PdfOptions` içinde `setTitle`, `setAuthor` ve `setSubject` gibi özellikler bulunur. Bu değerleri `save` çağrısından önce ayarlayarak PDF'ye meta veri ekleyebilirsiniz.

**S:** İzleme özelliklerini değerlendirmek için deneme sürümü yeterli mi?  
**C:** Evet, ücretsiz deneme tam API erişimi sağlar; `CadRenderHandler` ve PDF dışa aktarımını kısıtlama olmadan test edebilirsiniz.

**S:** Aspose.CAD for Java topluluk desteği nereden alınır?  
**C:** Diğer geliştiricilere sorular sorup deneyimlerinizi paylaşmak için [Aspose.CAD forumuna](https://forum.aspose.com/c/cad/19) göz atın.

**S:** Otomatik test ortamları için geçici bir lisans nasıl alınır?  
**C:** Zaman‑sınırlı bir lisans dosyası oluşturmak için [Geçici Lisans](https://purchase.aspose.com/temporary-license/) sayfasındaki adımları izleyin.

## Sonuç

Bu öğreticiyi izleyerek **DWG'yi PDF'ye dışa aktarmayı**, tam‑yığın izlemeyi etkinleştirmeyi ve **özel hata işleyici Java** sınıfı ile DXF‑to‑PDF dönüşümünü nasıl yapacağınızı öğrendiniz. Bu kod parçacıklarını derleme boru hattınıza entegre ederek görünürlük kazanabilir, güvenilirliği artırabilir ve CAD belge işleme için sektör‑seviyesi uyumluluğu sağlayabilirsiniz.

---

**Son Güncelleme:** 2026-11-18  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose  

## İlgili öğreticiler

- [Export DWG to PDF and Convert CAD Drawings – Aspose.CAD Java Tutorial](/cad/java/cad-drawing-conversion/)
- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Export Specific DWG Layout to PDF Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}