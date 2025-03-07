---
title: A vászon méretének és módjának beállítása az Aspose.CAD for .NET-ben
linktitle: A vászon méretének és módjának beállítása
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Tekintse meg az Aspose.CAD for .NET programban a vászon méretének és módjának beállításáról szóló, lépésről lépésre szóló útmutatót. Ezzel az átfogó oktatóanyaggal könnyedén optimalizálhatja CAD-megjelenítését.
weight: 16
url: /hu/net/cad-features-and-support/setting-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# A vászon méretének és módjának beállítása az Aspose.CAD for .NET-ben

## Bevezetés

Készen áll arra, hogy kiaknázza az Aspose.CAD .NET-hez való teljes potenciálját, és forradalmasítsa CAD-megjelenítési élményét? Ebben a lépésről lépésre bemutatott oktatóanyagban a vászon méretének és módjának a nagy teljesítményű Aspose.CAD könyvtár használatával történő beállításának bonyolultságába fogunk elmélyülni. Akár tapasztalt fejlesztő, akár csak kezdő, ez az útmutató végigvezeti Önt a folyamaton, biztosítva, hogy hatékonyan használja ki az Aspose.CAD képességeit.

## Előfeltételek

Mielőtt belevágnánk az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételek teljesülnek:

-  Aspose.CAD Library: Töltse le és telepítse az Aspose.CAD könyvtárat a[Aspose.CAD weboldal](https://releases.aspose.com/cad/net/).

- Fejlesztői környezet: Győződjön meg arról, hogy a gépén be van állítva .NET fejlesztői környezet.

-  Minta CAD fájl: Ehhez az oktatóanyaghoz egy minta DXF fájlt használunk. Találsz egyet a[Aspose.CAD dokumentáció](https://reference.aspose.com/cad/net/).

## Névterek importálása

A kezdéshez importálja a szükséges névtereket a .NET-alkalmazás elejére:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1. lépés: Töltse be a CAD-fájlt

Kezdje a CAD-fájl betöltésével a következő kóddal:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // további lépések kódja ide kerül
}
```

## 2. lépés: A CadRasterizationOptions létrehozása

 Hozzon létre egy példányt a`CadRasterizationOptions` és állítsa be a tulajdonságait:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## 3. lépés: PdfOptions létrehozása

 Hozzon létre egy példányt a`PdfOptions` és állítsa be`VectorRasterizationOptions` ingatlan:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 4. lépés: Exportálás PDF-be

Exportálja a CAD-fájlt PDF-be a konfigurált beállításokkal:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## 5. lépés: Hozzon létre TiffOptions

 Hozzon létre egy példányt a`TiffOptions` és állítsa be`VectorRasterizationOptions` ingatlan:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 6. lépés: Exportálás TIFF formátumba

Exportálja a CAD-fájlt TIFF-be a konfigurált beállításokkal:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Következtetés

Gratulálunk! Sikeresen beállította a vászon méretét és módját az Aspose.CAD for .NET programban. Ez a hatékony funkció a lehetőségek világát nyitja meg a CAD renderelésben. Kísérletezzen különböző lehetőségekkel, és fedezze fel az Aspose.CAD teljes potenciálját .NET-alkalmazásaiban.

## GYIK

### 1. kérdés: Használhatom az Aspose.CAD-ot más .NET könyvtárakkal?

1. válasz: Igen, az Aspose.CAD zökkenőmentesen integrálódik más .NET-könyvtárakba, és továbbfejlesztett lehetőségeket biztosít a CAD-kezeléshez.

### 2. kérdés: Elérhető az Aspose.CAD ingyenes próbaverziója?

 2. válasz: Igen, felfedezheti az Aspose.CAD szolgáltatásait egy ingyenes próbaverzióval. Látogatás[itt](https://releases.aspose.com/) kezdeni.

### 3. kérdés: Hogyan kaphatok támogatást az Aspose.CAD-hez?

 A3: Támogatásért és megbeszélésekért keresse fel a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19).

### 4. kérdés: Hol találom az Aspose.CAD átfogó dokumentációját?

 A4: Lásd a[Aspose.CAD dokumentáció](https://reference.aspose.com/cad/net/) részletes információkért és példákért.

### 5. kérdés: Hogyan vásárolhatom meg az Aspose.CAD-et .NET-hez?

 5. válasz: Az Aspose.CAD megvásárlásához látogassa meg a[vásárlási oldal](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
