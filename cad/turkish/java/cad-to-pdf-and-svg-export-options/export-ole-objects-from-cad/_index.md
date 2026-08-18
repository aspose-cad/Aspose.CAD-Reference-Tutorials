---
date: 2026-03-02
description: Aspose.CAD for Java'nin potansiyelini ortaya çıkarın. OLE nesnelerini
  zahmetsizce dışa aktarın ve **CAD'i PNG olarak kaydedin**. Kesintisiz CAD veri yönetimi
  için hemen indirin.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: CAD'i PNG Olarak Kaydet – Aspose.CAD for Java Kullanarak OLE Nesnelerini Dışa
  Aktar
url: /tr/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD'i PNG Olarak Kaydet – Aspose.CAD for Java Kullanarak OLE Nesnelerini Dışa Aktarın

## Giriş

Bilgisayar Destekli Tasarım (CAD) dünyasının dinamik ortamında, OLE (Object Linking and Embedding) nesnelerini verimli bir şekilde yönetmek ve çıkarmak — ve **CAD'i PNG olarak kaydetmek** — raporlama, web önizleme veya arşivleme gibi sonraki iş akışları için kritik öneme sahiptir. Aspose.CAD for Java, sadece OLE nesnelerini dışa aktarmanızı ve CAD çizimlerini yüksek kaliteli PNG görüntülerine dönüştürmenizi birkaç satır kodla sağlayan güçlü, kod‑ilk çözüm sunar.

## Hızlı Yanıtlar
- **Aspose.CAD ne yapar?** CAD dosyalarını (DWG, DXF, DGN vb.) yerel CAD yazılımına ihtiyaç duymadan okur, manipüle eder ve dönüştürür.  
- **CAD'i PNG olarak kaydedebilir miyim?** Evet—herhangi bir yerleşimi rasterleştirmek için `PngOptions` ve `CadRasterizationOptions` kullanın.  
- **OLE nesnelerini nasıl dışa aktarırım?** CAD dosyasını `Image.load` ile yükleyin ve OLE içeren her yerleşimi PNG olarak kaydedin.  
- **Lisans gerekir mi?** Ücretsiz deneme mevcuttur; ticari lisans değerlendirme sınırlamalarını kaldırır.  
- **Hangi Java sürümü gereklidir?** Java 8 veya üzeri tam olarak desteklenir.

## **save CAD as PNG** nedir?
CAD'i PNG olarak kaydetmek, vektör tabanlı CAD çizimlerini piksel tabanlı bir PNG görüntüsüne rasterleştirmek anlamına gelir. Bu dönüşüm, web sayfaları, mobil uygulamalar veya dokümantasyon için hafif, evrensel olarak görüntülenebilir bir format gerektiğinde faydalıdır.

## Aspose.CAD for Java'ı **CAD'i PNG'e dönüştürmek** için neden kullanmalısınız?
- **CAD kurulumu gerekmez** – kütüphane tamamen Java'da çalışır.  
- **Yerleşim bütünlüğünü korur** – belirli yerleşimleri seçebilir, DPI'yı kontrol edebilir ve çizgi kalitesini koruyabilirsiniz.  
- **Toplu işleme** – basit bir döngü ile birden fazla dosya üzerinde yineleme yapabilirsiniz.  
- **OLE nesnelerini dışa aktar** – DWG/DXF dosyalarına gömülü OLE içeriği otomatik olarak PNG çıktısına işlenir.

## Önkoşullar

Öğreticiye başlamadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- **Java Ortamı** – Makinenizde bir Java geliştirme ortamının kurulu olduğundan emin olun.  
- **Aspose.CAD for Java** – Aspose.CAD for Java kütüphanesini indirin ve kurun. Kütüphaneyi [indirme bağlantısında](https://releases.aspose.com/cad/java/) bulabilirsiniz.  
- **CAD Dosyaları** – Dışa aktarmak istediğiniz OLE nesnelerini içeren CAD dosyalarını hazırlayın.

## Ad Alanlarını İçe Aktarın

İşlemeye başlamak için gerekli ad alanlarını Java projenize dahil edin. Bu ad alanları, Aspose.CAD kullanarak CAD dosyalarıyla çalışmak için gerekli sınıfları ve işlevleri sağlar.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Şimdi, CAD'den OLE nesnelerini dışa aktarma sürecini birden fazla adıma ayıralım:

## **CAD'i PNG olarak kaydetmek** ve OLE nesnelerini dışa aktarmak

### Adım 1: Belge Dizinini Ayarlayın

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

`"Your Document Directory"` ifadesini CAD dosyalarınızı içeren dizinin yoluyla değiştirin.

### Adım 2: CAD Dosya Adlarını Tanımlayın

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

`files` dizisinde işlemek istediğiniz CAD dosyalarının adlarını belirtin.

### Adım 3: PNG Dışa Aktarma Seçeneklerini Ayarlayın

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Vektör rasterleştirme ve yerleşim ayarlarını içerecek şekilde PNG dışa aktarma seçeneklerini yapılandırın. Bu seçenekler, istediğiniz kaliteyle **CAD'i PNG'e dönüştürmenizi** sağlar.

### Adım 4: CAD Dosyaları Üzerinde Döngü

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Belirtilen her CAD dosyasını Aspose.CAD ile yükleyin ve OLE nesnelerini PNG görüntüleri olarak kaydedin. Bu döngü, toplu olarak **DWG'yi PNG'e dönüştürmenin** basit bir yolunu gösterir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|----------|
| **Boş PNG çıktısı** | Yerleşim adı eşleşmiyor | `"`Layout1`"` adlı yerleşimin kaynak DWG'de mevcut olduğunu doğrulayın. |
| **OLE grafikleri eksik** | OLE nesneleri farklı bir yerleşimde depolanmış | Tüm ilgili yerleşimleri `rasterizationOptions.setLayouts(...)` içinde ekleyin. |
| **Büyük dosyalarda bellek yetersizliği hatası** | Yüksek DPI ayarları | DPI'yi `rasterizationOptions.setResolution(...)` ile azaltın veya dosyaları tek tek işleyin. |

## Sıkça Sorulan Sorular

**S: Aspose.CAD tüm CAD dosya formatlarıyla uyumlu mu?**  
C: Aspose.CAD, DWG, DXF ve DGN dahil olmak üzere çeşitli CAD formatlarını destekler. Tam liste için [belgelere](https://reference.aspose.com/cad/java/) bakın.

**S: OLE nesneleri için dışa aktarma ayarlarını özelleştirebilir miyim?**  
C: Evet, Aspose.CAD, dışa aktarma ayarlarını özelleştirmenize olanak tanıyan kapsamlı seçenekler sunar; böylece çıktıyı özel gereksinimlerinize göre şekillendirebilirsiniz.

**S: Aspose.CAD için ücretsiz bir deneme mevcut mu?**  
C: Evet, [buradan](https://releases.aspose.com/) ücretsiz bir deneme alarak Aspose.CAD'in yeteneklerini keşfedebilirsiniz.

**S: Aspose.CAD topluluk desteğini nereden alabilirim?**  
C: Yardım almak ve deneyimlerinizi paylaşmak için Aspose.CAD topluluğuna [forumda](https://forum.aspose.com/c/cad/19) katılın.

**S: Aspose.CAD için bir lisans nasıl satın alabilirim?**  
C: Geliştirme ihtiyaçlarınıza uygun bir lisans edinmek için [satın alma sayfasını](https://purchase.aspose.com/buy) ziyaret edin.

## Sonuç

Bu basit ama güçlü adımlarla, Aspose.CAD for Java kullanarak CAD dosyalarından OLE nesnelerini dışa aktarırken **CAD'i PNG olarak kaydedebilir** ve görüntü‑tabanlı iş akışlarınıza yeni olanaklar katabilirsiniz. Bu çok yönlü araç, geliştiricilerin CAD verilerini verimli bir şekilde yönetmesini sağlar ve CAD uygulama geliştirme ile sonraki görüntü‑tabanlı süreçlerde yeni fırsatlar sunar.

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}