---
date: 2025-12-10
description: CAD'den PDF oluşturmayı Aspose.CAD for Java ile Otomatik Yerleşim Ölçeklendirme
  kullanarak öğrenin. Bu adım adım kılavuz, CAD'yi PDF'ye verimli ve güvenilir bir
  şekilde dışa aktarmayı gösterir.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: CAD'den PDF Oluştur – Aspose.CAD Java ile Otomatik Düzen Ölçeklendirme
url: /tr/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD'den PDF Oluşturma – Aspose.CAD Java ile Otomatik Düzen Ölçeklendirme

## Giriş

CAD dosyalarından **PDF oluşturmak** istiyorsanız ve bunu hızlı bir şekilde mükemmel ölçeklendirme ile yapmak istiyorsanız, Aspose.CAD for Java ihtiyacınızı karşılar. Otomatik Düzen Ölçeklendirme, orijinal CAD sayfa boyutundan bağımsız olarak, ortaya çıkan PDF'nin tam olarak istediğiniz gibi görünmesi için düzen boyutlarını otomatik olarak ayarlar. Bu öğreticide, bir DXF dosyasını yüklemekten PDF'ye dışa aktarmaya kadar tam süreci adım adım gösterecek ve kütüphanenin **CAD'den PDF'ye dışa aktarma** yeteneklerini vurgulayacağız.

## Hızlı Yanıtlar
- **Auto Layout Scaling ne yapar?** Rasterleştirirken CAD düzenlerini hedef sayfa boyutlarına otomatik olarak yeniden boyutlandırır.
- **Hangi formatları dönüştürebilirim?** Aspose.CAD tarafından desteklenen herhangi bir format (ör. DXF, DWG, DWF) PDF'ye dönüştürülebilir.
- **Üretim için lisansa ihtiyacım var mı?** Evet, değerlendirme dışı kullanım için ticari bir lisans gereklidir.
- **Dönüştürme ne kadar sürer?** Modern donanımda standart dosyalar için genellikle bir saniyenin altında sürer.
- **Sayfa boyutunu değiştirebilir miyim?** Evet, `CadRasterizationOptions` aracılığıyla özel sayfa boyutları ayarlayabilirsiniz.

## “CAD'den PDF oluşturma” nedir?
CAD'den PDF oluşturmak, vektör tabanlı bir mühendislik çizimini (DXF, DWG vb.) alıp bir PDF belgesine rasterleştirmek anlamına gelir. PDF, orijinal çizimin görsel bütünlüğünü korur ve herhangi bir platformda geniş çapta görüntülenebilir.

## Neden Otomatik Düzen Ölçeklendirme Kullanmalı?
- **Tutarlı çıktı:** Tüm düzenlerin PDF sayfasını manuel boyut hesaplaması yapmadan doldurulmasını garanti eder.
- **Zaman tasarrufu:** Her çizim için ölçek faktörlerini manuel olarak ayarlama ihtiyacını ortadan kaldırır.
- **Yüksek kalite:** Dönüştürme sırasında hat kalınlığı ve geometri doğruluğunu korur.

## Ön Koşullar

1. **Aspose.CAD for Java Kütüphanesi** – en son sürümü [download page](https://releases.aspose.com/cad/java/) adresinden indirin.  
2. **Kaynak Dizini** – CAD dosyalarını saklamak için makinenizde bir klasör oluşturun; kodda `"Your Document Directory"` ifadesini bu yol ile değiştirin.  
3. **Örnek CAD Dosyası** – bu kılavuz için Aspose örnek veri setinde bulunan `conic_pyramid.dxf` dosyasını kullanacağız.

## Ad Alanlarını İçe Aktarma

İlk olarak, gerekli sınıfları içe aktarın. Bu, görüntü yükleme, rasterleştirme ve PDF dışa aktarma özelliklerine erişmemizi sağlar.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Adım 1: CAD Dosyasını Yükleyin

Kaynak dosyayı yüklemek, **CAD'i PDF belgesine nasıl dışa aktarılır** sürecinin ilk adımıdır.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Adım 2: Rasterleştirme Seçeneklerini Oluşturun

Hedef sayfa boyutlarını tanımlayın. Özel bir düzen tercih ediyorsanız, bu bloğu **CAD sayfa boyutunu** manuel olarak ayarlamak için de kullanabilirsiniz.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## Adım 3: Otomatik Düzen Ölçeklendirmeyi Ayarlayın

Otomatik ölçeklendirme özelliğini etkinleştirin. Bu, CAD‑to‑PDF dönüşümü için **ölçek ayarlamanın** temelidir.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## Adım 4: PDF Seçeneklerini Oluşturun

Rasterleştirme ayarlarını PDF dışa aktarma seçeneklerine bağlayın.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Adım 5: PDF Olarak Dışa Aktarın

Son olarak, işlenmiş görüntüyü bir PDF dosyası olarak kaydedin. Bu adım **DXF'i PDF'ye dönüştür** iş akışını tamamlar.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Yukarıdaki adımları, işlemeniz gereken ek CAD dosyaları için tekrarlayın.

## Yaygın Sorunlar ve Çözüm Yolları

| Belirti | Muhtemel Neden | Çözüm |
|---------|----------------|-------|
| Boş PDF çıktısı | Rasterleştirme seçenekleri ayarlanmamış veya dosya yolu hatalı | `srcFile` yolunu doğrulayın ve `setPageWidth/Height` değerlerinin sıfır olmadığından emin olun |
| Bozulmuş ölçekleme | `setAutomaticLayoutsScaling` `false` olarak bırakılmış | Otomatik ölçeklendirmeyi etkinleştirin veya ölçek faktörünü manuel olarak hesaplayın |
| Eksik katmanlar | Kaynak DXF desteklenmeyen varlıklar içeriyor | Desteklenen varlık tipleri için Aspose.CAD sürüm notlarını kontrol edin |

## SSS

### Q1: Aspose.CAD for Java tüm CAD dosya formatlarıyla uyumlu mu?
A1: Aspose.CAD for Java, DWG, DXF ve DWF dahil olmak üzere çeşitli CAD formatlarını destekler.

### Q2: Ölçeklendirme seçeneklerini daha da özelleştirebilir miyim?
A2: Evet, `CadRasterizationOptions` sınıfı, ölçeklendirme ve diğer ayarları ince ayar yapmak için çeşitli özellikler sunar.

### Q3: Aspose.CAD for Java için ek belgeleri nerede bulabilirim?
A3: Derinlemesine bilgi ve örnekler için [documentation](https://reference.aspose.com/cad/java/) adresine bakın.

### Q4: Aspose.CAD for Java için ücretsiz deneme sürümü mevcut mu?
A4: Evet, Aspose.CAD for Java'ın yeteneklerini deneyimlemek için bir [free trial](https://releases.aspose.com/) keşfedebilirsiniz.

### Q5: Aspose.CAD for Java hakkında yardım almak veya tartışmalara katılmak nasıl mümkün?
A5: Toplulukla iletişime geçmek ve destek almak için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

**Additional Common Questions**

**S: DWG dosyasını DXF yerine PDF'ye nasıl dönüştürürüm?**  
C: Aynı kod çalışır; sadece `srcFile` içindeki dosya uzantısını `.dwg` olarak değiştirin.

**S: Daha yüksek çözünürlüklü PDF'ler için özel DPI ayarlayabilir miyim?**  
C: Evet, `rasterizationOptions.setResolution(300);` (veya ihtiyacınız olan herhangi bir DPI) kullanın.

**S: Oluşturulan PDF'ye fontları gömmek mümkün mü?**  
C: Aspose.CAD çizimi rasterleştirir, bu yüzden fontlar vektör olarak işlenir; ayrı bir font gömme gerekmez.

## Sonuç

Bu kılavuzu izleyerek, Aspose.CAD for Java ile Otomatik Düzen Ölçeklendirme kullanarak **CAD dosyalarından PDF oluşturma** yöntemini artık biliyorsunuz. İşlem, **CAD'i PDF'ye dışa aktarma** iş akışını basitleştirir, tutarlı ölçeklemeyi sağlar ve değerli geliştirme zamanınızı tasarruf ettirir. Proje ihtiyaçlarınıza uygun farklı sayfa boyutları, çözünürlükler ve CAD formatlarıyla denemeler yapmaktan çekinmeyin.

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}