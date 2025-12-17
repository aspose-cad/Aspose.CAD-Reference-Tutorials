---
date: 2025-12-10
description: Aspose.CAD for Java kullanarak kalem özelleştirmesiyle CAD'den PDF oluşturmayı
  öğrenin. Bu adım adım rehber, CAD'i PDF'ye verimli bir şekilde dışa aktarmayı gösterir.
linktitle: Pen Support in Export
second_title: Aspose.CAD Java API
title: CAD'den Dışa Aktarmada Kalem Desteğiyle PDF Nasıl Oluşturulur
url: /tr/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dışa Aktarmada Kalem Desteği

## Giriş

CAD dönüşümlerinin hızlı hareket ettiği dünyada, geliştiriciler genellikle görsel sadakati koruyarak **CAD'den PDF oluşturma** ihtiyacı duyar. Aspose.CAD for Java bu süreci basitleştirir ve dışa aktarma sırasında çizgi stillerini ince ayarlamanıza olanak tanıyan kalem özelleştirme gibi zengin seçenekler sunar. Bu rehberde, **CAD'den PDF'ye dışa aktarma** işlemini özel kalem ayarlarıyla nasıl yapacağınızı gösteren eksiksiz, uygulamalı bir örnek üzerinden ilerleyeceğiz; böylece DXF çizimlerinden doğrudan cilalı PDF'ler üretebileceksiniz.

## Hızlı Yanıtlar
- **“create PDF from CAD” ne anlama geliyor?** Bir CAD çizimini (ör. DXF) vektör kalitesini koruyarak PDF belgesine dönüştürmek.  
- **Kalem özelleştirmesini hangi kütüphane yönetiyor?** Aspose.CAD for Java’nın `PenOptions` sınıfı.  
- **Bunu diğer formatlar için de kullanabilir miyim?** Evet – aynı kalem ayarları PNG, BMP, TIFF vb. formatlarda da geçerlidir.  
- **Lisans gerekli mi?** Üretim kullanımında geçerli bir Aspose.CAD lisansı gereklidir.  
- **Minimum Java sürümü nedir?** Java 8 veya üzeri.

## “create PDF from CAD” nedir?
CAD'den PDF oluşturmak, bir CAD çizimini PDF dosyasına rasterleştirerek veya vektör olarak render ederek dönüştürmek anlamına gelir. Bu, mühendislik tasarımlarının alıcı tarafında CAD yazılımı olmadan kolayca paylaşılmasını, yazdırılmasını ve arşivlenmesini sağlar.

## CAD'ı PDF olarak dışa aktarırken neden kalem desteği kullanmalı?
Kalem desteği, çizgi uçlarını, birleşimlerini ve kalınlığını kontrol etmenizi sağlar; böylece kurumsal kimliğe veya teknik çizim standartlarına uygunluk elde edersiniz. Varsayılan çizgi render'ı görsel gereksinimlerinizi karşılamadığında özellikle faydalıdır.

## Önkoşullar

- **Java Geliştirme Ortamı** – çalışan bir JDK (8 veya daha yeni) ve tercih ettiğiniz bir IDE veya derleme aracı.  
- **Aspose.CAD Kütüphanesi** – resmi siteden en yeni JAR'ı [burada](https://releases.aspose.com/cad/java/) indirin.  
- **Örnek bir DXF dosyası** – bu öğreticide `conic_pyramid.dxf` dosyasını kullanacağız.

Şimdi ortamı hazırladığımıza göre, koda dalalım.

## Ad Alanlarını İçe Aktar

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## Adım 1: Belge Dizinini Tanımlayın

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

> **Pro tip:** `"Your Document Directory"` ifadesini DXF dosyalarınızın bulunduğu mutlak yol ile değiştirin.

## Adım 2: CAD Dosyasını Yükleyin

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

`Image.load` yöntemi DXF dosyasını okur ve üzerinde işlem yapabileceğimiz bir `CadImage` nesnesi oluşturur.

## Adım 3: Rasterleştirme Seçeneklerini Yapılandırın

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

Sayfa boyutlarını ayarlayarak ortaya çıkan PDF'in çözünürlüğünü kontrol edebilirsiniz. 100 ile çarpmak, baskı için uygun yüksek çözünürlüklü bir çıktı verir.

## Adım 4: Kalem Seçeneklerini Özelleştirin

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

Burada kalemin başlangıç ve bitiş uçlarını `Flat` olarak ayarlıyoruz. Farklı görsel etkiler elde etmek için diğer `LineCap` değerlerini (ör. `Round`, `Square`) deneyebilirsiniz.

## Adım 5: PDF Dışa Aktarma Seçeneklerini Yapılandırın

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

`PdfOptions` nesnesi rasterleştirme ayarlarını PDF dışa aktarma sürecine bağlar.

## Adım 6: Dışa Aktarılan PDF'yi Kaydedin

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Bu satırı çalıştırmak, tanımladığınız özel kalem stilini içeren `9LHATT-A56_generated.pdf` adlı PDF dosyasını `dataDir` klasörünüze yazar.

## Yaygın Kullanım Senaryoları

- **Teknik dokümantasyon** – PDF kılavuzlarda hassas mühendislik çizimlerini gömün.  
- **Otomatik raporlama** – web hizmetlerinde CAD verilerinden anlık PDF'ler üretin.  
- **Kalite kontrol** – ölçüm hatlarını veya toleransları vurgulamak için özel çizgi uçları uygulayın.

## Sorun Giderme ve İpuçları

- **Yanlış dosya yolu** – `dataDir`'in bir dosya ayırıcı (`/` veya `\\`) ile bittiğinden emin olun.  
- **Lisans eksik** – geçerli bir lisans olmadan kütüphane değerlendirme modunda çalışır ve filigran ekleyebilir.  
- **Beklenmeyen çizgi stilleri** – `save` çağrısından önce `PenOptions`'ın ayarlandığını kontrol edin; aksi takdirde varsayılan kalemler kullanılır.

## Sıkça Sorulan Sorular

### S1: Kalem seçeneklerini PDF dışındaki formatlar için de özelleştirebilir miyim?

C1: Evet, bu öğreticide gösterilen kalem özelleştirmesi PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF ve WMF dahil olmak üzere çeşitli görüntü formatlarında uygulanabilir.

### S2: Kalemler için farklı başlangıç ve bitiş uçlarını nasıl ayarlayabilirim?

C2: `PenOptions` sınıfını kullanarak istediğiniz başlangıç ve bitiş uçlarını belirleyebilir, çizgilerin görünümünü esnek bir şekilde tanımlayabilirsiniz.

### S3: PenOptions ayarlamazsam ne olur?

C3: PenOptions açıkça ayarlanmazsa sistem varsayılan kalemleri kullanır; bu kalemler farklı bağlamlarda değişiklik gösterebilir.

### S4: Rasterleştirme seçenekleriyle ilgili özel bir dikkat edilmesi gereken nokta var mı?

C4: Rasterleştirme seçeneklerinde sayfa genişliği ve yüksekliğini ayarlayarak dışa aktarılan görüntünün boyutlarını kontrol edebilirsiniz.

### S5: Ek destek veya topluluk tartışmalarını nereden bulabilirim?

C5: Destek ve tartışmalar için Aspose.CAD topluluk forumuna [burada](https://forum.aspose.com/c/cad/19) göz atabilirsiniz.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}