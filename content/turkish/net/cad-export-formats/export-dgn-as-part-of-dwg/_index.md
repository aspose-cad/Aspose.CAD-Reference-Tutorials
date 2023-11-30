---
title: Aspose.CAD for .NET'te DGN'yi DWG'nin bir parçası olarak dışa aktarın
linktitle: DGN'yi DWG'nin bir parçası olarak dışa aktarın
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET'te DWG'nin bir parçası olarak DGN'yi nasıl dışa aktaracağınızı öğrenin. Sorunsuz entegrasyon için adım adım kılavuzumuzu izleyin.
type: docs
weight: 11
url: /tr/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## giriiş

.NET geliştirme dünyasında Aspose.CAD, Bilgisayar Destekli Tasarım (CAD) dosyalarıyla çalışmak için güçlü bir kütüphane olarak öne çıkıyor. Bu eğitim, Aspose.CAD for .NET kullanarak bir DGN (Tasarım) dosyasını bir DWG (Çizim) dosyasının parçası olarak dışa aktarma sürecinde size rehberlik edecektir. İster deneyimli bir geliştirici olun ister yeni başlıyor olun, bu adım adım kılavuz, bu özel görevi verimli bir şekilde gerçekleştirmek için Aspose.CAD'in yeteneklerinden yararlanmanıza yardımcı olacaktır.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

-  Aspose.CAD for .NET: Aspose.CAD for .NET kütüphanesinin kurulu olduğundan emin olun. İndirebilirsin[Burada](https://releases.aspose.com/cad/net/).

- Geliştirme Ortamı: Visual Studio gibi tercih ettiğiniz .NET geliştirme ortamını kurun.

- Temel C# Bilgisi: C# programlama diline aşina olun.

## Ad Alanlarını İçe Aktar

Aspose.CAD işlevselliğine erişmek için C# projenize gerekli ad alanlarını ekleyin. Kod dosyanızın başına aşağıdaki kullanma yönergelerini ekleyin:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Şimdi sağlanan kodu birden çok adıma ayıralım:

## 1. Adım: Dosya Yollarını Tanımlayın

```csharp
//Giriş ve Çıkış dosyası yolları
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Adım 2: PdfOptions Örneği Oluşturun

```csharp
// DWG'yi PDF'ye aktarmak için PdfOptions sınıfının bir örneğini oluşturun
PdfOptions exportOptions = new PdfOptions();
```

## Adım 3: DWG Dosyasını Yükleyin

```csharp
// Mevcut DWG dosyasını resim olarak yükleyin ve CadImage türüne dönüştürün
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Adım 4: Varlıklar Arasında Yineleme Yapın

```csharp
// DWG dosyasındaki her varlığı yineleyin
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Adım 5: Varlık Türünü Kontrol Edin

```csharp
// Varlığın bir görüntü tanımı olup olmadığını kontrol edin
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Adım 6: Alt Katman Yolunu Alın

```csharp
// Bu bir görüntü tanımıysa, nesnenin dış referansını alın
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Adım 7: Rasterleştirme Seçeneklerini Tanımlayın

```csharp
// CadRasterizationOptions nesnesi için ayarları tanımlayın
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Adım 8: DWG'yi PDF'ye aktarın

```csharp
// Kaydet yöntemini çağırarak DWG'yi PDF'ye aktarın
cadImage.Save(outPath, exportOptions);
```

## Çözüm

Tebrikler! Aspose.CAD for .NET'i kullanarak bir DGN dosyasını DWG dosyasının bir parçası olarak dışa aktarma işlemini başarıyla gerçekleştirdiniz. Bu eğitimde, bu özel görevi sorunsuz bir şekilde gerçekleştirmeniz için size temel adımlar ve kod parçacıkları sağlanmıştır.

## SSS'ler

### S1: Aspose.CAD for .NET'i ticari projelerimde kullanabilir miyim?
 A1: Evet, yapabilirsin. Ziyaret etmek[Burada](https://purchase.aspose.com/buy) Lisanslama seçeneklerini keşfetmek için.

### S2: İşleyebileceğim DWG dosyalarının boyutunda herhangi bir sınırlama var mı?
Cevap2: Aspose.CAD büyük DWG dosyalarının işlenmesini destekler ancak donanım sınırlamaları geçerli olabilir.

### S3: Deneme sürümü mevcut mu?
 A3: Evet, ücretsiz deneme sürümünden yararlanabilirsiniz[Burada](https://releases.aspose.com/).

### S4: Geçici lisansları nasıl alabilirim?
 Cevap4: Geçici lisanslar alınabilir[Burada](https://purchase.aspose.com/temporary-license/).

### S5: Sorunla karşılaşırsam nereden yardım alabilirim?
 Cevap5: Aspose.CAD forumunu ziyaret edebilirsiniz[Burada](https://forum.aspose.com/c/cad/19) destek için.