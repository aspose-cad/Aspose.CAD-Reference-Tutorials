---
date: 2026-01-02
description: Ismerje meg, hogyan exportálhatja a DWG-t PDF-be, engedélyezheti a rejtett
  vonalakat, és konvertálhatja a DWG-t PDF-be az Aspose.CAD for Java segítségével
  ebben a lépésről‑lépésre útmutatóban.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: DWG exportálása PDF-be rejtett vonalakkal – Aspose.CAD for Java
url: /hu/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG exportálása PDF-be rejtett vonalakkal – Aspose.CAD for Java

## Bevezetés

Ebben az útmutatóban megtanulja, hogyan **exportálja a DWG-t PDF-be** a rejtett vonalak megőrzésével az Aspose.CAD for Java használatával. Akár **DWG-t PDF-re kell konvertálni**, akár egy **dwg to pdf tutorial**‑stílusú útmutatót szeretne létrehozni, vagy egyszerűen **DWG-t PDF-be menteni** rejtett vonal támogatással, lépésről lépésre végigvezetjük. A végére egy kész, használatra kész megoldást kap, amelyet bármely Java projektbe beilleszthet.

## Gyors válaszok
- **Mi a tutorial tartalma?** A rejtett vonalak megjelenítésének engedélyezése a DWG PDF-be exportálásakor az Aspose.CAD for Java segítségével.  
- **Melyik elsődleges műveletet hajtja végre?** `export dwg as pdf`.  
- **Szükségem van licencre?** Egy ingyenes próba a teszteléshez megfelelő; a termeléshez kereskedelmi licenc szükséges.  
- **Mik a előfeltételek?** Java fejlesztői környezet, Aspose.CAD for Java könyvtár, és DWG fájlok.  
- **Mennyi időt vesz igénybe a megvalósítás?** Körülbelül 10‑15 perc egy alap beállításhoz.

## Mi az a „export dwg as pdf”?
A DWG fájl PDF-be exportálása a vektor‑alapú CAD rajzot hordozható dokumentumformátummá alakítja, miközben megőrzi a rétegeket, vonaltípusokat és az opcionális rejtett vonal megjelenítést. Ez megkönnyíti a CAD tervek megosztását az érintettekkel, akiknek nincs CAD szoftverük.

## Miért engedélyezzük a rejtett vonalakat exportáláskor?
A rejtett vonalak tisztább vizuális ábrázolást biztosítanak a komplex 3D modellek 2‑D oldalon, biztosítva, hogy csak a látható élek legyenek hangsúlyosak. Ez javítja az olvashatóságot és gyakran szükséges a mérnöki dokumentációban.

## Előfeltételek

1. **Aspose.CAD for Java** – töltse le a könyvtárat a hivatalos oldalról [itt](https://releases.aspose.com/cad/java/).  
2. **DWG fájlok** – rendelkezzen a forrás DWG rajzokkal egy ismert könyvtárban.  
3. **Java fejlesztői környezet** – JDK 8+ és a kedvenc IDE-je (Eclipse, IntelliJ, stb.).  

Most, hogy minden készen áll, merüljünk el a kódban.

## Namespace-ek importálása

Kezdje a szükséges osztályok importálásával, hogy a CAD képekkel és PDF beállításokkal dolgozhasson.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## 1. lépés: Projekt beállítása

Hozzon létre egy Java projektet, és adja hozzá az Aspose.CAD JAR-t a build útvonalához. Ezután határozza meg a DWG fájlokat tartalmazó könyvtárat.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro tipp:** Használjon abszolút útvonalat, vagy konfiguráljon relatív útvonalat a projekt erőforrások mappája alapján.

## 2. lépés: DWG fájl betöltése

Töltse be a forrás DWG fájlt egy `CadImage` objektumba, hogy manipulálni tudja.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## 3. lépés: Rasterizálási beállítások konfigurálása

Válassza ki a beilleszteni kívánt rétegeket, és állítsa be az oldalméretet az eredeti rajzhoz igazodva. Itt engedélyezzük a rejtett vonalak megjelenítését a layout megadásával.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## 4. lépés: PDF beállítások megadása

Adja meg az Aspose.CAD-nek, hogy rasterizálja a vektor adatokat PDF-be, a „Model” layout használatával, hogy a rejtett vonalak rejtve maradjanak.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 5. lépés: Az eredmény mentése

Végül exportálja a DWG-t PDF fájlként. A rejtett vonalak a beállított layout szerint lesznek kezelve.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Gyakori hiba:** Ha elfelejti a layout beállítását `"Model"`-re, akkor minden vonal (beleértve a rejtetteket is) szilárdként jelenik meg a PDF-ben.

## Következtetés

Most már rendelkezik egy teljes, termelésre kész módszerrel a **DWG PDF-be exportálásához** rejtett vonal támogatással az Aspose.CAD for Java használatával. Ez a megközelítés integrálható kötegelt feldolgozó eszközökbe, webszolgáltatásokba vagy asztali alkalmazásokba a CAD‑PDF konverzió automatizálásához.

## Gyakran Ismételt Kérdések

### Q1: Használhatom az Aspose.CAD for Java-t más CAD fájlformátumokkal?
A1: Igen, az Aspose.CAD számos CAD formátumot támogat, például DWG, DXF, DWF és egyebek.

### Q2: Elérhető ingyenes próba az Aspose.CAD for Java-hoz?
A2: Igen, az ingyenes próbát [itt](https://releases.aspose.com/) találja.

### Q3: Hogyan kaphatok támogatást az Aspose.CAD for Java-hoz?
A3: Látogassa meg az Aspose.CAD fórumot [itt](https://forum.aspose.com/c/cad/19) a közösségi támogatásért.

### Q4: Hol találhatók részletes dokumentációk az Aspose.CAD for Java-hoz?
A4: Tekintse meg a dokumentációt [itt](https://reference.aspose.com/cad/java/).

### Q5: Vásárolhatok ideiglenes licencet az Aspose.CAD for Java-hoz?
A5: Igen, ideiglenes licencet szerezhet [itt](https://purchase.aspose.com/temporary-license/).

### Q6: Ez a módszer működik a DWG PDF-re konvertálásához fej nélküli szerverkörnyezetben is?
A6: Teljesen. Mivel a kód csak az Aspose.CAD API-t használja, UI függőségek nélkül fut, így ideális a szerver‑oldali automatizáláshoz.

**Utolsó frissítés:** 2026-01-02  
**Tesztelt verzió:** Aspose.CAD for Java 24.12  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}