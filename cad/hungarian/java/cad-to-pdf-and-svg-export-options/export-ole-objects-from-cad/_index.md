---
title: Exportáljon OLE-objektumokat CAD-ből az Aspose.CAD for Java segítségével
linktitle: OLE objektumok exportálása a CAD-ből
second_title: Aspose.CAD Java API
description: Használja ki az Aspose.CAD for Java lehetőségeit. Könnyedén exportálhat OLE objektumokat CAD-fájlokból. Töltse le most a zökkenőmentes CAD-adatkezeléshez.
weight: 10
url: /hu/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportáljon OLE-objektumokat CAD-ből az Aspose.CAD for Java segítségével

## Bevezetés

A számítógéppel segített tervezés (CAD) dinamikus világában az OLE (Object Linking and Embedding) objektumok hatékony kezelése és kibontása kulcsfontosságú. Az Aspose.CAD for Java hatékony megoldást kínál az OLE objektumok CAD-fájlokból történő exportálására. Ez a lépésenkénti útmutató végigvezeti Önt a folyamaton, és biztosítja, hogy az eszközben rejlő lehetőségeket teljes mértékben kihasználja.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételeket teljesítette:

- Java környezet: Győződjön meg arról, hogy be van állítva a Java fejlesztői környezet a gépén.
-  Aspose.CAD for Java: Töltse le és telepítse az Aspose.CAD for Java könyvtárat. A könyvtárat megtalálod a[letöltési link](https://releases.aspose.com/cad/java/).
- CAD-fájlok: Készítse elő az exportálni kívánt OLE-objektumokat tartalmazó CAD-fájlokat.

## Névterek importálása

Kezdésként importálja a szükséges névtereket a Java projektbe. Ezek a névterek biztosítják az Aspose.CAD használatával végzett CAD-fájlok használatához szükséges alapvető osztályokat és funkciókat.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Most bontsuk le az OLE objektumok CAD-ből történő exportálásának folyamatát több lépésre:

## 1. lépés: Állítsa be a dokumentumkönyvtárat

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Győződjön meg arról, hogy a "Dokumentumkönyvtár" helyére a CAD-fájlokat tartalmazó könyvtár elérési útját írja.

## 2. lépés: Határozza meg a CAD fájlneveket

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

 Adja meg a feldolgozni kívánt CAD-fájlok nevét`files` sor.

## 3. lépés: Állítsa be a PNG-exportálási beállításokat

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Konfigurálja a PNG-exportálási beállításokat, beleértve a vektorraszterezési és elrendezési beállításokat.

## 4. lépés: Ismétlés CAD-fájlokon keresztül

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Ismételje meg az egyes megadott CAD-fájlokat, töltse be az Aspose.CAD használatával, és mentse az OLE-objektumokat PNG-képként.

## Következtetés

Ezekkel az egyszerű, de hatékony lépésekkel zökkenőmentesen exportálhat OLE-objektumokat CAD-fájlokból az Aspose.CAD for Java segítségével. Ez a sokoldalú eszköz lehetővé teszi a fejlesztők számára a CAD-adatok hatékony kezelését, és új lehetőségeket nyit meg a CAD-alkalmazások fejlesztésében.

## GYIK

### 1. kérdés: Az Aspose.CAD kompatibilis az összes CAD fájlformátummal?

 1. válasz: Az Aspose.CAD különféle CAD-formátumokat támogat, beleértve a DWG-t, a DXF-et és a DGN-t. Utal[dokumentáció](https://reference.aspose.com/cad/java/) a teljes listához.

### 2. kérdés: Testreszabhatom az OLE objektumok exportálási beállításait?

2. válasz: Igen, az Aspose.CAD kiterjedt lehetőségeket kínál az exportálási beállítások testreszabásához, lehetővé téve a kimenetek egyedi igényeihez szabását.

### 3. kérdés: Elérhető ingyenes próbaverzió az Aspose.CAD számára?

 3. válasz: Igen, felfedezheti az Aspose.CAD képességeit, ha ingyenes próbaverziót szerez[itt](https://releases.aspose.com/).

### 4. kérdés: Hol kaphatok közösségi támogatást az Aspose.CAD-hez?

 4. válasz: Csatlakozzon az Aspose.CAD közösséghez a webhelyen[fórum](https://forum.aspose.com/c/cad/19) segítséget kérni és megosztani tapasztalatait.

### 5. kérdés: Hogyan vásárolhatok licencet az Aspose.CAD-hez?

A5: Látogassa meg a[vásárlási oldal](https://purchase.aspose.com/buy) fejlesztési igényeinek megfelelő licenc megszerzéséhez.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
