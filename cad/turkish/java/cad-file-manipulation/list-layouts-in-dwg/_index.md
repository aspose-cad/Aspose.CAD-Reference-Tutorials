---
date: 2025-12-28
description: Aspose.CAD for Java kullanarak DWG dosyalarını nasıl okuyacağınızı öğrenin
  ve DWG dosyalarındaki düzenleri zahmetsizce listeleyin. Güçlü CAD işlevselliğini
  Java uygulamalarınıza entegre edin.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java Kullanarak DWG Dosyasını Okuma ve DWG'deki Düzenleri Listeleme
url: /tr/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG'yi Okuma ve DWG'de Layout'ları Listeleme Aspose.CAD for Java Kullanarak

## Giriş

Programatik olarak **DWG** dosyalarını okumanız ve layout adları gibi bilgileri çıkarmanız gerekiyorsa, Aspose.CAD for Java bunu oldukça basit hale getirir. Bu adım‑adım öğreticide **DWG'yi nasıl okuyacağınızı** ve bir DWG (veya DXF) dosyasında bulunan tüm layout'ları nasıl listeleyeceğinizi göstereceğiz. Kılavuzun sonunda, CAD verileriyle çalışan herhangi bir Java uygulamasına bu yeteneği ekleyebileceksiniz.

## Hızlı Yanıtlar
- **Hangi kütüphane gereklidir?** Aspose.CAD for Java.
- **DWG dosyalarını herhangi bir işletim sisteminde okuyabilir miyim?** Evet – Java platform‑bağımsızdır.
- **Örneği çalıştırmak için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme yeterlidir; üretim için lisans gereklidir.
- **Hangi CAD formatları destekleniyor?** DWG, DXF, DWF ve diğerleri.
- **Kod Java 8+ ile uyumlu mu?** Kesinlikle.

## Java'da “DWG nasıl okunur” nedir?

DWG dosyasını okumak, ikili CAD verilerini sorgulayabileceğiniz bir nesne modeline yüklemek anlamına gelir. Aspose.CAD, karmaşık DWG yapısını basit .NET/Java sınıflarının arkasına gizler ve ihtiyacınız olan bilgiye odaklanmanızı sağlar – bu durumda layout adları.

## Neden bir DWG dosyasında layout'ları listelemek?

Bir DWG birden fazla layout (kağıt alanı, model alanı, özel sayfalar) içerebilir. Layout adlarını bilmek şunları yapmanızı sağlar:
- Layout başına raporlar oluşturmak.
- Belirli layout'ları görüntülere veya PDF'lere dışa aktarmak.
- Çizimlerin toplu işlenmesini otomatikleştirmek.

## Önkoşullar

Kodun içine dalmadan önce aşağıdakilere sahip olduğunuzu doğrulayın:

- **Aspose.CAD for Java Library** – en son JAR dosyasını [website](https://releases.aspose.com/cad/java/) adresinden indirin.
- **Java Development Environment** – JDK 8 veya üzeri, ve tercih ettiğiniz bir IDE ya da derleme aracı.

## İçe Aktarma Ad Alanları

Java kaynak dosyanızda, gerekli Aspose.CAD sınıflarını içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Adım 1: Belge Dizinini Ayarlayın

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

**“Your Document Directory”** ifadesini CAD dosyalarınızın bulunduğu mutlak yol ile değiştirin.

## Adım 2: DWG Dosyasını Yükleyin

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

`Image.load` yöntemi dosya formatını otomatik olarak algılar, bu yüzden aynı kodu **DWG** ve **DXF** dosyaları için kullanabilirsiniz.

## Adım 3: Layout'ları Alın ve İsimlerini Yazdırın

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

Döngü her layout nesnesi üzerinde iterasyon yapar ve adını konsola yazar – **DWG**'yi başarıyla okuduğunuzu ve layout bilgilerini çıkardığınızı doğrulamanın basit bir yoludur.

## Yaygın Tuzaklar ve İpuçları

- **Incorrect file path** – `dataDir` değişkeninin işletim sisteminize uygun bir ayırıcı (`/` veya `\\`) ile bittiğinden emin olun.
- **Unsupported DWG version** – Güncel bir Aspose.CAD sürümü kullandığınızdan emin olun; eski DWG sürümleri dönüştürme gerektirebilir.
- **Memory usage** – Büyük çizimler önemli miktarda bellek tüketebilir. İşiniz bittiğinde `CadImage` nesnesini serbest bırakın: `cadImage.dispose();`.

## Sonuç

Tebrikler! Artık Aspose.CAD for Java kullanarak **DWG'yi nasıl okuyacağınızı** ve layout'larını nasıl listeleyeceğinizi biliyorsunuz. Bu teknik, belirli layout'ları görüntülere veya PDF'lere dışa aktarma gibi daha ileri CAD otomasyonları için temel oluşturur. Daha derin bir keşif için resmi [documentation](https://reference.aspose.com/cad/java/) sayfasına bakın.

## Sık Sorulan Sorular

### Q1: Aspose.CAD for Java'ı diğer CAD dosya formatlarıyla kullanabilir miyim?
**A1:** Evet, Aspose.CAD çeşitli CAD formatlarını destekler, bunlar arasında DWG, DXF, DWF ve daha fazlası bulunur.

### Q2: Aspose.CAD for Java için ücretsiz deneme mevcut mu?
**A2:** Evet, [buradan](https://releases.aspose.com/) ücretsiz deneme alabilirsiniz.

### Q3: Aspose.CAD for Java için topluluk desteğini nereden alabilirim?
**A3:** Aspose.CAD forumuna [buradan](https://forum.aspose.com/c/cad/19) ulaşabilirsiniz.

### Q4: Aspose.CAD for Java için lisans nasıl satın alınır?
**A4:** Lisansı [satın alma sayfasından](https://purchase.aspose.com/buy) alabilirsiniz.

### Q5: Test amaçlı geçici bir lisans kullanabilir miyim?
**A5:** Evet, geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

**Ek Sorular**

**Q:** Bu yaklaşım Linux'ta DWG dosyalarını okumak için çalışır mı?  
**A:** Kesinlikle. Çözüm saf Java olduğundan, uyumlu bir JDK'ya sahip herhangi bir işletim sisteminde çalışır.

**Q:** DWG dosyasını tüm çizimi belleğe yüklemeden okuyabilir miyim?  
**A:** Aspose.CAD çizimi belleğe yükler; çok büyük dosyalar için ayrı iş parçacıklarında işleme veya gelecekteki sürümlerde sunulabilecek akış API'lerini kullanmayı düşünebilirsiniz.

**Q:** Layout'ları isimlerine göre filtrelemenin bir yolu var mı?  
**A:** Evet – `CadLayoutDictionary`'yi aldıktan sonra `layout.getLayoutName().equalsIgnoreCase("MyLayout")` kontrolünü yaparak işleme devam edebilirsiniz.

---

**Son Güncelleme:** 2025-12-28  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}