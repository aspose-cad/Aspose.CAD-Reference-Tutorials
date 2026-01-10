---
date: 2026-01-10
description: Tanulja meg, hogyan exportálhatja a DGN-t DWG-be, és konvertálhatja a
  MicroStation DGN-t AutoCAD DWG-re az Aspose.CAD for Java segítségével. Lépésről‑lépésre
  útmutató.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: DGN exportálása DWG-be az Aspose.CAD for Java segítségével
url: /hu/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN exportálása DWG-be az Aspose.CAD for Java segítségével

## Bevezetés

Ebben az útmutatóban megtanulja, hogyan **exportálja a dgn-t dwg-re** és hogyan ágyazhat be egy MicroStation DGN tervet egy AutoCAD DWG fájlba az Aspose.CAD Java könyvtár segítségével. Akár régi MicroStation rajzok migrálásáról van szó, akár DGN alárajzok DWG elrendezésekkel való kombinálásáról, ez a leírás minden lépést végigvezet – a környezet beállításától a végleges DWG PDF előnézetének generálásáig.

## Gyors válaszok
- **Mit ér el a „export dgn to dwg” művelettel?** Egy DGN alárajzot ágyaz be egy DWG-be, lehetővé téve a zökkenőmentes megtekintést AutoCAD-ben.
- **Milyen formátumba exportálhatom a végeredményt gyors előnézethez?** **Exportálhat CAD fájlt PDF-be** a `PdfOptions` használatával.
- **Szükség van licencre a kód futtatásához?** Ideiglenes vagy megvásárolt Aspose.CAD licenc szükséges a termelési környezetben.
- **Mely Java verzió támogatott?** A Java 8 vagy újabb verziók működnek a legújabb Aspose.CAD for Java kiadással.
- **Elérhető ingyenes próba?** Igen – töltsön le egy próbaverziót az Aspose weboldaláról.

## Mi az a „export dgn to dwg”?
A DGN exportálása DWG-be azt jelenti, hogy egy MicroStation DGN tervet konvertál vagy beágyaz egy AutoCAD DWG rajz alárajzaként. Ez lehetővé teszi a CAD szakemberek számára, hogy meglévő DGN eszközöket használjanak anélkül, hogy a geometriát újra kellene létrehozniuk.

## Miért konvertáljuk a MicroStation DGN-t AutoCAD DWG-re?
- **Együttműködés:** Az AutoCAD-et használó csapatok közvetlenül megtekinthetik és szerkeszthetik a DGN tartalmat.
- **Standardizálás:** A DWG a de‑facto formátum számos downstream folyamatban (pl. PDF generálás, 3D renderelés).
- **Megőrzés:** Az eredeti DGN hivatkozások érintetlenek maradnak, csökkentve az adatvesztést.

## Előfeltételek

Mielőtt elkezdenénk, győződjön meg róla, hogy az alábbiak rendelkezésre állnak:
1. **Aspose.CAD könyvtár:** Töltse le és telepítse az Aspose.CAD könyvtárat Java-hoz. A könyvtárat megtalálja [itt](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** Győződjön meg róla, hogy a Java telepítve van a rendszerén.
3. **Integrált fejlesztői környezet (IDE):** Válasszon egy Java IDE-t, például Eclipse vagy IntelliJ, a gördülékeny fejlesztéshez.

## Csomagok importálása

A Java projektjében importálja a szükséges Aspose.CAD csomagokat a CAD fájlok manipulálásához. Példa:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## 1. lépés: Fájlútvonalak beállítása

Határozza meg a bemeneti és kimeneti útvonalakat a DWG fájlhoz. Frissítse a `dataDir`, `fileName` és `outPath` változókat ennek megfelelően.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## 2. lépés: PdfOptions példány létrehozása

Hozzon létre egy `PdfOptions` példányt, mivel **a CAD fájlt PDF-be exportáljuk** a gyors ellenőrzéshez.

```java
PdfOptions exportOptions = new PdfOptions();
```

## 3. lépés: DWG fájl betöltése

Töltsön be egy meglévő DWG fájlt képként, és konvertálja `CadImage` típusra.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## 4. lépés: Entitások bejárása

Iteráljon végig a DWG fájl minden entitásán, és ellenőrizze, hogy képaddefinícióról van‑e szó. Ha igen, szerezze be a külső hivatkozást az objektumra.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## 5. lépés: Rasterizálási beállítások definiálása

Állítsa be a `CadRasterizationOptions` objektum paramétereit, beleértve az oldal szélességét, magasságát, elrendezéseket és háttérszínt.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## 6. lépés: Vektoros rasterizálási beállítások

Állítsa be a vektoros rasterizálási opciókat az exportáláshoz.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## 7. lépés: DWG exportálása PDF-be

Végül exportálja a DWG-t PDF-be a `save` metódus meghívásával.

```java
cadImage.save(outPath, exportOptions);
```

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| **Nem jelenik meg DGN alárajz** | A DWG nem tartalmaz `DGNUNDERLAY` entitást. | Ellenőrizze, hogy a forrás DWG tartalmaz-e DGN hivatkozást. |
| **A PDF üres** | Rasterizálási beállítások nulla méretűek vagy rossz elrendezés. | Győződjön meg róla, hogy a `setPageWidth`/`setPageHeight` pozitív, és a `setLayouts` egyezik a DWG elrendezés nevével. |
| **Licenckivétel** | Érvényes Aspose.CAD licenc hiánya. | Alkalmazzon ideiglenes vagy megvásárolt licencet, mielőtt bármely API metódust meghívná. |

## Gyakran ismételt kérdések

### Q1: Hol találom az Aspose.CAD for Java dokumentációját?

A dokumentáció [itt](https://reference.aspose.com/cad/java/) érhető el.

### Q2: Hogyan tölthetem le az Aspose.CAD könyvtárat Java-hoz?

A könyvtárat letöltheti [erről a linkről](https://releases.aspose.com/cad/java/).

### Q3: Elérhető ingyenes próba az Aspose.CAD for Java-hoz?

Igen, az ingyenes próbaverziót [itt](https://releases.aspose.com/) találja.

### Q4: Hol szerezhetek ideiglenes licencet az Aspose.CAD for Java-hoz?

Ideiglenes licencet kaphat [itt](https://purchase.aspose.com/temporary-license/).

### Q5: Segítségre vagy kérdésekre van szükségem?

Látogassa meg az Aspose.CAD közösségi támogatási fórumot [itt](https://forum.aspose.com/c/cad/19).

### Q6: Vissza tudom-e konvertálni a kapott PDF-et DWG-be?

A PDF egy raster előnézet; a visszakonvertáláshoz külön fordított‑mérnöki eszköz szükséges.

### Q7: Ez a megközelítés működik más CAD formátumokkal, például DWF vagy DXF?

Igen, az Aspose.CAD számos formátumot támogat; csak a fájlkiterjesztést és a rasterizálási beállításokat kell módosítani.

---

**Legutóbb frissítve:** 2026-01-10  
**Tesztelve:** Aspose.CAD for Java 24.11  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}