---
date: 2026-01-04
description: Ismerje meg, hogyan **menthet CAD fájlt PNG‑ként**, és hogyan exportálhatja
  könnyedén az OLE objektumokat CAD fájlokból az Aspose.CAD for Java használatával.
  Gyors beállítás, teljes kódminta és legjobb gyakorlatok tippek.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: CAD mentése PNG formátumba és OLE-objektumok exportálása az Aspose.CAD for
  Java-val
url: /hu/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD mentése PNG formátumban és OLE objektumok exportálása az Aspose.CAD for Java segítségével

## Introduction

A számítógéppel segített tervezés (CAD) gyorsan változó világában a **CAD mentése PNG** formátumban, miközben a beágyazott OLE (Object Linking and Embedding) objektumokat kinyerjük, jelentősen felgyorsíthatja a munkafolyamatot. Akár kötegelt konverziós eszközt épít, akár webportálhoz készít előnézeti képeket, vagy egyszerűen OLE tartalmat szeretne archiválni, az Aspose.CAD for Java tiszta, programozható megoldást kínál. Ebben az útmutatóban végigvezetjük a teljes folyamatot, a projekt beállításától az egyes OLE objektumok PNG képként történő exportálásáig.

## Quick Answers
- **Exportálhatok OLE objektumokat közvetlenül PNG‑be?** Igen – az Aspose.CAD betölti a CAD fájlt, és lehetővé teszi, hogy minden elrendezést PNG‑be rasterizáljon.  
- **Milyen Java verzió szükséges?** Java 8 vagy újabb.  
- **Szükségem van licencre ehhez a funkcióhoz?** Egy ingyenes próba verzió elegendő értékeléshez; licenc szükséges a termeléshez.  
- **Megmarad a vektor adat?** A PNG rasterizálás megőrzi a vizuális hűséget, de a kimenet raster, nem vektor.  
- **Támogatott a kötegelt feldolgozás?** Teljesen – iteráljon a fájlok tömbjén, ahogy a kódmintában látható.

## Prerequisites

Mielőtt elkezdené, győződjön meg róla, hogy a következők rendelkezésre állnak:

- **Java Development Kit (JDK)** – Java 8+ telepítve és konfigurálva.  
- **Aspose.CAD for Java** – Töltse le a legújabb könyvtárat a [download link](https://releases.aspose.com/cad/java/).  
- **CAD forrásfájlok** – Bármely DWG/DXF/DGN fájl, amely OLE objektumokat tartalmaz, amelyeket exportálni szeretne.

## Import Namespaces

A CAD fájlokkal való munka érdekében importálni kell a core Aspose.CAD osztályokat. Tartsa meg az import blokkot pontosan úgy, ahogy látható – ez biztosítja a később a tutorialban használt osztályokat.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## How to Save CAD as PNG

Az alábbiakban egy tömör, lépésről‑lépésre útmutatót talál, amely **bemutatja, hogyan exportálhat OLE objektumokat és mentheti a CAD‑t PNG‑ként**. Minden lépés egy rövid magyarázatot tartalmaz, majd a pontos kódot, amelyet a projektjébe másolhat.

### Step 1: Set Your Document Directory

Adja meg azt a mappát, amely a CAD rajzokat tartalmazza. Cserélje le a helyőrzőt a gépén lévő tényleges útvonalra.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Step 2: Define CAD File Names

Sorolja fel az összes CAD fájlt, amelyet feldolgozni kíván. Tetszőlegesen sok bejegyzést adhat hozzá.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Step 3: Set PNG Export Options

Állítsa be a rasterizálási beállításokat. Itt egy konkrét elrendezést (`Layout1`) célozunk meg, és az alapértelmezett PNG opciókat használjuk.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Step 4: Iterate Through CAD Files and Save as PNG

Töltse be minden CAD fájlt, rasterizálja az OLE objektumokat, és írja ki a PNG kimenetet. Az `_out.png` utótag segít az előállított képek azonosításában.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Common Issues and Solutions

| Problem | Why it Happens | Fix |
|---------|----------------|-----|
| **`Image.load` throws `FileNotFoundException`** | A `dataDir` útvonal helytelen vagy a fájlnév el van gépelve. | Ellenőrizze a könyvtár karakterláncot, és győződjön meg róla, hogy a fájlnevek pontosan egyeznek, beleértve a szóközöket is. |
| **Output PNG is blank** | Az elrendezés neve nem létezik a forrás CAD fájlban. | Használja a `cadImage.getLayouts()` metódust az elérhető elrendezések listázásához, majd frissítse a `rasterizationOptions.setLayouts(...)` beállítást. |
| **Large CAD files cause OutOfMemoryError** | A magas felbontású képek rasterizálása sok heap memóriát igényel. | Növelje a JVM heap méretét (`-Xmx2g`) vagy csökkentse a rasterizálási felbontást a `rasterizationOptions.setResolution(...)` segítségével. |

## FAQ's

### Q1: Is Aspose.CAD compatible with all CAD file formats?

A1: Az Aspose.CAD számos CAD formátumot támogat, többek között a DWG, DXF és DGN formátumokat. A teljes lista megtalálható a [documentation](https://reference.aspose.com/cad/java/) oldalon.

### Q2: Can I customize the export settings for OLE objects?

A2: Igen, az Aspose.CAD kiterjedt lehetőségeket biztosít az export beállítások testreszabásához, így a kimenetet az Ön specifikus igényeihez igazíthatja.

### Q3: Is there a free trial available for Aspose.CAD?

A3: Igen, az Aspose.CAD képességeit ingyenes próba verzióval is kipróbálhatja a [here](https://releases.aspose.com/) linken.

### Q4: Where can I get community support for Aspose.CAD?

A4: Csatlakozzon az Aspose.CAD közösséghez a [forum](https://forum.aspose.com/c/cad/19) oldalon, ahol segítséget kérhet és megoszthatja tapasztalatait.

### Q5: How can I purchase a license for Aspose.CAD?

A5: Látogassa meg a [purchase page](https://purchase.aspose.com/buy) oldalt, és szerezzen be egy olyan licencet, amely megfelel fejlesztési igényeinek.

## Conclusion

Az öt egyszerű lépés követésével **mentheti a CAD‑t PNG‑ként**, és kinyerheti az összes beágyazott OLE objektumot néhány Java kódsorral. Ez a megközelítés ideális kötegelt konverziókhoz, automatizált jelentéskészítéshez vagy bármilyen olyan helyzethez, ahol a CAD tartalom raster képeire van szükség manuális exportálás nélkül. Nyugodtan kísérletezzen különböző rasterizálási beállításokkal, hogy a minőség és a teljesítmény igényeinek megfelelően optimalizálja a folyamatot.

---

**Last Updated:** 2026-01-04  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}