---
title: Szöveg hozzáadása DWG-fájlokhoz C#-ban - Aspose.CAD oktatóanyag
linktitle: Szöveg hozzáadása DWG-fájlokhoz C#-ban
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Ismerje meg, hogyan adhat hozzá szöveget DWG-fájlokhoz C# és Aspose.CAD használatával. Kövesse ezt a lépésenkénti oktatóanyagot a zökkenőmentes integráció érdekében. Fedezze fel az Aspose.CAD dokumentációt átfogó útmutatásért.
type: docs
weight: 14
url: /hu/net/dwg-file-manipulation/adding-text-to-dwg/
---
## Bevezetés

A számítógéppel segített tervezés (CAD) és .NET-fejlesztés dinamikus birodalmában az Aspose.CAD a DWG-fájlok kezelésének hatékony eszközeként tűnik ki. Szöveg hozzáadása a DWG-fájlokhoz gyakori követelmény, és ebben az oktatóanyagban megvizsgáljuk, hogyan érhetjük el ezt a C# és az Aspose.CAD használatával.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a helyén van a következők:

-  Aspose.CAD Library: Töltse le és telepítse az Aspose.CAD könyvtárat a[letöltési link](https://releases.aspose.com/cad/net/).

-  Dokumentumkönyvtár: Állítson be egy könyvtárat a dokumentumok számára, és jegyezze fel az elérési utat a következőként`MyDir`.

Most bontsuk le a folyamatot kezelhető lépésekre.

## Névterek importálása

A C# kódban adja meg az Aspose.CAD funkciók eléréséhez szükséges névtereket.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## 1. lépés: Töltse be a DWG fájlt

 Töltse be a DWG fájlt egy`Image` objektumot az Aspose.CAD könyvtár használatával.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // A következő lépésekhez tartozó kód itt található
}
```

## 2. lépés: Hozzon létre CadText objektumot

 Példányosítás a`CadText` objektumot a DWG-fájlhoz hozzáadni kívánt szöveg megjelenítéséhez.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;
cadText.ScaleX = 0.0;
```

## 3. lépés: Szöveg hozzáadása a DWG-hez

 Adja hozzá a létrehozottat`CadText` objektumot a DWG fájlhoz az Aspose.CAD használatával.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## 4. lépés: Konfigurálja a PDF-beállításokat

Konfigurálja a PDF-beállításokat a módosított DWG-fájl PDF-ként való mentéséhez.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 5. lépés: Mentés PDF-ként

Mentse el a módosított DWG-fájlt PDF-ként a hozzáadott szöveggel.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

Sikeresen hozzáadott szöveget egy DWG-fájlhoz a C# és az Aspose.CAD használatával. Nyugodtan fedezze fel az Aspose.CAD további szolgáltatásait és funkcióit CAD-kezelési igényeinek kielégítésére.

## Következtetés

Ebben az oktatóanyagban bemutattuk azokat a lényeges lépéseket, amelyekkel szöveget adhatunk DWG-fájlokhoz C# és Aspose.CAD használatával. Ez az erőteljes kombináció lehetőséget nyit a dinamikus és testreszabott CAD-dokumentumok generálására.

## GYIK

### 1. kérdés: Az Aspose.CAD kompatibilis a DWG-fájlok összes verziójával?

1. válasz: Az Aspose.CAD a DWG fájlverziók széles skáláját támogatja, biztosítva a kompatibilitást a különböző CAD szoftverekkel.

### 2. kérdés: Hozzáadhatok több szöveges entitást egyetlen DWG-fájlhoz az Aspose.CAD használatával?

2. válasz: Igen, több szöveges entitást is hozzáadhat egy DWG-fájlhoz az oktatóanyagban vázolt folyamat megismétlésével.

### 3. kérdés: Hogyan változtathatom meg a szöveg betűtípusát és stílusát az Aspose.CAD-ben?

 3. válasz: A szöveg betűtípusának és stílusának módosításához állítsa be a tulajdonságait`CadText` objektumot, mielőtt hozzáadná a DWG fájlhoz.

### 4. kérdés: Vannak-e licencelési megfontolások az Aspose.CAD kereskedelmi projektekben való használatához?

 4. válasz: Igen, gondoskodjon az Aspose.CAD licencfeltételeinek való megfelelésről. Hivatkozni[Aspose.CAD vásárlás](https://purchase.aspose.com/buy) a részletekért.

### 5. kérdés: Hol kérhetek segítséget vagy vitathatom meg az Aspose.CAD-vel kapcsolatos lekérdezéseket?

A5: Látogassa meg a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19)kapcsolatba lépni a közösséggel és támogatást kapni.