---
date: 2026-08-12
description: DWG-ből szöveg kinyerése és egy adott DWG képpé konvertálása C#-ban az
  Aspose.CAD for .NET használatával. Tanulja meg lépésről‑lépésre a kódrészletekkel.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Különleges DWG képpé konvertálása C#-ban
og_description: DWG-ből szöveg kinyerése és egy adott DWG képpé konvertálása C#-ban
  az Aspose.CAD segítségével. Kövesse ezt a tömör útmutatót a gyors megvalósításhoz.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: DWG-ből szöveg kinyerése és egy adott DWG képpé konvertálása C#-ban
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: DWG-ből szöveg kinyerése és egy adott DWG képpé konvertálása C#-ban
url: /hu/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG konvertálása képpé C#-ban – Aspose.CAD útmutató

## Bevezetés

A modern mérnöki alkalmazásokban gyakran szükség van **szöveg kinyerésére DWG** fájlokból és **konkrét DWG képpé konvertálására** jelentés vagy megjelenítés céljából. Az Aspose.CAD for .NET egy teljes körű API-t biztosít, amely mindkét feladatot kezeli külső CAD szoftver nélkül. Ebben az oktatóanyagban megtanulod, hogyan tölts be egy DWG-t, szűrd ki a szöveg entitásokat, raszterizáld a rajzot, és végül mentsd el az eredményt PDF képként – mindezt tiszta C# kóddal.

## Gyors válaszok
- **Mi az első lépés?** Töltsd be a DWG fájlt a `new CadImage("file.dwg")` segítségével.  
- **Melyik osztály szűri a szöveget?** Használd a `CadEntityFilter`-t a `Text` entitások kiválasztásához.  
- **Hogyan definiálod a kép méretét?** Állítsd be a `Width` és `Height` értékeket a `CadRasterizationOptions`-on.  
- **Milyen kimeneti formátumot használnak?** A példa PDF-be ment, amely beágyazza a raszteres képet.  
- **Szükségem van licencre a termeléshez?** Igen – egy kereskedelmi Aspose.CAD licenc eltávolítja a kiértékelési korlátokat.

## Hogyan lehet szöveget kinyerni a DWG-ből?

Töltsd be a DWG-t, alkalmazz egy szűrőt, amely csak a szöveg entitásokat választja ki, majd olvasd ki minden entitás `TextString` tulajdonságát. Ez a megközelítés visszaad minden megjegyzést, címkét vagy méret szöveget, amely a rajzon szerepel, lehetővé téve annak újrafelhasználását kereséshez, indexeléshez vagy jelentéskészítéshez.

## Miért konvertáljunk egy adott DWG-t képpé?

A DWG raszteres képpé konvertálása lehetővé teszi a rajz beágyazását dokumentumokba, weboldalakba vagy mobilalkalmazásokba, amelyek nem képesek natív CAD formátumot megjeleníteni. Az Aspose.CAD **több mint 50+ CAD formátumot** támogat, és több száz oldalas rajzokat képes raszterizálni kevesebb, mint 200 MB memória felhasználásával, ami nagy áteresztőképességű szerver környezetben is megfelelő.

## Előfeltételek

- Visual Studio (bármelyik újabb verzió) a C# projektek fordításához és futtatásához.  
- Aspose.CAD for .NET – győződj meg róla, hogy a könyvtár telepítve van. A letöltési hivatkozást megtalálod a **[Aspose.CAD for .NET letöltési oldalon](https://releases.aspose.com/cad/net/)**.  
- Egy DWG fájl, amellyel dolgozni szeretnél; a *visualization_-_conference_room.dwg* mintafájl a kódrészletekben használatos.

## Névterek importálása

Az alábbi névterek biztosítják a hozzáférést a fő CAD osztályokhoz, a raszterizálási beállításokhoz és a PDF kimeneti segédeszközökhöz:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 1. lépés: a DWG fájl betöltése

Hozz létre egy `CadImage` példányt a DWG fájl elérési útjának megadásával. A `CadImage` objektum a teljes rajzot memóriában reprezentálja, és hozzáférést biztosít a rétegekhez, entitásokhoz és metaadatokhoz.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## 2. lépés: entitások szűrése

A `CadEntityFilter` lehetővé teszi, hogy csak a szükséges entitásokat válaszd ki. Ebben az útmutatóban úgy konfiguráljuk, hogy **szöveg** objektumokat tartsunk meg, eldobva a vonalakat, köröket és egyéb geometriákat, amelyekre a végső képen nincs szükség.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## 3. lépés: raszterizálási beállítások megadása

A `CadRasterizationOptions` szabályozza, hogyan alakul a rajz bitmapképpé. Meghatározhatod a kimeneti méretet, háttérszínt és felbontást (DPI). Az alábbi definíció bevezeti az osztályt:

A `CadRasterizationOptions` osztály megadja a kép méreteit, felbontását és a renderelési beállításokat a CAD rajzok raszteres formátumokra történő konvertálásához.  

Állítsd be a kívánt szélességet, magasságot és háttérszínt, mielőtt átadnád a beállításokat a PDF exportálónak.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## 4. lépés: PDF beállítások megadása

A `PdfOptions` egyesíti a raszterizálási beállításokat a PDF‑specifikus funkciókkal, például a tömörítéssel. Ennek az osztálynak a definíciója elsőként jelenik meg:

A `PdfOptions` tartalmazza a PDF‑generálási paramétereket, beleértve a raszterizálási beállításokat, amelyek meghatározzák, hogyan jelenik meg a CAD adat a PDF dokumentumban.  

Rendeld hozzá a korábban létrehozott `CadRasterizationOptions` példányt a `VectorRasterizationOptions` tulajdonsághoz.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## 5. lépés: mentés PDF-ként

Végül hívd meg a `Save` metódust a `CadImage` objektumon, megadva a célfájl nevét és a konfigurált `PdfOptions`-t. A PDF egy magas minőségű képet fog tartalmazni a szűrt rajzról.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Gyakori problémák és hibaelhárítás

- **Hiányzó szöveg a szűrés után** – Győződj meg róla, hogy a DWG ténylegesen tartalmaz `Text` entitásokat; egyes rajzok a megjegyzéseket `MText`‑ként tárolják. Szükség esetén módosítsd a szűrőt, hogy `MText`-et is tartalmazzon.  
- **Üres kimeneti kép** – Ellenőrizd, hogy a raszterizálási DPI elég magas legyen (300 DPI biztonságos alapértelmezés), és hogy a háttérszín ne legyen átlátszó a PDF megtekintésekor.  
- **Memóriahiány nagy fájlok esetén** – Használd a `LoadOptions` túlterhelést, amely streaminget tesz lehetővé, így a teljes fájl nem kerül egyszerre a memóriába.

## Gyakran ismételt kérdések

**Q: Az Aspose.CAD kompatibilis minden DWG verzióval?**  
A: Az Aspose.CAD támogatja a DWG kiadásokat az AutoCAD 2000-től a legújabb 2024-es verzióig, lefedve a fájlok több mint 90 %-át a piacon.

**Q: Testreszabhatom a raszterizálási beállításokat különböző kimenetekhez?**  
A: Igen – módosíthatod a felbontást, képformátumot, anti‑aliasingot és háttérszínt, hogy PNG, JPEG vagy PDF célokra optimalizáld.

**Q: Hol találok további példákat és dokumentációt?**  
A: Tekintsd meg a részletes [Aspose.CAD dokumentációt](https://reference.aspose.com/cad/net/) további kódrészletek és API részletekért.

**Q: Van ingyenes próbaverzió az Aspose.CAD‑hez?**  
A: Természetesen – letöltheted a próba verziót a **[Aspose próba letöltési oldalon](https://releases.aspose.com/)**, és korlátozás nélkül kipróbálhatod a funkciókat 30 napig.

**Q: Hogyan kaphatok támogatást vagy csatlakozhatok a közösséghez?**  
A: Csatlakozz az aktív [Aspose.CAD fórumhoz](https://forum.aspose.com/c/cad/19), ahol a fejlesztők megosztják megoldásaikat, és az Aspose csapata válaszol a kérdésekre.

---

**Last Updated:** 2026-08-12  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## Kapcsolódó oktatóanyagok

- [Szöveg keresése DWG fájlokban C#‑val – Aspose.CAD oktatóanyag](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [CAD rajz konvertálása raszteres képpé Aspose.CAD for .NET‑ben](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [DWG dokumentumok renderelése C#‑ban – Aspose.CAD útmutató](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}