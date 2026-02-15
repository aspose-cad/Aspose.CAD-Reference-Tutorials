---
date: 2026-02-15
description: Aspose.CAD for Java kullanarak kalem özelleştirmesiyle CAD'den PDF oluşturmayı
  öğrenin. Bu adım adım rehber, CAD'i PDF'ye verimli bir şekilde dışa aktarmayı gösterir.
linktitle: Pen Support in Export
second_title: Aspose.CAD Java API
title: Dışa Aktarmada Kalem Desteğiyle CAD'den PDF Nasıl Oluşturulur
url: /tr/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Pen Desteği ile Dışa Aktarım

## Giriş

CAD dönüşümlerinin hızlı hareket ettiği dünyada, geliştiriciler genellikle görsel bütünlüğü koruyarak **create PDF from CAD** dosyaları oluşturmak zorundadır. Aspose.CAD for Java bu süreci basitleştirir ve dışa aktarım sırasında satır stillerini ince ayar yapmanıza olanak tanıyan kalem özelleştirme gibi zengin seçenekler sunar. Bu kılavuzda, **export CAD to PDF** işlemini özel kalem ayarlarıyla nasıl gerçekleştireceğinizi gösteren eksiksiz, uygulamalı bir örnek üzerinden adım adım ilerleyeceğiz; böylece DXF çizimlerinden doğrudan cilalı PDF'ler üretebileceksiniz.

## Hızlı Yanıtlar
- **“create PDF from CAD” ne anlama geliyor?** Bir CAD çizimini (ör. DXF) vektör kalitesini koruyarak PDF belgesine dönüştürmek.  
- **Kalem özelleştirmesini hangi kütüphane yönetiyor?** Aspose.CAD for Java’nın `PenOptions` sınıfı.  
- **Bunu başka formatlar için de kullanabilir miyim?** Evet – aynı kalem ayarları PNG, BMP, TIFF vb. formatlarda da geçerlidir.  
- **Bir lisansa ihtiyacım var mı?** Üretim ortamında kullanmak için geçerli bir Aspose.CAD lisansı gereklidir.  
- **Minimum Java sürümü nedir?** Java 8 veya üzeri.

## “create PDF from CAD” nedir?
CAD'den PDF oluşturmak, bir CAD çizimini PDF dosyasına rasterleştirerek veya vektör olarak renderlayarak dönüştürmek anlamına gelir. Bu sayede mühendislik tasarımları, alıcı tarafın CAD yazılımına sahip olmasına gerek kalmadan kolayca paylaşılabilir, yazdırılabilir ve arşivlenebilir.

## CAD'i PDF olarak dışa aktarırken neden kalem desteği kullanmalı?
Kalem desteği, satır uçları, birleşim tipleri ve kalınlık gibi özellikleri kontrol etmenizi sağlar; böylece kurumsal kimliğe veya teknik çizim standartlarına uygun görünümler elde edebilirsiniz. Varsayılan satır renderı görsel gereksinimlerinizi karşılamadığında bu özellik özellikle faydalıdır.

## CAD'den PDF oluşturma – Adım adım kılavuz
Aşağıda, ortamınızı kurmaktan son PDF'yi üretmeye kadar her şeyi kapsayan pratik bir yürütme rehberi bulacaksınız. Her adımı izleyin; **export CAD to PDF** işlemini tam kalem kontrolüyle kullanıma hazır bir çözüm elde edeceksiniz.

## Önkoşullar

- **Java Geliştirme Ortamı** – çalışan bir JDK (8 veya daha yeni) ve tercih ettiğiniz bir IDE ya da derleme aracı.  
- **Aspose.CAD Kütüphanesi** – resmi siteden en yeni JAR dosyasını [buradan](https://releases.aspose.com/cad/java/) indirin.  
- **Örnek bir DXF dosyası** – bu öğreticide `conic_pyramid.dxf` dosyasını kullanacağız.

Şimdi sahneyi kurduk, koda dalalım.

## İçe Aktarma Ad Alanları

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## Adım 1: Belge Dizininizi Tanımlayın

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

Sayfa boyutlarını ayarlayarak ortaya çıkan PDF'nin çözünürlüğünü kontrol edebilirsiniz. 100 ile çarpmak, baskı için uygun yüksek çözünürlüklü bir çıktı verir.

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

`PdfOptions` nesnesi rasterleştirme ayarlarını PDF dışa aktarım süreciyle birleştirir.

## Adım 6: Dışa Aktarılan PDF'yi Kaydedin

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Bu satırı çalıştırdığınızda, tanımladığınız `dataDir` klasörüne `9LHATT-A56_generated.pdf` adlı bir PDF dosyası yazılır; içinde tanımladığınız özel kalem stilleri bulunur.

## Yaygın Kullanım Senaryoları

- **Teknik dokümantasyon** – PDF kılavuzlarda hassas mühendislik çizimlerini gömün.  
- **Otomatik raporlama** – web servislerinde CAD verilerinden anlık PDF'ler üretin.  
- **Kalite kontrol** – ölçüm hatlarını veya toleransları vurgulamak için özel satır uçları uygulayın.

## Sorun Giderme ve İpuçları

- **Yanlış dosya yolu** – `dataDir`'in bir dosya ayırıcı (`/` veya `\\`) ile bittiğinden emin olun.  
- **Lisans eksik** – geçerli bir lisans olmadan kütüphane değerlendirme modunda çalışır ve filigran ekleyebilir.  
- **Beklenmeyen satır stilleri** – `save` çağrısından önce `PenOptions`'ın ayarlandığını kontrol edin; aksi takdirde varsayılan kalemler kullanılır.

## Sık Sorulan Sorular

### Q1: PDF dışındaki formatlar için kalem seçeneklerini özelleştirebilir miyim?

A1: Evet, bu öğreticide gösterilen kalem özelleştirmesi PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF ve WMF gibi çeşitli görüntü formatları için geçerlidir.

### Q2: Kalemlerin farklı başlangıç ve bitiş uçlarını nasıl yönetebilirim?

A2: İstediğiniz başlangıç ve bitiş uçlarını ayarlamak için `PenOptions` sınıfını kullanın; bu, çizgilerin görünümünü tanımlamada esneklik sağlar.

### Q3: Kalem seçeneklerini belirtmezsem ne olur?

A3: Kalem seçenekleri açıkça ayarlanmazsa sistem, bağlamına göre değişebilen varsayılan kalemleri kullanır.

### Q4: Rasterleştirme seçenekleriyle ilgili özel bir dikkat edilmesi gereken nokta var mı?

A4: Dışa aktarılan görüntünün boyutlarını kontrol etmek için rasterleştirme seçeneklerinde sayfa genişliği ve yüksekliğini ayarlayın.

### Q5: Ek destek veya topluluk tartışmalarını nerede bulabilirim?

A5: Destek ve tartışmalar için Aspose.CAD topluluk forumunu [burada](https://forum.aspose.com/c/cad/19) inceleyin.

---

**Son Güncelleme:** 2026-02-15  
**Test Edilen Sürüm:** Aspose.CAD 24.11 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}