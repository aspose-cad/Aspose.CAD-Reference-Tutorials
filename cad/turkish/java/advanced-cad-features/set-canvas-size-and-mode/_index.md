---
date: 2026-02-15
description: Aspose.CAD for Java kullanarak PDF sayfa boyutunu nasıl ayarlayacağınızı
  ve CAD'i PDF'ye nasıl dönüştüreceğinizi öğrenin; otomatik düzen ölçeklendirme ve
  TIFF dışa aktarımıyla.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: PDF Sayfa Boyutunu Ayarla – CAD'i PDF'ye Dönüştür (Java)
url: /tr/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tuval Boyutunu ve Modunu Ayarlama

## Giriş

CAD çizimlerini PDF'ye dönüştürürken **PDF sayfa boyutunu ayarlamanız** gerekiyorsa doğru yerdesiniz. Bu öğreticide Aspose.CAD for Java'yı kullanarak tam tuval boyutlarını nasıl tanımlayacağınızı, otomatik yerleşim ölçeklendirmesini nasıl etkinleştireceğinizi ve ardından sonucu PDF ve TIFF olarak nasıl dışa aktaracağınızı göstereceğiz. Mühendislik şemalarını baskı için hazırlıyor ya da bir web galerisinde küçük önizlemeler oluşturuyorsanız, sayfa boyutunu ve çıktı çözünürlüğünü kontrol etmek çok önemlidir.

## Hızlı Yanıtlar
- **“CAD'i PDF'ye dönüştürmek” ne anlama geliyor?** Bir CAD çizimini (ör. DXF, DWG) herhangi bir platformda görüntülenebilen bir PDF belgesine dönüştürmek.  
- **TIFF olarak da dışa aktarabilir miyim?** Evet—yüksek çözünürlüklü raster görüntüler oluşturmak için `TiffOptions` kullanın.  
- **Java'da tuval boyutunu kontrol eden seçenek hangisidir?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Otomatik yerleşim ölçeklendirmesi nedir?** Tuval boyutu değiştiğinde orijinal yerleşim oranlarını koruyan bir bayrak (`setAutomaticLayoutsScaling(true)`).  
- **Aspose.CAD için bir lisansa ihtiyacım var mı?** Üretim kullanımında geçici veya kalıcı bir lisans gereklidir.

## CAD'i PDF'ye Dönüştürürken PDF Sayfa Boyutunu Nasıl Ayarlarsınız (Java)

PDF sayfa boyutunu (veya tuval boyutunu) ayarlamak, belgeyi istediğiniz nihai boyutlarda oluşturmanızı sağlar; bu, PDF boyutlarını baskı standartlarına veya UI gereksinimlerine göre **değiştirmeniz** gerektiğinde özellikle faydalıdır. Aşağıda her adımı, kod satırlarının *neden*ini açıklayarak ilerliyoruz.

## **convert CAD to PDF** nedir?

CAD'i PDF'ye dönüştürmek, vektör tabanlı mühendislik çizimlerini PDF sayfaları olarak render etmek, çizgi çalışması, katmanlar ve geometrileri korurken dosyayı evrensel olarak erişilebilir hâle getirmek anlamına gelir.

## **java**'da tuval boyutu neden ayarlanmalı?

Java'da tuval boyutunu ayarlamak, çıktı çözünürlüğünü ve sayfa boyutlarını tanımlamanızı sağlar; böylece oluşturulan PDF veya TIFF, baskı ya da görüntüleme gereksinimlerinize tam olarak uyar. Ayrıca ölçeklendirme davranışı üzerinde kontrol sunar; bu büyük formatlı çizimler için kritiktir.

## Ön Koşullar

Öğreticiye başlamadan önce aşağıdaki ön koşulların sağlandığından emin olun:

- Aspose.CAD for Java: Java ortamınıza Aspose.CAD kütüphanesinin kurulu olduğundan emin olun. Kütüphaneyi [buradan](https://releases.aspose.com/cad/java/) indirebilirsiniz.  
- Belge Dizini: CAD dosyalarınızı saklayacağınız bir belge dizini oluşturun. Bu dizin öğreticideki adımlarda referans alınacaktır.

Şimdi adım adım kılavuza geçelim.

## Ad Alanlarını İçe Aktarma

Bu adımda Aspose.CAD projenizi başlatmak için gerekli ad alanlarını içe aktaracağız.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Adım 1: Aspose.CAD Sınıflarını İçe Aktarma

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Bu kod parçasında, kaynak dizini yolunu ayarlıyor ve Aspose.CAD'in `Image` sınıfını kullanarak bir DXF dosyasını yüklüyoruz.

## Adım 2: **CadRasterizationOptions** Özelliklerini Ayarlama (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Burada bir `CadRasterizationOptions` örneği oluşturup sayfa genişliği, sayfa yüksekliği ve **otomatik yerleşim ölçeklendirmesi** gibi özellikleri yapılandırıyoruz. Bu, dönüşümünüz için **tuval modunu yapılandırmanın** temelidir.

## Adım 3: PdfOptions Oluşturma ve VectorRasterizationOptions Ayarlama

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Şimdi bir `PdfOptions` örneği oluşturup, daha önce yapılandırdığımız `CadRasterizationOptions` nesnesini `VectorRasterizationOptions` özelliği olarak atıyoruz.

## Adım 4: PDF Olarak Dışa Aktarma (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Son olarak, belirtilen seçeneklerle CAD görüntüsünü bir PDF dosyasına kaydediyoruz ve **CAD'i PDF'ye dönüştürme** sürecini tamamlıyoruz.

## Adım 5: TiffOptions Oluşturma ve VectorRasterizationOptions Ayarlama (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Bu adımda bir `TiffOptions` örneği oluşturup `VectorRasterizationOptions` özelliğini yapılandırıyoruz.

## Adım 6: TIFF Olarak Dışa Aktarma

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Son olarak, belirtilen seçeneklerle CAD görüntüsünü bir TIFF dosyasına kaydediyoruz; bu, tuval boyutu yapılandırıldıktan sonra **CAD'i TIFF olarak dışa aktarma** örneğidir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Sebep | Çözüm |
|-------|-------|------|
| Çıktı PDF boş | `setNoScaling(true)` bazı çizimler için renderlamayı devre dışı bırakıyor | `setNoScaling(true)` ifadesini kaldırın veya `false` olarak ayarlayın. |
| TIFF çözünürlüğü düşük | Sayfa genişliği/yüksekliği çok küçük | `setPageWidth` / `setPageHeight` değerlerini artırın. |
| Yerleşim bozulmuş | Otomatik yerleşim ölçeklendirmesi devre dışı | `setAutomaticLayoutsScaling(true)` etkin olduğundan emin olun. |

## Neden Tuval Boyutu ve DPI Ayarlanmalı?

Tuval boyutunu değiştirmek, çıktının rasterizasyon çözünürlüğünü doğrudan etkiler. **TIFF çözünürlüğünü artırmanız** gerekiyorsa, sadece `setPageWidth` / `setPageHeight` değerlerini yükseltin ya da `TiffOptions` oluşturmadan önce `rasterizationOptions.setResolution(300)` çağrısını yapın. Bu, baskı ya da detaylı inceleme için yüksek kaliteli raster görüntüler sağlar.

## Sık Sorulan Sorular

### S1: Aspose.CAD for Java'yı diğer Java çerçeveleriyle kullanabilir miyim?

C1: Evet, Aspose.CAD çeşitli Java çerçeveleriyle sorunsuz bir şekilde bütünleşecek şekilde tasarlanmıştır.

### S2: Aspose.CAD için geçici bir lisans mevcut mu?

C2: Evet, geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

### S3: Aspose.CAD için topluluk desteği nereden alınır?

C3: Topluluk desteği ve tartışmalar için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

### S4: Aspose.CAD'ı ücretsiz deneyebilir miyim?

C4: Kesinlikle! Ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) edinebilirsiniz.

### S5: Aspose.CAD for Java'yı nasıl satın alabilirim?

C5: Ürünü [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

**Ek Soru‑Cevap**

**S: Tuval boyutu PDF'deki vektör kalitesini etkiler mi?**  
C: Hayır. Tuval boyutu sayfa boyutlarını kontrol eder; vektör verileri çözünürlükten bağımsızdır ve herhangi bir yakınlaştırma seviyesinde net render sağlar.

**S: TIFF çıktısı için farklı bir DPI ayarlayabilir miyim?**  
C: Evet. `TiffOptions` oluşturmadan önce `rasterizationOptions.setResolution(dpiValue)` ifadesini ayarlayın.

**S: CAD'i yeniden render etmeden mevcut bir PDF'in **PDF boyutlarını değiştirmek** nasıl yapılır?**  
C: Aspose.PDF kullanarak oluşturulan PDF'i yükleyin ve `pdf.getPages().setPageSize(PageSize.A4)` ya da özel bir boyut çağrısı yapın.

**S: Katmanları koruyarak **dxf'i pdf'ye dönüştürmenin** en iyi yolu nedir?**  
C: `setAutomaticLayoutsScaling(true)` tutun ve `setNoScaling(true)` kullanmaktan kaçının; bu, katman görünürlüğünü ve yerleşim bütünlüğünü korur.

## Sonuç

Tebrikler! **CAD'i PDF'ye dönüştürme** ve **CAD'i TIFF olarak dışa aktarma** işlemlerini **java’da tuval boyutunu ayarlama**, **otomatik yerleşim ölçeklendirmesini etkinleştirme** ve **tuval modunu yapılandırma** konularını öğrenerek başarıyla tamamladınız. Bu öğretici, CAD dönüşüm projeleriniz için sağlam bir temel sunar. Daha fazla özellik ve olasılık keşfetmek için [Aspose.CAD belgelerine](https://reference.aspose.com/cad/java/) göz atın.

---

**Son Güncelleme:** 2026-02-15  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.12  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}