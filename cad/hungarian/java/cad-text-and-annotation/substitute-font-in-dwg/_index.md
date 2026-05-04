---
date: 2026-05-04
description: Tanulja meg, hogyan konvertálja a dxf-et dwg-re, és állítsa be az alap
  betűtípust Java-ban az Aspose.CAD használatával. Lépésről lépésre útmutató a tökéletes
  CAD vizuálisokhoz.
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: Betűtípus helyettesítése DWG‑ben
second_title: Aspose.CAD Java API
title: DXF konvertálása DWG-re és betűtípus módosítása DWG-ben Aspose.CAD Java
url: /hu/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan töltsünk be DWG fájlt Java-ban és cseréljünk betűtípust az Aspose.CAD segítségével

## Bevezetés

Ha Java alkalmazásokban **convert dxf to dwg**-ra van szükséged, és szeretnéd, hogy a rajzaid kifinomult megjelenést kapjanak, a betűtípus cseréje gyors megoldás. Az Aspose.CAD for Java segítségével kicserélheted az alapértelmezett szövegstílust bármely rendszer‑telepített betűtípusra, biztosítva, hogy minden annotáció pontosan úgy jelenjen meg, ahogy elvárod. Ebben az útmutatóban végigvezetünk a teljes folyamaton – a DWG fájl Java‑ban történő betöltésétől a `setPrimaryFontName` metódus használatáig a betűtípus módosításához.

## Gyors válaszok
- **Milyen könyvtárra van szükségem?** Aspose.CAD for Java.  
- **Betölthetek DWG fájlt Java-ban?** Igen, egyszerűen hívd a `Image.load()`-t a DWG útvonalon.  
- **Melyik metódus változtatja a betűtípust?** `setPrimaryFontName`.  
- **Szükségem van licencre a termeléshez?** Igen, kereskedelmi licenc szükséges.  
- **Lehetséges a kötegelt feldolgozás?** Teljesen – ugyanazzal a kóddal több fájlt is feldolgozhatsz ciklusban.

## Mi az **convert dxf to dwg**?

A “convert dxf to dwg” arra utal, hogy egy DXF (Drawing Exchange Format) fájlt átalakítanak a natív DWG formátummá, amelyet számos CAD alkalmazás használ. A konvertálás lehetővé teszi, hogy egy széles körben támogatott DXF rajzot DWG munkafolyamatba vigyünk, majd fejlett stílusalkalmazásokat—például betűtípuscsere—használjunk az Aspose.CAD segítségével.

## Miért cseréljünk betűtípusokat egy DWG fájlban?

- **Következetesség:** Garantálja, hogy minden együttműködő ugyanazt a betűtípust lássa, függetlenül a helyi betűtár beállításaitól.  
- **Olvashatóság:** Néhány alapértelmezett CAD betűtípus nehezen olvasható a képernyőkön; egy tiszta betűtípusra, például az Arial-ra cserélve javul a tisztaság.  
- **Márkázás:** Összhangba hozza a műszaki rajzokat a vállalati stílus útmutatókkal.  

## Gyakori felhasználási esetek

| Forgatókönyv | Miért fontos |
|--------------|--------------|
| **Örökölt DXF rajzok kötegelt konvertálása** | Átalakíthatod őket DWG-re, és egy lépésben érvényesítheted a vállalati betűtípust. |
| **Rajzok előkészítése ügyfélprezentációkhoz** | A következetes, olvasható betűtípusok professzionális megjelenést kölcsönöznek a dokumentumoknak. |
| **Automatizált CAD folyamatok** | A betűtípuscsere beágyazása megszünteti a kézi utófeldolgozási lépéseket. |

## Előfeltételek

- **Java Development Kit (JDK)** – bármely friss verzió (8+ ajánlott).  
- **Aspose.CAD for Java** – letöltés a [website](https://releases.aspose.com/cad/java/).  
- **Sample DWG/DXF file** – egy rajz, amelyet módosítani szeretnél (bármilyen DWG vagy DXF fájlt használhatsz teszteléshez).

## Névterek importálása

Java projektedben importáld a szükséges osztályokat az Aspose.CAD használatához. Ezek az importok hozzáférést biztosítanak a kép betöltéséhez, a CAD‑specifikus objektumokhoz és a stíluskezeléshez.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Lépésről‑lépésre útmutató a betűtípus cseréjéhez

### 1. lépés: Töltsd be a DWG fájlt (load dwg file java)

Először állítsd be az API-t a DWG (vagy DXF) fájl helyére, és töltsd be egy `CadImage` objektumba.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro tip:** Ha közvetlenül DWG fájlokkal dolgozol, cseréld le a `.dxf` kiterjesztést `.dwg`-re a `srcFile` változóban.

### 2. lépés: Iterálj a stílus táblán és állítsd be az elsődleges betűtípus nevét

Minden CAD rajz tartalmaz egy stílusobjektumok gyűjteményét. Iterálj végig rajtuk, és használd a `setPrimaryFontName` metódust (az API hívás, amely **sets primary font name**), hogy kicseréld a betűtípust.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

A `"Arial"`-t bármely, a kódot futtató gépen telepített betűtípusra cserélheted.

### 3. lépés: Mentsd el a módosított rajzot

Miután frissítetted a betűtípust, írd vissza a változtatásokat egy új DWG fájlba (vagy írd felül az eredetit).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

A mentett fájl most a megadott betűtípust használja, és minden szöveges annotáció ezzel a betűtípussal jelenik meg.

## Gyakori problémák és megoldások

| Probléma | Megoldás |
|----------|----------|
| **Betűtípus nem alkalmazva** | Ellenőrizd, hogy a betűtípus telepítve van-e a host operációs rendszeren, és hogy a név pontosan egyezik. |
| **`Image.load` kivételt dob** | Győződj meg róla, hogy a fájl útvonala helyes, és hogy a fájl támogatott DWG/DXF formátum. |
| **Teljesítménycsökkenés nagy fájlok esetén** | Feldolgozd a fájlokat külön szálon vagy kötegeld őket a UI blokkolás elkerülése érdekében. |

## Gyakran feltett kérdések

**Q: A `setPrimaryFontName` metódus csak szöveges entitásokra hat?**  
A: Frissíti a stílus táblázat elsődleges betűtípusát, ami viszont minden olyan szövegobjektust befolyásol, amely hivatkozik arra a stílusra.

**Q: Használhatok egy egyedi betűtípust, amely nincs telepítve a rendszerben?**  
A: Az Aspose.CAD az operációs rendszer betűtár-nyilvántartására támaszkodik. Egy egyedi betűtípus használatához telepíteni kell azt a kódot futtató gépre.

**Q: Lehetséges csak egyetlen réteg betűtípusát megváltoztatni?**  
A: Igen, a `setPrimaryFontName` hívása előtt szűrheted a stílusokat réteg neve alapján.

**Q: Mely Aspose.CAD verzió szükséges a DWG 2022 fájlokhoz?**  
A: A legújabb kiadás (2025-ig) teljes mértékben támogatja a DWG 2022-t. Mindig ellenőrizd a kiadási megjegyzéseket a konkrét formátumtámogatásért.

**Q: Hogyan kezelem a licencelést fejlesztői környezetben?**  
A: Használj ideiglenes értékelő licencet a teszteléshez. Termelésben ágyazd be a megvásárolt licencfájlt a `License.setLicense("Aspose.Total.Java.lic");` segítségével.

---

**Utoljára frissítve:** 2026-05-04  
**Tesztelve ezzel:** Aspose.CAD for Java 24.11  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}