---
date: 2026-10-14
description: Lär dig hur Java CAD-biblioteket Aspose.CAD för Java kan exportera DWG
  till PDF eller rasterbilder snabbt och exakt.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: Exportera DWG PDF och rasterbilder
og_description: Exportera DWG PDF snabbt med Aspose.CAD för Java. Lär dig högkvalitativ
  PDF‑konvertering, rasteralternativ och licensiering i denna steg‑för‑steg‑guide.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: Exportera DWG PDF och rasterbilder med Java CAD-biblioteket Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: Exportera DWG PDF och rasterbilder med Java CAD-biblioteket Aspose.CAD
url: /sv/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera DWG PDF och rasterbilder med Java CAD-biblioteket Aspose.CAD

## Introduktion

Att exportera DWG till PDF är ett vanligt krav för ingenjörer, arkitekter och alla som behöver dela CAD-ritningar utan att avslöja det ursprungliga filformatet. Med **Aspose.CAD for Java** kan du **export dwg pdf** — eller rasterbilder — på bara några rader Java‑kod, samtidigt som du behåller vektorfidelitet och layoutprecision. Denna handledning guidar dig genom att läsa in en DWG‑fil, konfigurera rasterisering och spara resultatet som en högkvalitativ PDF eller bild. Du får också se varför Aspose.CAD är det föredragna Java CAD‑biblioteket för pålitlig, plattformsoberoende konvertering.

För en fokuserad guide om endast PDF‑konvertering, se [Export DWG to PDF tutorial](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## Snabba svar
- **Vad täcker den här handledningen?** Export av DWG‑filer till PDF eller rasterbilder med Aspose.CAD for Java.  
- **Behöver jag en licens?** En gratis tillfällig licens finns tillgänglig för utvärdering; en full licens krävs för produktion.  
- **Vilken Java‑version stöds?** Alla Java 8+‑miljöer fungerar med det senaste Aspose.CAD Java‑API‑et.  
- **Kan jag konvertera DWG till andra bildformat?** Ja – samma rasteriseringsalternativ låter dig generera PNG, JPEG, BMP osv.  
- **Hur lång tid tar konverteringen?** Vanligtvis under en sekund för standardritningar; större filer kan ta några sekunder.

## Varför Java CAD‑bibliotek är det bästa valet för DWG‑konvertering?

Aspose.CAD for Java är det bästa valet eftersom det erbjuder en ren‑Java‑implementation som inte kräver inhemska DLL‑filer, automatiskt upptäcker metriska eller imperiella enheter, levererar rasterutdata upp till 1200 DPI och genererar vektor‑bevarande PDF‑filer utan externa beroenden. Biblioteket har också en flexibel licensmodell som låter dig börja med en tillfällig licens och skala upp till företagsanvändning.

## Vad är “export dwg to pdf”?

`Export dwg pdf` är processen att konvertera en inhemsk DWG‑ritningsfil till ett PDF‑dokument samtidigt som vektordata, lager och skalning bevaras. Denna konvertering skapar en enhetsoberoende fil som kan visas på vilken plattform som helst utan behov av AutoCAD. Eftersom PDF‑filen behåller vektorinformation är text sökbar och grafik förblir skarp vid alla zoomnivåer, vilket gör den idealisk för dokumentation, kundgranskning och arkivering.

## Varför använda Aspose.CAD Java för denna konvertering?

Du bör använda Aspose.CAD Java eftersom biblioteket hanterar enhetskonvertering, rasterisering och PDF‑inbäddning internt, vilket eliminerar behovet av tredjepartsverktyg eller komplexa kommandorads‑pipelines. Dess API är utformat för utvecklare: ett enda `Image`‑objekt representerar ritningen, och några konfigurationsobjekt låter dig finjustera DPI, sidstorlek och komprimering. Resultatet blir konsekvent, repeterbar output på Windows, Linux och macOS.

## Förutsättningar

Innan du dyker ner i koden, se till att du har:

- Grundläggande kunskaper i Java‑programmering.  
- Aspose.CAD for Java‑biblioteket installerat. Om du ännu inte har laddat ner det, hämta det **[download Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- En DWG‑fil för testning – exempelfilen **Bottom_plate.dwg** används i den här guiden.  

## Importera namnrymder

I ditt Java‑projekt importerar du de nödvändiga klasserna för att kick‑starta konverteringen:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Steg‑för‑steg guide

### Steg 1: Ladda DWG-filen

Först laddar du din DWG‑ritning med `Image`‑klassen. Detta skapar en minnesrepresentation som Aspose.CAD kan arbeta med.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Steg 2: Bestäm enhetstyp

Att förstå om ritningen använder metrisk eller imperiell enhet är avgörande för korrekt skalning. Hjälpmetoden `IsMetric` (implementation utelämnad för korthet) returnerar en boolesk flagga.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Steg 3: Ställ in rasteriseringsalternativ

Klassen `CadRasterizationOptions` definierar rasteriseringsparametrar såsom DPI, sidstorlek och enhetskonvertering. Baserat på enhetssystemet konfigurerar du sidstorlek, skalning och mål‑enhetstyp. Dessa alternativ styr hur DWG rasteriseras innan den paketeras i en PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Steg 4: Konfigurera PDF-alternativ (pdf options cad)

Klassen `PdfOptions` specificerar PDF‑specifika inställningar, inklusive komprimering och metadata. Skapa en `PdfOptions`‑instans och fäst rasteriseringsinställningarna. Detta talar om för Aspose.CAD hur den rasteriserade innehållet ska bäddas in i den slutgiltiga PDF‑filen.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Steg 5: Spara som PDF

`save`‑metoden skriver bilden till den angivna filsökvägen med de medföljande alternativen. Slutligen exporterar du ritningen till en PDF‑fil. `save`‑metoden tar utdata‑sökvägen och de konfigurerade `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

När koden är klar hittar du **Saved.pdf** i din `DWGDrawings`‑mapp, redo för distribution eller arkivering.

## Hur konverterar man DWG rasterbilder med Java CAD‑bibliotek?

Du kan konvertera DWG till rasterformat genom att byta ut `PdfOptions` mot en raster‑specifik alternativklass såsom `PngOptions` eller `JpegOptions`. Återanvänd samma `CadRasterizationOptions`‑instans, justera utdataformatet och anropa `save`‑metoden med det nya alternativobjektet. Detta tillvägagångssätt låter dig generera PNG, JPEG, BMP eller TIFF‑filer med en enda rad förändring, samtidigt som arbetsflödet förblir konsistent.

## Hur genererar man PDF DWG med PDF‑alternativ CAD?

Exemplet ovan **genererar pdf dwg**‑output redan. För att finjustera PDF‑storleken, aktivera komprimering genom att anropa `pdfOptions.setCompress(true)`. Du kan också bädda in anpassad metadata, ange PDF‑version eller lägga till lösenordsskydd via ytterligare `PdfOptions`‑egenskaper. Dessa justeringar ger dig full kontroll över den slutgiltiga PDF‑filen utan att lämna Java‑kodbasen.

## Vanliga problem & tips

- **Fel sidstorlek** – Dubbelkolla logiken för enhetskonvertering; felaktiga koefficienter kan producera för stora sidor.  
- **Saknade typsnitt eller linjebredder** – Säkerställ att DWG‑filen refererar till alla externa resurser innan konvertering.  
- **Prestanda på stora ritningar** – Öka `DPI`‑inställningen i `CadRasterizationOptions` endast när högre kvalitet krävs; lägre DPI snabbar upp bearbetningen.  
- **Licensfrågor** – För utvärdering kan du använda en **temporary license Aspose**; en full licens krävs för produktionsdistributioner.

## Vanliga frågor

**Q: Kan jag använda Aspose.CAD för Java med andra Java‑ramverk?**  
A: Ja, Aspose.CAD for Java integreras sömlöst med populära Java‑ramverk såsom Spring, Jakarta EE och Android.

**Q: Finns en tillfällig licens för Aspose.CAD för Java?**  
A: Ja, du kan skaffa en tillfällig licens **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.

**Q: Var kan jag hitta support för Aspose.CAD för Java?**  
A: Besök **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** för hjälp från communityn och Aspose‑ingenjörer.

**Q: Hur kan jag köpa en licens för Aspose.CAD för Java?**  
A: Du kan köpa en licens **[purchase a license](https://purchase.aspose.com/buy)**.

**Q: Vilka enheter stöder Aspose.CAD för Java?**  
A: Aspose.CAD for Java stöder både metrisk och imperiell enhet, och upptäcker automatiskt ritningens enhetssystem.

**Q: Kan jag konvertera DWG till andra bildformat (t.ex. PNG, JPEG) med samma API?**  
A: Absolut. Byt ut `PdfOptions` mot lämpliga raster‑bildalternativ (t.ex. `PngOptions`) och återanvänd samma `CadRasterizationOptions`.

## Slutsats

Denna handledning demonstrerade hur du **export dwg pdf** och rasterbilder med **java cad library** Aspose.CAD for Java. Genom att följa steg‑för‑steg‑guiden kan du integrera pålitlig CAD‑konvertering i vilken Java‑applikation som helst, oavsett om du behöver PDF‑filer för dokumentation eller rasterbilder för webbvisning. Bibliotekets rena Java‑natur, högkvalitativa output och flexibla licensiering gör det till ett starkt val för både små verktyg och storskaliga företags‑pipeline.

---

**Last Updated:** 2026-10-14  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## Relaterade handledningar

- [Exportera DWG till PDF: Specifik layout med Aspose.CAD för Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exportera DWG till PDF i Java – Ställ in PDF‑sidstorlek med Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Exportera DWG till PDF med dolda linjer – Aspose.CAD för Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}