---
date: 2026-03-26
description: CAD'den PDF oluşturmayı ve DXF'yi PDF'ye dönüştürmeyi, Aspose.CAD for
  .NET kullanarak, hassas ve uyarlanabilir render için Otomatik Düzen Ölçeklendirme
  ile öğrenin.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'CAD''den PDF Oluştur: Otomatik Düzen Ölçekleme – Aspose.CAD'
url: /tr/net/cad-features-and-support/setting-auto-layout-scaling/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD'den PDF Oluşturma: Otomatik Düzen Ölçeklendirme – Aspose.CAD

Modern .NET uygulamalarında, CAD çizimlerini yüksek kaliteli PDF'lere dönüştürmek yaygın bir gereksinimdir—raporlama, paylaşma veya arşivleme için **CAD'den PDF oluşturmanız** gerektiğinde. Bu öğretici, Aspose.CAD for .NET kullanarak Otomatik Düzen Ölçeklendirmeyi etkinleştirmenizi, piksel mükemmel sonuçlar almanızı ve aynı zamanda **DXF'yi PDF'ye dönüştürmeyi** ve **CAD'yi PDF'ye dışa aktarmayı** minimal kodla nasıl yapacağınızı gösterir.

## Hızlı Yanıtlar
- **Auto Layout Scaling ne yapar?** Sayfa boyutuna uyması için düzeni otomatik olarak ayarlar, geometrik doğruluğu korur.  
- **Hangi formatlar destekleniyor?** Aspose.CAD'in okuyabildiği herhangi bir format (DXF, DWG, DGN, vb.) PDF'ye dışa aktarılabilir.  
- **Lisans gerekli mi?** Geliştirme için ücretsiz deneme sürümü çalışır; üretim için ticari lisans gereklidir.  
- **Sayfa boyutunu değiştirebilir miyim?** Evet—`CadRasterizationOptions` içinde `PageWidth` ve `PageHeight` ayarlayın.  
- **.NET Core ile uyumlu mu?** Kesinlikle, .NET Framework ve .NET Core/5/6+ ile çalışır.

## “CAD'den PDF oluşturma” nedir?
Bir CAD dosyasından PDF oluşturmak, vektör çizim verilerini taşınabilir bir belge formatına rasterleştirmek anlamına gelir. Bu dönüşüm, katmanları, çizgi kalınlıklarını ve renkleri korurken dosyanın CAD yazılımı olmadan herhangi bir cihazda görüntülenebilmesini sağlar.

## Neden Auto Layout Scaling kullanmalısınız?
Auto Layout Scaling, tüm çizimin çıktı sayfasına düzgün bir şekilde sığmasını sağlar ve ölçek faktörleri için manuel hesaplamaları ortadan kaldırır. Özellikle mimari planlar veya mekanik şemalar gibi farklı boyutlardaki çizimlerle çalışırken çok faydalıdır.

## Önkoşullar
Başlamadan önce, aşağıdakilere sahip olduğunuzdan emin olun:

1. **Aspose.CAD for .NET** – En son kütüphaneyi [download page](https://releases.aspose.com/cad/net/) adresinden indirin.  
2. **Bir .NET geliştirme ortamı** – Visual Studio, Rider veya C# destekleyen herhangi bir editör.  
3. **Örnek bir DXF dosyası** – örneğin `conic_pyramid.dxf` veya dönüştürmek istediğiniz herhangi bir CAD dosyası.

## İsim Uzaylarını İçe Aktarın
Aspose.CAD sınıflarına erişebilmek için gerekli isim uzaylarını ekleyin.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Adım 1: CAD Dosyasını Yükleyin
Kaynak çizimi bir `Image` nesnesine yükleyin. Bu, sonraki tüm işlemler için giriş noktasıdır.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Adım 2: Rasterizasyon Seçeneklerini Yapılandırın
Çıktı sayfa boyutlarını tanımlayın. Bu değerleri istediğiniz PDF boyutuna göre ayarlayın.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Adım 3: Auto Layout Scaling'i Etkinleştirin
Çizimin sayfaya kırpılmadan sığması için otomatik ölçeklendirmeyi açın.

```csharp
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Adım 4: PDF Seçeneklerini Oluşturun
Rasterizasyon ayarlarını PDF dışa aktarıcısına bağlayın.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Adım 5: Sonucu Kaydedin – CAD'den PDF Oluşturun
Çıktı yolunu belirleyin ve görüntüyü PDF olarak kaydedin. Bu adım, yapılandırdığınız ölçekleme ile **CAD'den PDF oluşturur**.

```csharp
MyDir = MyDir + "result_out.pdf";
image.Save(MyDir, pdfOptions);
```

## Yaygın Sorunlar ve İpuçları
- **Eksik fontlar veya çizgi stilleri?** CAD dosyası referanslarının gömülü veya sunucuda mevcut olduğundan emin olun.  
- **Büyük dosyalar bellek baskısına neden mi oluyor?** Çizimi parçalar halinde işleyin veya uygulamanın bellek limitini artırın.  
- **Çıktı bulanık mı görünüyor?** Daha yüksek DPI için `PageWidth`/`PageHeight` değerlerini artırın veya `CadRasterizationOptions` içinde `Resolution` ayarlayın.

## Sık Sorulan Sorular

**Q: Auto Layout Scaling'i DXF dışındaki diğer dosya formatlarına uygulayabilir miyim?**  
**A:** Evet, Aspose.CAD otomatik ölçeklendirme için DWG, DGN ve birçok diğer CAD formatını destekler.

**Q: Renderleme sürecinde hataları nasıl yönetebilirim?**  
**A:** Dönüştürme kodunu bir `try‑catch` bloğuna sarın ve ayrıntılı hata bilgileri için `Aspose.CAD.CadException` yakalayın.

**Q: Aspose.CAD'in işleyebileceği dosya boyutu için bir limit var mı?**  
**A:** Kütüphane büyük dosyalar için tasarlanmıştır, ancak performans mevcut RAM ve CPU'ya bağlıdır. Çok büyük çizimleri yeterli kaynaklara sahip bir sunucuda işlemeyi düşünün.

**Q: Çıktı PDF'yi (ör. filigran eklemek veya meta veri eklemek) daha da özelleştirebilir miyim?**  
**A:** Kesinlikle. Kaydettikten sonra PDF'yi değiştirmek için Aspose.PDF kullanabilirsiniz—filigran ekleyin, belge özelliklerini ayarlayın veya sayfaları birleştirin.

**Q: Aspose.CAD için ek kaynakları ve desteği nerede bulabilirim?**  
**A:** Topluluk yardımı için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini inceleyin ve daha derin API detayları için [documentation](https://reference.aspose.com/cad/net/) adresine bakın.

## Sonuç
Artık **CAD'den PDF oluşturmayı**, **Auto Layout Scaling'i** etkinleştirmeyi ve Aspose.CAD for .NET kullanarak **DXF'yi PDF'ye dönüştürmeyi** etkili bir şekilde öğrendiniz. Bu yaklaşım, uygulamayı basit tutarken render kalitesi üzerinde tam kontrol sağlar.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-03-26  
**Test Edilen:** Aspose.CAD for .NET 24.12 (en son)  
**Yazar:** Aspose