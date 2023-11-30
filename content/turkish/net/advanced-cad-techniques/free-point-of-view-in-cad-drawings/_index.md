---
title: CAD Çizimlerinde Serbest Bakış Açısı - Aspose.CAD Guide
linktitle: CAD Çizimlerinde Serbest Bakış Açısı
second_title: Aspose.CAD .NET - CAD ve BIM Dosya Formatı
description: Aspose.CAD for .NET ile CAD görselleştirme özgürlüğünü keşfedin. Benzersiz bir bakış açısı için adım adım kılavuzumuzu izleyin.
type: docs
weight: 11
url: /tr/net/advanced-cad-techniques/free-point-of-view-in-cad-drawings/
---
Bilgisayar Destekli Tasarım (CAD) alanında çizimlerde özgür bir bakış açısı kazanmak, karmaşık tasarımları görselleştirmenin ve sunmanın çok önemli bir yönüdür. Aspose.CAD for .NET, bu özgürlüğü elde etmek için güçlü bir çözüm sunarak kullanıcıların CAD çizimlerini kolaylıkla değiştirmesine ve optimize etmesine olanak tanır. Bu adım adım kılavuzda Aspose.CAD for .NET kullanarak CAD çizimlerinde özgür bir bakış açısı elde etme sürecini inceleyeceğiz.

## Önkoşullar

Eğiticiye dalmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

1. Aspose.CAD Kurulumu
 Geliştirme ortamınızda Aspose.CAD for .NET'in kurulu olduğundan emin olun. Değilse, adresinden indirebilirsiniz.[Aspose.CAD web sitesi](https://releases.aspose.com/cad/net/).

2. CAD Çizim Dosyası
Düzenlemek istediğiniz bir CAD çizim dosyasını hazırlayın. Bu kılavuz için "conic_pyramid.dxf" adlı örnek bir dosya kullanacağız.

3. Geliştirme Ortamı
Çalışan bir .NET geliştirme ortamının Visual Studio veya tercih edilen herhangi bir IDE ile kurulmasını sağlayın.

## Ad Alanlarını İçe Aktar

.NET projenize Aspose.CAD işlevselliği için gerekli ad alanlarını içe aktarın. Aşağıdaki kod parçasını dosyanızın en üstüne ekleyin:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```


## 1. Adım: Belge Dizinini Tanımlayın

```csharp
// Belgeler dizininin yolu.
string MyDir = "Your Document Directory";
```

"Belge Dizininiz"i belge dizininizin gerçek yolu ile değiştirdiğinizden emin olun.

## Adım 2: Kaynak Dosyayı Belirleyin

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

CAD çizim dosyanızın yolunu belirtin.

## Adım 3: Çıkış Yolunu Ayarlayın

```csharp
var outPath = Path.Combine(MyDir, "FreePointOfView_out.jpg");
```

Değiştirilen CAD çiziminin kaydedileceği yolu tanımlayın.

## Adım 4: CAD Görüntüsünü Yükleyin

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
```

Aspose.CAD'i kullanarak CAD çizimini yükleyin.

## 5. Adım: JPEG Seçeneklerini Yapılandırın

```csharp
JpegOptions options = new JpegOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500, PageHeight = 1500
    }
};
```

CAD çizimini JPEG formatına aktarma seçeneklerini yapılandırın.

## Adım 6: Dönme Açılarını Ayarlayın

```csharp
float xAngle = 10; //X ekseni boyunca dönme açısı
float yAngle = 30; //Y ekseni boyunca dönme açısı
float zAngle = 40; //Z ekseni boyunca dönme açısı
((CadRasterizationOptions)(options.VectorRasterizationOptions)).ObserverPoint = new ObserverPoint(xAngle, yAngle, zAngle);
```

İstenilen bakış açısına ulaşmak için X, Y ve Z eksenleri boyunca dönüş açılarını belirtin.

## Adım 7: Düzenlenmiş CAD Çizimini Kaydedin

```csharp
cadImage.Save(outPath, options);
}
```

Değiştirilen CAD çizimini belirtilen çıktı yoluna kaydedin.

## Adım 8: Başarı Mesajını Görüntüleyin

```csharp
Console.WriteLine("\n3D images exported successfully to JPEG.\nFile saved at " + outPath);
```

Kullanıcıyı 3D görüntünün başarıyla dışa aktarıldığı konusunda bilgilendirin.

## Çözüm

Bu eğitimde Aspose.CAD for .NET kullanarak CAD çizimlerinde özgür bir bakış açısı elde etme sürecini araştırdık. Bu adım adım talimatları izleyerek CAD görselleştirme yeteneklerinizi geliştirebilir ve tasarımlarınızı yeni keşfedilmiş bir perspektifle sunabilirsiniz.


## SSS'ler

### S1: Aspose.CAD for .NET'i diğer CAD dosya formatlarıyla kullanabilir miyim?

Cevap1: Evet, Aspose.CAD for .NET, DWG ve DXF dahil olmak üzere çeşitli CAD dosya formatlarını destekler.

### S2: Aspose.CAD'in deneme sürümü mevcut mu?

 C2: Evet, ücretsiz deneme sürümünü şuradan indirebilirsiniz:[Burada](https://releases.aspose.com/).

### S3: Aspose.CAD için nasıl geçici lisans alabilirim?

 Cevap 3: Şu adresten geçici bir lisans alabilirsiniz:[Burada](https://purchase.aspose.com/temporary-license/).

### S4: Aspose.CAD için ek desteği nerede bulabilirim?

 A4: Ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) topluluk desteği ve tartışmalar için.

### S5: Farklı görüntü formatları için dışa aktarma seçeneklerini özelleştirebilir miyim?

A5: Kesinlikle! Aspose.CAD, dışa aktarma sürecini özel gereksinimlerinize göre uyarlamanıza olanak tanıyan bir dizi kişiselleştirme seçeneği sunar.