---
date: 2025-12-01
description: Aspose.CAD for Java kullanarak PDF sayfa boyutunu ayarlamayı, DWG'yi
  PDF'ye dönüştürmeyi ve DWG değişikliklerini izlemeyi öğrenin.
language: tr
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: PDF Sayfa Boyutunu Ayarlayın ve Aspose.CAD Java ile DWG'yi Takip Edin
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF Sayfa Boyutunu Ayarlama ve Aspose.CAD Java ile DWG İzleme

## Giriş

CAD projelerinde iş birliği yaparken, tutarlı bir düzen için genellikle **PDF sayfa boyutunu ayarlamanız**, **DWG'yi PDF'ye dönüştürmeniz** ve çizimde yapılan her değişikliği takip etmeniz gerekir. Aspose.CAD for Java, tüm bunları tek bir, sorunsuz iş akışında mümkün kılar. Bu öğreticide, **PDF sayfa boyutunu ayarlama**, **DWG değişikliklerini izleme** ve çizimi PDF olarak dışa aktarma adımlarını Java kullanarak göstereceğiz.

## Hızlı Yanıtlar
- **PDF sayfa boyutunu nasıl ayarlarım?** Dışa aktarmadan önce `CadRasterizationOptions.setPageWidth()` ve `setPageHeight()` kullanın.  
- **Dışa aktarırken değişiklikleri izleyebilir miyim?** Evet – izleme sonuçlarını yakalamak için özel bir `CadRenderHandler` uygulayın.  
- **DWG'yi PDF'ye dönüştüren yöntem hangisidir?** Seçenekleri yapılandırdıktan sonra `image.save(stream, pdfOptions)` çağırın.  
- **Ana önkoşullar nelerdir?** JDK, Aspose.CAD for Java ve DWG/DXF dosyalarını içeren bir klasör.  
- **Üretim için lisans gerekli mi?** Evet, deneme dışı dağıtımlar için geçerli bir Aspose.CAD lisansı gerekir.

## DWG dışa aktarım bağlamında “PDF sayfa boyutunu ayarlama” nedir?

PDF sayfa boyutunu ayarlamak, ortaya çıkan PDF tuvalinin (genişlik × yükseklik piksel olarak) boyutlarını belirler. Bu, dışa aktarılan çizimin belirli bir kağıt boyutuna veya ekran düzenine uymasını istediğinizde, tüm öğelerin tam olarak beklediğiniz yerde görünmesini sağlamak için gereklidir.

## DWG dosyalarını dışa aktarırken izlemeyi neden etkinleştirmelisiniz?

İzleme (veya değişiklik izleme), dönüşüm sırasında ortaya çıkan render hatalarını, eksik yazı tiplerini veya desteklenmeyen varlıkları kaydeder. Bu bilgiyi yakalayarak şunları yapabilirsiniz:
- Son teslimattan önce düzeltilmesi gereken sorunları hızlıca tespit edin.
- Neğin değiştirildiği veya atlandığı konusunda ekip üyelerine net geri bildirim sağlayın.
- Uyum gerektiren sektörler için denetim izini koruyun.

## Önkoşullar

- **Java Development Kit (JDK)** – herhangi bir yeni sürüm (8+).  
- **Aspose.CAD for Java** – resmi [Aspose CAD indirme sayfasından](https://releases.aspose.com/cad/java/) indirin.  
- **Document Directory** – işlemek istediğiniz DWG/DXF dosyalarını içeren bir klasör.

## Ad Alanlarını İçe Aktarma

Gerekli Aspose.CAD sınıflarını ve standart Java I/O sınıflarını içe aktararak başlayın.

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

## Adım 1: DWG (veya DXF) Dosyasını Yükleyin

Kaynak çiziminizi bir `Image` nesnesine yükleyin. Yolu kendi dizininize göre ayarlayın.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Adım 2: PDF Dışa Aktarma Seçeneklerini (sayfa boyutu dahil) Yapılandırın

Burada PDF seçeneklerini ayarlıyoruz ve açıkça **PDF sayfa boyutunu** 800 × 600 piksel olarak belirliyoruz. Bu, ana anahtar kelimenin uygulandığı yerdir.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Adım 3: İzlemeyi Uygulayın

Dönüşüm sürecinde izleme bilgilerini alacak özel bir hata işleyicisi oluşturun.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Adım 4: PDF Olarak Dışa Aktarın

Seçenekler ve izleme işleyicisi hazır olduğunda, çizimi dışa aktarın. Bu adım **DWG'yi PDF'ye dönüştürür** (örneğimizde DXF'yi PDF'ye dönüştürür).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Adım 5: CadRenderHandler Sınıfı – İzleme Sonuçlarını Yakalama

`ErrorHandler` sınıfı `CadRenderHandler` sınıfını genişletir ve **DWG dosyalarında değişiklik izlerken** ortaya çıkan render problemlerini yazdırır.

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

## Yaygın Sorunlar ve Çözüm Yolları

| Issue | Why it Happens | Fix |
|-------|----------------|-----|
| **Missing fonts** | CAD dosyası, sunucuda yüklü olmayan yazı tiplerine referans verir. | Gerekli yazı tiplerini yükleyin veya kaynak çizime gömün. |
| **Unsupported entities** | Bazı DWG varlıkları henüz Aspose.CAD tarafından desteklenmemektedir. | İzleme çıktısını kullanarak bunları belirleyin ve çizimi sadeleştirin. |
| **Incorrect page size** | `setPageWidth/Height` dışa aktarmadan önce çağrılmamış. | Yukarıda gösterildiği gibi `CadRasterizationOptions` içinde sayfa boyutunun ayarlandığından emin olun. |

## Sık Sorulan Sorular

### Q1: Aspose.CAD for Java kullanarak diğer CAD dosya formatları için izlemeyi etkinleştirebilir miyim?

A1: Aspose.CAD öncelikle DWG/DXF dosyaları için izlemeyi destekler. Diğer formatlar için mevcut özellikleri görmek üzere resmi belgeleri inceleyin.

### Q2: Aspose.CAD for Java'da ek dışa aktarma seçeneklerini nasıl yönetebilirim?

A2: Kütüphane DPI, arka plan rengi ve vektör rasterleştirme gibi birçok seçenek sunar. Bunları [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) adresinde keşfedin.

### Q3: Aspose.CAD for Java için bir deneme sürümü mevcut mu?

A3: Evet, ücretsiz bir deneme sürümünü [Aspose.CAD Free Trial](https://releases.aspose.com/) adresinden indirebilirsiniz.

### Q4: Aspose.CAD for Java ile ilgili yardım almak veya sorunları tartışmak için nereye başvurabilirim?

A4: [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresindeki topluluk forumu, sorular sormak ve deneyim paylaşmak için harika bir yerdir.

### Q5: Aspose.CAD for Java için geçici bir lisans nasıl alabilirim?

A5: Değerlendirme için zaman sınırlı bir lisans talep etmek üzere [Temporary License](https://purchase.aspose.com/temporary-license/) sayfasında belirtilen adımları izleyin.

### Q6: Katmanları koruyarak **DWG'yi PDF'ye dönüştürebilir** miyim?

A6: Evet. `CadRasterizationOptions` yapılandırılarak ortaya çıkan PDF'de katman bilgisi korunabilir.

### Q7: Özel sayfa boyutlarıyla **DWG'yi PDF olarak dışa aktarmanın** en iyi yolu nedir?

A7: `image.save()` çağırmadan önce `setPageWidth` ve `setPageHeight` kullanarak istenen genişlik ve yüksekliği ayarlayın – tam olarak Adım 2'de gösterildiği gibi.

## Sonuç

Yukarıdaki adımları izleyerek Aspose.CAD for Java kullanarak **PDF sayfa boyutunu ayarlayabilir**, **DWG'yi PDF'ye dönüştürebilir** ve **DWG dosyalarındaki değişiklikleri izleyebilirsiniz**. Bu iş akışı, çıktı düzeni üzerinde tam kontrol sağlar ve CAD iş birliğinizi sorunsuz ve hatasız tutacak değerli tanılamalar sunar. Ek render seçeneklerini keşfetmekten ve bu kodu daha büyük otomasyon hatlarına entegre etmekten çekinmeyin.

---

**Son Güncelleme:** 2025-12-01  
**Test Edilen:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}