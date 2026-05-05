---
date: 2026-03-29
description: Tanulja meg, hogyan cserélhet gyorsan betűtípusokat az Aspose.CAD for
  .NET-ben. Ez a lépésről‑lépésre útmutató megmutatja, hogyan állíthatja be az elsődleges
  betűtípus nevét, és hogyan testreszabhatja hatékonyan a CAD‑rajzokat.
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hogyan cseréljünk betűtípusokat az Aspose.CAD .NET-ben
url: /hu/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan cseréljünk betűtípusokat az Aspose.CAD for .NET-ben

## Bevezetés

A .NET használatával történő CAD fejlesztés területén a **betűtípusok cseréjének megtanulása** kulcsfontosságú készség, amely drámaian javíthatja a rajzok vizuális minőségét. Az Aspose.CAD for .NET egyszerű API-t kínál, amely lehetővé teszi a **primer betűtípus nevének** beállítását bármely stílushoz, így a globális vagy szelektív betűtípuscsere könnyedén megvalósítható. Ebben az útmutatóban végigvezetünk a teljes folyamaton – a rajz betöltésétől a betűtípusok globális vagy egyedi stílusnév szerinti cseréjéig.

## Gyors válaszok
- **Mi a fő osztály a CAD manipulációhoz?** `Aspose.CAD.Image` (vagy a származtatott `CadImage`).
- **Melyik tulajdonság változtatja a betűtípust?** `PrimaryFontName` a `CadStyleTableObject`-on.
- **Lecserélhetem a betűtípusokat minden stílusra egyszerre?** Igen, iteráljon a `cadImage.Styles`-en és állítsa be a tulajdonságot.
- **Szükségem van licencre a termeléshez?** Érvényes Aspose.CAD licenc szükséges a nem‑próba használathoz.
- **Támogatott .NET verziók?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Mi a betűtípus helyettesítés a CAD-ban?
A betűtípus helyettesítés azt jelenti, hogy a CAD rajzban eredetileg használt betűkészletet egy olyanra cseréljük, amely elérhető a célrendszeren. Ez különösen hasznos, ha az eredeti betűtípus hiányzik, ha egységes vállalati stílusra van szükség, vagy ha a rajzokat olyan nyomtatókra készítik, amelyek csak korlátozott betűtípuskészletet támogatnak.

## Miért cseréljünk betűtípusokat az Aspose.CAD-vel?
- **Nincsenek külső függőségek** – a könyvtár belsőleg kezeli a betűtérképezést.
- **Sok formátummal működik** – DXF, DWG, DGN és még sok más.
- **Programozott vezérlés** – automatizálható a folyamat kötegelt konverziókhoz vagy CI pipeline-okhoz.
- **Megőrzi a rajz geometriáját** – csak a szöveg vizuális megjelenése változik.

## Előfeltételek

- Alapvető .NET programozási ismeretek.
- Aspose.CAD for .NET telepítve. Ha még nem telepítette, töltse le [itt](https://releases.aspose.com/cad/net/).
- Egy CAD rajzfájl (DXF, DWG stb.) a kísérletezéshez.

## Névterek importálása

Mielőtt elkezdené, importálja a szükséges névtereket az Aspose.CAD funkciók eléréséhez .NET alkalmazásában.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## 1. lépés: CAD rajz betöltése

Kezdje a CAD rajz betöltésével egy `CadImage` példányba. Győződjön meg róla, hogy a helyes útvonalat adja meg a dokumentum könyvtárához.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## 2. lépés: Stílusok iterálása

Ezután iteráljon a CAD rajz stílusain egy `foreach` ciklussal. Ez lehetővé teszi az egyes betűstílusok elérését és módosítását.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## Hogyan állítsuk be az elsődleges betűtípus nevét a betűtípus helyettesítéshez

A `PrimaryFontName` tulajdonság minden `CadStyleTableObject` esetén szabályozza, hogy melyik betűtípus legyen használva a rajz renderelésekor. Ennek beállításával hatékonyan lecserélheti az eredeti betűtípust.

### 3. lépés: Betűtípusok helyettesítése globálisan

Az **összes** stílus betűtípusának cseréjéhez állítsa be a `PrimaryFontName` tulajdonságot minden stílusra a kívánt betűtípus nevére, például `"Arial"`.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### 4. lépés: Betűtípus helyettesítése stílusnév alapján

Ha csak egy adott stílus (például a `"Roman"` nevű) betűtípusát szeretné cserélni, adjon hozzá egy feltételes ellenőrzést a ciklusba.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## Gyakori problémák és hibaelhárítás

| Probléma | Ok | Megoldás |
|----------|----|----------|
| A betűtípus nem változik a kód futtatása után | A rajz gyorsítótárazva van vagy csak‑olvasás módban nyílt meg | Győződjön meg róla, hogy a módosítás után elmenti a képet (`cadImage.Save(...)`), vagy töltse be újra a fájlt a ellenőrzéshez. |
| A kívánt betűtípus nem található a rendszeren | A betűtípus nincs telepítve azon a gépen, ahol a kód fut | Telepítse a szükséges TrueType/OpenType betűtípust, vagy ágyazza be az alkalmazás erőforrásaiba. |
| A szöveg torzult | Helytelen kódolás vagy hiányzó Unicode támogatás | Használjon olyan betűtípust, amely támogatja a szükséges karakterkészletet (pl. Arial Unicode MS). |

## Gyakran Ismételt Kérdések

**K: Vissza tudom állítani a betűtípus változtatásokat az Aspose.CAD for .NET-ben?**  
A: Igen, visszaállíthatja az eredeti CAD rajz újratöltésével vagy a módosítások előtt készített biztonsági másolat megtartásával.

**K: Vannak más betűtípus tulajdonságok, amelyeket módosíthatok?**  
A: Természetesen. A `PrimaryFontName` mellett dolgozhat a `SecondaryFontName`, `FontFamily` és más stílus‑kapcsolódó attribútumokkal a fejlett testreszabáshoz.

**K: Az Aspose.CAD kompatibilis különböző CAD formátumokkal?**  
A: Igen, az Aspose.CAD számos formátumot támogat, például DXF, DWG, DGN, DWF és még sok más, így rugalmasságot biztosít a projektek között.

**K: Automatizálhatom a betűtípus helyettesítést kötegelt feldolgozásban?**  
A: Természetesen. A betöltési és helyettesítési logikát egy ciklusba ágyazhatja, amely egy mappában lévő CAD fájlokon iterál, vagy integrálhatja CI/CD folyamatba.

**K: Hol találok további támogatást az Aspose.CAD for .NET-hez?**  
A: További támogatásért és közösségi megbeszélésekért látogasson el az [Aspose.CAD fórumra](https://forum.aspose.com/c/cad/19).

---

**Utolsó frissítés:** 2026-03-29  
**Tesztelve:** Aspose.CAD for .NET (legújabb kiadás)  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}