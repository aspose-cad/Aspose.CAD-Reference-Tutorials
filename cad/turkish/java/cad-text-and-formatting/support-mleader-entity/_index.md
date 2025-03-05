---
title: Aspose.CAD for Java ile DWG Formatı için MLeader Entity'yi destekleyin
linktitle: Java ile DWG Formatı için MLeader Varlığını Destekleyin
second_title: Aspose.CAD Java API'si
description: DWG formatında MLeader varlıklarını desteklemeye yönelik adım adım eğitimimizle Aspose.CAD for Java'nın gücünün kilidini açın.
type: docs
weight: 12
url: /tr/java/cad-text-and-formatting/support-mleader-entity/
---
## giriiş

Java ile bilgisayar destekli tasarım (CAD) alanında, DWG formatındaki MLeader varlıkları için desteği anlamak ve uygulamak değerli bir beceridir. Aspose.CAD for Java, bir dizi güçlü araç ve işlevsellik sunarak bu tür görevler için sağlam bir çözüm sunar. Bu eğitim, Aspose.CAD ile Java kullanarak DWG dosyalarındaki MLeader varlıklarını destekleme sürecinde size rehberlik edecektir.

## Önkoşullar

Eğiticiye geçmeden önce aşağıdaki önkoşulların yerine getirildiğinden emin olun:

1. Java Geliştirme Ortamı: Sisteminizde bir Java geliştirme ortamının kurulu olduğundan emin olun.

2.  Aspose.CAD Kütüphanesi: Java için Aspose.CAD kütüphanesini şuradan indirip yükleyin:[İndirme: {link](https://releases.aspose.com/cad/java/).

## Ad Alanlarını İçe Aktar

Aspose.CAD'in özelliklerinden etkin bir şekilde yararlanmak için Java projenize gerekli ad alanlarını içe aktarın. Kodunuza aşağıdaki satırları ekleyin:

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

Şimdi Aspose.CAD ile Java kullanarak DWG formatı için MLeader varlıklarını desteklemek üzere kodu adım adım bir kılavuza ayıralım.

## 1. DWG Dosyasını Yükleyin ve CadImage'a Erişin

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. MLeader Varlıklarını Doğrulayın

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. MLeader Stilini ve Niteliklerini Doğrulayın

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. MLeader Bağlam Verilerine Erişin

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. Bağlam Niteliklerini Doğrulayın

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. MLeader Düğümüne ve Lider Çizgiye Erişim

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

## 7. Ek MLeader Niteliklerini Doğrulayın

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. Metin Niteliklerini Doğrulayın

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. Ek MLeader Nitelikleri

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Çözüm

Tebrikler! Java ve Aspose.CAD kullanarak DWG formatı için MLeader varlıklarını desteklemeye ilişkin kapsamlı kılavuzda başarıyla gezindiniz. Bu yetenek, gelişmiş CAD manipülasyonlarına kapı açar ve Java geliştirme araç setinizi geliştirir.

## SSS'ler

### S1: Aspose.CAD for Java'yı diğer CAD formatlarıyla kullanabilir miyim?

C1: Evet, Aspose.CAD, DWG'nin ötesinde çeşitli CAD formatlarını destekleyerek projelerinizde çok yönlülük sağlar.

### S2: Aspose.CAD for Java'nın ayrıntılı belgelerini nerede bulabilirim?

 A2: Bkz.[dokümantasyon](https://reference.aspose.com/cad/java/) Aspose.CAD'in yeteneklerine ilişkin derinlemesine bilgiler için.

### S3: Ücretsiz deneme sürümü mevcut mu?

 C3: Evet, işlevleri ilk elden keşfedin.[ücretsiz deneme](https://releases.aspose.com/).

### S4: Aspose.CAD için nasıl geçici lisans alabilirim?

Cevap4: Geçici bir lisans alın:[bu bağlantı](https://purchase.aspose.com/temporary-license/).

### S5: Topluluk desteğini ve yardımını nereden alabilirim?

A5: ziyaret edin[Aspose.CAD forumu](https://forum.aspose.com/c/cad/19) toplulukla bağlantı kurmak ve yardım almak için.