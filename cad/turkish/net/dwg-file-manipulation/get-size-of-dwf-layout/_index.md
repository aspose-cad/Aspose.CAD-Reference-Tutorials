---
date: 2026-04-06
description: Aspose.CAD kullanarak C#'ta DWF'yi JPG'ye nasıl dönüştüreceğinizi öğrenin
  ve DWG dosyalarından DWF düzen boyutunu nasıl çıkaracağınızı keşfedin.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: C#'ta DWG Dosyalarıyla Çalışma - DWF Düzeninin Boyutunu Almak
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: C# ile DWF'yi JPG'ye Dönüştür – DWG'den DWF Yerleşim Boyutunu Al
url: /tr/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# ile DWF'yi JPG'ye Dönüştür – DWG'den DWF Düzen Boyutunu Al

## Giriş

Eğer **DWF'yi JPG'ye dönüştürürken** aynı zamanda tam düzen boyutlarını da öğrenmek istiyorsanız, doğru yerdesiniz. Bu öğreticide, Aspose.CAD for .NET kullanarak DWG türetilmiş bir DWF dosyasını açan, her düzenin boyutunu okuyan ve düzeni yüksek kaliteli bir JPG görüntüsü olarak kaydeden tam bir uçtan uca örnek üzerinden geçeceğiz. Sonunda sadece DWF düzen bilgilerini nasıl çıkaracağınızı öğrenmekle kalmayacak, aynı zamanda herhangi bir C# projesine ekleyebileceğiniz yeniden kullanılabilir bir kod parçacığına da sahip olacaksınız.

## Hızlı Cevaplar
- **“DWF'yi JPG'ye dönüştürmek” ne anlama geliyor?** Vektörel bir DWF düzenini bitmap JPEG görüntüsüne rasterleştirmek anlamına gelir.  
- **Önce düzen boyutunu okumak neden önemli?** Tam ölçüleri bilmek, doğru sayfa boyutlarını ayarlamanızı sağlar ve gerilmiş ya da kesilmiş çıktıyı önler.  
- **Bu işlemi hangi kütüphane gerçekleştiriyor?** Aspose.CAD for .NET, DWG, DWF ve raster görüntü dönüşümü için tam destek sunar.  
- **Lisans gerekli mi?** Değerlendirme için geçici bir lisans yeterlidir; üretim için tam lisans gereklidir.  
- **Hangi .NET sürümleri destekleniyor?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## “DWF'yi JPG'ye dönüştürmek” nedir ve neden önemlidir?

DWF (Design Web Format) dosyasını JPG'ye dönüştürmek, tarayıcılarda görüntülenebilen, raporlara gömülebilen veya CAD yazılımı olmayan paydaşlarla paylaşılabilen taşınabilir bir görüntü oluşturur. Dönüşüm ayrıca görüntüyü (yeniden boyutlandırma, sıkıştırma, filigran ekleme) standart görüntü işleme araçlarıyla manipüle etme esnekliği sağlar.

## Neden DWF düzen boyutunu çıkartmalıyız?

Bir DWF dosyası birden fazla düzen içerebilir; her birinin kendi koordinat sistemi ve birimi (inç, milimetre vb.) vardır. Düzen boyutunu çıkartmak şunları mümkün kılar:

1. Rasterleştirirken orijinal en-boy oranını korumak.  
2. Yüksek çözünürlüklü çıktı için doğru DPI'yi seçmek.  
3. Manuel ayarlama yapmadan birçok düzeni toplu olarak işlemek.

## Önkoşullar

Bu öğreticiyi sorunsuz bir şekilde takip edebilmek için aşağıdaki önkoşulları yerine getirdiğinizden emin olun:

- Aspose.CAD for .NET: Aspose.CAD for .NET'in kurulu olduğundan emin olun. İndirmek için [Aspose.CAD for .NET indirme sayfasını](https://releases.aspose.com/cad/net/) ziyaret edebilirsiniz.

Kütüphane hazır olduğunda, bağımlılıkları aramak yerine koda odaklanabilirsiniz.

## Ad Alanlarını İçe Aktar

Kodlamaya başlamadan önce gerekli ad alanlarını içe aktarın. Bu ad alanları, CAD dosyaları, rasterleştirme seçenekleri ve dosya I/O işlemleri için ihtiyacımız olan sınıfları sağlar.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Adım 1: Ortamınızı Kurun

Yeni bir C# konsol ya da sınıf‑kütüphane projesi oluşturun, **Aspose.CAD.dll**'ye referans ekleyin ve projenin uyumlu bir .NET sürümünü hedeflediğinden emin olun.

## Adım 2: Dosya Yollarını Tanımlayın (DWF nasıl çıkarılır)

Kaynak DWF dosyanızın nerede bulunduğunu ve oluşturulan JPG dosyalarının nereye yazılacağını belirtin.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Pro ipucu:** Farklı işletim sistemlerinde daha güvenli yol işleme için `Path.Combine(MyDir, "blocks_and_tables.dwf")` kullanın.

## Adım 3: DWF Görüntüsünü Yükleyin

DWF dosyasını bir `Aspose.CAD.Image` nesnesine yükleyin. Sayfa‑özel özelliklere erişebilmek için bunu `DwfImage` tipine dönüştürüyoruz.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Adım 4: Sayfalar Üzerinde Döngü

Bir DWF birden fazla sayfa (düzen) içerebilir. Her birini ayrı ayrı işleyebilmek için döngüye alın.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Adım 5: Düzen Bilgilerini Alın

Döngü içinde düzen adını alın. Bu ad, hem günlük kaydı hem de çıktı JPG dosyasının adlandırılması için kullanılacak.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Adım 6: JPG Seçeneklerini Ayarlayın

Bir `JpegOptions` örneği oluşturun ve rasterleştirme seçeneklerini yapılandırın. `Layouts` özelliği, Aspose.CAD'in hangi düzeni render edeceğini belirtir.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Adım 7: Sayfa Boyutunu Belirleyin (dwg'yi jpg'ye dönüştür)

Düzenin yerel birimlerdeki genişlik ve yüksekliğini hesaplayın. Bu bilgi, raster sayfa boyutunu doğru ayarlamak için kritiktir.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Adım 8: Sayfa Boyutlarını Ayarlayın

Yerel birimleri (inç ya da milimetre) piksele, Aspose.CAD tarafından sağlanan yardımcı metodları kullanarak dönüştürün. Birim tipi başka bir şeyse, ham değerleri kullanarak geri dönüyoruz.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Adım 9: JPG Dosyasını Kaydedin

Son olarak rasterleştirme seçeneklerini JPEG seçeneklerine bağlayın ve görüntüyü diske kaydedin.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Döngü tamamlandığında, her düzen için orijinal DWF boyutlarıyla tam olarak eşleşen bir JPG dosyanız olacak.

## Yaygın Sorunlar ve Çözümler

| Semptom | Muhtemel Neden | Çözüm |
|---------|----------------|-------|
| Boş JPG çıktısı | `options.Layouts` doğru ayarlanmamış | Düzen adının `page.Name` ile eşleştiğini doğrulayın. |
| Bozuk görüntü | Yanlış DPI dönüşümü | Dönüştürmeden önce `CommonHelper.DPI = 300` (veya hedef DPI'niz) kullanın. |
| Dosya bulunamadı | `MyDir` yolu hatalı | Mutlak yollar veya `Path.Combine` kullanın. |
| Lisans hatası | Lisans uygulanmadı | `Image.Load` çağrılmadan önce geçici veya kalıcı bir lisans yükleyin. |

## Sık Sorulan Sorular

### S1: Aspose.CAD en son DWG dosya formatlarıyla uyumlu mu?

A1: Aspose.CAD, en son sürümler dahil olmak üzere çeşitli DWG dosya formatlarını destekler. Belirli uyumluluk detayları için [belgelendirmeye](https://reference.aspose.com/cad/net/) bakın.

### S2: Aspose.CAD'i hem ticari hem de kişisel projelerde kullanabilir miyim?

A2: Evet, Aspose.CAD hem ticari hem de kişisel kullanım için esnek lisans seçenekleri sunar. Daha fazla bilgi için [satın alma sayfasını](https://purchase.aspose.com/buy) ziyaret edin.

### S3: Aspose.CAD için geçici bir lisans nasıl alabilirim?

A3: Değerlendirme amaçlı geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) edinebilirsiniz.

### S4: Aspose.CAD için destek nereden bulunur?

A4: Herhangi bir soru ya da yardım için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

### S5: Aspose.CAD için ücretsiz deneme sürümü var mı?

A5: Evet, ücretsiz deneme sürümüne [burada](https://releases.aspose.com/) ulaşabilirsiniz.

### S6: DWF çıkarmadan doğrudan DWG dosyasını JPG'ye nasıl dönüştürürüm?

A6: `Aspose.CAD.Image.Load` ile DWG dosyasını yükleyebilir ve aynı rasterleştirme iş akışını kullanabilirsiniz; sadece `options.Layouts` değerini DWG'den istediğiniz düzen adı(ları) olarak ayarlayın.

### S7: Dönüşüm vektör kalitesini korur mu?

A7: JPG'ye rasterleştirildiğinde görüntü bitmap tabanlı olur, bu yüzden vektörel ölçeklenebilirlik kaybolur. Kayıpsız ölçekleme için PNG veya SVG olarak dışa aktarmayı düşünün.

---

**Son Güncelleme:** 2026-04-06  
**Test Edilen:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}