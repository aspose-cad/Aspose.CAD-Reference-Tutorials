---
title: Egyetlen PDF készítése különböző elrendezésekkel – Aspose.CAD útmutató
linktitle: Egyetlen PDF készítése különböző elrendezésekkel
second_title: Aspose.CAD .NET - CAD és BIM fájlformátum
description: Hozzon létre egyetlen PDF-t különböző elrendezésekkel az Aspose.CAD for .NET segítségével. Kövesse lépésről lépésre útmutatónkat a zökkenőmentes integráció és a hatékony PDF-generálás érdekében.
weight: 13
url: /hu/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Egyetlen PDF készítése különböző elrendezésekkel – Aspose.CAD útmutató

## Bevezetés

Egyetlen PDF-dokumentumot szeretne létrehozni egy különböző elrendezésű CAD-rajzból az Aspose.CAD for .NET használatával? Ez a lépésenkénti útmutató végigvezeti Önt a folyamaton, segíti a zökkenőmentes integrációt és a hatékony PDF-készítést. Az Aspose.CAD for .NET hatékony funkciókat kínál a CAD-rajzok programozott kezeléséhez, és ebben az oktatóanyagban egyetlen PDF létrehozására összpontosítunk különböző elrendezésekkel.

## Előfeltételek

Mielőtt belevágna az oktatóanyagba, győződjön meg arról, hogy rendelkezik a következő előfeltételekkel:

-  Aspose.CAD for .NET: Győződjön meg arról, hogy az Aspose.CAD for .NET telepítve van. Letöltheti innen[itt](https://releases.aspose.com/cad/net/).

- Fejlesztői környezet: Hozzon létre egy .NET fejlesztői környezetet, és rendelkezzen alapvető ismeretekkel a C# programozásról.

## Névterek importálása

C#-projektben tartalmazza a szükséges névtereket az Aspose.CAD for .NET funkcióinak kihasználásához:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 1. lépés: Töltse be a CAD-képet

```csharp
// A dokumentumok könyvtárának elérési útja.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Az 1. lépés kódja ide kerül
}
```

## 2. lépés: A raszterezési beállítások testreszabása

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Egyedi méretek többféle elrendezéshez
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## 3. lépés: Adja meg a PDF-beállításokat

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## 4. lépés: Mentés PDF-ként

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Sikeresen létrehozott egyetlen PDF-dokumentumot különböző elrendezésekkel az Aspose.CAD for .NET segítségével. Nyugodtan fedezze fel a további funkciókat, és szabja testre a kódot sajátos igényei szerint.

## Következtetés

Ebben az oktatóanyagban az Aspose.CAD for .NET használatával egyetlen PDF létrehozásának folyamatát ismertettük CAD-rajzból különböző elrendezésekkel. Ez a nagy teljesítményű könyvtár leegyszerűsíti a CAD-kezelési feladatokat, és rugalmasságot kínál a különféle forgatókönyvekhez.

## GYIK

### 1. kérdés: Használhatom az Aspose.CAD for .NET fájlt más CAD formátumokkal?

1. válasz: Igen, az Aspose.CAD for .NET támogatja a különböző CAD formátumokat, mint például a DWG, DXF, DGN stb.

### 2. kérdés: Van ingyenes próbaverzió?

 2. válasz: Igen, felfedezheti az ingyenes próbaverziót[itt](https://releases.aspose.com/).

### 3. kérdés: Hogyan kaphatok támogatást az Aspose.CAD for .NET számára?

 A3: Látogassa meg a[Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) közösségi támogatásért.

### 4. kérdés: Hol találok részletes dokumentációt?

 A4: Lásd a dokumentációt[itt](https://reference.aspose.com/cad/net/).

### 5. kérdés: Vásárolhatok licencet az Aspose.CAD for .NET számára?

 V5: Igen, vásárolhat licencet[itt](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
