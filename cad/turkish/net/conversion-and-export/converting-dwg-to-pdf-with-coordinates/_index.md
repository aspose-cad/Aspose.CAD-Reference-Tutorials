---
title: C#'ta DWG'yi Koordinatlarla PDF'ye Dönüştürme - Aspose.CAD Eğitimi
linktitle: C#'ta Koordinatlarla DWG'yi PDF'ye dönüştürme
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD kullanarak C#'ta DWG'yi belirli koordinatlarla PDF'ye nasıl dönüştüreceğinizi öğrenin. Hassas ve verimli CAD dosya dönüşümleri için adım adım kılavuzumuzu izleyin.
weight: 11
url: /tr/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#'ta DWG'yi Koordinatlarla PDF'ye Dönüştürme - Aspose.CAD Eğitimi

## giriiş

Aspose.CAD for .NET kullanarak DWG dosyalarını belirtilen koordinatlarla PDF'ye dönüştürmeyi anlatan bu kapsamlı eğitime hoş geldiniz. Aspose.CAD, geliştiricilerin .NET uygulamalarında CAD dosya formatlarıyla sorunsuz bir şekilde çalışmasına olanak tanıyan güçlü bir kütüphanedir. Bu eğitimde, hassasiyeti artırmak için belirli koordinatlar sağlayarak bir DWG dosyasını PDF'ye dönüştürme sürecinde size yol göstereceğiz.

## Önkoşullar

Başlamadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

- Aspose.CAD Kütüphanesi: .NET için Aspose.CAD kütüphanesini indirip yükleyin. Kütüphaneyi bulabilirsiniz[Burada](https://releases.aspose.com/cad/net/).

- Geliştirme Ortamı: Visual Studio veya tercih edilen herhangi bir IDE de dahil olmak üzere uyumlu bir geliştirme ortamı kurduğunuzdan emin olun.

- DWG Dosyası: Dönüştürme için hazır bir DWG dosyası bulundurun. Sağlanan örnek dosyayı veya özel DWG dosyanızı kullanabilirsiniz.

## Ad Alanlarını İçe Aktar

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

Daha iyi anlaşılması için kodu adım adım kılavuza ayıralım:

## Adım 1: Belge Dizinini Tanımlayın

```csharp
string MyDir = "Your Document Directory";
```

## Adım 2: Kaynak DWG Dosya Yolunu Ayarlayın

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## 3. Adım: DWG Dosyasını Yükleyin ve Rasterleştirme Seçeneklerini Yapılandırın

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Adım 4: Koordinatları ve Görünüm Penceresini Tanımlayın

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

## Adım 5: Görünüm Penceresi Ayarlarını Uygulayın

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

## 6. Adım: PDF Seçeneklerini Yapılandırın ve Dışa Aktarın

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Adım 7: Başarı Mesajını Görüntüleyin

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Çözüm

Tebrikler! Aspose.CAD for .NET'i kullanarak bir DWG dosyasını belirtilen koordinatlara sahip PDF'ye başarıyla dönüştürdünüz. Bu eğitimde temel adımlar yer alıyordu ve geliştiriciler için net bir kılavuz sağlanıyordu.

## SSS'ler

### S1: Aspose.CAD'i diğer CAD dosya formatlarıyla kullanabilir miyim?

Cevap1: Evet, Aspose.CAD, DWG, DXF, DWF ve daha fazlası dahil olmak üzere çeşitli CAD formatlarını destekler.

### S2: Dönüştürme işlemi sırasındaki hataları nasıl halledebilirim?

Cevap 2: İstisnaları yakalamak ve yönetmek için try-catch bloklarını kullanarak hata işleme mekanizmalarını uygulayın.

### S3: Aspose.CAD hem Windows hem de Linux ortamlarına uygun mudur?

Cevap3: Evet, Aspose.CAD hem Windows hem de Linux platformlarıyla uyumludur.

### S4: PDF çıktısını daha da özelleştirebilir miyim?

A4: Kesinlikle! PDF çıktısını özel gereksinimlerinize göre uyarlamak için Aspose.CAD tarafından sağlanan kapsamlı seçenekleri keşfedin.

### S5: Ek desteği veya topluluk tartışmalarını nerede bulabilirim?

A5: ziyaret edin[Aspose.CAD Forumu](https://forum.aspose.com/c/cad/19) topluluk desteği ve tartışmalar için.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
