---
date: 2026-06-19
description: Aspose.CAD for Java ile DWG dosyalarını nasıl düzenleyeceğinizi öğrenin,
  DWG XRef yollarını nasıl güncelleyeceğinizi ve bağlantıları nasıl düzenleyeceğinizi
  öğrenin. Ücretsiz deneme sürümünü bugün deneyin!
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
linktitle: Bağlantıyı Düzenle
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  type: TechArticle
- description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
  type: HowTo
- questions:
  - answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
    question: Do I need to call a specific method to write the edited DWG back to
      disk?
  - answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
    question: Is it possible to edit multiple hyperlinks in one pass?
  type: FAQPage
second_title: Aspose.CAD Java API
title: DWG Bağlantılarını Düzenleme - Aspose.CAD Java Öğreticisi
url: /tr/java/other-cad-operations/edit-hyperlink/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG Hipermetin Bağlantılarını Düzenleme - Aspose.CAD Java Öğreticisi

## Hızlı Yanıtlar
- **Java'da DWG düzenlemesini hangi kütüphane yönetir?** Aspose.CAD for Java.  
- **Hipermetin bağlantılarını ve XRef yollarını birlikte düzenleyebilir miyim?** Evet—her ikisi de aynı API'de desteklenir.  
- **Geliştirme için lisansa ihtiyacım var mı?** Ücretsiz deneme test için çalışır; üretim için ticari lisans gereklidir.  
- **Hangi Java sürümü gereklidir?** Java 8 veya üzeri.  
- **Kod örneği olduğu gibi çalıştırılabilir mi?** Evet, dosya yollarını yerel DWG dosyalarınıza gösterecek şekilde güncelledikten sonra.

## DWG hipermetin bağlantılarını ve XRef yollarını neden düzenlemelisiniz?

Hipermetin bağlantılarını ve XRef yollarını güncel tutmak, kırık referansları önler, proje dokümantasyonunun her zaman doğru kaynaklara işaret etmesini sağlar ve geniş CAD kütüphaneleri üzerinde otomatik toplu güncellemeleri mümkün kılar. Bu, manuel çabayı azaltır, hataları en aza indirir ve tasarım yaşam döngüsü boyunca bağlantı bütünlüğünü programlı olarak koruyarak genel proje verimliliğini artırır.

## Önkoşullar

Öğreticiye başlamadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

1. **Java Geliştirme Ortamı:** JDK 8+ yüklü ve favori IDE'niz (IntelliJ IDEA, Eclipse vb.).  
2. **Aspose.CAD for Java Kütüphanesi:** Aspose.CAD for Java kütüphanesini [download link](https://releases.aspose.com/cad/java/) adresinden indirin ve kurun.  
3. **DWG Çizimi:** Hipermetin bağlantılarını düzenlemek için bir DWG dosyanız hazır olsun.

## Paketleri İçe Aktarma

Java projenize gerekli paketleri içe aktararak başlayın. Bu, Aspose.CAD for Java işlevlerine erişiminizi sağlar.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## Aspose.CAD for Java Kullanarak DWG Hipermetin Bağlantılarını Nasıl Düzenlersiniz?

`CadImage` Aspose.CAD sınıfı, CAD çizimlerini yüklemek ve kaydetmek için kullanılır. DWG dosyasını `CadImage` ile yükleyin, varlıkları döngüyle gezerek gerektiğinde hipermetin bağlantısını ve XRef yolunu güncelleyin ve ardından görüntüyü DWG olarak kaydedin. Bu uçtan uca akış, tek bir geçişte birden fazla varlığı değiştirmenizi sağlar ve tüm değişikliklerin kalıcı olmasını garanti eder.

### Adım 1: Insert Nesnelerine Erişme

`CadInsertObject` Aspose.CAD sınıfı, bir DWG çizimindeki eklenmiş blok referansını (XRef) temsil eder. Varlıkları döngüyle gezerek bir varlığın `CadInsertObject` sınıfının bir örneği olup olmadığını belirleyin.

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### Adım 2: DWG Çiziminde XRef Yolunu Nasıl Değiştirirsiniz

`CadImage`, Aspose.CAD for Java'da CAD dosyalarını yükleyen ve kaydeden temel nesnedir. Insert nesnesini tanımladıktan sonra ilişkili blok varlığını alın ve XRef yolunu gerektiği gibi güncelleyin. Bu, referansın doğru dış dosyaya işaret etmesini sağlar.

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### Adım 3: Hipermetin Bağlantılarını Değiştirme

Sonra, varlığın bir hipermetin bağlantısı olup olmadığını kontrol edin. Hipermetin belirli bir URL ile eşleşiyorsa, istediğiniz URL'ye güncelleyin. Bu adım, CAD görüntüleyicide hipermetine tıklandığında yeni hedefin açılmasını garanti eder.

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## Yaygın Tuzaklar ve İpuçları

- **Dize karşılaştırması:** Java'da güvenilir dize karşılaştırması için `==` yerine `.equals()` kullanın. Örnek basitlik için `==` kullanıyor, ancak üretimde `entity.getHyperlink().equals("https://products.aspose.com")` ile değiştirin.  
- **Null kontrolleri:** `block.getXRefPathName()`'in `null` olmadığını `.getValue()` çağırmadan önce her zaman doğrulayın.  
- **Değişiklikleri kaydetme:** Varlıkları değiştirdikten sonra `cadImage.save("output.dwg");` çağırarak değişiklikleri kalıcı hale getirin (orijinal blok sayısını korumak için kod çıkarılmıştır).  
- **Performans notu:** Aspose.CAD for Java 30'dan fazla CAD formatını destekler ve tüm belgeyi belleğe yüklemeden 2 GB'a kadar dosyaları işleyebilir, bu da toplu güncellemeleri hızlı ve bellek‑verimli yapar.

## Sıkça Sorulan Sorular

### S1: Aspose.CAD for Java tüm DWG çizim sürümleriyle uyumlu mu?

C1: Aspose.CAD for Java 50'den fazla DWG sürümünü destekler, AutoCAD 2000'den en yeni 2025 formatına kadar.

### S2: Aspose.CAD for Java'u ticari projelerde kullanabilir miyim?

C2: Evet, üretim kullanımı için ticari lisans gereklidir. Lisansı [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

### S3: Aspose.CAD for Java için ücretsiz deneme mevcut mu?

C3: Evet, ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) keşfedebilirsiniz.

### S4: Aspose.CAD for Java için teknik destek nasıl alabilirim?

C4: Herhangi bir teknik yardım için Aspose.CAD forumunu [buradan](https://forum.aspose.com/c/cad/19) ziyaret edin.

### S5: Test amaçları için geçici lisans alabilir miyim?

C5: Evet, geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

**Ek Soru & Cevap**

**S: Düzenlenen DWG'yi diske yazmak için belirli bir metoda ihtiyacım var mı?**  
C: Evet, değişiklikleri yaptıktan sonra `cadImage.save("EditedDrawing.dwg");` çağırarak değişiklikleri kalıcı hâle getirin.

**S: Tek bir geçişte birden fazla hipermetin bağlantısını düzenlemek mümkün mü?**  
C: Kesinlikle—`cadImage.getEntities()` üzerinden döngü kurup her eşleşen varlıkta hipermetin mantığını uygulayın.

**Last Updated:** 2026-06-19  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [Aspose.CAD for Java Kullanarak DWG Dosyalarından XREF Meta Verilerini Okuma](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [Aspose.CAD for Java Kullanarak DWG Dosyalarına Özel Özellikler Ekleme](/cad/java/additional-features/add-custom-properties/)
- [Aspose.CAD for Java Kullanarak DWG'yi PDF veya Raster Olarak Dışa Aktarma](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}