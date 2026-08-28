---
date: 2026-06-14
description: Lär dig hur du exporterar CAD till PDF och konverterar DGN till PDF med
  Aspose.CAD för Java. Steg‑för‑steg‑guide för Java‑utvecklare.
keywords:
- export cad to pdf
- convert dwg to pdf
- convert dgn to pdf
- java convert cad pdf
- batch convert dgn pdf
linktitle: Exportera inbäddad DGN
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  headline: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  name: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  steps:
  - name: Set Up Input and Output Paths
    text: Define the directory that contains your source file and specify the DWG
      that holds the embedded DGN.
  - name: Load DWG File
    text: '`Image` loads the DWG and automatically detects any embedded DGN data,
      exposing it for further processing.'
  - name: Configure Rasterization Options
    text: Select which layout(s) you want to include in the PDF. In this example we
      export only the **Model** layout, which is the most common view for engineering
      drawings.
  - name: Configure PDF Options
    text: Attach the rasterization settings to the PDF export options so that the
      final document respects the chosen layout and DPI.
  - name: Save PDF File
    text: Finally, write the PDF to disk using the configured options. The `save`
      method writes the configured image to the target file format on disk.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java is a commercial library. You can obtain a license
      from [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Yes, you can access a free trial of Aspose.CAD for Java [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: You can seek support from the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: What if I need a temporary license?
  - answer: The documentation is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the official documentation?
  type: FAQPage
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

I den här handledningen kommer du att upptäcka **hur man exporterar CAD till PDF** genom att konvertera en inbäddad DGN‑fil till ett högkvalitativt PDF‑dokument med Aspose.CAD för Java. Aspose.CAD är ett robust bibliotek som ger Java‑utvecklare full kontroll över CAD‑filhantering, oavsett om du behöver **konvertera DGN till PDF**, **konvertera DWG till PDF**, eller helt enkelt rendera CAD‑ritningar i andra format. Följ den steg‑för‑steg‑guiden nedan, så kan du integrera denna funktion i dina applikationer på några minuter.

## Snabba svar

- **Vad betyder “export CAD to PDF”?** Den konverterar CAD‑ritningar (DWG, DGN, etc.) till PDF‑filer samtidigt som vektor‑kvaliteten bevaras.  
- **Vilket bibliotek används?** Aspose.CAD för Java.  
- **Behöver jag en licens?** En licens krävs för produktion; en gratis provversion finns tillgänglig.  
- **Vad är de viktigaste förutsättningarna?** Java‑utvecklingsmiljö och Aspose.CAD för Java‑JAR‑filen.  
- **Kan jag anpassa resultatet?** Ja – du kan välja layouter, ställa in rasteriseringsalternativ och kontrollera PDF‑inställningarna.

## Vad är “export CAD to PDF”?

Export CAD till PDF konverterar en inbyggd CAD‑ritning (DWG, DGN, etc.) till en PDF‑fil som behåller den ursprungliga vektorgeometrin, lager och layout, vilket gör att vem som helst kan visa, skriva ut eller dela designen utan CAD‑programvara. Denna transformation skapar ett plattformsoberoende dokument som ser identiskt ut på alla zoomnivåer, vilket gör det idealiskt för samarbete och arkivering.

## Varför använda Aspose.CAD för Java för att konvertera DGN till PDF?

Aspose.CAD för Java erbjuder en ren‑Java‑lösning som eliminerar behovet av externa CAD‑verktyg, säkerställer exakt vektor‑fidelity i de resulterande PDF‑filerna och erbjuder omfattande konfigurationsalternativ såsom layoutval, DPI‑kontroll och inbäddning av teckensnitt, vilket gör den idealisk för både enkla och företagsstorskaliga konverteringsuppgifter.

- **Inga externa beroenden** – fungerar rent i Java på alla operativsystem.  
- **Bevarar vektordata** – PDF‑filer förblir skarpa på alla zoomnivåer.  
- **Fin‑granulär kontroll** – välj specifika layouter, ställ in rasteriserings‑DPI och bädda in teckensnitt.  
- **Företagsklar** – stödjer filer upp till **2 GB**, batch‑bearbetning av tusentals ritningar och flexibel licensiering.  

## Förutsättningar

Innan vi börjar, se till att du har följande:

- **Java Development Environment** – JDK 8 eller högre installerat och konfigurerat.  
- **Aspose.CAD for Java** – ladda ner den senaste JAR‑filen från [here](https://releases.aspose.com/cad/java/).  

## Importera paket

Import‑satserna importerar de nödvändiga Aspose.CAD‑klasserna till scopet.  
`Image` är kärnklassen som representerar vilken rasteriserbar CAD‑fil som helst, medan `PdfOptions` och `RasterizationOptions` låter dig finjustera PDF‑utdata.  
`CadRasterizationOptions` specificerar rasteriseringsparametrar såsom DPI, sidstorlek och layout för CAD‑rendering.

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

## Hur exporterar man CAD till PDF med Aspose.CAD för Java?

Processen börjar med att ladda DWG‑filen som innehåller den inbäddade DGN, sedan ställa in rasteriseringsparametrar för att definiera utdataupplösning och layout, bifoga dessa parametrar till ett PdfOptions‑objekt och slutligen anropa save‑metoden för att generera PDF‑filen. Detta tillvägagångssätt säkerställer högkvalitativa, vektor‑bevarande resultat med minimal kod.

Nedan följer en tydlig, numrerad genomgång som visar exakt hur man konverterar en inbäddad DGN‑fil (lagrad i en DWG) till en PDF.

### Steg 1: Ange in‑ och utdata‑sökvägar

Definiera katalogen som innehåller din källfil och ange DWG‑filen som innehåller den inbäddade DGN.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Steg 2: Ladda DWG‑fil

`Image` laddar DWG‑filen och upptäcker automatiskt eventuell inbäddad DGN‑data, vilket gör den tillgänglig för vidare bearbetning.

```java
Image objImage = Image.load(fileName);
```

### Steg 3: Konfigurera rasteriseringsalternativ

Välj vilka layout(ar) du vill inkludera i PDF‑filen. I detta exempel exporterar vi endast **Model**‑layouten, som är den vanligaste vyn för ingenjörsritningar.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Steg 4: Konfigurera PDF‑alternativ

Bifoga rasteriseringsinställningarna till PDF‑exportalternativen så att det slutgiltiga dokumentet respekterar den valda layouten och DPI‑värdet.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Steg 5: Spara PDF‑fil

Slutligen skriv PDF‑filen till disk med de konfigurerade alternativen. `save`‑metoden skriver den konfigurerade bilden till målfilformatet på disken.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Konvertera DWG till PDF – ett extra tips

Om din källfil är en vanlig DWG (utan inbäddad DGN) kan du återanvända samma kod – ändra helt enkelt `fileName` så att den pekar på den DWG du vill konvertera. Rasteriserings‑ och PDF‑alternativen förblir identiska, vilket ger dig ett konsekvent **convert DWG to PDF**‑arbetsflöde.

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|-------|--------|----------|
| **Tom PDF‑utdata** | Layoutnamn matchar inte | Verifiera att layoutnamnet som skickas till `setLayouts` exakt matchar layouten i källfilen (skiftlägeskänsligt). |
| **Licensundantag** | Använder provversion utan licens | Applicera en giltig Aspose.CAD‑licens innan bilden laddas (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Fil ej hittad** | Felaktig `dataDir`‑sökväg | Använd en absolut sökväg eller säkerställ att den relativa sökvägen är korrekt i förhållande till projektets arbetskatalog. |
| **Grafik med låg upplösning** | Standard‑DPI för rasterisering är låg | Ställ in `rasterizationOptions.setResolution(300)` eller justera `setPageWidth/Height` för att öka DPI. |

## Vanliga frågor

**Q: Kan jag använda Aspose.CAD för Java i ett kommersiellt projekt?**  
A: Ja, Aspose.CAD för Java är ett kommersiellt bibliotek. Du kan skaffa en licens från [here](https://purchase.aspose.com/buy).

**Q: Finns det en gratis provversion tillgänglig?**  
A: Ja, du kan få åtkomst till en gratis provversion av Aspose.CAD för Java [here](https://releases.aspose.com/).

**Q: Hur kan jag få support för Aspose.CAD för Java?**  
A: Du kan söka support från Aspose.CAD‑gemenskapen på [forum](https://forum.aspose.com/c/cad/19).

**Q: Vad händer om jag behöver en tillfällig licens?**  
A: Du kan skaffa en tillfällig licens [here](https://purchase.aspose.com/temporary-license/).

**Q: Var kan jag hitta den officiella dokumentationen?**  
A: Dokumentationen finns tillgänglig [here](https://reference.aspose.com/cad/java/).

## Slutsats

Du har nu lärt dig hur man **exporterar CAD till PDF**, specifikt hur man **konverterar DGN till PDF** och även **konverterar DWG till PDF** med Aspose.CAD för Java. Genom att följa stegen ovan kan du integrera sömlös CAD‑till‑PDF‑konvertering i vilken Java‑baserad lösning som helst, och leverera högkvalitativa PDF‑filer till dina användare utan behov av extra CAD‑programvara.

---

**Senast uppdaterad:** 2026-06-14  
**Testat med:** Aspose.CAD for Java 24.12  
**Författare:** Aspose

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Exportera DGN till DWG med Aspose.CAD för Java – Handledning](/cad/java/dgn-export-options/)
- [Enkel DGN‑till‑AutoCAD PDF‑export med Aspose.CAD för Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [dwg till pdf java – Exportera CAD till PDF med Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}