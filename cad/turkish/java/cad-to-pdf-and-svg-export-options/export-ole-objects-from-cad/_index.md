---
date: 2026-01-04
description: CAD'i PNG olarak kaydetmeyi ve Aspose.CAD for Java kullanarak CAD dosyalarından
  OLE nesnelerini sorunsuz bir şekilde dışa aktarmayı öğrenin. Hızlı kurulum, tam
  kod örneği ve en iyi uygulama ipuçları.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: CAD'yi PNG olarak kaydedin ve Aspose.CAD for Java ile OLE nesnelerini dışa
  aktarın
url: /tr/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD'yi PNG Olarak Kaydet ve OLE Nesnelerini Aspose.CAD for Java ile Dışa Aktar

## Giriş

Bilgisayar Destekli Tasarım (CAD) dünyasının hızlı temposunda, gömülü OLE (Object Linking and Embedding) nesnelerini çıkartırken **CAD'yi PNG olarak kaydetmek**, iş akışınızı büyük ölçüde hızlandırabilir. İster toplu dönüşüm aracı oluşturuyor olun, ister bir web portalı için küçük resimler üretiyor olun ya da sadece OLE içeriğini arşivlemeniz gereksin, Aspose.CAD for Java bunu temiz ve programatik bir şekilde yapmanızı sağlar. Bu öğreticide, projenizi kurmaktan her OLE nesnesini PNG görüntüsü olarak dışa aktarmaya kadar tüm süreci adım adım inceleyeceğiz.

## Hızlı Yanıtlar
- **OLE nesnelerini doğrudan PNG'ye dışa aktarabilir miyim?** Evet – Aspose.CAD CAD dosyasını yükler ve her yerleşimi PNG'ye rasterleştirmenize olanak tanır.  
- **Hangi Java sürümü gereklidir?** Java 8 veya üzeri.  
- **Bu özellik için lisans gerekli mi?** Değerlendirme için ücretsiz deneme çalışır; üretim için lisans gereklidir.  
- **Vektör verileri korunacak mı?** PNG rasterleştirme görsel doğruluğu korur, ancak çıktı raster, vektör değildir.  
- **Toplu işleme destekleniyor mu?** Kesinlikle – kod örneğinde gösterildiği gibi dosya dizisi üzerinde döngü yapabilirsiniz.  

## Önkoşullar

- **Java Development Kit (JDK)** – Java 8+ yüklü ve yapılandırılmış.  
- **Aspose.CAD for Java** – En son kütüphaneyi [download link](https://releases.aspose.com/cad/java/) adresinden indirin.  
- **CAD kaynak dosyaları** – Dışa aktarmak istediğiniz OLE nesnelerini içeren herhangi bir DWG/DXF/DGN dosyası.  

## İsim Uzaylarını İçe Aktarma

CAD dosyalarıyla çalışmak için temel Aspose.CAD sınıflarını içe aktarmanız gerekir. İçe aktarma bloğunu tam olarak gösterildiği gibi tutun – bu, daha sonra öğreticide kullanılan sınıfları sağlar.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## CAD'yi PNG Olarak Kaydetme

Aşağıda, **OLE nesnelerini dışa aktarma ve CAD'yi PNG olarak kaydetme** yöntemini gösteren özlü, adım‑adım bir rehber bulunmaktadır. Her adım kısa bir açıklama ve projenize kopyalamanız gereken tam kodu içerir.

### Adım 1: Belge Dizinini Ayarlayın

CAD çizimlerinizi tutan klasörü tanımlayın. Yer tutucuyu makinenizdeki gerçek yol ile değiştirin.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Adım 2: CAD Dosya Adlarını Tanımlayın

İşlemek istediğiniz her CAD dosyasını listeleyin. Gerekli olduğu kadar giriş ekleyebilirsiniz.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Adım 3: PNG Dışa Aktarma Seçeneklerini Ayarlayın

Rasterleştirme ayarlarını yapılandırın. Burada belirli bir yerleşim (`Layout1`) hedeflenir ve varsayılan PNG seçenekleri kullanılır.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Adım 4: CAD Dosyaları Üzerinde Döngü Yapın ve PNG Olarak Kaydedin

Her CAD dosyasını yükleyin, OLE nesnelerini rasterleştirin ve çıktı PNG dosyasını yazın. `_out.png` eki, oluşturulan görüntüleri tanımlamanıza yardımcı olur.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|--------------|-------|
| **`Image.load` `FileNotFoundException` hatası verir** | `dataDir` yolu yanlış veya dosya adında bir yazım hatası var. | Dizin dizesini tekrar kontrol edin ve dosya adlarının tam olarak, boşluklar dahil, eşleştiğinden emin olun. |
| **Çıktı PNG boş** | Yerleşim adı kaynak CAD dosyasında mevcut değil. | `cadImage.getLayouts()` kullanarak mevcut yerleşimleri listeleyin, ardından `rasterizationOptions.setLayouts(...)` ile güncelleyin. |
| **Büyük CAD dosyaları OutOfMemoryError hatasına neden olur** | Yüksek çözünürlüklü görüntülerin rasterleştirilmesi çok fazla yığın alanı tüketir. | JVM yığın boyutunu artırın (`-Xmx2g`) veya rasterleştirme çözünürlüğünü `rasterizationOptions.setResolution(...)` ile düşürün. |

## SSS

### Soru 1: Aspose.CAD tüm CAD dosya formatlarıyla uyumlu mu?

A1: Aspose.CAD çeşitli CAD formatlarını destekler, DWG, DXF ve DGN dahil. Tam liste için [documentation](https://reference.aspose.com/cad/java/) adresine bakın.

### Soru 2: OLE nesneleri için dışa aktarma ayarlarını özelleştirebilir miyim?

A2: Evet, Aspose.CAD geniş seçenekler sunar; böylece çıktıyı özel gereksinimlerinize göre şekillendirebilirsiniz.

### Soru 3: Aspose.CAD için ücretsiz deneme mevcut mu?

A3: Evet, [here](https://releases.aspose.com/) adresinden ücretsiz deneme alarak Aspose.CAD yeteneklerini keşfedebilirsiniz.

### Soru 4: Aspose.CAD için topluluk desteğini nereden alabilirim?

A4: Yardım almak ve deneyimlerinizi paylaşmak için Aspose.CAD topluluğuna [forum](https://forum.aspose.com/c/cad/19) üzerinden katılabilirsiniz.

### Soru 5: Aspose.CAD için lisans nasıl satın alınır?

A5: Geliştirme ihtiyaçlarınıza uygun bir lisans edinmek için [purchase page](https://purchase.aspose.com/buy) adresini ziyaret edin.

## Sonuç

Bu beş basit adımı izleyerek **CAD'yi PNG olarak kaydedebilir** ve sadece birkaç satır Java kodu ile gömülü tüm OLE nesnelerini çıkarabilirsiniz. Bu yaklaşım, toplu dönüşümler, otomatik raporlama veya CAD içeriğinin manuel dışa aktarma olmadan raster görüntülere ihtiyaç duyduğu her senaryo için idealdir. Kalite ve performans gereksinimlerinize uygun farklı rasterleştirme seçenekleriyle denemeler yapmaktan çekinmeyin.

---

**Last Updated:** 2026-01-04  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}