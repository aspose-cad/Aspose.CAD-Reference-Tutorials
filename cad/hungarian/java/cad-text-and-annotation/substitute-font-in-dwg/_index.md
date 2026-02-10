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

## Bevezetés

Ha **DWG fájl Java** betöltésére van szükséged Java-alkalmazásokban, és szeretnéd, hogy a rajzaid kifinomult megjelenése kapjanak, a betűtípus cseréje gyors megoldás. Az Aspose.CAD for Java segítségével a leglényegesebb szövegstílust minden rendszer-telepített betűtípusra cserélve, biztosítva, hogy minden megjegyzés pontosan úgy jelenjen meg, ahogy elvárod. Ebben az útmutatóban végigvezetünk a teljes folyamaton – a DWG fájl Java-ban történő betöltésétől a `setPrimaryFontName` metódus használatáig a betűtípus megváltoztatásához.

## Gyors válaszok
- **Melyik könyvtárra van szükségem?** Aspose.CAD for Java.
- **Betölthetek DWG fájlt Java-ban?** Igen, egyszerűen hívd a `Image.load()`-t a DWG útvonalára.
- **Melyik metódus változtatja meg a betűtípust?** `setPrimaryFontName`.
- **Szükség van licencre a termeléshez?** Igen, kereskedelmi licenc szükséges.
- **Lehetséges kötegelt feldolgozás?** Teljesen – ugyanazzal a kóddal ciklusba teheted több fájlt.

## Mi az a „Java dwg fájl betöltése”?

A DWG fájl Java környezetben történő betöltése azt jelenti, hogy a bináris CAD adatot egy `Image` objektumba olvassuk be, amelyet az Aspose.CAD manipulálni tud. A fájl betöltése után teljes programozott hozzáféréssel lesz a rétegekhez, stílusokhoz és szöveges entitásokhoz.

## Miért érdemes betűtípusokat helyettesíteni egy DWG-fájlban?

- **Következetesség** Biztosítja, hogy minden együttműködő betűtípust lássa, teljesen helyi típus-beállításaiktól.
- **Olvashatóság:** Néhány alap CAD-betűtípus nehezen olvasható a képernyőkön; egy tiszta betűtípusra, például az Arial-ra cserélve javul a tisztaság.
- **Márkaépítés:** A műszaki rajzok összhangba hozása a vállalati stílusirányelvekkel.

## Előfeltételek

- **Java Development Kit (JDK)** – minden friss verzió (8+ ajánlott).
- **Aspose.CAD for Java** – letölthető a [weboldalról](https://releases.aspose.com/cad/java/).
- **Sample DWG file** – egy rajz, csak módosítani szeretnél (bármely DWG vagy DXF fájlt használhatsz teszteléshez).

## Névterek importálása

A Java projektedben importáld a szükséges osztályokat az Aspose.CAD használatához. Ezek az importok hozzáférést biztosítanak a képbetöltéshez, CAD-specifikus objektumokhoz és stíluskezeléshez.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Útmutató lépésről lépésre a betűtípus helyettesítéséhez

### 1. lépés: Töltse be a DWG fájlt (töltsön be dwg fájlt java)

először állítsd be az API-t a DWG (vagy DXF) fájl helyére, és töltsd be egy `CadImage` objektumba.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Pro tip:** Ha közvetlenül DWG fájlokkal dolgozol, cseréld le a `.dxf` kiterjesztést `.dwg`-re a `srcFile` változóban.

### 2. lépés: Ismételje meg a stílustáblázatot, és állítsa be az elsődleges betűtípus nevét

Minden CAD‑rajz tartalmaz egy stílusobjektum‑gyűjteményt. Iterálj végig rajtuk, és használd a `setPrimaryFontName` metódust (az API‑hívás, amely **beállítja az elsődleges betűtípust**) a betűtípus cseréjéhez.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

A `"Arial"`‑t bármely, a gépen telepített betűtípusra cserélheted.

### 3. lépés: Mentse el a módosított rajzot

A betűtípus frissítése után írd vissza a változtatásokat egy új DWG fájlba (vagy írd felül az eredetit).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

A mentett fájl most már a megadott betűtípust használja, és minden szöveges megjegyzés ezzel a betűtípussal jelenik meg.

## Gyakori problémák és megoldások

| Kiadás | Megoldás |
|-------|-----------|
| **A betűtípus nincs alkalmazva** | Ellenőrizd, hogy a betűtípus telepítve van-e a gazda operációs rendszeren, és hogy a név pontosan egyezik-e. |
| **Az "Image.load" kivételt tesz** | Győződj meg róla, hogy az elérési út helyes, és a fájl támogatott DWG/DXF formátumú. |
| **Teljesítménylassulás nagy fájlok esetén** | Fájlokat külön szálon dolgozz fel, vagy kötegeld őket a UI blokkolás elkerülése érdekében. |

## Gyakran Ismételt Kérdések

**K: A `setPrimaryFontName` metódus csak szöveges entitásokra hat?**
A: Frissíti az összes elsődleges betűtípust a stílustáblában, ami viszont befolyásolja az olyan szövegobjektumot, amelyre a stílusra hivatkozik.

**Q: Használhatok egyedi betűtípust, amely nincs telepítve a rendszerben?**
A: Az Aspose.CAD a rendszer betűtárát használja. Egyedi betűtípus használatához telepíteni kell azt a gépre, ahol a kód fut.

**Q: Lehetséges egyetlen réteghez külön betűtípust beállítani?**
A: Igen, a `setPrimaryFontName` hívása előtt szűrheti a stílusokat réteg-név alapján.

**K: Mely Aspose.CAD verzió szükséges a DWG 2022 fájlokhoz?**
A: A legújabb kiadás (2025-től) teljes mértékben támogatja a DWG 2022-t. Mindig ellenőrizd a kiadási megjegyzéseket a konkrét formátumtámogatásért.

**Q: Hogyan kezeljem a licencelést fejlesztői környezetben?**
A: Használj ideiglenes értékelési licencet teszteléshez. Termelésben a megvásárolt licencfájlt ágyazd be a `License.setLicense("Aspose.Total.Java.lic");` hívással.

---

**Utolsó frissítés:** 2025.12.28
**Tesztelve:** Aspose.CAD for Java 24.11
**Szerző:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}