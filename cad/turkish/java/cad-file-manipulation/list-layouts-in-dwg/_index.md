---
date: 2026-02-28
description: Aspose.CAD for Java kullanarak DWG dosyalarını nasıl okuyacağınızı öğrenin
  ve DWG dosyalarındaki düzenleri zahmetsizce listeleyin. Güçlü CAD işlevselliğini
  Java uygulamalarınıza entegre edin.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java Kullanarak DWG Dosyasını Okuma ve DWG'deki Düzenleri Listeleme
url: /tr/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

 >}}

We must keep them.

Now ensure we didn't translate any URLs or code block placeholders. Keep them unchanged.

Check for any variable names: dataDir, CadImage, cadImage.dispose(); etc. Those are inside text, not code blocks. Should keep as is.

Also keep **read dwg on linux** unchanged.

Now produce final output with all markdown and shortcodes.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java Kullanarak DWG'yi Okuma ve Layout'ları Listeleme

## Giriş

Programlı olarak **how to read dwg** dosyalarını okumak için güvenilir bir yol arıyorsanız, Aspose.CAD for Java, bir çizimi yüklemenizi ve dosya içindeki tüm layout adları gibi ihtiyacınız olan herhangi bir bilgiyi almanızı sağlayan temiz, çapraz‑platform bir API sunar. Bu adım‑adım öğreticide **how to read DWG** nasıl yapılacağını ve bir DWG (veya DXF) dosyasında bulunan her layout'u nasıl listeleyeceğinizi göstereceğiz, böylece bu yeteneği CAD verileriyle çalışan herhangi bir Java uygulamasına entegre edebilirsiniz.

## Hızlı Yanıtlar
- **Gerekli kütüphane nedir?** Aspose.CAD for Java.  
- **DWG dosyalarını herhangi bir işletim sisteminde okuyabilir miyim?** Evet – Java çapraz‑platform olduğundan, **read dwg on linux** işlemini Windows'ta olduğu gibi kolayca yapabilirsiniz.  
- **Örneği çalıştırmak için lisansa ihtiyacım var mı?** Değerlendirme için ücretsiz deneme çalışır; üretim için lisans gereklidir.  
- **Hangi CAD formatları destekleniyor?** DWG, DXF, DWF ve diğerleri.  
- **Kod Java 8+ ile uyumlu mu?** Kesinlikle.

## Java'da “how to read dwg” nedir?

DWG dosyasını okumak, ikili CAD verilerini sorgulayabileceğiniz bir nesne modeline yüklemek anlamına gelir. Aspose.CAD, karmaşık DWG yapısını basit Java sınıflarının arkasına soyutlayarak, ihtiyacınız olan bilgiye odaklanmanızı sağlar – bu durumda layout adları.

## Neden bir DWG dosyasında layout'ları listelemelisiniz?

Bir DWG birden fazla layout (kağıt alanı, model alanı, özel sayfalar) içerebilir. Layout adlarını bilmek şunları yapmanızı sağlar:

- Layout başına raporlar oluşturmak.  
- Belirli layout'ları görüntülere veya PDF'lere dışa aktarmak.  
- Çizimlerin toplu işlenmesini otomatikleştirmek.

## Önkoşullar

Koda geçmeden önce aşağıdakilere sahip olduğunuzu doğrulayın:

- **Aspose.CAD for Java Library** – en son JAR'ı [website](https://releases.aspose.com/cad/java/) adresinden indirin.  
- **Java Geliştirme Ortamı** – JDK 8 veya üzeri, ve tercih ettiğiniz bir IDE ya da derleme aracı.

## İsim Uzaylarını İçe Aktarma

Java kaynak dosyanızda, gerekli Aspose.CAD sınıflarını içe aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Adım 1: Belge Dizinini Ayarlama

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

**“Your Document Directory”** ifadesini CAD dosyalarınızın bulunduğu mutlak yol ile değiştirin. Linux'ta `/home/user/cad/` gibi bir yol kullanabilirsiniz.

## Adım 2: DWG Dosyasını Yükleme

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

`Image.load` yöntemi dosya formatını otomatik olarak algılar, bu yüzden aynı kod **DWG** ve **DXF** dosyaları için çalışır.

## Adım 3: Layout'ları Al ve İsimleri Yazdır

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

Döngü her layout nesnesi üzerinde iterasyon yapar ve adını konsola yazar – **read DWG** işlemini başarıyla gerçekleştirdiğinizi ve layout bilgilerini çıkardığınızı doğrulamanın basit bir yoludur.

## Linux'ta DWG'yi PDF'ye Dönüştürme

Daha sonra belirli bir layout'u PDF'ye dönüştürmeniz gerekirse, Aspose.CAD layout'u bir görüntüye render edebilir ve ardından bu görüntüyü bir PDF belgesine gömmek için Aspose.PDF (veya başka bir PDF kütüphanesi) kullanabilirsiniz. Dönüştürme kodu Linux'ta da aynıdır çünkü API saf Java'dır.

## Yaygın Tuzaklar ve İpuçları

- **Yanlış dosya yolu** – `dataDir`'in işletim sisteminize uygun bir ayırıcı (`/` veya `\\`) ile bittiğinden emin olun.  
- **Desteklenmeyen DWG sürümü** – Güncel bir Aspose.CAD sürümü kullandığınızdan emin olun; eski DWG sürümleri dönüşüm gerektirebilir.  
- **Bellek kullanımı** – Büyük çizimler önemli miktarda bellek tüketebilir. İşiniz bittiğinde `CadImage` nesnesini serbest bırakın: `cadImage.dispose();`.  
- **Başsız sunucularda çalıştırma** – UI bileşenlerine ihtiyaç yoktur, bu yüzden kod grafik ortamı olmayan Linux sunucularında çalışır.

## Sonuç

Tebrikler! Artık Aspose.CAD for Java kullanarak **how to read dwg** ve layout'larını listelemeyi biliyorsunuz. Bu teknik, belirli layout'ları görüntülere, PDF'lere dışa aktarma veya Linux'ta DWG'yi PDF'ye dönüştürme gibi daha gelişmiş CAD otomasyonunun temelini oluşturur. Daha derin bir keşif için resmi [documentation](https://reference.aspose.com/cad/java/) adresine bakın.

## Sıkça Sorulan Sorular

**Q1: Aspose.CAD for Java'yi diğer CAD dosya formatlarıyla kullanabilir miyim?**  
A1: Evet, Aspose.CAD çeşitli CAD formatlarını destekler, DWG, DXF, DWF ve daha fazlası dahil.

**Q2: Aspose.CAD for Java için ücretsiz deneme mevcut mu?**  
A2: Evet, [buradan](https://releases.aspose.com/) ücretsiz deneme alabilirsiniz.

**Q3: Aspose.CAD for Java için topluluk desteğini nereden alabilirim?**  
A3: Topluluk desteği için [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adresini ziyaret edin.

**Q4: Aspose.CAD for Java için lisans nasıl satın alınır?**  
A4: Lisansı [purchase page](https://purchase.aspose.com/buy) adresinden satın alabilirsiniz.

**Q5: Test amaçlı geçici bir lisans kullanabilir miyim?**  
A5: Evet, geçici lisansı [buradan](https://purchase.aspose.com/temporary-license/) alabilirsiniz.

**Ek Sorular**

**Q: Bu yaklaşım Linux'ta DWG dosyalarını okumak için çalışır mı?**  
A: Kesinlikle. Çözüm saf Java olduğu için uyumlu bir JDK'ya sahip herhangi bir işletim sisteminde çalışır.

**Q: DWG dosyasını tüm çizimi belleğe yüklemeden okuyabilir miyim?**  
A: Aspose.CAD çizimi belleğe yükler; çok büyük dosyalar için ayrı iş parçacıklarında işleme yapmayı veya gelecekteki sürümlerde mevcut olabilecek akış API'lerini kullanmayı düşünebilirsiniz.

**Q: Layout'ları isimlerine göre filtrelemenin bir yolu var mı?**  
A: Evet – `CadLayoutDictionary`'yi aldıktan sonra işleme başlamadan önce `layout.getLayoutName().equalsIgnoreCase("MyLayout")` kontrol edebilirsiniz.

---

**Son Güncelleme:** 2026-02-28  
**Test Edilen Versiyon:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}