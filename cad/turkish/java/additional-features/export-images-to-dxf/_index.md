---
title: Aspose.CAD for Java Kullanarak Görüntüleri DXF Formatına Aktarın
linktitle: Java Kullanarak Görüntüleri DXF Formatına Aktarma
second_title: Aspose.CAD Java API'si
description: Aspose.CAD for Java'yı kullanarak görüntüleri DXF formatına aktarmanın kusursuz sürecini keşfedin. Adım adım kılavuz, SSS ve daha fazlası.
weight: 15
url: /tr/java/additional-features/export-images-to-dxf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java Kullanarak Görüntüleri DXF Formatına Aktarın

## giriiş

Aspose.CAD for Java kullanarak görüntüleri DXF formatına aktarmaya ilişkin kapsamlı bir eğitime hoş geldiniz. Aspose.CAD, geliştiricilerin CAD çizimleriyle programlı olarak çalışmasına olanak tanıyan güçlü bir Java kütüphanesidir. Bu eğitimde, görüntüleri DXF formatına aktarma sürecinde size yol göstereceğiz ve bu görevi gerçekleştirmek için çeşitli adımları ve teknikleri göstereceğiz.

## Önkoşullar

Başlamadan önce aşağıdakilere sahip olduğunuzdan emin olun:

- Java programlamanın temel anlayışı.
-  Aspose.CAD for Java kütüphanesi kuruldu. İndirebilirsin[Burada](https://releases.aspose.com/cad/java/).
- Aspose.CAD için geçerli bir lisans veya geçici lisans. Onu edinin[Burada](https://purchase.aspose.com/temporary-license/).
- Test amaçlı DXF formatında bazı örnek resimler.

## Ad Alanlarını İçe Aktar

Aspose.CAD için gerekli ad alanlarını Java projenize aktarın:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
import java.io.File;
import static java.lang.System.in;
```

## 1. Adım: Belge Başına Yeni Yazı Tipi Ayarlayın

```java
// Kaynak dizininin yolu.
String dataDir = "Your Document Directory" + "DXFDrawings/";

File[] files = new File(dataDir).listFiles();
for (File file : files) {
    String extension = GetFileExtension(file);
    if (extension.equals(".dxf")) {
        CadImage cadImage = (CadImage)Image.load(file.getName());
        for (Object style : cadImage.getStyles()) {
            ((CadStyleTableObject)style).setPrimaryFontName("Broadway");
        }
        cadImage.save(file.getName() + "_font.dxf");
    }
}
```

## Adım 2: Tüm "Düz" Çizgileri Gizle

```java
CadImage cadImageEntity = (CadImage)Image.load(file.getName());
for (CadBaseEntity entity : cadImageEntity.getEntities()) {
    if (entity.getTypeName() == CadEntityTypeName.LINE) {
        entity.setVisible((short)0);
    }
}
cadImageEntity.save(file.getName() + "_lines.dxf");
```

## Adım 3: Metinle Düzenlemeler

```java
CadImage cadImageText = (CadImage)Image.load(file.getName());
for (CadBaseEntity entity : cadImageText.getEntities()) {
    if (entity.getTypeName() == CadEntityTypeName.TEXT) {
        ((CadText)entity).setDefaultValue("New text here!!! :)");
        break;
    }
}
cadImageText.save(file.getName() + "_text.dxf");
```

Dizininizdeki her DXF dosyası için bu adımları tekrarlayın.

## Çözüm

Tebrikler! Aspose.CAD for Java'yı kullanarak görüntüleri DXF formatına nasıl aktaracağınızı başarıyla öğrendiniz. Bu eğitim, yazı tiplerini ayarlama, satırları gizleme ve CAD görüntüleri içindeki metinleri değiştirme gibi temel adımları kapsıyordu.

## SSS'ler

### S1: Aspose.CAD for Java'yı lisans olmadan kullanabilir miyim?

 A1: Mevcut geçici lisansla kullanabilirsiniz[Burada](https://purchase.aspose.com/temporary-license/).

### S2: Aspose.CAD belgelerini nerede bulabilirim?

 A2: Belgeler mevcut[Burada](https://reference.aspose.com/cad/java/).

### S3: Aspose.CAD desteğini nasıl alabilirim?

 Cevap 3: Destek forumunu ziyaret edin[Burada](https://forum.aspose.com/c/cad/19).

### S4: Aspose.CAD for Java'yı nereden indirebilirim?

 Cevap4: Kitaplığı indirin[Burada](https://releases.aspose.com/cad/java/).

### S5: Ücretsiz deneme sürümü var mı?

 A5: Evet, ücretsiz deneme sürümünden yararlanabilirsiniz[Burada](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
