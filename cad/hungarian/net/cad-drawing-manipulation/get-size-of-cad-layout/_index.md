---
date: 2026-03-21
description: Ismerje meg, hogyan lehet lekérni a CAD elrendezés méretét .NET‑ben az
  Aspose.CAD használatával. Kövesse lépésről‑lépésre útmutatónkat a hatékony CAD fájlkezeléshez.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD elrendezés méretének lekérése az Aspose.CAD for .NET‑ben
url: /hu/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD elrendezés méretének lekérése az Aspose.CAD for .NET-ben

## Bevezetés

Ebben az átfogó oktatóanyagban megtudja, **hogyan lehet lekérni a CAD elrendezés méretét** az Aspose.CAD .NET könyvtár segítségével. Akár CAD nézőt épít, előnézeti képeket generál, vagy pontos elrendezésméretekre van szüksége a további feldolgozáshoz, a minden egyes elrendezés pontos méretének ismerete elengedhetetlen. Végigvezetjük a teljes munkafolyamaton – a rajz betöltésétől az elrendezés méreteinek kinyeréséig, illetve opcionálisan képként való mentéséig – hogy magabiztosan integrálhassa ezt a funkciót saját alkalmazásaiba.

## Gyors válaszok
- **Mit jelent a „get CAD layout size”?** Ez azt jelenti, hogy a CAD fájl minden nem‑üres elrendezésének (paper space) szélességét és magasságát (rajz egységekben) lekérdezzük.  
- **Melyik könyvtár támogatja ezt?** Az Aspose.CAD for .NET egyszerű API-t biztosít az elrendezésinformációk eléréséhez.  
- **Szükség van licencre?** Ingyenes próba verzióval értékelhető; a kereskedelmi licenc kötelező a termelésben való használathoz.  
- **Támogatott formátumok?** A DWG, DXF és számos más CAD/BIM formátum teljes körűen támogatott.  
- **Tipikus implementációs idő?** Körülbelül 10‑15 perc egy alap méretlekérdező rutin elkészítéséhez.

## Mi az a „get CAD layout size”?
A CAD elrendezés méretének lekérése azt jelenti, hogy kinyerjük minden elrendezés (paper space) geometriai kiterjedését, amely a CAD rajzban definiálva van. Ezek a kiterjedések a rajz natív egységeiben (általában milliméter vagy hüvelyk) vannak megadva, és hasznosak például méretezéshez, nyomtatáshoz vagy előnézeti képek generálásához.

## Miért kell lekérni a CAD elrendezés méretét az Aspose.CAD használatával?
- **CAD szoftver nélkül** – Teljesen szerveroldalon működik.  
- **Kereszt‑platform** – .NET Framework, .NET Core és .NET 5/6+ környezetekkel kompatibilis.  
- **Pontos mérések** – A fájlban tárolt pontos kiterjedéseket adja vissza, elkerülve a kézi elemzést.  
- **Könnyű integráció** – Egyszerű API‑hívások természetesen illeszkednek a meglévő C# projektekbe.

## Előkövetelmények

Mielőtt belemerülnénk a kódba, győződjön meg arról, hogy a következőkkel rendelkezik:

- Aspose.CAD for .NET telepítve van. Letöltheti a [Aspose.CAD for .NET letöltési oldalról](https://releases.aspose.com/cad/net/).
- Egy vagy több CAD fájl (DWG, DXF, stb.), amelyet elemezni szeretne. Ebben az útmutatóban a `conic_pyramid.dxf` és a `Bottom_plate.dwg` mintafájlokat használjuk.

## Névtér importálása

A .NET projektjében kezdje a szükséges névterek importálásával:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Lépés 1: A dokumentum könyvtár beállítása

Határozza meg azt a mappát, amely a CAD fájlokat tartalmazza. Cserélje le a helyőrzőt a gépén lévő tényleges útvonalra.

```csharp
string MyDir = "Your Document Directory";
```

## Lépés 2: CAD fájl útvonalak megadása

Hozzon létre egy tömböt, amely az összes feldolgozni kívánt CAD fájlra mutat.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Lépés 3: CAD fájlok iterálása

Töltse be minden fájlt, ismerje fel a formátumát, és készüljön fel az elrendezésinformációk kinyerésére.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## Lépés 4: Nem üres elrendezések lekérése

Szükségünk van egy segédfüggvényre, amely csak azokat az elrendezéseket adja vissza, amelyek ténylegesen tartalmaznak rajzelemeket. Az üres elrendezéseket figyelmen kívül hagyjuk, mivel nincs méretük, amit jelenteni lehetne.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## Lépés 5: Elrendezések lekérése DWG fájlokhoz

A DWG fájlok a `HeaderVariables` táblában tárolják az elrendezésinformációkat. Az alábbi módszer kinyeri az összes nem‑üres elrendezés nevét egy DWG rajzhoz.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Lépés 6: Elrendezések lekérése DXF fájlokhoz

A DXF fájlok más struktúrát használnak. Ez a metódus a `Tables` gyűjteményt elemzi, hogy megtalálja az entitásokat tartalmazó paper space elrendezéseket.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Lépés 7: Elrendezés méretének lekérése és mentése képként

Végül iteráljon minden felfedezett elrendezésen, olvassa ki a kiterjedéseket, és opcionálisan renderelje az elrendezést egy képfájlba a vizuális ellenőrzéshez.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## Gyakori problémák és tippek

- **Hiányzó elrendezésnevek:** Győződjön meg arról, hogy a CAD fájl valóban tartalmaz paper space elrendezéseket; egyes fájlok csak model space‑t tartalmaznak.  
- **Helytelen egységek:** A méret a rajz natív egységeiben kerül visszaadásra. Szükség esetén konvertálja milliméterre vagy hüvelykre.  
- **Teljesítmény:** Nagyon nagy DWG/DXF fájlok betöltése memóriaigényes lehet; fontolja meg a fájlok aszinkron vagy kötegelt feldolgozását.

## Gyakran feltett kérdések

**Q: Az Aspose.CAD kompatibilis minden CAD fájlformátummal?**  
A: Igen, az Aspose.CAD széles körű formátumtámogatást nyújt, beleértve a DWG, DXF, DGN és számos BIM fájltípust.

**Q: Testreszabhatom a képm mentési beállításokat?**  
A: Természetesen! A `CadRasterizationOptions` (formátum, felbontás, háttérszín stb.) módosításával a saját igényeihez igazíthatja a kimenetet.

**Q: Hol találok további dokumentációt?**  
A: Tekintse meg az [Aspose.CAD dokumentációt](https://reference.aspose.com/cad/net/) a részletes API‑referenciákért és további példákért.

**Q: Elérhető ingyenes próba?**  
A: Igen, felfedezheti az Aspose.CAD-et egy [ingyenes próbaverzióval](https://releases.aspose.com/).

**Q: Hogyan kaphatok technikai támogatást?**  
A: Technikai támogatásért látogasson el az [Aspose.CAD fórumra](https://forum.aspose.com/c/cad/19).

---

**Utolsó frissítés:** 2026-03-21  
**Tesztelve a következővel:** Aspose.CAD 24.11 for .NET  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}