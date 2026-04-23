---
date: 2026-03-21
description: Tanulja meg, hogyan hozhat létre PDF-et DWG‑ből, és exportálhat DGN‑t
  a DWG részeként az Aspose.CAD for .NET használatával. Ez az útmutató bemutatja,
  hogyan konvertálhatja a DWG‑t PDF‑re, és hogyan állíthatja be a PDF beállításait.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: PDF létrehozása DWG‑ből és DGN exportálása a DWG részeként – Aspose.CAD for
  .NET
url: /hu/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PDF létrehozása DWG-ből és DGN exportálása a DWG részeként – Aspose.CAD for .NET

## Bevezetés

Ha **PDF-et kell létrehoznod DWG** fájlokból, miközben egy DGN tervet is beágyazol a DWG-be, az Aspose.CAD for .NET egyszerűvé teszi ezt. Ebben az útmutatóban végigvezetünk a teljes munkafolyamaton: DWG betöltése, a beágyazott DGN alátábla megtalálása, a rasterizálási beállítások konfigurálása, és végül az eredmény exportálása PDF dokumentumba. Akár kötegelt konverziós eszközt, jelentéskészítő motorot vagy CAD‑BIM integrációs szolgáltatást építesz, az alábbi lépések szilárd, termelés‑kész alapot biztosítanak.

## Gyors válaszok
- **Melyik könyvtár kezeli a DWG → PDF konverziót?** Aspose.CAD for .NET  
- **Exportálhatok DGN alátáblát a PDF létrehozása közben?** Igen – az alátáblához a `CadDgnUnderlay` segítségével férhetsz hozzá.  
- **Melyik metódus állítja be a PDF beállításokat?** `PdfOptions` együtt a `CadRasterizationOptions`‑szal.  
- **Szükségem van licencre kereskedelmi használathoz?** Igen, érvényes Aspose.CAD licenc szükséges.  
- **Támogatott .NET verziók?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Mi az a „PDF létrehozása DWG-ből”?

A PDF létrehozása DWG fájlból azt jelenti, hogy a vektoros rajzot raster vagy vektor‑alapú PDF dokumentummá rendereljük. Ez a folyamat hasznos a rajzok megosztásához olyan érintettekkel, akiknek nincs CAD szoftvere, archiváláshoz vagy nyomtatható jelentések generálásához. Az Aspose.CAD leegyszerűsíti a feladatot, mivel a DWG entitások feldolgozását és a kimenet finomhangolását a `PdfOptions` segítségével végzi.

## Miért exportáljuk a DGN-t a DWG részeként?

A DGN alátáblát gyakran használják MicroStation projektek referenciageometriájaként. A DGN exportálásával a DWG‑vel együtt megőrzöd az eredeti tervezési kontextust, biztosítva, hogy a downstream felhasználók a teljes rajzkészletet lássák. Ez különösen értékes multidiszciplináris projektekben, ahol a DWG és DGN fájlok egyaránt jelen vannak.

## Előfeltételek

- **Aspose.CAD for .NET** – töltsd le [itt](https://releases.aspose.com/cad/net/).  
- **Fejlesztői környezet** – Visual Studio (bármely friss verzió) vagy a kedvenc .NET IDE-d.  
- **Alap C# ismeretek** – kényelmesen kell tudnod a C# szintaxist és a .NET projekt struktúráját.

## Névterek importálása

Add hozzá a szükséges `using` direktívákat a C# forrásfájlod tetejéhez:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Lépésről‑lépésre útmutató

### 1. lépés: Fájl útvonalak meghatározása

Állítsd be a bemeneti DWG fájlt és a kimeneti PDF nevét.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### 2. lépés: `PdfOptions` példány létrehozása (PDF beállítások megadása)

A `PdfOptions` lehetővé teszi a PDF generálásának irányítását, például az oldalméretet, tömörítést és metaadatokat.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### 3. lépés: DWG fájl betöltése

Töltsd be a DWG‑t `CadImage`‑ként, hogy ellenőrizhesd az entitásait.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### 4. lépés: Entitások bejárása

Járd be a rajz minden entitását, hogy megtaláld a DGN alátáblát.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### 5. lépés: Entitás típusának ellenőrzése (hogyan exportáljuk a dgn-t)

Azonosítsd, hogy a jelenlegi entitás DGN alátábla-e.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### 6. lépés: Alátáblá útvonalának lekérése

Szerezd meg a DGN fájl külső hivatkozási útvonalát.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### 7. lépés: Rasterizálási beállítások meghatározása (DWG konvertálása PDF-be)

Állítsd be, hogyan legyen rasterizálva a DWG, mielőtt a PDF‑be kerül.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### 8. lépés: DWG exportálása PDF-be

Végül mentsd el a renderelt képet PDF fájlként.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| **`Image.Load` throws “File not found”** | Helytelen útvonal vagy hiányzó fájl. | Használj abszolút útvonalat, vagy győződj meg róla, hogy a DWG a kimeneti mappába másolva van. |
| **Underlay path is empty** | DGN alátábla nincs beágyazva vagy a hivatkozás hibás. | Ellenőrizd, hogy a DWG valóban tartalmaz DGN alátáblát, és hogy a külső DGN fájl elérhető. |
| **PDF output is blank** | Rasterizálási beállítások nulla méretűek. | Állítsd be a `PageWidth`/`PageHeight` értékeket, vagy állítsd `NoScaling = false`‑ra. |
| **License exception** | Érvénytelen vagy hiányzó Aspose.CAD licenc. | Alkalmazd a licencet a kép betöltése előtt: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Gyakran ismételt kérdések

### Q1: Használhatom az Aspose.CAD for .NET-et kereskedelmi projektjeimben?
A1: Igen, használhatod. Látogass el [ide](https://purchase.aspose.com/buy) a licencelési lehetőségek megtekintéséhez.

### Q2: Van korlátozás a feldolgozható DWG fájlok méretére vonatkozóan?
A2: Az Aspose.CAD nagy DWG fájlok kezelését támogatja, de a hardver korlátai érvényesülhetnek.

### Q3: Elérhető-e próbaverzió?
A3: Igen, ingyenes próbaverziót kaphatsz [itt](https://releases.aspose.com/).

### Q4: Hogyan juthatok ideiglenes licencekhez?
A4: Ideiglenes licenceket szerezhetsz [itt](https://purchase.aspose.com/temporary-license/).

### Q5: Hol kérhetek segítséget, ha problémába ütközöm?
A5: Látogass el az Aspose.CAD fórumra [ide](https://forum.aspose.com/c/cad/19) támogatásért.

**Q: Hogyan állíthatok be további PDF metaadatokat (szerző, cím, stb.)?**  
A: Használd az `exportOptions.Metadata` tulajdonságokat a `Save` hívása előtt.

**Q: Exportálhatok több elrendezést külön PDF oldalakra?**  
A: Igen – állítsd be a `Layouts = new string[] { "Layout1", "Layout2" }` értéket a `CadRasterizationOptions`‑ban.

**Q: Támogatja-e az Aspose.CAD a DWG konvertálását más képformátumokra?**  
A: Teljes mértékben. Exportálhatsz PNG, JPEG, SVG és további formátumokba a megfelelő `Image.Save` túlterhelésekkel.

---

**Utolsó frissítés:** 2026-03-21  
**Tesztelve:** Aspose.CAD 24.11 for .NET  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}