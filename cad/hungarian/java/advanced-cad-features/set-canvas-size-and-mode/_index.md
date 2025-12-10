---
date: 2025-12-10
description: Tanulja meg, hogyan konvertálhat CAD-et PDF-be az Aspose.CAD for Java
  használatával, miközben beállítja a vászon méretét, az automatikus elrendezés méretezését,
  és TIFF-be exportál.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: CAD konvertálása PDF-be – Vászonméret és mód beállítása (Java)
url: /hu/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Állítsa be a vászon méretét és módját

## Bevezetés

Szeretne **CAD-et PDF-re konvertálni**, miközben teljes ellenőrzést gyakorol a vászon mérete és a renderelési mód felett? Ez az átfogó útmutató lépésről lépésre végigvezet a vászon méretének Java-ban történő beállításán, az automatikus elrendezés méretezés engedélyezésén, majd az eredmény PDF és TIFF formátumokba történő exportálásán az Aspose.CAD használatával. Akár egy gyártási folyamatot finomít, akár egy prototípussal kísérletezik, itt világos, gyakorlati útmutatót talál.

## Gyors válaszok
- **Mit jelent a “convert CAD to PDF”?** Egy CAD rajz (pl. DXF, DWG) PDF dokumentummá alakítása, amely bármely platformon megtekinthető.  
- **Exportálhatok TIFF-be is?** Igen – használja a `TiffOptions`-t magas felbontású raszteres képek létrehozásához.  
- **Melyik opció szabályozza a vászon méretét Java-ban?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Mi az automatikus elrendezés méretezés?** Egy jelző (`setAutomaticLayoutsScaling(true)`), amely a vászon méretének változása esetén megőrzi az eredeti elrendezés arányait.  
- **Szükségem van licencre az Aspose.CAD-hez?** Ideiglenes vagy állandó licenc szükséges a termelési használathoz.

## Mi a **convert CAD to PDF**?

A CAD PDF-re konvertálása azt jelenti, hogy vektor‑alapú mérnöki rajzokat PDF oldalakká renderelünk, megőrizve a vonalakat, rétegeket és geometriát, miközben a fájlt univerzálisan hozzáférhetővé tesszük.

## Miért állítsuk be a vászon méretét **java**-ban?

A vászon méretének Java-ban történő beállítása lehetővé teszi a kimeneti felbontás és az oldal méretek meghatározását, biztosítva, hogy a létrejövő PDF vagy TIFF megfeleljen a nyomtatási vagy megjelenítési követelményeknek. Emellett szabályozhatja a méretezési viselkedést, ami nagyformátumú rajzok esetén elengedhetetlen.

## Előfeltételek

Mielőtt belemerülne a bemutatóba, győződjön meg arról, hogy a következő előfeltételek rendelkezésre állnak:

- Aspose.CAD for Java: Győződjön meg róla, hogy az Aspose.CAD könyvtár telepítve van a Java környezetében. Letöltheti [itt](https://releases.aspose.com/cad/java/).
- Dokumentum könyvtár: Hozzon létre egy könyvtárat a CAD fájlok tárolásához. Ez a könyvtár lesz hivatkozva a bemutató lépéseiben.

Most kezdjük el a lépésről‑lépésre útmutatót.

## Névterek importálása

Ebben a lépésben importáljuk a szükséges névtereket, hogy elindítsuk az Aspose.CAD projektet.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## 1. lépés: Aspose.CAD osztályok importálása

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Ebben a kódrészletben beállítjuk az erőforrás könyvtár elérési útját, és betöltünk egy DXF fájlt az Aspose.CAD `Image` osztályával.

## 2. lépés: **CadRasterizationOptions** tulajdonságok beállítása (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Itt létrehozunk egy `CadRasterizationOptions` példányt, és beállítjuk a tulajdonságokat, mint például az oldal szélesség, magasság és a **automatikus elrendezés méretezés**. Ez a **canvas mód konfigurálása** központi része a konverzióhoz.

## 3. lépés: PdfOptions létrehozása és VectorRasterizationOptions beállítása

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Most létrehozunk egy `PdfOptions` példányt, és beállítjuk a `VectorRasterizationOptions` tulajdonságát a korábban konfigurált `CadRasterizationOptions`-ra.

## 4. lépés: Exportálás PDF-be (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Végül a megadott beállításokkal elmentjük a CAD képet PDF fájlba, befejezve a **convert CAD to PDF** folyamatot.

## 5. lépés: TiffOptions létrehozása és VectorRasterizationOptions beállítása (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ebben a lépésben létrehozunk egy `TiffOptions` példányt, és beállítjuk a `VectorRasterizationOptions` tulajdonságát.

## 6. lépés: Exportálás TIFF-be

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Végül a megadott beállításokkal elmentjük a CAD képet TIFF fájlba, bemutatva, hogyan **exportálhat CAD-et TIFF-be** a vászon méretének konfigurálása után.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| A kimeneti PDF üres | `setNoScaling(true)` letiltja a renderelést bizonyos rajzoknál | `setNoScaling(true)` eltávolítása vagy `false`-ra állítása. |
| A TIFF felbontása alacsony | Az oldal szélesség/magasság túl kicsi | Növelje a `setPageWidth` / `setPageHeight` értékeket. |
| Az elrendezés torz | Az automatikus elrendezés méretezés letiltva | Győződjön meg róla, hogy a `setAutomaticLayoutsScaling(true)` engedélyezve van. |

## Következtetés

Gratulálunk! Sikeresen **convert CAD to PDF** és **export CAD to TIFF** műveleteket hajtott végre, miközben **set canvas size java**-t alkalmazott, engedélyezve a **automatikus elrendezés méretezést**, és megtanulta, hogyan **configure canvas mode** a magas minőségű kimenetekhez. Ez a bemutató szilárd alapot nyújt a CAD konverziós projektjeihez. Fedezze fel a további funkciókat és lehetőségeket az [Aspose.CAD dokumentációban](https://reference.aspose.com/cad/java/).

## GyIK

### Q1: Használhatom az Aspose.CAD for Java-t más Java keretrendszerekkel?

A1: Igen, az Aspose.CAD úgy van tervezve, hogy zökkenőmentesen integrálódjon különböző Java keretrendszerekbe.

### Q2: Elérhető ideiglenes licenc az Aspose.CAD-hez?

A2: Igen, ideiglenes licencet szerezhet [itt](https://purchase.aspose.com/temporary-license/).

### Q3: Hol kaphatok közösségi támogatást az Aspose.CAD-hez?

A3: Látogassa meg az [Aspose.CAD fórumot](https://forum.aspose.com/c/cad/19) a közösségi támogatás és megbeszélésekért.

### Q4: Próbálhatom ingyen az Aspose.CAD-t?

A4: Természetesen! Szerezzen ingyenes próbaverziót [itt](https://releases.aspose.com/).

### Q5: Hogyan vásárolhatom meg az Aspose.CAD for Java-t?

A5: Vásárolja meg a terméket [itt](https://purchase.aspose.com/buy).

**További kérdések és válaszok**

**Q: Befolyásolja a vászon mérete a vektor minőségét a PDF-ben?**  
A: Nem. A vászon mérete az oldal méreteit szabályozza; a vektor adatok felbontás‑függetlenek, így bármilyen nagyításnál éles megjelenítést biztosítanak.

**Q: Beállíthatok más DPI-t a TIFF kimenethez?**  
A: Igen. Állítsa be a `rasterizationOptions.setResolution(dpiValue)`-t a `TiffOptions` létrehozása előtt.

---

**Utoljára frissítve:** 2025-12-10  
**Tesztelve:** Aspose.CAD for Java 24.12  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}