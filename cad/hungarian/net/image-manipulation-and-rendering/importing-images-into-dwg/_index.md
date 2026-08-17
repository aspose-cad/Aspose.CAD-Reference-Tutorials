---
date: 2026-08-17
description: Ismerje meg, hogyan adhat hozzá képet dwg fájlokhoz C# és az Aspose.CAD
  .NET-hez. Ez az útmutató végigvezeti a képek importálásán, a beszúrási pontok beállításán
  és a PDF-be exportáláson.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Képek importálása DWG fájlokba C#-val
og_description: Ismerje meg, hogyan adhat hozzá képet dwg fájlokhoz C#-ban. Ez a bemutató
  a képek importálását, a beszúrási pontok beállítását és a dwg PDF-be konvertálását
  az Aspose.CAD segítségével tárgyalja.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Hogyan adjunk hozzá képet dwg fájlokhoz C#-ban az Aspose.CAD használatával
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: Hogyan adjunk hozzá képet dwg fájlokhoz C#-ban az Aspose.CAD használatával
url: /hu/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan adjon hozzá képet a dwg fájlokhoz C#-ban az Aspose.CAD használatával

## Bevezetés

Kép hozzáadása egy DWG fájlhoz rutinszerű igény, amikor CAD rajzokat szeretne logókkal, fényképekkel vagy rasztergrafikákkal gazdagítani. Ebben az útmutatóban megtanulja, hogyan **add image to dwg** programozottan C# és Aspose.CAD for .NET használatával, majd opcionálisan átalakítja az eredményt PDF‑be. A lépések bontva vannak, hogy könnyen másolhassa‑beilleszthesse őket a saját projektjébe.

## Gyors válaszok
- **Melyik könyvtár végzi a feladatot?** Aspose.CAD for .NET.
- **Beágyazhatok PNG fájlokat?** Igen – a PNG, JPEG, BMP és más raszterformátumok támogatottak.
- **Szükségem van licencre a fejlesztéshez?** Egy ingyenes próba a teszteléshez megfelelő; a termeléshez kereskedelmi licenc szükséges.
- **Támogatott a PDF export?** Teljesen – egy sorban konvertálhatja a frissített DWG‑t PDF‑be.
- **Mely .NET verziók kompatibilisek?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Mi az a DWG fájl?

A DWG fájl az Autodesk AutoCAD rajzok natív bináris formátuma, amely vektoros geometriát, rétegeket és metaadatokat tárol. Széles körben használják az építészet, mérnöki tudományok és az építőipar területén, és az Aspose.CAD képes olvasni és írni ezt a formátumot AutoCAD telepítése nélkül.

## Miért adjunk képet a dwg-hez az Aspose.CAD használatával?

Az Aspose.CAD **50+ bemeneti és kimeneti formátumot** támogat, képes 500 MB-nál nagyobb fájlokat feldolgozni anélkül, hogy a teljes dokumentumot a memóriába töltené, és determinisztikus API‑t biztosít, amely fej nélküli szerverkörnyezetben működik. Ez a DWG rajzok tömeges feldolgozását gyors és megbízható teszi.

## Előfeltételek
- Alapvető C# programozási ismeretek.
- Az Aspose.CAD for .NET telepítve van. Letöltheti a [Aspose.CAD for .NET letöltési oldalról](https://releases.aspose.com/cad/net/). További Aspose termékeket a [Aspose kiadási oldalon](https://releases.aspose.com/) fedezhet fel.
- Fejlesztői környezet, például Visual Studio 2022 vagy újabb.

## Hogyan adjunk képet a dwg-hez az Aspose.CAD használatával?

Töltse be a cél DWG‑t, hozzon létre egy raszter kép objektumot, amely leírja a beágyazni kívánt képet, állítsa be a beillesztési pontot és a méretezési vektorokat, majd csatolja a képet a rajzhoz. Végül mentse a módosított DWG‑t vagy exportálja közvetlenül PDF‑be. Az egész munkafolyamat csak néhány API‑hívást igényel, és tipikus 2‑oldalas rajzok esetén kevesebb, mint egy másodperc alatt lefut.

### Névterek importálása
Tartalmazza azokat a névtereket, amelyek a szükséges CAD osztályokat teszik elérhetővé.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### 1. lépés: állítsa be a dokumentum könyvtárát
Készítse elő a mappát, amely a forrás DWG‑t és a beágyazni kívánt képet tartalmazza.

```csharp
string MyDir = "Your Document Directory";
```

### 2. lépés: DWG fájl betöltése
`CadImage` osztály egy DWG rajzot képvisel, és hozzáférést biztosít az entitásaihoz, rétegeihez és metaadataihoz.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### 3. lépés: a kép tulajdonságainak meghatározása
Hozzon létre egy `Image` objektumot, amely a raszter fájlra (pl. PNG) mutat, és adja meg annak formátumát.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### 4. lépés: beillesztési pont és vektorok beállítása a DWG‑ben
Adja meg, hol jelenjen meg a kép a rajzon belül, és hogyan legyen méretezve. A beillesztési pont egy 2‑D koordinátával van definiálva, míg a vektorok a szélességet és magasságot szabályozzák.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### 5. lépés: raszter kép létrehozása és konfigurálása
Példányosítson egy `RasterImage` objektumot, rendelje hozzá a kép adatokat, és állítson be további renderelési beállításokat.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### 6. lépés: kép hozzáadása a DWG fájlhoz
Illessze be a konfigurált raszter képet a DWG entitásgyűjteményébe, hogy a rajz része legyen.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### 7. lépés: mentés PDF‑ként (DWG exportálása PDF‑be)
A kép beágyazása után egyetlen hívással **convert dwg to pdf** vagy **save dwg as pdf** műveletet végezhet. Ez hasznos a rajz megosztásához olyan érintettekkel, akiknek nincs CAD szoftvere.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Hogyan konvertáljuk a dwg‑t PDF‑be a kép beágyazása után?

Hívja meg a `Save` metódust a `CadImage` példányon, átadva a `SaveFormat.Pdf` értéket, és opcionálisan egy `PdfOptions` objektumot az oldalméret, raszterizálás és metaadatok szabályozásához. Az Aspose.CAD megőrzi a beágyazott raszter képet, rétegeket és vonalvastagságokat, így hű PDF ábrázolást hoz létre, amely bármely megjelenítőben megnyitható. Ez a konverzió egyetlen kódsorban történik.

## Gyakori problémák és megoldások
- **A kép a rossz helyen jelenik meg** – ellenőrizze a beillesztési pont koordinátáit és az irányvektorokat; ezek a rajz origójához viszonyítva vannak.
- **Nagy képek memóriacsúcsot okoznak** – használja a `Resize` opciót a raszter képen a beillesztés előtt, vagy dolgozzon alacsonyabb felbontású másolattal.
- **A PDF export elveszíti a vektor minőséget** – győződjön meg róla, hogy `PdfOptions`‑szel ment, amely megőrzi a vektor adatokat; a raszter képek mindig úgy vannak beágyazva, ahogy vannak.

## Gyakran ismételt kérdések

**Q: Használhatom az Aspose.CAD for .NET-et más programozási nyelvekkel?**  
A: A core könyvtár .NET‑specifikus, de az Aspose ekvivalens API‑kat kínál Java, Python és más platformok számára.

**Q: Elérhető ingyenes próba az Aspose.CAD‑hez?**  
A: Igen, egy ingyenes próbát a [Aspose free trial page](https://releases.aspose.com/) oldalon tekinthet meg.

**Q: Hol találok részletes dokumentációt az Aspose.CAD‑hez?**  
A: A dokumentáció a [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/) oldalon érhető el.

**Q: Hogyan szerezhetek ideiglenes licencet az Aspose.CAD‑hez?**  
A: Látogassa meg a [temporary license page](https://purchase.aspose.com/temporary-license/) oldalt egy ideiglenes licencért.

**Q: Vannak közösségi fórumok az Aspose.CAD támogatásához?**  
A: Igen, támogatást kérhet és a közösséggel kapcsolatba léphet a [Aspose.CAD community forum](https://forum.aspose.com/c/cad/19) oldalon.

---

**Last Updated:** 2026-08-17  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## Kapcsolódó útmutatók

- [DWG exportálása PDF‑be vagy raszter képekbe – Aspose.CAD útmutató](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [DWG exportálása DXF formátumba C#‑ban – Aspose.CAD tutorial](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Speciális elrendezések exportálása PDF‑be – Aspose.CAD útmutató](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}