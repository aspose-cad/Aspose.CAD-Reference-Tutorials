---
title: Vízjelek hozzáadása CAD-rajzokhoz – Aspose.CAD útmutató
linktitle: Vízjelek hozzáadása CAD-rajzokhoz
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Fejlessze CAD-rajzait professzionális vízjelekkel az Aspose.CAD for .NET segítségével. Kövesse lépésről lépésre szóló útmutatónkat a személyre szabott és megnyerő tervekhez.
type: docs
weight: 11
url: /hu/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## Bevezetés

Professzionális vízjelek hozzáadásával javítani szeretné CAD-rajzait? Az Aspose.CAD for .NET robusztus megoldást kínál a vízjelek zökkenőmentes integrálására a CAD-fájlokba. Ebben a lépésenkénti útmutatóban végigvezetjük a vízjelek Aspose.CAD használatával történő hozzáadásának folyamatán, így biztosítva, hogy rajzai ne csak kritikus információkat közvetítsenek, hanem az Ön egyedi jelét is hordozzák.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy rendelkezik az alábbiakkal:
-  Aspose.CAD for .NET: Győződjön meg arról, hogy telepítve van az Aspose.CAD könyvtár. Letöltheti[itt](https://releases.aspose.com/cad/net/).
- Dokumentumkönyvtár: Hozzon létre egy könyvtárat a CAD-rajzok tárolására.
Most kezdjük el a vízjelek hozzáadásával a CAD-rajzokhoz!

## Névterek importálása

Kezdje azzal, hogy importálja a szükséges névtereket .NET-projektjébe:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 1. lépés: Töltse be a CAD-rajzot

```csharp
// A dokumentumok könyvtárának elérési útja.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## 2. lépés: Adjon hozzá vízjelet MTEXT-ként

```csharp
// Új MTEXT hozzáadása
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## 3. lépés: Vagy adjon hozzá vízjelet szövegként

```csharp
// Alternatív megoldásként adjon hozzá egy egyszerűbb entitást, például a szöveget
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## 4. lépés: Exportálás PDF-be

```csharp
// Exportálja a vízjellel ellátott CAD-rajzot PDF-be
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Ismételje meg ezeket a lépéseket a különböző rajzokhoz, és pillanatok alatt professzionális megjelenésű vízjeles CAD-fájlokat kaphat!

## Következtetés

Gratulálunk! Sikeresen megtanulta, hogyan adhat vízjeleket CAD-rajzaihoz az Aspose.CAD for .NET segítségével. Ez az egyszerű, de hatékony folyamat lehetővé teszi, hogy személyre szabja a terveit, miközben megőrzi műszaki rajzai integritását.

## GYIK

### 1. kérdés: Testreszabhatom a vízjel megjelenését?

V1: Igen, testreszabhatja a vízjel szövegét, betűtípusát, méretét és helyzetét saját igényei szerint.

### 2. kérdés: Az Aspose.CAD kompatibilis a különböző CAD fájlformátumokkal?

2. válasz: Az Aspose.CAD számos CAD fájlformátumot támogat, beleértve a DWG-t és a DXF-et is, biztosítva ezzel a széleskörű kompatibilitást.

### 3. kérdés: Hozzáadhatok több vízjelet egyetlen CAD-rajzhoz?

A3: Abszolút! Tetszőleges számú vízjelet adhat hozzá, rugalmasságot biztosítva a különböző használati esetekhez.

### 4. kérdés: Az Aspose.CAD kínál ingyenes próbaverziót?

4. válasz: Igen, felfedezheti az Aspose.CAD szolgáltatásait egy ingyenes próbaverzióval. Szerezd meg[itt](https://releases.aspose.com/).

### 5. kérdés: Hol találok támogatást az Aspose.CAD számára?

 5. válasz: Ha kérdése vagy segítsége van, keresse fel a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19).