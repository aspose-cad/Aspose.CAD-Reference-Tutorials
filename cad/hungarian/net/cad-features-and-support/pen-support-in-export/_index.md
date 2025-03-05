---
title: Növelje a CAD-exportálást egyéni tollbeállításokkal az Aspose.CAD for .NET-ben
linktitle: Toll támogatás az exportálásban
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Ismerje meg, hogyan javíthatja a CAD-képek exportálását az Aspose.CAD for .NET használatával. Testreszabhatja a tollbeállításokat a lenyűgöző látványokhoz PDF, PNG, BMP és sok más formátumban.
type: docs
weight: 12
url: /hu/net/cad-features-and-support/pen-support-in-export/
---
## Bevezetés

Az Aspose.CAD for .NET hatékony eszközkészletet biztosít a számítógéppel segített tervezési (CAD) fájlokkal való munkavégzéshez, lehetővé téve a fejlesztők számára a CAD-képek zökkenőmentes kezelését és exportálását. Az egyik figyelemre méltó funkció a toll támogatása az exportálás során, amely lehetővé teszi a felhasználók számára, hogy testreszabják a tollak kezdő- és végzáró beállításait, amikor CAD-képeket exportálnak különféle formátumokba, például PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF és WMF.

Ebben az oktatóanyagban az Aspose.CAD for .NET segítségével történő exportálás során a toll támogatásának sajátosságaiba fogunk beleásni. Lebontjuk az egyes lépéseket, világos magyarázatokkal és példákkal, amelyek végigvezetik Önt a folyamaton.

## Előfeltételek

Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

- Az Aspose.CAD for .NET telepítve van a fejlesztői környezetében. Letöltheti a[kiadási oldal](https://releases.aspose.com/cad/net/).

- A CAD fájlformátumok alapvető ismerete, különösen a DXF (Drawing Exchange Format).

- C# programozási nyelv gyakorlati ismerete.

## Névterek importálása

A kezdéshez feltétlenül importálja a szükséges névtereket a C# projektbe:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## 1. lépés: Állítsa be a dokumentumkönyvtárat

Határozza meg a könyvtárat, ahol a CAD-dokumentum található:

```csharp
string MyDir = "Your Document Directory";
```

## 2. lépés: Töltse be a CAD-képet

Töltse be a CAD-képet az Aspose.CAD segítségével:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## 3. lépés: Konfigurálja a raszterezési beállításokat

Hozzon létre raszterezési és PDF-beállításokat az exportálási folyamat testreszabásához:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## 4. lépés: A tollbeállítások testreszabása

Állítsa be a tollak kezdő- és végsapkáját:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## 5. lépés: Alkalmazza a vektorraszterezési beállításokat

Alkalmazza a raszterezési beállításokat a PDF-beállításokra:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 6. lépés: Mentse el az exportált PDF-fájlt

Mentse el a CAD-képet a testreszabott tollbeállításokkal PDF-fájlként:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## Következtetés

Ebben az oktatóanyagban megvizsgáltuk az Aspose.CAD for .NET exportálási funkciójának tolltámogatását. A lépésenkénti útmutató követésével könnyedén testreszabhatja a tollak kezdő- és végsapkájának beállításait, növelve ezzel a CAD-képek exportálásának rugalmasságát.

Nyugodtan kísérletezzen a különböző tollbeállításokkal, hogy elérje a kívánt vizuális effektusokat az exportált képeken.

## GYIK

### 1. kérdés: Használhatom ezeket a tollbeállításokat a PDF-en kívül más képformátumokhoz is?

1. válasz: Igen, a tollbeállítások különféle képformátumokhoz alkalmazhatók, például PNG, BMP, GIF, JPEG stb.

### 2. kérdés: Hol találok további dokumentációt az Aspose.CAD for .NET-hez?

 A2: Lásd a[dokumentáció](https://reference.aspose.com/cad/net/) átfogó információkért és példákért.

### 3. kérdés: Elérhető ingyenes próbaverzió az Aspose.CAD for .NET számára?

 3. válasz: Igen, hozzáférhet az ingyenes próbaverzióhoz[itt](https://releases.aspose.com/).

### 4. kérdés: Hogyan szerezhetek ideiglenes licenceket az Aspose.CAD for .NET számára?

 A4: Látogassa meg a[ideiglenes licenc oldal](https://purchase.aspose.com/temporary-license/) az ideiglenes engedélyezési lehetőségekért.

### 5. kérdés: Hol kérhetek közösségi támogatást az Aspose.CAD for .NET-hez?

 V5: Vegyen részt a közösséggel a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19).