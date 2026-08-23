---
date: 2026-08-23
description: Aspose.CAD kullanarak viewport dwg c# nasıl oluşturulacağını öğrenin.
  Bu kılavuz, bir DWG dosyasını yüklemeyi, rasterleştirmeyi yapılandırmayı, bir viewport
  tanımlamayı ve sonucu PDF olarak kaydetmeyi kapsar.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: C#'da DWG Belgelerini İşleme
og_description: Aspose.CAD kullanarak .NET'te viewport dwg c# nasıl oluşturulacağını
  öğrenin. Bu adım adım kılavuz, yüklemeyi, rasterleştirmeyi, viewport'ları tanımlamayı
  ve PDF olarak kaydetmeyi gösterir.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Aspose.CAD for .NET ile viewport dwg c# nasıl oluşturulur
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Aspose.CAD for .NET ile viewport dwg c# nasıl oluşturulur
url: /tr/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#'ta DWG belgelerini işleme – viewport dwg c# oluşturma öğreticisi

## Giriş

Bu kapsamlı öğreticide **create viewport dwg c#** işlemini Aspose.CAD ile nasıl yapacağınızı ve bir DWG dosyasını PDF olarak nasıl render edeceğinizi öğreneceksiniz. Belirli bir layout'u çıkarmak, yazdırılabilir bir sayfa oluşturmak ya da bir raporda CAD görünümünü gömmek ister misiniz, viewport kontrolü size kesin render kontrolü sağlar. Aspose.CAD **20+ CAD formatını** destekler ve tüm belgeyi belleğe yüklemeden binlerce varlığı işleyebilir, bu da yüksek performanslı .NET uygulamaları için idealdir.

## Hızlı cevaplar
- **İlk adım nedir?** `CadImage.Load` ile DWG dosyasını yükleyin.
- **Hangi sınıf görünüm alanını tanımlar?** `CadRasterizationOptions` içinde `Viewport`.
- **PDF olarak çıktı alabilir miyim?** Evet, rasterleştirmeden sonra `PdfOptions` kullanarak.
- **Üretim için lisansa ihtiyacım var mı?** Ticari bir lisans gereklidir; değerlendirme için ücretsiz deneme sürümü çalışır.
- **.NET Core destekleniyor mu?** Kesinlikle – Aspose.CAD .NET Framework, .NET Core ve .NET 5/6 ile çalışır.

## Önkoşullar

Kodlamaya başlamadan önce şunlara sahip olduğunuzdan emin olun:

- C# programlama temelleri.
- Visual Studio (herhangi bir yeni sürüm) yüklü.
- Projenize eklenmiş Aspose.CAD kütüphanesi. İndirmek için [Aspose.CAD download page](https://releases.aspose.com/cad/net/) adresini ziyaret edin.
- Takip edebilmek için **Bottom_plate.dwg** gibi bir örnek DWG dosyası.

## Ad alanlarını içe aktar

C# dosyanızın üst kısmına gerekli `using` yönergelerini ekleyin, böylece derleyici Aspose.CAD tiplerini bulabilir.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Ortam hazır olduğuna göre, uygulamayı adım adım inceleyelim.

## viewport dwg c# nasıl oluşturulur?

Özel bir viewport oluşturmak için önce DWG dosyasını bir `CadImage` nesnesine yükleyin, ardından istediğiniz layout ve ölçeklendirmeyi içeren `CadRasterizationOptions`'ı yapılandırın. Görüntülemek istediğiniz bölgeyi tanımlayın, hesaplanan merkez, yükseklik ve en‑boy oranı ile bir `CadVportTableObject` örneği oluşturun, aktif viewport'u değiştirin, PDF seçeneklerini ayarlayın ve son olarak sonucu kaydedin.

## Adım 1: dwg dosyasını yükle

`CadImage.Load` bir DWG dosyasını bir `CadImage` nesnesine yükler; bu nesne CAD çizimini bellekte temsil eder.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Adım 2: rasterleştirme seçeneklerini yapılandır

`CadRasterizationOptions`, CAD çiziminin rasterleştirilme şeklini belirler; layout seçimi, ölçeklendirme ve çıktı boyutu gibi ayarları içerir.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Adım 3: çizim bölgesini tanımla

`Point`, render edilecek bölgenin sol‑üst köşesinin X ve Y koordinatlarını tanımlar.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Adım 4: yeni bir viewport oluştur

`CadVportTableObject`, render edilen çizimin görünür alanını ve en‑boy oranını kontrol eden bir viewport nesnesini temsil eder.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Adım 5: aktif viewport'u değiştir

Bu döngü, özel görünüm ayarlarını uygulamak için aktif viewport'u yeni oluşturulan viewport ile değiştirir.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Adım 6: PDF seçeneklerini yapılandır

`PdfOptions`, sıkıştırma ve meta veri gibi PDF çıktı parametrelerini yapılandırır.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Adım 7: render edilen dwg'yi PDF olarak kaydet

`image.Save`, belirtilen format seçenekleriyle render edilen görüntüyü bir dosyaya yazar.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## DWG render ederken özel bir viewport neden kullanılır?

Özel bir viewport, belirli bir layout veya bölgeyi izole etmenizi sağlar; bu da dosya boyutunu azaltır ve render hızını artırır. Odaklanmış bir viewport kullanıldığında Aspose.CAD, 300 sayfalık bir DWG'yi 2 saniyenin altında render edebilir; tam çizim renderı ise birkaç saniye daha uzun sürebilir.

## Yaygın sorunlar ve çözümler

- **Boş çıktı** – Viewport koordinatlarının çizim sınırları içinde olduğundan emin olun; sınırları doğrulamak için `CadImage.Size` kullanın.
- **Eksik katmanlar** – `CadRasterizationOptions.Layouts` özelliğini doğru layout adına ayarlayın; aksi takdirde varsayılan layout boş olabilir.
- **Performans yavaşlaması** – Sadece hızlı bir önizleme ihtiyacınız varsa `CadRasterizationOptions` içinde anti‑aliasing'i devre dışı bırakın.

## Sıkça sorulan sorular

### Q1: Aspose.CAD'i diğer CAD dosya formatlarıyla kullanabilir miyim?
A1: Evet, Aspose.CAD çeşitli formatları destekler, DWG, DXF, DWF ve 20'den fazla ek CAD türü dahil.

### Q2: Aspose.CAD .NET Core ile uyumlu mu?
A2: Evet, Aspose.CAD .NET Framework, .NET Core ve en yeni .NET sürümleriyle çalışır.

### Q3: Bir DWG dosyasındaki farklı layout'ları nasıl yönetebilirim?
A3: Render etmeden önce `CadRasterizationOptions`'ın `Layouts` özelliğini kullanarak istediğiniz layout'u belirtin.

### Q4: Aspose.CAD kullanımıyla ilgili lisans konuları var mı?
A4: Lisans detayları için [Aspose.CAD licensing page](https://purchase.aspose.com/buy) adresini ziyaret edin.

### Q5: Ek destek nereden bulunabilir?
A5: Topluluk yardımı ve tartışmalar için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresine bakın.

### Q6: PDF yerine doğrudan PNG olarak render edebilir miyim?
A6: Evet, `PdfOptions` yerine `PngOptions` kullanın ve `image.Save("output.png", pngOptions)` şeklinde çağırın.

### Q7: Render edilen görüntüyü bir Windows Forms uygulamasına nasıl gömebilirim?
A7: Kaydedilen görüntüyü `Image.FromFile("output.png")` kullanarak bir `PictureBox` kontrolüne yükleyin.

## Sonuç

Artık **create viewport dwg c#** işlemini ve Aspose.CAD kullanarak bir DWG dosyasını PDF (veya diğer raster formatları) olarak nasıl render edeceğinizi biliyorsunuz. Viewport manipülasyonunu ustalaştırarak görsel çıktının ince ayarını yapabilir, doğru mühendislik çizimleri, raporlar veya küçük resimler oluşturabilirsiniz. Ek rasterleştirme ayarlarını keşfedin, farklı çıktı formatlarıyla deney yapın ve kodu daha büyük .NET servislerine ya da masaüstü yardımcı programlarına entegre edin.

---

**Son Güncelleme:** 2026-08-23  
**Test edildi:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose

## İlgili Öğreticiler

- [C# ile Koordinatlarla DWG'yi PDF'ye Dönüştürürken Viewport Ayarlama - Aspose.CAD Öğreticisi](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [CAD Rasterleştirme Seçeneklerini Ayarlamayı Öğrenin – Aspose.CAD ile Belirli Layout'ları PDF'ye Aktarma](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Aspose.CAD for .NET ile DWG'yi PDF ve Raster Görsellere Dönüştürme](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}