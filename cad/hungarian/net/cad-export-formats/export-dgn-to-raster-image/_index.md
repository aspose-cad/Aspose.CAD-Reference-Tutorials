---
date: 2026-03-24
description: Ismerje meg, hogyan konvertálhatja a DGN-t PNG-re, és mentheti a CAD-et
  JPEG formátumban az Aspose.CAD for .NET segítségével – egy gyors útmutató a CAD
  képpé konvertálásához.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hogyan konvertáljuk a DGN-t PNG-re az Aspose.CAD for .NET-ben
url: /hu/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN konvertálása PNG-re az Aspose.CAD for .NET-ben

## Gyors válaszok
- **Konvertálhatok DGN-t PNG-re az Aspose.CAD segítségével?** Igen – csak állítsa be a rasterizálási beállításokat, és válassza a PNG vagy JPEG kimenetet.  
- **Szükségem van licencre a termelésben való használathoz?** Érvényes Aspose.CAD licenc szükséges a nem‑próba telepítésekhez.  
- **Mely .NET verziók támogatottak?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Milyen képfájl formátumok érhetők el?** PNG, JPEG, BMP, GIF, TIFF, és több.  
- **Szükséges a kivételkezelés?** Abszolút – csomagolja a konvertálást try/catch blokkba a fájlhozzáférési problémák kezeléséhez.

## Mi az a „convert dgn to png”?
A DGN (MicroStation) fájl PNG-re konvertálása azt jelenti, hogy a vektoros CAD adatokat raszteres, pixel‑alapú képpé alakítjuk. Ez hasznos előnézet generálásához, rajzok HTML e‑mailben való beágyazásához, vagy bélyegképek létrehozásához dokumentumkezelő rendszerekben.

## Miért használja az Aspose.CAD-et CAD‑kép átalakításhoz?
- **Nincs külső függőség** – teljesen a managed kódban működik.  
- **Nagy pontosság** – megőrzi a vonalvastagságokat, rétegeket és színeket.  
- **Rugalmas kimenet** – PNG, JPEG, BMP stb. között válthat egyetlen beállítás módosításával.  
- **Teljesítmény‑optimalizált** – a rasterizálás gyors még nagy rajzok esetén is.

## Előkövetelmények

Mielőtt elkezdenénk, győződjön meg róla, hogy rendelkezik a következőkkel:

- **Aspose.CAD for .NET** telepítve a projektjében. Letöltheti a [weboldalról](https://reference.aspose.com/cad/net/).  
- Egy mint DGN fájl (pl. `Nikon_D90_Camera.dgn`) egy ismert könyvtárban elhelyezve.

## Névterek importálása

Kezdje a szükséges `using` utasítások hozzáadásával, hogy elérhesse az Aspose.CAD osztályokat.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## 1. lépés: DGN fájl betöltése

Töltse be a forrás DGN-t egy `CadImage` objektumba. Ez az objektum a CAD rajzot memóriában képviseli, és a rasterizálás forrása lesz.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## 2. lépés: Rasterizálási beállítások meghatározása

Állítsa be, hogyan legyen a CAD rajz rasterizálva. Itt szabályozhatja a kép méretét, méretezését és háttérszínét.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## 3. lépés: Kimeneti formátum kiválasztása (PNG vagy JPEG)

Bár a bemutató a PNG-re fókuszál, előfordulhat, hogy **cad-et jpeg‑ként szeretne menteni**. Hozza létre a megfelelő képbeállítási objektumot, és csatolja a rasterizálási beállításokat.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tipp:** PNG fájl generálásához cserélje le a `new JpegOptions()`-t `new PngOptions()`-ra.

## 4. lépés: Raster kép mentése

Végül hívja meg a `Save` metódust a `CadImage` példányon, megadva a kívánt fájlnevet és a beállított opciós objektumot.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Ha `PngOptions`-ra váltott, a fájl `ExportDGNToRasterImage_out.png` néven lesz mentve.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| **Üres kimeneti kép** | `NoScaling` helytelenül beállítva vagy a layout nincs kiválasztva | Állítsa be `AutomaticLayoutsScaling = true`-t, vagy adja meg a kívánt layoutot. |
| **Memóriahiány nagy fájlok esetén** | Nagy DGN betöltése streaming nélkül | Használja a `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })` metódust. |
| **Nem támogatott DGN verzió** | Régebbi MicroStation verziók | Győződjön meg róla, hogy a legújabb Aspose.CAD verziót használja, amely támogatja a régi formátumokat. |

## Gyakran ismételt kérdések

**K: Exportálhatok DGN fájlokat más formátumba, mint a JPEG?**  
A: Igen, az Aspose.CAD for .NET támogatja a PNG, BMP, GIF, TIFF és egyebeket – csak cserélje ki az opciós osztályt (pl. `new PngOptions()`).

**K: Hogyan kezeljem a kivételeket a konvertálás során?**  
A: Csomagolja a konvertálási kódot egy `try/catch` blokkba, és naplózza az `Aspose.CAD.CadException`-t a részletes hibainformációkért.

**K: Elérhető próba verzió az Aspose.CAD for .NET‑hez?**  
A: Igen, a terméket ingyenes próba verzióval kipróbálhatja. További információért látogasson el [ide](https://releases.aspose.com/).

**K: Hol kérhetek segítséget vagy vitathatok meg Aspose.CAD for .NET‑hez kapcsolódó problémákat?**  
A: Látogasson el az [Aspose.CAD fórumra](https://forum.aspose.com/c/cad/19) a közösségi támogatásért és megbeszélésekért.

**K: Hogyan szerezhetek ideiglenes licencet az Aspose.CAD for .NET‑hez?**  
A: Látogasson el [erre a linkre](https://purchase.aspose.com/temporary-license/), hogy ideiglenes licencet szerezzen fejlesztési igényeihez.

## Összegzés

Most már megtanulta, hogyan **convert dgn to png** (vagy JPEG) az Aspose.CAD for .NET használatával. A rasterizálási beállítások módosításával és a kép‑opciók osztályának cseréjével a kimenetet bármely projektkövetelményhez igazíthatja. Nyugodtan kísérletezzen különböző oldalméretekkel, DPI beállításokkal és fájlformátumokkal, hogy a tökéletes raster képet kapja alkalmazásához.

---

**Utolsó frissítés:** 2026-03-24  
**Tesztelve a következővel:** Aspose.CAD 24.11 for .NET  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}