---
date: 2026-10-19
description: Lär dig hur du exporterar AutoCAD-ritningar till PDF med en anpassad
  PDF-sidstorlek med hjälp av Aspose.CAD för Java. Denna steg‑för‑steg‑guide täcker
  konvertering av DWG till PDF, rasteriseringsalternativ och licensiering.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: Exportera AutoCAD‑bilder till PDF
og_description: Ställ in en anpassad PDF-sidstorlek när du exporterar AutoCAD-ritningar
  till PDF med Aspose.CAD för Java. Lär dig DWG‑till‑PDF‑konvertering, rasteriseringsinställningar
  och licensiering på några minuter.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Ställ in anpassad PDF-sidstorlek för AutoCAD-export med Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Ställ in anpassad PDF-sidstorlek för AutoCAD-export med Aspose.CAD
url: /sv/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera AutoCAD PDF - exportera AutoCAD‑bilder till PDF med Aspose.CAD för Java

## Introduktion

Om du behöver **konvertera DWG till PDF** och kontrollera de exakta dimensionerna på utdatafilen, har du kommit till rätt ställe. Denna handledning visar hur du ställer in en **anpassad PDF‑sidstorlek** när du exporterar AutoCAD‑bilder till PDF med Aspose.CAD för Java. I slutet av guiden kommer du att veta hur du laddar en DWG, konfigurerar rasteriseringsalternativ såsom DPI och sidbredd/höjd, tillämpar en licens och genererar en produktionsklar PDF.

## Snabba svar
- **Kan jag konvertera DWG till PDF med Java?** Ja – Aspose.CAD for Java stöder DWG, DXF, DWF och många andra CAD‑format inbyggt.  
- **Behöver jag en licens för produktionsanvändning?** En fullständig Aspose.CAD‑licens tar bort alla utvärderingsgränser; en tillfällig licens finns tillgänglig för testning.  
- **Vilka Java‑versioner är kompatibla?** Biblioteket fungerar med Java 8 och senare JDK.  
- **Hur ändrar jag PDF‑sidans dimensioner?** Ställ in `pageWidth` och `pageHeight` på `PdfOptions.getRasterizationOptions()` till önskad storlek.  
- **Stöds 3‑D‑rendering?** Ja – aktivera `TypeOfEntities.Entities3D` för att rasterisera 3‑D‑entiteter.

## Vad är export av AutoCAD PDF?
Att exportera AutoCAD PDF innebär att konvertera vektorbaserade CAD‑ritningar (DWG, DXF, DWF osv.) till ett portabelt PDF‑dokument samtidigt som lager, linjebredder och valfri 3‑D‑geometri bevaras. Detta gör det möjligt att dela design med kunder, arkivera ritningar eller skriva ut utan att installera CAD‑programvara.

## Varför använda Aspose.CAD för Java för att konvertera DWG till PDF?
Aspose.CAD för Java är idealiskt för att konvertera DWG till PDF eftersom det erbjuder omfattande formatstöd, körs på ren Java utan inhemska beroenden, ger högupplöst rasterisering med full kontroll över DPI och sidstorlek, samt inkluderar flexibel licensiering som låter dig börja med en provperiod och skala upp till produktion.

- **Brett formatstöd** – stöder över 50 in- och utdataformat, inklusive DWG, DXF, DWF, DGN och PDF.  
- **Ren Java‑implementation** – inga inhemska DLL‑filer eller externa beroenden, så distribution är enkel på alla plattformar.  
- **Högupplöst rasterisering** – du kan ange DPI, sidstorlek och layout, vilket ger dig full kontroll över resultatets **anpassade PDF‑sidstorlek**.  
- **Skalbar licensiering** – börja med en gratis provperiod, och uppgradera sedan till en permanent **Aspose CAD‑licens**.  

## Förutsättningar

- **Java Development Kit** – JDK 8 eller nyare installerat på din maskin.  
- **Aspose.CAD för Java** – ladda ner den senaste JAR‑filen från [download link](https://releases.aspose.com/cad/java/).  
- **Arbetskatalog** – en mapp som innehåller käll‑DWG‑filerna och som kommer att ta emot de genererade PDF‑filerna.

## Importera namnrymder

`Image`‑klassen är Aspose.CAD:s kärnobjekt som representerar en CAD‑ritning i minnet. Importera de nödvändiga paketen innan du börjar koda.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Låt oss nu gå igenom koden steg för steg.

## Hur ställer man in en anpassad PDF‑sidstorlek när man exporterar DWG till PDF?

Ladda din DWG, definiera önskad sidbredd och -höjd, och spara sedan resultatet som PDF – det är allt du behöver för att skapa en PDF med en anpassad sidstorlek. Följande steg illustrerar den exakta sekvensen och den minsta kod som krävs.

### Steg 1: ange sökvägen till resurskatalogen

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Proffstips:** Ersätt `"Your Document Directory"` med den absoluta sökvägen till den mapp du skapade i förutsättningarna.

### Steg 2: ladda CAD‑bilden

`Image`‑klassen laddar CAD‑filen och ger dig åtkomst till Aspose.CAD:s rasteriseringsmotor.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Varför detta är viktigt:** När CAD‑filen är laddad kan du manipulera rasteriseringsalternativ innan du renderar till PDF.

### Steg 3: ange rasteriseringsalternativ

`CadRasterizationOptions`‑klassen specificerar hur CAD‑ritningen rasteriseras innan den sparas som PDF. Justera `pageWidth` och `pageHeight` för att definiera en **anpassad PDF‑sidstorlek**. Du kan också aktivera 3‑D‑rendering genom att avkommentera raden `setTypeOfEntities`.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – mätt i pixlar; ändra dessa värden för att matcha A4, Letter eller någon annan anpassad dimension.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – renderar 3‑D‑entiteter när det behövs.  
- `setLayouts` – väljer vilken layout (Model, Layout1, etc.) som ska rasteriseras.

### Steg 4: konfigurera PDF‑alternativ

`PdfOptions`‑klassen innehåller PDF‑specifika inställningar och länkar rasteriseringsalternativen till utdatafilen, vilket säkerställer att de anpassade siddimensionerna tillämpas korrekt.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Steg 5: spara PDF‑filen

`save`‑metoden skriver den renderade bilden till den angivna PDF‑filen.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Den resulterande filen, `Export3DImagestoPDF_out_.pdf`, är en **save cad as pdf**‑representation av din ursprungliga AutoCAD‑ritning med de exakta siddimensioner du angav.

## Vanliga problem & lösningar

| Symtom | Trolig orsak | Åtgärd |
|---------|--------------|-----|
| Tom PDF‑utdata | Rasteriseringsalternativ ej inställda eller layout‑mismatch | Verifiera att `setLayouts` matchar layout‑namnet i din CAD‑fil. |
| Lågupplöst bild | `pageWidth`/`pageHeight` för små eller DPI låg | Öka dimensionerna eller anropa `rasterizationOptions.setResolution(...)` med en högre DPI. |
| Licensundantag | Ingen giltig licens tillämpad | Tillämpa en permanent Aspose.CAD‑licens eller använd en tillfällig licens för testning. |

## Vanliga frågor

**Q: Kan jag använda Aspose.CAD för Java med andra CAD‑filformat?**  
A: Ja, biblioteket stöder DWG, DXF, DWF, DGN och många fler, vilket ger dig flexibilitet i olika projekt.

**Q: Hur får jag en tillfällig licens för Aspose.CAD för Java?**  
A: Besök [temporary license page](https://purchase.aspose.com/temporary-license/) för att begära en tidsbegränsad licens för utvärdering.

**Q: Finns det layoutalternativ för rasterisering?**  
A: Absolut. Använd `setLayouts("Model")` eller specificera andra layoutnamn för att styra vilken vy som renderas.

**Q: Kan jag anpassa storleken på den genererade PDF‑filen?**  
A: Ja – ändra `pageWidth` och `pageHeight` i rasteriseringsalternativen till de dimensioner du behöver.

**Q: Var kan jag få hjälp eller diskutera problem relaterade till Aspose.CAD för Java?**  
A: Det dedikerade [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) erbjuder community‑support och officiella svar från Aspose‑teamet.

## Ytterligare FAQ (AI‑vänligt format)

**Q: Kräver Aspose.CAD några inhemska bibliotek på Windows eller Linux?**  
A: Nej. Aspose.CAD för Java är ett rent Java‑bibliotek, så det körs på alla plattformar som stöder JDK utan extra inhemska DLL‑filer.

**Q: Hur stor DWG‑fil kan biblioteket bearbeta?**  
A: Biblioteket kan hantera ritningar med flera hundra sidor (upp till 500 MB) utan att ladda hela filen i minnet, tack vare dess streaming‑arkitektur.

**Q: Är det möjligt att batch‑konvertera många DWG‑filer till PDF i ett körning?**  
A: Ja. Iterera över en katalog, ladda varje fil med `Image.load()`, tillämpa samma rasteriseringsalternativ och anropa `save()` för varje utdata‑PDF.

**Q: Vilken prestanda kan jag förvänta mig på en vanlig server?**  
A: Att konvertera en 100‑sidig DWG vid 300 DPI på en standard 2,5 GHz‑CPU tar ungefär 12 sekunder, baserat på Asposes benchmark‑tester.

**Q: Bevarar biblioteket lagerinformation i PDF‑filen?**  
A: Även om utdata är rasteriserade återges det visuella utseendet på lager, linjebredder och färger troget.

**Senast uppdaterad:** 2026-10-19  
**Testat med:** Aspose.CAD for Java 24.10  
**Författare:** Aspose

## Relaterade handledningar

- [Exportera DWG till PDF och aktivera spårning med Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Exportera DWG till PDF: specifik layout med Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exportera DWG till BMP och justera CAD‑storlek med enhetstyp med Aspose.CAD för Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}