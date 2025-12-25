---
date: 2025-12-25
description: DWG'yi BMP'ye dışa aktarmayı Aspose.CAD for Java ile öğrenin. Bu adım
  adım kılavuz, CAD çizim boyutunu ayarlamayı ve CAD'yi BMP'ye verimli bir şekilde
  dönüştürmeyi gösterir.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: DWG'yi BMP'ye Dışa Aktar – Birim Tipi Kullanarak CAD Boyutunu Ayarla (Java)
url: /tr/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi BMP'ye Dışa Aktarma – Aspose.CAD for Java ile Birim Türü Kullanarak CAD Çizim Boyutunu Ayarlama

## Giriş

**DWG'yi BMP'ye dışa aktarmanız** gerektiğinde, çıktı boyutunu ve ölçü birimini kontrol etmek, sonraki işlem veya baskı için çok önemlidir. Bu öğreticide, `UnitType` özelliğini kullanarak ölçü birimini tanımlayarak CAD çizim boyutunu nasıl ayarlayacağınızı ve CAD'i BMP'ye nasıl dönüştüreceğinizi Aspose.CAD for Java ile öğreneceksiniz. Adımlar sade bir dille açıklanmıştır, bu sayede kütüphaneye yeni olsanız bile rahatlıkla takip edebilirsiniz.

## Hızlı Yanıtlar
- **“DWG'yi BMP'ye dışa aktarmak” ne anlama geliyor?** DWG çizimini bir BMP raster görüntüsüne dönüştürmek.  
- **Çıktı boyutunu kontrol eden özellik hangisidir?** `CadRasterizationOptions.setUnitType()` birimi (ör. santimetre) ayarlar.  
- **Kodu çalıştırmak için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme sürümü yeterlidir; üretim ortamı için lisans gereklidir.  
- **Başka düzenler seçebilir miyim?** Evet, `setLayouts()` ile model veya kağıt alanı düzenlerini belirtebilirsiniz.  
- **Hangi çıktı formatları destekleniyor?** BMP dışında, seçenek sınıfını değiştirerek PNG, JPEG, TIFF vb. formatlara da dışa aktarabilirsiniz.

## **DWG'yi BMP'ye dışa aktarmak** nedir?

DWG'yi BMP'ye dışa aktarmak, vektör tabanlı bir DWG dosyasını bitmap (BMP) görüntüsüne rasterleştirmek anlamına gelir. Bu, eski sistemler, görüntü işleme hatları veya basit görüntüleme senaryoları için piksel‑tam bir temsil gerektiğinde faydalıdır.

## **Birim Türü** ile CAD çizim boyutunu ayarlamak neden önemlidir?

Birim türünü ayarlamak, ölçek faktörlerini manuel olarak hesaplamadan dışa aktarılan görüntünün fiziksel boyutlarını kontrol etmenizi sağlar. Bu, bitmap'in gerçek dünya ölçüleriyle (ör. santimetre) eşleşmesini garantileyerek mühendislik çizimleri ve basılı dokümantasyon için kritik bir adımdır.

## Ön Koşullar

Öğreticiye başlamadan önce aşağıdaki ön koşulların sağlandığından emin olun:

- **Java Geliştirme Ortamı** – Çalışır durumda bir JDK (8 veya üzeri) ve bir IDE ya da yapı aracı (Maven/Gradle).  
- **Aspose.CAD for Java Kütüphanesi** – Aspose.CAD kütüphanesini Java projenize indirin ve entegre edin. Kütüphaneyi [buradan](https://releases.aspose.com/cad/java/) edinebilirsiniz.

## İsim Uzaylarını İçe Aktarma

Java kodunuzda Aspose.CAD işlevlerine erişmek için gerekli isim uzaylarını ekleyin. Aşağıdaki import satırlarını ekleyin:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Şimdi, birim türü kullanarak CAD çizim boyutunu ayarlama sürecini yönetilebilir adımlara bölelim:

## Adım 1: Veri Dizinini Tanımlama

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

CAD dosyalarınızın bulunduğu dizinin yolunu ayarlayın.

## Adım 2: CAD Çizimini Yükleme

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Aspose.CAD'in `Image` sınıfını kullanarak CAD çizimini yükleyin.

## Adım 3: BMP Seçeneklerini Oluşturma

```java
BmpOptions bmpOptions = new BmpOptions();
```

CAD düzenini BMP formatına dışa aktarmak için `BmpOptions` sınıfının bir örneğini oluşturun.

## Adım 4: Rasterleştirme Seçeneklerini Yapılandırma

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

`CadRasterizationOptions` sınıfının bir örneğini oluşturun ve vektör rasterleştirme için `BmpOptions` ile ilişkilendirin.

## Adım 5: Birim Türünü Ayarlama

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

CAD çizimi için istenen birim türünü belirtin. Bu örnekte **Centimeter** (Santimetre) olarak ayarladık; bu, **CAD çizim boyutunu ayarlama** sırasında dışa aktarılan görüntü boyutunu doğrudan etkiler.

## Adım 6: Düzenleri Belirleme

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Dışa aktarım sırasında dikkate alınacak düzenleri tanımlayın. Bu örnekte **"Model"** düzenini seçtik, ancak ihtiyaç duyulursa kağıt alanı düzenlerine geçebilirsiniz.

## Adım 7: BMP'ye Dışa Aktarma

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Son olarak, değiştirilmiş CAD çizimini BMP formatında kaydedin. Bu adım, **DWG'yi BMP'ye dışa aktarma** iş akışını tamamlar ve yapılandırdığınız boyut ayarlarını korur.

## Yaygın Sorunlar ve Çözümleri

| Sorun | Sebep | Çözüm |
|-------|--------|-----|
| **Çıktı resmi çok küçük** | Birim türü ayarlanmamış veya varsayılan (piksel) kullanılmış | `setUnitType()` ile istenen ölçüyü (ör. `UnitType.Centimeter`) belirtin. |
| **Yanlış düzen dışa aktarıldı** | Düzen adı yazım hatası | Bir CAD görüntüleyicide düzen adlarını kontrol edin; `setLayouts()` içinde tam stringi kullanın. |
| **Lisans istisnası** | Üretimde geçerli bir lisans olmadan çalıştırma | SSS'de açıklandığı gibi geçici veya kalıcı bir lisans uygulayın. |

## Sıkça Sorulan Sorular (Genişletilmiş)

**S: Aspose.CAD for Java'yı başka programlama dilleriyle kullanabilir miyim?**  
C: Aspose.CAD öncelikle Java'yı destekler, ancak .NET gibi diğer diller için de sürümleri mevcuttur.

**S: Aspose.CAD için lisans seçenekleri var mı?**  
C: Evet, lisans seçeneklerini inceleyebilir ve Aspose.CAD'i [buradan](https://purchase.aspose.com/buy) satın alabilirsiniz.

**S: Aspose.CAD için ücretsiz deneme mevcut mu?**  
C: Elbette, ücretsiz deneme sürümüne [buradan](https://releases.aspose.com/) ulaşabilirsiniz.

**S: Aspose.CAD for Java için destek nasıl alınır?**  
C: Kapsamlı destek için Aspose.CAD forumuna [buradan](https://forum.aspose.com/c/cad/19) göz atabilirsiniz.

**S: Aspose.CAD için geçici bir lisans alabilir miyim?**  
C: Evet, geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) temin edebilirsiniz.

---

**Son Güncelleme:** 2025-12-25  
**Test Edilen Sürüm:** Aspose.CAD for Java 24.10  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}