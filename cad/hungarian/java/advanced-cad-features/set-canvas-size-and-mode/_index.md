---
date: 2026-08-29
description: Ismerje meg, hogyan állíthatja be a pdf oldalméretet, és konvertálhatja
  a CAD-et PDF-re az Aspose.CAD for Java segítségével, automatikus elrendezésméretezéssel
  és TIFF exporttal.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: PDF oldalméret beállítása – CAD konvertálása PDF-re
og_description: Ismerje meg, hogyan állíthatja be a pdf oldalméretet a CAD rajzok
  PDF-re konvertálása közben Java-ban az Aspose.CAD használatával. Ez az útmutató
  a vászon méreteket, az automatikus elrendezésméretezést és a magas felbontású TIFF
  exportálást tárgyalja.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: PDF oldalméret beállítása – CAD konvertálása PDF-re az Aspose használatával
  Java-ban
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: PDF oldalméret beállítása – CAD konvertálása PDF-re (Java)
url: /hu/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF oldal méretének beállítása – CAD konvertálása PDF-be (Java)

## Bevezetés

Ha **PDF oldal méretét** kell beállítania CAD rajzok PDF-be konvertálása közben, jó helyen jár. Ebben az oktatóanyagban megmutatjuk, hogyan használhatja az Aspose.CAD for Java-t a pontos vászonméretek meghatározásához, az automatikus elrendezés méretezés engedélyezéséhez, majd az eredmény exportálásához PDF és TIFF formátumba. Akár nyomtatásra készülő mérnöki vázlatokat, akár webgaléria bélyegképeket generál, az oldal méretének és a kimeneti felbontásnak a szabályozása elengedhetetlen.

## Gyors válaszok
- **Mi a “CAD PDF-be konvertálás” jelentése?** Egy CAD rajz (pl. DXF, DWG) átalakítása PDF dokumentummá, amely bármely platformon megtekinthető.  
- **Exportálhatok-e TIFF-be is?** Igen – használja a `TiffOptions`-t magas felbontású raszteres képek létrehozásához.  
- **Melyik opció szabályozza a vászon méretét Java-ban?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Mi az automatikus elrendezés méretezés?** Egy jelző (`setAutomaticLayoutsScaling(true)`), amely megőrzi az eredeti elrendezés arányait a vászon méretének változása esetén.  
- **Szükségem van licencre az Aspose.CAD-hez?** Ideiglenes vagy állandó licenc szükséges a termelésben való használathoz.

## Hogyan állítsuk be a PDF oldal méretét CAD PDF-be konvertálásakor Java-ban

Töltse be a CAD fájlt, konfigurálja a `CadRasterizationOptions`-t a kívánt szélességgel és magassággal, engedélyezze az automatikus elrendezés méretezést, majd mentse az eredményt PDF-ként. Ez a kétszakaszos megközelítés lehetővé teszi a kimeneti oldal pontos méreteinek szabályozását a vektorminőség feláldozása nélkül.

## Mi a CAD PDF-be konvertálás?

A CAD PDF-be konvertálás azt jelenti, hogy vektor‑alapú mérnöki rajzokat PDF oldalakká alakítunk, megőrizve a vonalakat, rétegeket és geometriát, miközben a fájlt univerzálisan elérhetővé tesszük. A folyamat a megadott beállítások szerint rasterizálja a rajzot, egy PDF-et hozva létre, amely bármely eszközön megnyitható CAD szoftver nélkül, és megőrzi az eredeti tervezés vizuális hűségét.

## Miért állítsuk be a vászon méretét Java-ban?

A vászon méretének beállítása Java-ban lehetővé teszi a kimeneti felbontás és az oldal méretek meghatározását, biztosítva, hogy a létrehozott PDF vagy TIFF megfeleljen a nyomtatási vagy megjelenítési követelményeknek. Emellett szabályozza a méretezési viselkedést, ami nagyformátumú rajzok esetén elengedhetetlen.

## Előfeltételek

Mielőtt belemerülne az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek rendelkezésre állnak:

- Aspose.CAD for Java: Győződjön meg róla, hogy az Aspose.CAD könyvtár telepítve van a Java környezetében. Letöltheti az Aspose.CAD for Java könyvtárat [here](https://releases.aspose.com/cad/java/).
- Dokumentum könyvtár: Hozzon létre egy dokumentum könyvtárat a CAD fájlok tárolásához. Ez a könyvtár lesz hivatkozva az oktatóanyag lépéseiben.

Most kezdjük el a lépésről‑lépésre útmutatót.

## Névterek importálása

Ebben a lépésben importáljuk a szükséges névtereket, hogy elindítsuk az Aspose.CAD projektet.

`Image` a fő osztály a CAD fájlok betöltéséhez.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 1. lépés: Aspose.CAD osztályok importálása

A `Image` osztály módszereket biztosít a CAD rajzok betöltéséhez és mentéséhez.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Ebben a kódrészletben beállítjuk az erőforrás könyvtár elérési útját, és betöltünk egy DXF fájlt az Aspose.CAD `Image` osztályával.

## 2. lépés: CadRasterizationOptions tulajdonságainak beállítása (vászon méretének beállítása Java-ban)

`CadRasterizationOptions` a rasterizálási beállításokat határozza meg, például az oldal méretét és a méretezést a CAD‑raster konverzióhoz.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Itt létrehozunk egy `CadRasterizationOptions` példányt, és beállítjuk a tulajdonságokat, mint az oldal szélessége, magassága és a **automatikus elrendezés méretezés**. Ez a **vászon mód konfigurálása** magja a konverzióhoz.

## 3. lépés: PdfOptions létrehozása és vectorRasterizationOptions beállítása

`PdfOptions` a PDF kimeneti beállításokat definiálja a konverzióhoz.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Most létrehozunk egy `PdfOptions` példányt, és beállítjuk a `VectorRasterizationOptions` tulajdonságát a korábban konfigurált `CadRasterizationOptions`-ra.

## 4. lépés: Exportálás PDF-be (CAD PDF-be konvertálása)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Végül a CAD képet a megadott beállításokkal PDF fájlba mentjük, befejezve a **CAD PDF-be konvertálás** folyamatát.

## 5. lépés: TiffOptions létrehozása és vectorRasterizationOptions beállítása (CAD exportálása TIFF-be)

`TiffOptions` a TIFF kimeneti paramétereket konfigurálja, például a tömörítést és a felbontást.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ebben a lépésben beállítunk egy `TiffOptions` példányt, és konfiguráljuk a `VectorRasterizationOptions` tulajdonságát.

## 6. lépés: Exportálás TIFF-be

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Végül a CAD képet a megadott beállításokkal TIFF fájlba mentjük, bemutatva, hogyan **exportálhatunk CAD-et TIFF-be** a vászon méretének beállítása után.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| A PDF kimenet üres | `setNoScaling(true)` letiltja a renderelést néhány rajznál | Távolítsa el a `setNoScaling(true)`-t, vagy állítsa `false`-ra. |
| A TIFF felbontás alacsony | Az oldal szélesség/magasság túl kicsi | Növelje a `setPageWidth` / `setPageHeight` értékeket. |
| Az elrendezés torz | Az automatikus elrendezés méretezés le van tiltva | Győződjön meg róla, hogy a `setAutomaticLayoutsScaling(true)` engedélyezve van. |

## Miért állítsuk be a vászon méretét és DPI-t?

A vászon méretének és DPI-nak a módosítása közvetlenül befolyásolja a kimenet rasterizációs felbontását. Ha **növelni szeretné a TIFF felbontást**, egyszerűen emelje a `setPageWidth` / `setPageHeight` értékeket, vagy hívja a `rasterizationOptions.setResolution(300)`-t a `TiffOptions` létrehozása előtt. Ez magas minőségű raster képeket biztosít, amelyek nyomtatásra vagy részletes vizsgálatra alkalmasak.

## Gyakran ismételt kérdések

**Q1: Használhatom az Aspose.CAD for Java-t más Java keretrendszerekkel?**  
A: Igen, az Aspose.CAD úgy van tervezve, hogy zökkenőmentesen integrálódjon különböző Java keretrendszerekkel.

**Q2: Elérhető ideiglenes licenc az Aspose.CAD-hez?**  
A: Igen, ideiglenes licenc oldalt szerezhet a [here](https://purchase.aspose.com/temporary-license/) linken.

**Q3: Hol kaphatok közösségi támogatást az Aspose.CAD-hez?**  
A: Látogassa meg az Aspose.CAD fórumot [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) a közösségi támogatás és megbeszélésekért.

**Q4: Próbálhatom ingyen az Aspose.CAD-t?**  
A: Természetesen! Szerezzen ingyenes próbaverziót a [here](https://releases.aspose.com/) oldalon.

**Q5: Hogyan vásárolhatok Aspose.CAD for Java-t?**  
A: Vásárolja meg az Aspose.CAD for Java-t [here](https://purchase.aspose.com/buy) linken.

**Q: Befolyásolja a vászon mérete a vektor minőségét a PDF-ben?**  
A: Nem. A vászon mérete az oldal dimenzióit szabályozza; a vektoradatok felbontás‑függetlenek maradnak, biztosítva a tiszta megjelenítést bármilyen nagyításnál.

**Q: Beállíthatok más DPI-t a TIFF kimenethez?**  
A: Igen. Állítsa be a `rasterizationOptions.setResolution(dpiValue)`-t a `TiffOptions` létrehozása előtt.

**Q: Hogyan változtathatom meg egy meglévő PDF méreteit a CAD újrarenderelése nélkül?**  
A: Használja az Aspose.PDF-t a generált PDF betöltéséhez, és hívja a `pdf.getPages().setPageSize(PageSize.A4)` vagy egy egyéni méretet.

**Q: Mi a legjobb módja a dxf PDF-be konvertálásának a rétegek megőrzésével?**  
A: Tartsa meg a `setAutomaticLayoutsScaling(true)` beállítást, és kerülje a `setNoScaling(true)` használatát; ez megőrzi a rétegek láthatóságát és az elrendezés hűségét.

## Következtetés

Gratulálunk! Sikeresen **konvertált CAD-et PDF-be** és **exportált CAD-et TIFF-be**, miközben **beállította a vászon méretét Java-ban**, engedélyezte az **automatikus elrendezés méretezést**, és megtanulta, hogyan **konfigurálja a vászon módot** a magas minőségű kimenetekhez. Ez az oktatóanyag szilárd alapot nyújt CAD konverziós projektjeihez. Fedezze fel a további funkciókat és lehetőségeket az [Aspose.CAD documentation](https://reference.aspose.com/cad/java/) oldalon.

---

**Last Updated:** 2026-08-29  
**Tested with:** Aspose.CAD for Java 24.12  
**Author:** Aspose

## Kapcsolódó oktatóanyagok

- [Vászon Méretének Beállítása – Haladó CAD Funkciók Aspose.CAD for Java-val](/cad/java/advanced-cad-features/)
- [DWG Exportálása PDF-be Java-ban – PDF oldal méretének beállítása Aspose.CAD-val](/cad/java/cad-export-options/export-to-pdf/)
- [Egyedi Oldal Méret Beállítása – PDF CAD-ből Automatikus Elrendezés Méretezéssel](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}