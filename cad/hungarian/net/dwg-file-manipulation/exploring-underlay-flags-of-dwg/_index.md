---
title: A DWG-fájlok alatti zászlóinak felfedezése – Aspose.CAD oktatóanyag
linktitle: A DWG fájlok alátétjelzőinek felfedezése
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Fedezze fel az Aspose.CAD for .NET erejét a DWG fájlok alátétjelzőinek felfedezésében. Kövesse lépésenkénti útmutatónkat.
weight: 13
url: /hu/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# A DWG-fájlok alatti zászlóinak felfedezése – Aspose.CAD oktatóanyag

## Bevezetés

Ha elmélyül a CAD-fájlok, különösen a DWG-fájlok bonyolult világában, és szeretné feltárni az alátétjelzők titkait, akkor jó helyen jár. Ez az oktatóanyag végigvezeti Önt a DWG-fájlok alatti jelzőtábláinak feltárásán a hatékony Aspose.CAD for .NET könyvtár használatával.

## Előfeltételek

Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy rendelkezik a következőkkel:

- Alapvető ismeretek a C# és .NET programozásról.
-  Aspose.CAD for .NET könyvtár telepítve. Ha nem, akkor letöltheti[itt](https://releases.aspose.com/cad/net/).
- Egy DWG fájl tesztelésre. Használhatja az oktatóanyagban található "BlockRefDgn.dwg" mintafájlt.

## Névterek importálása

A kezdéshez importálnia kell a szükséges névtereket. Íme egy részlet, amely segít:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## 1. lépés: Töltse be a DWG fájlt, és konvertálja CadImage formátumba

Kezdje azzal, hogy betölti a meglévő DWG fájlt, és konvertálja CadImage formátumba:

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Töltse be a DWG fájlt, és konvertálja CadImage formátumba
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // A következő lépések kódja ide kerül
}
```

## 2. lépés: Iterálás entitásokon keresztül

Ezután ismételje meg a DWG-fájlon belüli minden entitást:

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // A következő lépések kódja ide kerül
}
```

## 3. lépés: Ellenőrizze a CadDgnUnderlay típust

Ellenőrizze, hogy az entitás CadDgnUnderlay típusú-e:

```csharp
if (entity is CadDgnUnderlay)
{
    // A következő lépések kódja ide kerül
}
```

## 4. lépés: Hozzáférés az alátét zászlókhoz

Különböző alátétjelzők elérése és releváns információk kinyerése:

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

## Következtetés

Gratulálunk! Az Aspose.CAD for .NET segítségével sikeresen felfedezte a DWG-fájlok alátétjelzőit. Ez az oktatóanyag az entitások közötti navigáláshoz és az alátétekkel kapcsolatos fontos információk kinyeréséhez szükséges ismeretekkel ruházta fel.

## GYIK

### 1. kérdés: Használhatom az Aspose.CAD for .NET fájlt más CAD fájlformátumokkal?

1. válasz: Az Aspose.CAD különféle CAD-formátumokat támogat, beleértve a DWG-t, DXF-et, DGN-t stb. A teljes listát a dokumentációban találja.

### 2. kérdés: Rendelkezésre áll ideiglenes licenc az Aspose.CAD for .NET számára?

 V2: Igen, beszerezhet ideiglenes engedélyt[itt](https://purchase.aspose.com/temporary-license/).

### 3. kérdés: Hol találok támogatást az Aspose.CAD for .NET számára?

 3. válasz: Látogassa meg a támogatási fórumot[itt](https://forum.aspose.com/c/cad/19) segítségért.

### 4. kérdés: Hogyan vásárolhatok Aspose.CAD-et .NET-hez?

A4: Vásárolja meg a könyvtárat[itt](https://purchase.aspose.com/buy).

### 5. kérdés: Van ingyenes próbaverzió?

 5. válasz: Igen, hozzáférhet az ingyenes próbaverzióhoz[itt](https://releases.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
