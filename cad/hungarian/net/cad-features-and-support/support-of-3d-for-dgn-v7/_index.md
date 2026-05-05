---
date: 2026-03-29
description: Ismerje meg, hogyan konfigurálhatja a CAD rasterizálási beállításokat,
  és exportálhatja a DGN-t PDF-be 3D támogatással az Aspose.CAD for .NET használatával.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD raszterizálási beállítások konfigurálása a DGN V7 3D-hez
url: /hu/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD rasterizálási beállítások konfigurálása DGN V7 3D-hoz

## Bevezetés

Ebben az átfogó útmutatóban megtanulja, **hogyan konfigurálja a CAD rasterizálási beállításokat**, hogy egy 3‑D DGN V7 fájlt PDF-be exportáljon az Aspose.CAD for .NET segítségével. Akár CAD nézegetőt, jelentéskészítő eszközt vagy automatizált konverziós folyamatot épít, ezen beállítások elsajátítása pontos irányítást biztosít az oldalméret, a layout méretezés, a háttérszínek és a megjeleníteni kívánt nézetek felett. Lépésről lépésre végigvezetjük a folyamatot.

## Gyors válaszok
- **Mit jelent a „CAD rasterizálási beállítások konfigurálása”?**  
  Ez a CAD fájl raster formátumba (például PDF) történő konvertálása előtt a lapméretek, a méretezés, a háttérszín és a layout kiválasztása stb. tulajdonságainak beállítását jelenti.
- **Hogyan exportáljuk a DGN-t PDF-be 3‑D támogatással?**  
  Töltsük be a DGN-t a `DgnImage` segítségével, definiáljuk a `PdfOptions` + `CadRasterizationOptions` beállításokat, majd hívjuk a `Save` metódust.
- **Szükségem van licencre a termeléshez?**  
  Igen – a telepítéshez kereskedelmi licenc szükséges; ingyenes próba is elérhető.
- **Mely .NET verziók támogatottak?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Kiválaszthatok konkrét nézeteket az exportáláshoz?**  
  Természetesen – állítsa be a `Layouts` tömböt a rasterizálási beállításokban.

## Mi a „CAD rasterizálási beállítások konfigurálása”?

A CAD rasterizálási beállítások konfigurálása azt jelenti, hogy testre szabja, hogyan kerül rasterizálásra (vektorról bitmapre vagy PDF-re) egy CAD rajz. Ezeknek a beállításoknak a módosításával irányíthatja a vizuális kimenetet, a teljesítményt és a létrejövő dokumentum fájlméretét.

## Miért használjuk az Aspose.CAD-et 3‑D DGN V7 exportáláshoz?

- **Teljes .NET integráció** – nincs szükség COM vagy natív DLL-ekre.  
- **3‑D geometria támogatása** – megőrzi a mélységi információkat PDF-re rendereléskor.  
- **Finomhangolt vezérlés** – válassza ki a pontos layoutokat, a méretezést és a háttérszíneket.  
- **Keresztplatformos** – működik Windows, Linux és macOS rendszereken .NET Core használatával.

## Előfeltételek

Mielőtt elkezdené, győződjön meg róla, hogy rendelkezik:

- **Aspose.CAD for .NET** – töltse le [itt](https://releases.aspose.com/cad/net/).  
- **Visual Studio** vagy bármely kompatibilis .NET IDE.  
- **Egy minta DGN fájl** – ebben az útmutatóban a `Nikon_D90_Camera.dgn` fájlt használjuk (az Aspose minta csomagban szerepel).  

Most, hogy minden készen áll, merüljünk el a kódban.

## Névterek importálása

A .NET projektjében importálja a szükséges névtereket:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## 1. lépés: Dokumentumkönyvtár beállítása

Hozzon létre egy változót, amely a forrás DGN és a kimeneti fájlok tárolására szolgáló mappára mutat.

```csharp
string MyDir = "Your Document Directory";
```

## 2. lépés: DGN fájl betöltése

Töltse be a DGN fájlt `DgnImage`-ként. Ez az objektum hozzáférést biztosít a CAD adatokhoz és a rasterizálási folyamathoz.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## 3. lépés: PDF exportálási beállítások konfigurálása (CAD rasterizálási beállítások konfigurálása)

Itt **konfiguráljuk a CAD rasterizálási beállításokat**, amelyek meghatározzák, hogyan kerül a 3‑D modell PDF-re renderelésre. Állíthatja az oldalméretet, engedélyezheti az automatikus layout méretezést, beállíthat háttérszínt, és kiválaszthatja a pontos layoutokat (nézeteket), amelyeket exportálni szeretne.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## 4. lépés: Raster kép mentése

Végül exportálja a DGN-t PDF fájlba a most beállított opciók használatával.

```csharp
dgnImage.Save(outFile, options);
```

## Gyakori problémák és megoldások

| Probléma | Megoldás |
|----------|----------|
| **Üres PDF kimenet** | Ellenőrizze, hogy a `Layouts` tömb a DGN fájlban lévő helyes nézetazonosítókat tartalmazza. |
| **Helytelen színek** | Győződjön meg róla, hogy a `BackgroundColor` a kívánt értékre van állítva; használja a `Color.White`-t a világos háttérhez. |
| **Teljesítménybottleneck nagy fájlok esetén** | Engedélyezze a `AutomaticLayoutsScaling`-et, és fontolja meg a `PageWidth/PageHeight` csökkentését a kisebb raster felbontás érdekében. |
| **Licenc kivétel** | Telepítsen érvényes Aspose.CAD licencet a kép betöltése előtt, hogy elkerülje a próba vízjelek megjelenését. |

## Gyakran Ismételt Kérdések

**Q: Használhatom az Aspose.CAD for .NET-et más CAD fájlformátumokkal?**  
A: Igen, az Aspose.CAD támogatja a DWG, DXF, DWF, DGN és még sok más formátumot.

**Q: Hogyan kezelhetem a kivételeket az Aspose.CAD használata közben?**  
A: Tegye a kódját egy `try‑catch` blokkba, és vizsgálja meg az `Aspose.CAD.CADException`-t a részletes hibainformációkért.

**Q: Alkalmas-e az Aspose.CAD kereskedelmi projektekhez?**  
A: Természetesen. Licencet vásárolhat [itt](https://purchase.aspose.com/buy).

**Q: Próbálhatom-e az Aspose.CAD for .NET-et vásárlás előtt?**  
A: Igen, ingyenes próba elérhető [itt](https://releases.aspose.com/).

**Q: Hol találok közösségi támogatást az Aspose.CAD-hez?**  
A: Csatlakozzon a megbeszélő fórumhoz [itt](https://forum.aspose.com/c/cad/19).

---

**Utolsó frissítés:** 2026-03-29  
**Tesztelve:** Aspose.CAD 24.11 for .NET  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}