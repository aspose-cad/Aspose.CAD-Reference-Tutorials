---
date: 2026-01-10
description: Bu adım adım öğreticide, Aspose.CAD for Java kullanarak DWG dosyalarını
  nasıl okuyacağınızı ve çoklu lider DWG varlıklarını nasıl oluşturacağınızı öğrenin.
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: DWG Dosyalarını Okuma ve Aspose.CAD for Java ile MLeader Desteği
url: /tr/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi Okumak ve Aspose.CAD for Java ile MLeader'ı Desteklemek

## Giriş

Java uygulamasında **DWG** dosyalarını okumak ve **multileader DWG** varlıklarıyla çalışmak istiyorsanız doğru yerdesiniz. Aspose.CAD for Java, DWG çizimlerini açmak, MLeader nesnelerini incelemek ve özelliklerini doğrulamak için tam donanımlı bir CAD istasyonuna ihtiyaç duymadan temiz, programatik bir yol sunar. Bu öğreticide, bir DWG dosyasını yüklemekten çoklayıcı lider verilerinin beklenen stile uygunluğunu onaylamaya kadar her adımı adım adım göstereceğiz.

## Hızlı Yanıtlar
- **“dwg nasıl okunur” neyi kapsar?** DWG'yi `Image.load()` ile yükleyip `CadImage`'a dönüştürmek.
- **Multileader dwg varlıkları oluşturabilir miyim?** Evet – CadMLeader API'si ile MLeader nesnelerini ekleyebilir, düzenleyebilir ve doğrulayabilirsiniz.
- **Hangi kütüphane sürümü gereklidir?** 2024+ sürümleriyle çalışan herhangi bir güncel Aspose.CAD for Java sürümü.
- **Geliştirme için lisansa ihtiyacım var mı?** Test için geçici bir lisans yeterli; üretim için tam lisans gereklidir.
- **Kod çapraz‑platform mu?** Kesinlikle – Java Windows, Linux ve macOS'ta çalışır.

## Aspose.CAD ile “dwg nasıl okunur” nedir?

DWG dosyasını okumak, ikili çizimi bellekte bir `CadImage` nesnesine dönüştürmek anlamına gelir. Bu nesneye sahip olduğunuzda, varlıklarını (çizgiler, daireler, metin, **MLeader** nesneleri vb.) sıralayabilir ve özelliklerini inceleyebilirsiniz.

## Neden MLeader varlıklarını desteklemek?

MLeader (multileader) nesneleri, lider çizgilerini ekli metin veya bloklarla birleştirir ve mühendislik çizimlerinde açıklamalar için vazgeçilmezdir. Bunları desteklemek şunları sağlar:

- Açıklamaların şirket standartlarına uygunluğunu doğrulama.
- Metni sonraki işlemler için çıkarma (ör. BOM oluşturma).
- Lider stillerini programatik olarak değiştirme veya blok içeriğini değiştirme.

## Önkoşullar

İlerlemeye başlamadan önce şunların kurulu olduğundan emin olun:

1. **Java Geliştirme Ortamı** – JDK 11+ ve tercih ettiğiniz IDE (IntelliJ, Eclipse, VS Code).  
2. **Aspose.CAD for Java** – En son JAR dosyasını [indirme bağlantısı](https://releases.aspose.com/cad/java/) üzerinden indirin.  

## İsim Uzaylarını İçe Aktarın

DWG varlıkları ve rasterleştirme seçenekleriyle çalışabilmek için Java sınıfınıza aşağıdaki içe aktarmaları ekleyin:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Aspose.CAD for Java ile DWG Dosyalarını Okuma

### Adım 1: DWG dosyasını yükleyin ve bir `CadImage` alın

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### Adım 2: Çizimin MLeader varlıkları içerdiğini doğrulayın

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### Adım 3: MLeader stilini ve temel öznitelikleri doğrulayın

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### Adım 4: MLeader bağlam verilerine erişin (multileader'ın kalbi)

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### Adım 5: Bağlam‑seviyesi öznitelikleri doğrulayın

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### Adım 6: MLeader düğümü ve onun lider çizgisiyle çalışın

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

### Adım 7: Ek MLeader düğüm özniteliklerini doğrulayın

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### Adım 8: Metin‑ile ilgili özellikleri kontrol edin

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### Adım 9: Tamamlayıcılık için diğer MLeader özniteliklerini gözden geçirin

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden Oluşur | Çözüm |
|-------|--------------|-------|
| `ClassCastException` varlık dönüştürülürken | Seçilen indeks bir MLeader nesnesi değildir. | Dönüştürmeden önce `cadImage.getEntities()[i] instanceof CadMLeader` kontrol edin. |
| Lider çizgi noktaları için `null` değerler | Çizim, tam olarak desteklenmeyen özel bir lider stili kullanıyor. | En yeni Aspose.CAD sürümünü kullanın veya test için varsayılan stile geri dönün. |
| Sayısal değerlerde doğrulama hataları | CAD sürümleri arasındaki hafif yuvarlama farkları. | Örneklerde gösterildiği gibi `Assert.areEqual(..., delta)` toleransını ayarlayın. |

## Sık Sorulan Sorular

**S: Aspose.CAD for Java'yi diğer CAD formatlarıyla kullanabilir miyim?**  
C: Evet, Aspose.CAD DWG'nin yanı sıra DXF, DWF, DGN ve çeşitli raster formatlarını da destekler.

**S: Aspose.CAD for Java için ayrıntılı belgeleri nereden bulabilirim?**  
C: API detayları ve kod örnekleri için resmi [belgelere](https://reference.aspose.com/cad/java/) bakın.

**S: Ücretsiz deneme sürümü mevcut mu?**  
C: Kesinlikle – [ücretsiz deneme](https://releases.aspose.com/) sayfasından bir deneme sürümü indirebilirsiniz.

**S: Test için geçici bir lisans nasıl alabilirim?**  
C: [Geçici lisans bağlantısı](https://purchase.aspose.com/temporary-license/) üzerinden geçici bir lisans edinin.

**S: Toplulukta yardım almak için nereden sorabilirim?**  
C: Sorularınızı ve çözümlerinizi paylaşmak için en iyi yer [Aspose.CAD forumu](https://forum.aspose.com/c/cad/19)'dur.

## Sonuç

Artık **dwg nasıl okunur** ve **multileader DWG** varlıkları oluşturulur** konularında Aspose.CAD for Java kullanarak eksiksiz, uçtan uca bir yol haritasına sahipsiniz. Yukarıdaki adımları izleyerek MLeader stillerini doğrulayabilir, açıklama verilerini çıkarabilir ve DWG işleme yeteneklerini herhangi bir Java‑tabanlı iş akışına entegre edebilirsiniz.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Son Güncelleme:** 2026-01-10  
**Test Edilen:** Aspose.CAD 24.11 for Java  
**Yazar:** Aspose