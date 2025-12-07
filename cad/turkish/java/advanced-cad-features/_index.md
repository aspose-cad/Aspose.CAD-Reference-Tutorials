---
date: 2025-12-07
description: Aspose.CAD for Java kullanarak tuval boyutunu ayarlamayı ve diğer gelişmiş
  CAD özelliklerini öğrenin; CAD'i PDF'ye dönüştürme, blok özniteliklerini çıkarma,
  CAD arka planını ayarlama ve otomatik düzen ölçeklendirme gibi.
language: tr
linktitle: Set Canvas Size – Advanced CAD Features
second_title: Aspose.CAD Java API
title: Tuval Boyutunu Ayarla – Java için Aspose.CAD ile Gelişmiş CAD Özellikleri
url: /java/advanced-cad-features/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tuval Boyutunu Ayarlama – Aspose.CAD for Java ile Gelişmiş CAD Özellikleri

## Giriş

Java’da CAD dosyalarıyla çalışırken **set canvas size** özelliğini arıyorsanız doğru yerdesiniz. Aspose.CAD for Java, tuval boyutlarını kontrol etmenizi sağlamakla kalmaz, aynı zamanda **CAD’i PDF’ye dönüştürme**, **blok öznitelik değerlerini çıkarma**, **CAD arka plan renklerini ayarlama** ve **auto layout scaling** uygulama gibi zengin bir gelişmiş özellik seti sunar. Bu rehberde temel konuları adım adım inceleyecek, neden önemli olduklarını açıklayacak ve her özelliğe dair daha derinlemesine eğitimlere yönlendireceğiz.

## Hızlı Yanıtlar
- **“set canvas size” ne yapar?** Çıktı görüntüsü veya PDF’nin genişlik ve yüksekliğini tanımlar, böylece nihai render alanı üzerinde kesin kontrol sağlar.  
- **Tuval boyutunu ayarladıktan sonra CAD’i PDF’ye dönüştürebilir miyim?** Evet—Aspose.CAD, belirttiğiniz tuval boyutlarını koruyarak CAD dosyalarını PDF’ye dönüştürmenize olanak tanır.  
- **Blok öznitelik değerlerini çıkarmak destekleniyor mu?** Kesinlikle; API, dış referanslardan öznitelik değerlerini okuma yöntemleri sunar.  
- **CAD render’ının arka plan rengini nasıl değiştiririm?** `setBackgroundColor` seçeneğini kullanarak dışa aktarmadan önce özel bir arka plan uygulayabilirsiniz.  
- **Auto layout scaling nedir?** Çizimi tuvale otomatik olarak sığdırır, manuel hesaplamalara gerek kalmadan optimal görüntüleme sağlar.

## Aspose.CAD for Java’da “set canvas size” nedir?
Tuval boyutunu ayarlamak, render motoruna çıktı dosyası için tam piksel (veya fiziksel) boyutları bildirir. Bu, tutarlı sayfa düzenleri oluşturmanız, CAD görsellerini raporlara entegre etmeniz veya öngörülebilir boyutlarda küçük resimler üretmeniz gerektiğinde hayati öneme sahiptir.

## Aspose.CAD’ın gelişmiş özelliklerini neden kullanmalısınız?
- **Tutarlı çıktı** – Tuval boyutu ve arka plan kontrolü, birden çok dosyada aynı görünümü sağlar.  
- **Daha geniş uyumluluk** – CAD çizimlerini PDF, TIFF veya PNG’ye detay kaybı olmadan dönüştürün.  
- **Otomasyon‑hazır** – Blok özniteliklerini çıkarın ve auto layout scaling’i programatik olarak uygulayın; toplu işleme için idealdir.  
- **Harici bağımlılık yok** – Tüm özellikler doğrudan Java API’si üzerinden sunulur, üçüncü‑taraf araçlara ihtiyaç kalmaz.

## Önkoşullar
- Java Development Kit (JDK) 8 veya üzeri.  
- Aspose.CAD for Java kütüphanesi (Aspose web sitesinden en son sürümü indirin).  
- Üretim kullanımı için geçerli bir Aspose.CAD lisansı (değerlendirme için ücretsiz deneme sürümü yeterlidir).

## Gelişmiş Konuların Adım‑Adım Genel Bakışı

### Aspose.CAD for Java’da tuval boyutu nasıl ayarlanır?
`CadImage` örneği oluşturduğunuzda, kaydetmeden önce `ImageOptions` nesnesi aracılığıyla tuval genişliği ve yüksekliğini belirtebilirsiniz. Bu, dışa aktarılan dosyanın ihtiyacınız olan boyutlarla eşleşmesini sağlar.

### Tuval boyutunu koruyarak CAD’i PDF’ye nasıl dönüştürürüm?
`PdfOptions` sınıfını tuval ayarlarıyla birlikte kullanın. Dönüştürme işlemi tuval boyutlarını dikkate alır ve ekrandaki render ile aynı görünümü sağlayan bir PDF üretir.

### Dış referanslardan blok öznitelik değerlerini nasıl çıkarırım?
API, bir `BlockReference` koleksiyonu sunar. Bu koleksiyon üzerinde döngü kurarak katman adları, renkler veya DWG/DXF dosyasına gömülü özel veriler gibi öznitelik değerlerini okuyabilirsiniz.

### Daha şık bir görünüm için CAD arka plan rengini nasıl ayarlarım?
Render seçeneklerinin `BackgroundColor` özelliği sayesinde istediğiniz RGB rengi seçebilirsiniz. Bu, varsayılan beyaz arka planın marka veya UI temanızla çakıştığı durumlarda özellikle faydalıdır.

### Dinamik tuval ayarlamaları için auto layout scaling’i nasıl uygularım?
Render seçeneklerinde `AutoLayoutScaling` bayrağını etkinleştirin. Motor, çizimi tuvale otomatik olarak ölçeklendirir, en boy oranını korur ve manuel hesaplamalardan sizi kurtarır.

## Her Özellik İçin Ayrıntılı Eğitimler
Aşağıda her gelişmiş yeteneği adım adım anlatan eğitimler yer alıyor. Daha fazla bilgi edinmek için istediğiniz bağlantıya tıklayın.

### [CAD Render İşlemine İzleme Etkinleştirme](./enable-tracking-for-cad-rendering-process/)
Aspose.CAD for Java ile CAD render’ınızı geliştirin. İzlemeyi etkinleştirmek ve PDF dönüşüm deneyiminizi yükseltmek için adım‑adım kılavuzumuzu izleyin.

### [IGES Formatını Entegre Etme](./integrate-iges-format/)
Aspose.CAD for Java ile IGES formatını sorunsuz bir şekilde entegre edin. CAD geliştirme deneyiminizi yükseltmek için adım‑adım rehberimizi takip edin.

### [Java’da Mesh Desteği](./mesh-support-in-cad/)
Java uygulamalarında mesh desteğini keşfedin. Aspose.CAD ile CAD dosyalarını PDF’ye zahmetsizce dönüştürün.

### [Dışa Aktarmada Kalem Desteği](./pen-support-in-export/)
Aspose.CAD for Java ile CAD dışa aktarımında kalem özelleştirmesini ustalıkla yönetin. Sorunsuz entegrasyon için adım‑adım kılavuzumuzu izleyin.

### [DWT Dosyalarını Okuma](./reading-dwt-files/)
Aspose.CAD ile Java’da DWT dosyalarını okumayı öğrenin. Sorunsuz entegrasyon için adım‑adım rehberimizi takip edin.

### [Arka Plan ve Çizim Rengini Ayarlama](./setting-background-and-drawing-color/)
Aspose.CAD for Java kullanarak CAD dosyalarını PDF ve TIFF’e zahmetsizce dönüştürün. Görsel açıdan çarpıcı sonuçlar için özel arka plan ve çizim renkleri ayarlayın.

### [Tuval Boyutu ve Modunu Ayarlama](./set-canvas-size-and-mode/)
Aspose.CAD for Java’nın gücünü **tuval boyutu** ve modunu ayarlama üzerine adım‑adım rehberimizle keşfedin. CAD dosyalarını PDF ve TIFF formatlarına zahmetsizce dönüştürün.

### [Auto Layout Scaling’i Ayarlama](./setting-auto-layout-scaling/)
Aspose.CAD for Java ile CAD iş akışınızı geliştirin. Bu adım‑adım kılavuz, Auto Layout Scaling’i tanıtarak optimal görüntüleme ve verimlilik sağlar. Kütüphaneyi indirin, eğitimi izleyin ve CAD projelerinizi dönüştürün.

### [Java’da Katman Desteği](./support-of-layers-in-cad/)
Aspose.CAD ile Java CAD geliştirmede katman desteğini ustalıkla yönetin. Çizimleri düzenli bir şekilde organize edin ve dışa aktarın.

### [Dış Referanstan Blok Öznitelik Değeri Çıkarma](./extract-block-attribute-value/)
Aspose.CAD kullanarak Java’da DWG dış referanslarından blok öznitelik değerlerini çıkarmayı keşfedin. CAD geliştirme iş akışınızı zahmetsizce geliştirin.

## Yaygın Sorunlar ve Sorun Giderme
- **Tuval boyutu uygulanmadı:** `save()` çağrısından önce doğru `ImageOptions` nesnesine boyutu ayarladığınızdan emin olun.  
- **Arka plan rengi değişmedi:** Render modunun arka plan renklerini desteklediğini (ör. PNG, TIFF) doğrulayın.  
- **Blok öznitelikleri null döndürüyor:** DWG dosyasının gerçekten öznitelik tanımları içerdiğini ve doğru blok referansına eriştiğinizi kontrol edin.  
- **Auto layout scaling bozulmuş görünüyor:** En‑boy oranı bayrağının etkin olduğundan emin olun; aksi takdirde motor çizimi gerip uzatabilir.

## Sıkça Sorulan Sorular

**S: Toplu işleme sırasında her dosya için özel bir tuval boyutu ayarlayabilir miyim?**  
C: Evet. CAD dosyalarınızın koleksiyonunu döngüye alıp, her `ImageOptions` örneğinde tuval boyutunu yapılandırarak çıktıyı programatik olarak kaydedebilirsiniz.

**S: Tuval boyutunu ayarlamak dışa aktarılan PDF’nin kalitesini etkiler mi?**  
C: Kalite, render seçeneklerindeki DPI ayarıyla belirlenir. Tuval boyutlarını korurken DPI’yı artırarak daha yüksek çözünürlüklü PDF’ler elde edebilirsiniz.

**S: Dış referans içeren bir DWG’den blok öznitelik değerlerini nasıl çıkarırım?**  
C: `ExternalReference` koleksiyonunu kullanarak referansı çözün, ardından `BlockReference` nesneleri üzerinde döngü kurarak öznitelik değerlerini okuyun.

**S: Auto layout scaling vektör çıktı formatları (PDF gibi) ile uyumlu mu?**  
C: Evet. Ölçekleme mantığı raster (PNG, TIFF) ve vektör (PDF, SVG) çıktılarının her ikisi için de çalışır, çizimin tuvale sığmasını sağlar.

**S: Ticari kullanım için hangi lisans gereklidir?**  
C: Üretim ortamları için ücretli bir Aspose.CAD lisansı gereklidir. Geliştirme ve test amaçlı ücretsiz bir değerlendirme lisansı kullanılabilir.

---

**Son Güncelleme:** 2025-12-07  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.12 (latest)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}