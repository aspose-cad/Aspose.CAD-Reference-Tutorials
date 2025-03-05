---
title: DGN exportálása raszterképbe az Aspose.CAD for .NET-ben
linktitle: DGN exportálása raszterképbe
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Könnyedén konvertálja a DGN-t raszterképekké az Aspose.CAD for .NET segítségével. Fedezze fel a lépésenkénti útmutatót, és engedje szabadjára a .NET erejét a CAD-fájlok kezelésében.
type: docs
weight: 13
url: /hu/net/cad-export-formats/export-dgn-to-raster-image/
---
## Bevezetés

A .NET fejlesztés dinamikus birodalmában az Aspose.CAD hatékony eszközként jelenik meg a számítógéppel segített tervezési (CAD) fájlok kezelésében. Ez az oktatóanyag a DGN-fájlok raszterképekké történő exportálásának folyamatát mutatja be az Aspose.CAD for .NET használatával. Ha szeretné DGN-fájljait zökkenőmentesen látványos raszterképekké alakítani, akkor jó helyen jár.

## Előfeltételek

Mielőtt nekivágnánk ennek az útnak, győződjön meg arról, hogy a következő előfeltételeket teljesíti:

-  Aspose.CAD for .NET: Győződjön meg arról, hogy az Aspose.CAD könyvtár telepítve van a .NET projektben. A könyvtárat és a vonatkozó dokumentációkat megtalálja a[weboldal](https://reference.aspose.com/cad/net/).

- Minta DGN-fájl: Készítsen DGN-fájlt a konvertálásra. Példánkban a „Nikon_D90_Camera.dgn” fájlt használjuk.

Most merüljünk el a lépésről lépésre szóló útmutatóban.

## Névterek importálása

.NET-projektben kezdje az Aspose.CAD szükséges névtereinek importálásával. Ezzel a lépéssel hozzáférhet a DGN-ből raszteres képpé konvertáláshoz szükséges osztályokhoz és metódusokhoz.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1. lépés: Töltse be a DGN fájlt

 Kezdje azzal, hogy betölti a DGN fájlt a`CadImage` tárgy. Ez alapot ad a későbbi műveletekhez.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // A további feldolgozáshoz szükséges kód itt található
}
```

## 2. lépés: Adja meg a raszterezési beállításokat

 Hozzon létre egy`CadRasterizationOptions` objektumot, és állítson be különféle tulajdonságokat a raszterezési folyamat igényeinek megfelelő testreszabásához.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 3. lépés: JpegOptions objektum létrehozása

 Mivel a DGN fájlt JPEG formátumba szeretnénk konvertálni, hozzon létre a`JpegOptions` objektumot, és rendelje hozzá a korábban definiált`CadRasterizationOptions` hozzá.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## 4. lépés: Mentse el a raszterképet

 Használja ki a`Save` módszere a`CadImage` osztályt, hogy a DGN-fájlt raszteres képpé exportálja a kívánt formátumban, jelen esetben JPEG-ben.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Következtetés

Gratulálunk! Sikeresen végighaladt a DGN-fájl raszterképbe történő exportálásának lépésein az Aspose.CAD for .NET használatával. Ez az oktatóanyag felvértezte az alapvető ismereteket, amelyek segítségével könnyedén integrálhatja ezt a funkciót .NET-projektjeibe.

## GYIK

### 1. kérdés: Exportálhatok DGN fájlokat JPEG-től eltérő formátumba?

1. válasz: Igen, az Aspose.CAD for .NET különféle kimeneti formátumokat támogat. A beállításokat ennek megfelelően módosíthatja a 3. lépésben.

### Q2 Hogyan kezelhetem a kivételeket az átalakítási folyamat során?

2. válasz: Győződjön meg arról, hogy megfelelő kivételkezeléssel rendelkezik, amint az a mellékelt kódban is látható, a lehetséges problémák megoldása érdekében.

### 3. kérdés: Elérhető az Aspose.CAD .NET-hez próbaverziója?

 3. válasz: Igen, felfedezheti a terméket egy ingyenes próbaverzióval. Látogatás[itt](https://releases.aspose.com/) további információért.

### 4. kérdés: Hol kérhetek segítséget vagy vitathatom meg az Aspose.CAD for .NET-hez kapcsolódó problémákat?

 A4: Menjen át a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) közösségi támogatásra és beszélgetésekre.

### 5. kérdés: Hogyan szerezhetek ideiglenes licencet az Aspose.CAD for .NET számára?

 A5: Látogassa meg[ez a link](https://purchase.aspose.com/temporary-license/)hogy ideiglenes licencet szerezzen fejlesztési igényeihez.