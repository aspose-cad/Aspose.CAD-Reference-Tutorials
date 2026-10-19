---
date: 2026-10-19
description: Ismerje meg, hogyan konvertálhatja a DWG-t PDF-be Java-ban az Aspose.CAD
  segítségével. Ez a lépésről‑lépésre útmutató bemutatja, hogyan exportálhat AutoCAD
  PDF-et, mentheti a CAD-et PDF formátumba, és alkalmazhat licencet.
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: AutoCAD képek exportálása PDF-be
og_description: Ismerje meg, hogyan konvertálhatja a DWG-t PDF-be Java-ban az Aspose.CAD
  segítségével. Ez a lépésről‑lépésre útmutató bemutatja, hogyan exportálhat AutoCAD
  PDF-et, mentheti a CAD-et PDF formátumba, és alkalmazhat licencet.
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: DWG konvertálása PDF-be Java-ban az Aspose.CAD használatával
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: DWG konvertálása PDF-be Java-ban az Aspose.CAD használatával
url: /hu/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# AutoCAD PDF export – AutoCAD képek exportálása PDF-be az Aspose.CAD for Java segítségével

## Bevezetés

Ha **DWG-t PDF-re szeretne konvertálni Java-ban**, jó helyen jár. Ez az útmutató megmutatja, hogyan exportálhat AutoCAD képeket PDF-be az Aspose.CAD for Java segítségével, egy tisztán Java‑alapú könyvtár, amely a DWG, DXF, DWF és számos más CAD formátumot kezeli natív függőségek nélkül. A végére képes lesz **CAD-et PDF-ként menteni**, a rasterizálási beállításokat, például az oldalméretet finomhangolni, és helyesen alkalmazni egy **Aspose CAD licencet** a termelési használathoz.

## Gyors válaszok
- **Átalakíthatok DWG-t PDF-re Java-val?** Igen – az Aspose.CAD for Java natívan támogatja a DWG, DXF és tucatnyi más CAD formátumot.  
- **Szükségem van licencre?** Egy állandó **Aspose CAD licenc** eltávolítja az összes értékelési korlátozást; ideiglenes licenc is elérhető teszteléshez.  
- **Mely Java verziók támogatottak?** A Java 8 és újabb verziók teljes mértékben támogatottak.  
- **Módosíthatom a PDF oldal méreteit?** Természetesen – állítsa be a `pageWidth` és `pageHeight` értékeket a rasterizálási beállításokban.  
- **Lehetséges a 3‑D renderelés?** Igen – engedélyezze a `TypeOfEntities.Entities3D` beállítást a 3‑D entitások rasterizálásához.

## Mi az az AutoCAD PDF exportálás?
Az AutoCAD PDF exportálás a vektoros CAD rajzok hordozható PDF dokumentummá alakításának folyamata. Megőrzi a rétegeket, vonalvastagságokat, színeket, és opcionálisan a 3‑D geometriát, megkönnyítve a tervek megosztását az ügyfelekkel vagy archiválását CAD szoftver nélkül.

## Miért konvertáljunk DWG-t PDF-re az Aspose.CAD for Java-val?
Az Aspose.CAD **50+ bemeneti és kimeneti formátumot** támogat, több száz oldalas rajzokat dolgoz fel anélkül, hogy a teljes fájlt a memóriába töltené, és bármely, Java 8+‑ot támogató platformon fut. A könyvtár teljes irányítást biztosít a DPI, az oldalméret és az elrendezés felett, így **testreszabhatja a PDF oldalméretet** a pontos projekt specifikációknak megfelelően, mindezt natív DLL-ek telepítése nélkül.

## Előkövetelmények

- **Java Development Kit** – JDK 8 vagy újabb telepítve a munkaállomáson.  
- **Aspose.CAD for Java** – töltse le a legújabb JAR fájlt a [letöltési linkről](https://releases.aspose.com/cad/java/).  
- **Munkakönyvtár** – egy mappa, ahol a forrás DWG fájlok és a generált PDF-ek tárolódnak.

## Namespace-ek importálása

Az `Image` osztály bármely rasterizálható CAD rajzot képvisel, míg a `RasterizationOptions` és a `PdfOptions` lehetővé teszik a konverzió finomhangolását.

Az `Image` osztály az Aspose.CAD legfelső szintű objektuma, amely a CAD rajzot a memóriában tárolja.  
A `RasterizationOptions` osztály meghatározza, hogyan rasterizálódik a vektoradat a PDF-be írás előtt.  
A `PdfOptions` osztály a rasterizálási beállításokat PDF‑specifikus kimeneti paraméterekkel egyesíti.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Most lépésről lépésre áttekintjük a kódot.

## Hogyan konvertáljunk DWG-t PDF-re az Aspose.CAD for Java-val?

A DWG fájl PDF-re konvertálásához az Aspose.CAD for Java-val, töltse be a rajzot az Image osztállyal, konfigurálja a CadRasterizationOptions‑t (például DPI, oldalméret és entitástípusok), csomagolja ezeket az opciókat a PdfOptions‑ba, majd hívja meg a save metódust, megadva egy .pdf fájlnevet. Ez a sorrend biztosítja, hogy a vektoradat helyesen rasterizálódik, és a kapott PDF megfelel az elrendezési követelményeknek.

### 1. lépés: a forráskönyvtár útvonalának beállítása

Cserélje le a `"Your Document Directory"` értéket a teljes elérési útra, amelyet az előkövetelményekben létrehozott mappára mutat.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tipp:** Használja a `Paths.get(...).toAbsolutePath()` metódust, hogy elkerülje az útvonallal kapcsolatos hibákat különböző operációs rendszereken.

### 2. lépés: a CAD kép betöltése

A CAD fájl `Image` objektumba történő betöltése teljes hozzáférést biztosít az Aspose.CAD rasterizációs motorjához.

Az `Image` osztály betölti a DWG fájlt és előkészíti a konverzióra.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Miért fontos:** Miután a rajz a memóriában van, lekérdezheti annak elrendezéseit, rétegeit és metaadatait a rasterizálás előtt.

### 3. lépés: rasterizálási beállítások megadása

Állítsa be a `pageWidth` és `pageHeight` értékeket a **PDF oldalméret testreszabásához**. A `setTypeOfEntities(TypeOfEntities.Entities3D)` engedélyezése teljes 3‑D renderelést tesz lehetővé, ha szükséges.

A `RasterizationOptions` objektum szabályozza a DPI-t, az oldalméreteket és az entitástípusokat a kimenethez.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` pontban van megadva (1 pt = 1/72 in).  
- A `setTypeOfEntities` sor kikommentálásával engedélyezhető a 3‑D rasterizálás.  
- A `setLayouts` választja ki, melyik elrendezést (Model, Layout1, stb.) kell renderelni.

### 4. lépés: PDF beállítások konfigurálása

Kapcsolja össze a rasterizálási beállításokat a PDF kimenettel, biztosítva, hogy a vektoradat helyesen legyen átalakítva.

A `PdfOptions` osztály összekapcsolja a rasterizálási konfigurációt a végső PDF fájllal.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 5. lépés: PDF mentése

Az eredményül kapott fájl, `Export3DImagestoPDF_out_.pdf`, a **CAD PDF-ként mentése** ábrázolása az eredeti AutoCAD rajzodnak.

A `save` metódus a rasterizált képet egy PDF fájlba írja a lemezen.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## Gyakori problémák és megoldások

| Tünet | Valószínű ok | Megoldás |
|-------|--------------|----------|
| Üres PDF kimenet | A rasterizálási beállítások nincsenek megadva vagy az elrendezés nem egyezik | Ellenőrizze, hogy a `setLayouts` megegyezik a CAD fájlban szereplő elrendezés nevével. |
| Alacsony felbontású kép | `pageWidth`/`pageHeight` túl kicsi | Növelje a méreteket vagy állítson be magasabb DPI-t a `rasterizationOptions.setResolution(...)` segítségével. |
| Licenc kivétel | Nincs érvényes licenc alkalmazva | Alkalmazzon egy **Aspose CAD licencet**, vagy használjon ideiglenes licencet teszteléshez. |

## Gyakran feltett kérdések

**Q: Használhatom az Aspose.CAD for Java-t más CAD fájlformátumokkal?**  
A: Igen – a könyvtár támogatja a DWG, DXF, DWF, DGN és több mint 30 további formátumot, így rugalmasságot biztosít a projektek során.

**Q: Hogyan szerezhetek ideiglenes licencet az Aspose.CAD for Java-hoz?**  
A: Látogassa meg a [ideiglenes licenc oldal](https://purchase.aspose.com/temporary-license/) oldalt, hogy időkorlátos licencet kérjen értékeléshez.

**Q: Vannak elrendezési opciók a rasterizáláshoz?**  
A: Természetesen. Használja a `setLayouts("Model")`, `setLayouts("Layout1")` stb. beállításokat, hogy kiválassza, melyik nézet kerül PDF-be renderelésre.

**Q: Megváltoztathatom a kimeneti PDF fájl méretét?**  
A: Igen – módosítsa a `pageWidth` és `pageHeight` értékeket a rasterizálási beállításokban, hogy megfeleljenek a kívánt oldalméreteknek.

**Q: Hol kaphatok segítséget, ha problémáim vannak?**  
A: A dedikált közösség elérhető a [Aspose.CAD fórumon](https://forum.aspose.com/c/cad/19), ahol kérdéseket tehet fel és megoszthat megoldásokat.

---

**Utoljára frissítve:** 2026-10-19  
**Tesztelve a következővel:** Aspose.CAD for Java 24.10  
**Szerző:** Aspose

## Kapcsolódó oktatóanyagok

- [DWG exportálása PDF-be Java-ban – PDF oldalméret beállítása az Aspose.CAD segítségével](/cad/java/cad-export-options/export-to-pdf/)
- [DWG exportálása PDF-be: Specifikus elrendezés az Aspose.CAD for Java használatával](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [DWG exportálása PDF-be és nyomkövetés engedélyezése az Aspose.CAD Java-val](/cad/java/additional-features/enable-tracking/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}