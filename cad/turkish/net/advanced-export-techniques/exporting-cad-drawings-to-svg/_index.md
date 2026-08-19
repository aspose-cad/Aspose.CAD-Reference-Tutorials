---
date: 2026-03-07
description: Aspose.CAD for .NET kullanarak CAD'i SVG'ye nasıl dışa aktaracağınızı,
  SVG rengini nasıl özelleştireceğinizi ve DWG'yi verimli bir şekilde SVG'ye nasıl
  dönüştüreceğinizi öğrenin.
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD'yi SVG'ye Aktar – CAD Çizimlerini SVG Formatına Aktarma - Aspose.CAD Kılavuzu
url: /tr/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD'i SVG'ye Dışa Aktarma – CAD Çizimlerini SVG Formatına Dışa Aktarma

## Giriş

CAD çizimlerini SVG'ye dışa aktarmak, web sayfaları, raporlar veya etkileşimli görselleştirmeler için çözünürlük‑bağımsız grafiklere ihtiyaç duyduğunuzda yaygın bir gereksinimdir. Bu öğreticide **CAD'i SVG'ye nasıl dışa aktaracağınızı** Aspose.CAD for .NET ile öğrenecek, **SVG rengini özelleştirme** seçeneklerini keşfedecek ve sadece birkaç satır kodla **DWG'yi SVG'ye (veya DXF'yi SVG'ye) dönüştürmeyi** göreceksiniz. Adımlar hızlıdır, API sezgiseldir ve ortaya çıkan SVG dosyaları herhangi bir cihazda mükemmel ölçeklenir.

## Hızlı Yanıtlar
- **Dönüşümü hangi kütüphane yönetir?** Aspose.CAD for .NET.
- **Renk modunu değiştirebilir miyim?** Evet – `SvgColorMode` kullanarak gri‑ton, siyah‑beyaz veya tam renk ayarlayabilirsiniz.
- **Hangi CAD formatları destekleniyor?** DWG, DXF ve birçok diğer format (Aspose.CAD belgelerine bakınız).
- **Geliştirme için lisansa ihtiyacım var mı?** Test için geçici bir lisans mevcuttur.
- **Dönüşüm ne kadar sürer?** Standart çizimler için genellikle bir saniyenin altında.

## “CAD'i SVG'ye dışa aktarma” nedir?
CAD'i SVG'ye dışa aktarmak, yerel bir CAD dosyasını (ör. DWG veya DXF) Ölçeklenebilir Vektör Grafikleri formatına dönüştürmek anlamına gelir. SVG, XML‑tabanlı, hafif ve CSS ile stillendirilebilir—bu da modern web ve mobil uygulamalar için idealdir.

## Neden CAD'i SVG'ye dışa aktarmak için Aspose.CAD kullanmalı?
- **Harici bağımlılık yok** – saf .NET API, AutoCAD kurulumuna gerek yok.  
- **İnce ayarlı kontrol** – **SVG rengini özelleştirebilir**, metnin şekil olarak tutulup tutulmayacağını belirleyebilir ve rasterleştirme seçeneklerini seçebilirsiniz.  
- **Geniş format desteği** – aynı kod **DWG'yi SVG'ye dönüştürme**, **DXF'yi SVG'ye dönüştürme** ve diğer formatlar için çalışır, kod tabanınızı basitleştirir.  
- **Yüksek performans** – hız ve düşük bellek kullanımı için optimize edilmiştir, toplu işleme için uygundur.

## Önkoşullar

Başlamadan önce şu şeylerin kurulu olduğundan emin olun:

- **Aspose.CAD for .NET** yüklü. Kütüphaneyi [buradan](https://releases.aspose.com/cad/net/) indirebilirsiniz.  
- Bir .NET geliştirme ortamı (Visual Studio, Rider veya .NET CLI).  
- Dönüştürmek istediğiniz bir CAD dosyası (DWG veya DXF).

## Ad Alanlarını İçe Aktarma

İlk olarak, sınıfların kullanılabilir olması için gerekli ad alanlarını projenize ekleyin.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Adım‑Adım Kılavuz

### Adım 1: Belge Dizini Ayarla  
Kaynak CAD dosyanızın bulunduğu ve SVG çıktısının kaydedileceği klasörü tanımlayın.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### Adım 2: CAD Çizimini Yükle  
`Image.Load` kullanarak DWG (veya DXF) dosyasını okuyun. Bu, **load DWG .NET** senaryoları için çalışır.

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### Adım 3: SVG Dışa Aktarma Seçeneklerini Yapılandır  
İhtiyacınıza göre dışa aktarma ayarlarını düzenleyin. Burada renk modunu gri‑ton olarak ayarlıyor ve tüm metnin vektör şekil olarak render edilmesini zorunlu kılıyoruz.

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### Adım 4: SVG Dosyasını Kaydet  
Son olarak, SVG dosyasını diske yazın. Bu adım **CAD'i SVG olarak kaydeder** ve dönüşümü tamamlar.

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

Bu dört kısa adımı izleyerek **DWG'yi SVG'ye** (veya **DXF'yi SVG'ye**) tam kontrolle dışa aktarabilirsiniz.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|-------|
| **Boş SVG çıktısı** | Kaynak dosya yolu hatalı veya dosya bozuk. | `MyDir`'i doğrulayın ve CAD dosyasının hatasız açıldığından emin olun. |
| **Renkler yanlış görünüyor** | `SvgColorMode` yanlışlıkla Gri tonlamaya ayarlanmış. | `options.ColorType`'ı `SvgColorMode.FullColor` olarak değiştirerek orijinal renkleri koruyun. |
| **Metin eksik** | `TextAsShapes` `false` olarak ayarlanmış ve görüntüleyici gömülü fontları desteklemiyor. | `TextAsShapes = true` tutun veya SVG'ye gerekli fontları gömün. |

## Sık Sorulan Sorular

### Q1: Aspose.CAD tüm CAD formatlarıyla uyumlu mu?

A1: Aspose.CAD, DWG ve DXF dahil olmak üzere çeşitli CAD formatlarını destekler ve geniş bir uyumluluk sağlar.

### Q2: SVG'ye dışa aktarırken renk modunu özelleştirebilir miyim?

A2: Evet, Aspose.CAD renk modunu seçmenize izin verir, böylece çıktıda esneklik elde edersiniz.

### Q3: Test amaçlı geçici lisanslar mevcut mu?

A3: Evet, değerlendirme için geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

### Q4: Aspose.CAD için detaylı belgeleri nerede bulabilirim?

A4: Belgeler [burada](https://reference.aspose.com/cad/net/) mevcuttur.

### Q5: Aspose.CAD ile ilgili destek alabilir veya soru sorabilir miyim?

A5: Destek ve tartışmalar için topluluk forumunu [burada](https://forum.aspose.com/c/cad/19) ziyaret edebilirsiniz.

## Yaygın Sorulan Sorular

**Q:** Bu kodu .NET Core veya .NET 6 ile kullanabilir miyim?  
**A:** Kesinlikle. Aspose.CAD for .NET, .NET Framework, .NET Core ve .NET 5/6+ ile uyumludur.

**Q:** Sadece belirli bir düzeni veya katmanı dışa aktarmak mümkün mü?  
**A:** Evet. `SvgOptions` içinde `PageIndex` ayarlayabilir veya kaydetmeden önce katmanları filtreleyebilirsiniz.

**Q:** Oluşturulan SVG'ye özel CSS stilleri nasıl eklenir?  
**A:** Kaydetme sonrası SVG XML'ini işleyerek `<style>` öğeleri ekleyebilir veya yeni sürümlerde mevcutsa `options.CustomCss` kullanabilirsiniz.

**Q:** Kaynak CAD dosyası için hangi boyut sınırlamaları vardır?  
**A:** Kütüphane büyük dosyaları işleyebilir, ancak bellek tüketimi karmaşıklıkla artar. Çok büyük çizimler için sayfaları ayrı ayrı işlemek daha iyidir.

**Q:** Dönüşüm çizgi kalınlıklarını ve çizgi tiplerini korur mu?  
**A:** Varsayılan olarak çizgi kalınlıkları korunur. Daha ince kontrol için `SvgOptions` içinde render ayarlarını değiştirebilirsiniz.

---

**Son Güncelleme:** 2026-03-07  
**Test Edilen Sürüm:** Aspose.CAD for .NET 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}