---
date: 2025-12-01
description: Lär dig hur du ställer in PDF‑sidstorlek, konverterar DWG till PDF och
  aktiverar spårning av DWG‑ändringar med Aspose.CAD för Java.
language: sv
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Ställ in PDF‑sidstorlek och spåra DWG med Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ställ in PDF-sidstorlek och spåra DWG med Aspose.CAD Java

## Introduktion

När du samarbetar i CAD-projekt behöver du ofta **ställa in PDF-sidstorlek** för en konsekvent layout, **konvertera DWG till PDF** och hålla reda på varje förändring som görs i ritningen. Aspose.CAD för Java gör allt detta möjligt i ett enda, strömlinjeformat arbetsflöde. I den här handledningen går vi igenom de exakta stegen för att **ställa in PDF-sidstorlek**, aktivera **spårning av DWG-ändringar** och exportera ritningen som en PDF — allt med Java.

## Snabba svar
- **Hur ställer jag in PDF-sidstorleken?** Använd `CadRasterizationOptions.setPageWidth()` och `setPageHeight()` innan export.  
- **Kan jag spåra ändringar vid export?** Ja – implementera en anpassad `CadRenderHandler` för att fånga spårningsresultat.  
- **Vilken metod konverterar DWG till PDF?** Anropa `image.save(stream, pdfOptions)` efter att ha konfigurerat alternativen.  
- **Vad är de viktigaste förutsättningarna?** JDK, Aspose.CAD för Java och en mapp med DWG/DXF-filer.  
- **Krävs en licens för produktion?** Ja, en giltig Aspose.CAD-licens behövs för icke‑testdistributioner.

## Vad betyder “ställa in PDF-sidstorlek” i samband med DWG-export?

Att ställa in PDF-sidstorlek bestämmer dimensionerna på den resulterande PDF‑canvasen (bredd × höjd i pixlar). Detta är viktigt när du vill att den exporterade ritningen ska passa ett specifikt papperformat eller skärmupplägg, så att alla element visas exakt där du förväntar dig dem.

## Varför aktivera spårning vid export av DWG-filer?

Spårning (eller ändringsspårning) registrerar eventuella renderingsproblem, saknade teckensnitt eller ej stödda enheter som uppstår under konverteringen. Genom att fånga denna information kan du:

- Snabbt identifiera problem som måste åtgärdas innan slutleverans.  
- Ge tydlig återkoppling till teammedlemmar om vad som har ändrats eller utelämnats.  
- Upprätthålla en revisionsspårning för branscher med strikta efterlevnadskrav.

## Förutsättningar

- **Java Development Kit (JDK)** – någon nyare version (8+).  
- **Aspose.CAD for Java** – ladda ner från den officiella [Aspose CAD nedladdningssidan](https://releases.aspose.com/cad/java/).  
- **Document Directory** – en mapp som innehåller de DWG/DXF-filer du vill bearbeta.

## Importera namnrymder

Börja med att importera de nödvändiga Aspose.CAD-klasserna och standard Java I/O-klasserna.

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

## Steg 1: Läs in DWG‑filen (eller DXF‑filen)

Läs in din källritning i ett `Image`‑objekt. Justera sökvägen så att den pekar på din egen katalog.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Steg 2: Konfigurera PDF‑exportalternativ (inklusive sidstorlek)

Här ställer vi in PDF‑alternativen och explicit **ställer in PDF-sidstorlek** till 800 × 600 pixlar. Detta är där huvudnyckelordet tillämpas.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Steg 3: Implementera spårning

Skapa en anpassad felhanterare som kommer att ta emot spårningsinformation under konverteringsprocessen.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Steg 4: Exportera till PDF

Med alternativen och spårningshanteraren på plats, exportera ritningen. Detta steg **konverterar DWG till PDF** (eller DXF till PDF i vårt exempel).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Steg 5: CadRenderHandler‑klass – Fånga spårningsresultat

`ErrorHandler`‑klassen ärver från `CadRenderHandler` och skriver ut eventuella renderingsproblem som uppstod medan **spårning av DWG‑ändringar** filer.

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

## Vanliga problem och hur du löser dem

| Problem | Varför det händer | Lösning |
|-------|----------------|-----|
| **Saknade teckensnitt** | CAD-filen refererar till teckensnitt som inte är installerade på servern. | Installera de nödvändiga teckensnitten eller bädda in dem i källritningen. |
| **Ej stödda enheter** | Vissa DWG‑enheter stöds ännu inte av Aspose.CAD. | Använd spårningsutdata för att identifiera dem och förenkla ritningen. |
| **Fel sidstorlek** | `setPageWidth/Height` har inte anropats före export. | Se till att sidstorleken är inställd i `CadRasterizationOptions` som visat ovan. |

## Vanliga frågor

### Q1: Kan jag aktivera spårning för andra CAD‑filformat med Aspose.CAD för Java?

Aspose.CAD stödjer främst spårning för DWG/DXF‑filer. För andra format, konsultera den officiella dokumentationen för att se vilka funktioner som finns tillgängliga.

### Q2: Hur kan jag hantera ytterligare exportalternativ i Aspose.CAD för Java?

Biblioteket erbjuder många alternativ såsom DPI, bakgrundsfärg och vektorrasterisering. Utforska dem i [Aspose.CAD Java-dokumentationen](https://reference.aspose.com/cad/java/).

### Q3: Finns det en provversion av Aspose.CAD för Java?

Ja, du kan ladda ner en gratis provversion från [Aspose.CAD Free Trial](https://releases.aspose.com/).

### Q4: Var kan jag få hjälp eller diskutera problem relaterade till Aspose.CAD för Java?

Community‑forumet på [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) är en bra plats för att ställa frågor och dela erfarenheter.

### Q5: Hur får jag en tillfällig licens för Aspose.CAD för Java?

Följ stegen som beskrivs på sidan [Temporary License](https://purchase.aspose.com/temporary-license/) för att begära en tidsbegränsad licens för utvärdering.

### Q6: Kan jag **konvertera DWG till PDF** samtidigt som jag bevarar lager?

Ja. Genom att konfigurera `CadRasterizationOptions` kan du bevara lagerinformation i den resulterande PDF‑filen.

### Q7: Vad är det bästa sättet att **exportera DWG som PDF** med anpassade sidmått?

Ställ in önskad bredd och höjd med `setPageWidth` och `setPageHeight` innan du anropar `image.save()` – exakt som demonstrerat i Steg 2.

## Slutsats

Genom att följa stegen ovan kan du **ställa in PDF-sidstorlek**, **konvertera DWG till PDF** och **spåra ändringar i DWG‑filer** med Aspose.CAD för Java. Detta arbetsflöde ger dig full kontroll över utdata‑layouten samtidigt som det ger värdefulla diagnostikuppgifter som håller ditt CAD‑samarbete smidigt och felfritt. Känn dig fri att utforska ytterligare renderingsalternativ och integrera denna kod i större automatiseringspipeline.

---

**Last Updated:** 2025-12-01  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}