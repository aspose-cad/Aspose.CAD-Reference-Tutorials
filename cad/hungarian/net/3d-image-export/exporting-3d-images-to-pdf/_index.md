---
date: 2026-07-04
description: Ismerje meg, hogyan állíthatja be a PDF oldalméretet, és exportálhat
  PDF-et 3D CAD képekből az Aspose.CAD for .NET használatával – egy lépésről‑lépésre
  útmutató a DWG PDF‑re konvertálásához és a CAD PDF‑ként történő mentéséhez.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: 3D képek exportálása PDF-be
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: PDF oldalméret beállítása – 3D képek exportálása PDF-be az Aspose.CAD segítségével
url: /hu/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 3D képek exportálása PDF-be – Aspose.CAD útmutató

## Bevezetés

Ha **PDF oldalméretet** kell beállítania egy 3‑D CAD rajz PDF-be konvertálása közben, jó helyen jár. Ez az útmutató lépésről lépésre megmutatja, hogyan töltsön be egy CAD fájlt, konfigurálja a rasterizálási beállításokat – beleértve az egyedi oldalméreteket – és generáljon magas hűségű PDF-et az Aspose.CAD for .NET használatával. A végére képes lesz **PDF exportálására CAD-ből**, **CAD mentésére PDF-ként**, és minden elrendezési részletet irányítani AutoCAD telepítése nélkül.

## Gyors válaszok
- **Mi jelent a „PDF exportálása CAD-ből”?** Egy CAD rajzot (DWG, DXF, DGN stb.) PDF‑be konvertál, amely bármely eszközön megnyitható.  
- **Melyik könyvtár végzi a konverziót?** Az Aspose.CAD for .NET rasterizálást és PDF exportot biztosít külső függőségek nélkül.  
- **Szükségem van licencre?** Ideiglenes vagy teljes licenc szükséges a termeléshez; ingyenes próba elérhető.  
- **Beállíthatok egyedi oldalméreteket?** Igen – használja a `PageWidth` és `PageHeight` értékeket a `RasterizationOptions`‑ban.  
- **Megmarad a 3‑D geometria?** A 3‑D elemek rasterizálva lesznek; a teljes 3‑D támogatáshoz engedélyezze a `TypeOfEntities.Entities3D`‑t.  

## Mi az a „PDF exportálás” a CAD kontextusában?

A PDF exportálása CAD-ből azt jelenti, hogy egy CAD rajzot (DWG, DXF, DGN stb.) PDF fájlba konvertálunk, amely tartalmazhat vektoros grafikát, rasterizált 3‑D nézeteket és pontos oldalelrendezési információkat, így könnyen megosztható azokkal, akiknek nincs CAD szoftverük.

## Miért használja az Aspose.CAD‑t PDF exportáláshoz?

Az Aspose.CAD lehetővé teszi, hogy **PDF oldalméretet** állítson be, és PDF-eket exportáljon teljesen menedzselt .NET kódból. Több mint 50 CAD formátumot támogat, akár 2 GB‑os fájlokat is feldolgoz anélkül, hogy a teljes dokumentumot a memóriába töltené, és megőrzi a vonalvastagságokat, színeket, valamint az opcionális 3‑D elemek renderelését akár 1200 DPI rasterizációval. A könyvtár Windows, Linux és macOS rendszereken fut, így a generált PDF-ek minden platformon működnek.

## Előkövetelmények

- **Aspose.CAD for .NET** telepítve. Töltse le a [Aspose.CAD for .NET letöltési oldalról](https://releases.aspose.com/cad/net/).
- Egy mappa, amely a konvertálni kívánt CAD fájlokat tartalmazza (pl. `C:\CAD\`).
- .NET 6.0 vagy újabb (vagy .NET Framework 4.7.2).

## Névtér importálása

`using` utasítások importálják az Aspose.CAD névtereket, amelyek a rasterizáláshoz és a PDF beállításokhoz szükségesek.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Lépésről‑lépésre útmutató

### Hogyan állítsuk be a PDF oldalméretet CAD PDF‑be exportálásakor?

Töltse be a CAD fájlt, konfigurálja az oldalméreteket a `RasterizationOptions`‑ban, csatolja ezeket az opciókat egy `PdfOptions` példányhoz, és hívja meg a `Save`‑t. Ez a négylépéses folyamat teljes irányítást biztosít a kimeneti méret és minőség felett, miközben a kód rövid marad.

### 1. lépés: CAD kép betöltése

Az `Image` osztály egy memóriába betöltött CAD rajzot képvisel, amely készen áll a rasterizálásra.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### 2. lépés: Rasterizálási beállítások konfigurálása (CAD mentése PDF‑ként)

A `RasterizationOptions` osztály meghatározza, hogyan kerül rasterizálásra a CAD adat, beleértve az oldalméretet, DPI‑t és hogy a 3‑D elemek renderelve legyenek-e.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### 3. lépés: PDF beállítások megadása (PDF létrehozása CAD‑ból)

A `PdfOptions` osztály tartalmazza a kimeneti formátum beállításait, és összekapcsolja a rasterizálási beállításokat a PDF generálással.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 4. lépés: Mentés PDF‑ként (PDF generálása 3D modellből)

A `Save` metódus az `Image` objektumon a rasterizált tartalmat a megadott PDF fájlba írja, így egy megosztható dokumentumot hoz létre.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| **A kimeneti PDF üres** | Helytelen elrendezés neve vagy hiányzó `Model` elrendezés. | Ellenőrizze, hogy a `rasterizationOptions.Layouts` megegyezik-e a CAD fájlban lévő elrendezéssel. |
| **Alacsony felbontás** | Az alapértelmezett rasterizálási DPI alacsony. | Állítsa be a `rasterizationOptions.Resolution = 300;` értéket a mentés előtt. |
| **A 3‑D elemek nem jelennek meg** | `TypeOfEntities` ki van kommentálva. | Kommentár eltávolítása a `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;` sorból. |
| **Licenc kivétel** | Próba verzió használata licenc nélkül. | Alkalmazzon ideiglenes vagy állandó licencet a `License license = new License(); license.SetLicense("Aspose.CAD.lic");` kóddal. |

## Gyakran Ismételt Kérdések

**Q: Az Aspose.CAD kompatibilis minden CAD fájlformátummal?**  
A: Igen, az Aspose.CAD több mint 50 bemeneti és kimeneti formátumot támogat, beleértve a DWG, DXF, DGN, STL és IFC formátumokat, biztosítva a rugalmasságot bármely projekthez.

**Q: Testreszabhatom az oldalméreteket PDF exportálásakor?**  
A: Természetesen. Állítsa be a `PageWidth` és `PageHeight` értékeket a `RasterizationOptions`‑ban bármilyen méretre pontban, hüvelykben vagy milliméterben a `Save` hívása előtt.

**Q: Elérhetők ideiglenes licencek az Aspose.CAD‑hez?**  
A: Igen, ideiglenes licenceket szerezhet az Aspose.CAD‑hez a [Temporary License](https://purchase.aspose.com/temporary-license/) oldalon.

**Q: Hol találok további támogatást vagy közösségi megbeszéléseket?**  
A: Látogasson el az [Aspose.CAD Fórumra](https://forum.aspose.com/c/cad/19) szakértői segítség és közösségi tanácsokért.

**Q: Van ingyenes próba verziója az Aspose.CAD‑nek?**  
A: Igen, felfedezheti az Aspose.CAD funkcióit a [free trial](https://releases.aspose.com/) elérésével.

## Összegzés

Most már rendelkezik egy teljes, termelésre kész módszerrel a **PDF oldalméret beállítására** és a **PDF exportálására 3D CAD képekből** az Aspose.CAD for .NET használatával. A rasterizálási beállítások módosításával finomhangolhatja a felbontást, az oldalelrendezést és a 3‑D elemek renderelését, hogy megfeleljen bármilyen dokumentációs követelménynek. Kísérletezzen különböző DPI beállításokkal és oldalméretekkel, hogy elérje a tökéletes egyensúlyt a fájlméret és a vizuális hűség között.

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó útmutatók

- [Specifikus elrendezések exportálása PDF‑be – Aspose.CAD útmutató](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [DWG exportálása PDF‑be vagy raszter képekké – Aspose.CAD útmutató](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [DGN exportálása PDF‑be az Aspose.CAD for .NET-ben](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Utoljára frissítve:** 2026-07-04  
**Tesztelve a következővel:** Aspose.CAD 24.11 for .NET  
**Szerző:** Aspose