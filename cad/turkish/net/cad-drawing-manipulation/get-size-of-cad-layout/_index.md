---
date: 2026-03-21
description: Aspose.CAD kullanarak .NET’te CAD düzen boyutunu nasıl alacağınızı öğrenin.
  Verimli CAD dosyası manipülasyonu için adım adım rehberimizi izleyin.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET'te CAD Düzen Boyutunu Al
url: /tr/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET'te CAD Düzen Boyutunu Alın

## Giriş

Bu kapsamlı öğreticide, Aspose.CAD .NET kütüphanesini kullanarak **CAD düzen boyutunu nasıl alacağınızı** keşfedeceksiniz. Bir CAD görüntüleyici oluşturuyor, küçük resimler üretiyor ya da sonraki işlem adımları için kesin düzen boyutlarına ihtiyacınız varsa, her düzenin tam boyutunu bilmek çok önemlidir. Çizimi yüklemekten düzen boyutlarını çıkarmaya ve isteğe bağlı olarak bunları görüntü olarak kaydetmeye kadar tüm iş akışını adım adım inceleyeceğiz; böylece bu yeteneği kendi uygulamalarınıza güvenle entegre edebileceksiniz.

## Hızlı Yanıtlar
- **“CAD düzen boyutunu al” ne anlama geliyor?** Bir CAD dosyasındaki her boş olmayan düzenin (paper space) genişlik ve yüksekliğini (çizim birimlerinde) elde etmektir.  
- **Hangi kütüphane bunu destekliyor?** Aspose.CAD for .NET, düzen bilgilerine erişmek için basit bir API sunar.  
- **Lisans gerekli mi?** Değerlendirme için ücretsiz deneme sürümü yeterlidir; üretim kullanımı için ticari lisans gereklidir.  
- **Desteklenen formatlar?** DWG, DXF ve birçok diğer CAD/BIM formatı tam olarak desteklenir.  
- **Tipik uygulama süresi?** Temel bir boyut‑alma rutinı için yaklaşık 10‑15 dakikadır.

## “CAD düzen boyutunu al” nedir?
CAD düzen boyutunu almak, bir CAD çiziminde tanımlı her düzenin (paper space) geometrik sınırlarını çıkarmak anlamına gelir. Bu sınırlar, çizimin yerel birimlerinde (genellikle milimetre veya inç) ifade edilir ve ölçekleme, baskı veya ön izleme görüntüleri oluşturma gibi görevler için faydalıdır.

## Neden Aspose.CAD ile CAD düzen boyutunu almalı?
- **CAD yazılımı gerekmez** – Tamamen sunucu tarafında çalışır.  
- **Çapraz‑platform** – .NET Framework, .NET Core ve .NET 5/6+ ile uyumludur.  
- **Doğru ölçümler** – Dosyada saklanan tam sınırları döndürür, manuel ayrıştırmayı önler.  
- **Kolay entegrasyon** – Basit API çağrıları mevcut C# projelerine doğal olarak uyum sağlar.

## Önkoşullar

Kodlamaya başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- Aspose.CAD for .NET yüklü. İndirmek için [Aspose.CAD for .NET indirme sayfasını](https://releases.aspose.com/cad/net/) ziyaret edebilirsiniz.  
- Analiz etmek istediğiniz bir veya daha fazla CAD dosyası (DWG, DXF vb.). Bu kılavuzda örnek dosyalar olarak `conic_pyramid.dxf` ve `Bottom_plate.dwg` kullanılmaktadır.

## Ad Alanlarını İçe Aktarın

.NET projenizde, gerekli ad alanlarını içe aktararak başlayın:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Adım 1: Belge Dizinini Ayarlayın

CAD dosyalarınızı içeren klasörü tanımlayın. Yer tutucuyu makinenizdeki gerçek yol ile değiştirin.

```csharp
string MyDir = "Your Document Directory";
```

## Adım 2: CAD Dosya Yollarını Belirtin

İşlemek istediğiniz her CAD dosyasına işaret eden bir dizi oluşturun.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Adım 3: CAD Dosyaları Üzerinde Döngü

Her dosyayı yükleyin, formatını tespit edin ve düzen bilgilerini çıkarmaya hazırlanın.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## Adım 4: Boş Olmayan Düzenleri Al

Sadece çizim varlıkları içeren düzenleri döndüren bir yardımcı metoda ihtiyacımız var. Boş düzenler, raporlanacak bir boyuta sahip olmadıkları için göz ardı edilir.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## Adım 5: DWG Dosyaları İçin Düzenleri Al

DWG dosyaları, düzen bilgilerini `HeaderVariables` tablosunda saklar. Aşağıdaki yöntem, bir DWG çizimi için tüm boş olmayan düzenlerin adlarını çıkarır.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Adım 6: DXF Dosyaları İçin Düzenleri Al

DXF dosyaları farklı bir yapıya sahiptir. Bu yöntem, varlık içeren paper space düzenlerini bulmak için `Tables` koleksiyonunu ayrıştırır.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Adım 7: Düzen Boyutunu Al ve Görüntü Olarak Kaydet

Son olarak, keşfedilen her düzeni döngüye alıp sınırlarını okuyun ve isteğe bağlı olarak görsel doğrulama için düzeni bir görüntü dosyasına render edin.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## Yaygın Sorunlar ve İpuçları

- **Düzen adları eksik:** CAD dosyasının gerçekten paper space düzenleri içerdiğinden emin olun; bazı dosyalarda yalnızca model space bulunur.  
- **Yanlış birimler:** Boyut, çizimin yerel birimlerinde döndürülür. Gerekirse milimetre veya inçe dönüştürün.  
- **Performans:** Çok büyük DWG/DXF dosyalarının yüklenmesi bellek yoğun olabilir; dosyaları asenkron veya toplu işleyerek performansı iyileştirmeyi düşünün.

## Sıkça Sorulan Sorular

**S: Aspose.CAD tüm CAD dosya formatlarıyla uyumlu mu?**  
C: Evet, Aspose.CAD DWG, DXF, DGN ve birçok BIM dosya türü dahil olmak üzere geniş bir format yelpazesini destekler.

**S: Görüntü‑kaydetme seçeneklerini özelleştirebilir miyim?**  
C: Kesinlikle! `CadRasterizationOptions` (format, çözünürlük, arka plan rengi vb.) ayarlarını ihtiyaçlarınıza göre düzenleyebilirsiniz.

**S: Ek belgeleri nereden bulabilirim?**  
C: Ayrıntılı API referansları ve daha fazla örnek için [Aspose.CAD belgelerine](https://reference.aspose.com/cad/net/) bakın.

**S: Ücretsiz bir deneme sürümü var mı?**  
C: Evet, bir [ücretsiz deneme](https://releases.aspose.com/) ile Aspose.CAD'i keşfedebilirsiniz.

**S: Teknik destek nasıl alınır?**  
C: Teknik destek için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

**Son Güncelleme:** 2026-03-21  
**Test Edilen Sürüm:** Aspose.CAD 24.11 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}