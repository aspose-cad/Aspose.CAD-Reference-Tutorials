---
date: 2026-03-02
description: Fedezze fel az Aspose.CAD for Java lehetőségeit. Könnyedén exportáljon
  OLE-objektumokat és **mentse a CAD-et PNG formátumban**. Töltse le most a zökkenőmentes
  CAD adatkezelésért.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: CAD mentése PNG formátumban – OLE objektumok exportálása az Aspose.CAD for
  Java segítségével
url: /hu/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD mentése PNG‑ként – OLE objektumok exportálása az Aspose.CAD for Java segítségével

## Bevezetés

A számítógépes tervezés (CAD) dinamikus világában az OLE (Object Linking and Embedding) objektumok hatékony kezelése és kinyerése – valamint a **CAD mentése PNG‑ként** képesség – kulcsfontosságú a jelentéskészítés, webes előnézet vagy archiválás során. Az Aspose.CAD for Java egy erőteljes, kódfolyamra épülő megoldást kínál, amely lehetővé teszi az OLE objektumok exportálását és a CAD rajzok magas minőségű PNG képekké konvertálását néhány kódsorral.

## Gyors válaszok
- **Mit csinál az Aspose.CAD?** CAD fájlokat (DWG, DXF, DGN stb.) olvas, manipulál és konvertál anélkül, hogy natív CAD szoftverre lenne szükség.  
- **Menthetek CAD‑t PNG‑ként?** Igen – használja a `PngOptions`‑t a `CadRasterizationOptions`‑szal együtt bármely elrendezés rasterizálásához.  
- **Hogyan exportáljam az OLE objektumokat?** Töltse be a CAD fájlt a `Image.load`‑nal, és mentse el minden OLE‑t tartalmazó elrendezést PNG‑ként.  
- **Szükségem van licencre?** Ingyenes próbaverzió elérhető; a kereskedelmi licenc eltávolítja a kiértékelési korlátozásokat.  
- **Milyen Java verzió szükséges?** A Java 8 vagy újabb teljes mértékben támogatott.

## Mi az a **CAD mentése PNG‑ként**?
A CAD mentése PNG‑ként azt jelenti, hogy a vektor‑alapú CAD rajzokat pixel‑alapú PNG képpé rasterizáljuk. Ez a konverzió akkor hasznos, amikor könnyű, minden platformon megjeleníthető formátumra van szükség weboldalakhoz, mobilalkalmazásokhoz vagy dokumentációhoz.

## Miért használja az Aspose.CAD for Java‑t a **CAD PNG‑re konvertálásához**?
- **Nincs szükség CAD telepítésre** – a könyvtár teljesen Java‑ban működik.  
- **Megőrzi az elrendezés hűségét** – kiválaszthatja a konkrét elrendezéseket, szabályozhatja a DPI‑t, és megtartja a vonalak minőségét.  
- **Kötegelt feldolgozás** – egyszerű ciklussal több fájlt is feldolgozhat.  
- **OLE objektumok exportálása** – a DWG/DXF fájlokba beágyazott OLE tartalom automatikusan megjelenik a PNG kimenetben.

## Előkövetelmények

Mielőtt elkezdené a gyakorlati példát, győződjön meg róla, hogy a következő előfeltételek teljesülnek:

- **Java környezet** – Győződjön meg róla, hogy a gépén be van állítva egy Java fejlesztői környezet.  
- **Aspose.CAD for Java** – Töltse le és telepítse az Aspose.CAD for Java könyvtárat. A könyvtárat megtalálja a [letöltési linken](https://releases.aspose.com/cad/java/).  
- **CAD fájlok** – Készítse elő az OLE objektumokat tartalmazó CAD fájlokat, amelyeket exportálni szeretne.

## Névterek importálása

A Java projektjébe importálja a szükséges névtereket. Ezek a névterek biztosítják az Aspose.CAD használatához szükséges osztályokat és funkciókat.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Most bontsuk le az OLE objektumok CAD‑ből történő exportálásának folyamatát több lépésre:

## Hogyan **mentse a CAD‑t PNG‑ként** és exportálja az OLE objektumokat

### 1. lépés: Állítsa be a dokumentum könyvtárát

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Győződjön meg róla, hogy a `"Your Document Directory"` helyére a CAD fájlokat tartalmazó könyvtár elérési útját írja.

### 2. lépés: Definiálja a CAD fájlneveket

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Adja meg a `files` tömbben a feldolgozni kívánt CAD fájlok nevét.

### 3. lépés: PNG exportálási beállítások megadása

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Állítsa be a PNG exportálási opciókat, beleértve a vektor rasterizálást és az elrendezés beállításait. Ezek az opciók teszik lehetővé a **CAD PNG‑re konvertálását** a kívánt minőségben.

### 4. lépés: CAD fájlok bejárása

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Iteráljon minden megadott CAD fájlon, töltse be az Aspose.CAD‑dal, és mentse el az OLE objektumokat PNG képekként. Ez a ciklus egyszerű módot mutat be a **DWG PNG‑re konvertálására** tömegesen.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| **Üres PNG kimenet** | Elrendezésnév eltérés | Ellenőrizze, hogy a `"Layout1"` elrendezés létezik‑e a forrás DWG‑ben. |
| **Hiányzó OLE grafika** | Az OLE objektumok más elrendezésben vannak | Vegye fel az összes releváns elrendezést a `rasterizationOptions.setLayouts(...)`‑ban. |
| **Memória‑hiány hiba nagy fájloknál** | Magas DPI beállítások | Csökkentse a DPI‑t a `rasterizationOptions.setResolution(...)`‑val, vagy dolgozzon egy fájlon egyszerre. |

## Gyakran ismételt kérdések

**Q: Az Aspose.CAD kompatibilis minden CAD fájlformátummal?**  
A: Az Aspose.CAD számos CAD formátumot támogat, többek között a DWG, DXF és DGN formátumokat. A teljes listáért tekintse meg a [dokumentációt](https://reference.aspose.com/cad/java/).

**Q: Testreszabhatom az OLE objektumok exportálási beállításait?**  
A: Igen, az Aspose.CAD kiterjedt lehetőségeket kínál az exportálási beállítások testreszabására, így a kimenetet pontosan az Ön igényeihez igazíthatja.

**Q: Van ingyenes próbaverzió az Aspose.CAD‑hez?**  
A: Igen, az Aspose.CAD képességeit ingyenes próbaverzióból is kipróbálhatja [innen](https://releases.aspose.com/).

**Q: Hol kaphatok közösségi támogatást az Aspose.CAD‑hez?**  
A: Csatlakozzon az Aspose.CAD közösséghez a [fórumban](https://forum.aspose.com/c/cad/19), ahol segítséget kérhet és megoszthatja tapasztalatait.

**Q: Hogyan vásárolhatok licencet az Aspose.CAD‑hez?**  
A: Látogassa meg a [vásárlási oldalt](https://purchase.aspose.com/buy), ahol a fejlesztési igényeinek megfelelő licencet szerezhet.

## Következtetés

Ezekkel az egyszerű, de hatékony lépésekkel zökkenőmentesen **mentheti a CAD‑t PNG‑ként**, miközben OLE objektumokat exportál CAD fájlokból az Aspose.CAD for Java segítségével. Ez a sokoldalú eszköz lehetővé teszi a fejlesztők számára a CAD adatok hatékony kezelését, új lehetőségeket nyitva meg a CAD‑alkalmazásfejlesztés és a képalapú downstream munkafolyamatok terén.

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}