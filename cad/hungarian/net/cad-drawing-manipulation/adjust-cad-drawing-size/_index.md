---
date: 2026-03-19
description: Tanulja meg, hogyan méretezhet újra CAD-rajzokat .NET-ben az Aspose.CAD
  segítségével, beleértve a CAD-rajzegységek skálázását és az elrendezés méretének
  beállítását. Kövesse lépésről‑lépésre útmutatónkat.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hogyan méretezzük át a CAD rajzokat az Aspose.CAD for .NET segítségével
url: /hu/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan méretezhetünk át CAD rajzokat az Aspose.CAD for .NET segítségével

## Bevezetés

Ha **hogyan méretezhetünk át CAD** fájlokat közvetlenül a .NET alkalmazásából, jó helyen jár. Ebben az útmutatóban megmutatjuk, hogyan változtathatja meg a CAD egységbeállításokat, skálázhatja a CAD rajz méreteit, és programozottan állíthatja be a CAD méretet az Aspose.CAD for .NET használatával. A végére egy stabil, termelés‑kész megoldást kap a támogatott CAD formátumok átméretezésére.

## Gyors válaszok
- **Melyik könyvtár szükséges?** Aspose.CAD for .NET  
- **Megváltoztatható az egységtípus?** Igen – állítsa be a `UnitType` értékét a `CadRasterizationOptions`‑ban  
- **Szükséges licenc a termeléshez?** Érvényes Aspose.CAD licenc szükséges a nem‑próba használathoz  
- **Milyen képfájl formátumba exportál a példa?** BMP (de bármely támogatott raszteres formátum működik)  
- **Hány sor kód?** Kevesebb, mint 30 sor egy teljes átméretezési művelethez  

## Mi az a „how to resize CAD” a gyakorlatban?
A CAD rajz átméretezése azt jelenti, hogy a vektoralapú adatot egy adott skálán vagy egységben (pl. centiméter, hüvelyk) raszteres képpé konvertáljuk. Ez akkor hasznos, ha a rajzokat jelentésekbe kell beágyazni, bélyegképeket kell generálni, vagy CAD vizuális elemeket weboldalakba kell integrálni.

## Miért állítsuk be a CAD méretét az Aspose.CAD‑del?
- **Nincs külső CAD szoftver** – minden a .NET kódban fut.  
- **Finomhangolt vezérlés** az egységek, elrendezések és rasterizálási beállítások felett.  
- **Kereszt‑formátum támogatás** – ugyanaz a kód működik DWG, DXF, DWF és további formátumok esetén.  

## Előfeltételek

Mielőtt belevágna, győződjön meg róla, hogy rendelkezik:

- Aspose.CAD for .NET Library: Töltse le és telepítse a könyvtárat a [Aspose.CAD for .NET letöltési oldalról](https://releases.aspose.com/cad/net/).  
- Minta CAD rajz: Egy `sample.dwg` nevű fájl a projekt dokumentumkönyvtárában.  

## Névterek importálása

Először importálja azokat a névtereket, amelyek hozzáférést biztosítanak az Aspose.CAD osztályaihoz.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1. lépés: CAD rajz betöltése

Töltse be a forrásfájlt egy `Image` objektumba. Ez az objektum a CAD rajzot memóriában képviseli, és az összes további művelet alapja lesz.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## 2. lépés: BmpOptions (vagy bármely más raszteres formátum) létrehozása

A `BmpOptions` megmondja az Aspose.CAD‑nek, hogyan renderelje a vektoralapú adatot, amikor bitmapként menti. Cserélheti `PngOptions`, `JpegOptions` stb. osztályokra a kívánt kimeneti formátumnak megfelelően.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## 3. lépés: CadRasterizationOptions beállítása

A `CadRasterizationOptions` tartalmazza a skálázás, egységkonverzió és elrendezés kiválasztásának fő beállításait. A `BmpOptions` `VectorRasterizationOptions` tulajdonságához való csatolása biztosítja, hogy a rasterizáló az Ön egyedi beállításait használja.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## 4. lépés: UnitType beállítása (CAD egység módosítása)

Itt módosítjuk a CAD egységet az alapértelmezettől centiméterre. Itt található a **change cad unit** kulcsszó, és közvetlenül befolyásolja a végső képméretet.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## 5. lépés: Elrendezések kiválasztása (CAD layoutok beállítása)

Ha a rajz több layout‑ot tartalmaz (pl. Model, Sheet1), adja meg, melyik(ek)et szeretné rasterizálni. A megfelelő layout kiválasztása elengedhetetlen, amikor **set cad layouts**‑t használ egy átméretezett kimenethez.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## 6. lépés: Exportálás BMP‑be (CAD rajz átméretezése)

Végül mentse a rasterizált képet. A kimeneti fájl tükrözi az új méretet, egységet és elrendezést, amelyet beállított – ezzel befejezve a **resize CAD drawing** műveletet.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Most már rendelkezik egy BMP fájllal, amely a átméretezett CAD rajzot reprezentálja, készen áll további feldolgozásra vagy megjelenítésre.

## Gyakori problémák és megoldások

| Probléma | Miért fordul elő | Megoldás |
|----------|------------------|----------|
| A kimenet homályos | Alapértelmezett alacsony DPI (pont per hüvelyk) | Állítsa be a `cadRasterizationOptions.Resolution = 300;` értéket mentés előtt |
| Rossz layout jelenik meg | Layout név elgépelése | Ellenőrizze a pontos layout nevet CAD‑viewerrel vagy a `Layouts` gyűjteménnyel |
| Az egységkonverzió hibás | Metri és angol egységek keverése | Győződjön meg róla, hogy a `UnitType` megfelel a kívánt mérési rendszernek |

## GyIK

### Q1: Az Aspose.CAD for .NET kompatibilis minden CAD formátummal?

A1: Az Aspose.CAD for .NET számos CAD formátumot támogat, köztük DWG, DXF, DWF és még sok mást. Tekintse meg a [dokumentációt](https://reference.aspose.com/cad/net/) a teljes listáért.

### Q2: Méretezhetek egyszerre több layout‑ot?

A2: Igen, több layout‑ot is átméretezhet a `CadRasterizationOptions` `Layouts` tömbjének módosításával.

### Q3: Hol kaphatok támogatást az Aspose.CAD for .NET‑hez?

A3: Látogassa meg az [Aspose.CAD fórumot](https://forum.aspose.com/c/cad/19) a közösségi támogatásért és segítségért.

### Q4: Van ingyenes próba verzió?

A4: Igen, kipróbálhat egy [ingyenes próbaverziót](https://releases.aspose.com/), hogy értékelje az Aspose.CAD for .NET funkcióit.

### Q5: Hogyan szerezhetek ideiglenes licencet az Aspose.CAD for .NET‑hez?

A5: Ideiglenes licencet tesztelési célokra szerezhet [itt](https://purchase.aspose.com/temporary-license/).

## Gyakran feltett kérdések

**K: Hogyan skálázhatok egy CAD rajzot anélkül, hogy megváltoztatnám az egységtípust?**  
V: Állítsa be a `CadRasterizationOptions` `Zoom` tulajdonságát (pl. `cadRasterizationOptions.Zoom = 2.0;`), hogy a méret duplájára nőjön, miközben az eredeti egység megmarad.

**K: Exportálhatok más formátumba, mint a BMP?**  
V: Természetesen. Cserélje le a `BmpOptions`‑t `PngOptions`, `JpegOptions` vagy bármely más támogatott raszteres formátum osztályra.

**K: Lehetséges egy mappában lévő rajzok kötegelt feldolgozása?**  
V: Igen. Iteráljon a könyvtár fájljain, alkalmazza ugyanazt a rasterizálási logikát, és mentse az egyes kimeneteket egyedi névvel.

---

**Utoljára frissítve:** 2026-03-19  
**Tesztelve:** Aspose.CAD for .NET 24.11 (a cikk írásakor legújabb)  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}