---
date: 2026-03-29
description: Ismerje meg, hogyan hozhat létre PDF-et CAD-ből, állíthatja be a vászon
  méretét, és exportálhatja a CAD-et PDF vagy TIFF formátumba az Aspose.CAD for .NET
  használatával ebben a lépésről‑lépésre útmutatóban.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'PDF létrehozása CAD-ből: Vászonméret és mód beállítása az Aspose.CAD for .NET-ben'
url: /hu/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vászon méretének és módjának beállítása az Aspose.CAD for .NET-ben

## Bevezetés

Készen áll arra, hogy **create PDF from CAD** fájlokból, miközben szabályozza a kimeneti méreteket? Ebben az útmutatóban végigvezetjük a vászon méretének és módjának beállításán, egy CAD fájl betöltésén, és az exportáláson PDF vagy TIFF formátumba az Aspose.CAD for .NET segítségével. Akár **convert DXF to PDF** szeretne, magas felbontású rajzokat generál, vagy egyszerűen csak a rasterizációs területet szeretné módosítani, az alábbi lépések egy stabil, termelésre kész megoldást nyújtanak.

## Gyors válaszok
- **Mit jelent a “create PDF from CAD”?** A CAD rajz (pl. DXF, DWG) PDF dokumentummá konvertálása, amely megőrzi a vektor- és raszter részleteket.  
- **Melyik beállítás szabályozza a kimeneti méretet?** `CadRasterizationOptions.PageWidth` és `PageHeight` (vászon mérete).  
- **Exportálhatok TIFF‑be is?** Igen – használja a `TiffOptions`‑t ugyanazzal a rasterizációs beállítással.  
- **Szükségem van licencre a termeléshez?** Kereskedelmi licenc szükséges; ingyenes próba elérhető.  
- **Támogatott .NET verziók?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Mi az a “create PDF from CAD”?

A PDF létrehozása CAD‑ből azt jelenti, hogy a CAD rajzot egy oldal‑orientált formátumba (PDF) rendereljük, amely megtekinthető, nyomtatható vagy megosztható CAD szoftver nélkül. Az Aspose.CAD elvégzi a nehéz munkát, lehetővé téve a vászon méretének, méretezésnek és kimeneti formátumnak a meghatározását.

## Miért kell beállítani a vászon méretét CAD‑ből PDF‑t készítve?

A vászon méretének beállítása pontos kontrollt biztosít a létrehozott PDF vagy TIFF felbontása és méretei felett. Ez különösen hasznos, ha:
- Rajzok előkészítése nyomtatásra meghatározott papírméreteken.  
- Miniatűrök vagy nagy felbontású képek generálása webes előnézethez.  
- Konzisztens elrendezés biztosítása több dokumentumban.

## Előfeltételek

- Aspose.CAD könyvtár: Töltse le és telepítse az Aspose.CAD könyvtárat a [Aspose.CAD weboldalról](https://releases.aspose.com/cad/net/).
- Fejlesztői környezet: Győződjön meg róla, hogy a gépén be van állítva egy .NET fejlesztői környezet.
- Minta CAD fájl: Ebben az útmutatóban egy minta DXF fájlt használunk. Egyet megtalál a [Aspose.CAD dokumentációban](https://reference.aspose.com/cad/net/).

## Névterek importálása

Először importálja a CAD feldolgozáshoz szükséges névtereket:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Hogyan hozzunk létre PDF-et CAD‑ből egyedi vászon mérettel

### 1. lépés: CAD fájl betöltése

Először **betöltjük a CAD fájlt** (pl. egy DXF‑et) egy `Image` objektumba. Ez az a pont, ahol **betölti a CAD fájlt** a memóriába.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### 2. lépés: CadRasterizationOptions létrehozása

Hozzon létre egy `CadRasterizationOptions` példányt, és határozza meg a vászon méretét. A `PageWidth` és `PageHeight` tulajdonságok lehetővé teszik, hogy **beállítsa a vászon méretét** a pontos kívánt dimenziókra.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### 3. lépés: PdfOptions létrehozása (CAD exportálása PDF‑be)

Kapcsolja össze a rasterizációs beállításokat egy `PdfOptions` objektummal. Ez a konfiguráció lehetővé teszi, hogy **exportálja a CAD‑et PDF‑be** az egyedi vászonnal, amelyet definiált.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 4. lépés: Exportálás PDF‑be (DXF konvertálása PDF‑re)

Most mentse a képet PDF‑ként. Ez a lépés **PDF-et hoz létre CAD‑ből** a beállított opciók használatával.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### 5. lépés: TiffOptions létrehozása (CAD exportálása TIFF‑be)

Ha raster képre is szüksége van, konfigurálja a `TiffOptions`‑t. Ugyanazok a rasterizációs beállítások kerülnek újrahasználatra, így a **CAD exportálása TIFF‑be** tiszteletben tartja a vászon méretét.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 6. lépés: Exportálás TIFF‑be

Végül mentse a rajzot TIFF fájlként.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Gyakori problémák és megoldások

- **A vászon levágottnak tűnik** – Ellenőrizze, hogy az `AutomaticLayoutsScaling` `true`‑ra, a `NoScaling` pedig `false`‑ra van állítva, hogy a rajz a vászonhoz igazodjon.  
- **Alacsony felbontású PDF** – Növelje a `PageWidth`/`PageHeight` értékeket, vagy állítsa be a `Resolution`‑t a `CadRasterizationOptions`‑on.  
- **Fájl nem található hiba** – Győződjön meg róla, hogy a `MyDir` egy érvényes könyvtárra mutat, és a DXF fájl neve pontosan egyezik.

## Gyakran feltett kérdések

### Q1: Használhatom az Aspose.CAD‑ot más .NET könyvtárakkal?

A1: Igen, az Aspose.CAD zökkenőmentesen integrálódik más .NET könyvtárakkal, kibővített lehetőségeket biztosítva a CAD manipulációhoz.

### Q2: Elérhető ingyenes próba az Aspose.CAD‑hoz?

A2: Igen, ingyenes próba keretében felfedezheti az Aspose.CAD funkcióit. Látogassa meg [itt](https://releases.aspose.com/) a kezdéshez.

### Q3: Hogyan kaphatok támogatást az Aspose.CAD‑hoz?

A3: Támogatásért és megbeszélésekért látogassa meg az [Aspose.CAD fórumot](https://forum.aspose.com/c/cad/19).

### Q4: Hol találhatom a részletes dokumentációt az Aspose.CAD‑hoz?

A4: Tekintse meg az [Aspose.CAD dokumentációt](https://reference.aspose.com/cad/net/) a részletes információk és példákért.

### Q5: Hogyan vásárolhatok Aspose.CAD‑ot .NET‑hez?

A5: Az Aspose.CAD megvásárlásához látogassa meg a [vásárlási oldalt](https://purchase.aspose.com/buy).

**További kérdések és válaszok**

**Q: Exportálhatok többoldalas CAD rajzot egyetlen PDF‑be?**  
A: Igen. Állítsa be a `PageCount`‑t a `CadRasterizationOptions`‑ban, és a könyvtár egy PDF‑be fűzi össze az oldalakat.

**Q: Befolyásolja a vászon mérete a vektoradatok minőségét?**  
A: A vektoradatok felbontás‑függetlenek maradnak; a vászon mérete csak a rasterizált elemeket és a kép felbontását érinti.

---

**Legutóbb frissítve:** 2026-03-29  
**Tesztelve a következővel:** Aspose.CAD 24.11 for .NET  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}