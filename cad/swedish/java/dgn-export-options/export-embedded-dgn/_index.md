---
date: 2026-01-07
description: Lär dig hur du exporterar CAD till PDF och konverterar DGN till PDF med
  Aspose.CAD för Java. Steg‑för‑steg‑guide för Java‑utvecklare.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: Exportera CAD till PDF – Exportera inbäddad DGN med Aspose.CAD för Java
url: /sv/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera CAD till PDF – Exportera inbäddad DGN med Aspose.CAD för Java

## Introduktion

I den här handledningen kommer du att upptäcka **how to export CAD to PDF** genom att konvertera en inbäddad DGN‑fil till ett högkvalitativt PDF‑dokument med Aspose.CAD för Java. Aspose.CAD är ett robust bibliotek som ger Java‑utvecklare full kontroll över CAD‑filhantering, oavsett om du behöver **convert DGN to PDF**, **convert DWG to PDF**, eller helt enkelt rendera CAD‑ritningar i andra format. Följ den steg‑för‑steg‑guide som följer, så kan du integrera denna funktion i dina applikationer på några minuter.

## Snabba svar
- **What does “export CAD to PDF” mean?** Det konverterar CAD‑ritningar (DWG, DGN osv.) till PDF‑filer samtidigt som vektorkvaliteten bevaras.  
- **Which library is used?** Aspose.CAD för Java.  
- **Do I need a license?** En licens krävs för produktion; en gratis provversion finns tillgänglig.  
- **What are the main prerequisites?** Java‑utvecklingsmiljö och Aspose.CAD för Java‑JAR‑filen.  
- **Can I customize the output?** Ja – du kan välja layouter, ställa in rasteriseringsalternativ och kontrollera PDF‑inställningarna.

## Vad är “export CAD to PDF”?

Att exportera CAD till PDF innebär att ta en inbyggd CAD‑fil (såsom DWG eller DGN) och generera ett PDF‑dokument som troget återger den ursprungliga geometrin. PDF‑filen kan visas på vilken plattform som helst utan att behöva CAD‑programvara, vilket gör den idealisk för delning, utskrift eller arkivering.

## Varför använda Aspose.CAD för Java för att konvertera DGN till PDF?

- **No external dependencies** – fungerar enbart i Java.  
- **Preserves vector data** – PDF‑filer förblir skarpa på alla zoomnivåer.  
- **Fine‑grained control** – välj specifika layouter, ställ in rasteriserings‑DPI och bädda in typsnitt.  
- **Enterprise‑ready** – stödjer stora filer, batch‑bearbetning och licensalternativ.

## Förutsättningar

Innan vi börjar, se till att du har följande:

- **Java Development Environment** – JDK 8 eller högre installerad och konfigurerad.  
- **Aspose.CAD for Java** – ladda ner den senaste JAR‑filen från [here](https://releases.aspose.com/cad/java/).

## Importera paket

För att komma igång måste du importera de nödvändiga klasserna i ditt Java‑projekt. Lägg till följande import‑satser i din källfil:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Hur exporterar man DGN till PDF med Aspose.CAD för Java?

Nedan följer en tydlig, numrerad genomgång som visar exakt hur du konverterar en inbäddad DGN‑fil (lagrad i en DWG) till en PDF.

### Steg 1: Ställ in in‑ och utdata‑sökvägar

Definiera katalogen som innehåller din källfil och ange DWG‑filen som innehåller den inbäddade DGN‑filen.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Steg 2: Läs in DWG‑fil

Läs in DWG‑filen i ett `Image`‑objekt. Aspose.CAD upptäcker automatiskt inbäddad DGN‑data.

```java
Image objImage = Image.load(fileName);
```

### Steg 3: Konfigurera rasteriseringsalternativ

Välj vilka layout(ar) du vill inkludera i PDF‑filen. I det här exemplet exporterar vi endast **Model**‑layouten.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Steg 4: Konfigurera PDF‑alternativ

Bifoga rasteriseringsinställningarna till PDF‑exportalternativen.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Steg 5: Spara PDF‑fil

Skriv slutligen PDF‑filen till disk med de konfigurerade alternativen.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Konvertera DWG till PDF – ett extra tips

Om din källfil är en vanlig DWG (utan inbäddad DGN) kan du återanvända samma kod – ändra helt enkelt `fileName` så att den pekar på den DWG du vill konvertera. Rasteriserings‑ och PDF‑alternativen förblir identiska, vilket ger dig ett konsekvent **convert DWG to PDF**‑arbetsflöde.

## Vanliga problem och lösningar

| Issue | Reason | Solution |
|-------|--------|----------|
| **Tom PDF‑utdata** | Layoutnamn matchar inte | Verifiera att layoutnamnet som skickas till `setLayouts` exakt matchar layouten i källfilen (skiftlägeskänsligt). |
| **Licensundantag** | Använder provversionen utan licens | Applicera en giltig Aspose.CAD‑licens innan bilden laddas (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Fil ej hittad** | Felaktig `dataDir`‑sökväg | Använd en absolut sökväg eller säkerställ att den relativa sökvägen är korrekt i förhållande till projektets arbetskatalog. |
| **Grafik med låg upplösning** | Standard‑DPI för rasterisering är låg | Ställ in `rasterizationOptions.setPageWidth/Height` eller `setResolution` för att öka DPI. |

## Vanliga frågor

**Q: Kan jag använda Aspose.CAD för Java i ett kommersiellt projekt?**  
A: Ja, Aspose.CAD för Java är ett kommersiellt bibliotek. Du kan skaffa en licens från [here](https://purchase.aspose.com/buy).

**Q: Finns det en gratis provversion tillgänglig?**  
A: Ja, du kan få åtkomst till en gratis provversion av Aspose.CAD för Java [here](https://releases.aspose.com/).

**Q: Hur kan jag få support för Aspose.CAD för Java?**  
A: Du kan söka support från Aspose.CAD‑gemenskapen på [forum](https://forum.aspose.com/c/cad/19).

**Q: Vad händer om jag behöver en tillfällig licens?**  
A: Du kan skaffa en tillfällig licens [here](https://purchase.aspose.com/temporary-license/).

**Q: Var kan jag hitta dokumentationen?**  
A: Dokumentationen finns tillgänglig [here](https://reference.aspose.com/cad/java/).

## Slutsats

Du har nu lärt dig hur du **export CAD to PDF**, specifikt hur du **convert DGN to PDF** och även **convert DWG to PDF** med Aspose.CAD för Java. Genom att följa stegen ovan kan du integrera sömlös CAD‑till‑PDF‑konvertering i vilken Java‑baserad lösning som helst, och leverera högkvalitativa PDF‑filer till dina användare utan behov av extra CAD‑programvara.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose