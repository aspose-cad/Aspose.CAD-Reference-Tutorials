---
date: 2025-12-22
description: Aspose.CAD for Java ile DWG dosyasını nasıl yükleyeceğinizi ve alt katman
  bilgilerini nasıl çıkaracağınızı öğrenin – alt katman bayraklarını kapsayan adım
  adım bir rehber.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: DWG Dosyasını Yükle ve Alt Katman Bayraklarına Eriş – Aspose.CAD for Java
url: /tr/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG Dosyasını Yükleme ve Alt Katman Bayraklarına Erişim – Aspose.CAD for Java

Modern CAD iş akışlarında, **DWG dosyasını hızlı bir şekilde yüklemek** ve alt katman detaylarını çıkarmak yaygın bir gereksinimdir. İster bir görüntüleyici oluşturuyor olun, toplu işlem otomasyonu yapıyor olun, ister GIS entegrasyonu için meta verileri çıkarıyor olun, Aspose.CAD for Java bunu temiz, kod‑öncelikli bir şekilde yapmanızı sağlar. Bu öğreticide **DWG dosyasını yükleme**, varlıklarını yineleme ve birçok geliştiricinin göz ardı ettiği alt katman bayraklarını okuma adımlarını adım adım göstereceğiz.

## Hızlı Yanıtlar
- **DWG'yi açmak için birincil sınıf nedir?** `com.aspose.cad.Image.load()` returns a `CadImage`.
- **Alt katman bilgilerini hangi nesne tutar?** `CadUnderlay` (or its derived types like `CadDgnUnderlay`).
- **Geliştirme için lisansa ihtiyacım var mı?** Test için ücretsiz deneme çalışır; üretim için ticari bir lisans gereklidir.
- **Bir döngüde birden fazla DWG dosyasını işleyebilir miyim?** Evet – sadece yükle‑ve‑yineleme desenini tekrarlayın.
- **Bu yaklaşım Java 11+ ile uyumlu mu?** Kesinlikle, Aspose.CAD Java 8'den en yeni LTS sürümlere kadar destekler.

## Aspose.CAD'de “load dwg file” nedir?
`Image.load()` ikili DWG içeriğini okur ve bellekte bir `CadImage` nesnesi oluşturur. Buradan katmanları, blokları ve alt katman varlıklarını, DWG dosya formatıyla doğrudan uğraşmadan keşfedebilirsiniz.

## Neden bir DWG'den alt katman bayraklarını çıkarmalıyız?
Alt katman bayrakları, harici bir referansın (örneğin bir DGN veya PDF alt katmanı) çizim içinde nasıl konumlandırıldığını, ölçeklendirildiğini ve döndürüldüğünü gösterir. Bu değerleri bilmek şunları yapmanızı sağlar:
- Özel bir görüntüleyicide tam görsel düzeni yeniden oluşturmak.
- Alt katmanları daha fazla düzenleme için yerel CAD varlıklarına dönüştürmek.
- Uyumluluk veya dokümantasyon için alt katman meta verilerini içeren raporlar oluşturmak.

## Önkoşullar
- **Aspose.CAD Library** – [releases](https://releases.aspose.com/cad/java/) sayfasından indirin.
- **Java Development Kit** – JDK 8 veya daha yeni bir sürüm.
- **A folder** containing the DWG files you want to analyse. Replace `"Your Document Directory"` in the code with your actual path.

## Ad Alanlarını İçe Aktarın

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
DWG dosyalarınızın bulunduğu yeri tanımlayın. Ayrı bir klasör kullanmak örneği temiz ve taşınabilir tutar.

### Adım 2: DWG Dosyasını Yükle
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Burada **dwg dosyasını yükleyerek** `BlockRefDgn.dwg` dosyasını bir `CadImage` örneğine alıyoruz, inceleme için hazır.

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
Sadece `CadDgnUnderlay` nesneleri aradığımız alt katman bayraklarını içerir, bu yüzden onları filtreliyoruz.

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

## Yaygın Sorunlar ve İpuçları
- **Null alt katman yolu** – DWG'nin gerçekten harici bir dosyaya referans verdiğinden emin olun; aksi takdirde yol boş olur.
- **Desteklenmeyen alt katman türü** – Aspose.CAD şu anda DGN alt katmanlarını destekler; PDF alt katmanları henüz API üzerinden sunulmamaktadır.
- **Lisans istisnaları** – Geçerli bir lisans olmadan kodu çalıştırmak, dışa aktarılan tüm görüntülere bir filigran ekleyecektir.

## Sıkça Sorulan Sorular

**S: Aspose.CAD for Java'yi diğer CAD dosya formatlarıyla kullanabilir miyim?**  
C: Aspose.CAD öncelikle DWG formatına odaklanır ancak DXF, DWF ve diğer CAD formatlarını da destekler.

**S: Aspose.CAD for Java için bir deneme sürümü mevcut mu?**  
C: Evet, özellikleri ücretsiz deneme sürümüyle [buradan](https://releases.aspose.com/) keşfedebilirsiniz.

**S: Aspose.CAD for Java ile ilgili destek alabilir veya yardım isteyebilir miyim?**  
C: Topluluk desteği ve tartışmalar için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

**S: Aspose.CAD for Java için geçici lisanslar mevcut mu?**  
C: Evet, geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

**S: Aspose.CAD for Java için kapsamlı belgeleri nerede bulabilirim?**  
C: Ayrıntılı bilgi için [belgelere](https://reference.aspose.com/cad/java/) bakın.

---

**Son Güncelleme:** 2025-12-22  
**Test Edilen Versiyon:** Aspose.CAD 24.12 for Java  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}