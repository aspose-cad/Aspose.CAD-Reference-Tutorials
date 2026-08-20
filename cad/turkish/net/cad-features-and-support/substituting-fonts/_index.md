---
date: 2026-03-29
description: Aspose.CAD for .NET'te yazı tiplerini hızlı bir şekilde nasıl değiştireceğinizi
  öğrenin. Bu adım adım rehber, birincil yazı tipi adını nasıl ayarlayacağınızı ve
  CAD çizimlerini verimli bir şekilde nasıl özelleştireceğinizi gösterir.
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET'te Yazı Tiplerini Nasıl Değiştirilir
url: /tr/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET'te Yazı Tiplerini Nasıl Değiştirilir

## Giriş

.NET kullanarak CAD geliştirme alanında **yazı tiplerini nasıl değiştireceğinizi** öğrenmek, çizimlerinizin görsel kalitesini büyük ölçüde artırabilecek kritik bir beceridir. Aspose.CAD for .NET, herhangi bir stil için **set primary font name** sağlayan basit bir API sunar; bu sayede global ya da seçmeli yazı tipi ikamesi zahmetsizce yapılabilir. Bu öğreticide, bir çizimi yüklemekten yazı tiplerini global ya da belirli stil adıyla değiştirmeye kadar tüm süreci adım adım inceleyeceğiz.

## Hızlı Yanıtlar
- **CAD manipülasyonu için ana sınıf nedir?** `Aspose.CAD.Image` (veya türetilmiş `CadImage`).
- **Yazı tipini değiştiren özellik hangisidir?** `CadStyleTableObject` üzerindeki `PrimaryFontName`.
- **Tüm stiller için aynı anda yazı tiplerini değiştirebilir miyim?** Evet, `cadImage.Styles` üzerinden döngü yapıp özelliği ayarlayın.
- **Üretim için lisansa ihtiyacım var mı?** Deneme dışı kullanım için geçerli bir Aspose.CAD lisansı gereklidir.
- **Desteklenen .NET sürümleri?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## CAD'de Yazı Tipi Değiştirme Nedir?

Yazı tipi ikamesi, bir CAD çiziminde kullanılan orijinal tipografiyi, hedef sistemde mevcut olan başka bir tipografiyle değiştirmeyi ifade eder. Bu, orijinal yazı tipi eksik olduğunda, tutarlı bir kurumsal stil gerektiğinde veya yalnızca sınırlı yazı tipi setini destekleyen cihazlarda baskı hazırlarken özellikle faydalıdır.

## Neden Aspose.CAD ile Yazı Tiplerini Değiştirmelisiniz?

- **Harici bağımlılık yok** – kütüphane yazı tipi eşlemesini dahili olarak yönetir.
- **Birçok formatla çalışır** – DXF, DWG, DGN ve daha fazlası.
- **Programatik kontrol** – toplu dönüşümler veya CI pipeline'ları için süreci otomatikleştirin.
- **Çizim geometrisini korur** – yalnızca metnin görsel temsili değişir.

## Önkoşullar

- .NET programlaması hakkında temel bilgi.
- Aspose.CAD for .NET yüklü. Henüz yüklemediyseniz, [buradan](https://releases.aspose.com/cad/net/) indirin.
- Deneme yapmak için bir CAD çizim dosyası (DXF, DWG vb.).

## Ad Alanlarını İçe Aktarın

Uygulamanızda Aspose.CAD işlevlerine erişmek için gerekli ad alanlarını içe aktarmadan önce aşağıdaki adımları izleyin.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## Adım 1: CAD Çizimini Yükleyin

CAD çizimini bir `CadImage` örneğine yükleyerek başlayın. Belge dizininize doğru yolu sağladığınızdan emin olun.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## Adım 2: Stilleri Döngüyle Gezin

CAD çizimindeki stilleri bir `foreach` döngüsüyle yineleyin. Bu, bireysel yazı tipi stillerine erişip onları manipüle etmenizi sağlar.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## Yazı Tipi Değiştirme için Birincil Yazı Tipi Adını Nasıl Ayarlarsınız

Her `CadStyleTableObject` üzerindeki `PrimaryFontName` özelliği, çizim render edildiğinde hangi yazı tipinin kullanılacağını kontrol eder. Bu özelliği ayarlayarak orijinal yazı tipini etkili bir şekilde değiştirebilirsiniz.

### Adım 3: Yazı Tiplerini Genel Olarak Değiştir

**Tüm** stiller için yazı tiplerini değiştirmek amacıyla, her stilin `PrimaryFontName` özelliğini istediğiniz yazı tipi adıyla (örneğin, `"Arial"`) ayarlayın.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### Adım 4: Stil Adına Göre Yazı Tipini Değiştir

Yalnızca belirli bir stil için (örneğin `"Roman"` adlı stil) yazı tipini değiştirmek istiyorsanız, döngü içinde koşullu bir kontrol ekleyin.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## Yaygın Sorunlar ve Sorun Giderme

| Sorun | Neden | Çözüm |
|-------|-------|-----|
| Kod çalıştırıldıktan sonra yazı tipi değişmiyor | Çizim önbelleğe alınmış veya yalnızca‑okunur modda açılmış | Değişiklikten sonra resmi kaydettiğinizden (`cadImage.Save(...)`) emin olun veya dosyayı yeniden yükleyerek doğrulayın. |
| İstenen yazı tipi sistemde bulunamadı | Kodun çalıştığı makinede yazı tipi yüklü değil | Gerekli TrueType/OpenType yazı tipini yükleyin veya uygulama kaynaklarına gömün. |
| Metin bozuk görünüyor | Yanlış kodlama veya Unicode desteği eksik | Gerekli karakter setini destekleyen bir yazı tipi kullanın (ör. Arial Unicode MS). |

## Sık Sorulan Sorular

**Q: Aspose.CAD for .NET'te yazı tipi değişikliklerini geri alabilir miyim?**  
**A:** Evet, orijinal CAD çizimini yeniden yükleyerek veya değişiklik yapmadan önce bir yedek kopya tutarak geri alabilirsiniz.

**Q: Değiştirebileceğim başka yazı tipi özellikleri var mı?**  
**A:** Kesinlikle. `PrimaryFontName` dışında `SecondaryFontName`, `FontFamily` ve gelişmiş özelleştirme için diğer stil‑ilişkili özniteliklerle çalışabilirsiniz.

**Q: Aspose.CAD farklı CAD formatlarıyla uyumlu mu?**  
**A:** Evet, Aspose.CAD DXF, DWG, DGN, DWF ve daha fazlası gibi geniş bir format yelpazesini destekleyerek projelerinizde esneklik sağlar.

**Q: Toplu işleme sırasında yazı tipi değiştirmeyi otomatikleştirebilir miyim?**  
**A:** Elbette. Yükleme ve değiştirme mantığını bir klasördeki CAD dosyaları üzerinde döngüye alabilir veya bir CI/CD pipeline'ına entegre edebilirsiniz.

**Q: Aspose.CAD for .NET için ek destek nereden bulunur?**  
**A:** Ek destek ve topluluk tartışmaları için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

---

**Son Güncelleme:** 2026-03-29  
**Test Edilen Versiyon:** Aspose.CAD for .NET (en son sürüm)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}