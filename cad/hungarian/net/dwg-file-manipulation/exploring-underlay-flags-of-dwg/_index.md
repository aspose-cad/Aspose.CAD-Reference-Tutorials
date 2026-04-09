---
date: 2026-04-09
description: Tanulja meg, hogyan konvertálja a DWG-t képpé, és hogyan olvassa a háttérjelzőket
  az Aspose.CAD for .NET használatával ebben a lépésről‑lépésre útmutatóban.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: A DWG-fájlok alaprajz jelzőinek felfedezése
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG konvertálása képre – A DWG fájlok alaprajz jelzőinek feltárása – Aspose.CAD
  oktatóanyag
url: /hu/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG fájlok alávetett jelzőinek felfedezése – Aspose.CAD bemutató

## Bevezetés

Ha a CAD fájlok bonyolult világába merülsz, különösen a DWG fájlokba, és szeretnél **DWG-t képpé konvertálni**, miközben felfedezed a **alávetett jelzők** olvasását, jó helyen vagy. Ez a bemutató minden lépésen végigvezet a hatékony Aspose.CAD for .NET könyvtár segítségével, így magabiztosan kinyerheted az alávetett információkat, és a rajzot képként megjelenítheted.

## Gyors válaszok
- **Mi jelent a “convert DWG to image”?**  
  Ez azt jelenti, hogy egy DWG rajzot raszteres formátumba (PNG, JPEG stb.) renderelünk az Aspose.CAD használatával.
- **Melyik metódus tárja fel az alávetett jelzőket?**  
  A DWG betöltése után a `CadUnderlay` objektum `Flags` tulajdonságához férhetsz hozzá.
- **Szükségem van licencre az Aspose.CAD-hez?**  
  Ideiglenes licenc elérhető értékeléshez; a teljes licenc a termeléshez kötelező.
- **Mely .NET verziók támogatottak?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 és újabbak.
- **Kinyerhetem az alávetett geometriát?**  
  Igen – az alávetett útvonal, beillesztési pont, méretezés, forgatás és a jelzők állapota mind elérhető.

## Mi az a “convert DWG to image” és miért fontos?

Egy DWG fájl képpé konvertálása lehetővé teszi a CAD rajzok megjelenítését böngészőkben, beágyazását jelentésekbe, vagy megosztását olyan érintettekkel, akiknek nincs CAD megjelenítőjük. A renderelés során gyakran szükséges az **alávetett** objektumok (pl. DGN hivatkozások) ellenőrzése, hogy biztosan helyesen jelenjenek meg. Az alávetett jelzők megértése segít a vágás, a monokróm megjelenítés és a láthatósági problémák hibaelhárításában, még mielőtt a végső képet generálnád.

## Előfeltételek

- Alapvető C# és .NET programozási ismeretek.  
- **Aspose.CAD for .NET** könyvtár telepítve. Ha még nincs, töltsd le **[itt](https://releases.aspose.com/cad/net/)**.  
- Teszteléshez egy DWG fájl – a példafájl **„BlockRefDgn.dwg”** a teljes útmutató során használatos.

## Névterek importálása

A kezdéshez importáld a szükséges névtereket:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1. lépés: DWG fájl betöltése és konvertálása `CadImage`-re

Először töltsd be a DWG fájlt, és alakítsd `CadImage` típusra. Ez az objektum hozzáférést biztosít az összes rajzelemhez, beleértve az alávetetteket is.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## 2. lépés: Entitások bejárása

Ezután iterálj végig minden entitáson a rajzban. Itt fogod megtalálni az alávetett objektumokat.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## 3. lépés: `CadDgnUnderlay` típus ellenőrzése

Az alávetett entitásokat a futásidejű típusuk ellenőrzésével azonosíthatod. A `CadDgnUnderlay` osztály a DWG-be beágyazott DGN alávetetteket képviseli.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## 4. lépés: Alávetett jelzők elérése

Miután megszerezted a `CadDgnUnderlay`-t, castold `CadUnderlay`-ra, hogy elolvasd a tulajdonságait és a jelzők állapotát. A jelzők megmutatják, hogy az alávetett látható, vágott vagy monokróm módon renderelt-e.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### Mit mond a kimenet

- **UnderlayPath / UnderlayName** – ahol a külső DGN fájl található.  
- **InsertionPoint (X, Y)** – koordináták, ahol az alávetett a DWG térben elhelyezkedik.  
- **RotationAngle** – az alávetettre alkalmazott forgatás.  
- **ScaleX / ScaleY / ScaleZ** – az egyes tengelyek méretezési tényezői.  
- **Flags** – logikai értékek, amelyek a láthatóságot (`UnderlayIsOn`), a vágást (`ClippingIsOn`) és a monokróm renderelést (`Monochrome`) jelzik.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| Nincs kimenet a jelző ellenőrzéseknél | Az alávetett jelzők alapértelmezés szerint 0‑ra vannak állítva, ha az alávetett ki van kapcsolva. | Győződj meg róla, hogy a DWG valóban tartalmaz aktív alávetettet, vagy állítsd be a láthatóságot a forrás CAD fájlban. |
| `Invalid cast` kivétel | Az entitás nem `CadDgnUnderlay`. | Ellenőrizd a `if (entity is CadDgnUnderlay)` feltételt a castolás előtt. |
| Kép renderelése sikertelen a jelzők kinyerése után | Az alávetett lehet vágott vagy kikapcsolt, ami üres területet eredményez. | Állítsd be a jelzőket (`UnderlayIsOn = true`, `ClippingIsOn = false`) a végső kép renderelése előtt. |

## Gyakran ismételt kérdések

### Q1: Használhatom az Aspose.CAD for .NET-et más CAD fájlformátumokkal?

A1: Az Aspose.CAD számos CAD formátumot támogat, többek között DWG, DXF, DGN és továbbiakat. A teljes listáért tekintsd meg a dokumentációt.

### Q2: Elérhető ideiglenes licenc az Aspose.CAD for .NET-hez?

A2: Igen, ideiglenes licencet **[itt](https://purchase.aspose.com/temporary-license/)** szerezhetsz be.

### Q3: Hol találok támogatást az Aspose.CAD for .NET-hez?

A3: Látogasd meg a támogatási fórumot **[itt](https://forum.aspose.com/c/cad/19)** segítségért.

### Q4: Hogyan vásárolhatok Aspose.CAD for .NET-et?

A4: A könyvtárat **[itt](https://purchase.aspose.com/buy)** vásárolhatod meg.

### Q5: Van ingyenes próba?

A5: Igen, az ingyenes próbaverziót **[itt](https://releases.aspose.com/)** érheted el.

## Összegzés

Gratulálunk! Sikeresen megtanultad, **hogyan konvertálj DWG-t képpé**, miközben elsajátítottad **az alávetett jelzők** olvasását az Aspose.CAD for .NET segítségével. Ezzel a tudással:

- Renderelhetsz DWG rajzokat raszteres képekké webes vagy jelentési környezetben.  
- Ellenőrizheted és módosíthatod az alávetett tulajdonságait a helyes megjelenítés érdekében.  
- Hibakeresheted a láthatósági, vágási és monokróm problémákat a végső kép generálása előtt.

Fedezd fel az Aspose.CAD további funkcióit, például a rétegkezelést, szövegkinyerést és kötegelt konvertálást, hogy tovább bővítsd CAD automatizálási munkafolyamataidat.

---

**Legutóbb frissítve:** 2026-04-09  
**Tesztelve:** Aspose.CAD for .NET 24.11  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}