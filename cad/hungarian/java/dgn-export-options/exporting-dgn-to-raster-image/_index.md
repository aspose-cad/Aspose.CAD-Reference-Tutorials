---
title: Java DGN konvertálása JPEG formátumba az Aspose.CAD oktatóanyaggal
linktitle: DGN exportálása AutoCAD formátumban raszteres képformátumba
second_title: Aspose.CAD Java API
description: Ismerje meg, hogyan exportálhat DGN-fájlokat JPEG-képekké Java nyelven az Aspose.CAD használatával. Ez a lépésről lépésre haladó útmutató könnyedén végigvezeti a folyamaton.
type: docs
weight: 13
url: /hu/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## Bevezetés

Üdvözöljük ebben az átfogó oktatóanyagban, amely a DGN (Design) fájlok raszteres képformátumba történő exportálásáról szól az Aspose.CAD for Java használatával. Az Aspose.CAD egy hatékony könyvtár, amely lehetővé teszi a Java fejlesztők számára, hogy zökkenőmentesen dolgozzanak CAD fájlokkal. Ebben az oktatóanyagban végigvezetjük Önt a DGN-fájlok JPEG-képekké konvertálásának folyamatán, lépésről lépésre és kódpéldákkal.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételeket teljesítette:
1.  Aspose.CAD könyvtár: Győződjön meg arról, hogy telepítve van az Aspose.CAD for Java könyvtár. Letöltheti[itt](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Győződjön meg arról, hogy a Java telepítve van a gépen.
3. Integrált fejlesztői környezet (IDE): Használjon Java-kompatibilis IDE-t, például az IntelliJ-t vagy az Eclipse-t.

## Csomagok importálása

Java-projektjében importálja az Aspose.CAD-hez szükséges csomagokat. Adja hozzá a következő sorokat a kódhoz:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## 1. lépés: Töltse be a DGN fájlt

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## 2. lépés: JpegOptions objektum létrehozása

```java
ImageOptionsBase options = new JpegOptions();
```

## 3. lépés: Raszterezési beállítások hozzárendelése

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## 4. lépés: Mentse el a konvertált képet

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Ismételje meg ezeket a lépéseket az adott DGN-fájloknál, és ennek megfelelően állítsa be a fájl elérési útját.

## Következtetés

Gratulálunk! Sikeresen megtanulta, hogyan exportálhat DGN fájlokat raszteres képformátumba az Aspose.CAD for Java segítségével. Ez az oktatóanyag felvértezte Önt azokkal az ismeretekkel, amelyekkel beépítheti ezt a funkciót Java-alkalmazásaiba.

## GYIK

### 1. kérdés: Használhatom az Aspose.CAD for Java-t más CAD fájlformátumokkal?

1. válasz: Igen, az Aspose.CAD különféle CAD formátumokat támogat, így sokoldalú megoldást kínál a Java fejlesztők számára.

### 2. kérdés: Elérhető az Aspose.CAD for Java ingyenes próbaverziója?

 2. válasz: Igen, hozzáférhet az ingyenes próbaverzióhoz[itt](https://releases.aspose.com/).

### 3. kérdés: Hol találom az Aspose.CAD for Java dokumentációját?

 V3: Lásd a dokumentációt[itt](https://reference.aspose.com/cad/java/).

### 4. kérdés: Hogyan kaphatok támogatást az Aspose.CAD for Java számára?

 4. válasz: Látogassa meg a támogatási fórumot[itt](https://forum.aspose.com/c/cad/19).

### 5. kérdés: Hol vásárolhatok licencet az Aspose.CAD for Java számára?

 V5: Vásárolhat licencet[itt](https://purchase.aspose.com/buy).