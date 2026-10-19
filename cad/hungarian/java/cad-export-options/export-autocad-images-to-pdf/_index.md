---
date: 2026-10-19
description: Ismerje meg, hogyan exportálhat AutoCAD rajzokat PDF-be egyedi PDF oldalmérettel
  az Aspose.CAD for Java használatával. Ez a lépésről‑lépésre útmutató lefedi a DWG
  PDF-re konvertálást, a rasterizációs beállításokat és a licencelést.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: AutoCAD képek exportálása PDF-be
og_description: Állítson be egyedi PDF oldalméretet AutoCAD rajzok PDF-be exportálásakor
  az Aspose.CAD for Java használatával. Tanulja meg a DWG PDF konvertálást, a rasterizációs
  beállításokat és a licencelést percek alatt.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Egyedi PDF oldalméret beállítása AutoCAD exportáláshoz az Aspose.CAD segítségével
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Egyedi PDF oldalméret beállítása AutoCAD exportáláshoz az Aspose.CAD segítségével
url: /hu/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportálás AutoCAD PDF - AutoCAD képek exportálása PDF-be az Aspose.CAD for Java segítségével

## Bevezetés

Ha **DWG-t PDF-re** kell konvertálnia, és pontosan szabályozni szeretné a kimeneti fájl méretét, jó helyen jár. Ez a bemutató megmutatja, hogyan állíthat be **egyedi PDF oldalméretet** AutoCAD képek PDF-be exportálásakor az Aspose.CAD for Java használatával. A útmutató végére tudni fogja, hogyan töltsön be egy DWG-t, hogyan konfigurálja a raszterizálási beállításokat, például DPI-t és oldal szélességet/magasságot, hogyan alkalmazzon licencet, és hogyan generáljon termelésre kész PDF-et.

## Gyors válaszok
- **Átalakíthatok DWG-t PDF-re Java-val?** Igen – az Aspose.CAD for Java natívan támogatja a DWG, DXF, DWF és számos más CAD formátumot.  
- **Szükségem van licencre a termeléshez?** A teljes Aspose.CAD licenc eltávolítja az összes értékelési korlátot; teszteléshez ideiglenes licenc is elérhető.  
- **Mely Java verziók kompatibilisek?** A könyvtár a Java 8‑al és minden későbbi JDK‑val működik.  
- **Hogyan változtathatom meg a PDF oldal méreteit?** Állítsa be a `pageWidth` és `pageHeight` értékeket a `PdfOptions.getRasterizationOptions()`‑on a kívánt méretre.  
- **Támogatott a 3‑D renderelés?** Igen – engedélyezze a `TypeOfEntities.Entities3D`‑t a 3‑D entitások raszterizálásához.

## Mi az export AutoCAD PDF?
Az AutoCAD PDF exportálása azt jelenti, hogy vektoralapú CAD rajzokat (DWG, DXF, DWF stb.) alakítunk át hordozható PDF dokumentummá, miközben megőrzik a rétegeket, vonalvastagságokat és opcionális 3‑D geometriát. Ez lehetővé teszi a tervek megosztását ügyfelekkel, a rajzok archiválását vagy nyomtatását CAD szoftver telepítése nélkül.

## Miért használja az Aspose.CAD for Java-t a DWG PDF-re konvertálásához?
Az Aspose.CAD for Java ideális a DWG PDF-re konvertálásához, mivel kiterjedt formátumtámogatást nyújt, tiszta Java környezetben fut natív függőségek nélkül, magas felbontású raszterizálást biztosít teljes DPI és oldalméret szabályozással, és rugalmas licencelést kínál, amely lehetővé teszi a próbaverzióval való kezdést és a termelésre való átállást.

- **Széles körű formátumtámogatás** – 50+ bemeneti és kimeneti formátumot támogat, beleértve a DWG, DXF, DWF, DGN és PDF formátumokat.  
- **Tiszta Java megvalósítás** – nincs natív DLL vagy külső függőség, így a telepítés egyszerű bármely platformon.  
- **Magas felbontású raszterizálás** – megadhatja a DPI-t, oldalméretet és elrendezést, teljes irányítást biztosítva a **egyedi PDF oldalméret** felett az eredményben.  
- **Skálázható licencelés** – kezdje ingyenes próbaverzióval, majd frissítsen állandó **Aspose CAD licencre**.  

## Előkövetelmények

- **Java Development Kit** – JDK 8 vagy újabb telepítve a gépén.  
- **Aspose.CAD for Java** – töltse le a legújabb JAR-t a [download link](https://releases.aspose.com/cad/java/) oldalról.  
- **Munkakönyvtár** – egy mappa, amely tartalmazza a forrás DWG fájlokat és fogadja a generált PDF-eket.

## Névterek importálása

Az `Image` osztály az Aspose.CAD alapobjektuma, amely egy CAD rajzot ábrázol a memóriában. Importálja a szükséges csomagokat, mielőtt elkezdené a kódolást.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Most lépésről lépésre áttekintjük a kódot.

## Hogyan állítsunk be egyedi PDF oldalméretet DWG PDF-be exportálásakor?

Töltse be a DWG-jét, határozza meg a kívánt oldal szélességet és magasságot, majd mentse az eredményt PDF-ként – ennyi a szükséges ahhoz, hogy egyedi oldalmérettel rendelkező PDF-et hozzon létre. A következő lépések bemutatják a pontos sorrendet és a minimális kódot.

### 1. lépés: az erőforrás könyvtár útvonalának beállítása

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tipp:** Cserélje le a `"Your Document Directory"`-t a teljes elérési útra a mappához, amelyet az előkövetelményekben hozott létre.

### 2. lépés: a CAD kép betöltése

Az `Image` osztály betölti a CAD fájlt, és hozzáférést biztosít az Aspose.CAD raszterizálási motorjához.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Miért fontos:** Miután a CAD fájl betöltődött, módosíthatja a raszterizálási beállításokat a PDF-be renderelés előtt.

### 3. lépés: raszterizálási beállítások megadása

A `CadRasterizationOptions` osztály meghatározza, hogyan raszterizálódik a CAD rajz, mielőtt PDF-ként mentésre kerül. Állítsa be a `pageWidth` és `pageHeight` értékeket egy **egyedi PDF oldalméret** meghatározásához. A 3‑D renderelést is engedélyezheti a `setTypeOfEntities` sor kikommentelésével.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – pixelben mérve; módosítsa ezeket az értékeket az A4, Letter vagy bármely egyedi mérethez.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – szükség esetén 3‑D entitásokat renderel.  
- `setLayouts` – kiválasztja, melyik elrendezést (Model, Layout1 stb.) raszterizálja.

### 4. lépés: PDF beállítások konfigurálása

A `PdfOptions` osztály PDF‑specifikus beállításokat tartalmaz, és összekapcsolja a raszterizálási beállításokat a kimeneti fájllal, biztosítva, hogy az egyedi oldalméretek helyesen legyenek alkalmazva.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 5. lépés: PDF mentése

A `save` metódus a renderelt képet a megadott PDF fájlba írja.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Az eredményül kapott fájl, `Export3DImagestoPDF_out_.pdf`, egy **save cad as pdf** ábrázolása az eredeti AutoCAD rajznak a megadott pontos oldalméretekkel.

## Gyakori problémák és megoldások

| Tünet | Valószínű ok | Megoldás |
|-------|--------------|----------|
| Üres PDF kimenet | A raszterizálási beállítások nincsenek beállítva vagy az elrendezés nem egyezik | Ellenőrizze, hogy a `setLayouts` egyezik-e a CAD fájlban lévő elrendezés nevével. |
| Alacsony felbontású kép | `pageWidth`/`pageHeight` túl kicsi vagy alacsony DPI | Növelje a méreteket, vagy hívja a `rasterizationOptions.setResolution(...)`‑t magasabb DPI-vel. |
| Licenc kivétel | Nincs érvényes licenc alkalmazva | Alkalmazzon állandó Aspose.CAD licencet, vagy használjon ideiglenes licencet teszteléshez. |

## Gyakran feltett kérdések

**Q: Használhatom az Aspose.CAD for Java-t más CAD fájlformátumokkal?**  
A: Igen, a könyvtár támogatja a DWG, DXF, DWF, DGN és még sok más formátumot, így rugalmasságot biztosít a projektek között.

**Q: Hogyan szerezhetek ideiglenes licencet az Aspose.CAD for Java-hoz?**  
A: Látogassa meg a [temporary license page](https://purchase.aspose.com/temporary-license/) oldalt, hogy időkorlátos licencet kérjen értékeléshez.

**Q: Vannak elrendezési lehetőségek a raszterizáláshoz?**  
A: Természetesen. Használja a `setLayouts("Model")`‑t vagy adjon meg más elrendezésneveket, hogy szabályozza, melyik nézet legyen renderelve.

**Q: Testreszabhatom a kimeneti PDF fájl méretét?**  
A: Igen – módosítsa a `pageWidth` és `pageHeight` értékeket a raszterizálási beállításokban a szükséges méretekre.

**Q: Hol kaphatok segítséget vagy vitathatok problémákat az Aspose.CAD for Java-val kapcsolatban?**  
A: A dedikált [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) közösségi támogatást és az Aspose csapat hivatalos válaszait nyújtja.

## További GYIK (AI‑barát formátum)

**Q: Az Aspose.CAD igényel natív könyvtárakat Windows vagy Linux rendszeren?**  
A: Nem. Az Aspose.CAD for Java egy tiszta Java könyvtár, így bármely, a JDK-t támogató platformon fut, további natív DLL-ek nélkül.

**Q: Milyen nagy DWG fájlt képes a könyvtár feldolgozni?**  
A: A könyvtár több száz oldalas rajzokat (akár 500 MB-ig) képes kezelni anélkül, hogy a teljes fájlt a memóriába töltené, streaming architektúrájának köszönhetően.

**Q: Lehetséges sok DWG fájlt egyszerre batch‑konvertálni PDF-re?**  
A: Igen. Iteráljon egy könyvtáron, töltse be minden fájlt az `Image.load()`‑val, alkalmazza ugyanazokat a raszterizálási beállításokat, és hívja meg a `save()`‑t minden kimeneti PDF-hez.

**Q: Milyen teljesítményt várhat el egy tipikus szerveren?**  
A: Egy 100 oldalas DWG 300 DPI‑n történő konvertálása egy standard 2,5 GHz CPU-n körülbelül 12 másodpercet vesz igénybe, az Aspose benchmark tesztek alapján.

**Q: A könyvtár megőrzi a réteg információkat a PDF-ben?**  
A: Bár a kimenet raszterizált, a rétegek, vonalvastagságok és színek vizuális megjelenése hűen reprodukálódik.

**Last Updated:** 2026-10-19  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## Kapcsolódó bemutatók

- [DWG exportálása PDF-be és nyomkövetés engedélyezése Aspose.CAD Java-val](/cad/java/additional-features/enable-tracking/)
- [DWG exportálása PDF-be: Specifikus elrendezés az Aspose.CAD Java használatával](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [DWG exportálása BMP-be és CAD méret beállítása egységtípus használatával az Aspose.CAD for Java-val](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}