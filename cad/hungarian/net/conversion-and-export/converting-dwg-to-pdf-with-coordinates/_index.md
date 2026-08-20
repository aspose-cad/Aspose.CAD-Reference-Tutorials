---
date: 2026-04-03
description: Tanulja meg, hogyan állíthat be nézetablakot, és konvertálhatja a DWG-t
  PDF‑be C#‑ban az Aspose.CAD használatával. Ez a DWG‑PDF útmutató pontos exportálást
  mutat be koordinátákkal.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: DWG konvertálása PDF-re koordinátákkal C#‑ban
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hogyan állítsuk be a nézetablakot DWG PDF-re konvertálása közben koordinátákkal
  C#-ban – Aspose.CAD útmutató
url: /hu/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG konvertálása PDF-re koordinátákkal C#-ban – Aspose.CAD útmutató

## Bevezetés

Üdvözöljük ebben az átfogó útmutatóban, amely bemutatja, hogyan **állítsuk be a nézetablakot** a DWG fájlok PDF-re konvertálása során megadott koordinátákkal az Aspose.CAD for .NET használatával. A nézetablak vezérlésével pixel‑pontos PDF-eket kapunk, amelyek pontosan a szükséges területet fedik le – tökéletesek építészeti rajzokhoz, alaprajz‑előnézetekhez vagy bármely BIM munkafolyamathoz.

## Gyors válaszok
- **Mi jelent a “set viewport”?** A CAD rajz látható területét és méretezését határozza meg a raszterizálás során.  
- **Melyik könyvtár kezeli a konverziót?** Aspose.CAD for .NET.  
- **Szükségem van licencre?** Egy ingyenes próba verzió elegendő értékeléshez; a termeléshez kereskedelmi licenc szükséges.  
- **Támogatott platformok?** Windows, Linux és macOS .NET 5/6/7 vagy .NET Framework 4.6+ környezetekkel.  
- **Tipikus megvalósítási idő?** Körülbelül 10‑15 perc egy alap konverzióhoz.

## Előfeltételek

Mielőtt elkezdenénk, győződjön meg róla, hogy a következő előfeltételek rendelkezésre állnak:

- **Aspose.CAD Library** – Töltse le és telepítse az Aspose.CAD könyvtárat .NET-hez. A könyvtárat megtalálja [itt](https://releases.aspose.com/cad/net/).
- **Fejlesztői környezet** – Visual Studio, Rider vagy bármely .NET fejlesztést támogató IDE.
- **DWG fájl** – Legyen egy DWG fájl készen a konverzióhoz. Használhatja a mellékelt példafájlt vagy saját DWG fájlját.

## Hogyan állítsuk be a nézetablakot a pontos PDF exportáláshoz

A nézetablak beállítása a kulcsfontosságú lépés, amely lehetővé teszi a rajz pontos területének meghatározását, amelyet renderelni szeretne. Az alábbi kódban létrehozunk egy új `CadVportTableObject`‑ot, a bal‑felső koordinátával helyezzük el, és kiszámítjuk a szélességet, magasságot és az arányt. Ez a **hogyan állítsuk be a nézetablakot** megvalósítás vezérli a konverzió többi részét.

## Névterek importálása

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Törjük le a kódot lépésről‑lépésre a jobb megértés érdekében:

## 1. lépés: A dokumentum könyvtár meghatározása

```csharp
string MyDir = "Your Document Directory";
```

## 2. lépés: A forrás DWG fájl útvonalának beállítása

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## 3. lépés: DWG fájl betöltése és a raszterizálási beállítások konfigurálása

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## 4. lépés: Koordináták és nézetablak meghatározása  

Itt ténylegesen **beállítjuk a nézetablakot** (hogyan állítsuk be a nézetablakot) a bal‑felső sarok, a szélesség és a magasság megadásával, amely területet exportálni szeretnénk.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## 5. lépés: A nézetablak beállításainak alkalmazása

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## 6. lépés: PDF beállítások konfigurálása és exportálás  

Most mindent összekapcsolunk, és **DWG-t PDF-re konvertálunk** a most előkészített raszterizálási beállítások használatával.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## 7. lépés: Sikerüzenet megjelenítése

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Gyakori felhasználási esetek

- **Építési dokumentáció** – Nyomtatható PDF-ek generálása a specifikus alaprajz‑szakaszokról.  
- **BIM koordináció** – Csak az érdeklődési terület exportálása ütközés‑detektáláshoz.  
- **Ügyfélprezentációk** – Tiszta PDF biztosítása egy kiválasztott szobáról vagy emelésről anélkül, hogy az egész rajzot felfedné.

## Összegzés

Gratulálunk! Sikeresen **konvertáltad a DWG-t PDF-re** pontos koordinátákkal, és megtanultad, hogyan **állítsd be a nézetablakot** az Aspose.CAD for .NET használatával. Ez a **dwg to pdf tutorial** bemutatja, hogyan **hozz létre PDF-et DWG-ből** és **exportálj DWG-t PDF-ként C#-ban**, miközben teljes ellenőrzést gyakorolsz a kimeneti terület felett.

## GYIK

### Q1: Használhatom az Aspose.CAD-et más CAD fájlformátumokkal?

A1: Igen, az Aspose.CAD számos CAD formátumot támogat, többek között DWG, DXF, DWF és egyebeket.

### Q2: Hogyan kezelhetem a hibákat a konverziós folyamat során?

A2: Hibakezelő mechanizmusok bevezetése try‑catch blokkokkal a kivételek elkapásához és kezeléséhez.

### Q3: Az Aspose.CAD alkalmas Windows és Linux környezetekre egyaránt?

A3: Igen, az Aspose.CAD kompatibilis mind Windows, mind Linux platformokkal.

### Q4: Testreszabhatom a PDF kimenetet tovább?

A4: Természetesen! Fedezze fel az Aspose.CAD által kínált kiterjedt lehetőségeket a PDF kimenet testreszabásához az Ön specifikus igényei szerint.

### Q5: Hol találok további támogatást vagy közösségi megbeszéléseket?

A5: Látogassa meg az [Aspose.CAD Fórumot](https://forum.aspose.com/c/cad/19) a közösségi támogatás és megbeszélésekért.

## További gyakran ismételt kérdések

**K: Működik ez a megközelítés nagy DWG fájlokkal (százak MB)?**  
A: Igen. A raszterizálás oldalanként történik, és a `rasterizationOptions` (pl. `Resolution`) beállításával egyensúlyozhat a minőség és a memóriahasználat között.

**K: Exportálhatok több nézetablakot külön PDF oldalakon?**  
A: A `cadImage.ViewPorts` elemein ciklizálva, mindegyiket aktívvá teheti, majd minden oldalra meghívhatja a `Save`‑t, végül összevonhatja a PDF-eket az Aspose.PDF használatával.

**K: Lehetőség van vízjel hozzáadására a generált PDF-hez?**  
A: A PDF mentése után újra megnyithatja az Aspose.PDF‑vel, és szöveges vagy képes vízjelet alkalmazhat a felhasználó számára történő kézbesítés előtt.

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}