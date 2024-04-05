---
title: Konvertálja az elrendezéseket raszteres képpé az Aspose.CAD for .NET-ben
linktitle: Konvertálja az elrendezéseket raszteres képpé
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Könnyedén konvertálja a CAD-elrendezéseket raszterképekké az Aspose.CAD for .NET segítségével. Fokozza fejlesztését hatékony CAD-manipulációs képességekkel.
type: docs
weight: 12
url: /hu/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---
## Bevezetés

Könnyedén szeretné átalakítani az elrendezéseket raszterképekké .NET-alkalmazásaiban? Ne keressen tovább! Ez a részletes útmutató végigvezeti a folyamaton az Aspose.CAD for .NET használatával, amely egy hatékony könyvtár, amely leegyszerűsíti a számítógéppel segített tervezési (CAD) feladatokat.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

- Aspose.CAD for .NET Library: Töltse le és telepítse a könyvtárat a[Aspose.CAD for .NET letöltési oldal](https://releases.aspose.com/cad/net/).

- Fejlesztői környezet: Győződjön meg arról, hogy működő .NET fejlesztői környezet van beállítva a gépen.

- Konvertálandó dokumentum: Készítsen egy CAD-dokumentumot, amely tartalmazza a raszteres képekké konvertálni kívánt elrendezéseket.

- Az Ön dokumentumkönyvtára: Cserélje le a „Saját dokumentumkönyvtár” helyőrzőt a kódban a dokumentumkönyvtár elérési útjával.

## Névterek importálása

Először is importáljuk a szükséges névtereket, hogy elérhetővé tegyük az Aspose.CAD funkciókat a kódban.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1. lépés: Töltse be a CAD-dokumentumot

Kezdje a CAD-dokumentum betöltésével az Aspose.CAD könyvtár használatával.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    // további lépések kódja ide kerül
}
```

## 2. lépés: Konfigurálja a raszterezési beállításokat

 Hozzon létre egy példányt a`CadRasterizationOptions` az oldal szélességének és magasságának beállításához, valamint a konvertálni kívánt elrendezések megadásához.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## 3. lépés: A TiffOptions beállítása az eredményül kapott képhez

 Hozzon létre egy példányt a`TiffOptions`az eredményül kapott kép formátumának meghatározásához.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## 4. lépés: Mentse el a kapott képet

Adja meg a kimeneti útvonalat, és mentse a konvertált képet.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Következtetés

Gratulálunk! Sikeresen konvertálta a CAD-elrendezéseket raszteres képformátumba az Aspose.CAD for .NET használatával. A lehetőségek hatalmasak, és ez az útmutató kiindulópontként szolgál a CAD-vel kapcsolatos törekvéseihez.

## GYIK

### 1. kérdés: Az Aspose.CAD kompatibilis az összes CAD formátummal?

 1. válasz: Az Aspose.CAD a CAD formátumok széles skáláját támogatja, beleértve a DWG-t, DXF-et, DWF-et, STL-t és még sok mást. Ellenőrizd a[dokumentáció](https://reference.aspose.com/cad/net/) átfogó listáért.

### 2. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.CAD számára?

 A2: Látogassa meg a[ideiglenes licenc oldal](https://purchase.aspose.com/temporary-license/) tesztelési és értékelési célú ideiglenes engedély megszerzésére.

### 3. kérdés: Hol találok támogatást az Aspose.CAD számára?

 3. válasz: A fórumok remek hely a segítség kérésére. Meglátogatni a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) kapcsolatba lépni a közösséggel és segítséget kapni.

### 4. kérdés: Kipróbálhatom ingyenesen az Aspose.CAD-et?

 A4: Abszolút! Fogd meg[ingyenes próbaverzió](https://releases.aspose.com/) hogy feltárja az Aspose.CAD szolgáltatásait és képességeit.

### 5. kérdés: Hol vásárolhatok licencet az Aspose.CAD-hez?

 A5: Navigáljon a[vásárlási oldal](https://purchase.aspose.com/buy) licencet vásárolni és az Aspose.CAD teljes potenciálját kiaknázni.