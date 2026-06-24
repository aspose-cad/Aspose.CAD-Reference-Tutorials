---
date: 2026-04-09
description: Bu adım adım rehberde Aspose.CAD for .NET kullanarak DWG'yi görüntüye
  dönüştürmeyi ve alt katman bayraklarını okumayı öğrenin.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: DWG Dosyalarının Alt Katman Bayraklarını Keşfetmek
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG'yi Görsele Dönüştür – DWG Dosyalarının Alt Katman Bayraklarını Keşfetmek
  - Aspose.CAD Öğreticisi
url: /tr/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG Dosyalarının Alt Katman Bayraklarını Keşfetmek - Aspose.CAD Öğreticisi

## Giriş

CAD dosyalarının, özellikle DWG dosyalarının karmaşık dünyasına dalıyorsanız ve **convert DWG to image** yaparken aynı zamanda **how to read underlay** bayraklarını keşfetmek istiyorsanız, doğru yerdesiniz. Bu öğretici, güçlü Aspose.CAD for .NET kütüphanesini kullanarak her adımı size gösterir, böylece alt katman bilgilerini çıkarabilir ve çizimi güvenle bir görüntü olarak işleyebilirsiniz.

## Hızlı Yanıtlar
- **convert DWG to image** ne anlama geliyor?  
  Bu, Aspose.CAD kullanarak bir DWG çizimini raster formatına (PNG, JPEG vb.) işlemek anlamına gelir.
- **underlay flags**'ı gösteren yöntem hangisidir?  
  DWG'yi yükledikten sonra `CadUnderlay` nesnesinin `Flags` özelliğine erişin.
- **Aspose.CAD için lisansa ihtiyacım var mı?**  
  Değerlendirme için geçici bir lisans mevcuttur; üretim için tam lisans gereklidir.
- **Hangi .NET sürümleri destekleniyor?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 ve sonrası.
- **underlay geometrisini çıkarabilir miyim?**  
  Evet – alt katman yolu, ekleme noktası, ölçek, dönüş ve bayrak durumları tümü erişilebilir.

## “convert DWG to image” nedir ve neden önemlidir?

DWG dosyasını bir görüntüye dönüştürmek, CAD çizimlerini tarayıcılarda görüntülemenizi, raporlara yerleştirmenizi veya CAD görüntüleyicisi olmayan paydaşlarla paylaşmanızı sağlar. İşleme sırasında, **underlay** nesnelerini (ör. DGN referansları) doğru göründüklerinden emin olmak için sıkça incelemeniz gerekir. Alt katman bayraklarını anlamak, kırpma, tek renk işleme ve görünürlük sorunlarını nihai görüntüyü oluşturmadan önce çözmenize yardımcı olur.

## Önkoşullar

- C# ve .NET programlamasına temel bir anlayış.  
- **Aspose.CAD for .NET** kütüphanesi yüklü. Henüz yoksa, **[here](https://releases.aspose.com/cad/net/)** adresinden indirin.  
- Test için bir DWG dosyası – örnek dosya **“BlockRefDgn.dwg”** bu kılavuz boyunca kullanılmıştır.

## Ad Alanlarını İçe Aktarma

Başlamak için gerekli ad alanlarını içe aktarın:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Adım 1: DWG Dosyasını Yükleyin ve `CadImage`'a Dönüştürün

İlk olarak, DWG dosyasını yükleyin ve `CadImage` tipine dönüştürün. Bu nesne, alt katmanlar da dahil olmak üzere tüm çizim varlıklarına erişim sağlar.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Adım 2: Varlıkları Döngüyle Gezin

Sonra, çizimdeki her varlığı döngüyle geçin. Burada alt katman nesnelerini bulacaksınız.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Adım 3: `CadDgnUnderlay` Türünü Kontrol Edin

Alt katman varlıklarını, çalışma zamanındaki tiplerini kontrol ederek tanımlayın. `CadDgnUnderlay` sınıfı, bir DWG içine gömülmüş DGN alt katmanlarını temsil eder.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Adım 4: Alt Katman Bayraklarına Erişin

Bir `CadDgnUnderlay` elde ettiğinizde, özelliklerini ve bayrak durumlarını okumak için `CadUnderlay` tipine dönüştürün. Bayraklar, alt katmanın görünür, kırpılmış veya tek renk olarak işlenip işlenmediğini gösterir.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### Çıktının Size Söyledikleri

- **UnderlayPath / UnderlayName** – dış DGN dosyasının bulunduğu yer.  
- **InsertionPoint (X, Y)** – alt katmanın DWG alanına yerleştirildiği koordinatlar.  
- **RotationAngle** – alt katmana uygulanan dönüş.  
- **ScaleX / ScaleY / ScaleZ** – her eksen için ölçek faktörleri.  
- **Flags** – görünürlük (`UnderlayIsOn`), kırpma (`ClippingIsOn`) ve tek renk işleme (`Monochrome`) durumlarını gösteren boolean değerler.

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| Bayrak kontrolleri için çıktı yok | Alt katman kapalı olduğunda bayraklar 0 olarak varsayılır. | DWG'nin gerçekten aktif bir alt katman içerdiğinden emin olun veya kaynak CAD dosyasında görünürlüğü değiştirin. |
| `Invalid cast` istisnası | Varlık bir `CadDgnUnderlay` değil. | Dönüştürmeden önce `if (entity is CadDgnUnderlay)` kontrolünü doğrulayın. |
| Bayrak çıkarımından sonra görüntü işleme başarısız | Alt katman kırpılmış veya kapalı olabilir, bu da boş bir alan oluşturur. | Nihai görüntüyü işlemeden önce bayrakları (`UnderlayIsOn = true`, `ClippingIsOn = false`) ayarlayın. |

## Sıkça Sorulan Sorular

### S1: Aspose.CAD for .NET'i diğer CAD dosya formatlarıyla kullanabilir miyim?
A1: Aspose.CAD, DWG, DXF, DGN ve daha fazlası dahil olmak üzere çeşitli CAD formatlarını destekler. Tam liste için belgeleri kontrol edin.

### S2: Aspose.CAD for .NET için geçici bir lisans mevcut mu?
A2: Evet, geçici bir lisansı **[here](https://purchase.aspose.com/temporary-license/)** adresinden alabilirsiniz.

### S3: Aspose.CAD for .NET için desteği nerede bulabilirim?
A3: Yardım için destek forumunu **[here](https://forum.aspose.com/c/cad/19)** ziyaret edin.

### S4: Aspose.CAD for .NET'i nasıl satın alabilirim?
A4: Kütüphaneyi **[here](https://purchase.aspose.com/buy)** adresinden satın alabilirsiniz.

### S5: Ücretsiz deneme mevcut mu?
A5: Evet, ücretsiz denemeye **[here](https://releases.aspose.com/)** adresinden erişebilirsiniz.

## Sonuç

Tebrikler! Aspose.CAD for .NET kullanarak **DWG'yi görüntüye dönüştürmeyi** ve **alt katman bayraklarını okumayı** başarıyla öğrendiniz. Bu bilgi ile şunları yapabilirsiniz:

- Web veya raporlama senaryoları için DWG çizimlerini raster görüntüler olarak işleyin.  
- Alt katman özelliklerini inceleyin ve manipüle edin, doğru görüntülenmeyi sağlayın.  
- Nihai görüntüyü oluşturmadan önce görünürlük, kırpma ve tek renk sorunlarını ayıklayın.

Aspose.CAD'in katman yönetimi, metin çıkarımı ve toplu dönüşüm gibi diğer özelliklerini keşfederek CAD otomasyon iş akışlarınızı daha da genişletebilirsiniz.

---

**Son Güncelleme:** 2026-04-09  
**Test Edilen Versiyon:** Aspose.CAD for .NET 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}