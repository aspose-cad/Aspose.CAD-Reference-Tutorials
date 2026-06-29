---
date: 2026-02-10
description: Aspose.CAD for Java kullanarak DWG dosyalarında izlemeyi etkinleştirme
  ve DXF'yi özel bir hata işleyicisiyle PDF'ye dönüştürme adım adım rehberi.
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Java'da Aspose.CAD Kullanarak DWG Dosyalarında İzlemeyi Nasıl Etkinleştirirsiniz
url: /tr/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java’da Aspose.CAD ile DWG Dosyalarında İzlemeyi Etkinleştirme

## Giriş

Eğer ortak CAD projeleri üzerinde çalışıyorsanız, **DWG iş akışınızda izlemeyi etkinleştirmenin** nasıl yapılacağını bilmek büyük bir fark yaratır. Gerçek zamanlı olarak render sorunlarını görmenizi sağlar, dönüşüm hatalarını erken yakalamanıza yardımcı olur ve tüm paydaşları bilgilendirir. Bu öğreticide, Aspose.CAD for Java ile izlemeyi etkinleştirmenin tam adımlarını gösterecek ve aynı pipeline içinde **DXF’yi PDF’ye nasıl dönüştüreceğinizi** de göstereceğiz. Sonunda, çizimlerinizi dışa aktarırken **özel hata işleyici Java** sınıfı aracılığıyla hataları raporlayan, üretime hazır bir kod parçacığına sahip olacaksınız.

## Hızlı Yanıtlar
- **“enable dwg tracking java” ne yapar?** Aspose.CAD’in hata‑işleme geri çağrılarını etkinleştirir, böylece dışa aktarım sırasında render sorunlarını görebilirsiniz.  
- **Lisans gerekli mi?** Test için bir deneme sürümü yeterlidir; üretim için ticari lisans gerekir.  
- **DXF’yi PDF’ye de dönüştürebilir miyim?** Evet – DWG için kullanılan aynı `PdfOptions` DXF için de çalışır, *java convert dxf pdf* senaryosunu karşılar.  
- **Hangi JDK sürümü gerekir?** Java 8 veya üzeri.  
- **Daha fazla örnek nerede?** Aşağıdaki Aspose.CAD Java Dokümantasyonuna bakın.

## Java’da Aspose.CAD ile DWG Dosyalarında İzlemeyi Etkinleştirme

Java uygulamasında DWG izlemeyi etkinleştirmek, CAD dosyası rasterleştirilirken veya dışa aktarılırken uyarı, hata ve diğer tanı bilgilerini yakalayan özel bir render işleyicisi eklemek anlamına gelir. Bu görünürlük, geliştiricilerin dönüşüm hatlarını ayıklamasına yardımcı olur ve daha yüksek kalite teslimatlar sağlar.

## Neden Aspose.CAD for Java Kullanmalı?

- **Tam özellikli CAD desteği** – DWG, DXF, DGN ve daha fazlası.  
- **Harici bağımlılık yok** – saf Java kütüphanesi, sunucu‑tarafı otomasyon için ideal.  
- **Yerleşik izleme** – `CadRenderHandler` aracılığıyla ayrıntılı render sonuçları.  
- **Kolay PDF dışa aktarımı** – vektör verisini koruyarak tek satırla dönüşüm.  

## Ön Koşullar

Uygulamaya geçmeden önce aşağıdaki ön koşulların sağlandığından emin olun:

- Java Development Kit (JDK): Sisteminizde Java yüklü olmalı.  
- Aspose.CAD for Java: [indirme bağlantısı](https://releases.aspose.com/cad/java/) üzerinden Aspose.CAD for Java’ı indirin ve kurun.  
- Belge Dizini: DWG dosyalarınızın bulunduğu bir dizin hazırlayın.

## İsim Uzaylarını İçe Aktarma

Java projenizde Aspose.CAD işlevlerini kullanmak için gerekli isim uzaylarını içe aktararak başlayın:

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

## Adım 1: DWG Dosyasını Yükleme

DWG (veya DXF) dosyasını Java uygulamanıza yükleyin. Dosya yolunu buna göre ayarlayın:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Adım 2: PDF Dışa Aktarım Seçeneklerini Yapılandırma (DXF’yi PDF’ye Dönüştürme)

PDF dışa aktarım seçeneklerini ayarlayın, CAD için vektör rasterleştirme seçeneklerini belirtin. Bu aynı zamanda *java convert dxf pdf* yeteneğini gösterir:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Adım 3: İzlemeyi Uygulama (Özel Hata İşleyici Java)

İzlemeyi, özel bir hata işleyici sınıfı kullanarak uygulayın. Bu sınıf render sorunlarını yakalar ve konsola yazar:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Adım 4: PDF’ye Dışa Aktarma

İzleme etkinleştirilmiş şekilde DWG/DXF dosyasını PDF’ye dönüştürmek için dışa aktarım sürecini başlatın:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Adım 5: CadRenderHandler Sınıfı

Render sonuçlarını işlemek ve izleme bilgilerini çıkarmak için `ErrorHandler` sınıfını (`CadRenderHandler`’ı genişleterek) tanımlayın:

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

## Bunun Önemi Nedir?

İzlemeyi etkinleştirerek her dönüşüm adımının net bir denetim izini elde edersiniz. Bu, özellikle mimarlık, mühendislik, inşaat gibi düzenlemeye tabi sektörlerde, doğru render kanıtının uyum denetimleri için gerekli olduğu durumlarda çok değerlidir. Özel hata işleyici, sorunları bir izleme sistemine kaydetmek veya otomatik yeniden denemeleri tetiklemek için bir kanca da sağlar.

## Yaygın Sorunlar ve Çözümleri

- **`RenderResult` üzerinde `NullPointerException`** – Aspose.CAD 23.10 veya daha yeni bir sürüm kullandığınızdan emin olun; eski sürümlerde `RenderResult` API’si bulunmaz.  
- **Dosya bulunamadı** – `dataDir`’in doğru klasöre işaret ettiğini ve dosya adının büyük/küçük harf duyarlılığıyla tam eşleştiğini kontrol edin.  
- **İzleme çıktısı eksik** – Özel `ErrorHandler`’ın `cadRasterizationOptions.RenderResult`’a doğru şekilde atandığını doğrulayın.

## Sık Sorulan Sorular

**S:** Aspose.CAD for Java ile diğer CAD dosya formatları için de izleme etkinleştirebilir miyim?  
**C:** Aspose.CAD öncelikle DWG izlemeyi destekler. Diğer formatlar için resmi dokümantasyona bakın.

**S:** Aspose.CAD for Java’da ek dışa aktarım seçeneklerini nasıl yönetebilirim?  
**C:** Geniş dokümantasyonu [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) adresinde inceleyin.

**S:** Aspose.CAD for Java için bir deneme sürümü var mı?  
**C:** Evet, deneme sürümüne [Aspose.CAD Free Trial](https://releases.aspose.com/) üzerinden ulaşabilirsiniz.

**S:** Aspose.CAD for Java ile ilgili destek almak veya sorunları tartışmak için nereden yardım alabilirim?  
**C:** Topluluk desteği için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

**S:** Aspose.CAD for Java için geçici bir lisans nasıl alınır?  
**C:** [Temporary License](https://purchase.aspose.com/temporary-license/) sayfasındaki adımları izleyin.

## Sonuç

Aspose.CAD ile Java’da DWG izlemeyi etkinleştirmek, dönüşüm sorunlarına dair görünürlük sağlamakla kalmaz, aynı zamanda ortak tasarım iş akışlarını da kolaylaştırır. Yukarıdaki adımları izleyerek **izlemeyi nasıl etkinleştireceğinizi**, DXF’yi PDF’ye dönüştürmeyi ve render sorunlarını sorunsuz bir şekilde yönetmeyi öğrenmiş olacaksınız.

---

**Son Güncelleme:** 2026-02-10  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}