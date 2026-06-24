---
date: 2026-06-19
description: Konvertera enkelt DGN-filer till PDF med Aspose.CAD för Java. Följ vår
  steg-för-steg-guide för att exportera DGN till PDF, spara CAD som PDF och effektivisera
  ditt arbetsflöde.
keywords:
- convert dgn to pdf
- save cad as pdf
- export dgn to pdf
linktitle: Stöd för DGN V7
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Effortlessly convert DGN files to PDF using Aspose.CAD for Java. Follow
    our step‑by‑step guide to export DGN to PDF, save CAD as PDF, and streamline your
    workflow.
  headline: Convert DGN to PDF with Aspose.CAD for Java
  type: TechArticle
- description: Effortlessly convert DGN files to PDF using Aspose.CAD for Java. Follow
    our step‑by‑step guide to export DGN to PDF, save CAD as PDF, and streamline your
    workflow.
  name: Convert DGN to PDF with Aspose.CAD for Java
  steps:
  - name: Import Necessary Packages
    text: In your Java project, import the core Aspose.CAD classes that enable file
      loading and export.
  - name: Set File Paths
    text: Define absolute or relative paths for the source DGN file and the target
      PDF file.
  - name: Load DGN Image
    text: The `CadImage` class represents a CAD file in memory; loading the DGN file
      creates an object you can work with.
  - name: Configure PDF Export Options
    text: '`PdfExportOptions` defines settings for exporting a CAD drawing to PDF,
      such as page dimensions and layout options. Create a `PdfExportOptions` instance,
      set page size, enable automatic layout scaling, choose a background color, and
      specify which layouts to export.'
  - name: Save PDF File
    text: Call the `save` method on the `CadImage` instance, passing the output path
      and the configured `PdfExportOptions`. Repeat the above steps for each DGN file
      you need to convert, adjusting the file paths or export options as required.
  type: HowTo
- questions:
  - answer: Yes, the library supports more than 30 formats, including DWG, DXF, DWF,
      and IGES, allowing you to **export dgn to pdf** as well as many other conversions.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for evaluation purposes.
    question: Is a temporary license available for testing?
  - answer: Refer to the [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/)
      for full method signatures and usage examples.
    question: Where can I find detailed API documentation?
  - answer: Use the `setLayouts` method on `PdfExportOptions` and pass an array of
      layout names, e.g., `new String[] {"Model", "Layout1"}`.
    question: How do I specify which layouts to export?
  - answer: Wrap the steps in a loop that iterates over a directory of DGN files,
      applying the same export options to each file.
    question: What if I need to batch‑convert many DGN files?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Konvertera DGN till PDF med Aspose.CAD för Java
url: /sv/java/other-cad-operations/support-for-dgn-v7/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera DGN till PDF med Aspose.CAD för Java

I moderna CAD-miljöer är förmågan att **convert dgn to pdf** snabbt och pålitligt avgörande för att dela design med icke‑CAD‑intressenter. Aspose.CAD för Java tillhandahåller ett rent Java‑API som låter dig exportera DGN‑filer till högkvalitativa PDF‑dokument utan externa beroenden. Denna handledning guidar dig genom hela processen, från att installera biblioteket till att finjustera PDF‑exportalternativ, så att du kan integrera konverteringen i dina Java‑applikationer med förtroende.

## Snabba svar
- **Vilket bibliotek hanterar DGN‑konvertering?** Aspose.CAD for Java.
- **Kan jag exportera flera layouter?** Ja, ange layouts‑arrayen i exportalternativen.
- **Behöver jag en licens för produktion?** En giltig Aspose.CAD‑licens krävs för obegränsad användning.
- **Vilka Java‑versioner stöds?** Java 8 och senare.
- **Är konverteringen förlustfri?** PDF‑filen behåller vektorgrafik, lager och textens noggrannhet.

## Vad är convert dgn to pdf?
Convert dgn to pdf är processen att omvandla en DGN‑designfil (MicroStation) till Portable Document Format (PDF) för enkel visning, utskrift och distribution. Aspose.CAD för Java läser den inhemska DGN‑strukturen, renderar varje layout som vektorgrafik och skriver resultatet till en PDF‑fil samtidigt som geometri och textnoggrannhet bevaras.

## Varför använda Aspose.CAD för Java för att spara CAD som PDF?
Aspose.CAD kan **save CAD as PDF** för mer än 30 CAD‑format, bearbetar filer upp till 2 GB utan att ladda hela dokumentet i minnet, och levererar konverteringshastigheter upp till 5 × snabbare än konkurrerande bibliotek på vanlig serverhårdvara. API‑et kräver inga inhemska binärer, vilket gör distribution till moln‑ eller container‑miljöer sömlös.

## Förutsättningar

- **Aspose.CAD for Java Library** – ladda ner den från [Aspose.CAD for Java Download page](https://releases.aspose.com/cad/java/).
- **Java Development Environment** – JDK 8 eller nyare installerad och konfigurerad på din maskin.
- En giltig **Aspose.CAD license** för produktionsanvändning (en tillfällig licens finns tillgänglig för utvärdering).

För community‑support, besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

## Så exporterar du dgn till pdf steg för steg?

Läs in din DGN‑fil, konfigurera PDF‑exportalternativen och spara resultatet med bara några kodrader. Följande steg visar den exakta sekvensen du måste följa, och varje steg innehåller en kort kodplatshållare som du ersätter med den faktiska implementeringen från Aspose.CAD‑dokumentationen.

### Steg 1: Importera nödvändiga paket

I ditt Java‑projekt, importera de centrala Aspose.CAD‑klasserna som möjliggör filinläsning och export.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

### Steg 2: Ange filsökvägar

Definiera absoluta eller relativa sökvägar för käll‑DGN‑filen och mål‑PDF‑filen.
```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

### Steg 3: Läs in DGN‑bild

`CadImage`‑klassen representerar en CAD‑fil i minnet; inläsning av DGN‑filen skapar ett objekt som du kan arbeta med.
```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

### Steg 4: Konfigurera PDF‑exportalternativ

`PdfExportOptions` definierar inställningar för att exportera en CAD‑ritning till PDF, såsom sidstorlek och layoutalternativ.

Skapa en `PdfExportOptions`‑instans, ange sidstorlek, aktivera automatisk layoutskalning, välj en bakgrundsfärg och specificera vilka layouter som ska exporteras.
```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //only export 4 (1,2,3 and 9) views
options.setVectorRasterizationOptions(vectorOptions);
```

### Steg 5: Spara PDF‑fil

Anropa `save`‑metoden på `CadImage`‑instansen och skicka med utsökvägen samt de konfigurerade `PdfExportOptions`.
```java
objImage.save(outFile, options);
```

Upprepa ovanstående steg för varje DGN‑fil du behöver konvertera, och justera filsökvägar eller exportalternativ vid behov.

## Vanliga problem och lösningar

- **Missing layouts** – Se till att layoutnamnen du skickar till `setLayouts` exakt matchar dem i käll‑DGN‑filen; layoutnamn är skiftlägeskänsliga.
- **Out‑of‑memory errors** – För mycket stora ritningar, aktivera streaming genom att sätta `PdfExportOptions.setUseMemoryCache(true)`.
- **Incorrect colors** – Verifiera att bakgrundsfärgen är satt till `Color.WHITE` (eller önskad färg) för att undvika oväntade mörka bakgrunder i PDF‑filen.

## Vanliga frågor

**Q: Kan jag använda Aspose.CAD för Java med andra CAD‑filformat?**  
A: Ja, biblioteket stöder mer än 30 format, inklusive DWG, DXF, DWF och IGES, vilket gör att du kan **export dgn to pdf** samt många andra konverteringar.

**Q: Finns en tillfällig licens för testning?**  
A: Ja, du kan skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/) för utvärderingsändamål.

**Q: Var kan jag hitta detaljerad API‑dokumentation?**  
A: Se [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/) för fullständiga metodsignaturer och exempel.

**Q: Hur specificerar jag vilka layouter som ska exporteras?**  
A: Använd `setLayouts`‑metoden på `PdfExportOptions` och skicka en array med layoutnamn, t.ex. `new String[] {"Model", "Layout1"}`.

**Q: Vad händer om jag behöver batch‑konvertera många DGN‑filer?**  
A: Lägg stegen i en loop som itererar över en katalog med DGN‑filer och tillämpar samma exportalternativ på varje fil.

---

**Senast uppdaterad:** 2026-06-19  
**Testad med:** Aspose.CAD for Java 24.10  
**Författare:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Exportera DWG till PDF och konvertera CAD‑ritningar – Aspose.CAD Java‑handledning](/cad/java/cad-drawing-conversion/)
- [dwg till pdf java – Exportera CAD till PDF med Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Exportera CAD‑layouter till PDF med Aspose.CAD för Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}