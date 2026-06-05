---
date: 2026-01-17
description: Aspose.CAD kullanarak Java’da DWG dosyaları için ağ desteğini nasıl etkinleştireceğinizi
  ve DWG’yi PDF’ye nasıl dönüştüreceğinizi öğrenin. Sorunsuz 3D çizim manipülasyonu
  için adım adım rehber.
linktitle: Convert DWG to PDF with Mesh Support in Java
second_title: Aspose.CAD Java API
title: Java'da Mesh Desteğiyle DWG'yi PDF'ye Dönüştür
url: /tr/java/dwg-file-operations/mesh-support-for-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mesh Desteğiyle Java’da DWG’yi PDF’ye Dönüştürme

## Giriş

Java’da DWG dosyalarıyla çalışmak genellikle karmaşık 3‑B geometrisini koruyarak **DWG'yi PDF'ye dönüştürmeniz** gerektiği anlamına gelir. Mesh desteğini etkinleştirmek, PolyFaceMesh ve PolygonMesh gibi 3‑B varlıkların dönüşümden önce doğru şekilde yorumlanmasını sağladığı için kritik bir adımdır. Bu öğreticide Aspose.CAD for Java kullanarak mesh desteğini nasıl etkinleştireceğinizi adım adım gösterecek ve bu hazırlığın sonraki *DWG'yi PDF'ye dönüştürme* işlemini nasıl güvenilir ve doğru hale getirdiğini göstereceğiz.

## Hızlı Yanıtlar
- **DWG'yi doğrudan PDF'ye dönüştürebilir miyim?** Evet, mesh desteğini etkinleştirdikten sonra DWG'yi rasterleştirebilir veya PDF olarak dışa aktarabilirsiniz.
- **Aspose.CAD için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme çalışır; üretim için ticari lisans gereklidir.
- **Hangi Java sürümü gerekiyor?** Java 8 veya üzeri.
- **Mesh varlıkları PDF'de korunacak mı?** Mesh desteğini etkinleştirmek, köşelerin işlenmesini sağlar, böylece PDF orijinal 3‑B geometrisini yansıtır.
- **Ek yapılandırma gerekli mi?** Yalnızca standart Aspose.CAD kurulumu ve kaynakların doğru şekilde serbest bırakılması.

## DWG için mesh desteği nedir?

Mesh desteği, Aspose.CAD'in 3‑B yüzeyleri tanımlayan mesh tabanlı varlıkları (PolyFaceMesh ve PolygonMesh) tanımasını ve işlemesini sağlar. Bu destek olmadan, bu varlıklar daha sonra **DWG'yi PDF'ye dönüştürdüğünüzde** göz ardı edilebilir veya hatalı renderlanabilir.

## DWG'yi PDF'ye dönüştürmeden önce neden mesh desteği etkinleştirilmeli?

- **Doğru 3‑B temsili** – Mesh köşeleri korunur, böylece PDF istenen geometriyi gösterir.
- **Azaltılmış son‑işlem** – Dönüştürmeden sonra daha az manuel düzeltme gerekir.
- **Daha iyi performans** – Mesh'ler açıkça etkinleştirildiğinde Aspose.CAD mesh'leri verimli bir şekilde işler.

## Önkoşullar

İçeriğe başlamadan önce şunların yüklü olduğundan emin olun:

- Java Development Kit (JDK) yüklü.
- Aspose.CAD for Java kütüphanesi indirilmiş ve projenize eklenmiş. Kütüphaneyi [burada](https://releases.aspose.com/cad/java/) bulabilirsiniz.
- Java programlamaya temel bir anlayış.

## Paketleri İçe Aktarma

Başlamak için gerekli paketleri Java projenize içe aktarın. Bu paketler, Aspose.CAD for Java işlevlerine erişmenizi sağlar.

```java
import com.aspose.cad.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import java.awt.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.polylines.CadPolyFaceMesh;
import com.aspose.cad.fileformats.cad.cadobjects.polylines.CadPolygonMesh;
import java.util.ArrayList;
import java.util.List;
```

## Adım 1: DWG Dosyasını Yükleme

DWG dosyasını Aspose.CAD for Java kullanarak yükleyin. Doğru dosya yoluna sahip olduğunuzdan ve dosyanın mevcut olduğundan emin olun.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "meshes.dwg";
// com.aspose.cad. objImage = com.aspose.cad.CImage.load(srcFile);
CadImage cadImage =(CadImage) com.aspose.cad.Image.load(srcFile);;
```

## Adım 2: Varlıklar Üzerinde Döngü

Yüklenen DWG dosyasındaki varlıklar üzerinde döngü yapın. Aspose.CAD, farklı CAD öğelerini temsil eden çeşitli varlık sınıfları sunar.

```java
for (CadBaseEntity entity : cadImage.getEntities())
{
    // Check if the entity is a PolyFaceMesh
    if (entity instanceof CadPolyFaceMesh)
    {
        CadPolyFaceMesh asFaceMesh = (CadPolyFaceMesh)entity;
        if (asFaceMesh != null)
        {
            System.out.println("Vertices count: " + asFaceMesh.getMeshMVertexCount());
        }
    }
    // Check if the entity is a PolygonMesh
    else if (entity instanceof CadPolygonMesh)
    {
        CadPolygonMesh asPolygonMesh = (CadPolygonMesh)entity;
        if (asPolygonMesh != null)
        {
            System.out.println("Vertices count: " + asPolygonMesh.getMeshMVertexCount());
        }
    }
}
```

## Adım 3: Kaynakları Serbest Bırakma

Kullanım sonrası CadImage nesnesini serbest bırakarak doğru kaynak yönetimini sağlayın.

```java
finally
{
    cadImage.dispose();
}
```

## Mesh Desteği Etkinleştirildikten Sonra DWG'yi PDF'ye Nasıl Dönüştürülür

Mesh desteği etkinleştirildikten ve mesh varlıklarını doğruladıktan sonra DWG'yi PDF'ye dönüştürmek basittir:

1. **Rasterleştirme seçeneklerini yapılandırın** (ör. sayfa boyutu, arka plan rengi).  
2. **Bir `PdfOptions` örneği oluşturun** ve rasterleştirme ayarlarını atayın.  
3. **`cadImage.save(outputPath, pdfOptions)`** metodunu çağırarak PDF'yi oluşturun.

*Not:* Gerçek dönüşüm kodu burada mesh desteğine odaklanmak için çıkarılmıştır, ancak yukarıdaki adımlar dönüşümün iş akışındaki yerini gösterir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| Köşeler yazdırılmadı | Mesh varlıkları tanınmadı | En son Aspose.CAD sürümünü kullandığınızdan ve DWG'nin gerçekten mesh verisi içerdiğinden emin olun. |
| `cadImage` null | Yanlış dosya yolu | `srcFile`'ın geçerli bir DWG dosyasına işaret ettiğini doğrulayın. |
| PDF çıktısında 3‑B veri eksik | Mesh desteği etkinleştirilmedi | Dönüştürmeden önce mesh varlıklarını döngüyle kontrol edip doğrulamak için yukarıdaki adımları izleyin. |

## Sıkça Sorulan Sorular

**S: Aspose.CAD for Java'yi diğer CAD dosya formatlarıyla kullanabilir miyim?**  
C: Evet, Aspose.CAD DWG, DXF, DGN ve daha fazlası dahil olmak üzere çeşitli CAD formatlarını destekler.

**S: Aspose.CAD for Java için ayrıntılı belgeleri nerede bulabilirim?**  
C: Belgeleri [burada](https://reference.aspose.com/cad/java/) bulabilirsiniz.

**S: Aspose.CAD for Java için ücretsiz bir deneme mevcut mu?**  
C: Evet, ücretsiz denemeye [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

**S: Aspose.CAD for Java için geçici lisans nasıl alabilirim?**  
C: Geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) edinebilirsiniz.

**S: Yardıma ihtiyacınız var mı ya da sorularınız mı var?**  
C: Özel destek için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

---

**Son Güncelleme:** 2026-01-17  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.12 (yazım zamanındaki en yeni)  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}