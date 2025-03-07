---
title: Támogatott DGN-elemek az Aspose.CAD-ben .NET-hez
linktitle: Támogatott DGN elemek
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Fedezze fel az Aspose.CAD-et a .NET DGN-fájlok kezelésére szolgáló hatékony szolgáltatásaihoz. Kövesse lépésről lépésre útmutatónkat, hogy zökkenőmentesen dolgozzon a 2D és 3D elemekkel.
weight: 18
url: /hu/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Támogatott DGN-elemek az Aspose.CAD-ben .NET-hez

## Bevezetés

Ön .NET-fejlesztő, aki zökkenőmentesen szeretne dolgozni DGN-fájlokkal? Az Aspose.CAD for .NET robusztus megoldást kínál a DGN-fájlok hatékony kezelésére. Ebben az oktatóanyagban a támogatott DGN-elemekbe fogunk belemenni, és végigvezetjük az Aspose.CAD for .NET-hez való munkafolyamatán.

## Előfeltételek

Mielőtt elkezdené, győződjön meg arról, hogy rendelkezik a következőkkel:

- .NET programozási alapismeretek.
- A Visual Studio telepítve van a gépedre.
-  Aspose.CAD for .NET könyvtár, amelyet letölthet[itt](https://releases.aspose.com/cad/net/).

## Névterek importálása

A projekt elindításához importálja a szükséges névtereket .NET-alkalmazásába. Ez a lépés biztosítja, hogy hozzáférjen az Aspose.CAD for .NET szolgáltatásaihoz.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## 1. lépés: Töltse be a DGN fájlt

Kezdje azzal, hogy betölt egy meglévő DGN-fájlt CadImage-ként a .NET-alkalmazásába.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Itt a kódod
}
```

## 2. lépés: Ismétlés DGN-elemeken keresztül

Iteráljon a DGN elemeken keresztül egy foreach ciklus segítségével. Az Aspose.CAD for .NET különféle DGN-elemtípusokat kínál, amelyekkel dolgozhat.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Itt a kódod
}
```

## 3. lépés: A korábban támogatott entitások kezelése

Kezelje a korábban támogatott 2D entitásokat, amelyek most már a 3D-ben is támogatottak.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // További esetek
        {
            // Itt a kódod
            break;
        }
}
```

## 4. lépés: Kezelje a támogatott 3D entitásokat

Kezelje az Aspose.CAD for .NET által biztosított támogatott 3D entitásokat.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Itt a kódod
            break;
        }
}
```

## 5. lépés: Exportálás és mentés

Végül exportálja a módosított DGN fájlt raszterképbe, és mentse el a megadott könyvtárba.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Következtetés

Ebben az oktatóanyagban megvizsgáltuk az Aspose.CAD for .NET képességeit a DGN-fájlok kezelésében és kezelésében. A lépésenkénti útmutatót követve hatékonyan dolgozhat a támogatott DGN elemekkel, legyenek azok 2D vagy 3D entitások. Az Aspose.CAD for .NET lehetővé teszi a DGN-fájlfeldolgozás zökkenőmentes integrálását a .NET-alkalmazásokba.

## GYIK

### 1. kérdés: Hol találom az Aspose.CAD for .NET dokumentációját?

 V1: Megtalálhatja a dokumentációt[itt](https://reference.aspose.com/cad/net/).

### 2. kérdés: Hogyan tölthetem le az Aspose.CAD-et .NET-hez?

 2. válasz: Letöltheti a könyvtárat[itt](https://releases.aspose.com/cad/net/).

### 3. kérdés: Elérhető ingyenes próbaverzió az Aspose.CAD for .NET számára?

 3. válasz: Igen, hozzáférhet az ingyenes próbaverzióhoz[itt](https://releases.aspose.com/).

### 4. kérdés: Hol szerezhetek ideiglenes licenceket az Aspose.CAD for .NET számára?

 A4: Ideiglenes licencek állnak rendelkezésre[itt](https://purchase.aspose.com/temporary-license/).

### 5. kérdés: Segítségre van szüksége, vagy kérdései vannak?

 5. válasz: Keresse fel az Aspose.CAD for .NET közösséget[támogatói fórum](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
