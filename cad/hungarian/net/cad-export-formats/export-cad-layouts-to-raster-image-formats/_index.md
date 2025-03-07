---
title: CAD-elrendezések exportálása raszteres képformátumokba az Aspose.CAD for .NET-ben
linktitle: CAD-elrendezések exportálása raszteres képformátumokba
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Ismerje meg, hogyan exportálhat CAD-elrendezéseket raszterképekké az Aspose.CAD for .NET segítségével. Kövesse lépésenkénti útmutatónkat a zökkenőmentes átalakítás érdekében.
weight: 10
url: /hu/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD-elrendezések exportálása raszteres képformátumokba az Aspose.CAD for .NET-ben

## Bevezetés

Hatékonyan szeretné konvertálni a CAD-elrendezéseket raszteres képformátumokká az Aspose.CAD for .NET segítségével? Ez a lépésenkénti útmutató végigvezeti a folyamaton, részletes utasításokat és kódrészleteket biztosít a feladat zökkenőmentessé tételéhez. Akár tapasztalt fejlesztő, akár újonc az Aspose.CAD-ben, ez az oktatóanyag a szakértelem minden szintjét kielégíti.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy rendelkezik az alábbiakkal:

- Aspose.CAD for .NET Library: Győződjön meg arról, hogy telepítve van az Aspose.CAD könyvtár. Ha nem, akkor letöltheti a[Aspose.CAD weboldal](https://releases.aspose.com/cad/net/).

- CAD rajzfájl: Készítsen elő egy CAD rajzfájlt (pl. conic_pyramid.dxf), amelyet raszteres képformátumokká szeretne konvertálni.

## Névterek importálása

A .NET-projektben importálja a szükséges névtereket az Aspose.CAD funkciók kihasználásához. A kód elejére írja be a következő névtereket:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1. lépés: Töltse be a CAD-rajzot

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Töltsön be egy CAD-rajzot az Image példányába
using (var image = Image.Load(sourceFilePath))
{
    // Ide kerül a CAD-rajz betöltéséhez szükséges kód
}
```

## 2. lépés: A CadRasterizationOptions létrehozása

```csharp
// Hozzon létre egy CadRasterizationOptions példányt
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## 3. lépés: Adja meg a rétegeket

```csharp
// Adja hozzá a réteg nevét a CadRasterizationOptions fólialistájához
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## 4. lépés: JpegOptions létrehozása

```csharp
// Hozzon létre egy JpegOptions példányt (vagy bármilyen ImageOption raszteres formátum esetén)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## 5. lépés: Exportálás Jpeg formátumba

```csharp
// Exportáljon minden réteget Jpeg formátumba
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## További lépés: Konvertálja az összes réteget

Ha az összes réteget konvertálni szeretné, használja a következő módszert:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Ez a módszer a CAD-rajz összes fóliáján ismétlődik, és minden réteget külön Jpeg fájlba exportál.

## Következtetés

Gratulálunk! Sikeresen megtanulta, hogyan exportálhat CAD-elrendezéseket raszteres képformátumokba az Aspose.CAD for .NET segítségével. Ez az oktatóanyag átfogó útmutatót nyújt azoknak a fejlesztőknek, akik hatékony és megbízható megoldásokat keresnek a CAD-konverzióhoz.

## GYIK

### 1. kérdés: Használhatok más képformátumokat az exportáláshoz?

 A1: Igen, megteheti. Egyszerűen cserélje ki`JpegOptions` a kívánt formátum opcióival, mint pl`PngOptions` vagy`BmpOptions`.

### 2. kérdés: Elérhető próbaverzió?

 2. válasz: Igen, felfedezheti az Aspose.CAD funkcióit a próbaverzió letöltésével[itt](https://releases.aspose.com/).

### 3. kérdés: Hogyan kaphatok támogatást az Aspose.CAD-hez?

 3. válasz: Látogassa meg az Aspose.CAD-t[fórum](https://forum.aspose.com/c/cad/19) közösségi támogatásért, vagy fontolja meg a dedikált támogatás licencének vásárlását.

### 4. kérdés: Rendelkezésre állnak ideiglenes licencek?

 V4: Igen, ideiglenes engedélyt kaphat[itt](https://purchase.aspose.com/temporary-license/).

### 5. kérdés: Hol találom a dokumentációt?

 V5: Lásd a részletes dokumentációt[itt](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
