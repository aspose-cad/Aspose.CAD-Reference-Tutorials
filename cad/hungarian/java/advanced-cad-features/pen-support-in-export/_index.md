---
title: Toll támogatás az exportálásban
linktitle: Toll támogatás az exportálásban
second_title: Aspose.CAD Java API
description: Mester toll-testreszabás a CAD-exportban az Aspose.CAD for Java segítségével. Kövesse lépésenkénti útmutatónkat a zökkenőmentes integráció érdekében.
weight: 13
url: /hu/java/advanced-cad-features/pen-support-in-export/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Toll támogatás az exportálásban

## Bevezetés

CAD (Computer-Aided Design) konverziók folyamatosan fejlődő környezetében az Aspose.CAD for Java hatékony eszközként jelenik meg, amely széleskörű lehetőségeket kínál a CAD-fájlok kezeléséhez. Sokoldalú funkciói közül kiemelkedik a toll exportálás közbeni testreszabásának támogatása, amely lehetővé teszi a felhasználók számára, hogy személyre szabják az exportált képek megjelenését. Ez az oktatóanyag végigvezeti Önt a toll támogatásának az exportálási funkcióban való kihasználásán, a Java használatával való gyakorlati megvalósításra összpontosítva.

## Előfeltételek

Mielőtt belemerülne az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételekkel rendelkezik:

- Java fejlesztői környezet: Győződjön meg arról, hogy működő Java fejlesztői környezet van beállítva a gépén.

-  Aspose.CAD Library: Töltse le és integrálja az Aspose.CAD könyvtárat Java projektjébe. Megtalálhatod a könyvtárat[itt](https://releases.aspose.com/cad/java/).

Most ugorjunk bele az oktatóanyagba, és fedezzük fel a tolltámogatás kihasználásának lépéseit a CAD-exportálás során.

## Névterek importálása

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## 1. lépés: Határozza meg a dokumentumkönyvtárat

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Győződjön meg arról, hogy a "Dokumentumkönyvtár" helyett a CAD-dokumentumok tényleges elérési útja szerepel.

## 2. lépés: Töltse be a CAD-fájlt

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

Ez a lépés magában foglalja a CAD-fájl, jelen esetben a "conic_pyramid.dxf" betöltését az Aspose.CAD könyvtár használatával.

## 3. lépés: Konfigurálja a raszterezési beállításokat

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

Állítsa be az oldal szélességét és magasságát saját igényei szerint. Ezek az értékek határozzák meg az exportált kép méreteit.

## 4. lépés: A tollbeállítások testreszabása

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

Igény szerint testreszabhatja a tollak kezdő- és végsapkáját. Ez a testreszabás a CadImage objektum különféle képformátumokba történő exportálásakor érvényes.

## 5. lépés: Konfigurálja a PDF-exportálási beállításokat

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Adja meg a vektorraszterezési beállításokat, beleértve a korábban beállított raszterezési beállításokat is.

## 6. lépés: Mentse el az exportált PDF-fájlt

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Mentse az exportált PDF-fájlt a megadott fájlnévvel (ebben a példában "9LHATT-A56_generated.pdf") és a konfigurált beállításokkal.

## Következtetés

Összefoglalva, a toll támogatásának kihasználása a CAD-exportálás során az Aspose.CAD for Java segítségével lehetővé teszi a felhasználók számára, hogy testreszabják az exportált képek megjelenését. Ennek a lépésenkénti útmutatónak a követésével megtanulta, hogyan integrálhatja zökkenőmentesen a toll testreszabását a CAD-konverziós munkafolyamatba.

## GYIK

### 1. kérdés: Testreszabhatom a tollbeállításokat a PDF-től eltérő formátumokhoz?

1. válasz: Igen, az ebben az oktatóanyagban bemutatott toll-testreszabás különféle képformátumokra alkalmazható, beleértve a PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF és WMF képformátumokat.

### 2. kérdés: Hogyan kezelhetem a tollak különböző kezdő- és végsapkáját?

 A2: Használja a`PenOptions` osztályban beállíthatja a kívánt kezdő- és végsapkákat, rugalmasságot biztosítva a vonalak megjelenésének meghatározásában.

### 3. kérdés: Mi van, ha nem adok meg tollbeállításokat?

3. válasz: Ha a tollbeállítások nincsenek kifejezetten beállítva, a rendszer az alapértelmezett tollakat fogja használni, amelyek a különböző kontextusokban változhatnak.

### 4. kérdés: Vannak-e konkrét megfontolások a raszterezési beállításokkal kapcsolatban?

A4: Állítsa be az oldal szélességét és magasságát a raszterezési beállításoknál az exportált kép méreteinek szabályozásához.

### 5. kérdés: Hol találhatok további támogatást vagy közösségi megbeszéléseket?

 5. válasz: Fedezze fel az Aspose.CAD közösségi fórumot a címen[itt](https://forum.aspose.com/c/cad/19) támogatásért és megbeszélésekért.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
