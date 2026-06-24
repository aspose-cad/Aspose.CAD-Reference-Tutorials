---
date: 2026-06-19
description: Tanulja meg, hogyan állíthat be időkorlátot a CAD rajzok mentésekor az
  Aspose.CAD for Java használatával. Növelje a teljesítményt, kerülje el a lefagyásokat,
  és exportálja a CAD-et PDF-be hatékonyan.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: Időkorlát beállítása mentéskor
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Hogyan állítsunk be időkorlátot a CAD mentésére az Aspose.CAD használatával
url: /hu/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan állítsunk be időkorlátot a CAD mentésénél az Aspose.CAD használatával

## Bevezetés

Ebben az átfogó útmutatóban megtanulja, **hogyan állítsa be az időkorlátot** a CAD rajzok mentésekor az Aspose.CAD for Java használatával. Az időkorlát alkalmazása megakadályozza, hogy a hosszú ideig futó mentési műveletek lefagyassák az alkalmazást, ami különösen fontos, ha **CAD-et PDF-be kell exportálni** vagy **DWG-t PDF-be konvertálni** kötegelt feldolgozási helyzetekben. Az Aspose.CAD for Java több mint 50 CAD formátumot támogat, és több száz oldalas fájlokat is kezelhet anélkül, hogy a teljes dokumentumot a memóriába töltené, így kiszámítható teljesítményt és erőforrás-felhasználást biztosít.

## Gyors válaszok
- **Mi a timeout funkciója?** Leállítja a mentési műveletet egy meghatározott idő után, felszabadítja a szálat és megakadályozza az erőforrás-szivárgásokat.  
- **Melyik osztály vezérli az időkorlátot?** `InterruptionTokenSource` biztosítja a mentési rutin által használt megszakítási tokent.  
- **Exportálhatok még CAD-et PDF-be időkorlát után?** Igen – elkapja a megszakítási kivételt, és újrapróbálkozhat vagy naplózhatja a hibát.  
- **Szükségem van speciális licencre?** Egy szabályos Aspose.CAD licenc elegendő; az időkorlát funkció beépített.  
- **Ez a megközelítés szálbiztos?** Igen, ha minden mentés saját szálban fut saját tokennel.

## Mi az időkorlát a CAD mentési műveletekben?

Az időkorlát egy konfigurálható időkorlát, amely túllépése esetén leállítja a mentési folyamatot, és megszakítási kivételt dob. Ez megvédi a Java alkalmazását a bonyolult rajzok vagy I/O szűk keresztmetszetek által okozott végtelen függéstől.

## Miért állítsunk be időkorlátot CAD fájlok mentésekor?

Az Aspose.CAD **DWG-t PDF-be konvertál** és **CAD-et PDF-be exportál** tipikus rajzok esetén egy másodpercnél gyorsabban, de rendkívül nagy vagy sérült fájlok perceket vehetnek igénybe. Időkorlát meghatározásával garantálja, hogy egyetlen mentés sem haladja meg például a 30 másodpercet, ezáltal stabil marad a kötegelt feldolgozás áteresztőképessége, és elkerülhető a szálak elnyomása.

## Előfeltételek

Az útmutatóba merülés előtt győződjön meg arról, hogy a következő előfeltételek rendelkezésre állnak:
- **Aspose.CAD for Java Library** – Győződjön meg arról, hogy az Aspose.CAD for Java könyvtár be van integrálva a projektjébe. A könyvtárat letöltheti a [website](https://releases.aspose.com/cad/java/) oldalról.
- **Fejlesztői környezet** – Állítsa be a Java fejlesztői környezetét a szükséges eszközökkel és függőségekkel.

## Csomagok importálása

A kezdéshez importálja a szükséges csomagokat a Java projektjébe. Adja hozzá a következő sorokat a Java fájl elejéhez:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Most bontsuk le a példakódot lépésről‑lépésre útmutatóvá:

## Hogyan állítsuk be az időkorlátot a CAD rajzok mentésekor?

Töltse be a CAD fájlt, hozzon létre egy `InterruptionTokenSource`-t a kívánt időkorláttal, és adja át a tokent a PDF mentési beállításoknak. Ha a művelet meghaladja az időkorlátot, az Aspose.CAD `OperationCanceledException`-t dob, amelyet elkapva elegánsan kezelheti a hibát.

### 1. lépés: Forrás- és kimeneti könyvtárak beállítása

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Győződjön meg arról, hogy a CAD rajzokhoz a megfelelő forrás- és kimeneti könyvtárak vannak beállítva.

### 2. lépés: Interruption Token Source létrehozása

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Inicializáljon egy megszakítási token forrást a mentési művelet közbeni megszakítások kezeléséhez.

### 3. lépés: CAD rajz betöltése

A `CadImage` osztály az Aspose.CAD központi objektuma, amely a CAD rajzot memóriában képviseli, és metódusokat biztosít a rendereléshez és konverzióhoz.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### 4. lépés: Rasterizálási beállítások konfigurálása

`CadRasterizationOptions` határozza meg, hogyan kerül rasterizálásra a CAD rajz képpé.

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Állítsa be a rasterizálási opciókat a CAD rajzhoz.

### 5. lépés: PDF beállítások konfigurálása

`PdfOptions` meghatározza a CAD rajz PDF dokumentumként való mentésének beállításait.

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Állítsa be a PDF opciókat vektor rasterizálási beállításokkal és a megszakítási tokennel.

### 6. lépés: Rajz mentése időkorláttal

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Mentse a CAD rajzot PDF fájlba a megadott időkorláttal.

### 7. lépés: Megszakítás kezelése

`OperationCanceledException` akkor kerül dobásra, amikor egy mentési művelet meghaladja a megadott időkorlátot.

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Hozzon létre egy szálat a mentési művelet kezelésére, és szakítsa meg a megadott időkorlát után.

## Gyakori problémák és megoldások

- **Az időkorlát túl rövid** – Ha gyakori megszakításokat kap, növelje az időkorlát értékét a nagyobb rajzok befogadásához.  
- **InterruptedException nincs elkapva** – Mindig tegye a mentési hívást egy try‑catch blokkba `OperationCanceledException`-ra, hogy megakadályozza az alkalmazás összeomlását.  
- **Memóriahasználat** – Használja a `PdfOptions.setVectorRasterizationOptions`-t a kimenet streameléséhez ahelyett, hogy a teljes fájlt a memóriába töltené.

## Gyakran Ismételt Kérdések

**Q: Használhatom ezt a funkciót DWG‑t PDF‑be konvertálásra kötegelt feladatban?**  
A: Igen, csomagolja minden konverziót saját szálba külön megszakítási tokennel, hogy per‑fájl időkorlátot érvényesítsen.

**Q: Működik az időkorlát minden kimeneti formátumnál?**  
A: Az időkorlát mechanizmus a `InterruptionTokenSource`-hez kapcsolódik, és minden olyan formátummal működik, amely tiszteletben tartja a tokent, beleértve a PDF, PNG és SVG formátumokat.

**Q: Mi történik a részben írt fájlokkal időkorlát után?**  
A: Az Aspose.CAD automatikusan eldobja a befejezetlen kimenetet, így nem maradnak sérült PDF‑ek.

**Q: Szükséges licenc a termeléshez?**  
A: Igen, egy érvényes Aspose.CAD licenc szükséges a kereskedelmi telepítésekhez; ingyenes próba elérhető értékeléshez.

**Q: Hol találok további példákat a megszakítási tokenek használatára?**  
A: Az hivatalos Aspose.CAD dokumentáció további kódrészleteket és legjobb gyakorlatokat tartalmaz.

## További források

- [kiadási oldal](https://releases.aspose.com/cad/java/) – Közvetlen letöltési oldal a legújabb Aspose.CAD for Java kiadásokhoz.  
- [dokumentáció](https://reference.aspose.com/cad/java/) – Teljes API referencia és fejlesztői útmutatók.  
- [ez a link](https://releases.aspose.com/) – Általános Aspose termékkiadások.  
- [itt](https://purchase.aspose.com/temporary-license/) – Ideiglenes licenc beszerzése teszteléshez.  
- [Aspose.CAD fórum](https://forum.aspose.com/c/cad/19) – Közösségi támogatás és beszélgetések.

## Összegzés

Most már elsajátította, **hogyan állítsa be az időkorlátot** a CAD rajzok mentéséhez az Aspose.CAD for Java használatával. Az `InterruptionTokenSource` beépítésével a munkafolyamatba megbízhatóan **exportálhat CAD-et PDF-be** vagy **DWG‑t PDF‑be konvertálhat** anélkül, hogy hosszú ideig tartó függéseket kockáztatna, így alkalmazása reagáló és skálázható marad.

---

**Utolsó frissítés:** 2026-06-19  
**Tesztelve ezzel:** Aspose.CAD for Java 24.12  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó oktatóanyagok

- [DWG exportálása PDF-be vagy raszterként az Aspose.CAD for Java használatával](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Specifikus DWG elrendezés exportálása PDF-be az Aspose.CAD for Java használatával](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [DWG konvertálása PNG-re és más raszter formátumokra az Aspose.CAD for Java használatával](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}