---
date: 2026-02-15
description: Lär dig hur du ställer in PDF‑sidstorlek och konverterar CAD till PDF
  med Aspose.CAD för Java, med automatisk layoutskalning och TIFF‑export.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: Ställ in PDF‑sidstorlek – Konvertera CAD till PDF (Java)
url: /sv/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ställ in dukstorlek och läge

## Introduktion

Om du behöver **ange PDF‑sidstorlek** när du konverterar CAD‑ritningar till PDF, har du kommit till rätt ställe. I den här handledningen visar vi hur du använder Aspose.CAD för Java för att definiera exakta dukdimensioner, aktivera automatisk layoutskalning och sedan exportera resultatet till både PDF och TIFF. Oavsett om du förbereder ingenjörsscheman för utskrift eller genererar miniatyrbilder för ett webb‑galleri, är kontroll av sidstorlek och utdata‑upplösning avgörande.

## Snabba svar
- **Vad betyder “convert CAD to PDF”?** Att omvandla en CAD‑ritning (t.ex. DXF, DWG) till ett PDF‑dokument som kan visas på vilken plattform som helst.  
- **Kan jag också exportera till TIFF?** Ja — använd `TiffOptions` för att skapa högupplösta rasterbilder.  
- **Vilket alternativ styr dukstorlek i Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Vad är automatisk layoutskalning?** En flagga (`setAutomaticLayoutsScaling(true)`) som bevarar de ursprungliga layoutproportionerna när dukstorleken ändras.  
- **Behöver jag en licens för Aspose.CAD?** En tillfällig eller permanent licens krävs för produktionsanvändning.

## Hur du anger PDF‑sidstorlek när du konverterar CAD till PDF (Java)

Att ange PDF‑sidstorlek (eller dukstorlek) låter dig bestämma dokumentets slutliga dimensioner, vilket är särskilt användbart när du måste **ändra PDF‑dimensioner** för att matcha utskriftsstandarder eller UI‑krav. Nedan går vi igenom varje steg och förklarar *varför* bakom varje kodrad.

## Vad är **convert CAD to PDF**?

Att konvertera CAD till PDF innebär att ta vektorbaserade ingenjörsritningar och rendera dem som PDF‑sidor, samtidigt som linjearbete, lager och geometri bevaras och filen blir universellt åtkomlig.

## Varför ange dukstorlek **java**?

Att ange dukstorlek i Java låter dig definiera utdata‑upplösning och siddimensioner, så att den resulterande PDF‑ eller TIFF‑filen matchar dina utskrifts‑ eller visningskrav. Det ger dig också kontroll över skalningsbeteendet, vilket är viktigt för stora formatritningar.

## Förutsättningar

Innan du dyker ner i handledningen, se till att du har följande förutsättningar på plats:

- Aspose.CAD för Java: Säkerställ att du har Aspose.CAD‑biblioteket installerat i din Java‑miljö. Du kan ladda ner det [here](https://releases.aspose.com/cad/java/).
- Dokumentkatalog: Skapa en dokumentkatalog för att lagra dina CAD‑filer. Denna katalog kommer att refereras i handledningens steg.

Nu sätter vi igång med steg‑för‑steg‑guiden.

## Importera namnrymder

I detta steg importerar vi de nödvändiga namnrymderna för att kickstarta ditt Aspose.CAD‑projekt.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Steg 1: Importera Aspose.CAD‑klasser

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

I detta kodsnutt sätter vi upp sökvägen till resurskatalogen och laddar en DXF‑fil med Aspose.CAD:s `Image`‑klass.

## Steg 2: Ange **CadRasterizationOptions**‑egenskaper (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Här skapar vi en instans av `CadRasterizationOptions` och konfigurerar egenskaper som sidbredd, sidhöjd och **automatisk layoutskalning**. Detta är kärnan i **configure canvas mode** för din konvertering.

## Steg 3: Skapa PdfOptions och ange VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nu skapar vi en `PdfOptions`‑instans och sätter dess `VectorRasterizationOptions`‑egenskap till den tidigare konfigurerade `CadRasterizationOptions`.

## Steg 4: Exportera till PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Slutligen sparar vi CAD‑bilden till en PDF‑fil med de angivna alternativen, vilket fullbordar **convert CAD to PDF**‑processen.

## Steg 5: Skapa TiffOptions och ange VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

I detta steg sätter vi upp en `TiffOptions`‑instans och konfigurerar dess `VectorRasterizationOptions`‑egenskap.

## Steg 6: Exportera till TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Till sist sparar vi CAD‑bilden till en TIFF‑fil med de angivna alternativen, vilket demonstrerar hur man **export CAD to TIFF** efter att ha konfigurerat dukstorlek.

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|---------|-------|---------|
| Utdata‑PDF är tom | `setNoScaling(true)` inaktiverar rendering för vissa ritningar | Ta bort `setNoScaling(true)` eller sätt den till `false`. |
| TIFF‑upplösning ser låg ut | Sidbredd/sidhöjd för liten | Öka värdena för `setPageWidth` / `setPageHeight`. |
| Layouten ser förvrängd ut | Automatisk layoutskalning inaktiverad | Säkerställ att `setAutomaticLayoutsScaling(true)` är aktiverad. |

## Varför justera dukstorlek och DPI?

Att ändra dukstorleken påverkar direkt rasteriseringsupplösningen för utdata. Om du behöver **öka TIFF‑upplösning**, höj helt enkelt `setPageWidth` / `setPageHeight`‑värdena eller anropa `rasterizationOptions.setResolution(300)` innan du skapar `TiffOptions`. Detta ger dig högkvalitativa rasterbilder som är lämpliga för utskrift eller detaljerad granskning.

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD för Java med andra Java‑ramverk?

A1: Ja, Aspose.CAD är designat för att sömlöst integreras med olika Java‑ramverk.

### Q2: Finns en tillfällig licens för Aspose.CAD?

A2: Ja, du kan skaffa en tillfällig licens [here](https://purchase.aspose.com/temporary-license/).

### Q3: Var kan jag få community‑support för Aspose.CAD?

A3: Besök [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19) för community‑support och diskussioner.

### Q4: Kan jag prova Aspose.CAD gratis?

A4: Absolut! Få en gratis provversion [here](https://releases.aspose.com/).

### Q5: Hur köper jag Aspose.CAD för Java?

A5: Köp produkten [here](https://purchase.aspose.com/buy).

**Ytterligare Q&A**

**Q: Påverkar dukstorleken vektor­kvaliteten i PDF‑filen?**  
A: Nej. Dukstorleken styr siddimensionerna; vektordata förblir upplösningsoberoende, vilket säkerställer skarp rendering på alla zoomnivåer.

**Q: Kan jag ange en annan DPI för TIFF‑utdata?**  
A: Ja. Justera `rasterizationOptions.setResolution(dpiValue)` innan du skapar `TiffOptions`.

**Q: Hur kan jag **change PDF dimensions** för en befintlig PDF utan att rendera om CAD?**  
A: Använd Aspose.PDF för att ladda den genererade PDF‑filen och anropa `pdf.getPages().setPageSize(PageSize.A4)` eller en anpassad storlek.

**Q: Vad är det bästa sättet att **convert dxf to pdf** samtidigt som lager bevaras?**  
A: Behåll `setAutomaticLayoutsScaling(true)` och undvik `setNoScaling(true)`; detta behåller lagersynlighet och layout‑fidelity.

## Slutsats

Grattis! Du har framgångsrikt **convert CAD to PDF** och **export CAD to TIFF** medan du **set canvas size java**, aktiverat **automatic layout scaling** och lärt dig hur du **configure canvas mode** för högkvalitativa resultat. Denna handledning ger en solid grund för dina CAD‑konverteringsprojekt. Utforska fler funktioner och möjligheter i [Aspose.CAD‑dokumentationen](https://reference.aspose.com/cad/java/).

---

**Senast uppdaterad:** 2026-02-15  
**Testat med:** Aspose.CAD för Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}