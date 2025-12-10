---
date: 2025-12-10
description: Tanulja meg, hogyan hozhat létre PDF-et CAD-ból az Aspose.CAD for Java
  segítségével, toll testreszabással. Ez a lépésről‑lépésre útmutató hatékonyan mutatja
  be a CAD PDF‑be exportálását.
linktitle: Pen Support in Export
second_title: Aspose.CAD Java API
title: Hogyan hozzunk létre PDF-et CAD-ből tolltámogatással az export során
url: /hu/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Toll támogatás exportáláskor

## Bevezetés

A CAD konverziók gyorsan változó világában a fejlesztőknek gyakran szükségük van **PDF létrehozására CAD** fájlokból, miközben megőrzik a vizuális hűséget. Az Aspose.CAD for Java ezt egyszerűvé teszi, gazdag lehetőségeket kínálva, például a toll testreszabását, amely lehetővé teszi a vonalstílusok finomhangolását az exportálási folyamat során. Ebben az útmutatóban egy teljes, gyakorlati példán keresztül mutatjuk be, hogyan **exportálhat CAD-et PDF‑be** egyedi tollbeállításokkal, így közvetlenül a DXF rajzokból készíthetünk kifinomult PDF‑eket.

## Gyors válaszok
- **Mi jelent a “create PDF from CAD”?** CAD rajz (pl. DXF) PDF dokumentummá konvertálása, miközben megmarad a vektor minőség.  
- **Melyik könyvtár kezeli a toll testreszabását?** Az Aspose.CAD for Java `PenOptions` osztálya.  
- **Használhatom más formátumokhoz is?** Igen – ugyanazok a tollbeállítások alkalmazhatók PNG, BMP, TIFF stb. formátumokra.  
- **Szükség van licencre?** Érvényes Aspose.CAD licenc szükséges a termelésben való használathoz.  
- **Mi a minimum Java verzió?** Java 8 vagy újabb.

## Mi az a “create PDF from CAD”?
A PDF létrehozása CAD‑ből azt jelenti, hogy egy CAD rajzot rasterizálunk vagy vektorként renderelünk PDF fájlba. Ez lehetővé teszi a mérnöki tervek egyszerű megosztását, nyomtatását és archiválását anélkül, hogy a címzettnek CAD szoftvert kellene használnia.

## Miért használjunk toll támogatást CAD PDF exportálásakor?
A toll támogatás lehetővé teszi a vonalvégek, illeszkedések és vastagság szabályozását, így képes vagy megfelelni a vállalati arculatnak vagy a műszaki rajz szabványoknak. Különösen hasznos, ha az alapértelmezett vonalmegjelenítés nem felel meg a vizuális követelményeknek.

## Előfeltételek

- **Java fejlesztői környezet** – működő JDK (8 vagy újabb) és egy tetszőleges IDE vagy build eszköz.  
- **Aspose.CAD könyvtár** – töltse le a legújabb JAR‑t a hivatalos oldalról [itt](https://releases.aspose.com/cad/java/).  
- **Minta DXF fájl** – ebben a bemutatóban a `conic_pyramid.dxf` fájlt használjuk.

Miután felállítottuk a hátteret, merüljünk el a kódban.

## Importálási névterek

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## 1. lépés: Dokumentum könyvtár meghatározása

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

> **Pro tipp:** Cserélje le a `"Your Document Directory"` értéket a DXF fájlok helyét tartalmazó abszolút útvonalra.

## 2. lépés: CAD fájl betöltése

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

Az `Image.load` metódus beolvassa a DXF fájlt, és egy `CadImage` objektumot hoz létre, amelyet manipulálhatunk.

## 3. lépés: Rasterizálási beállítások konfigurálása

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

Állítsa be az oldal méreteit a kimeneti PDF felbontásának szabályozásához. A 100‑szal való szorzás nagy felbontású kimenetet eredményez, amely nyomtatáshoz alkalmas.

## 4. lépés: Toll beállítások testreszabása

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

Itt a toll kezdő‑ és végvégeit `Flat`‑re állítjuk. Kísérletezhet más `LineCap` értékekkel (pl. `Round`, `Square`), hogy különböző vizuális hatásokat érjen el.

## 5. lépés: PDF exportálási beállítások konfigurálása

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

A `PdfOptions` objektum összekapcsolja a rasterizálási beállításokat a PDF exportálási folyamattal.

## 6. lépés: Exportált PDF mentése

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Ennek a sor futtatásával egy `9LHATT-A56_generated.pdf` nevű PDF fájl kerül a `dataDir` mappába, a megadott egyedi tollstílussal.

## Gyakori felhasználási esetek

- **Műszaki dokumentáció** – pontos mérnöki rajzok beágyazása PDF kézikönyvekbe.  
- **Automatizált jelentéskészítés** – PDF‑ek generálása CAD adatokból valós időben webszolgáltatásokban.  
- **Minőségellenőrzés** – egyedi vonalvégek alkalmazása a mérővonalak vagy toleranciák kiemeléséhez.

## Hibakeresés és tippek

- **Helytelen fájlútvonal** – győződjön meg arról, hogy a `dataDir` fájlelválasztóval (`/` vagy `\\`) végződik.  
- **Hiányzó licenc** – érvényes licenc nélkül a könyvtár értékelő módban fut, ami vízjelet adhat a kimenethez.  
- **Váratlan vonalstílusok** – ellenőrizze, hogy a `PenOptions` be legyen állítva a `save` hívása előtt; ellenkező esetben az alapértelmezett beállítások lesznek használva.

## Gyakran ismételt kérdések

### Q1: Testreszabhatom a toll beállításait a PDF‑n kívül más formátumokhoz is?
A1: Igen, a bemutatott toll testreszabás alkalmazható különböző képformátumokra, beleértve a PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF és WMF formátumokat.

### Q2: Hogyan kezelhetek különböző kezdő és végvégű tollakat?
A2: Használja a `PenOptions` osztályt a kívánt kezdő‑ és végvég beállításához, ami rugalmasságot biztosít a vonalak megjelenésének meghatározásában.

### Q3: Mi történik, ha nem adok meg toll beállításokat?
A3: Ha a toll beállításait nem adja meg kifejezetten, a rendszer az alapértelmezett tollakat használja, amelyek különböző kontextusokban eltérhetnek.

### Q4: Vannak speciális szempontok a rasterizálási beállításoknál?
A4: Állítsa be a rasterizálási beállításoknál az oldal szélességét és magasságát a kiexportált kép méretének szabályozásához.

### Q5: Hol találok további támogatást vagy közösségi megbeszéléseket?
A5: Tekintse meg az Aspose.CAD közösségi fórumot [itt](https://forum.aspose.com/c/cad/19) támogatás és megbeszélések céljából.

---

**Legutóbb frissítve:** 2025-12-10  
**Tesztelve a következővel:** Aspose.CAD 24.11 for Java  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}