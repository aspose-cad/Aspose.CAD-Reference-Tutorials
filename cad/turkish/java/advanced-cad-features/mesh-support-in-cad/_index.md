---
date: 2025-12-09
description: Aspose.CAD for Java kullanarak DWG dosyalarından PDF oluşturmayı öğrenin.
  Mesh desteğiyle DWG'yi PDF'ye zahmetsizce dönüştürün.
linktitle: Mesh Support in CAD
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java ile DWG'den PDF Oluştur
url: /tr/java/advanced-cad-features/mesh-support-in-cad/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'den PDF Oluşturma Aspose.CAD for Java

## Introduction

Bu öğreticide **DWG dosyalarından PDF oluşturmayı** Aspose.CAD for Java kullanarak öğreneceksiniz. Kütüphanenin ağ desteği, karmaşık CAD çizimlerini—3‑B ağlar içerenleri—doğrudan PDF'ye kayıpsız dönüştürmenizi sağlar. Raporlama, arşivleme veya sonraki işleme için **DWG'yi PDF'ye dönüştürmeniz** gerektiğinde, aşağıdaki adımlar güvenilir, üretim‑hazır bir çözüm sunar.

## Quick Answers
- **Bu öğretici neyi kapsıyor?** Ağ içeren bir DWG dosyasını Aspose.CAD for Java kullanarak PDF'ye dönüştürmek.  
- **Lisans gerekli mi?** Test için geçici bir lisans yeterlidir; ticari kullanım için tam lisans gerekir.  
- **Hangi Java sürümü destekleniyor?** Java 8 ve üzeri.  
- **Başka formatları dışa aktarabilir miyim?** Evet – Aspose.CAD PNG, JPEG, BMP ve daha fazlasını destekler.  
- **Dönüşüm ne kadar sürer?** Standart‑boyutlu çizimler için genellikle bir saniyeden az.

## DWG'den PDF Nasıl Oluşturulur?

Aşağıda, projeyi kurmaktan son PDF'yi kaydetmeye kadar tüm süreci adım adım anlatan kısa bir rehber bulacaksınız.

## Prerequisites

- **Java Geliştirme Ortamı:** Makinenizde JDK 8 veya daha yeni bir sürüm yüklü olmalıdır.  
- **Aspose.CAD for Java Kütüphanesi:** En son JAR dosyasını [download link](https://releases.aspose.com/cad/java/) adresinden indirin.  
- **Ağ İçeren Belge:** Ağ verisi içeren bir DWG dosyası (ör. `meshes.dwg`).  

## Import Namespaces

Java kaynak dosyanızda, gerekli Aspose.CAD sınıflarını dahil edin:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Step 1: Set Up the Project

Yeni bir Java projesi oluşturun (veya mevcut bir projeye ekleyin) ve Aspose.CAD JAR dosyasını projenin sınıf yoluna ekleyin. Kaynak DWG dosyanızı ve oluşturulan PDF'yi tutacak bir temel dizin tanımlayın.

## Step 2: Define File Paths

Giriş DWG dosyasının nerede bulunduğunu ve çıkış PDF'nin nereye yazılacağını belirtin.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "meshes.dwg";
String outPath = dataDir + "meshes.pdf";
```

## Step 3: Load the CAD Image

DWG dosyasını bir `CadImage` nesnesine yükleyin, böylece Aspose.CAD iç yapısıyla çalışabilir.

```java
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Step 4: Configure Rasterization Options

Oluşturulan PDF sayfalarının boyut ve düzenini kontrol eden rasterleştirme seçeneklerini ayarlayın. `Layouts` dizisi, Aspose.CAD'in ağ varlıklarını içeren **Model** alanını render etmesini sağlar.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## Step 5: Set PDF Options

Rasterleştirme ayarlarını bir `PdfOptions` örneğine ekleyin. Bu, kütüphaneye PDF üretirken önceden tanımlanan seçenekleri kullanmasını söyler.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 6: Save the PDF

Son olarak, yüklenen CAD görüntüsünü PDF dosyası olarak kaydedin. Oluşan belge, orijinal DWG'nin, ağ geometrisi dahil, eksiksiz bir temsilini içerecektir.

```java
cadImage.save(outPath, pdfOptions);
```

### Why this works for **convert CAD to PDF**

Aspose.CAD, vektör tabanlı rasterleştirme yapar ve çizgi kalınlıklarını, renkleri ve 3‑B ağ detaylarını korur. Rasterleştirme seçeneklerini yapılandırarak çözünürlük ve düzeni kontrol edersiniz, böylece **CAD çiziminin dışa aktarımı** PDF'de tam olarak istediğiniz gibi görünür.

## Common Use Cases

- **Otomatik raporlama:** Mühendislik çizimlerinden anlık PDF raporları oluşturun.  
- **Belge arşivleme:** CAD çizimlerini uzun vadeli saklama için PDF olarak depolayın.  
- **Web hizmetleri:** DWG yüklemelerini kabul edip PDF dönen bir API sunun, SaaS platformları için faydalıdır.  

## Troubleshooting Tips

- **Çıktıda ağ eksik:** `Layouts` özelliğinin `"Model"` içerdiğini doğrulayın; ağlar genellikle model alanında depolanır.  
- **Yanlış ölçekleme:** Çizimin yerel birimlerine uyması için `PageWidth` ve `PageHeight` değerlerini ayarlayın.  
- **Lisans hataları:** Görüntüyü yüklemeden önce geçerli bir lisans dosyasıyla `License.setLicense()` çağrısı yaptığınızdan emin olun.

## Conclusion

Bu adımları izleyerek **DWG'yi PDF'ye dönüştürmeyi** güvenilir bir şekilde yapabilir ve Aspose.CAD'in ağ desteğinden tam olarak yararlanabilirsiniz. Bu özellik, karmaşık CAD çizimlerinin yüksek kaliteli PDF dışa aktarımını gerektiren iş akışlarını, dahili kullanım veya müşteri odaklı belgeler olsun, basitleştirir.

## FAQ's

### Q1: Aspose.CAD for Java ticari kullanım için uygun mu?

A1: Evet, Aspose.CAD for Java hem kişisel hem de ticari kullanım için tasarlanmıştır. Lisans detaylarını [purchase page](https://purchase.aspose.com/buy) adresinde bulabilirsiniz.

### Q2: Test amaçlı geçici bir lisans nasıl alabilirim?

A2: Test ve değerlendirme için geçici bir lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

### Q3: Aspose.CAD for Java için topluluk desteğini nereden bulabilirim?

A3: Topluluk desteği için Aspose.CAD'e özel forumu [https://forum.aspose.com/c/cad/19](https://forum.aspose.com/c/cad/19) adresinde ziyaret edin.

### Q4: PDF dışında desteklenen başka çıktı formatları var mı?

A4: Evet, Aspose.CAD for Java PNG, JPEG, BMP ve daha fazlası dahil çeşitli çıktı formatlarını destekler. Detaylar için belgelere bakın.

### Q5: Aspose.CAD for Java'ı ücretsiz deneyebilir miyim?

5: Evet, Aspose.CAD for Java'ın ücretsiz deneme sürümünü [buradan](https://releases.aspose.com/) inceleyebilirsiniz.

---

**Last Updated:** 2025-12-09  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}