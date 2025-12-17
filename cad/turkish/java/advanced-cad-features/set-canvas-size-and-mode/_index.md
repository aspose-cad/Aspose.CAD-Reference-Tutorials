---
date: 2025-12-10
description: Aspose.CAD for Java kullanarak CAD'i PDF'ye dönüştürmeyi, tuval boyutunu
  ayarlamayı, otomatik yerleşim ölçeklendirmesini ve TIFF olarak dışa aktarmayı öğrenin.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: CAD'yi PDF'ye Dönüştür – Tuval Boyutunu ve Modunu Ayarla (Java)
url: /tr/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tuval Boyutunu ve Modunu Ayarlama

## Giriş

Tuval boyutu ve renderleme modu üzerinde tam kontrol sağlarken **convert CAD to PDF** yapmak mı istiyorsunuz? Bu kapsamlı rehber, Java'da tuval boyutunu ayarlama, otomatik düzen ölçeklendirmesini etkinleştirme ve ardından sonucu Aspose.CAD kullanarak PDF ve TIFF formatlarında dışa aktarma adımlarını size gösterir. Üretim hattını iyileştiriyor ya da bir prototiple deneme yapıyor olun, burada net ve uygulanabilir talimatlar bulacaksınız.

## Hızlı Yanıtlar
- **convert CAD to PDF** ne anlama geliyor? Bir CAD çizimini (ör. DXF, DWG) herhangi bir platformda görüntülenebilen bir PDF belgesine dönüştürmek.  
- **TIFF olarak da dışa aktarabilir miyim?** Evet—yüksek çözünürlüklü raster görüntüler oluşturmak için `TiffOptions` kullanın.  
- **Java'da tuval boyutunu kontrol eden seçenek hangisidir?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Otomatik düzen ölçeklendirme nedir?** Tuval boyutu değiştiğinde orijinal düzen oranlarını koruyan bir işaretçi (`setAutomaticLayoutsScaling(true)`).  
- **Aspose.CAD için bir lisansa ihtiyacım var mı?** Üretim kullanımında geçici veya kalıcı bir lisans gereklidir.

## **convert CAD to PDF** nedir?

CAD'i PDF'e dönüştürmek, vektör tabanlı mühendislik çizimlerini PDF sayfaları olarak render etmek, çizgi çalışması, katmanlar ve geometriyi korurken dosyayı evrensel olarak erişilebilir hâle getirmek anlamına gelir.

## Neden **java**'da tuval boyutunu ayarlamalısınız?

Java'da tuval boyutunu ayarlamak, çıktı çözünürlüğünü ve sayfa boyutlarını tanımlamanızı sağlar; böylece ortaya çıkan PDF veya TIFF, baskı veya görüntüleme gereksinimlerinize uyar. Ayrıca ölçekleme davranışı üzerinde kontrol sağlar; bu, büyük formatlı çizimler için esastır.

## Önkoşullar

Öğreticiye başlamadan önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

- Aspose.CAD for Java: Java ortamınıza Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. **[buradan](https://releases.aspose.com/cad/java/)** indirebilirsiniz.

- Belge Dizini: CAD dosyalarınızı depolamak için bir belge dizini oluşturun. Bu dizin öğretici adımlarında referans alınacaktır.

Şimdi adım adım kılavuza başlayalım.

## Namespace'leri İçe Aktarın

Bu adımda, Aspose.CAD projenizi başlatmak için gerekli namespace'leri içe aktaracağız.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Adım 1: Aspose.CAD Sınıflarını İçe Aktarın

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Bu kod parçacığında, kaynak dizinine giden yolu ayarlıyor ve Aspose.CAD'in `Image` sınıfını kullanarak bir DXF dosyasını yüklüyoruz.

## Adım 2: **CadRasterizationOptions** Özelliklerini Ayarlayın (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Burada bir `CadRasterizationOptions` örneği oluşturuyor ve sayfa genişliği, sayfa yüksekliği ve **automatic layout scaling** gibi özellikleri yapılandırıyoruz. Bu, dönüşümünüz için **configure canvas mode**'un temelini oluşturur.

## Adım 3: PdfOptions Oluşturun ve VectorRasterizationOptions Ayarlayın

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Şimdi bir `PdfOptions` örneği oluşturuyor ve `VectorRasterizationOptions` özelliğini önceden yapılandırılmış `CadRasterizationOptions` nesnesine ayarlıyoruz.

## Adım 4: PDF Olarak Dışa Aktar (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Son olarak, belirtilen seçenekleri kullanarak CAD görüntüsünü bir PDF dosyasına kaydediyoruz ve **convert CAD to PDF** sürecini tamamlıyoruz.

## Adım 5: TiffOptions Oluşturun ve VectorRasterizationOptions Ayarlayın (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Bu adımda bir `TiffOptions` örneği oluşturuyor ve `VectorRasterizationOptions` özelliğini yapılandırıyoruz.

## Adım 6: TIFF Olarak Dışa Aktar

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Son olarak, belirtilen seçenekleri kullanarak CAD görüntüsünü bir TIFF dosyasına kaydediyoruz; bu, tuval boyutu yapılandırıldıktan sonra **export CAD to TIFF** nasıl yapılır gösterir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|-------|-----|
| Çıktı PDF boş | `setNoScaling(true)` bazı çizimler için renderlamayı devre dışı bırakır | `setNoScaling(true)` ifadesini kaldırın veya `false` olarak ayarlayın. |
| TIFF çözünürlüğü düşük görünüyor | Sayfa genişliği/yüksekliği çok küçük | `setPageWidth` / `setPageHeight` değerlerini artırın. |
| Düzen bozulmuş | Otomatik düzen ölçeklendirme devre dışı | `setAutomaticLayoutsScaling(true)` işaretçisinin etkin olduğundan emin olun. |

## Sonuç

Tebrikler! **convert CAD to PDF** ve **export CAD to TIFF** işlemlerini **set canvas size java** yaparken, **automatic layout scaling**'i etkinleştirerek ve yüksek kaliteli çıktılar için **configure canvas mode**'u öğrenerek başarıyla tamamladınız. Bu öğretici, CAD dönüşüm projeleriniz için sağlam bir temel sağlar. Daha fazla özellik ve olasılık keşfetmek için [Aspose.CAD documentation](https://reference.aspose.com/cad/java/) sayfasına göz atın.

## SSS

### Q1: Aspose.CAD for Java'yı diğer Java çerçeveleriyle kullanabilir miyim?

A1: Evet, Aspose.CAD çeşitli Java çerçeveleriyle sorunsuz entegrasyon için tasarlanmıştır.

### Q2: Aspose.CAD için geçici bir lisans mevcut mu?

A2: Evet, **[buradan](https://purchase.aspose.com/temporary-license/)** geçici bir lisans alabilirsiniz.

### Q3: Aspose.CAD için topluluk desteği nereden alınabilir?

A3: Topluluk desteği ve tartışmalar için **[Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19)** ziyaret edin.

### Q4: Aspose.CAD'ı ücretsiz deneyebilir miyim?

A4: Kesinlikle! **[Buradan](https://releases.aspose.com/)** ücretsiz deneme alabilirsiniz.

### Q5: Aspose.CAD for Java'yı nasıl satın alabilirim?

A5: Ürünü **[buradan](https://purchase.aspose.com/buy)** satın alabilirsiniz.

**Ek Soru&Cevap**

**S: Tuval boyutu PDF'teki vektör kalitesini etkiler mi?**  
C: Hayır. Tuval boyutu sayfa boyutlarını kontrol eder; vektör verisi çözünürlükten bağımsız kalır ve herhangi bir yakınlaştırma seviyesinde net render sağlar.

**S: TIFF çıktısı için farklı bir DPI ayarlayabilir miyim?**  
C: Evet. `TiffOptions` oluşturmadan önce `rasterizationOptions.setResolution(dpiValue)` ifadesini ayarlayın.

---

**Son Güncelleme:** 2025-12-10  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}