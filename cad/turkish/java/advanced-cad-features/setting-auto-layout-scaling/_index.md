---
date: 2026-02-15
description: Aspose.CAD for Java kullanarak özel sayfa boyutu ayarlamayı ve CAD'den
  PDF oluşturmayı öğrenin. Bu adım adım kılavuz, Auto Layout Scaling ile CAD'nin PDF'ye
  aktarımını kapsar.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Özel Sayfa Boyutu Ayarla – CAD'den PDF, Otomatik Düzen Ölçeklendirme ile
url: /tr/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Özel Sayfa Boyutu Ayarlama – Auto Layout Ölçeklendirme ile CAD'den PDF Oluşturma

## Giriş

Eğer **özel sayfa boyutu ayarlamak** ve **CAD'den PDF oluşturmak** istiyor, hızlı ve mükemmel ölçeklendirme ile, Aspose.CAD for Java ihtiyacınızı karşılar. Auto Layout Scaling, orijinal CAD sayfa boyutundan bağımsız olarak, ortaya çıkan PDF'nin tam olarak istenildiği gibi görünmesi için düzen boyutlarını otomatik olarak ayarlar. Bu öğreticide, bir DXF dosyasını yüklemekten PDF'ye dışa aktarmaya kadar tüm süreci adım adım inceleyecek, kütüphanenin **export CAD to PDF** yeteneklerini vurgulayacak ve gerektiğinde **convert DWG to PDF** ya da **increase PDF resolution** nasıl yapılır göstereceğiz.

## Hızlı Yanıtlar
- **Auto Layout Scaling ne yapar?** Rasterleştirme sırasında CAD düzenlerini hedef sayfa boyutlarına otomatik olarak yeniden boyutlandırır.
- **Hangi formatları dönüştürebilirim?** Aspose.CAD tarafından desteklenen herhangi bir format (ör. DXF, DWG, DWF) PDF'ye dönüştürülebilir.
- **Üretim için lisansa ihtiyacım var mı?** Evet, değerlendirme dışı kullanım için ticari bir lisans gereklidir.
- **Dönüştürme ne kadar sürer?** Modern donanımlarda standart dosyalar için genellikle bir saniyenin altında sürer.
- **Sayfa boyutunu değiştirebilir miyim?** Evet, `CadRasterizationOptions` aracılığıyla özel sayfa boyutları ayarlayabilirsiniz.

## “CAD'den PDF oluşturma” nedir?

CAD'den PDF oluşturma, vektör tabanlı bir mühendislik çizimini (DXF, DWG vb.) rasterleştirerek bir PDF belgesine dönüştürmek anlamına gelir. PDF, orijinal çizimin görsel bütünlüğünü korurken, herhangi bir platformda geniş çapta görüntülenebilir.

## Neden Auto Layout Scaling kullanmalı?

- **Tutarlı çıktı:** Tüm düzenlerin PDF sayfasını manuel boyut hesaplamalarına gerek kalmadan doldurmasını garanti eder.
- **Zaman tasarrufu:** Her çizim için ölçek faktörlerini manuel olarak ayarlama ihtiyacını ortadan kaldırır.
- **Yüksek kalite:** Dönüştürme sırasında hat kalınlığı ve geometri doğruluğunu korur.
- **Esneklik:** **convert dxf to pdf**, **convert dwg to pdf** işlemlerinin yanı sıra baskıya hazır dosyalar için **increase PDF resolution** gerektiğinde de çalışır.

## Önkoşullar

1. **Aspose.CAD for Java Library** – en son sürümü [download page](https://releases.aspose.com/cad/java/) adresinden indirin.  
2. **Kaynak Dizin** – CAD dosyalarını saklamak için makinenizde bir klasör oluşturun; kod içindeki `"Your Document Directory"` ifadesini bu yol ile değiştirin.  
3. **Örnek CAD Dosyası** – bu kılavuzda `conic_pyramid.dxf` dosyasını kullanacağız; bu dosya Aspose örnek veri setinde bulunur.

## İsim Uzaylarını İçe Aktarma

Gerekli sınıfları içe aktarın. Bu, görüntü yükleme, rasterleştirme ve PDF dışa aktarma özelliklerine erişim sağlar.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## CAD'den PDF için Özel Sayfa Boyutu Nasıl Ayarlanır

Adım‑adım koda geçmeden önce, özel sayfa boyutu ayarlamanın neden önemli olduğunu anlayalım. **Özel sayfa boyutu ayarladığınızda**, ortaya çıkan PDF'nin fiziksel boyutlarını (ör. A4, Letter veya özel bir boyut) kontrol edersiniz. Bu, çizimlerin sayfa standartlarıyla eşleşmesi gereken mühendislik iş akışları veya PDF'yi daha büyük belgeler içine yerleştirmeniz gerektiğinde kritiktir.

### Adım 1: CAD Dosyasını Yükleyin

**how to export CAD** bir PDF belgesine dönüştürmenin ilk adımı dosyayı yüklemektir.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Adım 2: Rasterleştirme Seçeneklerini Oluşturun

Hedef sayfa boyutlarını tanımlayın. İsterseniz bu blokta **set CAD page size** özelliğini manuel olarak da ayarlayabilirsiniz.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Adım 3: Auto Layout Scaling'i Ayarlayın

Otomatik ölçeklendirme özelliğini etkinleştirin. Bu, **how to set scaling** bir CAD‑to‑PDF dönüşümü için temel adımdır.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Adım 4: PDF Seçeneklerini Oluşturun

Rasterleştirme ayarlarını PDF dışa aktarma seçeneklerine bağlayın.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Adım 5: PDF Olarak Dışa Aktarın

Render edilen görüntüyü bir PDF dosyası olarak kaydedin. Bu adım **convert dxf to pdf** iş akışını tamamlar.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Yukarıdaki adımları, **DWG**, **DWF** veya diğer desteklenen formatlardaki ek CAD dosyalarınız için de tekrarlayın.

## Yaygın Kullanım Senaryoları

| Senaryo | Neden özel sayfa boyutu ayarlamalısınız? |
|----------|-----------------------------|
| **İnşaat çizimi teslimi** | PDF'yi düzenleyici kurumların talep ettiği standart A1/A2 kağıt boyutlarıyla hizalar. |
| **Teknik kılavuzlara gömme** | Çizimin, kılavuzun önceden tanımlanmış düzenine ekstra ölçekleme olmadan sığmasını sağlar. |
| **Yüksek çözünürlüklü baskı** | Sayfa boyutları tutarlı kalırken DPI'yi (ör. `rasterizationOptions.setResolution(300)`) artırmanıza olanak tanır. |

## Yaygın Sorunlar ve Çözüm Önerileri

| Semptom | Muhtemel Neden | Çözüm |
|---------|--------------|-----|
| Boş PDF çıktısı | Rasterizasyon seçenekleri ayarlanmamış veya dosya yolu hatalı | `srcFile` yolunu doğrulayın ve `setPageWidth/Height` değerlerinin sıfır olmadığından emin olun |
| Bozulmuş ölçekleme | `setAutomaticLayoutsScaling` `false` olarak bırakılmış | Otomatik ölçeklemeyi etkinleştirin veya ölçekleme faktörünü manuel olarak hesaplayın |
| Eksik katmanlar | Kaynak DXF desteklenmeyen varlıklar içeriyor | Desteklenen varlık tipleri için Aspose.CAD sürüm notlarını kontrol edin |

## Sık Sorulan Sorular

**S: Aspose.CAD for Java tüm CAD dosya formatlarıyla uyumlu mu?**  
C: Aspose.CAD for Java, DWG, DXF ve DWF dahil olmak üzere çeşitli CAD formatlarını destekler.

**S: Ölçeklendirme seçeneklerini daha da özelleştirebilir miyim?**  
C: Evet, `CadRasterizationOptions` sınıfı, ölçeklendirme, DPI ve diğer rasterleştirme ayarlarını ince ayar yapmanıza olanak tanıyan özellikler sunar.

**S: Aspose.CAD for Java için ek belgeleri nerede bulabilirim?**  
C: Derinlemesine bilgi ve örnekler için [documentation](https://reference.aspose.com/cad/java/) adresine bakın.

**S: Aspose.CAD for Java için ücretsiz deneme sürümü var mı?**  
C: Evet, Aspose.CAD for Java yeteneklerini deneyimlemek için bir [free trial](https://releases.aspose.com/) keşfedebilirsiniz.

**S: Aspose.CAD for Java hakkında destek almak ya da tartışmalara katılmak nasıl mümkün?**  
C: Toplulukla bağlantı kurmak ve destek almak için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

### Ek Yaygın Sorular

**S: DWG dosyasını DXF yerine PDF'ye nasıl dönüştürürüm?**  
C: Aynı kod çalışır; sadece `srcFile` içindeki dosya uzantısını `.dwg` olarak değiştirin.

**S: Daha yüksek çözünürlüklü PDF'ler için özel DPI ayarlayabilir miyim?**  
C: Evet, `rasterizationOptions.setResolution(300);` (veya ihtiyacınız olan herhangi bir DPI) kullanın.

**S: Oluşturulan PDF'ye font gömmek mümkün mü?**  
C: Aspose.CAD çizimi rasterleştirir, bu yüzden fontlar vektör olarak işlenir; ayrı bir font gömme gerekmeyiz.

## Sonuç

Bu kılavuzu izleyerek **özel sayfa boyutu ayarlama** ve **CAD'den PDF oluşturma** işlemlerini Aspose.CAD for Java ile Auto Layout Scaling kullanarak nasıl yapacağınızı öğrendiniz. İşlem, **export CAD to PDF** iş akışını basitleştirir, tutarlı ölçeklendirme sağlar ve geliştirme sürenizi önemli ölçüde azaltır. Farklı sayfa boyutları, çözünürlükler ve CAD formatlarıyla denemeler yapmaktan çekinmeyin; ister **DWG'yi PDF'ye dönüştürme**, ister **PDF çözünürlüğünü artırma** ya da bir **java CAD to PDF** toplu işlemci oluşturma ihtiyacınız olsun, projenize uygun ayarları bulabilirsiniz.

---

**Son Güncelleme:** 2026-02-15  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12 (latest)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}