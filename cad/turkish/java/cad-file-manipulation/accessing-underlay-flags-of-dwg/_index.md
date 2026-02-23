---
date: 2026-02-23
description: Aspose CAD DWG for Java kullanarak dwg dosyalarını nasıl yükleyeceğinizi
  ve alt katman bayraklarını nasıl çıkaracağınızı öğrenin – geliştiriciler için adım
  adım bir rehber.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – DWG'yi Yükle ve Alt Katman Bayraklarına Eriş (Java)
url: /tr/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG Dosyasını Yükle ve Alt Katman Bayraklarına Eriş – Aspose.CAD for Java

Modern CAD iş akışlarında, **aspose cad dwg ile bir DWG dosyasını hızlıca yükleyebilirsiniz** ve genellikle sıradan izleyicilerden gizli olan alt katman detaylarını çıkarabilirsiniz. Java DWG görüntüleyicisi oluşturuyor olun, bir toplu işlem dwg hattını otomatikleştiriyor olun veya GIS entegrasyonu için meta verileri çıkarıyor olun, Aspose.CAD for Java bunu temiz, kod‑öncelikli bir şekilde yapmanızı sağlar. Bu öğreticide **DWG dosyasını yükleme**, varlıklarını yineleme ve birçok geliştiricinin göz ardı ettiği alt katman bayraklarını okuma adımlarını adım adım göstereceğiz.

## Hızlı Yanıtlar
- **DWG'yi açmak için birincil sınıf nedir?** `com.aspose.cad.Image.load()` bir `CadImage` döndürür.
- **Alt katman bilgilerini hangi nesne tutar?** `CadUnderlay` (veya `CadDgnUnderlay` gibi türetilmiş tipleri).
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.
- **Bir döngüde birden fazla DWG dosyasını işleyebilir miyim?** Evet – sadece yükle‑ve‑yinele desenini tekrarlayın.
- **Bu yaklaşım Java 11+ ile uyumlu mu?** Kesinlikle, Aspose.CAD Java 8'den en yeni LTS sürümlere kadar destekler.

## aspose cad dwg – DWG Dosyası Yükleme (Java)

`Image.load()` ikili DWG içeriğini okur ve bellekte bir `CadImage` nesnesi oluşturur. Buradan katmanları, blokları ve alt katman varlıklarını DWG dosya formatıyla doğrudan uğraşmadan keşfedebilirsiniz.

## Neden bir DWG'den alt katman bayraklarını çıkarmalısınız?

Alt katman bayrakları, dış bir referansın (örneğin bir DGN veya PDF alt katmanı) çizim içinde nasıl konumlandırıldığını, ölçeklendirildiğini ve döndürüldüğünü gösterir. Bu değerleri bilmek şunları yapmanızı sağlar:
- Özel bir **java dwg viewer** içinde tam görsel düzeni yeniden oluşturmak.
- Alt katmanları daha fazla düzenleme için yerel CAD varlıklarına dönüştürmek.
- Uyumluluk veya dokümantasyon için alt katman meta verilerini içeren raporlar oluşturmak.
- **Batch process dwg** dosyalarını toplu işlemek ve alt katman meta verilerini daha sonra analiz için bir veritabanında saklamak.

## Önkoşullar
- **Aspose.CAD Library** – [releases](https://releases.aspose.com/cad/java/) sayfasından indirin.  
- **Java Development Kit** – JDK 8 veya daha yenisi.  
- **Bir klasör** analiz etmek istediğiniz DWG dosyalarını içerir. Koddaki `"Your Document Directory"` ifadesini gerçek yolunuzla değiştirin.

## İsim Uzaylarını İçe Aktar

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Adım‑Adım Kılavuz

### Adım 1: Kaynak Dizini Ayarla
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
DWG dosyalarınızın nerede bulunduğunu tanımlayın. Ayrı bir klasör kullanmak örneği temiz ve taşınabilir tutar.

### Adım 2: DWG Dosyasını Yükle
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Burada **dwg dosyasını yükliyoruz** `BlockRefDgn.dwg` dosyasını bir `CadImage` örneğine, inceleme için hazır.

### Adım 3: DWG Varlıklarını Döngüyle Gezin
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
Döngü her varlığı—çizgileri, daireleri, blokları ve alt katmanları—gezer, böylece ihtiyacımız olanları seçebiliriz.

### Adım 4: CadDgnUnderlay Varlıklarını Tanımla
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Yalnızca `CadDgnUnderlay` nesneleri aradığımız alt katman bayraklarını içerir, bu yüzden onları filtreliyoruz.

### Adım 5: Alt Katman Bilgilerine Eriş
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Bir `CadUnderlay` elde ettiğimizde, yolunu, adını, ekleme noktasını, dönüşünü, ölçek faktörlerini ve görünürlük, kırpma ve diğer render seçeneklerini gösteren `UnderlayFlags` enumunu okuyabiliriz.

## dwg dosyalarını toplu işte nasıl yüklersiniz

Eğer **batch process dwg** dosyalarına ihtiyacınız varsa, yukarıdaki adımları `dataDir` içindeki tüm dosyalar üzerinde yineleyen basit bir `for` döngüsüyle sarın. Aynı `Image.load()` çağrısı her dosya için çalışır ve çıkarılan bayrakları CSV ya da bir veritabanında sonraki raporlamalar için saklayabilirsiniz.

## Yaygın Sorunlar ve İpuçları
- **Null underlay path** – DWG'nin gerçekten dış bir dosyaya referans verdiğinden emin olun; aksi takdirde yol boş olur.
- **Unsupported underlay type** – Aspose.CAD şu anda DGN alt katmanlarını destekler; PDF alt katmanları henüz API üzerinden sunulmamaktadır.
- **License exceptions** – Geçerli bir lisans olmadan kodu çalıştırmak, dışa aktarılan tüm görüntülere bir filigran ekleyecektir.
- **Performance tip:** Birçok dosyayı toplu işte işlerken tek bir `Image` örneğini yeniden kullanarak GC baskısını azaltın.

## Sıkça Sorulan Sorular

**S: Aspose.CAD for Java'yi diğer CAD dosya formatlarıyla kullanabilir miyim?**  
C: Aspose.CAD öncelikle DWG formatına odaklanır, ancak DXF, DWF ve diğer CAD formatlarını da destekler.

**S: Aspose.CAD for Java için bir deneme sürümü mevcut mu?**  
C: Evet, [buradan](https://releases.aspose.com/) ücretsiz deneme ile özellikleri keşfedebilirsiniz.

**S: Aspose.CAD for Java ile ilgili destek alabilir veya yardım isteyebilir miyim?**  
C: Topluluk desteği ve tartışmalar için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

**S: Aspose.CAD for Java için geçici lisanslar mevcut mu?**  
C: Evet, geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

**S: Aspose.CAD for Java için kapsamlı belgeleri nerede bulabilirim?**  
C: Ayrıntılı bilgi için [belgelere](https://reference.aspose.com/cad/java/) bakın.

---

**Son Güncelleme:** 2026-02-23  
**Test Edilen Versiyon:** Aspose.CAD 24.12 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}