---
date: 2026-04-03
description: Aspose.CAD kullanarak C#'ta görünüm alanını nasıl ayarlayacağınızı ve
  DWG'yi PDF'ye nasıl dönüştüreceğinizi öğrenin. Bu DWG'den PDF'ye öğretici, koordinatlarla
  hassas dışa aktarmayı gösterir.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: DWG'yi Koordinatlarla C#'ta PDF'ye Dönüştürme
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: C# ile Koordinatlarla DWG'yi PDF'ye Dönüştürürken Görünüm Alanını Nasıl Ayarlarsınız
  - Aspose.CAD Öğreticisi
url: /tr/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi Koordinatlarla C#'ta PDF'ye Dönüştürme - Aspose.CAD Öğreticisi

## Giriş

Aspose.CAD for .NET kullanarak belirli koordinatlarla DWG dosyalarını PDF'ye dönüştürürken **viewport nasıl ayarlanır** hakkında bu kapsamlı öğreticiye hoş geldiniz. Viewport'u kontrol ederek ihtiyacınız olan alanla tam olarak eşleşen piksel‑mükemmel PDF'ler elde edersiniz—inşaat çizimleri, kat‑plan ön izlemeleri veya herhangi bir BIM iş akışı için mükemmeldir.

## Hızlı Yanıtlar
- **“set viewport” ne anlama geliyor?** CAD çiziminin rasterleştirme sırasında görünen bölgesini ve ölçeklendirmesini tanımlar.  
- **Dönüşümü hangi kütüphane yönetiyor?** Aspose.CAD for .NET.  
- **Bir lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.  
- **Desteklenen platformlar?** .NET 5/6/7 veya .NET Framework 4.6+ ile Windows, Linux ve macOS.  
- **Tipik uygulama süresi?** Temel bir dönüşüm için yaklaşık 10‑15 dakika.

## Önkoşullar

Başlamadan önce, aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

- **Aspose.CAD Kütüphanesi** – .NET için Aspose.CAD kütüphanesini indirin ve kurun. Kütüphaneyi [burada](https://releases.aspose.com/cad/net/) bulabilirsiniz.
- **Geliştirme Ortamı** – .NET geliştirmeyi destekleyen Visual Studio, Rider veya herhangi bir IDE.
- **DWG Dosyası** – Dönüştürme için hazır bir DWG dosyanız olsun. Sağlanan örnek dosyayı veya kendi DWG dosyanızı kullanabilirsiniz.

## Kesin PDF Dışa Aktarımı için Viewport Nasıl Ayarlanır

Viewport ayarlamak, render etmek istediğiniz çizimin tam alanını tanımlamanızı sağlayan temel adımdır. Aşağıdaki kodda yeni bir `CadVportTableObject` oluşturur, üst‑sol koordinatıyla konumlandırır ve genişlik, yükseklik ve en‑boy oranını hesaplarız. Bu, dönüşümün geri kalanını yönlendiren **viewport nasıl ayarlanır** uygulamasıdır.

## Ad Alanlarını İçe Aktarın

C# projenizde gerekli ad alanlarını içe aktarın:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Kodu daha iyi anlamak için adım‑adım bir rehbere ayıralım:

## Adım 1: Belge Dizini Tanımla

```csharp
string MyDir = "Your Document Directory";
```

## Adım 2: Kaynak DWG Dosya Yolunu Ayarla

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Adım 3: DWG Dosyasını Yükle ve Rasterleştirme Seçeneklerini Yapılandır

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Adım 4: Koordinatları ve Viewport'u Tanımla

Burada, dışa aktarmak istediğiniz alanın üst‑sol köşesini, genişliğini ve yüksekliğini belirterek gerçekte **viewport'u ayarlarız** (viewport nasıl ayarlanır).

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Adım 5: Viewport Ayarlarını Uygula

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Adım 6: PDF Seçeneklerini Yapılandır ve Dışa Aktar

Şimdi her şeyi birleştirip, az önce hazırladığımız rasterleştirme seçeneklerini kullanarak **DWG'yi PDF'ye dönüştürüyoruz**.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Adım 7: Başarı Mesajını Göster

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Yaygın Kullanım Senaryoları

- **İnşaat dokümantasyonu** – Belirli kat‑plan bölümlerinin yazdırılabilir PDF'lerini oluşturun.
- **BIM koordinasyonu** – Çakışma tespiti için yalnızca ilgi alanını dışa aktarın.
- **Müşteri sunumları** – Tüm çizimi göstermeden seçilen bir oda veya yükselişin temiz PDF'sini sunun.

## Sonuç

Tebrikler! Aspose.CAD for .NET kullanarak kesin koordinatlarla **DWG'yi PDF'ye dönüştürdünüz** ve **viewport nasıl ayarlanır** öğrendiniz. Bu **dwg to pdf öğreticisi**, **dwg'den pdf oluşturma** ve **dwg'yi pdf c# olarak dışa aktarma** işlemlerinin çıktının alanı üzerinde tam kontrol sağlarken nasıl yapılacağını gösterir.

## SSS

### S1: Aspose.CAD'i diğer CAD dosya formatlarıyla kullanabilir miyim?
C1: Evet, Aspose.CAD DWG, DXF, DWF ve daha fazlası dahil olmak üzere çeşitli CAD formatlarını destekler.

### S2: Dönüşüm sürecinde hataları nasıl ele alabilirim?
C2: İstisnaları yakalamak ve yönetmek için try‑catch blokları kullanarak hata işleme mekanizmaları uygulayın.

### S3: Aspose.CAD hem Windows hem de Linux ortamları için uygun mu?
C3: Evet, Aspose.CAD hem Windows hem de Linux platformlarıyla uyumludur.

### S4: PDF çıktısını daha da özelleştirebilir miyim?
C4: Kesinlikle! PDF çıktısını özel gereksinimlerinize göre uyarlamak için Aspose.CAD'in sunduğu kapsamlı seçenekleri keşfedin.

### S5: Ek destek veya topluluk tartışmalarını nereden bulabilirim?
C5: Topluluk desteği ve tartışmalar için [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

## Ek Sıkça Sorulan Sorular

**S: Bu yöntem büyük DWG dosyaları (yüzlerce MB) ile çalışır mı?**  
C: Evet. Rasterleştirme sayfa‑sayfa gerçekleştirilir ve kalite ile bellek kullanımını dengelemek için `rasterizationOptions` (ör. `Resolution`) ayarını değiştirebilirsiniz.

**S: Birden fazla viewport'u ayrı PDF sayfalarına dışa aktarabilir miyim?**  
C: `cadImage.ViewPorts` üzerinden döngü yapabilir, her birini aktif olarak ayarlayıp her sayfa için `Save` çağırabilir, ardından PDF'leri Aspose.PDF kullanarak birleştirebilirsiniz.

**S: Oluşturulan PDF'ye bir filigran eklemek mümkün mü?**  
C: PDF'yi kaydettikten sonra Aspose.PDF ile yeniden açıp kullanıcıya sunmadan önce metin veya görsel bir filigran uygulayabilirsiniz.

---

**Son Güncelleme:** 2026-04-03  
**Test Edilen Versiyon:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}