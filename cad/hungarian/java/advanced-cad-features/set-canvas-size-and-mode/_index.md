---
title: Állítsa be a vászon méretét és módját
linktitle: Állítsa be a vászon méretét és módját
second_title: Aspose.CAD Java API
description: Fedezze fel az Aspose.CAD for Java erejét a vászon méretének és módjának beállításáról szóló, lépésről lépésre bemutatott útmutatónkkal. Könnyedén konvertálhat CAD fájlokat PDF és TIFF formátumokká.
weight: 16
url: /hu/java/advanced-cad-features/set-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Állítsa be a vászon méretét és módját

## Bevezetés

Szeretné kihasználni az Aspose.CAD for Java erejét a CAD-konverziós folyamat javítása érdekében? Ez az átfogó útmutató végigvezeti a vászonméret és -mód beállításának lépésein az Aspose.CAD for Java használatával. Akár tapasztalt fejlesztő, akár csak most kezdi, ez az oktatóanyag a szükséges betekintést nyújtja.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételeket teljesítette:

-  Aspose.CAD for Java: Győződjön meg arról, hogy az Aspose.CAD könyvtár telepítve van a Java környezetben. Letöltheti[itt](https://releases.aspose.com/cad/java/).

- Dokumentumkönyvtár: Állítson be egy dokumentumkönyvtárat a CAD-fájlok tárolására. Erre a könyvtárra hivatkozunk az oktatóprogram lépéseiben.

Most pedig kezdjük a lépésről lépésre bemutatott útmutatóval.

## Névterek importálása

Ebben a lépésben importáljuk a szükséges névtereket az Aspose.CAD projekt elindításához.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 1. lépés: Importáljon Aspose.CAD osztályokat

```java
// Az erőforrás-könyvtár elérési útja.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 Ebben a kódrészletben beállítjuk az erőforrás-könyvtár elérési útját, és betöltünk egy DXF fájlt az Aspose.CAD segítségével`Image` osztály.

## 2. lépés: Állítsa be a CadRasterizationOptions tulajdonságait

```java
// Hozzon létre egy CadRasterizationOptions példányt, és állítsa be a különböző tulajdonságait
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Itt létrehozunk egy példányt`CadRasterizationOptions` és konfigurálhat olyan tulajdonságokat, mint az oldalszélesség, az oldal magassága és a méretezési beállítások.

## 3. lépés: PdfOptions létrehozása és VectorRasterizationOptions beállítása

```java
// Hozzon létre egy PdfOptions példányt
PdfOptions pdfOptions = new PdfOptions();

// Állítsa be a VectorRasterizationOptions tulajdonságot
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Most létrehozunk a`PdfOptions` példányt, és állítsa be`VectorRasterizationOptions` tulajdonságot a korábban beállítotthoz`CadRasterizationOptions`.

## 4. lépés: Exportálás PDF-be

```java
// CAD exportálása PDF-be
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Végül a CAD képet PDF fájlba mentjük a megadott opciókkal.

## 5. lépés: Hozzon létre TiffOptions-t és állítsa be a VectorRasterizationOptions-t

```java
// Hozzon létre egy TiffOptions példányt
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Állítsa be a VectorRasterizationOptions tulajdonságot
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ebben a lépésben beállítjuk a`TiffOptions` példányt, és konfigurálja azt`VectorRasterizationOptions` ingatlan.

## 6. lépés: Exportálás TIFF formátumba

```java
// CAD exportálása TIFF formátumba
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Végül a CAD-képet TIFF-fájlba mentjük a megadott beállításokkal.

## Következtetés

 Gratulálunk! Sikeresen beállította a vászon méretét és módját az Aspose.CAD for Java segítségével. Ez az oktatóanyag szilárd alapot biztosít CAD-konverziós projektjeihez. Fedezzen fel további funkciókat és lehetőségeket a[Aspose.CAD dokumentáció](https://reference.aspose.com/cad/java/).

## GYIK

### 1. kérdés: Használhatom az Aspose.CAD for Java-t más Java-keretrendszerekkel?

1. válasz: Igen, az Aspose.CAD-et úgy tervezték, hogy zökkenőmentesen integrálódjon a különböző Java-keretrendszerekkel.

### 2. kérdés: Rendelkezésre áll ideiglenes licenc az Aspose.CAD számára?

 V2: Igen, beszerezhet ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).

### 3. kérdés: Hol kaphatok közösségi támogatást az Aspose.CAD-hez?

 A3: Látogassa meg a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) közösségi támogatásra és beszélgetésekre.

### 4. kérdés: Kipróbálhatom ingyenesen az Aspose.CAD-et?

 A4: Abszolút! Ingyenes próbaverzió[itt](https://releases.aspose.com/).

### 5. kérdés: Hogyan vásárolhatom meg az Aspose.CAD for Java-t?

 A5: Vásárolja meg a terméket[itt](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
