---
date: 2025-12-03
description: DWG'den PDF'ye dönüştürürken PDF sayfa boyutunu nasıl ayarlayacağınızı
  ve Aspose.CAD for Java kullanarak DWG dosyalarında izlemeyi nasıl etkinleştireceğinizi
  öğrenin – CAD çizimini hassas bir şekilde PDF olarak dışa aktarmak için tam bir
  rehber.
language: tr
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Java'da Aspose.CAD Kullanarak PDF Sayfa Boyutunu Ayarlayın ve DWG Dosyalarında
  İzlemeyi Etkinleştirin
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG Dosyalarında PDF Sayfa Boyutunu Ayarlama ve İzlemeyi Etkinleştirme Aspose.CAD ile Java'da

## Introduction

Eğer **PDF sayfa boyutunu ayarlamanız** gerektiğinde *DWG'yi PDF'ye dönüştürürken* ve aynı zamanda oluşabilecek render sorunlarını izlemek istiyorsanız, Aspose.CAD for Java bu iki işlemi de temiz ve programatik bir şekilde yapmanıza olanak tanır. Bu öğreticide, sayfa boyutlarını yapılandırma, izlemeyi etkinleştirme ve bir CAD çizimini PDF olarak dışa aktarma adımlarını adım adım göstereceğiz—hepsi Java üzerinden. Sonunda, CAD çizimleri için doğru sayfa boyutunu ayarlamanın neden önemli olduğunu ve dışa aktarma sürecinde ayrıntılı izleme bilgilerinin nasıl yakalanacağını anlayacaksınız.

## Quick Answers
- **“PDF sayfa boyutunu ayarlamak” neyi etkiler?** Oluşturulan PDF tuvalinin genişlik ve yüksekliğini tanımlar, böylece çiziminiz mükemmel şekilde sığar.  
- **Bu özelliği kullanmak için lisansa ihtiyacım var mı?** Test için bir deneme sürümü yeterlidir; üretim ortamı için ticari lisans gereklidir.  
- **Hangi Aspose.CAD sürümü gereklidir?** `CadRasterizationOptions`'ı destekleyen herhangi bir yeni sürüm yeterlidir.  
- **Bunu diğer CAD formatlarıyla da kullanabilir miyim?** Örnek DWG/DXF gösterse de aynı yaklaşım çoğu desteklenen formatta çalışır.  
- **Dönüşüm ne kadar sürer?** Ortalama olarak orta boy dosyalar bir saniyenin altında tamamlanır; daha büyük çizimler daha uzun sürebilir.

## What is “set PDF page size” in the context of CAD export?
PDF sayfa boyutunu ayarlamak, renderlayıcıya çıktı tuvalinin tam boyutlarını (piksel veya nokta cinsinden) bildirir. Bu, ölçek ve yerleşimin korunması gereken teknik çizimler için özellikle önemlidir. Sayfa boyutu açıkça ayarlanmazsa, PDF varsayılan bir boyuta geçebilir ve çizim kırpılabilir ya da bozulabilir.

## Why set PDF page size when exporting CAD drawings?
- **Ölçeği koru** – Mühendisler gerçek ölçekli baskılara güvenir.  
- **Kağıda sığdır** – Proje gereksinimlerine uygun A4, Letter veya özel bir boyut seçin.  
- **Okunabilirliği artır** – Daha büyük sayfalar, detayları yakınlaştırmadan gösterebilir.  
- **Tutarlı çıktı** – Otomatikleştirilmiş hatlar her çalıştırmada aynı boyutlarda PDF üretir.

## How to set PDF page size when converting DWG to PDF?
Aşağıda, dışa aktarmadan önce `CadRasterizationOptions`'ı özel genişlik ve yükseklik değerleriyle yapılandıracağız. Bu adım, ana anahtar kelime **set PDF page size** ifadesini doğrudan ele alır.

## Prerequisites

- **Java Development Kit (JDK)** – Makinenizde Java 8 veya daha yeni bir sürüm kurulu olmalı.  
- **Aspose.CAD for Java** – Resmi [Aspose CAD indirme sayfasından](https://releases.aspose.com/cad/java/) indirin.  
- **Document Directory** – İşlemek istediğiniz DWG/DXF dosyalarını içeren bir klasör.

## Import Namespaces

First, import the classes you’ll need. The code block is unchanged from the original tutorial.

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

## Step 1: Load the DWG/DXF File

Load your source drawing. Adjust the path to point at your own file.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Step 2: Configure PDF Export Options (including page size)

Here we set the page width and height—this is where we **set PDF page size**. The values are in pixels; you can convert from inches or millimeters as needed.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Tip:** If you prefer standard paper sizes, use the conversion `1 inch = 72 points`. For an A4 page (8.27 × 11.69 in), set `pageWidth = 595` and `pageHeight = 842`.

## Step 3: Implement Tracking

Tracking captures any rendering problems. We attach a custom handler that will be invoked after the export.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Step 4: Export to PDF

Now perform the conversion. The PDF will be created with the dimensions you specified, and any tracking information will be printed to the console.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Step 5: CadRenderHandler Class

The handler prints out any failures that occurred during rendering. This helps you debug issues when **exporting CAD drawing PDF**.

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

## Common Issues and Solutions

| Sorun | Neden | Çözüm |
|-------|-------|-------|
| **Boş PDF** | Sayfa boyutu 0 veya çok küçük ayarlanmış | `setPageWidth` ve `setPageHeight` değerlerinin pozitif olduğundan emin olun. |
| **Geometri eksik** | Handler tarafından yakalanan render hataları | `ErrorHandler` çıktısını inceleyin ve ilgili `RenderCode`'u düzeltin. |
| **Dosya bulunamadı** | Yanlış `dataDir` yolu | Mutlak bir yol kullanın veya klasörün var olduğundan emin olun. |
| **Lisans istisnası** | Büyük dosyalar için geçerli bir lisans olmadan deneme sürümü kullanılması | Görüntüyü yüklemeden önce Aspose.CAD lisansınızı uygulayın. |

## Frequently Asked Questions

**S: Aspose.CAD for Java kullanarak diğer CAD dosya formatları için izlemeyi etkinleştirebilir miyim?**  
C: Aspose.CAD temel olarak izleme için DWG/DXF formatlarını destekler. Diğer formatlar için resmi dokümantasyona bakın.

**S: Aspose.CAD for Java'da ek dışa aktarma seçeneklerini nasıl yönetebilirim?**  
C: Kütüphane DPI, arka plan rengi ve vektör rasterleştirme gibi birçok seçenek sunar. Ayrıntılar için [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) sayfasına bakın.

**S: Aspose.CAD for Java için bir deneme sürümü mevcut mu?**  
C: Evet, ücretsiz deneme sürümünü [Aspose.CAD Free Trial](https://releases.aspose.com/) adresinden indirebilirsiniz.

**S: Aspose.CAD for Java ile ilgili yardım almak veya sorunları tartışmak için nereye başvurabilirim?**  
C: Topluluk desteği ve resmi yanıtlar için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

**S: Aspose.CAD for Java için geçici bir lisans nasıl elde edebilirim?**  
C: [Temporary License](https://purchase.aspose.com/temporary-license/) sayfasındaki adımları izleyin.

---

**Last Updated:** 2025-12-03  
**Tested With:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}