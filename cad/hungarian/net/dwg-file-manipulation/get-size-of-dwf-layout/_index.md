---
title: DWG-fájlok használata C#-ban – DWF-elrendezés méretének lekérése
linktitle: DWG-fájlok használata C#-ban – DWF-elrendezés méretének lekérése
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Fedezze fel az Aspose.CAD for .NET erejét a DWG-fájlok kezelésében. Tanulja meg a DWF-elrendezési méretek könnyed kibontását a C# használatával.
weight: 10
url: /hu/net/dwg-file-manipulation/get-size-of-dwf-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG-fájlok használata C#-ban – DWF-elrendezés méretének lekérése

## Bevezetés

A számítógéppel segített tervezés (CAD) és .NET-fejlesztés területén az Aspose.CAD hatékony eszköz a DWG-fájlok kezelésére. Ez az oktatóanyag végigvezeti Önt a DWG-fájlok C#-ban történő kezelésén és a DWF-elrendezés méretének kibontásán. Mielőtt belemerülnénk a kódba, győződjünk meg arról, hogy mindent beállítottunk ahhoz, hogy elinduljunk ezen az úton.

## Előfeltételek

Az oktatóanyag zökkenőmentes követéséhez győződjön meg arról, hogy a következő előfeltételeket teljesítette:

-  Aspose.CAD for .NET: Győződjön meg arról, hogy telepítve van az Aspose.CAD for .NET. Letöltheti a[Aspose.CAD for .NET letöltési oldal](https://releases.aspose.com/cad/net/).

Most, hogy megvannak a szükséges eszközök, ugorjunk a kódolási arénába.

## Névterek importálása

Mielőtt elkezdenénk dolgozni a kóddal, importáljuk a szükséges névtereket:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Ezek a névterek biztosítják az alapvető osztályokat és módszereket a CAD-fájlok Aspose.CAD-del történő kezeléséhez a C#-alkalmazásban.

## 1. lépés: Állítsa be környezetét

Kezdje azzal, hogy megbizonyosodjon arról, hogy a megfelelő környezet van beállítva a projekthez. Hivatkozzon az Aspose.CAD könyvtárra a C# projektben.

## 2. lépés: Határozza meg a fájl elérési útját

Határozza meg a DWG fájl elérési útját és a generált JPG fájlok kimeneti könyvtárát:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## 3. lépés: Töltse be a DWF-képet

Töltse be a DWF-képet az Aspose.CAD segítségével:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // A további lépések kódja itt található
}
```

## 4. lépés: Ismétlés oldalakon keresztül

Ismételje meg a DWF-kép oldalait:

```csharp
foreach (var page in image.Pages)
{
    // A további lépések kódja itt található
}
```

## 5. lépés: Szerezze be az elrendezési információkat

Szerezzen be elrendezési információkat az egyes oldalakról:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## 6. lépés: Állítsa be a JPG-beállításokat

Állítsa be az elrendezés JPG-fájlként való mentéséhez szükséges beállításokat:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // A további lépések kódja itt található
}
```

## 7. lépés: Határozza meg az oldalméretet

Határozza meg a DWF-elrendezés méretét:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// A további lépések kódja itt található
```

## 8. lépés: Állítsa be az oldalméreteket

Állítsa be az oldalméreteket az egység típusa alapján:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## 9. lépés: Mentse el a JPG fájlt

Mentse el a JPG fájlt a megadott beállításokkal:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Sikeresen kibontotta a DWF-elrendezés méretét a DWG-fájlból az Aspose.CAD segítségével C#-ban. Nyugodtan fedezze fel az Aspose.CAD által a .NET fejlesztéshez kínált további szolgáltatásokat és funkciókat.

## Következtetés

Ebben az oktatóanyagban végigjártuk a DWG-fájlok C# nyelven történő kezelésének folyamatát az Aspose.CAD használatával. Ha követi ezeket a lépéseket, akkor nem csak a DWF-elrendezés méretét érheti el, hanem az Aspose.CAD képességeit is kihasználhatja a .NET-projektek különböző CAD-vel kapcsolatos feladataihoz.

## GYIK

### 1. kérdés: Az Aspose.CAD kompatibilis a legújabb DWG fájlformátumokkal?

 1. válasz: Az Aspose.CAD különféle DWG fájlformátumokat támogat, beleértve a legújabb verziókat is. Utal[dokumentáció](https://reference.aspose.com/cad/net/) konkrét kompatibilitási részletekért.

### 2. kérdés: Használhatom az Aspose.CAD-et kereskedelmi és személyes projektekhez is?

 2. válasz: Igen, az Aspose.CAD rugalmas licencelési lehetőségeket kínál kereskedelmi és személyes használatra egyaránt. Meglátogatni a[vásárlási oldal](https://purchase.aspose.com/buy) további részletekért.

### 3. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.CAD számára?

 V3: Ideiglenes licencet szerezhet be[itt](https://purchase.aspose.com/temporary-license/) értékelési célokra.

### 4. kérdés: Hol találok támogatást az Aspose.CAD számára?

4. válasz: Ha kérdése vagy segítsége van, keresse fel a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19).

### 5. kérdés: Elérhető az Aspose.CAD ingyenes próbaverziója?

 5. válasz: Igen, hozzáférhet az Aspose.CAD ingyenes próbaverziójához[itt](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
