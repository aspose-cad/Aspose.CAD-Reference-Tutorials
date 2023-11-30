---
title: DWG Belgelerini C#'ta İşleme - Aspose.CAD Guide
linktitle: DWG Belgelerini C#'ta Oluşturma
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD kullanarak DWG belgelerini C#'ta nasıl oluşturacağınızı öğrenin. Bu adım adım kılavuz, kod örnekleriyle içe aktarmayı, yapılandırmayı ve kaydetmeyi kapsar.
type: docs
weight: 17
url: /tr/net/image-manipulation-and-rendering/rendering-dwg-documents/
---
## giriiş

Aspose.CAD kullanarak DWG belgelerinin C#'ta işlenmesine ilişkin kapsamlı kılavuza hoş geldiniz. İster deneyimli bir geliştirici olun ister .NET'e yeni başlıyor olun, bu eğitim size DWG dosyalarını verimli bir şekilde işlemek için Aspose.CAD'den yararlanma sürecinde yol gösterecektir. Aspose.CAD, CAD dosya formatlarıyla çalışmak için güçlü işlevler sağlayan güçlü bir API'dir ve bu da onu DWG dosyalarıyla çalışan geliştiricilerin tercihi haline getirir.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşullara sahip olduğunuzdan emin olun:

- Temel C# programlama dili bilgisi.
- Makinenizde Visual Studio yüklü.
-  Aspose.CAD kütüphanesi projenize entegre edilmiştir. Şuradan indirebilirsiniz[Burada](https://releases.aspose.com/cad/net/).
- Örneklerle birlikte "Bottom_plate.dwg" gibi örnek bir DWG dosyası.

## Ad Alanlarını İçe Aktar

Başlamak için C# kodunuzun başında gerekli ad alanlarını içe aktardığınızdan emin olun:

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

Şimdi verilen örneği birden çok adıma ayıralım:

## Adım 1: DWG Dosyasını Yükleyin

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //DWG dosyasını yükleme kodunuz buraya gelecek.
}
```

## Adım 2: Rasterleştirme Seçeneklerini Yapılandırın

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Buraya ek rasterleştirme yapılandırmaları eklenebilir.
```

## Adım 3: Çizilecek Bölgeyi Tanımlayın

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## 4. Adım: Yeni Bir Görünüm Penceresi Oluşturun

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Adım 5: Aktif Görünümü Değiştirin

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

## Adım 6: PDF Seçeneklerini Yapılandırın

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Adım 7: Oluşturulan DWG'yi PDF olarak kaydedin

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Çözüm

Tebrikler! C# dilinde Aspose.CAD kullanarak bir DWG belgesini başarıyla PDF'ye dönüştürdünüz. Daha fazla özelliği keşfetmekten ve kodu özel gereksinimlerinize göre özelleştirmekten çekinmeyin.

## SSS'ler

### S1: Aspose.CAD'i diğer CAD dosya formatlarıyla kullanabilir miyim?

Cevap1: Evet, Aspose.CAD, DWG, DXF, DWF ve daha fazlası dahil olmak üzere çeşitli CAD formatlarını destekler.

### S2: Aspose.CAD .NET Core ile uyumlu mu?

Cevap2: Evet, Aspose.CAD hem .NET Framework hem de .NET Core ile uyumludur.

### S3: Bir DWG dosyasındaki farklı düzenleri nasıl işleyebilirim?

 Cevap3: İstenilen düzeni şurada belirtebilirsiniz:`Layouts` mülkiyet`CadRasterizationOptions`.

### S4: Aspose.CAD kullanımında lisanslamayla ilgili hususlar var mı?

 Cevap4: Lisans ayrıntıları için şu adresi ziyaret edin:[Burada](https://purchase.aspose.com/buy).

### S5: Ek desteği nerede bulabilirim?

 A5: ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği ve tartışmalar için.