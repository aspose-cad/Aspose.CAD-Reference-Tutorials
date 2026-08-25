---
date: 2026-05-25
description: Ismerje meg, hogyan állíthatja be a mérő licencelést az Aspose.CAD for
  Java-ban a CAD feldolgozás optimalizálása, a költségek csökkentése és a használat
  hatékony nyomon követése érdekében.
keywords:
- how to set metered
- Aspose.CAD licensing
- Java metered licensing
linktitle: Hogyan állítsuk be a mérő licencelést az Aspose.CAD-ban
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to set metered licensing in Aspose.CAD for Java to optimize
    CAD processing, reduce costs, and track usage efficiently.
  headline: How to Set Metered Licensing in Aspose.CAD
  type: TechArticle
- questions:
  - answer: A usage‑based model that tracks API calls and charges per consumption
      unit.
    question: What is metered licensing?
  - answer: Two keys – a public and a private key – generated from your Aspose account.
    question: How many keys are required?
  - answer: Yes, call `License.getConsumptionQuantity()` before and after processing.
    question: Can I check usage programmatically?
  - answer: A free trial license can be obtained from the Aspose website.
    question: Is a trial available?
  - answer: Java 8 through 17 are fully supported.
    question: Which Java version is supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Hogyan állítsuk be a mérő licencelést az Aspose.CAD-ban
url: /hu/java/licensing-and-configuration/metered-licensing-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mérői licencelés az Aspose.CAD-ban

## Bevezetés

Fedezze fel az Aspose.CAD for Java teljes potenciálját a **metrikus licenc beállítása**! Ez a lépésről‑lépésre útmutató végigvezeti Önt minden szakaszon—az előkövetelmények telepítésétől, a megfelelő csomagok importálásáig, a fogyasztás méréséig a feldolgozás előtt és után. A végére pontosan tudni fogja, hogyan kell **metrikus licenc** kulcsokat beállítani, olvasni a használati mutatókat, és költséghatékonyan tartani a CAD munkafolyamatot.

## Gyors válaszok
- **Mi az a metrikus licencelés?** Egy használaton alapuló modell, amely nyomon követi az API hívásokat és egységfogyasztásonként számláz.  
- **Hány kulcsra van szükség?** Két kulcs – egy nyilvános és egy privát kulcs – amelyet az Aspose fiókjából generál.  
- **Ellenőrizhetem a használatot programozottan?** Igen, hívja a `License.getConsumptionQuantity()`‑t a feldolgozás előtt és után.  
- **Elérhető próba?** Ingyenes próba licenc szerezhető az Aspose weboldaláról.  
- **Mely Java verzió támogatott?** A Java 8‑tól 17‑ig teljes mértékben támogatott.

## Mi az a metrikus licencelés az Aspose.CAD-ban?
A metrikus licencelés az Aspose.CAD fizess‑amint‑használsz modellje, amely minden API hívást fogyasztási egységként rögzít. Lehetővé teszi a pontos használat nyomon követését, a túlkapacitás elkerülését, és csak a ténylegesen felhasznált mennyiségért való fizetést.

## Miért használjunk metrikus licencelést CAD feldolgozáshoz?
Az Aspose.CAD **50+** bemeneti és kimeneti formátumot támogat—beleértve a DWG, DXF, DGN és SVG formátumokat—és **2 GB**-ig képes fájlokat feldolgozni anélkül, hogy a teljes dokumentumot a memóriába töltené. Ez a hatékonyság alacsonyabb szerverköltségeket eredményez, különösen nagy rajzcsomagok kezelésekor.

## Előkövetelmények

Mielőtt belemerülne a metrikus licencelés világába az Aspose.CAD‑del, győződjön meg róla, hogy a következők rendelkezésre állnak:

### Java Development Kit (JDK) telepítése

Győződjön meg róla, hogy a legújabb Java Development Kit verzió telepítve van a rendszerén. Letöltheti [innen](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.CAD for Java könyvtár

Győződjön meg róla, hogy letölti és beállítja az Aspose.CAD for Java könyvtárat. A könyvtárat megtalálja [itt](https://releases.aspose.com/cad/java/). Más Aspose kiadásokat is böngészhet [itt](https://releases.aspose.com/).

## Hogyan állítsuk be a metrikus licencelést az Aspose.CAD for Java-ban?

Töltse be a nyilvános és privát kulcsait, hívja meg a `License.setMeteredKey(publicKey, privateKey)`‑t, és a könyvtár azonnal átvált metrikus módra. Ez az egyetlen hívás aktiválja a használat nyomon követését minden későbbi API műveletnél, lehetővé téve a fogyasztás lekérdezését a feldolgozás előtti és utáni lépésben.

## Csomagok importálása

A könyvtár használatához importálja a fő csomagját:

`import com.aspose.cad.*;` hozza be az Aspose.CAD osztályokat a projektbe.

```java
import com.aspose.cad;
```

## 1. lépés: Metrikus kulcs beállítása

`setMeteredKey` regisztrálja a nyilvános és privát kulcsait az Aspose.CAD könyvtárral.

Először állítsa be a metrikus kulcsot a `setMeteredKey` metódus használatával. Cserélje le a `<valid public key>` és `<valid private key>` helyőrzőket a tényleges nyilvános és privát kulcsokra.

```java
Metered.setMeteredKey("<valid public key>", "<valid private key>");
```

## 2. lépés: Fogyasztási mennyiség lekérése a feldolgozás előtt

`getConsumptionQuantity` visszaadja a eddig rögzített fogyasztási egységek teljes számát.

Szerezze be a felhasznált mennyiség értékét az Aspose.CAD API elérése előtt, hogy kezdeti képet kapjon.

```java
BigDecimal quantityOld = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity before processing: " + quantityOld);
```

## 3. lépés: Feldolgozás

Végezze el a kívánt CAD feldolgozást az Aspose.CAD funkciók használatával. Távolítsa el a megjegyzést a kódrészletről, amely az adott feladathoz kapcsolódik, például egy CAD kép betöltéséhez.

```java
// Example:
// com.aspose.cad.fileformats.cad.CadImage image =
// (com.aspose.cad.fileformats.cad.CadImage)com.aspose.cad.Image.load("BlockRefDgn.dwg");
```

## 4. lépés: Fogyasztási mennyiség lekérése a feldolgozás után

A feldolgozás után szerezze be újra a felhasznált mennyiség értékét, hogy felmérje a hatást.

```java
BigDecimal quantity = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity after processing: " + quantity);
```

Ismételje meg ezeket a lépéseket minden további feldolgozás vagy feladat esetén, ahogy szükséges.

## Gyakori problémák és megoldások

- **Érvénytelen kulcs hiba:** Ellenőrizze, hogy mindkét kulcs pontosan úgy van másolva, ahogy az Aspose fiókjában látható; a felesleges szóközök hitelesítési hibákat okoznak.  
- **Nulla fogyasztás jelentve:** Győződjön meg róla, hogy a `License.getConsumptionQuantity()`‑t az első API használat *után* hívja; az első hívás inicializálja a számlálót.  
- **Teljesítménycsökkenés nagy fájloknál:** Használja a `CadImage.load(..., LoadOptions)`‑t a `LoadOptions.setLoadMode(LoadMode.Stream)` beállítással, hogy elkerülje a teljes fájl memóriába töltését.

## Gyakran Ismételt Kérdések

**Q1: Használhatom a metrikus licencelést értékelési célokra?**  
A1: Igen, ingyenes próba licencet szerezhet [itt](https://releases.aspose.com/).

**Q2: Hol találhatók részletes dokumentációk az Aspose.CAD for Java-hoz?**  
A2: Tekintse meg a dokumentációt [itt](https://reference.aspose.com/cad/java/).

**Q3: Hogyan vásárolhatok licencet az Aspose.CAD for Java-hoz?**  
A3: Látogassa meg a vásárlási oldalt [itt](https://purchase.aspose.com/buy).

**Q4: Elérhető ideiglenes licenc opció?**  
A5: Igen, ideiglenes licenceket tekinthet meg [itt](https://purchase.aspose.com/temporary-license/).

**Q5: Közösségi támogatásra van szüksége vagy konkrét kérdései vannak?**  
A5: Látogassa meg az Aspose.CAD fórumot [itt](https://forum.aspose.com/c/cad/19).

**Q6: Működik a metrikus licencelés felhőalapú telepítésekkel?**  
A6: Absolút. A `setMeteredKey` hívás ugyanúgy működik Docker, Kubernetes vagy serverless környezetekben.

**Q7: Visszaállíthatom a fogyasztási számlálót?**  
A7: A számláló automatikusan visszaáll az új számlázási időszak elején; manuálisan nem állítható vissza.

## Következtetés

Gratulálunk! Sikeresen elsajátította a **metrikus licenc beállítását** az Aspose.CAD for Java-val. Az útmutató követésével beállította és zökkenőmentesen integrálta a metrikus licencelést Java projektjébe, biztosítva az Aspose.CAD képességek hatékony használatát, miközben a költségek átláthatóak maradnak.

---

**Last Updated:** 2026-05-25  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó oktatóanyagok

- [CAD konvertálása PDF-be az Aspose.CAD for Java segítségével – Teljes oktatóanyagok](/cad/java/)
- [PDF létrehozása CAD-ból – DXF exportálása PDF-be az Aspose.CAD for Java-val](/cad/java/additional-features/export-dxf-to-pdf/)
- [Vászonméret beállítása – Haladó CAD funkciók az Aspose.CAD for Java-val](/cad/java/advanced-cad-features/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}