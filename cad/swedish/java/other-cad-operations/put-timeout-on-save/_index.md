---
date: 2026-06-19
description: Lär dig hur du ställer in timeout vid sparande av CAD-ritningar med Aspose.CAD
  för Java. Öka prestanda, undvik hängningar och exportera CAD till PDF effektivt.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: Sätt timeout vid sparande
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
title: Hur man ställer in timeout vid sparande för CAD med Aspose.CAD
url: /sv/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man anger timeout vid sparande för CAD med Aspose.CAD

## Introduktion

I den här omfattande guiden kommer du att lära dig **hur man anger timeout** när du sparar CAD‑ritningar med Aspose.CAD för Java. Att använda en timeout förhindrar att långvariga sparoperationer hänger din applikation, vilket är särskilt viktigt när du behöver **exportera CAD till PDF** eller **konvertera DWG till PDF** i batch‑bearbetningsscenarier. Aspose.CAD för Java stödjer mer än 50 CAD‑format och kan hantera filer med flera hundra sidor utan att ladda hela dokumentet i minnet, vilket ger dig förutsägbar prestanda och resursanvändning.

## Snabba svar
- **Vad gör timeouten?** Den avbryter sparningsoperationen efter en angiven period, frigör tråden och förhindrar resurssläpp.  
- **Vilken klass styr timeouten?** `InterruptionTokenSource` tillhandahåller avbokningstoken som används av sparningsrutinen.  
- **Kan jag fortfarande exportera CAD till PDF efter en timeout?** Ja – du kan fånga avbrottsundantaget och försöka igen eller logga felet.  
- **Behöver jag en speciell licens?** En vanlig Aspose.CAD‑licens räcker; timeout‑funktionen är inbyggd.  
- **Är detta tillvägagångssätt trådsäkert?** Ja, när varje sparning körs i sin egen tråd med sin egen token.

## Vad är en timeout i CAD‑sparoperationer?
En timeout är en konfigurerbar tidsgräns som, när den överskrids, tvingar sparprocessen att stoppa och kasta ett avbrottsundantag. Detta skyddar din Java‑applikation från oändliga hängningar som orsakas av komplexa ritningar eller I/O‑flaskhalsar.

## Varför ange en timeout när du sparar CAD‑filer?
Aspose.CAD kan **konvertera DWG till PDF** och **exportera CAD till PDF** på under en sekund för typiska ritningar, men extremt stora eller korrupta filer kan ta minuter. Genom att definiera en timeout garanterar du att ingen enskild sparning överskrider exempelvis 30 sekunder, vilket håller den totala batch‑genomströmningen stabil och förhindrar trådstjärning.

## Förutsättningar

Innan du dyker ner i handledningen, se till att du har följande förutsättningar på plats:
- **Aspose.CAD for Java Library** – Säkerställ att du har Aspose.CAD för Java‑biblioteket integrerat i ditt projekt. Du kan ladda ner biblioteket från [website](https://releases.aspose.com/cad/java/).
- **Development Environment** – Ställ in din Java‑utvecklingsmiljö med alla nödvändiga verktyg och beroenden.

## Importera paket

För att komma igång, importera de nödvändiga paketen i ditt Java‑projekt. Lägg till följande rader i början av din Java‑fil:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Nu ska vi gå igenom exempel­koden steg för steg:

## Hur man anger timeout vid sparande av CAD‑ritningar?

Läs in din CAD‑fil, skapa ett `InterruptionTokenSource` med önskad timeout och skicka token till PDF‑sparalternativen. Om operationen överskrider timeouten kastar Aspose.CAD ett `OperationCanceledException`, som du kan fånga för att hantera felet på ett smidigt sätt.

### Steg 1: Ange käll‑ och målmappar

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Se till att du har rätt käll‑ och målmappar för dina CAD‑ritningar.

### Steg 2: Skapa Interruption Token Source

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Initiera en avbrottstokenkälla för att hantera avbrott under sparoperationen.

### Steg 3: Ladda CAD‑ritning

`CadImage`‑klassen är Aspose.CAD:s kärnobjekt som representerar en CAD‑ritning i minnet och erbjuder metoder för rendering och konvertering.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### Steg 4: Konfigurera rasteriseringsalternativ

`CadRasterizationOptions` specificerar hur CAD‑ritningen rasteriseras till en bild.

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Konfigurera rasteriseringsalternativ för CAD‑ritningen.

### Steg 5: Konfigurera PDF‑alternativ

`PdfOptions` definierar inställningar för att spara en CAD‑ritning som ett PDF‑dokument.

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Ställ in PDF‑alternativ med vektor‑rasteriseringsalternativ och avbrottstoken.

### Steg 6: Spara ritning med timeout

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Spara CAD‑ritningen till en PDF‑fil med den angivna timeouten.

### Steg 7: Hantera avbrott

`OperationCanceledException` kastas när en sparoperation överskrider den angivna timeouten.

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

Skapa en tråd för att hantera sparoperationen och avbryt den efter en specificerad timeout.

## Vanliga problem och lösningar

- **Timeout för kort** – Om du får frekventa avbrott, öka timeout‑värdet för att rymma större ritningar.  
- **InterruptedException fångas inte** – Omslut alltid sparningsanropet i ett try‑catch‑block för `OperationCanceledException` för att förhindra att applikationen kraschar.  
- **Minnesanvändning** – Använd `PdfOptions.setVectorRasterizationOptions` för att strömma utdata istället för att ladda hela filen i minnet.

## Vanliga frågor

**Q: Kan jag använda den här funktionen för att konvertera DWG till PDF i ett batch‑jobb?**  
A: Ja, omslut varje konvertering i sin egen tråd med en separat avbrottstoken för att upprätthålla tidsgränser per fil.

**Q: Fungerar timeouten på alla utdataformat?**  
A: Timeout‑mekanismen är knuten till `InterruptionTokenSource` och fungerar med alla format som respekterar token, inklusive PDF, PNG och SVG.

**Q: Vad händer med delvis skrivna filer efter en timeout?**  
A: Aspose.CAD kastar automatiskt bort ofullständig output, så du får inga korrupta PDF‑filer.

**Q: Krävs en licens för produktionsanvändning?**  
A: Ja, en giltig Aspose.CAD‑licens krävs för kommersiella distributioner; en gratis provversion finns tillgänglig för utvärdering.

**Q: Var kan jag hitta fler exempel på användning av avbrottstoken?**  
A: Den officiella Aspose.CAD‑dokumentationen innehåller ytterligare kodsnuttar och bästa praxis‑riktlinjer.

## Ytterligare resurser

- [releases page](https://releases.aspose.com/cad/java/) – Direkt nedladdningssida för de senaste Aspose.CAD för Java‑utgåvorna.  
- [documentation](https://reference.aspose.com/cad/java/) – Fullständig API‑referens och utvecklarguider.  
- [this link](https://releases.aspose.com/) – Allmänna Aspose‑produktutgåvor.  
- [here](https://purchase.aspose.com/temporary-license/) – Skaffa en tillfällig licens för testning.  
- [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) – Community‑support och diskussioner.

## Slutsats

Du har nu lärt dig **hur man anger timeout** för att spara CAD‑ritningar med Aspose.CAD för Java. Genom att integrera ett `InterruptionTokenSource` i ditt arbetsflöde kan du på ett pålitligt sätt **exportera CAD till PDF** eller **konvertera DWG till PDF** utan att riskera långvariga hängningar, vilket håller din applikation responsiv och skalbar.

---

**Last Updated:** 2026-06-19  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Exportera DWG till PDF eller raster med Aspose.CAD för Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Exportera specifikt DWG‑layout till PDF med Aspose.CAD för Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Konvertera DWG till PNG och andra rasterformat med Aspose.CAD för Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}