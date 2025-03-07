---
title: Aspose.CAD for .NET'te CAD Düzeninin Boyutunu Alın
linktitle: CAD Düzeninin Boyutunu Alın
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD kullanarak .NET'te CAD düzen boyutunu nasıl alacağınızı öğrenin. Verimli CAD dosyası manipülasyonu için adım adım kılavuzumuzu izleyin.
weight: 14
url: /tr/net/cad-drawing-manipulation/get-size-of-cad-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET'te CAD Düzeninin Boyutunu Alın

## giriiş

Aspose.CAD for .NET kullanarak CAD düzenlerinin boyutunu elde etmeye yönelik bu kapsamlı kılavuza hoş geldiniz. Aspose.CAD, geliştiricilerin CAD dosyalarıyla sorunsuz bir şekilde çalışmasını sağlayan güçlü bir kütüphanedir. Bu eğitimde, pratik örnekler ve adım adım talimatlar kullanarak CAD düzenlerinin boyutunu alma sürecinde size yol göstereceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.CAD for .NET: Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. adresinden indirebilirsiniz.[Aspose.CAD for .NET indirme sayfası](https://releases.aspose.com/cad/net/).

- Belge Dosyaları: Çalışmak istediğiniz CAD dosyalarını hazırlayın. Bu eğitimde örnek olarak "conic_pyramid.dxf" ve "Bottom_plate.dwg" kullanılmıştır.

Şimdi başlayalım!

## Ad Alanlarını İçe Aktar

.NET projenizde gerekli ad alanlarını içe aktararak başlayın:

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

## 1. Adım: Belge Dizinini Ayarlayın

 Belge dizininizin yolunu ayarlayın. Yer değiştirmek`"Your Document Directory"` gerçek yol ile.

```csharp
string MyDir = "Your Document Directory";
```

## Adım 2: CAD Dosya Yollarını Belirleyin

Analiz etmek istediğiniz bir dizi CAD dosyası yolu tanımlayın. Bu örnekte "conic_pyramid.dxf" ve "Bottom_plate.dwg" kullanıyoruz.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Adım 3: CAD Dosyalarını Yineleyin

Her CAD dosyasını yineleyin ve düzen bilgilerini alın.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (sonraki adıma devam et)
    }
}
```

## 4. Adım: Boş Olmayan Düzenler Alın

CAD dosya türüne göre boş olmayan düzenler elde etmek için bir yardımcı yöntem tanımlayın.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (sonraki adıma devam et)
}
```

## Adım 5: DWG Dosyaları İçin Düzenleri Alın

DWG dosyaları için boş olmayan düzenleri almak üzere mantık uygulayın.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (sonraki adıma devam et)
}
```

## Adım 6: DXF Dosyaları İçin Düzenleri Alın

DXF dosyaları için boş olmayan düzenleri almak üzere mantık uygulayın.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (sonraki adıma devam et)
}
```

## Adım 7: Düzen Boyutunu Alın ve Resim Olarak Kaydedin

Düzen boyutunu alma ve bunu resim olarak kaydetme işlemini tamamlayın.

```csharp
foreach (string layout in layouts)
{
    // ... (sonraki adıma devam et)
}
```

## Çözüm

Tebrikler! Aspose.CAD for .NET'i kullanarak CAD düzenlerinin boyutunu nasıl alacağınızı başarıyla öğrendiniz. Bu eğitim, projenizi ayarlamaktan düzen bilgilerinin alınmasına ve görüntü olarak kaydedilmesine kadar önemli adımları kapsıyordu. Artık verimli CAD dosyası manipülasyonu için bu bilgiyi .NET uygulamalarınıza dahil edebilirsiniz.

## SSS'ler

### S1: Aspose.CAD tüm CAD dosya formatlarıyla uyumlu mudur?

Cevap1: Evet, Aspose.CAD, DWG ve DXF dahil olmak üzere çeşitli CAD dosya formatlarını destekler.

### S2: Görüntü kaydetme seçeneklerini özelleştirebilir miyim?

A2: Kesinlikle! Özel gereksinimlerinizi karşılamak için format ve çözünürlük gibi görüntü seçeneklerini ayarlayabilirsiniz.

### S3: Ek belgeleri nerede bulabilirim?

 A3: Bkz.[Aspose.CAD belgeleri](https://reference.aspose.com/cad/net/) detaylı bilgi ve örnekler için.

### S4: Ücretsiz deneme sürümü mevcut mu?

 Cevap4: Evet, Aspose.CAD'i aşağıdaki yöntemlerle keşfedebilirsiniz:[ücretsiz deneme](https://releases.aspose.com/).

### S5; Nasıl teknik destek alabilirim?

 Cevap5: Teknik destek için şu adresi ziyaret edin:[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
