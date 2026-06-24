---
date: 2026-04-06
description: Tanulja meg, hogyan konvertálja a DWG-t PDF-re, és adjon hozzá egyedi
  szöveget C# és Aspose.CAD használatával. Ez a lépésről‑lépésre útmutató lefedi a
  PDF generálását DWG‑ből, egy szövegegység beszúrását, valamint a DWG szöveg betűtípusának
  módosítását.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Szöveg hozzáadása DWG fájlokhoz C#‑ban
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG konvertálása PDF-be és szöveg hozzáadása C#-ban – Aspose.CAD útmutató
url: /hu/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG konvertálása PDF‑re és szöveg hozzáadása C#‑ban – Aspose.CAD bemutató

## Bevezetés

A CAD és .NET fejlesztés gyorsan változó világában a **DWG PDF‑re konvertálása** egyedi megjegyzések beillesztése közben gyakori követelmény. Akár nyomtatható rajzokat kell generálnia ügyfelei számára, akár dinamikus megjegyzéseket szeretne közvetlenül egy DWG‑be ágyazni, az Aspose.CAD egyszerűvé teszi a feladatot. Ebben a bemutatóban megtanulja, hogyan **konvertálja a DWG‑t PDF‑re**, **adjon hozzá szöveg‑elemet**, és akár **módosítsa a DWG szöveg betűtípusát** C#‑ban.

## Gyors válaszok
- **Melyik könyvtár a legjobb a DWG‑PDF konvertáláshoz?** Aspose.CAD for .NET  
- **Hozzáadhatok egyedi szöveget a konvertálás során?** Igen – hozzon létre egy `CadText` entitást, és adja hozzá a mentés előtt.  
- **Szükségem van licencre a termeléshez?** Kereskedelmi licenc szükséges; ingyenes próbaverzió elérhető.  
- **Mely .NET verziók támogatottak?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Lehetőség van a szöveg betűtípusának módosítására?** Igen, állítsa be a `CadText` tulajdonságait, például a `StyleType` és a `TextHeight` értékeket.

## Mi az a „DWG PDF‑re konvertálás”?

A DWG fájl PDF‑re konvertálása egy vektoralapú CAD rajzot alakít át széles körben megosztható, eszközfüggetlen dokumentummá. A PDF megőrzi az eredeti geometriát és rétegeket, miközben lehetővé teszi megjegyzések, szöveg vagy egyéb metaadatok beágyazását. Az Aspose.CAD automatikusan kezeli a rasterizálást és a vektoros megjelenítést, így a szerveren nem szükséges semmilyen harmadik fél CAD szoftvere.

## Miért érdemes szöveget hozzáadni a DWG‑hez a konvertálás előtt?

A szöveg közvetlen beágyazása a DWG‑be teljes kontrollt biztosít a elhelyezés, a stílus és a réteg hozzárendelése felett. Amikor a fájlt később PDF‑re konvertálják, a szöveg pontosan ott jelenik meg, ahol elhelyezte, megőrizve a tervezési szándékot és kiküszöbölve a PDF‑szerkesztőben történő utófeldolgozás szükségességét.

## Előfeltételek

- **Aspose.CAD Library** – töltse le a [download link](https://releases.aspose.com/cad/net/) címről.  
- **Működő .NET környezet** (Visual Studio 2022, .NET 6 vagy bármely kompatibilis verzió).  
- **Mappa a tesztfájlokhoz** – a továbbiakban `MyDir`‑ként hivatkozunk rá.

Most lépésről lépésre végigvezetjük a folyamatot.

## Névterek importálása

Add a required `using` statements so you can access Aspose.CAD classes.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## 1. lépés: DWG fájl betöltése

Töltse be a forrás DWG fájlt egy `Image` objektumba. Ez az objektum hozzáférést biztosít a mögöttes CAD entitásokhoz.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## 2. lépés: CadText objektum létrehozása (szöveg‑entitás beszúrása)

A `CadText` osztály egy DWG‑ben lévő egyetlen szövegsort képvisel. Itt állítjuk be a stílusát, értékét, színét, rétegét és pozícióját. A `StyleType` vagy a `TextHeight` módosításával **módosíthatja a DWG szöveg betűtípusát**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## 3. lépés: Szöveg‑entitás hozzáadása a Model Space‑hez

A DWG model space a legtöbb rajz‑entitást tartalmazza. A `CadText` hozzáadásával a `*Model_Space` blokkhoz a szöveg a rajz részévé válik.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## 4. lépés: PDF beállítások konfigurálása (PDF generálása DWG‑ből)

Állítsa be a rasterizálási opciókat, amelyek szabályozzák, hogyan kerül a DWG PDF‑be renderelésre. Módosíthatja az oldal méretét, a rajzolási típust és az elrendezést.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 5. lépés: Módosított DWG mentése PDF‑ként

Végül exportálja a módosított rajzot. Az eredményül kapott PDF tartalmazza az újonnan beszúrt szöveget.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Pro tipp:** Ha nagyobb felbontású PDF‑re van szüksége, növelje arányosan a `PageHeight` és `PageWidth` értékeket.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| A szöveg nem jelenik meg a PDF‑ben | Helytelen réteg vagy színazonosító | Győződjön meg arról, hogy a `LayerName` létezik, és a `ColorId` látható színre van állítva (pl. 7 a fehérhez). |
| A szöveg rossz helyen van | Helytelen igazítási koordináták | Ellenőrizze a `FirstAlignment.X/Y` értékeket a rajz egységeihez képest. |
| A PDF üres | A rasterizálási opciók nincsenek beállítva | Állítsa a `DrawType`‑t `UseObjectColor` vagy `UseObjectLineWeight` értékre. |

## Gyakran ismételt kérdések (létező)

### Q1: Az Aspose.CAD kompatibilis a DWG fájlok minden verziójával?

A1: Az Aspose.CAD széles körű DWG fájlverziót támogat, biztosítva a kompatibilitást különböző CAD szoftverekkel.

### Q2: Hozzáadhatok több szöveg‑entitást egyetlen DWG fájlhoz az Aspose.CAD használatával?

A2: Igen, a bemutatóban leírt folyamat ismétlésével több szöveg‑entitást is hozzáadhat egy DWG fájlhoz.

### Q3: Hogyan változtathatom meg a szöveg betűtípusát és stílusát az Aspose.CAD‑ben?

A3: A szöveg betűtípusának és stílusának módosításához állítsa be a `CadText` objektum tulajdonságait, mielőtt hozzáadná a DWG fájlhoz.

### Q4: Vannak licencelési szempontok az Aspose.CAD kereskedelmi projektben való használatához?

A5: Igen, tartsa be az Aspose.CAD licencfeltételeit. Részletekért tekintse meg a [Aspose.CAD Purchase](https://purchase.aspose.com/buy) oldalt.

### Q5: Hol kérhetek segítséget vagy vitathatom meg az Aspose.CAD‑hez kapcsolódó kérdéseket?

A5: Látogassa meg az [Aspose.CAD fórumot](https://forum.aspose.com/c/cad/19), hogy kapcsolatba léphessen a közösséggel és támogatást kapjon.

## További GYIK

**K: Hogyan generálok PDF‑t DWG‑ből szöveg hozzáadása nélkül?**  
A: Hagyja ki a `CadText` létrehozási lépést, és közvetlenül konfigurálja a `PdfOptions`‑t, mielőtt meghívná az `image.Save(...)`‑t.

**K: Programozottan megváltoztathatom a szöveg színét?**  
A: Igen, állítsa be a `cadText.ColorId`‑t egy konkrét ACI színszámra (pl. 1 a piroshoz).

**K: Lehetséges több soros szöveget beszúrni?**  
A: Használja a `CadMText`‑et több soros szövegtömbökhez; a megközelítés hasonló a `CadText`‑hez.

**K: Az Aspose.CAD támogatja a több DWG fájl kötegelt konvertálását?**  
A: Teljes mértékben – iteráljon egy DWG fájlok könyvtárán, alkalmazza ugyanazokat a lépéseket, és mentse mindegyiket PDF‑ként.

## Következtetés

Most már rendelkezik egy teljes, termelésre kész munkafolyammal, amely **DWG PDF‑re konvertál**, **egyedi szöveget ad hozzá**, és **testreszabja a szöveg megjelenését** C# és Aspose.CAD használatával. Ez a technika ideális automatizált rajzgeneráláshoz, jelentéskészítő folyamatokhoz, vagy bármilyen olyan helyzethez, ahol valós időben kell gazdagítani a CAD fájlokat.

---

**Utoljára frissítve:** 2026-04-06  
**Tesztelve:** Aspose.CAD 24.11 for .NET  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}