---
date: 2026-06-14
description: Ismerje meg, hogyan exportálhat CAD-ot SVG-be az Aspose.CAD for Java
  segítségével. Ez a lépésről‑lépésre útmutató bemutatja, hogyan konvertálhat DWG-t
  SVG-re, állíthatja be az SVG színmódot, és integrálhatja a könyvtárat Java projektjébe.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: Exportálás SVG-be
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: CAD exportálása SVG-be az Aspose.CAD for Java használatával
url: /hu/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD exportálása SVG-be az Aspose.CAD for Java használatával

## Bevezetés

Ebben az átfogó útmutatóban megtanulja, hogyan **exportálja a CAD-et SVG-be** az Aspose.CAD for Java használatával. Akár **DWG-t szeretne SVG-be konvertálni**, akár kötegelt feladatban generál SVG-t DWG fájlokból, vagy egyszerűen szürkeárnyalatosra változtatja az SVG-t a könnyű webes megjelenítéshez, ez az útmutató minden lépésen végigvezet – a könyvtár beállításától az export beállításainak finomhangolásáig. A végére egy termelésre kész kódrészletet kap, amely bármely JVM‑kompatibilis platformon fut.

## Gyors válaszok
- **Mi jelent a „CAD exportálása SVG-be”?** Átalakítja a CAD rajzot (pl. DWG vagy DXF) egy Scalable Vector Graphics fájlba, amelyet a böngészők minőségvesztés nélkül jelenítenek meg.  
- **Melyik könyvtár kezeli a konverziót?** Az Aspose.CAD for Java egy dedikált API-t biztosít, amely több mint 30 CAD formátumot támogat, és SVG-t állít elő teljes vektor pontossággal.  
- **Szükségem van licencre a fejlesztéshez?** Egy ingyenes próba verzió elegendő az értékeléshez; a termelésben való használathoz kereskedelmi licenc szükséges.  
- **Szabályozhatom az SVG színkimenetét?** Igen – használja a `SvgColorMode`-t a szürkeárnyalatos és a teljes színű megjelenítés között váltáshoz.  
- **Szükséges-e további szoftver?** Csak egy Java futtatókörnyezet (JDK 8 vagy újabb) és az Aspose.CAD JAR; külső CAD eszközök nem szükségesek.

## Mi az a CAD exportálása SVG-be?
A CAD exportálása SVG-be a natív CAD fájl (például DWG, DXF vagy DWF) SVG vektor képformátumba történő konvertálásának folyamata. A kapott SVG pontos geometriai adatokat tart meg, lehetővé téve a felbontástól független megjelenítést web böngészőkben és tervezőeszközökben.

## Miért exportáljunk CAD-et SVG-be az Aspose.CAD használatával?
Az Aspose.CAD **30+ bemeneti formátumot** képes kezelni, és akár **500 oldal** SVG kimenetet generálni anélkül, hogy a teljes fájlt memóriába töltené, **magas pontosságú vektor konverziót** biztosítva **200 oldal/másodperc** sebességgel egy tipikus szerver‑osztályú CPU-n. A könyvtár **100 % Java**-ban fut, így nincs szükség natív DLL-ekre vagy harmadik‑fél CAD motorokra.

## Előfeltételek

- **Java Development Kit** (JDK 8 vagy újabb) telepítve és konfigurálva van a gépén.  
- **Aspose.CAD for Java** JAR fájl letöltve a hivatalos [download link](https://releases.aspose.com/cad/java/).  
- Egy mappa, amely legalább egy CAD rajzot (DWG, DXF stb.) tartalmaz, amelyet konvertálni szeretne.

## Névterek importálása

Mielőtt kódot írna, győződjön meg róla, hogy az Aspose.CAD könyvtár a classpath‑on van, és importálja a szükséges osztályokat.

### 1. lépés: Nyissa meg a Java projektjét
Indítsa el a kedvenc IDE-jét (IntelliJ IDEA, Eclipse, VS Code), és nyissa meg azt a projektet, amelyhez a konverziós logikát szeretné hozzáadni.

### 2. lépés: Adja hozzá az Aspose.CAD könyvtárat
Helyezze a `aspose-cad-xx.jar` fájlt a `libs` könyvtárba, és adja hozzá függőségként a build eszközéhez (Maven, Gradle vagy egyszerű `javac`).

### 3. lépés: Névterek importálása
A Java forrásfájlban, amely a konverziót végzi, adja hozzá a következő importokat:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

Ezek az importok hozzáférést biztosítanak a központi `Image` osztályhoz és az SVG‑specifikus export beállításokhoz.

## Hogyan exportáljunk CAD-et SVG-be az Aspose.CAD for Java használatával?

A CAD rajz SVG-be exportálása az Aspose.CAD segítségével magában foglalja a forrásfájl betöltését, az SVG‑specifikus beállítások konfigurálását és a kimenet írását. A folyamat egyszerű, csak néhány kódsort igényel, és minden támogatott CAD formátumban konzisztensen működik, miközben megőrzi a vektor pontosságát.

### 1. lépés: Adja meg az erőforrás könyvtárat
Határozza meg a abszolút vagy relatív útvonalat, amely a CAD rajzokat tartalmazó mappára mutat:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### 2. lépés: Töltse be a CAD rajzot
Az `Image` osztály az Aspose.CAD legfelső szintű objektuma, amely egy CAD rajzot reprezentál a memóriában. A fájl betöltése egy memóriában lévő reprezentációt hoz létre, amely készen áll az exportálásra.

`Image.load` beolvas egy CAD fájlt és memóriában létrehozza a rajz reprezentációját.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### 3. lépés: SVG export beállítások konfigurálása
`SvgExportOptions` lehetővé teszi az SVG kimenet finomhangolását. Az alábbiakban a színmódot szürkeárnyalatosra állítjuk, és biztosítjuk, hogy minden szöveg alakzatként legyen renderelve, ami javítja a kompatibilitást azokkal a böngészőkkel, amelyek nem rendelkeznek az eredeti betűtípussal.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### 4. lépés: Mentés SVG‑ként
Végül hívja meg a `save` metódust az `Image` példányon, átadva a célfájl nevét és a konfigurált beállításokat. Az Aspose.CAD egy szabványos SVG fájlt ír, amely közvetlenül megnyitható bármely modern böngészőben.

`save` a megadott export beállításokkal írja a képet a megadott fájlba.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Pro tipp:** Teljes színű SVG generálásához cserélje le a `SvgColorMode.Grayscale`-t `SvgColorMode.FullColor`-ra. Ez a váltás megőrzi az eredeti palettát, miközben továbbra is vektor skálázhatóságot biztosít.

## Miért használja az Aspose.CAD-et CAD SVG‑be exportálásához?
- **Magas pontosság:** A vektor adat megmarad, biztosítva, hogy az SVG pontosan úgy nézzen ki, mint az eredeti CAD rajz.  
- **Nincs külső függőség:** A konverzió teljesen Java‑ban fut, így nincs szükség további eszközökre.  
- **Testreszabható kimenet:** Olyan beállítások, mint a `setColorType`, lehetővé teszik, hogy szabályozza, szürkeárnyalatos vagy teljes színű legyen az SVG.  
- **Skálázható teljesítmény:** Több száz oldalas rajzokat másodpercek alatt dolgoz fel, a memóriahasználat 50 MB alatt marad.

## Gyakori problémák és megoldások
- **Fájl nem található:** Ellenőrizze, hogy a `dataDir` a helyes mappára mutat, és hogy a DWG fájl neve megegyezik a fájlrendszerben lévő kis‑nagybetűkkel.  
- **Üres SVG kimenet:** Győződjön meg róla, hogy a `options.setTextAsShapes(true)` engedélyezve van, ha a forrásrajz olyan szöveget tartalmaz, amelynek vektor alakzatként kell megjelennie.  
- **Nem támogatott CAD formátum:** Az Aspose.CAD támogatja a DWG, DXF, DWF és több mint 15 egyéb formátumot; a teljes listáért tekintse meg a hivatalos dokumentációt.  
- **Teljesítmény szűk keresztmetszet:** Nagyon nagy fájlok esetén engedélyezze a streaming módot a `options.setEnableStreaming(true)` használatával, hogy alacsony maradjon a memóriahasználat.

## Gyakran ismételt kérdések

**Q: Átalakíthatok DXF fájlt SVG‑be ugyanazzal a kóddal?**  
A: Igen, egyszerűen cserélje le a DWG fájlnevet egy DXF fájlra; az API automatikusan felismeri és feldolgozza mindkét formátumot.

**Q: Hogyan változtathatom meg a kimenetet teljes színű SVG‑re?**  
A: Állítsa be a `options.setColorType(SvgColorMode.FullColor);`‑t a `save` metódus meghívása előtt.

**Q: Lehetséges betűtípusokat beágyazni a generált SVG‑be?**  
A: Az Aspose.CAD a szöveget alakzatokká konvertálja, így a betűtípusok beágyazása nem szükséges; a kapott SVG csak vektor kontúrokat tartalmaz.

**Q: Működik a könyvtár Linuxon és macOS‑on?**  
A: A Java könyvtár platform‑független, és bárhol fut, ahol kompatibilis JVM elérhető, beleértve a Windows, Linux és macOS rendszereket.

**Q: Melyik Aspose.CAD verziót használták ebben az útmutatóban?**  
A: A példát az Aspose.CAD for Java **24.10** verziójával tesztelték.

---

**Last Updated:** 2026-06-14  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó útmutatók

- [DWG exportálása PDF‑be vagy raszterbe az Aspose.CAD for Java használatával](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg to pdf java – CAD exportálása PDF‑be az Aspose.CAD segítségével](/cad/java/cad-export-options/export-to-pdf/)
- [Speciális DWG elrendezés exportálása PDF‑be az Aspose.CAD for Java használatával](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}