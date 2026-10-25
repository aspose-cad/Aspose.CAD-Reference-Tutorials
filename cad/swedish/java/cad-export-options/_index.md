---
date: 2026-10-25
description: Lär dig hur du konverterar DWG till PDF, exporterar CAD‑layouter, BMP-,
  IFC- och STL‑filer med Aspose.CAD for Java. Inkluderar licensinformation, prestandatips
  och verkliga användningsfall.
keywords:
- convert dwg to pdf
- cad layout pdf export
- generate pdf from dwg
- java convert cad pdf
- export stl to png
lastmod: 2026-10-25
linktitle: CAD-exportalternativ
og_description: Konvertera DWG till PDF, BMP, IFC och STL med Aspose.CAD for Java.
  Lär dig steg för steg, se prestandaresultat och få licensvägledning i den här guiden
  för 2026.
og_image_alt: Screenshot of Aspose.CAD Java API converting DWG to PDF
og_title: Konvertera DWG till PDF och andra CAD-exportalternativ i Java
schemas:
- author: Aspose
  dateModified: '2026-10-25'
  description: Learn how to convert DWG to PDF, export CAD layouts, BMP, IFC, and
    STL files using Aspose.CAD for Java. Includes licensing notes, performance tips,
    and real‑world use cases.
  headline: How to convert DWG to PDF and other CAD export options in Java
  type: TechArticle
- questions:
  - answer: Load the IFC file with `Image.load("model.ifc")` and call `save("model.png",
      new PngOptions())`.
    question: How do I convert IFC to PNG using Aspose.CAD?
  - answer: Yes—Aspose.CAD treats layouts as images internally, so `save("layout.pdf",
      new PdfOptions())` handles it automatically.
    question: Can I export a CAD layout directly to PDF without converting to an image
      first?
  - answer: Exporting an AutoCAD drawing converts the entire drawing, while exporting
      a layout targets a specific paper‑space view, preserving its page settings.
    question: What is the difference between exporting AutoCAD to PDF and exporting
      a CAD layout to PDF?
  - answer: No inherent limit; each layout becomes a separate page in the resulting
      PDF.
    question: Is there a limit on the number of pages when exporting a multi‑sheet
      DWG to PDF?
  - answer: A single Aspose.CAD license covers all supported formats (PDF, PNG, BMP,
      etc.).
    question: Do I need a separate license for each export format?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg to pdf
- Aspose.CAD
- Java CAD conversion
- CAD export tutorials
title: Hur man konverterar DWG till PDF och andra CAD-exportalternativ i Java
url: /sv/java/cad-export-options/
weight: 30
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD-exportalternativ

## Introduktion

Om du är en Java‑utvecklare som snabbt och pålitligt behöver **convert DWG to PDF**, har du kommit till rätt ställe. Den här guiden går igenom de vanligaste export‑scenarierna för Aspose.CAD for Java — inklusive AutoCAD‑bilder, CAD‑layouter, BMP, PDF, IFC och STL‑filer. Du kommer att se varför dessa funktioner är viktiga i verkliga projekt, lära dig bästa praxis‑tips och få färdiga kodsnuttar att kopiera för dina egna applikationer.

## Snabba svar
- **Vad är det enklaste sättet att exportera AutoCAD till PDF?** Use `Image.save("output.pdf", new PdfOptions())` from Aspose.CAD.  
- **Vilka format kan jag konvertera IFC‑filer till?** PNG stöds fullt ut; ladda bara IFC‑filen och spara som PNG.  
- **Kan jag exportera STL‑filer direkt till PNG?** Ja—ladda STL‑modellen och anropa `save("image.png")`.  
- **Behöver jag en licens för produktionsanvändning?** En kommersiell licens krävs för icke‑testdistributioner.  
- **Vilken Java‑version krävs?** Java 8 eller högre rekommenderas.

## Vad är export av AutoCAD till PDF?

Att exportera AutoCAD‑ritningar till PDF innebär att konvertera vektorbaserade DWG/DXF‑filer till ett allmänt accepterat, sidorienterat format. PDF bevarar lager, linjebredder och färger, vilket gör det idealiskt för att dela designer med kunder, granskare eller efterföljande system som inte förstår inhemska CAD‑filer.

## Varför använda Aspose.CAD för Java?

Aspose.CAD for Java är ett **pure‑Java**‑bibliotek — inga inhemska DLL‑filer eller COM‑interoperabilitet krävs. Det återger geometri, text och rasterdata med **hög noggrannhet**, stödjer **batch‑bearbetning** av tusentals filer och hanterar **över 60 in‑ och utdataformat** (inklusive DWG, DXF, IFC, STL, BMP, PNG och PDF). Bibliotekets minnes‑effektiva pipeline låter dig bearbeta ritningar med flera hundra sidor utan att ladda hela filen i RAM.

## Varför detta är viktigt

Att kunna **convert DWG to PDF** i farten låter dig automatisera rapportgenerering, skapa leveranser redo för kunden och bädda in CAD‑data i webbportaler utan att exponera råa DWG‑filer. Samma API skapar även bild‑baserade export (BMP, PNG) för miniatyrer, snabba visuella kontroller och lätta förhandsgranskningar.

## Förutsättningar
- Java 8 eller nyare installerat.  
- Aspose.CAD for Java‑biblioteket tillagt i ditt projekt (Maven, Gradle eller manuell JAR).  
- En giltig Aspose‑licens för produktionsanvändning (gratis provversion finns för utvärdering).

## Så konverterar du DWG till PDF i Java

`Image` är den centrala Aspose.CAD‑klassen som representerar ett CAD‑dokument i minnet.  
`PdfOptions` konfigurerar PDF‑specifika utskriftsinställningar såsom upplösning och kompression.

Läs in DWG‑filen (eller något annat stödjert CAD‑format) med `Image.load`, och anropa sedan `save` med en `PdfOptions`‑instans. Detta tvåstegs‑mönster hanterar vektor‑till‑PDF‑konvertering, bevarar lager och låter dig justera DPI‑ eller komprimeringsinställningar.

`Image`‑klassen representerar alla stödjade CAD‑dokument i minnet, medan `PdfOptions` konfigurerar PDF‑utdata. Inga extra konverteringsverktyg eller externa verktyg behövs.

### Steg 1: läs in DWG‑filen
```java
// Load a DWG file – the Image class is the entry point for all Aspose.CAD operations
com.aspose.cad.Image cadImage = com.aspose.cad.Image.load("sample.dwg");
```

### Steg 2: konfigurera PDF‑alternativ (valfritt)
```java
// Create PDF options – you can set vector rasterization DPI, compression, etc.
com.aspose.cad.imageoptions.PdfOptions pdfOptions = new com.aspose.cad.imageoptions.PdfOptions();
pdfOptions.setVectorRasterizationOptions(
    new com.aspose.cad.imageoptions.VectorRasterizationOptions()
        .setPageWidth(2100)   // width in pixels (A4 at 300 DPI)
        .setPageHeight(2970)  // height in pixels
        .setResolution(300)   // 300 DPI for high‑quality output
);
```

### Steg 3: spara som PDF
```java
// Save the loaded DWG as a PDF file
cadImage.save("output.pdf", pdfOptions);

// Release resources – important when processing many files in a loop
cadImage.dispose();
```

De tre raderna ovan utgör ett komplett **convert DWG to PDF**‑arbetsflöde. Du kan placera dem i en loop för att batch‑bearbeta en katalog med ritningar.

## Exportera CAD‑layouter till PDF

Att exportera en specifik layout (paper‑space‑vy) fungerar på samma sätt eftersom Aspose.CAD behandlar varje layout som en bild internt. Läs helt enkelt in DWG‑filen, välj layouten efter namn om det behövs, och anropa `save` med `PdfOptions`. Inget extra konverteringssteg krävs.

## Exportera till BMP

`BmpOptions` specificerar BMP‑formatets utdata‑parametrar såsom bitdjup och upplösning. När du behöver raster‑miniatyrer eller bitmap‑tillgångar, använd `BmpOptions` istället för `PdfOptions`. Samma `Image`‑objekt kan sparas till BMP med ett enda anrop, vilket låter dig generera högupplösta förhandsgranskningar för kataloger eller UI‑miniatyrer.

## Exportera till PDF (generella CAD‑filer)

Utöver DWG kan biblioteket konvertera DXF, DWF och andra CAD‑format till PDF med identisk kod. Ändra bara filändelsen i `Image.load`. Den underliggande konverteringsmotorn upptäcker automatiskt källformatet.

## Exportera IFC till PNG

`PngOptions` definierar PNG‑formatinställningar såsom komprimeringsnivå. IFC‑filer (Industry Foundation Classes) är vanliga i BIM‑arbetsflöden. Läs in IFC‑filen med `Image.load` och spara den som PNG med `PngOptions`. Detta skapar en rasterbild som kan bäddas in i webb‑dashboards eller dokumentation.

## Exportera STL till PNG

`PngOptions` definierar PNG‑formatinställningar såsom komprimeringsnivå. STL‑filer beskriver 3‑D‑nät. Aspose.CAD renderar dem till en 2‑D‑bild, som du kan exportera som PNG för snabba visuella kontroller eller produktlistor. Samma `Image.save("model.png", new PngOptions())`‑mönster gäller.

## CAD‑exporthandledningar

### [Exportera AutoCAD‑bilder till PDF - Aspose.CAD för Java‑handledning](./export-autocad-images-to-pdf/)
Effortlessly export AutoCAD images to PDF using Aspose.CAD for Java. Follow our step‑by‑step guide for seamless integration.

### [Exportera CAD‑layouter till PDF med Aspose.CAD för Java](./export-cad-layouts-to-pdf/)
Explore Aspose.CAD for Java to effortlessly export CAD layouts to PDF. Efficient, reliable, and developer‑friendly.

### [Exportera till BMP med Aspose.CAD för Java](./export-to-bmp/)
Explore seamless CAD to BMP conversion with Aspose.CAD for Java. Follow our step‑by‑step guide for efficient and precise exports.

### [Exportera till PDF med Aspose.CAD för Java](./export-to-pdf/)
Learn how to export CAD files to PDF effortlessly with Aspose.CAD for Java. Follow our step‑by‑step guide for seamless integration.

### [Exportera IFC till PNG med Aspose.CAD för Java](./export-ifc-to-png/)
Convert IFC to PNG effortlessly with Aspose.CAD for Java. Follow our step‑by‑step tutorial.

### [Exportera STL till PNG med Aspose.CAD för Java](./export-stl-to-png/)
Explore the seamless process of exporting STL files to PNG in Java with Aspose.CAD. Simplify your workflow and enhance your Java projects effortlessly.

## Vanliga användningsfall
- **Kundleveranser** – Tillhandahåll designgranskningar i PDF utan att exponera käll‑DWG‑filer.  
- **Automatiserad rapportering** – Generera PNG‑miniatyrer av IFC‑ eller STL‑modeller för dashboards.  
- **Batch‑konverteringspipeline** – Bearbeta stora CAD‑arkiv över natten med en enkel Java‑loop.

## Tips och tricks
- **Proffstips:** Ställ in `PdfOptions.setVectorRasterizationOptions().setResolution(300)` för att kontrollera DPI för raster‑baserade export och hålla filstorlekarna rimliga.  
- **Undvik minnesspikar:** Anropa `Image.dispose()` efter varje `save` när du bearbetar många filer.  
- **Felsökning:** Om lager försvinner, kontrollera att käll‑DWG har synliga lager och aktivera kompression med `PdfOptions.setCompress(true)`.

## Vanliga frågor

**Q: Hur konverterar jag IFC till PNG med Aspose.CAD?**  
A: Läs in IFC‑filen med `Image.load("model.ifc")` och anropa `save("model.png", new PngOptions())`.

**Q: Kan jag exportera en CAD‑layout direkt till PDF utan att först konvertera till en bild?**  
A: Ja—Aspose.CAD behandlar layouter som bilder internt, så `save("layout.pdf", new PdfOptions())` hanterar det automatiskt.

**Q: Vad är skillnaden mellan att exportera AutoCAD till PDF och att exportera en CAD‑layout till PDF?**  
A: Att exportera en AutoCAD‑ritning konverterar hela ritningen, medan export av en layout riktar sig mot en specifik paper‑space‑vy och bevarar dess sidinställningar.

**Q: Finns det någon gräns för antalet sidor vid export av en multi‑sheet DWG till PDF?**  
A: Ingen inneboende gräns; varje layout blir en separat sida i den resulterande PDF‑filen.

**Q: Behöver jag en separat licens för varje exportformat?**  
A: En enda Aspose.CAD‑licens täcker alla stödjade format (PDF, PNG, BMP, etc.).

---

**Senast uppdaterad:** 2026-10-25  
**Testat med:** Aspose.CAD for Java 24.12  
**Författare:** Aspose

## Relaterade handledningar

- [Exportera CAD till PDF: Exportera CAD‑layouter till PDF med Aspose.CAD för Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Exportera DWG till PDF i Java – Ställ in PDF‑sidstorlek med Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}