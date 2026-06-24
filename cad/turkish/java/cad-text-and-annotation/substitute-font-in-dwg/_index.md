---
date: 2026-05-04
description: Aspose.CAD kullanarak Java’da dxf’i dwg’ye dönüştürmeyi ve birincil fontu
  ayarlamayı öğrenin. Mükemmel CAD görselleri için adım adım rehber.
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: DWG'de Yazı Tipi Değiştir
second_title: Aspose.CAD Java API
title: DXF'i DWG'ye dönüştür ve DWG'de fontu değiştir Aspose.CAD Java
url: /tr/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG dosyasını Java'da nasıl yükleyip fontu Aspose.CAD ile değiştirirsiniz

## Giriş

Java uygulamalarında **convert dxf to dwg** yapmanız ve çizimlerinize cilalı bir görünüm kazandırmanız gerekiyorsa, fontu değiştirmek hızlı bir çözümdür. Aspose.CAD for Java ile varsayılan metin stilini sistemde yüklü herhangi bir fontla değiştirebilir, böylece her açıklamanın tam olarak beklendiği gibi görünmesini sağlayabilirsiniz. Bu öğreticide, Java'da bir DWG dosyasını yüklemekten `setPrimaryFontName` metodunu kullanarak fontu değiştirmeye kadar tüm süreci adım adım göstereceğiz.

## Hızlı Yanıtlar
- **Hangi kütüphane gerekiyor?** Aspose.CAD for Java.  
- **Java'da bir DWG dosyasını yükleyebilir miyim?** Evet, DWG yolunda `Image.load()` metodunu çağırmanız yeterlidir.  
- **Hangi metod fontu değiştirir?** `setPrimaryFontName`.  
- **Üretim için lisansa ihtiyacım var mı?** Evet, ticari bir lisans gereklidir.  
- **Toplu işleme mümkün mü?** Kesinlikle – aynı kodla birden fazla dosya üzerinde döngü oluşturabilirsiniz.

## **convert dxf to dwg** nedir?

“Convert dxf to dwg”, birçok CAD uygulamasının kullandığı yerel DWG formatına bir DXF (Drawing Exchange Format) dosyasını dönüştürmeyi ifade eder. Dönüştürme, yaygın olarak desteklenen bir DXF çizimini alıp DWG iş akışına dahil etmenizi ve ardından Aspose.CAD kullanarak gelişmiş stil uygulamaları—örneğin font değiştirme—yapmanızı sağlar.

## DWG dosyasında neden font değiştirilir?

- **Tutarlılık:** Yerel font ayarlarından bağımsız olarak tüm iş ortaklarının aynı yazı tipini görmesini sağlar.  
- **Okunabilirlik:** Bazı varsayılan CAD fontları ekranda okunması zordur; Arial gibi temiz bir fonta geçmek netliği artırır.  
- **Markalaşma:** Teknik çizimleri kurumsal stil kılavuzlarıyla uyumlu hale getirir.

## Yaygın Kullanım Senaryoları

| Senaryo | Neden Önemlidir |
|----------|----------------|
| **Eski DXF çizimlerinin toplu dönüşümü** | Tek bir adımda DWG'ye dönüştürüp kurumsal fontu uygulayabilirsiniz. |
| **Müşteri sunumları için çizim hazırlama** | Tutarlı, okunabilir fontlar belgelerin profesyonel görünmesini sağlar. |
| **Otomatik CAD iş akışları** | Font değişimini gömmek, manuel sonrası işlem adımlarını ortadan kaldırır. |

## Önkoşullar

- **Java Development Kit (JDK)** – herhangi bir yeni sürüm (8+ önerilir).  
- **Aspose.CAD for Java** – [website](https://releases.aspose.com/cad/java/) adresinden indirin.  
- **Örnek DWG/DXF dosyası** – değiştirmek istediğiniz bir çizim (test için herhangi bir DWG veya DXF dosyası kullanabilirsiniz).

## İsim Uzaylarını İçe Aktarın

Java projenizde Aspose.CAD ile çalışmak için gerekli sınıfları içe aktarın. Bu importlar, görüntü yükleme, CAD‑özel nesneler ve stil manipülasyonuna erişim sağlar.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Fontu değiştirmek için adım adım rehber

### Adım 1: DWG dosyanızı yükleyin (load dwg file java)

İlk olarak, API'yi DWG (veya DXF) dosyanızın konumuna yönlendirin ve dosyayı bir `CadImage` nesnesine yükleyin.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro ipucu:** DWG dosyalarıyla doğrudan çalışıyorsanız, `srcFile` değişkenindeki `.dxf` uzantısını `.dwg` ile değiştirin.

### Adım 2: Stil tablosu üzerinde döngü oluşturun ve birincil font adını ayarlayın

Her CAD çizimi bir stil nesnesi koleksiyonu içerir. Bunlar üzerinde döngü oluşturun ve fontu değiştirmek için `setPrimaryFontName` metodunu (API çağrısı **birincil font adını ayarlar**) kullanın.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

`"Arial"` ifadesini, kodu çalıştıran makinede yüklü herhangi bir fontla değiştirebilirsiniz.

### Adım 3: Değiştirilen çizimi kaydedin

Fontu güncelledikten sonra değişiklikleri yeni bir DWG dosyasına (veya orijinali üzerine yazarak) kaydedin.

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Kaydedilen dosya artık belirttiğiniz fontu kullanacak ve tüm metin açıklamaları bu yazı tipiyle görüntülenecektir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Çözüm |
|-------|----------|
| **Font uygulanmadı** | Fontun ana işletim sistemine yüklü olduğunu ve adının tam olarak eşleştiğini doğrulayın. |
| **`Image.load` bir istisna fırlatıyor** | Dosya yolunun doğru olduğundan ve dosyanın desteklenen bir DWG/DXF formatında olduğundan emin olun. |
| **Büyük dosyalarda performans yavaşlaması** | Dosyaları ayrı bir iş parçacığında işleyin veya UI blokajını önlemek için toplu işleyin. |

## Sıkça Sorulan Sorular

**S: `setPrimaryFontName` metodu sadece metin varlıklarını etkiler mi?**  
C: Stil tablosu için birincil fontu günceller, bu da o stili referans alan tüm metin nesnelerini etkiler.

**S: Sistemde yüklü olmayan özel bir font kullanabilir miyim?**  
C: Aspose.CAD, işletim sisteminin font kayıt defterine dayanır. Özel bir font kullanmak için, kodu çalıştıran makineye fontu yüklemeniz gerekir.

**S: Sadece tek bir katman için fontu değiştirmek mümkün mü?**  
C: Evet, `setPrimaryFontName` metodunu çağırmadan önce stilleri katman adına göre filtreleyebilirsiniz.

**S: DWG 2022 dosyaları için hangi Aspose.CAD sürümü gereklidir?**  
C: En son sürüm (2025 itibarıyla) DWG 2022'yi tam olarak destekler. Belirli format desteği için her zaman sürüm notlarını kontrol edin.

**S: Geliştirme ortamında lisanslamayı nasıl yönetirim?**  
C: Test için geçici bir değerlendirme lisansı kullanın. Üretim için, satın aldığınız lisans dosyasını `License.setLicense("Aspose.Total.Java.lic");` yöntemiyle projeye ekleyin.

---

**Son Güncelleme:** 2026-05-04  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}