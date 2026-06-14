---
date: 2026-06-14
description: Ismerje meg, hogyan exportálhatja a CAD‑t PDF‑be, és konvertálhatja a
  DGN‑t PDF‑be az Aspose.CAD for Java használatával. Lépésről‑lépésre útmutató Java
  fejlesztőknek.
keywords:
- export cad to pdf
- convert dwg to pdf
- convert dgn to pdf
- java convert cad pdf
- batch convert dgn pdf
linktitle: Beágyazott DGN exportálása
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  headline: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  name: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  steps:
  - name: Set Up Input and Output Paths
    text: Define the directory that contains your source file and specify the DWG
      that holds the embedded DGN.
  - name: Load DWG File
    text: '`Image` loads the DWG and automatically detects any embedded DGN data,
      exposing it for further processing.'
  - name: Configure Rasterization Options
    text: Select which layout(s) you want to include in the PDF. In this example we
      export only the **Model** layout, which is the most common view for engineering
      drawings.
  - name: Configure PDF Options
    text: Attach the rasterization settings to the PDF export options so that the
      final document respects the chosen layout and DPI.
  - name: Save PDF File
    text: Finally, write the PDF to disk using the configured options. The `save`
      method writes the configured image to the target file format on disk.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java is a commercial library. You can obtain a license
      from [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Yes, you can access a free trial of Aspose.CAD for Java [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: You can seek support from the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: What if I need a temporary license?
  - answer: The documentation is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the official documentation?
  type: FAQPage
second_title: Aspose.CAD Java API
title: CAD exportálása PDF‑be – Beágyazott DGN exportálása az Aspose.CAD for Java
  segítségével
url: /hu/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD exportálása PDF-be – Beágyazott DGN exportálása az Aspose.CAD for Java-val

## Bevezetés

Ebben az útmutatóban megtudja, **hogyan exportálja a CAD-et PDF-be**, egy beágyazott DGN fájl átalakításával egy magas minőségű PDF dokumentummá az Aspose.CAD for Java segítségével. Az Aspose.CAD egy robusztus könyvtár, amely a Java fejlesztőknek teljes irányítást ad a CAD fájlok manipulálásához, legyen szó **DGN PDF‑be konvertálásáról**, **DWG PDF‑be konvertálásáról**, vagy egyszerűen a CAD rajzok más formátumokba való rendereléséről. Kövesse az alábbi lépésről‑lépésre útmutatót, és perceken belül be tudja integrálni ezt a funkciót alkalmazásaiba.

## Gyors válaszok

- **Mit jelent a “CAD exportálása PDF-be”?** Átalakítja a CAD rajzokat (DWG, DGN stb.) PDF fájlokká, miközben megőrzi a vektor minőséget.  
- **Melyik könyvtárat használják?** Aspose.CAD for Java.  
- **Szükségem van licencre?** Licenc szükséges a termeléshez; ingyenes próbaverzió elérhető.  
- **Mik a fő előfeltételek?** Java fejlesztői környezet és az Aspose.CAD for Java JAR.  
- **Testreszabhatom a kimenetet?** Igen – kiválaszthatja a layoutokat, beállíthatja a rasterizálási opciókat, és vezérelheti a PDF beállításokat.

## Mi az a “CAD exportálása PDF-be”?

A CAD PDF‑be exportálása egy natív CAD rajzot (DWG, DGN stb.) PDF fájlra alakít át, amely megőrzi az eredeti vektor geometriát, rétegeket és elrendezést, lehetővé téve bárki számára a tervezés megtekintését, nyomtatását vagy megosztását CAD szoftver nélkül. Ez az átalakítás platform‑független dokumentumot hoz létre, amely bármely nagyítási szinten azonosul, így ideális az együttműködéshez és archiváláshoz.

## Miért használja az Aspose.CAD for Java-t a DGN PDF‑be konvertálásához?

Az Aspose.CAD for Java tiszta Java megoldást kínál, amely megszünteti a külső CAD eszközök szükségességét, biztosítja a vektorok pontos hűségét a létrehozott PDF‑ekben, és kiterjedt konfigurációs lehetőségeket nyújt, mint például a layout kiválasztása, DPI vezérlés és betűtípus beágyazás, így ideális egyszerű és vállalati szintű konverziós feladatokhoz.

- **Nincs külső függőség** – tisztán Java‑ban működik bármely operációs rendszeren.  
- **Megőrzi a vektor adatokat** – a PDF‑ek bármely nagyítási szinten élesek maradnak.  
- **Finomhangolt vezérlés** – válasszon konkrét layoutokat, állítsa be a rasterizálási DPI‑t, és ágyazza be a betűtípusokat.  
- **Vállalati szintű** – támogatja a **2 GB**‑ig terjedő fájlokat, ezrek rajzainak kötegelt feldolgozását, és rugalmas licencelést.  

## Előfeltételek

Mielőtt belemerülnénk, győződjön meg róla, hogy a következőkkel rendelkezik:

- **Java fejlesztői környezet** – JDK 8 vagy újabb telepítve és konfigurálva.  
- **Aspose.CAD for Java** – töltse le a legújabb JAR‑t innen: [here](https://releases.aspose.com/cad/java/).  

## Csomagok importálása

A `import` utasítások a szükséges Aspose.CAD osztályokat hozzák be a láthatóságba. Az `Image` a központi osztály, amely bármely rasterizálható CAD fájlt képvisel, míg a `PdfOptions` és a `RasterizationOptions` lehetővé teszi a PDF kimenet finomhangolását. A `CadRasterizationOptions` rasterizálási paramétereket ad meg, mint például DPI, oldalméret és layout a CAD rendereléshez.

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Hogyan exportáljunk CAD-et PDF-be az Aspose.CAD for Java használatával?

A folyamat a beágyazott DGN‑t tartalmazó DWG fájl betöltésével kezdődik, majd a rasterizálási paraméterek beállításával, amelyek meghatározzák a kimeneti felbontást és layoutot, ezeket a paramétereket egy PdfOptions objektumhoz csatoljuk, végül a save metódus meghívásával generáljuk a PDF‑et. Ez a megközelítés magas minőségű, vektor‑megőrző eredményeket biztosít minimális kóddal.

Az alábbiakban egy világos, számozott lépésről‑lépésre útmutató látható, amely pontosan bemutatja, hogyan konvertáljunk egy beágyazott DGN fájlt (egy DWG‑ben tárolt) PDF‑be.

### 1. lépés: Bemeneti és kimeneti útvonalak beállítása

Adja meg azt a könyvtárat, amely a forrásfájlt tartalmazza, és határozza meg a beágyazott DGN‑t tartalmazó DWG‑t.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### 2. lépés: DWG fájl betöltése

Az `Image` betölti a DWG‑t, és automatikusan észleli a beágyazott DGN adatokat, amelyek további feldolgozásra elérhetők.

```java
Image objImage = Image.load(fileName);
```

### 3. lépés: Rasterizálási beállítások konfigurálása

Válassza ki, melyik layout(okat) szeretné a PDF‑be belefoglalni. Ebben a példában csak a **Model** layoutot exportáljuk, amely a mérnöki rajzok leggyakoribb nézete.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### 4. lépés: PDF beállítások konfigurálása

Csatolja a rasterizálási beállításokat a PDF export opciókhoz, hogy a végső dokumentum tiszteletben tartsa a kiválasztott layoutot és DPI‑t.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 5. lépés: PDF fájl mentése

Végül írja a PDF‑et a lemezre a konfigurált opciók használatával. A `save` metódus a konfigurált képet a cél fájlformátumba írja a lemezen.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## DWG PDF‑be konvertálása – egy további tipp

Ha a forrásfájl egy egyszerű DWG (beágyazott DGN nélkül), ugyanazt a kódot újra felhasználhatja – egyszerűen módosítsa a `fileName`‑t, hogy a konvertálni kívánt DWG‑re mutasson. A rasterizálási és PDF opciók változatlanok maradnak, így egy konzisztens **DWG PDF‑be konvertálás** munkafolyamatot kap.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| **Üres PDF kimenet** | Layout név eltérés | Ellenőrizze, hogy a `setLayouts`‑nek átadott layout név pontosan megegyezik-e a forrásfájlban lévő layout nevével (kis‑nagybetű érzékeny). |
| **Licenc kivétel** | Próbaverzió használata licenc nélkül | Alkalmazzon érvényes Aspose.CAD licencet a kép betöltése előtt (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Fájl nem található** | Helytelen `dataDir` útvonal | Használjon abszolút útvonalat vagy győződjön meg róla, hogy a relatív útvonal helyes a projekt munkakönyvtárához képest. |
| **Alacsony felbontású grafika** | Alapértelmezett rasterizálási DPI alacsony | Állítsa be a `rasterizationOptions.setResolution(300)`‑t vagy módosítsa a `setPageWidth/Height`‑t a DPI növeléséhez. |

## Gyakran Ismételt Kérdések

**Q: Használhatom az Aspose.CAD for Java-t kereskedelmi projektben?**  
A: Igen, az Aspose.CAD for Java egy kereskedelmi könyvtár. Licencet szerezhet [itt](https://purchase.aspose.com/buy).

**Q: Elérhető ingyenes próbaverzió?**  
A: Igen, ingyenes próbaverziót érhet el az Aspose.CAD for Java-hoz [itt](https://releases.aspose.com/).

**Q: Hogyan kaphatok támogatást az Aspose.CAD for Java-hoz?**  
A: Támogatást kérhet az Aspose.CAD közösségtől a [fórumon](https://forum.aspose.com/c/cad/19).

**Q: Mit tehetek, ha ideiglenes licencre van szükségem?**  
A: Ideiglenes licencet szerezhet [itt](https://purchase.aspose.com/temporary-license/).

**Q: Hol találom a hivatalos dokumentációt?**  
A: A dokumentáció elérhető [itt](https://reference.aspose.com/cad/java/).

## Összegzés

Most már megtanulta, hogyan **exportálja a CAD-et PDF-be**, különösen hogyan **konvertálja a DGN‑t PDF‑be**, és akár **DWG‑t PDF‑be** az Aspose.CAD for Java használatával. A fenti lépések követésével beépítheti a zökkenőmentes CAD‑PDF konverziót bármely Java‑alapú megoldásba, magas minőségű PDF‑eket biztosítva felhasználóinak további CAD szoftver nélkül.

---

**Legutóbb frissítve:** 2026-06-14  
**Tesztelt verzió:** Aspose.CAD for Java 24.12  
**Szerző:** Aspose

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó útmutatók

- [DGN exportálása DWG‑be az Aspose.CAD for Java‑val – Útmutató](/cad/java/dgn-export-options/)
- [Könnyed DGN‑ből AutoCAD PDF exportálás az Aspose.CAD for Java‑val](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [dwg to pdf java – CAD exportálása PDF‑be az Aspose.CAD‑dal](/cad/java/cad-export-options/export-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}