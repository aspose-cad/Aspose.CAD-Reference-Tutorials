---
title: 3D képek exportálása PDF-be – Aspose.CAD oktatóanyag
linktitle: 3D képek exportálása PDF-be
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Könnyedén konvertálhat 3D CAD képeket PDF-be az Aspose.CAD for .NET segítségével. Kövesse lépésről lépésre bemutató oktatóanyagunkat a zökkenőmentes PDF-exportáláshoz.
weight: 10
url: /hu/net/3d-image-export/exporting-3d-images-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 3D képek exportálása PDF-be – Aspose.CAD oktatóanyag

## Bevezetés

3D képeket szeretne zökkenőmentesen exportálni PDF formátumba az Aspose.CAD for .NET segítségével? Ez a lépésenkénti oktatóanyag végigvezeti Önt a folyamaton, biztosítva, hogy az Aspose.CAD erejét kihasználva könnyedén konvertálja 3D képeit PDF formátumba.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy a következő előfeltételeket teljesítette:

-  Aspose.CAD for .NET: Győződjön meg arról, hogy telepítve van a .NET Aspose.CAD könyvtára. Ha nem, akkor letöltheti a[Aspose.CAD for .NET letöltési oldal](https://releases.aspose.com/cad/net/).

- Dokumentumkönyvtár: Állítson be egy könyvtárat, ahol a CAD-fájlokat tárolja, és jegyezze fel az elérési utat.

## Névterek importálása

A .NET-projektben importálja az Aspose.CAD használatához szükséges névtereket. Adja hozzá a következő sorokat a kódfájl tetejéhez:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## 1. lépés: Töltse be a CAD-képet

 Kezdje a PDF-be exportálni kívánt CAD-kép betöltésével. Használja a`Load` módszert az Aspose.CAD könyvtárból. Cserélje ki`"conic_pyramid.dxf"` a CAD-fájl elérési útjával.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Ide kerül a CAD-kép betöltéséhez szükséges kód
}
```

## 2. lépés: Konfigurálja a raszterezési beállításokat

 Konfigurálja a CAD-kép raszterezési beállításait. Állítson be olyan paramétereket, mint az oldalszélesség, az oldal magassága és az elrendezés. Törölje a következőhöz kapcsolódó sor megjegyzését`TypeOfEntities` ha az entitásai 3D-sek.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## 3. lépés: Állítsa be a PDF-beállításokat

Hozzon létre PDF-beállításokat, és társítsa őket a raszterezési beállításokhoz.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 4. lépés: Mentés PDF-ként

Mentse el a CAD-képet PDF-fájlként a konfigurált beállítások segítségével. Adja meg a PDF-fájl kimeneti útvonalát.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Következtetés

Gratulálunk! Sikeresen exportálta a 3D képeket PDF-be az Aspose.CAD for .NET segítségével. Ez az egyszerű oktatóanyag biztosítja, hogy könnyedén konvertálja a CAD fájlokat egy könnyebben hozzáférhető formátumba.

## GYIK

### 1. kérdés: Az Aspose.CAD kompatibilis az összes CAD fájlformátummal?

1. válasz: Igen, az Aspose.CAD a CAD formátumok széles skáláját támogatja, rugalmasságot biztosítva a különféle fájltípusok kezelésében.

### 2. kérdés: Testreszabhatom az oldal méreteit PDF-be exportáláskor?

A2: Abszolút. Az oktatóanyag bemutatja, hogyan konfigurálhatja az oldal szélességét és magasságát az Ön igényei szerint.

### 3. kérdés: Rendelkezésre állnak ideiglenes licencek az Aspose.CAD számára?

 3. válasz: Igen, ideiglenes licenceket szerezhet be az Aspose.CAD-hez, ha felkeresi[Ideiglenes jogosítvány](https://purchase.aspose.com/temporary-license/).

### 4. kérdés: Hol találhatok további támogatást vagy közösségi megbeszéléseket?

 A4: Irány a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) a közösség támogatásáért és kapcsolattartásáért.

### 5. kérdés: Elérhető az Aspose.CAD ingyenes próbaverziója?

 5. válasz: Igen, felfedezheti az Aspose.CAD szolgáltatásait, ha eléri a[ingyenes próbaverzió](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
