---
date: 2026-08-29
description: Lär dig hur du ställer in pdf-sidstorlek och konverterar CAD till PDF
  med Aspose.CAD för Java, med automatisk layoutskalning och TIFF-export.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: Ställ in pdf-sidstorlek – konvertera cad till pdf
og_description: Lär dig hur du ställer in pdf-sidstorlek när du konverterar CAD-ritningar
  till PDF i Java med Aspose.CAD. Denna guide täcker canvas-dimensioner, automatisk
  layoutskalning och export till högupplöst TIFF.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: Ställ in pdf-sidstorlek – konvertera CAD till PDF med Aspose i Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: Ställ in pdf-sidstorlek – konvertera cad till pdf (Java)
url: /sv/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ställ in PDF-sidstorlek – konvertera CAD till PDF (Java)

## Introduktion

Om du behöver **ställa in PDF-sidstorlek** när du konverterar CAD-ritningar till PDF, har du kommit till rätt ställe. I den här handledningen visar vi hur du använder Aspose.CAD för Java för att definiera exakta canvas-dimensioner, aktivera automatisk layoutskalning och sedan exportera resultatet till både PDF och TIFF. Oavsett om du förbereder ingenjörsscheman för utskrift eller genererar miniatyrbilder för ett webbgaleri, är kontroll av sidstorlek och utskriftsupplösning avgörande.

## Snabba svar
- **Vad betyder “convert CAD to PDF”?** Att omvandla en CAD-ritning (t.ex. DXF, DWG) till ett PDF-dokument som kan visas på vilken plattform som helst.  
- **Kan jag också exportera till TIFF?** Ja – använd `TiffOptions` för att skapa högupplösta rasterbilder.  
- **Vilket alternativ styr canvas-storlek i Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Vad är automatisk layoutskalning?** En flagga (`setAutomaticLayoutsScaling(true)`) som bevarar de ursprungliga layoutproportionerna när canvas-storleken ändras.  
- **Behöver jag en licens för Aspose.CAD?** En tillfällig eller permanent licens krävs för produktionsanvändning.

## Hur man ställer in PDF-sidstorlek när man konverterar CAD till PDF i Java

Läs in din CAD-fil, konfigurera `CadRasterizationOptions` med önskad bredd och höjd, aktivera automatisk layoutskalning och spara sedan resultatet som PDF. Detta tvåstegs tillvägagångssätt låter dig kontrollera de exakta dimensionerna på utskriftssidan utan att offra vektor kvalitet.

## Vad betyder konvertera CAD till PDF?

Att konvertera CAD till PDF innebär att ta vektorbaserade ingenjörsritningar och rendera dem som PDF-sidor, samtidigt som linjearbete, lager och geometri bevaras och filen blir universellt åtkomlig. Processen rasteriserar ritningen enligt de angivna alternativen och skapar en PDF som kan öppnas på vilken enhet som helst utan att kräva CAD-programvara, och behåller den visuella troheten i den ursprungliga designen.

## Varför ställa in canvas-storlek i Java?

Att ställa in canvas-storlek i Java låter dig definiera utskriftsupplösning och sidimensioner, vilket säkerställer att den resulterande PDF- eller TIFF-filen matchar dina utskrifts- eller visningskrav. Det ger dig också kontroll över skalningsbeteendet, vilket är avgörande för stora formatritningar.

## Förutsättningar

Innan du dyker ner i handledningen, se till att du har följande förutsättningar på plats:

- Aspose.CAD för Java: Se till att du har Aspose.CAD-biblioteket installerat i din Java-miljö. Du kan ladda ner Aspose.CAD för Java-biblioteket [här](https://releases.aspose.com/cad/java/).
- Dokumentkatalog: Skapa en dokumentkatalog för att lagra dina CAD-filer. Denna katalog kommer att refereras till i handledningens steg.

Låt oss nu komma igång med steg‑för‑steg‑guiden.

## Importera namnrymder

I detta steg importerar vi de nödvändiga namnrymderna för att kickstarta ditt Aspose.CAD‑projekt.

`Image` är huvudklassen som används för att läsa in CAD-filer.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Steg 1: importera Aspose.CAD-klasser

`Image`‑klassen tillhandahåller metoder för att läsa in och spara CAD-ritningar.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

I detta kodsnutt sätter vi upp sökvägen till resurskatalogen och läser in en DXF-fil med hjälp av Aspose.CAD:s `Image`‑klass.

## Steg 2: ange CadRasterizationOptions-egenskaper (ställ in canvas-storlek i Java)

`CadRasterizationOptions` specificerar rasteriseringsinställningar såsom sidstorlek och skalning för CAD‑till‑raster‑konvertering.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Här skapar vi en instans av `CadRasterizationOptions` och konfigurerar egenskaper som sidbredd, sidhöjd och **automatisk layoutskalning**. Detta är kärnan i **konfigurera canvas‑läge** för din konvertering.

## Steg 3: skapa PdfOptions och ange vectorRasterizationOptions

`PdfOptions` definierar PDF‑utdatainställningar för konverteringen.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nu skapar vi en `PdfOptions`‑instans och sätter dess `VectorRasterizationOptions`‑egenskap till den tidigare konfigurerade `CadRasterizationOptions`.

## Steg 4: exportera till PDF (konvertera CAD till PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Till sist sparar vi CAD‑bilden till en PDF‑fil med de angivna alternativen, vilket slutför **konvertera CAD till PDF**‑processen.

## Steg 5: skapa TiffOptions och ange vectorRasterizationOptions (exportera CAD till TIFF)

`TiffOptions` konfigurerar TIFF‑utdata parametrar såsom komprimering och upplösning.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Steg 6: exportera till TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Till sist sparar vi CAD‑bilden till en TIFF‑fil med de angivna alternativen, vilket demonstrerar hur man **exporterar CAD till TIFF** efter att canvas‑storleken har konfigurerats.

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|-------|-------|-----|
| Utskriven PDF är tom | `setNoScaling(true)` inaktiverar rendering för vissa ritningar | Ta bort `setNoScaling(true)` eller sätt den till `false`. |
| TIFF-upplösning ser låg ut | Sidbredd/höjd för liten | Öka värdena för `setPageWidth` / `setPageHeight`. |
| Layout ser förvrängd ut | Automatisk layoutskalning inaktiverad | Se till att `setAutomaticLayoutsScaling(true)` är aktiverad. |

## Varför justera canvas-storlek och DPI?

Att ändra canvas-storleken påverkar direkt rasteriseringsupplösningen på utskriften. Om du behöver **öka TIFF-upplösningen**, höj helt enkelt `setPageWidth` / `setPageHeight`-värdena eller anropa `rasterizationOptions.setResolution(300)` innan du skapar `TiffOptions`. Detta ger dig högkvalitativa rasterbilder som är lämpliga för utskrift eller detaljerad granskning.

## Vanliga frågor

**Q1: kan jag använda Aspose.CAD för Java med andra Java-ramverk?**  
A: Ja, Aspose.CAD är utformat för att sömlöst integreras med olika Java-ramverk.

**Q2: finns en tillfällig licens tillgänglig för Aspose.CAD?**  
A: Ja, du kan få en tillfällig licens på sidan [här](https://purchase.aspose.com/temporary-license/).

**Q3: var kan jag få community‑support för Aspose.CAD?**  
A: Besök Aspose.CAD‑forumet [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för community‑support och diskussioner.

**Q4: kan jag prova Aspose.CAD gratis?**  
A: Absolut! Hämta en gratis provnedladdningssida [här](https://releases.aspose.com/).

**Q5: hur köper jag Aspose.CAD för Java?**  
A: Köp Aspose.CAD för Java [här](https://purchase.aspose.com/buy).

**Q: påverkar canvas-storleken vektor­kvaliteten i PDF:en?**  
A: Nej. Canvas-storleken styr sidans dimensioner; vektordata förblir upplösningsoberoende, vilket säkerställer skarp rendering på alla zoomnivåer.

**Q: kan jag ange en annan DPI för TIFF‑utdata?**  
A: Ja. Justera `rasterizationOptions.setResolution(dpiValue)` innan du skapar `TiffOptions`.

**Q: hur kan jag ändra PDF-dimensioner för en befintlig PDF utan att rendera om CAD?**  
A: Använd Aspose.PDF för att ladda den genererade PDF‑filen och anropa `pdf.getPages().setPageSize(PageSize.A4)` eller en anpassad storlek.

**Q: vad är det bästa sättet att konvertera dxf till pdf samtidigt som lager bevaras?**  
A: Behåll `setAutomaticLayoutsScaling(true)` och undvik `setNoScaling(true)`; detta bevarar lagersynlighet och layout‑trohet.

## Slutsats

Grattis! Du har framgångsrikt **konverterat CAD till PDF** och **exporterat CAD till TIFF** samtidigt som du **ställt in canvas-storlek i Java**, aktiverat **automatisk layoutskalning** och lärt dig hur du **konfigurerar canvas-läge** för högkvalitativa resultat. Denna handledning ger en solid grund för dina CAD-konverteringsprojekt. Utforska fler funktioner och möjligheter i [Aspose.CAD-dokumentationen](https://reference.aspose.com/cad/java/).

---

**Last Updated:** 2026-08-29  
**Tested with:** Aspose.CAD for Java 24.12  
**Author:** Aspose

## Relaterade handledningar

- [Ställ in canvas-storlek – avancerade CAD-funktioner med Aspose.CAD för Java](/cad/java/advanced-cad-features/)
- [Exportera DWG till PDF i Java – Ställ in PDF-sidstorlek med Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Ställ in anpassad sidstorlek – PDF från CAD med automatisk layoutskalning](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}