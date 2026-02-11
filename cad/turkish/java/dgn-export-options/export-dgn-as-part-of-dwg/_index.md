---
date: 2026-01-10
description: Aspose.CAD for Java kullanarak dgn'yi dwg'ye nasıl dışa aktaracağınızı
  ve MicroStation DGN'yi AutoCAD DWG'ye nasıl dönüştüreceğinizi öğrenin. Adım adım
  rehber.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java ile DGN'den DWG'ye Dışa Aktar
url: /tr/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java ile DGN'yi DWG'ye Dışa Aktarma

## Giriş

Bu öğreticide, **dgn'yi dwg'ye dışa aktarma** ve bir MicroStation DGN tasarımını bir AutoCAD DWG dosyasının içine gömme işlemini Aspose.CAD Java kütüphanesini kullanarak öğreneceksiniz. İster eski MicroStation çizimlerini taşıyor olun, ister DGN alt katmanlarını DWG düzenleriyle birleştirmeniz gerekiyor olsun, bu kılavuz ortamı kurmaktan son DWG'nin PDF önizlemesini oluşturmaya kadar her adımı size gösterecek.

## Hızlı Yanıtlar
- **“export dgn to dwg” ne işe yarar?** Bir DGN alt katmanını DWG içine gömer, AutoCAD'de sorunsuz görüntülenmesini sağlar.
- **Hızlı önizleme için sonucu hangi formata dışa aktarabilirim?** `PdfOptions` kullanarak **cad dosyasını pdf'ye dışa aktarabilirsiniz**.
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Üretim kullanımı için geçici veya ücretli bir Aspose.CAD lisansı gereklidir.
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri, en yeni Aspose.CAD for Java sürümüyle çalışır.
- **Ücretsiz deneme mevcut mu?** Evet – Aspose web sitesinden bir deneme sürümü indirebilirsiniz.

## “export dgn to dwg” nedir?
DGN'yi DWG'ye dışa aktarmak, bir MicroStation DGN tasarımını bir AutoCAD DWG çiziminin içinde alt katman (underlay) olarak dönüştürmek veya gömmek anlamına gelir. Bu, CAD profesyonellerinin mevcut DGN varlıklarını sıfırdan geometri oluşturmadan kullanmalarını sağlar.

## Neden MicroStation DGN'yi AutoCAD DWG'ye dönüştürmeliyiz?
- **İşbirliği:** AutoCAD kullanan ekipler DGN içeriğini doğrudan görüntüleyebilir ve düzenleyebilir.
- **Standartlaştırma:** DWG, birçok sonraki iş akışı (ör. PDF oluşturma, 3D render) için de‑fakto formattır.
- **Koruma:** Orijinal DGN referansları korunur, veri kaybı azalır.

## Ön Koşullar

Öğreticiye başlamadan önce aşağıdaki ön koşulların sağlandığından emin olun:
1. **Aspose.CAD Kütüphanesi:** Aspose.CAD Java kütüphanesini indirin ve kurun. Kütüphaneyi [buradan](https://releases.aspose.com/cad/java/) bulabilirsiniz.
2. **Java Development Kit (JDK):** Sisteminizde Java yüklü olmalı.
3. **Entegre Geliştirme Ortamı (IDE):** Daha sorunsuz bir geliştirme deneyimi için Eclipse veya IntelliJ gibi bir Java IDE'si seçin.

## Paketleri İçe Aktarma

Java projenizde CAD dosyası manipülasyonu için gerekli Aspose.CAD paketlerini içe aktarın. İşte bir örnek:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Adım 1: Dosya Yollarını Ayarlama

DWG dosyası için giriş ve çıkış dosya yollarını tanımlayın. `dataDir`, `fileName` ve `outPath` değişkenlerini buna göre güncelleyin.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Adım 2: PdfOptions Örneği Oluşturma

**CAD dosyasını PDF'ye dışa aktarmak** için `PdfOptions` sınıfının bir örneğini oluşturuyoruz; bu hızlı doğrulama sağlar.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Adım 3: DWG Dosyasını Yükleme

Mevcut DWG dosyasını bir görüntü olarak yükleyin ve `CadImage` tipine dönüştürün.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Adım 4: Varlıklar Üzerinde Döngü

DWG dosyasındaki her bir varlığı (entity) dolaşın ve bir görüntü tanımı (image definition) olup olmadığını kontrol edin. Eğer ise, nesnenin dış referansını alın.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Adım 5: Rasterizasyon Seçeneklerini Tanımlama

`CadRasterizationOptions` nesnesi için sayfa genişliği, yüksekliği, düzenler ve arka plan rengi gibi ayarları tanımlayın.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Adım 6: Vektör Rasterizasyon Seçeneklerini Ayarlama

Dışa aktarma için vektör rasterizasyon seçeneklerini ayarlayın.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Adım 7: DWG'yi PDF'ye Dışa Aktarma

Son olarak, `save` metodunu çağırarak DWG'yi PDF'ye dışa aktarın.

```java
cadImage.save(outPath, exportOptions);
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|----------|
| **DGN alt katmanı görünmüyor** | DWG içinde bir `DGNUNDERLAY` varlığı bulunmuyor. | Kaynak DWG'nin bir DGN referansı içerdiğini doğrulayın. |
| **PDF boş** | Rasterizasyon seçenekleri sıfır boyutta veya yanlış düzen olarak ayarlanmış. | `setPageWidth`/`setPageHeight` değerlerinin pozitif olduğundan ve `setLayouts`'in DWG düzen adıyla eşleştiğinden emin olun. |
| **Lisans istisnası** | Geçerli bir Aspose.CAD lisansı olmadan çalıştırılıyor. | API metodlarını çağırmadan önce geçici veya satın alınmış bir lisans uygulayın. |

## Sıkça Sorulan Sorular

### S1: Aspose.CAD for Java belgelerine nereden ulaşabilirim?

C1: Belgeler [burada](https://reference.aspose.com/cad/java/) bulunabilir.

### S2: Aspose.CAD Java kütüphanesini nasıl indirebilirim?

C2: Kütüphaneyi [bu bağlantıdan](https://releases.aspose.com/cad/java/) indirebilirsiniz.

### S3: Aspose.CAD for Java için ücretsiz bir deneme mevcut mu?

C3: Evet, ücretsiz deneme [burada](https://releases.aspose.com/) mevcuttur.

### S4: Aspose.CAD for Java için geçici bir lisans nasıl alınır?

C4: Geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

### S5: Yardım gerekiyor ya da sorularım var?

C5: Aspose.CAD topluluk destek forumunu [buradan](https://forum.aspose.com/c/cad/19) ziyaret edin.

### S6: Oluşturulan PDF'yi tekrar DWG'ye dönüştürebilir miyim?

C6: PDF bir raster önizlemedir; DWG'ye geri dönüşüm ayrı bir ters‑mühendislik aracı gerektirir.

### S7: Bu yöntem DWF veya DXF gibi diğer CAD formatlarıyla da çalışır mı?

C7: Evet, Aspose.CAD birçok formatı destekler; sadece dosya uzantılarını ve rasterizasyon ayarlarını uygun şekilde değiştirmeniz yeterlidir.

---

**Son Güncelleme:** 2026-01-10  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}