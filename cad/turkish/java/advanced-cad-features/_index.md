---
date: 2026-06-24
description: Aspose.CAD for Java kullanarak CAD'yi PDF'ye dönüştürmeyi, tuval boyutunu
  ayarlamayı, blok özniteliklerini çıkarmayı, CAD arka plan rengini ayarlamayı ve
  otomatik yerleşim ölçeklendirmesini uygulamayı öğrenin.
keywords:
- convert cad to pdf
- set canvas size java
- set cad background color
linktitle: Tuval Boyutunu Ayarla – Gelişmiş CAD Özellikleri
schemas:
- author: Aspose
  dateModified: '2026-06-24'
  description: Learn how to convert CAD to PDF, set canvas size, extract block attributes,
    set CAD background color, and apply auto layout scaling using Aspose.CAD for Java.
  headline: Convert CAD to PDF – Set Canvas Size and Advanced Features with Aspose.CAD
    for Java
  type: TechArticle
- questions:
  - answer: Yes. Loop through your collection of CAD files, configure the canvas size
      on each `ImageOptions` instance, and save the output programmatically.
    question: Can I set a custom canvas size for every file in a batch process?
  - answer: The quality is determined by the DPI setting in the rendering options.
      You can increase DPI while keeping the canvas dimensions to get higher‑resolution
      PDFs.
    question: Does setting the canvas size affect the quality of the exported PDF?
  - answer: Use the `ExternalReference` collection to resolve the reference, then
      iterate over its `BlockReference` objects to read attribute values.
    question: How do I extract block attribute values from a DWG that contains external
      references?
  - answer: Yes. The scaling logic works for both raster (PNG, TIFF) and vector (PDF,
      SVG) outputs, ensuring the drawing fits the canvas.
    question: Is auto layout scaling compatible with vector output formats like PDF?
  - answer: A paid Aspose.CAD license is required for production deployments. A free
      evaluation license can be used for development and testing.
    question: What licensing is required for commercial use?
  type: FAQPage
second_title: Aspose.CAD Java API
title: CAD'yi PDF'ye Dönüştür – Tuval Boyutunu Ayarlama ve Aspose.CAD for Java ile
  Gelişmiş Özellikler
url: /tr/java/advanced-cad-features/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD'i PDF'ye Dönüştür – Aspose.CAD for Java ile Tuval Boyutunu Ayarlama ve Gelişmiş Özellikler

## Giriş

Eğer Java'da **CAD'i PDF'ye dönüştür** ve aynı zamanda **tuval boyutunu ayarlama** yapmak istiyorsanız, doğru yerdesiniz. Aspose.CAD for Java, sadece tuval boyutlarını kontrol etmenizi sağlamakla kalmaz, aynı zamanda **blok öznitelik değerlerini çıkarma**, **CAD arka plan rengini ayarlama** ve **otomatik yerleşim ölçeklendirmesi** gibi zengin bir gelişmiş özellik seti sunar. Bu rehberde ana konuları ele alacak, neden önemli olduklarını açıklayacak ve her özelliğe daha derinlemesine dalan ayrıntılı öğreticilere yönlendireceğiz.

## Hızlı Yanıtlar
- **“set canvas size” ne yapar?** Çıktı görüntüsünün veya PDF'nin tam genişlik ve yüksekliğini tanımlar, böylece son render alanı üzerinde hassas kontrol sağlar.  
- **Tuval boyutunu ayarladıktan sonra CAD'i PDF'ye dönüştürebilir miyim?** Evet—Aspose.CAD, belirttiğiniz tuval boyutlarını koruyarak CAD dosyalarını PDF'ye dönüştürmenizi sağlar.  
- **Blok öznitelik değerlerini çıkarma destekleniyor mu?** Kesinlikle; API, dış referanslardan öznitelik değerlerini okuma yöntemleri sunar.  
- **Bir CAD render'ının arka plan rengini nasıl değiştiririm?** Dışa aktarmadan önce özel bir arka plan uygulamak için `setBackgroundColor` seçeneğini kullanın.  
- **Otomatik yerleşim ölçeklendirmesi nedir?** Çizimi otomatik olarak tuvalin içine sığdıracak şekilde ayarlar, manuel hesaplamalar yapmadan optimal görüntüleme sağlar.

## Aspose.CAD for Java'da “set canvas size” nedir?

Tuval boyutunu ayarlamak, render motoruna çıktı dosyası için tam piksel boyutlarını (veya fiziksel boyutu) bildirir. Bu, tutarlı sayfa düzenlerine ihtiyaç duyduğunuzda, CAD görüntülerini raporlara entegre ettiğinizde veya öngörülebilir boyutlarla küçük resimler oluşturduğunuzda hayati öneme sahiptir.

## Neden Aspose.CAD'in gelişmiş özelliklerini kullanmalısınız?

Aspose.CAD, **50+ giriş ve çıkış formatını**—DWG, DXF, DWF, PDF, PNG, TIFF ve SVG dahil—destekler ve tüm dosyayı belleğe yüklemeden çok sayfalı çizimleri işleyebilir. Kütüphane, **600 DPI'ye kadar yüksek doğrulukta render** sağlar ve dönüştürülen PDF'lerin çizgi kalınlıklarını, katmanları ve renkleri kaynak CAD dosyasında göründüğü gibi tam olarak korumasını garanti eder.

## Ön Koşullar
- Java Development Kit (JDK) 8 veya üzeri.  
- Aspose.CAD for Java kütüphanesi (en son sürümü Aspose web sitesinden indirin).  
- Üretim kullanımı için geçerli bir Aspose.CAD lisansı (değerlendirme için ücretsiz deneme sürümü çalışır).

## Gelişmiş Konuların Adım‑Adım Genel Bakışı

### Aspose.CAD for Java'da tuval boyutunu nasıl ayarlarsınız?

`CadImage` örneği oluşturduğunuzda, kaydetmeden önce `ImageOptions` nesnesi aracılığıyla tuval genişliğini ve yüksekliğini belirtebilirsiniz. Bu, dışa aktarılan dosyanın ihtiyacınız olan boyutlarla eşleşmesini sağlar.

**Doğrudan cevap:**  
`CadImage` nesnesi oluşturun, `setWidth` ve `setHeight` ile bir `ImageOptions` örneği yapılandırın, ardından `save` metodunu çağırın—çıktı, tanımladığınız tam tuval boyutunda render edilecektir.

**Tanım referansı:**  
`CadImage` Aspose.CAD'in bellekte yüklü bir CAD çizimini temsil eden temel sınıfıdır.  

`ImageOptions` tuval boyutu, DPI ve arka plan rengi gibi rasterleştirme parametrelerini kontrol eden yapılandırma nesnesidir.

### Tuval boyutunu koruyarak CAD'i PDF'ye nasıl dönüştürürsünüz?

`PdfOptions` sınıfını tuval ayarlarıyla birlikte kullanın. Dönüştürme işlemi tuval boyutlarını dikkate alır ve ekran render'ına tam olarak benzeyen bir PDF üretir.

**Doğrudan cevap:**  
`PdfOptions` nesnesi oluşturun, `setVectorRasterizationOptions` özelliğini tuval genişliği ve yüksekliğini içeren bir `ImageOptions` nesnesine ayarlayın, ardından `CadImage` üzerinde PDF formatıyla `save` metodunu çağırın. Oluşan PDF, belirttiğiniz tuval boyutunu koruyacaktır.

**Tanım referansı:**  
`PdfOptions` PDF'ye özgü dışa aktarma ayarlarını tanımlayan Aspose.CAD sınıfıdır; kesin düzen kontrolü için vektör‑rasterleştirme seçeneklerini içerir.

### Harici referanslardan blok öznitelik değerlerini nasıl çıkarırsınız?

API, bir `BlockReference` koleksiyonu sağlar. Bu koleksiyon üzerinde döngü yaparak DWG/DXF dosyasına gömülü katman adları, renkler veya özel veri gibi öznitelik değerlerini okuyabilirsiniz.

**Doğrudan cevap:**  
`CadImage` üzerindeki `getBlockReferences()` metoduna erişin, her bir `BlockReference` üzerinde döngü yapın ve blok özniteliklerini temsil eden anahtar‑değer çiftlerini almak için `getAttributes()` metodunu çağırın. Bu, hem iç hem de dış referanslar için çalışır.

**Tanım referansı:**  
`BlockReference`, bir CAD çizimindeki blok tanımının örneğini temsil eder; konum, dönüş ve ekli öznitelikler gibi özellikleri ortaya çıkarır.

### Daha şık bir görünüm için CAD arka plan rengini nasıl ayarlarsınız?

`BackgroundColor` render seçeneklerinin özelliği, istediğiniz herhangi bir RGB rengi seçmenizi sağlar. Bu, varsayılan beyaz arka planın marka kimliğiniz veya UI temanızla çakıştığı durumlarda özellikle faydalıdır.

**Doğrudan cevap:**  
`ImageOptions.setBackgroundColor(Color.getRGB(255, 255, 255))` (veya istediğiniz başka bir RGB değeri) komutunu görüntüyü veya PDF'yi kaydetmeden önce ayarlayın; seçilen renk, tüm çizim varlıklarının arkasındaki tuval arka planını dolduracaktır.

**Tanım referansı:**  
`BackgroundColor`, `ImageOptions` sınıfının bir özelliğidir ve CAD varlıkları çizilmeden önce tüm tuval üzerine uygulanacak doldurma rengini tanımlar.

### Dinamik tuval ayarlamaları için otomatik yerleşim ölçeklendirmesini nasıl uygularsınız?

`AutoLayoutScaling` bayrağını render seçeneklerinde etkinleştirin. Motor, en boy oranını koruyarak çizimi otomatik olarak tuvalin içine sığdıracak şekilde ölçeklendirecek, manuel hesaplamalardan sizi kurtaracaktır.

**Doğrudan cevap:**  
`ImageOptions.setAutoLayoutScaling(true)` metodunu çağırın; render motoru, tüm çizimin belirtilen tuval boyutları içinde bozulma olmadan sığması için optimal ölçek faktörünü hesaplayacaktır.

**Tanım referansı:**  
`AutoLayoutScaling`, `ImageOptions` içinde bir Boolean bayraktır ve etkinleştirildiğinde render motoruna çizimi otomatik olarak tuvali dolduracak şekilde ayarlamasını söyler.

## Her Özellik İçin Ayrıntılı Öğreticiler

Aşağıda, her gelişmiş yeteneği adım adım anlatan özel öğreticiler bulunmaktadır. Daha derinlemesine incelemek için herhangi bir bağlantıya tıklayın.

### [CAD Render İşlemi için İzlemeyi Etkinleştir](./enable-tracking-for-cad-rendering-process/)
### [IGES Formatını Entegre Et](./integrate-iges-format/)
### [Aspose.CAD for Java ile Mesh Desteği](./mesh-support-in-cad/)
### [Dışa Aktarmada Kalem Desteği](./pen-support-in-export/)
### [DWT Dosyalarını Okuma](./reading-dwt-files/)
### [Aspose.CAD for Java Kullanarak Arka Plan ve Çizim Rengini Ayarlama](./setting-background-and-drawing-color/)
### [Tuval Boyutunu ve Modunu Ayarlama](./set-canvas-size-and-mode/)
### [Aspose.CAD Java ile Otomatik Yerleşim Ölçeklendirmesini Ayarlama](./setting-auto-layout-scaling/)
### [Java'da Aspose.CAD ile Katman Desteği](./support-of-layers-in-cad/)
### [Aspose.CAD Kullanarak Java'da Harici Referanstan Blok Öznitelik Değerini Çıkarma](./extract-block-attribute-value/)

## Yaygın Sorunlar ve Sorun Giderme
- **Tuval boyutu uygulanmadı:** `save()` metodunu çağırmadan önce doğru `ImageOptions` nesnesinde boyutu ayarladığınızdan emin olun.  
- **Arka plan rengi değişmemiş gibi görünüyor:** Render modunun arka plan renklerini desteklediğini (ör. PNG, TIFF) doğrulayın.  
- **Blok öznitelikleri null döndürüyor:** DWG dosyasının gerçekten öznitelik tanımları içerdiğini ve doğru blok referansına eriştiğinizi kontrol edin.  
- **Otomatik yerleşim ölçeklendirmesi bozulmuş görünüyor:** En‑boy oranı bayrağının etkin olduğundan emin olun; aksi takdirde motor çizimi uzatabilir.  

## Sıkça Sorulan Sorular

**S:** Toplu işlemde her dosya için özel bir tuval boyutu ayarlayabilir miyim?  
**C:** Evet. CAD dosyalarınızın koleksiyonunu döngüyle işleyin, her `ImageOptions` örneğinde tuval boyutunu yapılandırın ve çıktıyı programlı olarak kaydedin.

**S:** Tuval boyutunu ayarlamak, dışa aktarılan PDF'nin kalitesini etkiler mi?  
**C:** Kalite, render seçeneklerindeki DPI ayarıyla belirlenir. Tuval boyutlarını korurken DPI'yi artırarak daha yüksek çözünürlüklü PDF'ler elde edebilirsiniz.

**S:** Harici referanslar içeren bir DWG'den blok öznitelik değerlerini nasıl çıkarırım?  
**C:** Referansı çözmek için `ExternalReference` koleksiyonunu kullanın, ardından öznitelik değerlerini okumak için `BlockReference` nesneleri üzerinde döngü yapın.

**S:** Otomatik yerleşim ölçeklendirmesi PDF gibi vektör çıktı formatlarıyla uyumlu mu?  
**C:** Evet. Ölçeklendirme mantığı, raster (PNG, TIFF) ve vektör (PDF, SVG) çıktılarının her ikisinde de çalışır ve çizimin tuvale sığmasını sağlar.

**S:** Ticari kullanım için hangi lisans gereklidir?  
**C:** Üretim dağıtımları için ücretli bir Aspose.CAD lisansı gereklidir. Geliştirme ve test için ücretsiz bir değerlendirme lisansı kullanılabilir.

**Son Güncelleme:** 2026-06-24  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.12 (latest)  
**Yazar:** Aspose  

{{< blocks/products/products-backtop-button >}}

## İlgili Öğreticiler

- [CAD'den PDF Oluştur – Aspose.CAD Java ile Otomatik Yerleşim Ölçeklendirme](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)
- [Aspose.CAD for Java ile DXF'yi PDF'ye Nasıl Dönüştürülür](/cad/java/additional-features/)
- [DWG'yi PDF'ye Dışa Aktar ve CAD Çizimlerini Dönüştür – Aspose.CAD Java Öğreticisi](/cad/java/cad-drawing-conversion/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}