---
date: 2026-02-23
description: Aspose.CAD for Java ile DWG'yi PDF'ye dönüştürürken PDF sayfa boyutunu
  nasıl ayarlayacağınızı öğrenin ve PDF çözünürlüğünü artırmak için PDF dışa aktarma
  seçeneklerini keşfedin.
linktitle: Export to PDF
second_title: Aspose.CAD Java API
title: PDF Sayfa Boyutunu Ayarla – Aspose.CAD ile dwg'den pdf'ye Java kullanarak
url: /tr/java/cad-export-options/export-to-pdf/
weight: 13
---

 rows.

Also keep bold formatting.

Let's craft translation.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# dwg to pdf java – Aspose.CAD for Java ile PDF'ye Dışa Aktarma

## Introduction

Eğer **PDF sayfa boyutunu ayarlamanız** gerekiyorsa ve **dwg to pdf java** dönüşümünü hızlı ve güvenilir bir şekilde gerçekleştirmek istiyorsanız doğru yerdesiniz. Bu öğreticide, DWG (veya desteklenen herhangi bir CAD formatı) dosyasını Aspose.CAD for Java kullanarak yüksek kalitede bir PDF'ye dönüştürmeyi adım adım gösteriyoruz. Ortamı kurmaktan PDF dışa aktarma seçeneklerini özelleştirmeye kadar her şeyi ele alacağız, böylece dönüşümü kendi Java uygulamalarınıza güvenle entegre edebilirsiniz.

## Quick Answers
- **What library handles dwg to pdf java?** Aspose.CAD for Java  
- **How long does a basic conversion take?** Genellikle tipik çizimler için bir saniyenin altında  
- **Do I need a license for development?** Test için ücretsiz deneme sürümü çalışır; üretim için lisans gerekir  
- **Can I customize page size and layout?** Evet – sayfa genişliği, yüksekliği ve düzeni ayarlamak için `CadRasterizationOptions` kullanın  
- **Is rasterization required?** Aspose.CAD, PDF'ye dışa aktarırken vektör verileri rasterleştirir ve kalite üzerinde kontrol sağlar  

## What is dwg to pdf java?

DWG dosyasını bir Java ortamında PDF'ye dönüştürmek, vektör tabanlı bir CAD çizimini herhangi bir cihazda görüntülenebilen taşınabilir bir belge formatına render etmektir. Aspose.CAD, CAD verilerini yorumlayarak, gerektiğinde rasterleştirerek ve orijinal tasarım sadakatini koruyan bir PDF üreterek bu süreci üstlenir.

## Why use Aspose.CAD for dwg to pdf java?

- **Broad format support** – DWG, DWF, DXF ve birçok diğer CAD türüyle çalışır.  
- **No external dependencies** – Saf Java kütüphanesi, yerel DLL veya COM bileşeni gerektirmez.  
- **Fine‑grained control** – Sayfa boyutlarını, rasterleştirme kalitesini ve düzen seçeneklerini ayarlayın.  
- **Scalable performance** – Toplu işleme veya web servislerinde anlık dönüşümler için uygundur.  

## How to set PDF page size

PDF sayfa boyutunu ayarlamak, `CadRasterizationOptions` üzerinden yapılandırdığınız **pdf export options** kısmının bir parçasıdır. `setPageWidth` ve `setPageHeight` tanımlayarak, ortaya çıkan PDF'nin tam boyutlarını kontrol edersiniz; bu, belirli bir kağıt boyutuna uymanız veya PDF'yi daha büyük bir iş akışına entegre etmeniz gerektiğinde kritiktir.

## Prerequisites

Öğreticiye başlamadan önce aşağıdaki ön koşulların sağlandığından emin olun:

- Aspose.CAD for Java: Java ortamınıza Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. İndirmek için [buraya](https://releases.aspose.com/cad/java/) tıklayın.  

- Resource Directory: CAD dosyalarınızın saklandığı bir dizin oluşturun. Sağlanan kod örneğindeki "Your Document Directory" ifadesini gerçek yol ile değiştirin.  

Şimdi ana adımlara geçelim.

## Import Namespaces

Java projenizde Aspose.CAD işlevlerini kullanabilmek için gerekli paketleri içe aktarın.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Step 1: Load CAD File

CAD dosyanızı Aspose.CAD `Image` nesnesine yükleyin. `"site.dwf"` ifadesini gerçek CAD dosya adınızla değiştirin.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## Step 2: Configure PDF Options

Sayfa yüksekliği, genişliği ve düzen gibi vektör rasterleştirme seçeneklerini içeren PDF dışa aktarma ayarlarını yapılandırın. Burada **pdf çıktısını özelleştirerek** gereksinimlerinize uygun hâle getirebilir ve gerektiğinde **PDF çözünürlüğünü artırabilirsiniz**.

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## Step 3: Export to PDF

Oluşturulan PDF dosyasının çıkış yolunu belirtin ve yapılandırılmış PDF seçenekleriyle resmi kaydedin. Bu adım **pdf cad** dosyalarını dağıtıma hazır hâle getirir.

```java
String outPath = dataDir + "site.pdf";
image.save(outPath, pdfOptions);
```

Congratulations! You have successfully exported your CAD file to a PDF using Aspose.CAD for Java.

## Common Issues and Solutions

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Blank pages in PDF** | Rasterization options not set or default size too small | `setPageWidth` / `setPageHeight` değerlerini kaynak çizim boyutlarıyla eşleyecek şekilde ayarlayın |
| **Low‑quality output** | Default rasterization DPI is low | DPI'yi artırmak için `rasterizationOptions.setResolution(300);` kullanın ve **increase PDF resolution** |
| **Unsupported CAD format** | The file type is not among Aspose.CAD’s supported list | Dosyayı desteklenen bir formata (ör. DWG, DWF, DXF) dönüştürerek yükleyin |

## Frequently Asked Questions

### Q1: Is Aspose.CAD compatible with all CAD file formats?

A1: Evet, Aspose.CAD geniş bir CAD formatı yelpazesini destekler ve çeşitli tasarım yazılımlarıyla uyumludur.

### Q2: Can I customize the PDF output settings?

A2: Kesinlikle. Öğreticide özelleştirme seçeneklerine bir bakış sunduk, ancak **rasterize cad pdf** ve çıktıyı ihtiyaçlarınıza göre şekillendirmek için daha fazlasını keşfedebilirsiniz.

### Q3: Where can I find additional support for Aspose.CAD?

A3: Herhangi bir soru veya sorun için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret ederek topluluktan yardım alabilirsiniz.

### Q4: Is there a free trial available?

A4: Evet, Aspose.CAD ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

### Q5: How can I obtain a temporary license for Aspose.CAD?

A5: Geçici lisans için [bu bağlantıyı](https://purchase.aspose.com/temporary-license/) ziyaret edin.

## Additional FAQs

**Q: How do I change the rasterization mode for smoother lines?**  
A: `rasterizationOptions.setSmoothingMode(SmoothingMode.AntiAlias);` kodunu kaydetmeden önce ayarlayın.

**Q: Can I export multiple CAD files in a batch?**  
A: Evet—yükleme ve kaydetme mantığını bir döngü içinde sararak aynı `PdfOptions` örneğini yeniden kullanabilirsiniz. Bu, **batch convert cad pdf** senaryolarını mümkün kılar.

**Q: Does the library support password‑protected PDFs?**  
A: PDF şifreleme Aspose.CAD içinde yer almaz; PDF'ye güvenlik eklemek için Aspose.PDF ile sonradan işleyebilirsiniz.

## FAQ – Quick Reference

**Q: How do I set PDF page size for a DWG conversion?**  
A: `rasterizationOptions.setPageWidth(width)` ve `rasterizationOptions.setPageHeight(height)` metodlarını `image.save()` çağrısından önce kullanın.

**Q: What setting should I use to **increase PDF resolution**?**  
A: Çıktı DPI'sını yükseltmek için `rasterizationOptions.setResolution(300);` (veya daha yüksek) çağrısını yapın.

**Q: Can I use this code in a micro‑service?**  
A: Evet, kütüphane saf Java olduğundan konteynerleştirilmiş veya sunucusuz ortamlarda sorunsuz çalışır.

**Q: Is there any limit to the number of files I can convert in one batch?**  
A: Limit, sisteminizin bellek ve CPU kapasitesiyle belirlenir; aynı `PdfOptions` örneğini yeniden kullanmak kaynak tüketimini düşük tutar.

**Q: How do I switch from DWG to another CAD format like DXF?**  
A: `fileName` uzantısını değiştirmeniz yeterlidir; Aspose.CAD formatı otomatik algılar.

## Conclusion

Bu öğreticide, **dwg to pdf java** kullanarak CAD çizimlerini PDF'ye dönüştürme sürecini, **set PDF page size** ve ilgili **pdf export options** üzerine odaklanarak adım adım inceledik. Bu talimatları izleyerek PDF dışa aktarmayı masaüstü, web veya mikro‑servis mimarilerine kolayca entegre edebilir, rasterleştirme, düzen ve çözünürlük üzerinde tam kontrol sağlayabilirsiniz.

---

**Last Updated:** 2026-02-23  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}