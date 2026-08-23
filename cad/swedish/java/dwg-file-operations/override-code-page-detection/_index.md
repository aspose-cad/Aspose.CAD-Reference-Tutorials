---
date: 2026-05-20
description: Lär dig hur du konverterar DWG till PDF samtidigt som du åsidosätter
  automatisk kodsidodetektering med Aspose.CAD för Java. Inkluderar steg för att exportera
  dwg till pdf, kodningstips och felsökning.
keywords:
- convert dwg pdf
- export dwg to pdf
- Aspose.CAD Java
linktitle: Åsidosätt automatisk kodsidodetektering i DWG-filer
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  headline: Convert DWG to PDF – Override Code Page Detection in Java
  type: TechArticle
- description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  name: Convert DWG to PDF – Override Code Page Detection in Java
  steps:
  - name: Set Up the Java Project
    text: Create a Maven or Gradle project and add the Aspose.CAD JAR to the classpath.
      This ensures the IDE can resolve the imported classes and that the runtime can
      locate the library.
  - name: Load the DWG File with a Specified Code Page
    text: Tell Aspose.CAD which encoding to use and whether to attempt recovery of
      malformed CIF/MIF data.
  - name: Export the CAD Image to PDF
    text: With the correct code page applied, you can safely export the drawing. The
      `PdfOptions` object lets you fine‑tune the PDF output (compression, rasterization,
      etc.).
  - name: Verify Success
    text: A simple console message confirms that the process completed without exceptions.
      You can repeat these steps for multiple DWG files, adjusting the source path
      and output name as needed.
  type: HowTo
- questions:
  - answer: It forces Aspose.CAD to use a specific character encoding instead of guessing.
    question: What does “override code page” mean?
  - answer: Yes – after setting the correct code page, you can save the CAD image
      as PDF.
    question: Can I export DWG directly to PDF?
  - answer: '`CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.'
    question: Which encoding works for Japanese text?
  - answer: A commercial license is required; a temporary license is available for
      testing.
    question: Do I need a license for production use?
  - answer: Any recent version that supports `LoadOptions` and `PdfOptions`.
    question: What version of Aspose.CAD is needed?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Konvertera DWG till PDF – Åsidosätt kodsidodetektering i Java
url: /sv/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera DWG till PDF – Åsidosätt kodsidansdetektering i Java

I den här omfattande handledningen kommer du att lära dig **hur man konverterar DWG till PDF** samtidigt som du åsidosätter den automatiska kodsidansdetektionen som kan förstöra text. Aspose.CAD för Java ger dig exakt kontroll över teckenkodning, vilket möjliggör återställning av felaktiga CIF/MIF‑data och generering av pålitlig PDF‑utdata. Oavsett om du bygger en batch‑konverterare eller lägger till CAD‑behandling i en större Java‑tjänst, guidar stegen nedan dig genom hela arbetsflödet – från projektuppsättning till verifiering.

## Snabba svar
- **Vad betyder “override code page”?** Det tvingar Aspose.CAD att använda en specifik teckenkodning istället för att gissa.
- **Kan jag exportera DWG direkt till PDF?** Ja – efter att ha ställt in rätt kodsida kan du spara CAD‑bilden som PDF.
- **Vilken kodning fungerar för japansk text?** `CodePages.Japanese` och `MifCodePages.Japanese` är de rätta valen.
- **Behöver jag en licens för produktionsbruk?** En kommersiell licens krävs; en tillfällig licens finns tillgänglig för testning.
- **Vilken version av Aspose.CAD behövs?** Vilken som helst nyare version som stödjer `LoadOptions` och `PdfOptions`.

## Vad är “export CAD till PDF”?
Att exportera CAD till PDF omvandlar en vektor‑baserad DWG‑ritning till ett universellt visningsbart PDF‑dokument med fast layout. Konverteringen behåller alla geometriska entiteter, linjer, lager och inbäddad text, samtidigt som ritningen plattas ut till ett format som enkelt kan delas, skrivas ut, arkiveras eller bäddas in i andra applikationer utan att kräva CAD‑programvara.

## Varför åsidosätta den automatiska kodsidansdetekteringen?
Att manuellt ange kodsidan garanterar att textbytes tolkas korrekt, vilket eliminerar de förvrängda tecken som ofta uppstår när Aspose.CAD:s autodetektion gissar fel gammal kodning. Detta är avgörande för icke‑latinska skript som japanska, kyrilliska eller arabiska, och det säkerställer att den exporterade PDF‑filen matchar originaldesignen.

## Förutsättningar
- **Java‑utvecklingsmiljö** – JDK 8+ och din föredragna IDE.  
- **Aspose.CAD för Java** – Ladda ner biblioteket från den officiella sidan [here](https://releases.aspose.com/cad/java/).  
- **DWG‑exempelfil** – Använd den medföljande `SimpleEntities.dwg` eller någon annan DWG du behöver konvertera.

## Importera paket
`Document`, `LoadOptions` och `PdfOptions`‑klasserna är kärnan i konverteringsprocessen.

`Document`‑klassen representerar en CAD‑ritning i minnet och tillhandahåller metoder för att ladda, manipulera och spara filen i olika format.  
`LoadOptions`‑klassen låter dig ange kodsidan och återställningsalternativ när du laddar en DWG‑fil.  
`PdfOptions`‑klassen styr PDF‑specifika inställningar såsom komprimering, rasterisering och metadata.

I ditt Java‑projekt, importera de nödvändiga Aspose.CAD‑klasserna:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Hur man konverterar DWG till PDF med kodsidansåsidosättning?
Läs in DWG‑filen med `LoadOptions` för att ange exakt kodsida, och anropa sedan `save`‑metoden på den resulterande `CadImage` med en konfigurerad `PdfOptions`‑instans. Detta tvåstegs‑förfarande säkerställer att text tolkas korrekt och att den genererade PDF‑filen bevarar ritningens originalfidelity, lager och vektor‑kvalitet.

### Steg 1: Ställ in Java‑projektet
Skapa ett Maven‑ eller Gradle‑projekt och lägg till Aspose.CAD‑JAR‑filen i klassvägen. Detta säkerställer att IDE:n kan lösa de importerade klasserna och att körtiden kan hitta biblioteket.

### Steg 2: Läs in DWG‑filen med en specificerad kodsida
Berätta för Aspose.CAD vilken kodning som ska användas och om återställning av felaktiga CIF/MIF‑data ska försökas.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Steg 3: Exportera CAD‑bilden till PDF
Med den korrekta kodsidan tillämpad kan du säkert exportera ritningen. `PdfOptions`‑objektet låter dig finjustera PDF‑utdata (komprimering, rasterisering osv.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Steg 4: Verifiera framgång
Ett enkelt konsolmeddelande bekräftar att processen slutfördes utan undantag.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Du kan upprepa dessa steg för flera DWG‑filer, justera källsökvägen och utskriftsnamnet efter behov.

## Vanliga problem & lösningar
- **Skräptecken visas fortfarande:** Dubbelkolla att `specifiedEncoding` matchar original‑DWG:ens kodsida. Använd ett annat `CodePages`‑enum om det behövs.  
- **`NullPointerException` på `cadImage.save`:** Säkerställ att DWG‑filen laddas korrekt; verifiera sökväg och filbehörigheter.  
- **PDF‑filen är stor:** Aktivera komprimering i `PdfOptions` (t.ex. `pdfOptions.setCompress(true)`) för att minska filstorleken utan att förlora kvalitet.

## Vanliga frågor

**Q1: Är Aspose.CAD kompatibel med alla versioner av DWG‑filer?**  
A1: Aspose.CAD stödjer över 30 DWG‑versioner, inklusive AutoCAD 2018 och tidigare versioner.

**Q2: Kan jag använda Aspose.CAD för kommersiella projekt?**  
A2: Ja, en kommersiell licens krävs för produktionsbruk. Du kan skaffa en licens [here](https://purchase.aspose.com/buy).

**Q3: Finns det några begränsningar i gratis‑testversionen?**  
A1: Testversionen har storleks‑ och funktionsbegränsningar; konsultera den officiella dokumentationen för detaljer.

**Q4: Hur kan jag få support för Aspose.CAD?**  
A4: Besök community‑[Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för hjälp och diskussioner.

**Q5: Finns det en tillfällig licens för teständamål?**  
A5: Ja, en tillfällig licens kan begäras [here](https://purchase.aspose.com/temporary-license/).

---

**Senast uppdaterad:** 2026-05-20  
**Testad med:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Författare:** Aspose

## Relaterade handledningar

- [Exportera DWG till PDF och konvertera CAD‑ritningar – Aspose.CAD Java‑handledning](/cad/java/cad-drawing-conversion/)
- [Exportera specifikt DWG‑layout till PDF med Aspose.CAD för Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exportera DWG till PDF eller raster med Aspose.CAD för Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}