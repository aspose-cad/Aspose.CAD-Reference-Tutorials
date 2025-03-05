---
title: Szöveg hozzáadása a DWG-ben az Aspose.CAD for Java használatával
linktitle: Szöveg hozzáadása a DWG-ben
second_title: Aspose.CAD Java API
description: Fokozza könnyedén DWG-rajzait az Aspose.CAD for Java segítségével. Adjon hozzá szöveget zökkenőmentesen lépésenkénti útmutatónkkal.
type: docs
weight: 10
url: /hu/java/cad-text-and-annotation/add-text-in-dwg/
---
## Bevezetés

A számítógéppel segített tervezés (CAD) területén az Aspose.CAD for Java hatékony eszköz a DWG-rajzok manipulálására és konvertálására. Egyik praktikus funkciója, hogy zökkenőmentesen adhat hozzá szöveget a DWG-fájlokhoz. Ebben az oktatóanyagban végigvezetjük a DWG-rajzokhoz szöveg hozzáadásának folyamatán az Aspose.CAD for Java segítségével.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

-  Aspose.CAD for Java Library: Töltse le és telepítse a könyvtárat a[Aspose.CAD for Java oldal](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Győződjön meg arról, hogy a legújabb JDK telepítve van a rendszeren.

- DWG rajz: Készítsen egy DWG rajzfájlt, amelyhez szöveget szeretne hozzáadni.

## Névterek importálása

Java kódban importálja az Aspose.CAD szükséges névtereit:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Most bontsuk fel a megadott kódrészletet több lépésre:

## 1. lépés: Állítsa be a dokumentumkönyvtárat és a DWG fájl elérési útját

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## 2. lépés: Töltse be a DWG képet

```java
Image image = Image.load(dwgPathToFile);
```

## 3. lépés: Hozzon létre CadText objektumot

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);
cadText.setScaleX(0);
```

## 4. lépés: Szöveg hozzáadása a CadImage-hez

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## 5. lépés: A PDF-beállítások beállítása

```java
PdfOptions pdfOptions = new PdfOptions();
```

## 6. lépés: A CadRasterizationOptions konfigurálása

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## 7. lépés: Mentse el a módosított DWG-t PDF formátumban

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Ha követi ezeket a lépéseket, az Aspose.CAD for Java segítségével zökkenőmentesen tud szöveget hozzáadni DWG-rajzaihoz.

## Következtetés

Az Aspose.CAD for Java feljogosítja a fejlesztőket a DWG rajzok programozott fejlesztésére és módosítására. Ez az oktatóanyag világos, lépésenkénti útmutatót kínál a DWG-fájlok szövegének hozzáadásához, bemutatva az Aspose.CAD egyszerűségét és erejét.

## GYIK

### 1. kérdés: Az Aspose.CAD kompatibilis a DWG-fájlok összes verziójával?

1. válasz: Az Aspose.CAD támogatja a DWG-fájlok különféle verzióit, biztosítva a kompatibilitást a CAD-szoftverek széles skálájával.

### 2. kérdés: Testreszabhatom a hozzáadott szöveg betűtípusát és formázását?

2. válasz: Igen, az Aspose.CAD segítségével testreszabhatja a DWG-fájlokhoz hozzáadott szöveg betűtípusát, stílusát és egyéb formázási beállításait.

### 3. kérdés: Elérhető ingyenes próbaverzió az Aspose.CAD for Java számára?

 3. válasz: Igen, felfedezheti az Aspose.CAD szolgáltatásait, ha ingyenes próbaverziót szerez a webhelyről[itt](https://releases.aspose.com/).

### 4. kérdés: Hol találom az Aspose.CAD for Java részletes dokumentációját?

 A4: Lásd a dokumentációt[itt](https://reference.aspose.com/cad/java/) részletes információkért és példákért.

### 5. kérdés: Hogyan kaphatok támogatást vagy kérhetek segítséget az Aspose.CAD-hez?

A5: Látogassa meg a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) segítséget kapni és kapcsolatba lépni a közösséggel.