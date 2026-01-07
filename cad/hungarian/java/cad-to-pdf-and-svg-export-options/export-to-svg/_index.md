---
date: 2026-01-07
description: Ismerje meg, hogyan exportálhatja a CAD-et SVG formátumba az Aspose.CAD
  for Java segítségével. Ez a lépésről‑lépésre útmutató bemutatja, hogyan konvertálhat
  DWG‑t SVG‑re, hogyan állíthatja be az SVG színmódot, és hogyan integrálhatja a könyvtárat
  Java projektjébe.
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: CAD exportálása SVG-be az Aspose.CAD for Java használatával
url: /hu/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD exportálása SVG-be az Aspose.CAD for Java segítségével

## Introduction

Üdvözöljük az Aspose.CAD for Java világában, egy erőteljes könyvtárban, amely lehetővé teszi a fejlesztők számára a CAD rajzok könnyű manipulálását. Akár tapasztalt fejlesztő, akár újonc a CAD területén, ez az átfogó útmutató lépésről lépésre végigvezeti Önt a **export CAD to SVG** folyamatán, bemutatva, hogyan konvertáljon DWG-t SVG-be, állítsa be az SVG színmódot, és integrálja az API-t Java projektjébe.

## Quick Answers
- **Mi jelent a „export CAD to SVG”?** CAD rajzot (pl. DWG) alakít át Scalable Vector Graphics (SVG) fájlba, amely böngészőkben megjeleníthető.  
- **Melyik könyvtár végzi a konverziót?** Az Aspose.CAD for Java egyszerű API-t biztosít ehhez a feladathoz.  
- **Szükségem van licencre a fejlesztéshez?** Ingyenes próba verzió teszteléshez elegendő; a termeléshez kereskedelmi licenc szükséges.  
- **Kezelhetem az SVG színkimenetet?** Igen, beállítható az SVG színmód (pl. szürkeárnyalatos).  
- **Szükséges-e további szoftver?** Csak egy Java futtatókörnyezet és az Aspose.CAD JAR fájl.

## Prerequisites

Mielőtt elkezdené a gyakorlati részt, győződjön meg róla, hogy rendelkezik a következőkkel:

- **Java fejlesztői környezet:** Győződjön meg róla, hogy a Java telepítve van a rendszerén.  
- **Aspose.CAD Library:** Töltse le és telepítse az Aspose.CAD for Java könyvtárat a [download link](https://releases.aspose.com/cad/java/).  
- **Document Directory:** Hozzon létre egy könyvtárat a CAD rajzok számára, és jegyezze fel az elérési útját.

## Import Namespaces

Ebben a lépésben importáljuk a szükséges névtereket, hogy elindítsuk az Aspose.CAD használatát. Kövesse az alábbi lépéseket:

### Step 1: Open Your Java Project
Nyissa meg a Java projektjét a választott IDE-ben.

### Step 2: Add Aspose.CAD Library
Adja hozzá az Aspose.CAD könyvtárat a projektjéhez. Ezt a JAR fájl projektfüggőségek közé való felvételével teheti meg.

### Step 3: Import Namespaces
A Java osztályában importálja a szükséges névtereket:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## Export CAD to SVG

Miután előkészítettük a környezetet, merüljünk el a **CAD exportálása SVG-be** lépésről lépésre az Aspose.CAD for Java használatával.

### Step 1: Specify the Resource Directory
Adja meg az erőforrás könyvtár elérési útját, ahol a CAD rajzok találhatók:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Step 2: Load the CAD Drawing
Töltse be a CAD rajzot az Aspose.CAD könyvtár segítségével:

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Step 3: Configure SVG Export Options
Állítsa be az SVG exportálási beállításokat a kimenet testreszabásához. Itt **beállítjuk az SVG színmódot** szürkeárnyalatosra, és megadjuk az exportálónak, hogy a szöveget alakzatokká konvertálja:

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### Step 4: Save as SVG
Mentse a CAD rajzot SVG fájlként:

```java
image.save(dataDir + "meshes.svg");
```

> **Pro tip:** Ha **DWG-t SVG-be** szeretne konvertálni a színek megőrzésével, cserélje a `SvgColorMode.Grayscale` értéket `SvgColorMode.FullColor`-ra.

Gratulálunk! Sikeresen exportált egy CAD rajzot SVG-be az Aspose.CAD for Java segítségével.

## Why Use Aspose.CAD to Export CAD to SVG?
- **Magas hűség:** A vektoradatok megmaradnak, biztosítva, hogy az SVG pontosan úgy nézzen ki, mint az eredeti CAD rajz.  
- **Nincs külső függőség:** A konverzió teljesen Java-ban fut, így nincs szükség további eszközökre.  
- **Testreszabható kimenet:** Az olyan beállítások, mint a `setColorType`, lehetővé teszik, hogy a SVG szürkeárnyalatos vagy teljes színű legyen.

## Common Issues and Solutions
- **Fájl nem található:** Ellenőrizze, hogy a `dataDir` a megfelelő mappára mutat, és a DWG fájl neve egyezik.  
- **Üres SVG kimenet:** Győződjön meg róla, hogy beállította a `options.setTextAsShapes(true)`-t, ha a rajz szöveget tartalmaz, amelyet alakzatként kell megjeleníteni.  
- **Nem támogatott CAD formátum:** Az Aspose.CAD támogatja a DWG, DXF, DWF és több más formátumot; ellenőrizze a dokumentációt a pontos listáért.

## Conclusion

Ebben az útmutatóban bemutattuk az Aspose.CAD for Java zökkenőmentes használatát a **CAD exportálásához SVG-be**. Intuitív API-jával és robusztus funkcióival az Aspose.CAD leegyszerűsíti a bonyolult feladatokat, és fejlesztőknek sokoldalú eszközt biztosít a CAD manipulációhoz.

## FAQ's

### Q1: Can I use Aspose.CAD for Java with other CAD formats?
Igen, az Aspose.CAD különböző CAD formátumokat támogat, beleértve a DWG, DXF, DWF és egyebeket.

### Q2: Is Aspose.CAD suitable for both beginners and experienced developers?
Abszolút! Az Aspose.CAD felhasználóbarát API-t kínál, ami a kezdők számára is hozzáférhető, miközben fejlett funkciókat nyújt a tapasztalt fejlesztőknek.

### Q3: Where can I find additional support or community discussions?
Látogassa meg az [Aspose.CAD Fórumot](https://forum.aspose.com/c/cad/19) támogatás és megbeszélések céljából.

### Q4: Is there a free trial available?
Igen, a [free trial](https://releases.aspose.com/) segítségével kipróbálhatja az Aspose.CAD-et.

### Q5: How can I purchase a license for Aspose.CAD for Java?
Licencet a [purchase page](https://purchase.aspose.com/buy) oldalon vásárolhat.

## Frequently Asked Questions

**Q: Can I convert a DXF file to SVG using the same code?**  
A: Igen, egyszerűen cserélje le a fájlnevet egy DXF fájlra; az API mindkét formátumot kezeli.

**Q: How do I change the output to full‑color SVG?**  
A: Állítsa be a `options.setColorType(SvgColorMode.FullColor);` értéket a mentés előtt.

**Q: Is it possible to embed fonts in the generated SVG?**  
A: Az Aspose.CAD jelenleg a szöveget alakzatokká konvertálja; betűtípusok beágyazása nem szükséges.

**Q: Does the library work on Linux and macOS?**  
A: A Java könyvtár platformfüggetlen, és bárhol fut, ahol kompatibilis JVM áll rendelkezésre.

**Q: What version of Aspose.CAD was used in this tutorial?**  
A: A példát az Aspose.CAD for Java 24.10 verzióval tesztelték.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

---