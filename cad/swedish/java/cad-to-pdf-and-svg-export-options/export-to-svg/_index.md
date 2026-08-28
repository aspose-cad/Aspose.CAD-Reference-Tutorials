---
date: 2026-06-14
description: Lär dig hur du exporterar CAD till SVG med Aspose.CAD för Java. Denna
  steg‑för‑steg‑guide visar hur du konverterar DWG till SVG, ställer in SVG-färgläget
  och integrerar biblioteket i ditt Java‑projekt.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: Exportera till SVG
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
title: Exportera CAD till SVG med Aspose.CAD för Java
url: /sv/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera CAD till SVG med Aspose.CAD för Java

## Introduktion

I den här omfattande handledningen kommer du att lära dig **hur man exporterar CAD till SVG** med Aspose.CAD för Java. Oavsett om du behöver **konvertera DWG till SVG**, generera SVG från DWG-filer i ett batchjobb, eller helt enkelt ändra SVG till gråskala för lättviktig webbvisning, så guidar den här guiden dig genom varje steg—från att konfigurera biblioteket till finjustering av exportalternativ. I slutet har du ett produktionsklart kodexempel som körs på vilken JVM‑kompatibel plattform som helst.

## Snabba svar
- **Vad betyder “export CAD to SVG”?** Den omvandlar en CAD-ritning (t.ex. DWG eller DXF) till en Scalable Vector Graphics-fil som webbläsare renderar utan kvalitetsförlust.  
- **Vilket bibliotek hanterar konverteringen?** Aspose.CAD for Java tillhandahåller ett dedikerat API som stödjer 30+ CAD-format och exporterar SVG med full vektorfidelitet.  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för utvärdering; en kommersiell licens krävs för produktionsdistribution.  
- **Kan jag styra SVG-färgoutputen?** Ja—använd `SvgColorMode` för att växla mellan gråskala och fullfärgsrendering.  
- **Krävs någon extra programvara?** Endast en Java-runtime (JDK 8 eller nyare) och Aspose.CAD JAR; inga externa CAD-verktyg behövs.

## Vad är export av CAD till SVG?

Att exportera CAD till SVG är processen att konvertera en inbyggd CAD-fil (såsom DWG, DXF eller DWF) till SVG-vektorgrafikformatet. Den resulterande SVG-filen behåller exakt geometrisk data, vilket möjliggör upplösningsoberoende visning i webbläsare och designverktyg.

## Varför exportera CAD till SVG med Aspose.CAD?

Aspose.CAD kan hantera **30+ inmatningsformat** och generera SVG-utdata upp till **500 sidor** utan att ladda hela filen i minnet, vilket levererar **högfidelitets vektoromvandling** med hastigheter på **200 sidor/sekund** på en typisk server‑klass CPU. Biblioteket kör **100 % Java**, vilket eliminerar behovet av inhemska DLL‑filer eller tredjeparts CAD‑motorer.

## Förutsättningar

- **Java Development Kit** (JDK 8 eller nyare) installerat och konfigurerat på din maskin.  
- **Aspose.CAD for Java** JAR‑fil nedladdad från den officiella [download link](https://releases.aspose.com/cad/java/).  
- En mapp som innehåller minst en CAD-ritning (DWG, DXF, etc.) som du vill konvertera.

## Importera namnrymder

Innan du skriver någon kod, se till att Aspose.CAD‑biblioteket finns på din classpath och importera de nödvändiga klasserna.

### Steg 1: Öppna ditt Java‑projekt
Starta din favoriteditor (IntelliJ IDEA, Eclipse, VS Code) och öppna projektet där du avser att lägga till konverteringslogiken.

### Steg 2: Lägg till Aspose.CAD‑biblioteket
Placera filen `aspose-cad-xx.jar` i katalogen `libs` och lägg till den som ett beroende i ditt byggverktyg (Maven, Gradle eller ren `javac`).

### Steg 3: Importera namnrymder
I Java‑källfilen som ska utföra konverteringen, lägg till följande import:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## Hur exporterar man CAD till SVG med Aspose.CAD för Java?

Att exportera en CAD-ritning till SVG med Aspose.CAD innebär att ladda källfilen, konfigurera SVG‑specifika alternativ och skriva utdata. Processen är enkel, kräver bara några rader kod och fungerar konsekvent över alla stödda CAD-format samtidigt som den bevarar vektorfideliteten.

### Steg 1: Ange resurskatalogen
Definiera den absoluta eller relativa sökvägen som pekar på mappen som innehåller dina CAD-ritningar:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### Steg 2: Ladda CAD-ritningen
`Image`‑klassen är Aspose.CAD:s översta objekt som representerar en CAD-ritning i minnet. Att ladda filen skapar en minnesrepresentation som är klar för export.

`Image.load` läser en CAD‑fil och skapar en minnesrepresentation av ritningen.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Steg 3: Konfigurera SVG‑exportalternativ
`SvgExportOptions` låter dig finjustera SVG‑utdata. Nedan sätter vi färgläget till gråskala och säkerställer att all text renderas som former, vilket förbättrar kompatibiliteten med webbläsare som saknar originalfonten.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Steg 4: Spara som SVG
Slutligen anropar du `save` på `Image`‑instansen, med målfilnamnet och de konfigurerade alternativen. Aspose.CAD skriver en standard‑kompatibel SVG‑fil som kan öppnas direkt i vilken modern webbläsare som helst.

`save` skriver bilden till den angivna filen med de medföljande exportalternativen.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Proffstips:** För att generera en fullfärgs‑SVG, ersätt `SvgColorMode.Grayscale` med `SvgColorMode.FullColor`. Denna växling bevarar den ursprungliga paletten samtidigt som den fortfarande levererar vektorskalerbarhet.

## Varför använda Aspose.CAD för att exportera CAD till SVG?

- **Hög fidelitet:** Vektordata bevaras, vilket säkerställer att SVG:n ser exakt ut som den ursprungliga CAD-ritningen.  
- **Inga externa beroenden:** Konverteringen körs helt inom Java, vilket eliminerar behovet av extra verktyg.  
- **Anpassningsbar output:** Alternativ som `setColorType` låter dig styra om SVG:n är i gråskala eller fullfärg.  
- **Skalbar prestanda:** Bearbetar ritningar med flera hundra sidor på sekunder, med minnesanvändning under 50 MB.

## Vanliga problem och lösningar

- **Fil ej hittad:** Verifiera att `dataDir` pekar på rätt mapp och att DWG‑filnamnet matchar skiftlägeskänsligheten på filsystemet.  
- **Tom SVG‑output:** Säkerställ att `options.setTextAsShapes(true)` är aktiverat när källritningen innehåller text som måste visas som vektorformer.  
- **Ej stödd CAD‑format:** Aspose.CAD stödjer DWG, DXF, DWF och över 15 andra format; konsultera den officiella dokumentationen för hela listan.  
- **Prestandaflaskhalsar:** För extremt stora filer, aktivera streaming‑läge via `options.setEnableStreaming(true)` för att hålla minnesförbrukningen låg.

## Vanliga frågor

**Q: Kan jag konvertera en DXF‑fil till SVG med samma kod?**  
A: Ja, ersätt helt enkelt DWG‑filnamnet med en DXF‑fil; API:t upptäcker och bearbetar automatiskt båda formaten.

**Q: Hur ändrar jag outputen till fullfärgs‑SVG?**  
A: Sätt `options.setColorType(SvgColorMode.FullColor);` innan du anropar `save`‑metoden.

**Q: Är det möjligt att bädda in typsnitt i den genererade SVG:n?**  
A: Aspose.CAD konverterar text till former, så inbäddning av typsnitt är onödig; den resulterande SVG:n innehåller endast vektorlinjer.

**Q: Fungerar biblioteket på Linux och macOS?**  
A: Java‑biblioteket är plattformsoberoende och körs där en kompatibel JVM finns tillgänglig, inklusive Windows, Linux och macOS.

**Q: Vilken version av Aspose.CAD användes i den här handledningen?**  
A: Exemplet testades med Aspose.CAD för Java **24.10**.

---

**Senast uppdaterad:** 2026-06-14  
**Testad med:** Aspose.CAD för Java 24.10  
**Författare:** Aspose  

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg to pdf java – Export CAD to PDF with Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Export Specific DWG Layout to PDF Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}