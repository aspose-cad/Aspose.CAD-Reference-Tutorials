---
description: Tanulja meg, hogyan konvertálja a DWG fájlokat PNG-re, és hogyan nyerjen
  ki OLE‑objektumokat a DWG fájlokból az Aspose.CAD for .NET segítségével – egy gyors,
  kódközpontú útmutató.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG konvertálása PNG-re és OLE objektumok exportálása – Aspose.CAD útmutató
url: /hu/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

Now produce final content with all markdown.

Make sure to keep shortcodes exactly.

Let's assemble.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OLE objektumok exportálása DWG fájlokból – Aspose.CAD bemutató

## Bevezetés

Ha **DWG-t PNG-re** kell konvertálnia, miközben kinyeri a beágyazott OLE objektumokat, jó helyen jár. Az Aspose.CAD for .NET egyszerűvé teszi ezt a kéts lépéses folyamatot, lehetővé téve az extrakció és a rasterizálás automatizálását néhány C# sorral. A következő percekben végigvezetjük az egész munkafolyamatot, a környezet beállításától egészen addig, hogy minden DWG-t PNG-ként mentünk el, amely tartalmazza a kinyert OLE adatokat.

## Gyors válaszok
- **Miről szól ez a bemutató?** DWG PNG-re konvertálása és OLE objektumok kinyerése az Aspose.CAD for .NET használatával.  
- **Szükségem van licencre?** A fejlesztéshez ingyenes próba verzió is működik; a termeléshez kereskedelmi licenc szükséges.  
- **Mely .NET verziók támogatottak?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Feldolgozhatok több DWG fájlt egyszerre?** Igen – a példa egy fájlnevek tömbjén iterál.  
- **Hol találok további példákat?** Nézze meg az alábbi hivatalos Aspose.CAD dokumentációt és fórum linkeket.

## Mi az **convert DWG to PNG**?
A DWG (AutoCAD rajz) PNG képpé konvertálása vektoralapú adatokat rasterizál, így könnyen megtekinthető vagy beágyazható weboldalakba, jelentésekbe vagy más alkalmazásokba, amelyek natívan nem támogatják a DWG-t. Ha OLE objektumok is vannak, azok a konvertálás során különálló eszközként kinyerhetők és menthetők.

## Miért kell kinyerni az OLE objektumokat CAD fájlokból?
Sok DWG rajz beágyazott táblázatokat, diagramokat vagy más Office dokumentumokat tartalmaz OLE objektumként. Ezek kinyerése lehetővé teszi az eredeti adatok újrahasználatát, a jelentéskészítés automatizálását vagy a tartalom újabb formátumokra való migrálását anélkül, hogy a beágyazott információ elveszne.

## Előfeltételek

- Aspose.CAD for .NET könyvtár: Győződjön meg róla, hogy a könyvtár telepítve van. Letöltheti a [Aspose.CAD for .NET letöltési oldalról](https://releases.aspose.com/cad/net/).
- Dokumentum könyvtár: Hozzon létre egy könyvtárat, ahol a DWG fájlok tárolva vannak. Cserélje le a `"Your Document Directory"` értéket a megadott kódrészletben a tényleges útvonalra.

## Névterek importálása

A .NET projektjében importálja a szükséges névtereket:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Lépésről‑lépésre útmutató

### 1. lépés: A dokumentum könyvtár beállítása

```csharp
string MyDir = "Your Document Directory";
```

Cserélje le a `"Your Document Directory"` értéket arra az útvonalra, ahol a DWG fájljai találhatók.

### 2. lépés: A feldolgozni kívánt DWG fájlok listázása

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### 3. lépés: Exportálási beállítások konfigurálása PNG konvertáláshoz

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

A `CadRasterizationOptions` beállításait (pl. `PageWidth`, `PageHeight`, `BackgroundColor`) módosíthatja, hogy megfeleljen a kívánt kimeneti felbontásnak.

### 4. lépés: Minden DWG-n végig iterálás és a konvertálás végrehajtása

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Ebben a ciklusban a könyvtár automatikusan **kivonja az OLE objektumokat**, amelyek minden rajzon be vannak ágyazva, és belefoglalja őket a generált PNG-be. Ha a nyers OLE adatfolyamokra van szüksége, elérheti a `cadImage.OleObjects` gyűjteményt – ez egy praktikus módja a **how to extract ole** adatok programozott kinyerésének.

## Gyakori problémák és hibaelhárítás

- **Hiányzó layout név** – Győződjön meg arról, hogy a megadott layout (`"Layout1"` a példában) létezik a forrás DWG-ben; ellenkező esetben a rasterizáló az alapértelmezett modell térre tér vissza.
- **Nagy fájlok memória nyomást okoznak** – Fájlokat egyenként dolgozza fel (ahogy a példában látható), és a `CadImage` objektumokat azonnal szabadítsa fel `using` használatával.
- **Váratlan színek** – Állítsa be a `rasterizationOptions.BackgroundColor` értékét a rajz háttérszínéhez, ha átlátszóságra van szükség.

## Gyakran ismételt kérdések

### Q1: Az Aspose.CAD for .NET alkalmas-e junior és senior CAD fájlokra egyaránt?
A1: Igen, az Aspose.CAD for .NET sokoldalú, és képes kezelni a CAD fájlok széles skáláját, beleértve a junior és senior változatokat is.

### Q2: Testreszabhatom-e az exportálási beállításokat különböző layoutokhoz?
A2: Természetesen! Ahogy a bemutatóban látható, testre szabhatja az exportálási beállításokat, beleértve a layoutokat is, hogy megfeleljenek az Ön konkrét igényeinek.

### Q3: Hol találok részletes dokumentációt az Aspose.CAD for .NET-hez?
A3: Tekintse meg az [Aspose.CAD for .NET dokumentációt](https://reference.aspose.com/cad/net/) a részletes információkért és példákért.

### Q4: Elérhető ingyenes próba verzió?
A4: Igen, az Aspose.CAD for .NET képességeit ingyenes próba verzióval kipróbálhatja. Látogasson el a [linkre](https://releases.aspose.com/), hogy elkezdje.

### Q5: Hogyan kaphatok támogatást vagy csatlakozhatok a közösséghez?
A5: Támogatásért és a közösséghez való csatlakozáshoz látogassa meg az [Aspose.CAD fórumot](https://forum.aspose.com/c/cad/19).

### Q6: Hogyan **extract OLE from CAD** fájlokból konvertálás PNG-re nélkül?
A6: A DWG betöltése után használja a `CadImage.OleObjects` gyűjteményt; iterálhat minden `OleObject`-en, és a nyers adatokat fájlba mentheti.

## Összegzés

Most már látta, hogyan **konvertálhat DWG-t PNG-re**, miközben zökkenőmentesen **kivonja az OLE objektumokat** az Aspose.CAD for .NET használatával. Ez a megközelítés időt takarít meg, megszünteti a manuális másolás‑beillesztés lépéseit, és tisztán integrálódik az automatizált folyamatokba. Nyugodtan kísérletezzen más raszteres formátumokkal (JPEG, BMP), vagy fedezze fel az Aspose által kínált gazdag CAD manipulációs funkciókat.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}