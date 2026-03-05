---
date: 2026-03-05
description: Aspose.CAD for .NET ile DWG'yi PDF'ye dönüştürürken kaydetme işlemlerinde
  zaman aşımını nasıl ayarlayacağınızı öğrenin. .NET uygulamalarınızda verimliliği
  ve kontrolü artırın.
linktitle: Setting Timeout on Save Operation
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Kaydetme İşleminde Zaman Aşımını Nasıl Ayarlarsınız - Aspose.CAD Öğreticisi
url: /tr/net/advanced-cad-techniques/setting-timeout-on-save-operation/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kaydetme İşleminde Zaman Aşımını Ayarlama - Aspose.CAD Öğreticisi

## Giriş

Bu rehberde, CAD kaydetme işlemlerinde **zaman aşımını nasıl ayarlayacağınızı** öğreneceksiniz; bu teknik, uzun süren dönüşümlerin yanıt vermeyen süreçlere dönüşmesini önlemeye yardımcı olur. Zaman aşımını yönetmek, **DWG'yi PDF'ye dönüştürürken** veya **CAD PDF dosyalarını dışa aktarırken** toplu işler veya web hizmetlerinde özellikle faydalıdır. Aspose.CAD for .NET, güçlü rasterleştirme motorundan yararlanırken kaydetme işlemini kontrol etmenizi sağlayan temiz bir API sunar.

## Hızlı Yanıtlar
- **Zaman aşımı neyi kontrol eder?** Belirtilen süreden daha uzun sürerse kaydetme/dışa aktarma işlemini iptal eder.  
- **Hangi formatlar en çok fayda sağlar?** İşleme süresi değişebilen büyük DWG dosyalarını PDF'ye veya raster görüntülere dönüştürmek.  
- **Lisans gerekir mi?** Üretim kullanımı için geçerli bir Aspose.CAD lisansı gereklidir; ücretsiz deneme sürümü değerlendirme için çalışır.  
- **Süreyi özelleştirebilir miyim?** Evet—senaryonuza uygun olarak `Thread.Sleep` değerini (milisaniye cinsinden) değiştirmeniz yeterlidir.  
- **Bu yaklaşım async‑uyumlu mu?** Örnek, `Task.Factory.StartNew` kullanır ve async iş akışlarına kolayca entegre edilmesini sağlar.

## CAD kaydetme bağlamında “zaman aşımını nasıl ayarlarsınız” ne anlama geliyor?

Zaman aşımı ayarlamak, kaydetme seçeneklerine bir `InterruptionToken` eklemek ve önceden tanımlanmış bir süreden sonra bir kesinti tetiklemek anlamına gelir. Bu, işlemin süresiz olarak takılı kalmasını önler ve size öngörülebilir performans ve daha iyi kaynak yönetimi sağlar.

## Neden Aspose.CAD'i DWG'yi PDF'ye zaman aşımıyla dönüştürmek için kullanmalısınız?

- **Güvenilirlik:** Kontrol dışı bir dönüşümün hizmetinizi engellemesini garanti eder.  
- **Ölçeklenebilirlik:** Tek bir dosyanın boru hattını durdurma korkusu olmadan birçok dosyayı paralel işleyebilmenizi sağlar.  
- **Kalite:** Güvenlik kontrolleri eklerken Aspose.CAD'in yüksek doğruluklu rasterleştirmesini korur.

## Önkoşullar

Başlamadan önce, aşağıdakilere sahip olduğunuzdan emin olun:

- **Aspose.CAD for .NET** – projenize entegre edilmiş. Bunu [buradan](https://releases.aspose.com/cad/net/) indirebilirsiniz.  
- **Document Directory** – kaynak DWG dosyalarınızın ve çıktı PDF'lerinizin bulunacağı bir klasör.

## Ad Alanlarını İçe Aktarın

İlk olarak, rasterleştirme, PDF seçenekleri ve kesinti mekanizması için ihtiyaç duyacağımız sınıfları sağlayan ad alanlarını içe aktarın.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Threading;
using System.Threading.Tasks;
```

## Kaydetme İşleminde Zaman Aşımını Nasıl Ayarlarsınız

Aşağıda adım adım bir rehber bulunmaktadır. Her adım kısa bir açıklama ve ardından orijinal kod bloğunu (değiştirilmemiş) içerir.

### Adım 1: CAD Çizimini Yükleyin

Kaynak DWG dosyasını belirlenen dizinden yüklüyoruz. `Image.Load` yöntemi, CAD çizimini temsil eden bir `Image` nesnesi döndürür.

```csharp
// Example: Loading CAD Drawing
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";

using (Image cadDrawing = Image.Load(SourceDir + "Drawing11.dwg"))
{
    // Code for subsequent steps will be placed here
}
```

### Adım 2: Rasterleştirme Seçeneklerini Yapılandırın

Dışa aktarılan PDF'nin orijinal çizim boyutlarıyla eşleşmesi için rasterleştirme seçeneklerini ayarlayın. Burada sayfa genişliği, yüksekliği ve diğer render ayarlarını kontrol edersiniz.

```csharp
// Example: Configuring Rasterization Options
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

### Adım 3: PDF Seçeneklerini Oluşturun (CAD PDF Dışa Aktarımı)

`PdfOptions` örneği oluşturun ve rasterleştirme ayarlarını ekleyin. Bu nesne, DWG dosyasının PDF sürümünü oluşturmak için `Save` metoduna geçirilecektir.

```csharp
// Example: Creating PDF Options
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

### Adım 4: Zaman Aşımı Mekanizmasını Uygulayın

Kaydetme işlemini kesebilecek bir token elde etmek için `InterruptionTokenSource` kullanıyoruz. Arka plan görevi dışa aktarmayı gerçekleştirirken, ana iş parçacığı istenen zaman aşımı süresi (ör. 10 saniye) kadar uyur. Uyku sonrası, işlem hâlâ çalışıyorsa iptal etmek için `Interrupt()` çağırırız.

```csharp
// Example: Implementing Timeout Mechanism
using (var its = new InterruptionTokenSource())
{
    CADf.InterruptionToken = its.Token;

    var exportTask = Task.Factory.StartNew(() =>
    {
        cadDrawing.Save(OutputDir + "PutTimeoutOnSave_out.pdf", CADf);
    });

    Thread.Sleep(10000); // Set your desired timeout duration in milliseconds
    its.Interrupt();

    exportTask.Wait();
}
```

### Adım 5: Sonlandır ve Onayla

Dışa aktarma (veya kesinti) sonrası, konsola bir onay mesajı yazın. Gerçek bir uygulamada sonucu kaydedebilir veya bir olay tetikleyebilirsiniz.

```csharp
// Example: Finalizing and Confirming
Console.WriteLine("PutTimeoutOnSave executed successfully");
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|--------|
| Dışa aktarma süresiz takılıyor | Kesinti tokenı eklenmemiş | `CADf.InterruptionToken = its.Token;` ifadesinin görev başlatılmadan önce ayarlandığından emin olun. |
| PDF boş veya bozuk | Çıktı dizini yolu hatalı | `OutputDir`'in bir yol ayırıcıyla bittiğini ve dosya adının geçerli olduğunu doğrulayın. |
| Zaman aşımı çok kısa, erken iptal oluşuyor | Büyük dosyalar için `Thread.Sleep` değeri çok düşük | Uyku süresini artırın veya dosya boyutuna göre uyarlamalı bir zaman aşımı hesaplayın. |

## Sıkça Sorulan Sorular

**S1: Zaman aşımı süresini özelleştirebilir miyim?**  
C: Kesinlikle. `Thread.Sleep`'e (milisaniye cinsinden) geçen değeri performans beklentilerinize göre değiştirin.

**S2: Rasterleştirme için başka seçenekler var mı?**  
C: Evet. `CadRasterizationOptions`, PDF çıktısını ince ayar yapmak için `Resolution`, `BackgroundColor` ve `DrawType` gibi özellikler sunar.

**S3: Uygulamamda kesintileri nasıl yönetebilirim?**  
C: Gösterildiği gibi `InterruptionToken` ve `InterruptionTokenSource` sınıflarını kullanın. Uzun süren işlemleri iptal etmenin thread‑safe bir yolunu sağlarlar.

**S4: Aspose.CAD hem 2D hem de 3D CAD dosyaları için uygun mu?**  
C: DWG, DXF, DGN ve daha fazlası dahil olmak üzere geniş bir 2D ve 3D format yelpazesini destekler.

**S5: Daha fazla yardım veya topluluk desteği nereden bulabilirim?**  
C: Topluluk tartışmaları, örnek kodlar ve sorun giderme ipuçları için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

## Sonuç

Yukarıdaki adımları izleyerek, artık CAD kaydetme işlemlerinde **zaman aşımını nasıl ayarlayacağınızı** biliyorsunuz; bu sayede yanıt vermeyen süreç riski olmadan **DWG'yi PDF'ye dönüştürmek** veya **CAD PDF dosyalarını dışa aktarmak** için güvenilir bir şekilde çalışabilirsiniz. Bu deseni toplu dönüştürücüler, web hizmetleri veya öngörülebilirliğin önemli olduğu herhangi bir otomatik boru hattına entegre edin.

---

**Son Güncelleme:** 2026-03-05  
**Test Edilen Versiyon:** Aspose.CAD 24.12 for .NET  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}