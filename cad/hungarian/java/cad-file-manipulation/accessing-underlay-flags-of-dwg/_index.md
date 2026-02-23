---
date: 2026-02-23
description: Tanulja meg, hogyan töltsön be DWG fájlokat az Aspose.CAD DWG for Java
  használatával, és hogyan nyerje ki az alaprajz jelzőit – lépésről lépésre útmutató
  fejlesztőknek.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – DWG betöltése és aláfestés jelzők elérése (Java)
url: /hu/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

## Why extract underlay flags from a DWG?" -> "## Miért kell kinyerni az alávetett jelzőket egy DWG‑ből?" maybe.

Proceed.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG fájl betöltése és alávetett jelzők elérése – Aspose.CAD for Java

A modern CAD munkafolyamatokban **az aspose cad dwg segítségével gyorsan betölthetsz egy DWG fájlt**, és kinyerheted az alávetett részleteket, amelyek gyakran rejtve maradnak a hétköznapi nézők előtt. Akár egy Java DWG megjelenítőt építesz, akár egy kötegelt feldolgozási dwg csővezetéket automatizálsz, vagy metaadatokat nyersz ki GIS integrációhoz, az Aspose.CAD for Java tiszta, kódközpontú megoldást nyújt. Ebben az útmutatóban lépésről‑lépésre bemutatjuk, hogyan **tölts be egy DWG fájlt**, járd be az entitásait, és olvasd ki az alávetett jelzőket, amelyeket sok fejlesztő figyelmen kívül hagy.

## Gyors válaszok
- **Mi a fő osztály egy DWG megnyitásához?** `com.aspose.cad.Image.load()` egy `CadImage`‑et ad vissza.
- **Melyik objektum tartalmazza az alávetett információkat?** `CadUnderlay` (vagy származtatott típusai, mint a `CadDgnUnderlay`).
- **Szükség van licencre fejlesztéshez?** Egy ingyenes próba verzió teszteléshez elegendő; a termeléshez kereskedelmi licenc szükséges.
- **Feldolgozhatok több DWG fájlt egy ciklusban?** Igen – egyszerűen ismételd a betöltés‑és‑iterálás mintát.
- **Ez a megközelítés kompatibilis a Java 11+ verzióval?** Teljesen, az Aspose.CAD támogatja a Java 8‑tól a legújabb LTS kiadásokig.

## aspose cad dwg – DWG fájl betöltése (Java)

`Image.load()` beolvassa a bináris DWG tartalmat, és egy memóriában lévő `CadImage` objektumot hoz létre. Innen felfedezheted a rétegeket, blokkokat és alávetett entitásokat anélkül, hogy magával a DWG formátummal kellene foglalkoznod.

## Miért kell kinyerni az alávetett jelzőket egy DWG‑ből?

Az alávetett jelzők megmutatják, hogyan van egy külső hivatkozás (például DGN vagy PDF alávetett) pozícionálva, méretezve és elforgatva a rajzon belül. Ezeknek az értékeknek a ismerete lehetővé teszi, hogy:

- Újraalkosd a pontos vizuális elrendezést egy egyedi **java dwg viewer**‑ben.
- Alávetetteket natív CAD entitásokká konvertáld további szerkesztéshez.
- Jelentéseket generálj, amelyek alávetett metaadatokat tartalmaznak megfelelőség vagy dokumentáció céljából.
- **Kötegelt dwg** fájlok feldolgozásával tárold az alávetett metaadatokat egy adatbázisban későbbi elemzéshez.

## Előfeltételek
- **Aspose.CAD Library** – töltsd le a [releases](https://releases.aspose.com/cad/java/) oldalról.  
- **Java Development Kit** – JDK 8 vagy újabb.  
- **Egy mappa**, amely a feldolgozni kívánt DWG fájlokat tartalmazza. A kódban a `"Your Document Directory"` helyet cseréld le a saját elérési útvonaladra.

## Import Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Lépés‑ről‑lépésre útmutató

### 1. lépés: Az erőforráskönyvtár beállítása
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Határozd meg, hol találhatók a DWG fájlok. Egy dedikált mappa használata tiszta és hordozható mintát eredményez.

### 2. lépés: DWG fájl betöltése
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Itt **betöltjük a dwg fájlt** `BlockRefDgn.dwg` egy `CadImage` példányba, amely készen áll a vizsgálatra.

### 3. lépés: DWG entitások bejárása
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
A ciklus minden entitást (vonalakat, köröket, blokkokat és alávetetteket) bejár, hogy kiválaszthassuk a szükségeseket.

### 4. lépés: CadDgnUnderlay entitások azonosítása
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Csak a `CadDgnUnderlay` objektumok tartalmazzák a keresett alávetett jelzőket, ezért ezeket szűrjük ki.

### 5. lépés: Alávetett információk elérése
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Miután megvan egy `CadUnderlay`, kiolvashatod az útvonalát, nevét, beillesztési pontját, forgását, méretezési tényezőit, valamint az `UnderlayFlags` enumerációt, amely a láthatóságot, vágást és egyéb megjelenítési opciókat jelzi.

## Hogyan tölts be dwg fájlokat kötegelt folyamatban

Ha **kötegelt dwg** fájlok feldolgozására van szükséged, csomagold a fenti lépéseket egy egyszerű `for` ciklusba, amely az összes fájlt a `dataDir`‑ben bejárja. Az ugyanaz az `Image.load()` hívás minden fájlra működik, és a kinyert jelzőket CSV‑be vagy adatbázisba mentheted a további jelentéskészítéshez.

## Gyakori problémák és tippek
- **Null alávetett útvonal** – Győződj meg arról, hogy a DWG valóban hivatkozik egy külső fájlra; ellenkező esetben az útvonal üres lesz.
- **Nem támogatott alávetett típus** – Az Aspose.CAD jelenleg csak DGN alávetetteket támogat; a PDF alávetettek még nem érhetők el az API‑n keresztül.
- **Licenc kivételek** – Érvényes licenc nélkül a kiexportált képekre vízjel kerül.
- **Teljesítmény tipp:** Több fájl kötegelt feldolgozásakor használd ugyanazt a `Image` példányt, hogy csökkentsd a GC terhelését.

## Gyakran feltett kérdések

**Q: Használhatom az Aspose.CAD for Java‑t más CAD fájlformátumokkal is?**  
A: Az Aspose.CAD elsősorban a DWG formátumra fókuszál, de támogatja a DXF, DWF és egyéb CAD formátumokat is.

**Q: Elérhető próba verzió az Aspose.CAD for Java‑hoz?**  
A: Igen, a funkciókat ingyenes próba verzióval kipróbálhatod [itt](https://releases.aspose.com/).

**Q: Hogyan kaphatok támogatást vagy segítséget az Aspose.CAD for Java‑hoz?**  
A: Látogasd meg az [Aspose.CAD fórumot](https://forum.aspose.com/c/cad/19) a közösségi támogatás és a megbeszélések céljából.

**Q: Elérhetők ideiglenes licencek az Aspose.CAD for Java‑hoz?**  
A: Igen, ideiglenes licencet kaphatsz [itt](https://purchase.aspose.com/temporary-license/).

**Q: Hol találom az Aspose.CAD for Java átfogó dokumentációját?**  
A: Tekintsd meg a [documentation](https://reference.aspose.com/cad/java/) oldalt a részletes információkért.

---

**Utolsó frissítés:** 2026-02-23  
**Tesztelve:** Aspose.CAD 24.12 for Java  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}