---
date: 2025-12-28
description: Aspose.CAD for Java kullanarak DWG dosyasını Java projelerine nasıl yükleyeceğinizi
  ve birincil yazı tipi adını nasıl ayarlayacağınızı öğrenin. Mükemmel CAD görselleri
  için adım adım rehber.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Java'da DWG dosyasını nasıl yükler ve fontu Aspose.CAD ile nasıl değiştiririz?
url: /tr/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java'da DWG dosyasını yükleme ve Aspose.CAD ile yazı tipini değiştirme

## Giriş

**DWG dosyasını Java** uygulamalarına yüklemeniz ve çizimlerinize profesyonel bir görünüm kazandırmanız gerekiyorsa, yazı tipini değiştirmek hızlı bir çözümdür. Aspose.CAD for Java ile varsayılan metin stilini sistemde yüklü herhangi bir yazı tipiyle değiştirebilir, böylece her açıklamanın tam olarak beklediğiniz gibi görünmesini sağlayabilirsiniz. Bu öğreticide, Java'da bir DWG dosyasını yüklemekten `setPrimaryFontName` metodunu kullanarak yazı tipini değiştirmeye kadar tüm süreci adım adım inceleyeceğiz.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.CAD for Java.  
- **Java'da DWG dosyası yükleyebilir miyim?** Evet, DWG yolunda `Image.load()` metodunu çağırmanız yeterlidir.  
- **Yazı tipini değiştiren metod hangisi?** `setPrimaryFontName`.  
- **Üretim ortamı için lisansa ihtiyacım var mı?** Evet, ticari bir lisans gereklidir.  
- **Toplu işlem mümkün mü?** Kesinlikle – aynı kodla birden fazla dosya üzerinde döngü kurabilirsiniz.

## “load dwg file java” nedir?

Java ortamında bir DWG dosyasını yüklemek, ikili CAD verilerini Aspose.CAD'in işleyebileceği bir `Image` nesnesine okumak anlamına gelir. Dosya yüklendikten sonra katmanlara, stillere ve metin varlıklarına tam programatik erişiminiz olur.

## DWG dosyasında neden yazı tipi değiştirilir?

- **Tutarlılık:** Yerel font ayarları ne olursa olsun tüm katılımcıların aynı tipografi görmesini garanti eder.  
- **Okunabilirlik:** Varsayılan CAD fontları ekranda zor okunabilir; Arial gibi temiz bir fonta geçmek netliği artırır.  
- **Markalaşma:** Teknik çizimleri kurumsal stil kılavuzlarıyla uyumlu hale getirir.

## Önkoşullar

- **Java Development Kit (JDK)** – herhangi bir yeni sürüm (8+ önerilir).  
- **Aspose.CAD for Java** – [web sitesinden](https://releases.aspose.com/cad/java/) indirin.  
- **Örnek DWG dosyası** – değiştirmek istediğiniz çizim (test için herhangi bir DWG veya DXF dosyası kullanabilirsiniz).

## İsim Uzaylarını İçe Aktarma

Java projenizde Aspose.CAD ile çalışmak için gerekli sınıfları içe aktarın. Bu içe aktarmalar, görüntü yükleme, CAD‑özel nesneler ve stil manipülasyonu erişimini sağlar.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Yazı tipini değiştirmek için adım adım rehber

### Adım 1: DWG dosyanızı yükleyin (load dwg file java)

Öncelikle API'yi DWG (veya DXF) dosyanızın konumuna yönlendirin ve dosyayı bir `CadImage` nesnesine yükleyin.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **İpucu:** DWG dosyalarıyla doğrudan çalışıyorsanız, `srcFile` değişkenindeki `.dxf` uzantısını `.dwg` ile değiştirin.

### Adım 2: Stil tablosu üzerinde döngü oluşturun ve birincil yazı tipini ayarlayın

Her CAD çizimi bir stil nesnesi koleksiyonu içerir. Bu koleksiyonu dolaşın ve `setPrimaryFontName` metodunu (birincil yazı tipini **ayarlar**) kullanarak fontu değiştirin.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

`"Arial"` ifadesini, kodu çalıştıran makinede yüklü olan herhangi bir fontla değiştirebilirsiniz.

### Adım 3: Değiştirilen çizimi kaydedin

Yazı tipini güncelledikten sonra değişiklikleri yeni bir DWG dosyasına (veya orijinali üzerine) yazın.

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Kaydedilen dosya artık belirttiğiniz fontu kullanır ve tüm metin açıklamaları bu tipografiyle görüntülenir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **Yazı tipi uygulanmadı** | Fontun ana işletim sistemine yüklü olduğunu ve adının tam olarak eşleştiğini doğrulayın. |
| **`Image.load` bir istisna fırlatıyor** | Dosya yolunun doğru olduğundan ve dosyanın desteklenen bir DWG/DXF formatında olduğundan emin olun. |
| **Büyük dosyalarda performans yavaşlıyor** | Dosyaları ayrı bir iş parçacığında işleyin veya UI blokajını önlemek için toplu işlem yapın. |

## SSS

### S1: DWG dosyamda yapılan yazı tipi değişikliklerini geri alabilir miyim?

C1: Evet, orijinal DWG dosyasını yeniden yükleyerek veya CAD yazılımınızdaki geri alma işlevini kullanarak yazı tipi değişikliklerini geri alabilirsiniz.

### S2: Aspose.CAD for Java'da yazı tipi değişiklikleriyle ilgili sınırlamalar var mı?

C2: Yazı tipi değişikliği yetenekleri sistemde mevcut fontlara bağlıdır. İstenen fontun erişilebilir olduğundan emin olun veya DWG dosyasına gömmeyi düşünün.

### S3: Değişiklik sırasında yazı tipi boyutunu nasıl ayarlayabilirim?

C3: Aspose.CAD içinde stil özelliklerine erişerek font boyutunu istediğiniz gibi değiştirebilirsiniz.

### S4: Yazı tipi değişikliğini toplu bir işlemde otomatikleştirebilir miyim?

C4: Evet, Aspose.CAD for Java toplu işleme destek verir. Betik veya programlama yoluyla birden fazla DWG dosyası üzerinde yazı tipi değişikliklerini otomatikleştirebilirsiniz.

### S5: Aspose.CAD for Java en yeni CAD dosya formatlarıyla uyumlu mu?

C5: Evet, Aspose.CAD for Java düzenli olarak güncellenir ve en yeni CAD dosya formatlarını destekler, böylece sektör standartlarıyla uyumluluk sağlanır.

## Sık Sorulan Sorular

**S: `setPrimaryFontName` metodu sadece metin varlıklarını etkiler mi?**  
C: Stil tablosundaki birincil fontu günceller; bu da o stili referans alan tüm metin nesnelerini etkiler.

**S: Sistemde yüklü olmayan özel bir font kullanabilir miyim?**  
C: Aspose.CAD, işletim sisteminin font kayıt defterine dayanır. Özel bir font kullanmak için kodu çalıştıran makineye fontu kurmanız gerekir.

**S: Tek bir katman için sadece fontu değiştirmek mümkün mü?**  
C: Evet, `setPrimaryFontName` metodunu çağırmadan önce katman adına göre stilleri filtreleyebilirsiniz.

**S: DWG 2022 dosyaları için hangi Aspose.CAD sürümü gerekir?**  
C: En son sürüm (2025 itibarıyla) DWG 2022'yi tam olarak destekler. Belirli format desteği için sürüm notlarını kontrol edin.

**S: Geliştirme ortamında lisanslamayı nasıl yönetirim?**  
C: Test için geçici bir değerlendirme lisansı kullanın. Üretim ortamında `License.setLicense("Aspose.Total.Java.lic");` kodu ile satın alınan lisans dosyasını gömün.

---

**Son Güncelleme:** 2025-12-28  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}