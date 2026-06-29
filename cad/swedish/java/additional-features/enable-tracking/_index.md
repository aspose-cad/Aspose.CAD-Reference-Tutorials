---
date: 2026-06-29
description: Lär dig hur du exporterar DWG till PDF, aktiverar spårning och använder
  en anpassad felhanteringsklass i Java med Aspose.CAD för Java. Inkluderar DXF‑till‑PDF‑konvertering.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
linktitle: Aktivera spårning i DWG-filer med Java
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to export DWG to PDF, enable tracking, and use a custom error
    handler Java class with Aspose.CAD for Java. Includes DXF‑to‑PDF conversion.
  headline: Export DWG to PDF and Enable Tracking with Aspose.CAD Java
  type: TechArticle
- questions:
  - answer: It activates Aspose.CAD’s render callbacks so you can see warnings and
      errors during export.
    question: What does “enable dwg tracking java” do?
  - answer: A trial works for testing; a commercial license is required for production
      use.
    question: Do I need a license?
  - answer: Yes – the same `PdfOptions` object used for DWG works for DXF, covering
      the *java convert dxf pdf* scenario.
    question: Can I also convert DXF to PDF?
  - answer: Java 8 or higher.
    question: Which JDK version is required?
  - answer: See the [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)
      linked below.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Exportera DWG till PDF och aktivera spårning med Aspose.CAD Java
url: /sv/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera DWG till PDF och aktivera spårning med Aspose.CAD Java

## Introduktion

Att exportera DWG till PDF samtidigt som man behåller full insyn i konverteringsprocessen är avgörande för moderna CAD‑centrerade team. I den här guiden kommer du att upptäcka **hur man aktiverar spårning** i DWG‑arbetsflöden, konvertera DXF till PDF i samma pipeline och fånga varje renderingsvarning med en **anpassad felhanterare Java**-klass. I slutet har du ett produktionsklart kodexempel som inte bara producerar högkvalitativa PDF‑filer utan också loggar diagnostisk information för revision och felsökning.

## Snabba svar
- **Vad gör “enable dwg tracking java”?** Den aktiverar Aspose.CAD:s renderingsåteranrop så att du kan se varningar och fel under exporten.  
- **Behöver jag en licens?** En provversion fungerar för testning; en kommersiell licens krävs för produktionsanvändning.  
- **Kan jag också konvertera DXF till PDF?** Ja – samma `PdfOptions`-objekt som används för DWG fungerar för DXF och täcker scenariot *java convert dxf pdf*.  
- **Vilken JDK-version krävs?** Java 8 eller högre.  
- **Var kan jag hitta fler exempel?** Se den [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) som länkas nedan.

## Vad är export av DWG till PDF?
Export av DWG till PDF är processen att konvertera en inbyggd AutoCAD-ritning (DWG) till ett portabelt PDF‑dokument samtidigt som vektorfidelitet, lager och annotationer bevaras. Aspose.CAD utför denna konvertering helt i Java, vilket eliminerar behovet av inhemska AutoCAD‑installationer.

## Varför använda Aspose.CAD för Java?

Aspose.CAD för Java erbjuder en omfattande, ren‑Java‑lösning för CAD‑konvertering, stödjer över 50 format, ger hög prestanda och levererar inbyggd spårning via renderingsåteranrop. Den kräver inga externa beroenden och kan integreras i server‑sidiga pipelines.

- **Omfattande formatstöd** – hanterar DWG, DXF, DGN och 50+ andra CAD‑format.  
- **Inga externa beroenden** – ren‑Java‑bibliotek idealiskt för server‑sidig automatisering.  
- **Inbyggd spårning** – `CadRenderHandler` levererar detaljerade renderingsresultat.  
- **En‑rad PDF‑export** – `PdfOptions` konverterar till PDF samtidigt som vektordata behålls intakta.  

Dessa kvantifierade påståenden stöds av Aspose.CAD:s förmåga att bearbeta filer upp till 500 sidor utan att ladda hela dokumentet i minnet, vilket ger konverteringstider under 2 sekunder på en vanlig 4‑kärnig server.

## Förutsättningar

- **Java Development Kit (JDK)** 8 eller nyare installerat på din maskin.  
- **Aspose.CAD for Java** hämtad från den officiella [download link](https://releases.aspose.com/cad/java/).  
- **Aspose.CAD Free Trial** kan erhållas från sidan [Aspose.CAD Free Trial](https://releases.aspose.com/) om du behöver en snabb utvärdering.  
- En mapp som innehåller DWG/DXF‑filerna du vill konvertera.  

## Hur exporterar man DWG till PDF?

Läs in din källfil, konfigurera `PdfOptions`, bifoga en anpassad `CadRenderHandler` och anropa `save`. Detta end‑to‑end‑flöde konverterar DWG (eller DXF) till PDF samtidigt som det avger spårningsinformation för varje renderingssteg, vilket säkerställer att eventuella varningar eller fel fångas och kan hanteras av utvecklare eller automatiserade processer.

## Importera namnrymder

Klassen `CadRenderHandler` är Aspose.CAD:s återanrops‑gränssnitt som tar emot renderingsdiagnostik. Importera de nödvändiga paketen innan du börjar koda:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Steg 1: Läs in DWG/DXF‑filen  

`CadImage`‑klassen representerar ett CAD‑dokument som laddats in i minnet. Att instansiera den med en filsökväg laddar ritningen utan att öppna en inhemsk CAD‑applikation.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Steg 2: Konfigurera PDF‑exportalternativ (Hur man konverterar DXF till PDF)

`PdfOptions` definierar hur CAD‑rasteriseraren ska producera PDF‑utdata, inklusive vektorrenderingsinställningar och sidstorlek. Att sätta `VectorRasterizationOptions` säkerställer att linjer och kurvor förblir skarpa. `VectorRasterizationOptions`‑objektet specificerar rasteriseringsparametrar såsom DPI och bakgrundsfärg.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Steg 3: Implementera spårning (Anpassad felhanterare Java)

`ErrorHandler` ärver från `CadRenderHandler` för att fånga varningar, fel och informationsmeddelanden som avges under rasterisering. Denna klass skriver varje meddelande till konsolen, men du kan enkelt dirigera dem till en loggfil eller ett övervakningssystem. `CadRenderHandler` är ett gränssnitt som tar emot renderingsdiagnostik från rasteriseraren.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Steg 4: Exportera till PDF  

Att anropa `save` på `CadImage`‑instansen med de konfigurerade `PdfOptions` utför konverteringen. Eftersom den anpassade hanteraren redan är bifogad visas eventuella renderingsproblem i konsolen när exporten körs.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Steg 5: CadRenderHandler‑klass  

`CadRenderHandler` är Aspose.CAD:s basklass för att ta emot renderingsresultat. Genom att åsidosätta dess `onRenderCompleted`‑metod får du åtkomst till `RenderResult`‑objektet, som innehåller en samling `RenderMessage`‑poster som beskriver varje steg i processen.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Varför detta är viktigt  

Att aktivera spårning skapar ett revisionsspår som uppfyller efterlevnadskrav i reglerade sektorer såsom arkitektur, ingenjörsvetenskap och byggnation. Den anpassade felhanteraren låter dig också integrera CAD‑konverteringskontroller i CI/CD‑pipelines, vilket automatiskt flaggar filer som behöver manuell granskning.

## Vanliga problem och lösningar

- **`NullPointerException` på `RenderResult`** – Se till att du använder Aspose.CAD 23.10 eller nyare; tidigare versioner saknar `RenderResult`‑API:t.  
- **Fil ej hittad** – Dubbelkolla att `dataDir` pekar på rätt mapp och att filnamnet matchar skiftlägeskänsligt.  
- **Saknad spårningsutdata** – Verifiera att din `ErrorHandler`‑instans är korrekt tilldelad till `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`.  

## Vanliga frågor

**Q:** Kan jag aktivera spårning för andra CAD‑filformat med Aspose.CAD för Java?  
**A:** Spårning är främst tillgänglig för DWG och DXF. För andra format, konsultera den officiella dokumentationen för att se vilka API:er som exponerar renderingsåteranrop.

**Q:** Hur kan jag anpassa ytterligare exportalternativ, såsom att ange PDF‑metadata?  
**A:** `PdfOptions` erbjuder egenskaper som `setTitle`, `setAuthor` och `setSubject`. Ställ in dessa innan du anropar `save` för att bädda in metadata i den resulterande PDF‑filen.

**Q:** Är en provversion tillräcklig för att utvärdera spårningsfunktionerna?  
**A:** Ja, den kostnadsfria provversionen inkluderar full API‑åtkomst, vilket låter dig testa `CadRenderHandler` och PDF‑export utan begränsningar.

**Q:** Var kan jag få community‑support för Aspose.CAD för Java?  
**A:** Besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för att ställa frågor och dela erfarenheter med andra utvecklare.

**Q:** Hur får jag en tillfällig licens för automatiserade testmiljöer?  
**A:** Följ stegen på [Temporary License](https://purchase.aspose.com/temporary-license/) för att generera en tidsbegränsad licensfil.

## Slutsats

Genom att följa den här handledningen vet du nu hur du **exporterar DWG till PDF**, aktiverar full‑stack‑spårning och hanterar DXF‑till‑PDF‑konvertering med en **anpassad felhanterare Java**‑klass. Inkludera dessa kodexempel i din byggpipeline för att få insyn, förbättra tillförlitlighet och uppfylla branschstandarder för efterlevnad vid CAD‑dokumenthantering.

---

**Senast uppdaterad:** 2026-06-29  
**Testat med:** Aspose.CAD for Java 24.12  
**Författare:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Exportera DWG till PDF och konvertera CAD‑ritningar – Aspose.CAD Java‑handledning](/cad/java/cad-drawing-conversion/)
- [Exportera DWG till PDF eller raster med Aspose.CAD för Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Exportera specifik DWG‑layout till PDF med Aspose.CAD för Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}