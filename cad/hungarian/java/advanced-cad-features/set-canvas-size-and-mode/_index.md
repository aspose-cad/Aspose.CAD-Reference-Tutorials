---
date: 2026-02-15
description: Tanulja meg, hogyan állíthatja be a PDF oldalméretét, és konvertálhatja
  a CAD-et PDF-be az Aspose.CAD for Java használatával, automatikus elrendezésméretezéssel
  és TIFF exporttal.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: PDF oldalméret beállítása – CAD konvertálása PDF‑be (Java)
url: /hu/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vászonméret és mód beállítása

## Bevezetés

Ha **PDF oldalméretet** kell beállítania CAD rajzok PDF‑re konvertálása közben, jó helyen jár. Ebben az útmutatóban megmutatjuk, hogyan használja az Aspose.CAD for Java‑t a pontos vászonméretek meghatározásához, az automatikus elrendezésméretezés engedélyezéséhez, majd az eredmény exportálásához PDF‑be és TIFF‑be. Akár nyomtatásra készülő mérnöki vázlatokat, akár webgaléria előnézeti képeket generál, az oldalméret és a kimeneti felbontás szabályozása elengedhetetlen.

## Gyors válaszok
- **Mit jelent a “convert CAD to PDF”?** Egy CAD rajz (pl. DXF, DWG) PDF‑dokumentummá alakítása, amely bármely platformon megtekinthető.  
- **Exportálhatok TIFF‑be is?** Igen — használja a `TiffOptions`‑t magas felbontású raszteres képek létrehozásához.  
- **Melyik opció vezérli a vászonméretet Java‑ban?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Mi az automatikus elrendezésméretezés?** Egy jelző (`setAutomaticLayoutsScaling(true)`), amely megőrzi az eredeti elrendezés arányait, amikor a vászonméret változik.  
- **Szükségem van licencre az Aspose.CAD‑hez?** Ideiglenes vagy állandó licenc szükséges a termelési használathoz.

## Hogyan állítsuk be a PDF oldalméretet CAD‑ról PDF‑re konvertáláskor (Java)

A PDF oldalméret (vagy vászonméret) beállítása lehetővé teszi a dokumentum végső méreteinek meghatározását, ami különösen hasznos, ha a **PDF méreteket** nyomtatási szabványokhoz vagy UI‑követelményekhez kell igazítani. Az alábbiakban lépésről‑lépésre bemutatjuk, miért fontos minden kódsor.

## Mi a **convert CAD to PDF**?

A CAD‑ról PDF‑re konvertálás azt jelenti, hogy vektoralapú mérnöki rajzokat PDF‑oldalakká renderelünk, megőrizve a vonalakat, rétegeket és geometriát, miközben a fájlt univerzálisan elérhetővé tesszük.

## Miért állítsuk be a vászonméretet **java**‑ban?

A vászonméret beállítása Java‑ban lehetővé teszi a kimeneti felbontás és az oldaldimenziók meghatározását, biztosítva, hogy a létrehozott PDF vagy TIFF megfeleljen a nyomtatási vagy megjelenítési követelményeknek. Emellett szabályozhatja a méretezési viselkedést, ami nagyformátumú rajzok esetén elengedhetetlen.

## Előkövetelmények

Mielőtt elkezdené a gyakorlati példát, ellenőrizze, hogy a következő előfeltételek teljesülnek:

- Aspose.CAD for Java: Győződjön meg róla, hogy az Aspose.CAD könyvtár telepítve van a Java környezetében. Letöltheti [itt](https://releases.aspose.com/cad/java/).
- Dokumentumkönyvtár: Hozzon létre egy könyvtárat a CAD fájlok tárolására. Ez a könyvtár lesz hivatkozva a tutorial lépéseiben.

Most kezdjünk is hozzá a lépés‑ről‑lépésre útmutatóhoz.

## Import Namespaces

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

Ebben a kódrészletben beállítjuk az erőforráskönyvtár elérési útját, és betöltünk egy DXF fájlt az Aspose.CAD `Image` osztályával.

## 2. lépés: **CadRasterizationOptions** tulajdonságainak beállítása (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Itt példányosítunk egy `CadRasterizationOptions` objektumot, és konfiguráljuk a tulajdonságokat, mint például az oldal szélessége, magassága és a **automatic layout scaling**. Ez a **configure canvas mode** központi eleme a konverziónak.

## 3. lépés: PdfOptions létrehozása és VectorRasterizationOptions beállítása

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Most létrehozzuk a `PdfOptions` példányt, és beállítjuk a `VectorRasterizationOptions` tulajdonságát a korábban konfigurált `CadRasterizationOptions`‑ra.

## 4. lépés: Exportálás PDF‑be (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Végül a CAD képet PDF fájlba mentjük a megadott beállításokkal, befejezve a **convert CAD to PDF** folyamatot.

## 5. lépés: TiffOptions létrehozása és VectorRasterizationOptions beállítása (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ebben a lépésben egy `TiffOptions` példányt állítunk be, és konfiguráljuk a `VectorRasterizationOptions` tulajdonságát.

## 6. lépés: Exportálás TIFF‑be

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Végül a CAD képet TIFF fájlba mentjük a megadott beállításokkal, bemutatva, hogyan **export CAD to TIFF** a vászonméret konfigurálása után.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| A kimeneti PDF üres | `setNoScaling(true)` letiltja a renderelést bizonyos rajzoknál | Távolítsa el a `setNoScaling(true)`‑t, vagy állítsa `false`‑ra. |
| A TIFF felbontása alacsony | Az oldal szélessége/magassága túl kicsi | Növelje a `setPageWidth` / `setPageHeight` értékeket. |
| Az elrendezés torz | Az automatikus elrendezésméretezés le van tiltva | Győződjön meg róla, hogy a `setAutomaticLayoutsScaling(true)` engedélyezve van. |

## Miért módosítsuk a vászonméretet és a DPI‑t?

A vászonméret közvetlenül befolyásolja a kimenet rasterizációs felbontását. Ha **növelni kell a TIFF felbontását**, egyszerűen emelje a `setPageWidth` / `setPageHeight` értékeket, vagy hívja a `rasterizationOptions.setResolution(300)`‑t a `TiffOptions` létrehozása előtt. Így magas minőségű raszteres képeket kap, amelyek nyomtatásra vagy részletes vizsgálatra alkalmasak.

## Gyakran ismételt kérdések

### Q1: Használhatom az Aspose.CAD for Java‑t más Java keretrendszerekkel?

A1: Igen, az Aspose.CAD úgy lett tervezve, hogy zökkenőmentesen integrálódjon különböző Java keretrendszerekbe.

### Q2: Elérhető ideiglenes licenc az Aspose.CAD‑hez?

A2: Igen, ideiglenes licencet szerezhet [itt](https://purchase.aspose.com/temporary-license/).

### Q3: Hol kaphatok közösségi támogatást az Aspose.CAD‑hez?

A3: Látogassa meg az [Aspose.CAD fórumot](https://forum.aspose.com/c/cad/19) a közösségi támogatás és a megbeszélések miatt.

### Q4: Próbálhatom ingyenesen az Aspose.CAD‑t?

A4: Természetesen! Szerezzen ingyenes próbaverziót [itt](https://releases.aspose.com/).

### Q5: Hogyan vásárolhatok Aspose.CAD for Java licencet?

A5: A terméket megvásárolhatja [itt](https://purchase.aspose.com/buy).

**További Q&A**

**K: Befolyásolja a vászonméret a vektor minőségét a PDF‑ben?**  
V: Nem. A vászonméret az oldaldimenziókat szabályozza; a vektoradat felbontás‑független marad, így bármely nagyításnál éles marad.

**K: Beállíthatok más DPI‑t a TIFF kimenethez?**  
V: Igen. Módosítsa a `rasterizationOptions.setResolution(dpiValue)`‑t a `TiffOptions` létrehozása előtt.

**K: Hogyan **change PDF dimensions** egy meglévő PDF‑n anélkül, hogy újra renderelném a CAD‑et?**  
V: Használja az Aspose.PDF‑t a generált PDF betöltéséhez, és hívja a `pdf.getPages().setPageSize(PageSize.A4)`‑t vagy egy egyedi méretet.

**K: Mi a legjobb módja a **convert dxf to pdf** elvégzésének a rétegek megőrzésével?**  
V: Tartsa be a `setAutomaticLayoutsScaling(true)` beállítást, és kerülje a `setNoScaling(true)` használatát; ez megőrzi a rétegek láthatóságát és az elrendezés hűségét.

## Összegzés

Gratulálunk! Sikeresen **convert CAD to PDF** és **export CAD to TIFF** műveleteket hajtott végre **set canvas size java** használatával, engedélyezve az **automatic layout scaling**‑et, és megtanulta, hogyan **configure canvas mode** a magas minőségű kimenetekhez. Ez az útmutató szilárd alapot nyújt CAD konverziós projektjeihez. Fedezze fel a további funkciókat és lehetőségeket az [Aspose.CAD dokumentációban](https://reference.aspose.com/cad/java/).

---

**Utoljára frissítve:** 2026-02-15  
**Tesztelt verzió:** Aspose.CAD for Java 24.12  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}