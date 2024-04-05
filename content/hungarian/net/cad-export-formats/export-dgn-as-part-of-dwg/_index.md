---
title: Exportálja a DGN-t a DWG részeként az Aspose.CAD-ben .NET-hez
linktitle: DGN exportálása a DWG részeként
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Ismerje meg, hogyan exportálhat DGN-t a DWG részeként az Aspose.CAD for .NET-ben. Kövesse lépésenkénti útmutatónkat a zökkenőmentes integráció érdekében.
type: docs
weight: 11
url: /hu/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## Bevezetés

.NET-fejlesztés világában az Aspose.CAD a számítógéppel segített tervezésű (CAD) fájlokkal való munkavégzés hatékony könyvtáraként tűnik ki. Ez az oktatóanyag végigvezeti Önt a DGN (Design) fájl DWG (rajz) fájl részeként történő exportálásán az Aspose.CAD for .NET használatával. Akár tapasztalt fejlesztő, akár csak most kezdi, ez a lépésről lépésre bemutató útmutató segít az Aspose.CAD képességeinek kihasználásában ennek a konkrét feladatnak a hatékony végrehajtásában.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételeket teljesítette:

-  Aspose.CAD for .NET: Győződjön meg arról, hogy telepítve van a .NET Aspose.CAD könyvtára. Letöltheti[itt](https://releases.aspose.com/cad/net/).

- Fejlesztési környezet: Állítsa be a kívánt .NET fejlesztői környezetet, például a Visual Studio-t.

- C# alapismeretek: Ismerkedjen meg a C# programozási nyelvvel.

## Névterek importálása

A C# projektben tartalmazza az Aspose.CAD funkció eléréséhez szükséges névtereket. Adja hozzá a következőket direktívák használatával a kódfájl elejéhez:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Most bontsuk fel a megadott kódot több lépésre:

## 1. lépés: Határozza meg a fájl elérési útját

```csharp
//Bemeneti és kimeneti fájl elérési útja
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## 2. lépés: PdfOptions példány létrehozása

```csharp
// Hozzon létre egy példányt a PdfOptions osztályból a DWG PDF-be exportálásához
PdfOptions exportOptions = new PdfOptions();
```

## 3. lépés: Töltse be a DWG fájlt

```csharp
// Töltse be a meglévő DWG fájlt képként, és alakítsa át CadImage típusra
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## 4. lépés: Iterálás entitásokon keresztül

```csharp
// Iteráljon végig a DWG-fájlon belüli egyes entitásokon
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## 5. lépés: Ellenőrizze az entitás típusát

```csharp
// Ellenőrizze, hogy az entitás képdefiníció-e
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## 6. lépés: Szerezze be az alátétútvonalat

```csharp
// Ha ez egy képdefiníció, szerezze be az objektum külső hivatkozását
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## 7. lépés: Adja meg a raszterezési beállításokat

```csharp
// Adja meg a CadRasterizationOptions objektum beállításait
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

## 8. lépés: DWG exportálása PDF-be

```csharp
// Exportálja a DWG-t PDF-be a Mentés metódus hívásával
cadImage.Save(outPath, exportOptions);
```

## Következtetés

Gratulálunk! Sikeresen végigment a DGN-fájl DWG-fájl részeként történő exportálásán az Aspose.CAD for .NET használatával. Ez az oktatóanyag megadja az alapvető lépéseket és kódrészleteket, amelyek segítségével zökkenőmentesen végrehajthatja ezt a konkrét feladatot.

## GYIK

### 1. kérdés: Használhatom az Aspose.CAD for .NET-et kereskedelmi projektjeimben?
 A1: Igen, megteheti. Látogatás[itt](https://purchase.aspose.com/buy) az engedélyezési lehetőségek feltárására.

### 2. kérdés: Vannak korlátozások a feldolgozható DWG-fájlok méretére vonatkozóan?
2. válasz: Az Aspose.CAD támogatja a nagy DWG-fájlok kezelését, de előfordulhatnak hardveres korlátozások.

### 3. kérdés: Elérhető próbaverzió?
V3: Igen, ingyenes próbaverziót kaphat[itt](https://releases.aspose.com/).

### 4. kérdés: Hogyan szerezhetek ideiglenes licenceket?
 A4: Ideiglenes engedélyek szerezhetők be[itt](https://purchase.aspose.com/temporary-license/).

### 5. kérdés: Hol kérhetek segítséget, ha problémákba ütközöm?
 5. válasz: Látogassa meg az Aspose.CAD fórumot[itt](https://forum.aspose.com/c/cad/19) támogatásért.