---
date: 2026-03-07
description: Aspose.CAD for Java kullanarak DWG dosyalarında yazı tipini nasıl değiştireceğinizi
  öğrenin. Bu adım adım kılavuz, belirli bir stilin **yazı tipini nasıl değiştireceğini**
  hassas bir şekilde gösterir.
linktitle: Substitute Font of a Particular Style in DWG
second_title: Aspose.CAD Java API
title: Aspose.CAD for Java Kullanarak DWG'de Belirli Bir Stilin Yazı Tipini Nasıl
  Değiştirilir
url: /tr/java/cad-text-and-annotation/substitute-font-of-particular-style-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java Kullanarak DWG'de Belirli Bir Stil İçin Font Nasıl Değiştirilir

## Giriş

CAD (Computer‑Aided Design) dünyasında hassasiyet ve detay çok önemlidir ve **fontun nasıl değiştirileceğini bilmek**, bir çizimde size sayısız saatlik yeniden çalışma tasarrufu sağlayabilir. Aspose.CAD for Java, geliştiricilere DWG dosyalarını değiştirmek için temiz, programatik bir yol sunar; buna belirli bir metin stilinin fontunu değiştirme yeteneği de dahildir. Bu öğreticide, bir DWG dosyasında belirli bir stilin fontunu değiştirmek için gereken adımları adım adım gösterecek, neden bunu yapmak isteyebileceğinizi açıklayacak ve sonucu nasıl doğrulayacağınızı göstereceğiz.

## Hızlı Yanıtlar
- **DWG'de “font değiştirme” ne anlama gelir?** Metin stili tanımına bağlı birincil fontu değiştirmek.  
- **Bu işlemi hangi kütüphane yönetir?** Aspose.CAD for Java.  
- **Lisans gerekli mi?** Test için ücretsiz deneme çalışır; üretim için ticari lisans gerekir.  
- **Birden fazla stili aynı anda değiştirebilir miyim?** Evet – stil koleksiyonunu döngüyle gezerek her bir fontu ayarlayabilirsiniz.  
- **Kod Java 8+ ile uyumlu mu?** Kesinlikle, API Java 8 ve üzeri hedef alır.

## DWG'de Font Değiştirme Nedir?

Font değiştirme, bir metin stilinin *birincil font* özelliğini güncellemek anlamına gelir (DWG terminolojisinde “stil” olarak da adlandırılır). Bir çizim bu stili referans aldığında, tüm metin parçaları otomatik olarak yeni fontu benimser ve dosyanın tamamında tutarlı bir görünüm sağlar.

## DWG Metin Stilini Neden Değiştirmelisiniz?

- **Marka tutarlılığını koruyun:** Tüm çizimlerde kurumsal fontları kullanın.  
- **Eksik fontları düzeltin:** Kullanılamayan fontları hedef sistemde yüklü olanlarla değiştirin.  
- **Baskı/plotlama için hazırlık:** Bazı plotterlar doğru çıktı için belirli fontlar gerektirir.

## Ön Koşullar

Bu öğreticiye başlamadan önce aşağıdaki öğelerin kurulu olduğundan emin olun:

1. **Aspose.CAD for Java Kütüphanesi:** Aspose.CAD kütüphanesini indirin ve kurun. Kütüphaneyi ve dokümantasyonunu [burada](https://releases.aspose.com/cad/java/) bulabilirsiniz.
2. **Java Development Kit (JDK):** Makinenizde Java yüklü olduğundan emin olun.

Gerekli araçlara sahip olduğunuza göre, bir sonraki bölüme geçelim.

## İsim Uzaylarını İçe Aktarma (DWG metin stilini değiştirmek için gerekli)

Java’da doğru isim uzaylarını içe aktarmak, harici kütüphaneleri kullanmak için çok önemlidir. Bu durumda, gerekli Aspose.CAD isim uzaylarını içe aktardığınızdan emin olun. İşte nasıl yapabileceğiniz:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
```

Şimdi, örnek kodu birden fazla adıma ayıralım.

## Adım 1: Kaynak Dizinini Ayarlama

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

`"Your Document Directory"` ifadesini gerçek belge dizininizin yolu ile değiştirin.

## Adım 2: CAD Çizimini Yükleme

```java
String srcFile = dataDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of CadImage
CadImage cadImage = (CadImage)Image.load(srcFile);
```

`"conic_pyramid.dxf"` ifadesini CAD çiziminizin gerçek adıyla değiştirin.

## Adım 3: Bir Stil İçin Font Belirleme (DWG stil fontunu değiştirme)

```java
// Specify the font for one particular style
((CadStyleTableObject)cadImage.getStyles().get_Item(0)).setPrimaryFontName("Arial");
```

Font adını (bu örnekte "Arial") gereksinimlerinize göre ayarlayın. Bu satır **DWG stilinin birincil fontunu ayarlar**, eski fontu etkili bir şekilde değiştirir.

## Yaygın Sorunlar ve Çözümler

| Sorun | Neden | Çözüm |
|-------|-------|----------|
| Kaydetme sonrası font değişmiyor | Çizim, değişiklikten sonra kaydedilmemiş | Font ayarlandıktan sonra `cadImage.save(outputPath);` çağırın. |
| Font adı tanınmıyor | Kodun çalıştığı sistemde font yüklü değil | Fontu yükleyin veya genel bir font adı kullanın (ör. "Tahoma"). |
| `ClassCastException` | `get_Item`'dan gelen nesne tipi yanlış | Dizinin bir `CadStyleTableObject`'e işaret ettiğinden emin olun. |

## SSS'ler

### Q1: Tek bir DWG dosyasında birden fazla fontu değiştirebilir miyim?

A1: Evet, farklı stilleri döngüyle gezerek her stil için birincil fontu ayrı ayrı ayarlayabilirsiniz.

### Q2: Kullanabileceğim font adları için bir limit var mı?

A2: Hayır, sisteminizde mevcut olan herhangi bir geçerli font adını kullanabilirsiniz.

### Q3: Font değişikliklerini geri alabilir miyim?

A3: Aspose.CAD esneklik sağlar; değişiklikleri geri alabilir veya DWG dosyanızın farklı sürümlerini kaydedebilirsiniz.

### Q4: Bu öğretici diğer CAD formatlarına da uygulanabilir mi?

A4: Örnek DWG üzerine odaklansa da, benzer prensipler diğer desteklenen CAD formatlarına da uygulanabilir.

### Q5: Aspose.CAD for Java için nasıl destek alabilirim?

A5: Topluluk desteği ve tartışmalar için [Aspose.CAD forumunu](https://forum.aspose.com/c/cad/19) ziyaret edin.

## Ek Sık Sorulan Sorular

**S: Değiştirilen çizimi nasıl kaydederim?**  
C: Yeni fontu ayarladıktan sonra, değişiklikleri yeni bir dosyaya yazmak için `cadImage.save(dataDir + "output.dwg");` çağırın.

**S: Yalnızca açıklama nesnelerinin fontunu değiştirebilir miyim?**  
C: Evet, `setPrimaryFontName` uygulamadan önce stil koleksiyonunu açıklama‑ile ilgili stillerle filtreleyebilirsiniz.

**S: Font değişikliğini kaydetmeden önizlemek mümkün mü?**  
C: Bellekte önizleme yapmak için `cadImage.save(outputStream, new ImageOptions());` kullanarak görüntüyü bitmap olarak render edebilirsiniz.

**S: Aspose.CAD TrueType ve OpenType fontlarını destekliyor mu?**  
C: TrueType (.ttf) ve OpenType (.otf) fontları, ana işletim sistemine yüklü oldukları sürece tam olarak desteklenir.

## Sık Sorulan Sorular

**S: Bu kod için hangi Aspose.CAD sürümü gereklidir?**  
C: Bu öğreticide kullanılan API, Aspose.CAD for Java 24.11 ve sonrası sürümlerde mevcuttur.

**S: Bu kodu bir Linux sunucusunda çalıştırabilir miyim?**  
C: Evet, gerekli fontlar sunucuya yüklü olduğu ve Java 8+ mevcut olduğu sürece çalıştırabilirsiniz.

**S: Font değiştirmeden önce mevcut tüm metin stillerini nasıl listeleyebilirim?**  
C: `cadImage.getStyles()` üzerinde döngü kurarak her stilin adını ve mevcut birincil fontunu yazdırabilirsiniz.

**S: Birçok DWG dosyasını toplu işleyebilecek bir yol var mı?**  
C: Her dosyayı yükleyen, istenen stili güncelleyen ve çıktıyı kaydeden bir döngü içinde mantığı sarabilirsiniz.

**S: Birincil fontu değiştirmek boyutları veya boşlukları etkiler mi?**  
C: Font metrikleri farklı olabilir, bu yüzden değişiklikten sonra metin yüksekliğini veya konumlandırmasını ayarlamanız gerekebilir.

## Sonuç

Aspose.CAD for Java, CAD manipülasyonu için güçlü olanaklar sunar ve **font nasıl değiştirilir** sadece birçok özelliğinden biridir. Farklı stillerle deneyler yapın, *modify DWG text style* veya *set primary font dwg* gibi ikincil anahtar kelimeleri kullanarak çizimlerinizi ince ayarlayın ve kodu toplu işleme için daha büyük otomasyon hatlarına entegre edin.

---

**Son Güncelleme:** 2026-03-07  
**Test Edilen:** Aspose.CAD for Java 24.11  
**Yazar:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}