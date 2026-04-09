---
date: 2026-04-09
description: C# ve Aspose.CAD for .NET kullanarak DWG katmanlarını dışa aktarmayı,
  DWG görüntüsünü dönüştürmeyi ve DWG JPEG olarak kaydetmeyi öğrenin. Verimli CAD
  dosyası manipülasyonu için adım adım kılavuz.
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: C# ile DWG Dosyalarında Katmanları Yönetme
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: C# ile DWG Katmanlarını Dışa Aktarma – Aspose.CAD Öğreticisi
url: /tr/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# ile DWG Katmanlarını Dışa Aktarma – Aspose.CAD Öğreticisi

## Giriş

Bu kapsamlı rehberde C# ve Aspose.CAD kütüphanesini kullanarak **DWG katmanlarını nasıl dışa aktaracağınızı** öğreneceksiniz. **DWG görüntü** formatlarını dönüştürmeniz, **DWG katman görünürlüğünü** kontrol etmeniz ya da sadece **DWG JPEG** dosyalarını kaydetmeniz gerekirse, aşağıdaki adımlar bunu verimli bir şekilde nasıl yapacağınızı tam olarak gösterecek. Rehberin sonunda, belirli bir katmanı izole eden ve yüksek kaliteli bir JPEG olarak render eden, çalıştırmaya hazır bir kod parçacığına sahip olacaksınız.

## Hızlı Yanıtlar
- **“export dwg layers” ne anlama geliyor?** Bir DWG dosyasının seçili katmanlarını JPEG veya PNG gibi bir görüntü formatına rasterleştirmek anlamına gelir.  
- **Bu görev için en iyi kütüphane hangisidir?** Aspose.CAD for .NET, AutoCAD gerektirmeden tam özellikli destek sağlar.  
- **Birden fazla katmanı aynı anda dışa aktarabilir miyim?** Evet – rasterleştirme seçeneklerine bir katman adı dizisi geçirin.  
- **Üretim kullanımında lisansa ihtiyacım var mı?** Ticari bir lisans gereklidir; değerlendirme için ücretsiz bir deneme sürümü mevcuttur.  
- **Hangi çıktı formatları destekleniyor?** JPEG, PNG, BMP, TIFF ve ImageOptions sınıfları aracılığıyla birkaç diğer format.

## Export dwg layers nedir?
DWG katmanlarını dışa aktarmak, bir DWG çizimindeki bir veya daha fazla katmana ait vektör verilerini alıp bir bitmap görüntüsüne rasterleştirmek anlamına gelir. Bu, tüm CAD dosyasını ortaya çıkarmadan bir çizimin belirli bir bölümünün görünümünü paylaşmak istediğinizde faydalıdır.

## Neden DWG katman görünürlüğünü kontrol etmeliyiz?
Katman görünürlüğünü kontrol etmek şunları sağlar:

- Sunumlar veya dokümantasyon için temiz görsel varlıklar oluşturma.  
- Yalnızca gereken geometrileri dışa aktararak dosya boyutunu azaltma.  
- Gizli katmanları gizleyerek tescilli tasarım detaylarını koruma.  

## Önkoşullar

Başlamadan önce şunların kurulu olduğundan emin olun:

- C# programlama diline temel bilgi.  
- Makinenizde Visual Studio yüklü olması.  
- Aspose.CAD for .NET kütüphanesi, bunu [Aspose.CAD web sitesinden](https://releases.aspose.com/cad/net/) indirebilirsiniz.

## Ad Alanlarını İçe Aktarma

Başlamak için rasterleştirme ve görüntü‑dışa aktarma özelliklerine erişmenizi sağlayan ad alanlarını içe aktarın.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Adım 1: DWG Dosyasını Yükle

Kaynak DWG (veya DWF) dosyasını bir `Image` nesnesine yükleyin. Bu nesne, çizimin tamamını bellekte temsil eder.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*Neden önemli:* Dosyayı bir kez yüklemek, aynı `image` örneğini katmana özgü birden fazla dışa aktarma için yeniden kullanmanıza olanak tanır, performansı artırır.

## Adım 2: Rasterleştirme Seçeneklerini Yapılandırma

Aspose.CAD'in çizimi nasıl render edeceğini belirlemek için bir `CadRasterizationOptions` örneği oluşturun. Burada, dışa aktarılan JPEG'in keskin olmasını sağlamak için yüksek bir çözünürlük (1600 × 1600) ayarlıyoruz.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

İhtiyaç duyulursa arka plan rengini, hat kalınlığı ölçeklendirmesini veya anti‑aliasing ayarlarını da değiştirebilirsiniz.

## Adım 3: Katmanları Belirtin (DWG Katman Görünürlüğü)

**export dwg layers** için dışa aktarmak istediğiniz katmanları ekleyin. Bu örnekte yalnızca “LayerA” dışa aktarılıyor. Birden fazla katman dışa aktarmak için, onları dizi içinde listeleyin.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*Pro tip:* Çizimde göründüğü gibi tam katman adını kullanın; katman adları büyük/küçük harfe duyarlıdır.

## Adım 4: Görüntü Dışa Aktarma Seçeneklerini Yapılandırma

Oluşturmak istediğiniz görüntü formatını seçin. JPEG, kalite ve dosya boyutu dengesi sağladığı için **save dwg jpeg** dosyaları için idealdir.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

DWG görüntüsünü PNG veya TIFF'e dönüştürmek isterseniz, `JpegOptions` yerine ilgili seçenek sınıfını kullanın.

## Adım 5: Dışa Aktarılan Görüntüyü Kaydet

Çıktı dosya yolunu tanımlayın ve `Save` metodunu çağırın. Rasterleştirme motoru sağladığınız katman listesini dikkate alır, böylece yalnızca “LayerA” son JPEG'te görünür.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

Bu satır çalıştırıldıktan sonra, `for_layers_test.jpg` dosyasını belge dizininizde bulacaksınız; yalnızca seçilen katmanı içerir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|------------|
| **Katman adı bulunamadı** | Orijinal DWG'deki katmanın tam yazımını ve büyük/küçük harf duyarlılığını doğrulayın. Katman adlarını listelemek için bir CAD görüntüleyici kullanın. |
| **Boş çıktı görüntüsü** | Rasterleştirme seçeneklerinin şeffaf olmayan bir arka plana sahip olduğundan ve seçilen katmanların gerçekten geometri içerdiğinden emin olun. |
| **Düşük çözünürlüklü çıktı** | `PageWidth` ve `PageHeight` değerlerini artırın veya `CadRasterizationOptions` içinde `Resolution` ayarlayın. |
| **Desteklenmeyen DWG sürümü** | En son Aspose.CAD sürümüne güncelleyin; bu, daha yeni AutoCAD sürümlerini destekler. |

## Sık Sorulan Sorular

### Q1: Birden fazla katmanı aynı anda işleyebilir miyim?
A1: Evet, yapabilirsiniz. Katman adlarını `rasterizationOptions.Layers` dizisine ekleyin.

### Q2: Aspose.CAD'in deneme sürümü mevcut mu?
A2: Evet, ücretsiz bir deneme sürümünü [buradan](https://releases.aspose.com/) edinebilirsiniz.

### Q3: Belgeleri nerede bulabilirim?
A3: Belgeler [burada](https://reference.aspose.com/cad/net/) mevcuttur.

### Q4: Aspose.CAD için desteği nasıl alabilirim?
A4: Destek için [Aspose.CAD forumuna](https://forum.aspose.com/c/cad/19) başvurabilirsiniz.

### Q5: Aspose.CAD için lisans seçenekleri nelerdir?
A5: Lisans seçeneklerini ve satın alma detaylarını [burada](https://purchase.aspose.com/buy) inceleyebilirsiniz.

**Ekstra Soru & Cevap**

**S: Çizimi JPEG yerine PNG olarak dışa aktarabilir miyim?**  
C: Kesinlikle. `JpegOptions` yerine `PngOptions` kullanın ve dosya uzantısını buna göre ayarlayın.

**S: Kütüphane hat stilini ve renkleri korur mu?**  
C: Evet. Tüm vektör özellikleri rasterleştirme sırasında eksiksiz bir şekilde render edilir.

**Son Güncelleme:** 2026-04-09  
**Test Edilen:** Aspose.CAD for .NET (latest release)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}