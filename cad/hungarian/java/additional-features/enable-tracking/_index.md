---
date: 2025-12-03
description: Tanulja meg, hogyan állíthatja be a PDF oldalméretet a DWG PDF-re konvertálása
  során, és hogyan engedélyezheti a nyomkövetést a DWG fájlokban az Aspose.CAD for
  Java használatával – egy átfogó útmutató a CAD rajz pontos PDF-exportálásához.
language: hu
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: PDF oldalméret beállítása és nyomkövetés engedélyezése DWG fájlokban az Aspose.CAD
  Java használatával
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF oldalméret beállítása és nyomkövetés engedélyezése DWG fájlokban az Aspose.CAD Java használatával

## Bevezetés

Ha **PDF oldalméretet** kell beállítania, amikor *DWG‑t PDF‑re konvertál*, és emellett nyomon szeretné követni az esetleges renderelési problémákat, az Aspose.CAD for Java tiszta, programozott módot biztosít mindkettőhöz. Ebben az útmutatóban lépésről‑lépésre bemutatjuk, hogyan konfigurálja az oldalméreteket, engedélyezi a nyomkövetést, és exportál egy CAD‑rajz PDF‑et – mindezt Java‑ból. A végére megérti, miért fontos a megfelelő oldalméret beállítása CAD‑rajzoknál, és hogyan rögzíthet részletes nyomkövetési információkat az exportálás során.

## Gyors válaszok
- **Mit befolyásol a “set PDF page size”?** Meghatározza a létrejövő PDF vászon szélességét és magasságát, biztosítva, hogy a rajz tökéletesen illeszkedjen.  
- **Szükség van licencre a funkció használatához?** A próba verzió tesztelésre elegendő; a gyártási környezethez kereskedelmi licenc szükséges.  
- **Melyik Aspose.CAD verzió szükséges?** Bármely, a `CadRasterizationOptions`‑t támogató friss verzió.  
- **Használható más CAD formátumokkal is?** A példa DWG/DXF‑et mutat, de ugyanaz a megközelítés a legtöbb támogatott formátumnál működik.  
- **Mennyi időt vesz igénybe a konvertálás?** Általában egy másodpercnél kevesebb közepes méretű fájloknál; nagyobb rajzok esetén hosszabb lehet.

## Mi az a “set PDF page size” a CAD exportálás kontextusában?
A PDF oldalméret beállítása azt jelzi a renderelőnek, hogy pontosan milyen méretekkel (pixelben vagy pontban) kell létrehozni a kimeneti vászont. Ez különösen fontos a műszaki rajzoknál, ahol a méretarány és az elrendezés megőrzése elengedhetetlen. Kifejezett oldalméret beállítás nélkül a PDF alapértelmezett méretre állhat, ami levágja vagy torzítja a rajzot.

## Miért kell PDF oldalméretet beállítani CAD rajzok exportálásakor?
- **Mérleg megőrzése** – A mérnökök a méretarányos nyomatokra támaszkodnak.  
- **Papírhoz igazítás** – Válasszon A4, Letter vagy egyedi méretet, amely megfelel a projekt specifikációinak.  
- **Olvashatóság javítása** – A nagyobb oldalak finom részleteket mutatnak nagyítás nélkül.  
- **Konzisztens kimenet** – Az automatizált folyamatok minden futtatáskor azonos méretű PDF-eket állítanak elő.

## Hogyan állítsuk be a PDF oldalméretet DWG PDF-re konvertálásakor?
Az alábbiakban a `CadRasterizationOptions`‑t konfiguráljuk egyedi szélesség‑ és magasságértékekkel az exportálás előtt. Ez a lépés közvetlenül a **set PDF page size** kulcsszóra reagál.

## Előkövetelmények

- **Java Development Kit (JDK)** – Java 8 vagy újabb telepítve a gépén.  
- **Aspose.CAD for Java** – Töltse le a hivatalos [Aspose CAD letöltési oldalról](https://releases.aspose.com/cad/java/).  
- **Dokumentum könyvtár** – Egy mappa, amely a feldolgozni kívánt DWG/DXF fájlokat tartalmazza.

## Névterek importálása

Először importálja a szükséges osztályokat. A kódrészlet változatlanul marad az eredeti útmutatóból.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## 1. lépés: DWG/DXF fájl betöltése

Töltse be a forrásrajzot. Igazítsa az elérési utat a saját fájljához.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## 2. lépés: PDF exportálási beállítások konfigurálása (beleértve az oldalméretet)

Itt állítjuk be az oldal szélességét és magasságát – ez a **set PDF page size** lépés. Az értékek pixelben vannak; szükség szerint átválthatók hüvelykre vagy milliméterre.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Tip:** Ha szabványos papírméreteket szeretne használni, alkalmazza az átváltást `1 inch = 72 points`. Egy A4 oldal (8.27 × 11.69 in) esetén állítsa be `pageWidth = 595` és `pageHeight = 842`.

## 3. lépés: Nyomkövetés megvalósítása

A nyomkövetés rögzíti a renderelési problémákat. Egy egyedi kezelőt csatolunk, amely az exportálás után meghívódik.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## 4. lépés: Exportálás PDF-be

Most hajtsa végre a konvertálást. A PDF a megadott méretekkel jön létre, a nyomkövetési információk pedig a konzolra kerülnek.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## 5. lépés: CadRenderHandler osztály

A kezelő kiírja az esetlegesen előforduló hibákat a renderelés során. Ez segít a hibakeresésben, amikor **exporting CAD drawing PDF**‑et végez.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| **Blank PDF** | Az oldalméret 0‑ra vagy túl kicsire van állítva | Ellenőrizze, hogy a `setPageWidth` és `setPageHeight` pozitív értékek legyenek. |
| **Missing geometry** | A kezelő által rögzített renderelési hibák | Tekintse át a `ErrorHandler` konzolkimenetét, és kezelje a konkrét `RenderCode`‑ot. |
| **File not found** | Hibás `dataDir` útvonal | Használjon abszolút elérési utat, vagy győződjön meg a könyvtár létezéséről. |
| **License exception** | Próba verzió használata érvényes licenc nélkül nagy fájlokhoz | Alkalmazza az Aspose.CAD licencet a kép betöltése előtt. |

## Gyakran Ismételt Kérdések

**Q: Engedélyezhetem a nyomkövetést más CAD fájlformátumokhoz az Aspose.CAD for Java‑val?**  
A: Az Aspose.CAD elsősorban DWG/DXF nyomkövetést támogat. Más formátumok esetén tekintse meg a hivatalos dokumentációt.

**Q: Hogyan kezelhetek további exportálási beállításokat az Aspose.CAD for Java‑ban?**  
A: A könyvtár számos lehetőséget kínál, például DPI, háttérszín és vektoros rasterizálás. Lásd a [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) részleteit.

**Q: Van elérhető próba verzió az Aspose.CAD for Java‑hoz?**  
A: Igen, letölthet egy ingyenes próbaverziót a [Aspose.CAD Free Trial](https://releases.aspose.com/) oldalról.

**Q: Hol kérhetek segítséget vagy vitathatok meg problémákat az Aspose.CAD for Java‑val kapcsolatban?**  
A: Látogassa meg az [Aspose.CAD fórumot](https://forum.aspose.com/c/cad/19) a közösségi támogatásért és hivatalos válaszokért.

**Q: Hogyan szerezhetek ideiglenes licencet az Aspose.CAD for Java‑hoz?**  
A: Kövesse a [Temporary License](https://purchase.aspose.com/temporary-license/) oldalon leírt lépéseket.

**Utolsó frissítés:** 2025-12-03  
**Tesztelve:** Aspose.CAD for Java 24.11 (legújabb a megírás időpontjában)  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}