---
title: A CAD-rajzméret beállítása az Aspose.CAD-ben .NET-hez
linktitle: A CAD rajz méretének beállítása
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Ismerje meg, hogyan állíthatja be könnyedén a CAD-rajzméreteket .NET-ben az Aspose.CAD használatával. Kövesse lépésenkénti útmutatónkat a zökkenőmentes átméretezéshez.
weight: 10
url: /hu/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# A CAD-rajzméret beállítása az Aspose.CAD-ben .NET-hez

## Bevezetés

Zökkenőmentesen szeretné beállítani a CAD-rajzok méretét .NET-alkalmazásaiban? Az Aspose.CAD for .NET robusztus megoldást kínál, amellyel könnyedén kezelheti a CAD-rajzok átméretezését. Ebben az oktatóanyagban végigvezetjük a folyamaton, lebontva az egyes lépéseket, hogy biztosan megértse a CAD-rajzok Aspose.CAD használatával történő átméretezésének bonyolultságát.

## Előfeltételek

Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

- Aspose.CAD for .NET Library: Töltse le és telepítse a könyvtárat a[Aspose.CAD for .NET letöltési oldal](https://releases.aspose.com/cad/net/).
- Minta CAD rajz: Győződjön meg róla, hogy van egy minta CAD rajzfájl (pl. "sample.dwg") a dokumentumkönyvtárában.

## Névterek importálása

Kezdje a szükséges névterek importálásával a .NET-alkalmazásba. Ez a lépés kulcsfontosságú az Aspose.CAD for .NET funkcióinak eléréséhez.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1. lépés: Töltse be a CAD-rajzot

Kezdje azzal, hogy betölti a CAD-rajzot az Aspose.CAD.Image osztály egy példányába. Győződjön meg arról, hogy a megfelelő fájl elérési útja van a mintarajzhoz.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Töltsön be egy CAD-rajzot az Image példányába
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Itt a kódod...
}
```

## 2. lépés: BmpOptions létrehozása

Hozzon létre egy példányt a BmpOptions osztályból, amely a CAD-rajz BMP-fájlként történő mentésekor a beállítások megadásáért felelős.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## 3. lépés: A CadRasterizationOptions beállítása

Példányosítsa a CadRasterizationOptions osztályt, és konfigurálja tulajdonságait a vektorraszterizáláshoz.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## 4. lépés: Állítsa be az UnitType tulajdonságot

Állítsa be a CadRasterizationOptions UnitType tulajdonságát az átméretezés mértékegységének megadásához. Ebben a példában centiméterre van állítva.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## 5. lépés: Állítsa be az elrendezések tulajdonságait

Adja meg az átméretezett rajzba felvenni kívánt elrendezéseket az Elrendezések tulajdonság beállításával.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 6. lépés: Exportálás BMP-be

Végül mentse az átméretezett elrendezést BMP-fájlként a Mentés módszerrel.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Sikeresen beállította CAD-rajzának méretét az Aspose.CAD for .NET segítségével!

## Következtetés

Ebben az oktatóanyagban végigjártuk a CAD-rajzok átméretezését .NET-ben az Aspose.CAD használatával. Ha követi ezeket a lépéseket, zökkenőmentesen integrálhatja ezt a funkciót alkalmazásaiba, zökkenőmentes felhasználói élményt biztosítva.

## GYIK

### 1. kérdés: Az Aspose.CAD for .NET kompatibilis az összes CAD formátummal?

 1. válasz: Az Aspose.CAD for .NET a CAD formátumok széles skáláját támogatja, beleértve a DWG-t, DXF-et, DWF-et stb. Ellenőrizd a[dokumentáció](https://reference.aspose.com/cad/net/) a teljes listához.

### 2. kérdés: Átméretezhetek több elrendezést egyszerre?

2. válasz: Igen, több elrendezést is átméretezhet az elrendezések tömbjének módosításával a CadRasterizationOptionsben.

### 3. kérdés: Hol kaphatok támogatást az Aspose.CAD for .NET-hez?

 A3: Látogassa meg a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) közösségi támogatásért és segítségért.

### 4. kérdés: Van ingyenes próbaverzió?

 A4: Igen, felfedezheti a[ingyenes próbaverzió](https://releases.aspose.com/) az Aspose.CAD for .NET szolgáltatásainak értékeléséhez.

### 5. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.CAD for .NET számára?

 5. válasz: Szerezzen be ideiglenes licencet tesztelési célokra[itt](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
