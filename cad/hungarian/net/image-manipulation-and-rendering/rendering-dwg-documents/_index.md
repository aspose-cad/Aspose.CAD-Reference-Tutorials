---
date: 2026-08-23
description: Ismerje meg, hogyan hozhat létre viewport dwg c#-t az Aspose.CAD használatával.
  Ez az útmutató bemutatja a DWG fájl betöltését, a rasterizáció beállítását, a viewport
  definiálását, és az eredmény PDF‑ként való mentését.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: DWG dokumentumok renderelése C#-ban
og_description: Ismerje meg, hogyan hozhat létre viewport dwg c#-t az Aspose.CAD .NET
  környezetben. Ez a lépésről‑lépésre útmutató bemutatja a betöltést, a rasterizálást,
  a viewportok definiálását, és a PDF‑be mentést.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Hogyan hozzunk létre viewport dwg c#-t az Aspose.CAD for .NET segítségével
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Hogyan hozzunk létre viewport dwg c#-t az Aspose.CAD for .NET segítségével
url: /hu/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG dokumentumok renderelése C#‑ban – viewport dwg c# létrehozása útmutató

## Bevezetés

Ebben az átfogó útmutatóban megtanulja, hogyan **create viewport dwg c#** az Aspose.CAD segítségével, és hogyan renderelhet egy DWG fájlt PDF‑be. Akár egy adott elrendezést kell kinyernie, akár nyomtatható lapot generál, vagy egy CAD nézetet kell beágyaznia egy jelentésbe, a viewport vezérlése pontos renderelési irányítást biztosít. Az Aspose.CAD **20+ CAD formátumot** támogat, és képes több ezer entitást tartalmazó fájlokat feldolgozni anélkül, hogy az egész dokumentumot a memóriába töltené, így ideális a nagy teljesítményű .NET alkalmazásokhoz.

## Gyors válaszok
- **Mi az első lépés?** Töltse be a DWG fájlt a `CadImage.Load` segítségével.
- **Melyik osztály határozza meg a nézet területét?** `Viewport` a `CadRasterizationOptions`‑ben.
- **Exportálhatok PDF‑be?** Igen, a rasterizálás után a `PdfOptions` használatával.
- **Szükség van licencre a termeléshez?** Kereskedelmi licenc szükséges; egy ingyenes próba a kiértékeléshez működik.
- **.NET Core támogatott?** Teljesen – az Aspose.CAD működik .NET Framework‑kel, .NET Core‑ral és .NET 5/6‑tal.

## Előfeltételek

- Alapvető C# programozási ismeretek.
- Telepített Visual Studio (bármely friss kiadás).
- Az Aspose.CAD könyvtár hozzáadva a projekthez. Letöltheti a [Aspose.CAD download page](https://releases.aspose.com/cad/net/) oldalról.
- Egy például **Bottom_plate.dwg** nevű DWG fájl a gyakorláshoz.

## Névtér importálása

Adja hozzá a szükséges `using` direktívákat a C# fájl tetejéhez, hogy a fordító megtalálja az Aspose.CAD típusokat.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Most, hogy a környezet készen áll, lépésről lépésre végigvezetjük a megvalósításon.

## Hogyan hozhatunk létre viewport dwg c#?

Egy egyedi viewport létrehozásához először töltse be a DWG fájlt egy `CadImage` objektumba, majd konfigurálja a `CadRasterizationOptions`‑t a kívánt elrendezéssel és méretezéssel. Határozza meg a megjeleníteni kívánt területet, hozza létre a `CadVportTableObject`‑et a kiszámított középponttal, magassággal és képaránnyal, cserélje le az aktív viewportot, állítsa be a PDF opciókat, majd mentse el az eredményt.

## 1. lépés: a dwg fájl betöltése

`CadImage.Load` betölti a DWG fájlt egy `CadImage` objektumba, amely a CAD rajzot a memóriában reprezentálja.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## 2. lépés: rasterizálási beállítások konfigurálása

`CadRasterizationOptions` meghatározza, hogyan kerül rasterizálásra a CAD rajz, beleértve az elrendezés kiválasztását, a méretezést és a kimeneti méretet.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## 3. lépés: a rajzolandó terület meghatározása

`Point` definiálja a rajzolandó terület bal‑felső sarkának X és Y koordinátáit.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## 4. lépés: új viewport létrehozása

`CadVportTableObject` egy viewport objektumot képvisel, amely a renderelt rajz látható területét és képarányát szabályozza.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## 5. lépés: az aktív viewport cseréje

A ciklus az aktív viewportot cseréli le az újonnan létrehozottra, hogy alkalmazza az egyedi nézetbeállításokat.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## 6. lépés: PDF opciók konfigurálása

`PdfOptions` konfigurálja a PDF kimeneti paramétereket, például a tömörítést és a metaadatokat.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 7. lépés: a renderelt dwg mentése PDF‑ként

`image.Save` a renderelt képet a megadott formátum opciókkal egy fájlba írja.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Miért használjunk egyedi viewportot DWG renderelésekor?

Egy egyedi viewport lehetővé teszi egy adott elrendezés vagy terület izolálását, csökkentve a fájlméretet és javítva a renderelés sebességét. Az Aspose.CAD egy 300 oldalas DWG‑t kevesebb mint 2 másodperc alatt tud renderelni, ha fókuszált viewportot használunk, szemben a teljes rajz renderelésével, ami több másodpercet vehet igénybe.

## Gyakori problémák és megoldások

- **Üres kimenet** – Győződjön meg róla, hogy a viewport koordináták a rajz kiterjedésein belül vannak; használja a `CadImage.Size`‑t a határok ellenőrzéséhez.
- **Hiányzó rétegek** – Állítsa be a `CadRasterizationOptions.Layouts`‑t a megfelelő elrendezés nevére; különben az alapértelmezett elrendezés üres lehet.
- **Teljesítménycsökkenés** – Tiltsa le az anti‑aliasingot a `CadRasterizationOptions`‑ben, ha csak gyors előnézetre van szüksége.

## Gyakran ismételt kérdések

### Q1: Használhatom az Aspose.CAD‑ot más CAD fájlformátumokkal?
A1: Igen, az Aspose.CAD számos formátumot támogat, többek között a DWG, DXF, DWF és több mint 20 további CAD típust.

### Q2: Az Aspose.CAD kompatibilis a .NET Core‑ral?
A2: Igen, az Aspose.CAD működik .NET Framework‑kel, .NET Core‑ral és a legújabb .NET kiadásokkal.

### Q3: Hogyan kezelhetem a különböző elrendezéseket egy DWG fájlban?
A3: A kívánt elrendezést a renderelés előtt a `CadRasterizationOptions` `Layouts` tulajdonságával adhatja meg.

### Q4: Vannak licencelési szempontok az Aspose.CAD használatakor?
A4: A licencelési részletekért látogassa meg a [Aspose.CAD licensing page](https://purchase.aspose.com/buy) oldalt.

### Q5: Hol találok további támogatást?
A5: Látogassa meg az [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) oldalt a közösségi segítségért és megbeszélésekért.

### Q6: Renderelhetek közvetlenül PNG‑be PDF helyett?
A6: Igen, cserélje a `PdfOptions`‑t `PngOptions`‑ra, és hívja meg a `image.Save("output.png", pngOptions)`‑t.

### Q7: Hogyan ágyazhatom be a renderelt képet egy Windows Forms alkalmazásba?
A7: Töltse be a mentett képet egy `PictureBox` vezérlőbe a `Image.FromFile("output.png")` használatával.

## Összegzés

Most már tudja, hogyan **create viewport dwg c#** és hogyan renderelhet egy DWG fájlt PDF‑be (vagy más raszteres formátumba) az Aspose.CAD segítségével. A viewport manipuláció elsajátításával finomhangolt irányítást kap a vizuális kimenet felett, ami elengedhetetlen a pontos műszaki rajzok, jelentések vagy bélyegképek előállításához. Fedezze fel a további rasterizálási beállításokat, kísérletezzen különböző kimeneti formátumokkal, és integrálja a kódot nagyobb .NET szolgáltatásokba vagy asztali segédprogramokba.

---

**Last Updated:** 2026-08-23  
**Tested with:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## Kapcsolódó útmutatók

- [Hogyan állítsunk be Viewportot DWG PDF‑re konvertálásakor koordinátákkal C#‑ban – Aspose.CAD útmutató](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Tanulja meg a CAD rasterizálási beállítások beállítását – Specifikus elrendezések exportálása PDF‑be az Aspose.CAD‑dal](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Hogyan konvertáljon DWG‑t PDF‑re és raszteres képekre az Aspose.CAD for .NET használatával](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}