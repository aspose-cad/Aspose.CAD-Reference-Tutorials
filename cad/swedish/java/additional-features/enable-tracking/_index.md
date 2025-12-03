---
date: 2025-12-03
description: Lär dig hur du ställer in PDF‑sidstorlek när du konverterar DWG till
  PDF och aktiverar spårning i DWG‑filer med Aspose.CAD för Java – en komplett guide
  för att exportera CAD‑ritningar till PDF med precision.
language: sv
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Ställ in PDF-sidstorlek och aktivera spårning i DWG-filer med Aspose.CAD i
  Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ställ in PDF-sidstorlek och aktivera spårning i DWG-filer med Aspose.CAD i Java

## Introduktion

Om du behöver **set PDF page size** när du *convert DWG to PDF* och även hålla koll på eventuella renderingsproblem, ger Aspose.CAD för Java dig ett rent, programatiskt sätt att göra båda. I den här handledningen går vi igenom de exakta stegen för att konfigurera siddimensionerna, aktivera spårning och exportera en CAD‑ritnings‑PDF — allt från Java. I slutet förstår du varför rätt sidstorlek är viktigt för CAD‑ritningar och hur du fångar detaljerad spårningsinformation under exportprocessen.

## Snabba svar
- **What does “set PDF page size” affect?** Det definierar bredden och höjden på den resulterande PDF‑canvasen, så att din ritning passar perfekt.  
- **Do I need a license to use this feature?** En provversion fungerar för testning; en kommersiell licens krävs för produktion.  
- **Which Aspose.CAD version is required?** Vilken som helst ny version som stödjer `CadRasterizationOptions`.  
- **Can I use this with other CAD formats?** Exemplet visar DWG/DXF, men samma metod fungerar för de flesta stödda format.  
- **How long does the conversion take?** Vanligtvis under en sekund för mindre filer; större ritningar kan ta längre tid.

## Vad betyder “set PDF page size” i samband med CAD-export?
Att ställa in PDF‑sidstorlek talar om för renderaren de exakta dimensionerna (i pixlar eller punkter) för utdata‑canvasen. Detta är särskilt viktigt för tekniska ritningar där skala och layout måste bevaras. Utan explicita sidstorleksinställningar kan PDF‑filen standardiseras till en storlek som beskär eller förvränger ritningen.

## Varför ställa in PDF-sidstorlek vid export av CAD-ritningar?
- **Bevara skala** – Ingenjörer förlitar sig på skala‑korrekta utskrifter.  
- **Anpassa till papper** – Välj A4, Letter eller en anpassad storlek som matchar projektspecifikationerna.  
- **Förbättra läsbarhet** – Större sidor kan visa fina detaljer utan zoom.  
- **Enhetlig output** – Automatiserade pipelines skapar PDF:er med identiska dimensioner varje körning.

## Hur ställer man in PDF-sidstorlek när man konverterar DWG till PDF?
Nedan konfigurerar vi `CadRasterizationOptions` med anpassade bredd‑ och höjdvärden innan export. Detta steg adresserar direkt huvudnyckelordet **set PDF page size**.

## Förutsättningar

- **Java Development Kit (JDK)** – Java 8 eller nyare installerat på din maskin.  
- **Aspose.CAD for Java** – Ladda ner från den officiella [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Dokumentkatalog** – En mapp som innehåller de DWG/DXF-filer du vill bearbeta.

## Importera namnrymder

Först importerar du de klasser du behöver. Kodblocket är oförändrat från den ursprungliga handledningen.

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

## Steg 1: Ladda DWG/DXF-filen

Läs in din källritning. Justera sökvägen så att den pekar på din egen fil.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Steg 2: Konfigurera PDF-exportalternativ (inklusive sidstorlek)

Här sätter vi sidbredd och -höjd — detta är där vi **set PDF page size**. Värdena är i pixlar; du kan konvertera från tum eller millimeter vid behov.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Tip:** Om du föredrar standardpappersstorlekar, använd konverteringen `1 inch = 72 points`. För en A4‑sida (8.27 × 11.69 in), sätt `pageWidth = 595` och `pageHeight = 842`.

## Steg 3: Implementera spårning

Spårning fångar eventuella renderingsproblem. Vi bifogar en anpassad hanterare som kommer att anropas efter exporten.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Steg 4: Exportera till PDF

Nu utför du konverteringen. PDF‑filen skapas med de dimensioner du angav, och all spårningsinformation skrivs ut i konsolen.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Steg 5: CadRenderHandler-klass

Hantera­ren skriver ut eventuella fel som inträffade under renderingen. Detta hjälper dig att felsöka problem när du **exporting CAD drawing PDF**.

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

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|-------|-------|-----|
| **Blank PDF** | Sidstorlek satt till 0 eller för liten | Verifiera att `setPageWidth` och `setPageHeight` har positiva värden. |
| **Missing geometry** | Renderingsfel fångade av hanteraren | Granska konsolutdata från `ErrorHandler` och åtgärda den specifika `RenderCode`. |
| **File not found** | Felaktig `dataDir`‑sökväg | Använd en absolut sökväg eller säkerställ att katalogen finns. |
| **License exception** | Använder provversion utan giltig licens för stora filer | Applicera din Aspose.CAD‑licens innan du laddar bilden. |

## Vanliga frågor

**Q: Can I enable tracking for other CAD file formats using Aspose.CAD for Java?**  
A: Aspose.CAD stödjer främst DWG/DXF för spårning. För andra format, konsultera den officiella dokumentationen.

**Q: How can I handle additional export options in Aspose.CAD for Java?**  
A: Biblioteket erbjuder många alternativ såsom DPI, bakgrundsfärg och vektor‑rasterisering. Se [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) för detaljer.

**Q: Is there a trial version available for Aspose.CAD for Java?**  
A: Ja, du kan ladda ner en gratis provversion från [Aspose.CAD Free Trial](https://releases.aspose.com/).

**Q: Where can I seek assistance or discuss issues related to Aspose.CAD for Java?**  
A: Besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för community‑stöd och officiella svar.

**Q: How do I obtain a temporary license for Aspose.CAD for Java?**  
A: Följ stegen som beskrivs på sidan [Temporary License](https://purchase.aspose.com/temporary-license/).

**Senast uppdaterad:** 2025-12-03  
**Testad med:** Aspose.CAD for Java 24.11 (senaste vid tidpunkten för skrivandet)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}