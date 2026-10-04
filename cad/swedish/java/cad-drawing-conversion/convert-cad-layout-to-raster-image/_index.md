---
date: 2026-10-04
description: Lär dig hur du snabbt konverterar DWG till PNG och exporterar CAD som
  PNG eller andra rasterformat med Aspose.CAD for Java. Få högkvalitativa resultat
  snabbt.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: Konvertera CAD-layout till rasterbildformat
og_description: Konvertera DWG till PNG snabbt med Aspose.CAD for Java. Lär dig steg‑för‑steg
  hur du exporterar CAD som PNG, JPEG, TIFF och mer.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Konvertera DWG till PNG och andra rasterformat med Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Konvertera DWG till PNG och andra rasterformat med Aspose.CAD for Java
url: /sv/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera DWG till PNG och andra rasterformat med Aspose.CAD för Java

## Introduktion

`Aspose.CAD for Java` är ett bibliotek som möjliggör programmatisk konvertering av CAD‑filer till rasterbilder såsom PNG, JPEG och TIFF. Att konvertera DWG till PNG (eller andra rasterbildformat) är ett vanligt krav när du behöver dela CAD‑ritningar med teammedlemmar som inte har en CAD‑visare, bädda in designer i dokumentation eller generera miniatyrbilder för webb­gallerier. I den här guiden lär du dig hur du konverterar dwg till png snabbt och pålitligt, oavsett om du arbetar med en fullständig ritningsfil eller bara ett specifikt layout. Du kan också behöva **konvertera CAD till raster** för webb‑förhandsvisningar, rapportverktyg eller mobilappar.

## Snabba svar
- **Vilket bibliotek hanterar DWG till PNG?** Aspose.CAD for Java tillhandahåller konverteringsmotorn.  
- **Vilka rasterformat kan jag exportera?** PNG, JPEG, TIFF, PDF, BMP och mer än 30 ytterligare format.  
- **Behöver jag en licens för testning?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Kan jag välja en specifik layout?** Ja – använd `setLayouts` för att rikta in dig på “Model”, “Layout1” osv.  
- **Är högupplöst output möjlig?** Absolut – justera `setPageWidth` och `setPageHeight` (eller `setResolution`) för att kontrollera DPI.

## Vad är “convert dwg to png”?

Att konvertera dwg till png innebär att omvandla en DWG‑vektorritning till en pixelbaserad PNG‑bild som kan visas av vilken standard bildvisare som helst. Denna process rasteriserar vektorelement, bevarar linjebredd, färger och lager samtidigt som de översätts till en bitmap med fast upplösning. Resultatet är idealiskt för inbäddning i PDF‑filer, Word‑dokument eller webbsidor där vektorsupport är begränsad.

## Varför exportera CAD som PNG (eller andra rasterformat)?

Att exportera CAD som PNG ger dig universell kompatibilitet, snabb laddning och enkel inbäddning på alla större plattformar. Rasterbilder laddas omedelbart jämfört med att öppna en tung DWG‑fil, och PNG:s förlustfria kompression säkerställer visuell trohet. Genom att kontrollera upplösning, bakgrundsfärg och layout garanterar du att alla intressenter ser samma utseende, oavsett om filen visas på en stationär dator, mobil enhet eller i en webbläsare.

## Vanliga användningsområden

| Scenario | Varför rasteroutput hjälper |
|----------|------------------------------|
| **Projekt-dokumentation** | Att bädda in PNG‑filer i PDF‑ eller Word‑dokument undviker att granskare måste ha CAD‑programvara. |
| **Webbportaler** | Miniatyrbilder genererade från DWG‑filer laddas omedelbart och förbättrar användarupplevelsen. |
| **Mobilappar** | Rasterbilder visas korrekt på enheter som saknar CAD‑visare. |
| **Automatiserad rapportering** | Batch‑konvertera flera layouter till PNG/JPEG för inkludering i diagram eller instrumentpaneler. |

## Förutsättningar

Innan du börjar, se till att du har:

1. **Java‑utvecklingsmiljö** – JDK 8 eller nyare installerad och konfigurerad.  
2. **Aspose.CAD for Java** – Ladda ner den senaste JAR‑filen från [Aspose.CAD for Java-dokumentationen](https://reference.aspose.com/cad/java/).  

## Importera namnrymder

`com.aspose.cad.Image` är kärnklassen som representerar någon CAD‑fil i minnet. `com.aspose.cad.imageoptions.*` tillhandahåller alternativobjekt för varje rasterformat. Importera de klasser du behöver för att läsa in en ritning, konfigurera rasterisering och spara resultatet.

> **Proffstips:** Om du planerar att **exportera CAD som PNG** istället för TIFF, ersätt `TiffOptions` med `PngOptions` (finns i `com.aspose.cad.imageoptions.PngOptions`).

## Steg‑för‑steg‑guide

### Steg 1: konfigurera resurskatalogen

Byt ut `"Your Document Directory"` mot den absoluta sökvägen där dina CAD‑filer finns. Denna katalog kommer att användas för både in‑ och utdatafiler.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Steg 2: läs in CAD‑filen

`Image.load` analyserar källfilen och skapar en minnesrepresentation som du kan rasterisera. Du kan läsa in vilket stödformat som helst (DWG, DXF, DGN, osv.) – detta är delen **hur man konverterar cad**.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Steg 3: konfigurera rasteriseringsalternativ

`CadRasterizationOptions` definierar hur vektordatan omvandlas till pixlar. `setPageWidth` och `setPageHeight` styr utdataupplösning (större värden = högre DPI). `setLayouts` låter dig **konvertera CAD till raster** för specifika layouter; utelämna den för att rasterisera hela ritningen.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Steg 4: ange bildalternativ

`TiffOptions` (eller `PngOptions` för PNG) talar om för Aspose vilket rasterformat som ska genereras och låter dig finjustera kompression, färgdjup och andra format‑specifika inställningar. Välj den alternativklass som matchar ditt önskade resultat.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Steg 5: spara den resulterande bilden

Anropa `save` på `Image`‑instansen och skicka med utskriftsfilens namn samt alternativobjektet. Ändra filändelsen till `.png` (och använd `PngOptions`) för att **spara CAD som PNG**. Samma mönster fungerar för JPEG, BMP eller PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Vanligt fallgropp:** Att glömma att matcha filändelsen med alternativklassen kommer att orsaka ett `UnsupportedFormatException`. Se alltid till att de är synkroniserade.

## Vanliga problem och lösningar

| Issue | Solution |
|-------|----------|
| **Tom bild** | Verifiera att layoutnamnen i `setLayouts` exakt matchar dem i käll‑CAD‑filen. |
| **Lågupplöst PNG** | Öka `setPageWidth` / `setPageHeight` eller sätt `setResolution` på rasteriseringsalternativen. |
| **Ej stöd för DWG‑version** | Säkerställ att du använder den senaste versionen av Aspose.CAD; äldre versioner kanske inte stödjer nyare DWG‑utgåvor. |
| **Minnesfel på stora filer** | Bearbeta sidor en åt gången eller öka JVM‑heapen (`-Xmx2g`). |

## Vanliga frågor

**Q: Är Aspose.CAD kompatibel med olika CAD‑filformat?**  
A: Ja, det stödjer över 30 CAD‑ och rasterformat, inklusive DWG, DXF, DGN och SVG.

**Q: Kan jag anpassa upplösningen på den resulterande rasterbilden?**  
A: Absolut. Justera `setPageWidth`, `setPageHeight` eller `setResolution` i `CadRasterizationOptions` för att uppnå önskad DPI.

**Q: Hur kan jag konvertera flera CAD‑layouter i ett enda körning?**  
A: Tillhandahåll en array med alla layoutnamn till `setLayouts`, t.ex. `new String[]{"Model","Layout1","Layout2"}`.

**Q: Finns det andra utdataformat än TIFF som stöds?**  
A: Ja—PNG, JPEG, BMP, PDF och fler finns tillgängliga via deras respektive `*Options`‑klasser.

**Q: Var kan jag få hjälp eller dela min erfarenhet med Aspose.CAD?**  
A: Besök [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19) för community‑stöd och officiell assistans.

## Slutsats

Genom att följa dessa steg kan du **konvertera DWG till PNG**, **exportera CAD som PNG**, **spara CAD som JPEG**, eller generera vilket annat rasterformat du behöver. Aspose.CAD for Java sköter det tunga arbetet, så att du kan fokusera på att integrera högkvalitativa bilder i dina applikationer, dokumentation eller webbportaler. Bibliotekets stöd för över 30 format och dess förmåga att rendera ritningar med hundratals sidor utan att ladda in hela filen i minnet gör det till ett robust val för företagsklassad CAD‑rasterisering.

---

**Senast uppdaterad:** 2026-10-04  
**Testat med:** Aspose.CAD for Java 24.12  
**Författare:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Relaterade handledningar

- [Exportera snabbt DWG till PDF eller raster med java cad-biblioteket Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Konvertera DWG till BMP med Aspose.CAD for Java](/cad/java/cad-export-options/export-to-bmp/)
- [Exportera DWG till PDF: Specifik layout med Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}