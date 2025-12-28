---
date: 2025-12-28
description: Tudja meg, hogyan tölthet be DWG fájlokat Java projektekbe, és állíthatja
  be az elsődleges betűtípus nevét az Aspose.CAD for Java használatával. Lépésről‑lépésre
  útmutató a tökéletes CAD vizuálokhoz.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Hogyan töltsünk be DWG fájlt Java-ban, és cseréljünk betűtípust az Aspose.CAD
  segítségével
url: /hu/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan töltsünk be DWG fájlt Java-ban és cseréljünk betűtípust az Aspose.CAD segítségével

## Introduction

Ha **DWG fájl Java** betöltésére van szükséged Java‑alkalmazásokban, és szeretnéd, hogy a rajzaid kifinomult megjelenést kapjanak, a betűtípus cseréje gyors megoldás. Az Aspose.CAD for Java segítségével a alapértelmezett szövegstílust bármely rendszer‑telepített betűtípusra cserélheted, biztosítva, hogy minden megjegyzés pontosan úgy jelenjen meg, ahogy elvárod. Ebben az útmutatóban végigvezetünk a teljes folyamaton – a DWG fájl Java‑ban történő betöltésétől a `setPrimaryFontName` metódus használatáig a betűtípus megváltoztatásához.

## Quick Answers
- **Melyik könyvtárra van szükségem?** Aspose.CAD for Java.
- **Betölthetek DWG fájlt Java‑ban?** Igen, egyszerűen hívd a `Image.load()`‑t a DWG útvonalára.
- **Melyik metódus változtatja meg a betűtípust?** `setPrimaryFontName`.
- **Szükség van licencre a termeléshez?** Igen, kereskedelmi licenc szükséges.
- **Lehetséges kötegelt feldolgozás?** Teljesen – ugyanazzal a kóddal ciklusba teheted több fájlt.

## What is “load dwg file java”?

A DWG fájl Java környezetben történő betöltése azt jelenti, hogy a bináris CAD adatot egy `Image` objektumba olvassuk be, amelyet az Aspose.CAD manipulálni tud. A fájl betöltése után teljes programozott hozzáférésed lesz a rétegekhez, stílusokhoz és szöveges entitásokhoz.

## Why substitute fonts in a DWG file?

- **Következetesség:** Biztosítja, hogy minden együttműködő ugyanazt a betűtípust lássa, függetlenül a helyi betűtípus-beállításaiktól.  
- **Olvashatóság:** Néhány alap CAD‑betűtípus nehezen olvasható a képernyőkön; egy tiszta betűtípusra, például az Arial‑ra cserélve javul a tisztaság.  
- **Márkaépítés:** A műszaki rajzok összhangba hozása a vállalati stílusirányelvekkel.

## Prerequisites

- **Java Development Kit (JDK)** – bármely friss verzió (8+ ajánlott).  
- **Aspose.CAD for Java** – letölthető a [weboldalról](https://releases.aspose.com/cad/java/).  
- **Sample DWG file** – egy rajz, amelyet módosítani szeretnél (bármely DWG vagy DXF fájlt használhatsz teszteléshez).

## Import Namespaces

A Java projektedben importáld a szükséges osztályokat az Aspose.CAD használatához. Ezek az importok hozzáférést biztosítanak a képbetöltéshez, CAD‑specifikus objektumokhoz és a stíluskezeléshez.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Step‑by‑step guide to substitute the font

### Step 1: Load your DWG file (load dwg file java)

Először állítsd be az API‑t a DWG (vagy DXF) fájl helyére, és töltsd be egy `CadImage` objektumba.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro tip:** Ha közvetlenül DWG fájlokkal dolgozol, cseréld le a `.dxf` kiterjesztést `.dwg`‑re a `srcFile` változóban.

### Step 2: Iterate over the style table and set primary font name

Minden CAD‑rajz tartalmaz egy stílusobjektum‑gyűjteményt. Iterálj végig rajtuk, és használd a `setPrimaryFontName` metódust (az API‑hívás, amely **beállítja az elsődleges betűtípust**) a betűtípus cseréjéhez.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

A `"Arial"`‑t bármely, a gépen telepített betűtípusra cserélheted.

### Step 3: Save the modified drawing

A betűtípus frissítése után írd vissza a változtatásokat egy új DWG fájlba (vagy írd felül az eredetit).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

A mentett fájl most már a megadott betűtípust használja, és minden szöveges megjegyzés ezzel a betűtípussal jelenik meg.

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **Font not applied** | Ellenőrizd, hogy a betűtípus telepítve van-e a gazda operációs rendszeren, és hogy a név pontosan egyezik‑e. |
| **`Image.load` throws an exception** | Győződj meg róla, hogy az elérési út helyes, és a fájl támogatott DWG/DXF formátumú. |
| **Performance slowdown on large files** | Fájlokat külön szálon dolgozz fel, vagy kötegeld őket a UI blokkolás elkerülése érdekében. |

## FAQ's

### Q1: Can I revert font substitutions in my DWG file?

A1: Igen, a betűtípus‑cseréket visszavonhatod az eredeti DWG fájl újratöltésével vagy a CAD szoftverben elérhető visszavonási funkció használatával.

### Q2: Are there any limitations to font substitutions in Aspose.CAD for Java?

A2: A betűtípus‑csere lehetőségei a rendszerben elérhető betűtípusoktól függenek. Győződj meg róla, hogy a kívánt betűtípus hozzáférhető, vagy fontold meg annak beágyazását a DWG fájlba.

### Q3: How can I handle font size adjustments during substitution?

A3: A betűméret‑állítások módosíthatók az Aspose.CAD‑on belüli stílus‑tulajdonságok elérésével és a betűméret megfelelő módosításával.

### Q4: Can I automate font substitution in a batch process?

A4: Igen, az Aspose.CAD for Java támogatja a kötegelt feldolgozást. Automatizálhatod a betűtípus‑cseréket több DWG fájlon szkriptek vagy programozás segítségével.

### Q5: Is Aspose.CAD for Java compatible with the latest CAD file formats?

A5: Igen, az Aspose.CAD for Java rendszeresen frissül, hogy támogassa a legújabb CAD fájlformátumokat, biztosítva a szabványos ipari kompatibilitást.

## Frequently Asked Questions

**Q: A `setPrimaryFontName` metódus csak szöveges entitásokra hat?**  
A: Frissíti az elsődleges betűtípust a stílustáblában, ami viszont befolyásolja az összes olyan szövegobjektet, amely erre a stílusra hivatkozik.

**Q: Használhatok egyedi betűtípust, amely nincs telepítve a rendszerben?**  
A: Az Aspose.CAD a operációs rendszer betűtárát használja. Egyedi betűtípus használatához telepítened kell azt a gépre, ahol a kód fut.

**Q: Lehetséges egyetlen réteghez külön betűtípust beállítani?**  
A: Igen, a `setPrimaryFontName` hívása előtt szűrheted a stílusokat réteg‑név alapján.

**Q: Mely Aspose.CAD verzió szükséges a DWG 2022 fájlokhoz?**  
A: A legújabb kiadás (2025‑től) teljes mértékben támogatja a DWG 2022‑t. Mindig ellenőrizd a kiadási megjegyzéseket a konkrét formátumtámogatásért.

**Q: Hogyan kezeljem a licencelést fejlesztői környezetben?**  
A: Használj ideiglenes értékelési licencet teszteléshez. Termelésben a megvásárolt licencfájlt ágyazd be a `License.setLicense("Aspose.Total.Java.lic");` hívással.

---

**Last Updated:** 2025-12-28  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}