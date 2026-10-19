---
date: 2026-10-19
description: Lär dig hur du konverterar DWG till PDF i Java med Aspose.CAD. Denna
  steg‑för‑steg‑guide visar hur du exporterar AutoCAD PDF, sparar CAD som PDF och
  tillämpar en licens.
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: Exportera AutoCAD‑bilder till PDF
og_description: Lär dig hur du konverterar DWG till PDF i Java med Aspose.CAD. Denna
  guide går dig igenom export av AutoCAD PDF, sparande av CAD som PDF och licensiering.
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: Konvertera DWG till PDF i Java med Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: Konvertera DWG till PDF i Java med Aspose.CAD
url: /sv/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera AutoCAD PDF – exportera AutoCAD‑bilder till PDF med Aspose.CAD för Java

## Introduktion

## Snabba svar
- **Kan jag konvertera DWG till PDF med Java?** Ja – Aspose.CAD för Java stöder nativt DWG, DXF och dussintals andra CAD‑format.  
- **Behöver jag en licens?** En permanent **Aspose CAD‑licens** tar bort alla utvärderingsrestriktioner; en tillfällig licens finns tillgänglig för testning.  
- **Vilka Java‑versioner stöds?** Java 8 och högre stöds fullt ut.  
- **Kan jag styra PDF‑sidans dimensioner?** Absolut – ange `pageWidth` och `pageHeight` i rasteriseringsalternativen.  
- **Är 3‑D‑rendering möjlig?** Ja – aktivera `TypeOfEntities.Entities3D` för att rasterisera 3‑D‑entiteter.

## Vad är export av AutoCAD PDF?
Exportering av AutoCAD PDF är processen att omvandla vektor‑CAD‑ritningar till ett portabelt PDF‑dokument. Det bevarar lager, linjebredder, färger och valfritt 3‑D‑geometri, vilket gör det enkelt att dela designer med kunder eller arkivera dem utan att behöva CAD‑programvara.

## Varför konvertera DWG till PDF med Aspose.CAD för Java?
Aspose.CAD stöder **över 50 in‑ och utdataformat**, bearbetar ritningar med hundratals sidor utan att ladda hela filen i minnet, och kör på alla plattformar som stödjer Java 8+. Biblioteket ger dig full kontroll över DPI, sidstorlek och layout, så du kan **anpassa PDF‑sidstorlek** för att matcha exakta projektspecifikationer, allt utan att installera inhemska DLL‑filer.

## Förutsättningar

- **Java Development Kit** – JDK 8 eller senare installerat på din arbetsstation.  
- **Aspose.CAD for Java** – ladda ner den senaste JAR‑filen från [download link](https://releases.aspose.com/cad/java/).  
- **Arbetskatalog** – en mapp där dina käll‑DWG‑filer och de genererade PDF‑filerna lagras.

## Importera namnrymder

`Image`‑klassen representerar vilken rasteriserbar CAD‑ritning som helst, medan `RasterizationOptions` och `PdfOptions` låter dig finjustera konverteringen.

`Image`‑klassen är Aspose.CAD:s översta objekt som håller en CAD‑ritning i minnet.  
`RasterizationOptions`‑klassen definierar hur vektordatan rasteriseras innan den skrivs till PDF.  
`PdfOptions`‑klassen samlar rasteriseringsinställningarna med PDF‑specifika utdata‑parametrar.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Låt oss nu gå igenom koden steg för steg.

## Hur konverterar man DWG till PDF med Aspose.CAD för Java?

För att konvertera en DWG‑fil till PDF med Aspose.CAD för Java, läs in ritningen med Image‑klassen, konfigurera CadRasterizationOptions (såsom DPI, sidstorlek och entitetstyper), paketera dessa alternativ i PdfOptions och anropa sedan save‑metoden med ett .pdf‑filnamn. Denna sekvens säkerställer att vektordatan rasteriseras korrekt och att den resulterande PDF‑filen matchar dina layoutkrav.

### Steg 1: ange sökvägen till resurskatalogen

Ersätt `"Your Document Directory"` med den absoluta sökvägen till den mapp du skapade i förutsättningarna.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Proffstips:** Använd `Paths.get(...).toAbsolutePath()` för att undvika sökvägsrelaterade fel på olika operativsystem.

### Steg 2: läs in CAD‑bilden

Att läsa in CAD‑filen i ett `Image`‑objekt ger dig full åtkomst till Aspose.CAD:s rasteriseringsmotor.

`Image`‑klassen läser in DWG‑filen och förbereder den för konvertering.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Varför detta är viktigt:** När ritningen är i minnet kan du fråga efter dess layouter, lager och metadata innan rasterisering.

### Steg 3: ange rasteriseringsalternativ

Justera `pageWidth` och `pageHeight` för att **anpassa PDF‑sidstorlek**. Aktivering av `setTypeOfEntities(TypeOfEntities.Entities3D)` möjliggör full 3‑D‑rendering när det behövs.

`RasterizationOptions`‑objektet styr DPI, sidmått och entitetstyper för utdata.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` mäts i punkter (1 pt = 1/72 tum).  
- Avkommentera raden `setTypeOfEntities` för 3‑D‑rasterisering.  
- `setLayouts` väljer vilken layout (Model, Layout1, etc.) som ska renderas.

### Steg 4: konfigurera PDF‑alternativ

Koppla rasteriseringsinställningarna till PDF‑utdata, så att vektordatan transformeras korrekt.

`PdfOptions`‑klassen länkar rasteriseringskonfigurationen med den slutgiltiga PDF‑filen.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Steg 5: spara PDF‑filen

Den resulterande filen, `Export3DImagestoPDF_out_.pdf`, är en **spara CAD som PDF**-representation av din ursprungliga AutoCAD‑ritning.

`save`‑metoden skriver den rasteriserade bilden till en PDF‑fil på disken.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## Vanliga problem & lösningar

| Symptom | Trolig orsak | Åtgärd |
|---------|--------------|-------|
| Tom PDF‑utdata | Rasteriseringsalternativ inte inställda eller layoutmatchning fel | Verifiera att `setLayouts` matchar layoutnamnet i din CAD‑fil. |
| Lågupplöst bild | `pageWidth`/`pageHeight` för små | Öka dimensionerna eller ange en högre DPI via `rasterizationOptions.setResolution(...)`. |
| Licensundantag | Ingen giltig licens tillämpad | Tillämpa en **Aspose CAD‑licens** eller använd en tillfällig licens för testning. |

## Vanliga frågor

**Q: Kan jag använda Aspose.CAD för Java med andra CAD‑filformat?**  
A: Ja – biblioteket stöder DWG, DXF, DWF, DGN och över 30 ytterligare format, vilket ger dig flexibilitet i olika projekt.

**Q: Hur får jag en tillfällig licens för Aspose.CAD för Java?**  
A: Besök [temporary license page](https://purchase.aspose.com/temporary-license/) för att begära en tidsbegränsad licens för utvärdering.

**Q: Finns det layoutalternativ för rasterisering?**  
A: Absolut. Använd `setLayouts("Model")`, `setLayouts("Layout1")` osv. för att välja vilken vy som renderas till PDF.

**Q: Kan jag ändra storleken på den genererade PDF‑filen?**  
A: Ja – ändra `pageWidth` och `pageHeight` i rasteriseringsalternativen för att matcha önskade sidmått.

**Q: Var kan jag få hjälp om jag stöter på problem?**  
A: Den dedikerade gemenskapen finns på [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) där du kan ställa frågor och dela lösningar.

---

**Senast uppdaterad:** 2026-10-19  
**Testad med:** Aspose.CAD for Java 24.10  
**Författare:** Aspose

## Relaterade handledningar

- [Exportera DWG till PDF i Java – Ställ in PDF‑sidstorlek med Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Exportera DWG till PDF: Specifik layout med Aspose.CAD för Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exportera DWG till PDF och aktivera spårning med Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}