---
title: Vízjelek hozzáadása a CAD-rajzokhoz – Aspose.CAD for Java Tutorial
linktitle: Vízjel hozzáadása
second_title: Aspose.CAD Java API
description: Az Aspose.CAD for Java segítségével személyre szabott vízjelekkel javíthatja CAD-rajzait. Kövesse lépésenkénti útmutatónkat a zökkenőmentes integráció érdekében.
weight: 12
url: /hu/java/other-cad-operations/add-watermark/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vízjelek hozzáadása a CAD-rajzokhoz – Aspose.CAD for Java Tutorial

## Bevezetés

Üdvözöljük ebben az átfogó útmutatóban, amely az Aspose.CAD for Java használatával vízjelek CAD-rajzokhoz való hozzáadásával foglalkozik. Ebből az oktatóanyagból megtudhatja, hogyan integrálhatja hatékonyan a vízjeleket, személyre szabott üzenetekkel vagy márkajelzéssel javítva CAD-dokumentumait. Az Aspose.CAD for Java hatékony funkciókat kínál, amelyek egyszerűvé teszik a vízjel hozzáadásának folyamatát.

## Előfeltételek

Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

-  Aspose.CAD for Java: Győződjön meg arról, hogy az Aspose.CAD könyvtár telepítve van a Java környezetben. Letöltheti[itt](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Győződjön meg arról, hogy a JDK legújabb verziója van telepítve a rendszerére.

## Csomagok importálása

A kezdéshez a Java projektben importálja a szükséges Aspose.CAD csomagokat:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 1. lépés: Új MTEXT hozzáadása

```java
//új MTEXT hozzáadása
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## 2. lépés: Adjon hozzá egyszerű entitást, például szöveget

Hozzáadhat egy egyszerűbb entitást is, például szöveget:

```java
// vagy adjon hozzá egyszerűbb entitást, például a szöveget
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## 3. lépés: Exportálás PDF-be

Exportálja a hozzáadott vízjellel ellátott CAD-rajzot PDF-fájlba:

```java
// exportálni pdf-be
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Következtetés

Gratulálunk! Sikeresen hozzáadott vízjeleket CAD-rajzaihoz az Aspose.CAD for Java segítségével. Ez az egyszerű, de hatékony folyamat lehetővé teszi, hogy személyre szabja a terveit, vagy védje azokat márkajelzéssel.

## GYIK

### 1. kérdés: Az Aspose.CAD kompatibilis az összes CAD fájlformátummal?

1. válasz: Az Aspose.CAD különféle CAD-formátumokat támogat, beleértve a DWG-t, DXF-et, DWT-t és DWF-et.

### 2. kérdés: Testreszabhatom a vízjel szövegének megjelenését?

2. válasz: Igen, teljes mértékben Ön szabályozhatja a vízjel megjelenését, beleértve a szöveg méretét, színét és helyzetét.

### 3. kérdés: Elérhető az Aspose.CAD for Java próbaverziója?

 3. válasz: Igen, letöltheti a próbaverziót[itt](https://releases.aspose.com/).

### 4. kérdés: Hogyan kaphatok támogatást az Aspose.CAD-hez?

 A4: Látogassa meg a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) közösségi támogatásért.

### 5. kérdés: Hol találom az Aspose.CAD for Java teljes dokumentációját?

 A5: Lásd a[dokumentáció](https://reference.aspose.com/cad/java/) részletes információkért.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
