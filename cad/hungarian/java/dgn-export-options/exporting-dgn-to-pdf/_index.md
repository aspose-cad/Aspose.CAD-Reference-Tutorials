---
title: Könnyű DGN az AutoCAD PDF-exportáláshoz az Aspose.CAD for Java segítségével
linktitle: DGN exportálása AutoCAD formátumban PDF-be
second_title: Aspose.CAD Java API
description: Tekintse meg a DGN-fájlok AutoCAD formátumba PDF formátumba történő exportálásáról szóló, lépésről lépésre szóló útmutatót az Aspose.CAD for Java használatával. Könnyedén növelheti Java-alkalmazása CAD-kezelési képességeit.
weight: 12
url: /hu/java/dgn-export-options/exporting-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Könnyű DGN az AutoCAD PDF-exportáláshoz az Aspose.CAD for Java segítségével

## Bevezetés

Üdvözöljük ebben az átfogó oktatóanyagban, amely az Aspose.CAD for Java használatáról szól DGN-fájlok AutoCAD formátumban történő exportálásához PDF-be. Ha javítani szeretné Java-alkalmazása CAD-fájlok kezelésére való képességét, az Aspose.CAD kiváló választás. Ebben az oktatóanyagban lépésről lépésre végigvezetjük a DGN-fájlok exportálásán.


## Előfeltételek
Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:
-  Aspose.CAD könyvtár: Győződjön meg arról, hogy telepítve van a Java Aspose.CAD könyvtára. Letöltheti[itt](https://releases.aspose.com/cad/java/).
- Dokumentumkönyvtár: Állítson be egy dokumentumkönyvtárat, ahol a bemeneti és kimeneti fájlokat tárolja.

## Csomagok importálása

Java projektjében importálja a szükséges csomagokat az Aspose.CAD funkciók eléréséhez:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Most bontsuk fel a példakódot több lépésre:

## 1. lépés: Határozza meg a fájl elérési útját

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Ügyeljen arra, hogy a „Dokumentumkönyvtár” kifejezést a fájlok tényleges elérési útjára cserélje.

## 2. lépés: Töltse be a DGN képet

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Töltse be a DGN fájlt az Aspose.CAD segítségével.

## 3. lépés: Állítsa be a PDF-exportálási beállításokat

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Adott nézetek exportálása
options.setVectorRasterizationOptions(vectorOptions);
```

Határozza meg a PDF-exportálási beállításokat, beleértve az oldalméreteket és az elrendezési beállításokat.

## 4. lépés: Mentse el a PDF fájlt

```java
objImage.save(outFile, options);
```

Mentse el az exportált PDF fájlt.

Ismételje meg ezeket a lépéseket minden további konvertálni kívánt DGN-fájl esetén. Gratulálunk! Sikeresen exportálta a DGN fájlokat AutoCAD formátumba PDF formátumban az Aspose.CAD for Java segítségével.

## Következtetés

Ebben az oktatóanyagban azt vizsgáltuk, hogyan lehet kihasználni az Aspose.CAD for Java-t az alkalmazás CAD-fájlkezelési képességeinek javítására. A könnyen követhető lépések és kódpéldák segítségével most zökkenőmentesen exportálhatja a DGN fájlokat AutoCAD formátumba PDF formátumban.

## GYIK

### 1. kérdés: Az Aspose.CAD kompatibilis az összes CAD fájlformátummal?

1. válasz: Igen, az Aspose.CAD a CAD formátumok széles skáláját támogatja, sokoldalúságot biztosítva a különféle fájltípusok kezelésében.

### 2. kérdés: Testreszabhatom a PDF-exportálási beállításokat?

A2: Abszolút. Ahogy az oktatóanyagban is látható, az igényeinek megfelelően beállíthatja az olyan beállításokat, mint például az oldalméretek és az elrendezések.

### 3. kérdés: Hol találhatok további támogatást vagy segítséget?

 A3: Látogassa meg a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) közösségi támogatásra és beszélgetésekre.

### 4. kérdés: Van ingyenes próbaverzió?

 4. válasz: Igen, hozzáférhet az ingyenes próbaverzióhoz[itt](https://releases.aspose.com/).

### 5. kérdés: Hogyan szerezhetek ideiglenes engedélyt?

 V5: Szerezzen ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
