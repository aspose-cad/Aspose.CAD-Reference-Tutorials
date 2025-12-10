---
date: 2025-12-10
description: Lär dig hur du konverterar CAD till PDF med Aspose.CAD för Java samtidigt
  som du ställer in canvasstorlek, automatisk layoutskalning och exporterar till TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: Konvertera CAD till PDF – Ställ in dukstorlek och läge (Java)
url: /sv/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ställ in dukstorlek och läge

## Introduktion

Letar du efter att **konvertera CAD till PDF** samtidigt som du har full kontroll över dukstorlek och renderingsläge? Denna omfattande guide visar dig exakt hur du ställer in dukstorlek i Java, aktiverar automatisk layoutskalning och sedan exporterar resultatet till både PDF- och TIFF-format med Aspose.CAD. Oavsett om du finjusterar en produktionspipeline eller experimenterar med ett prototyp, hittar du tydliga, handlingsbara instruktioner här.

## Snabba svar
- **Vad betyder “konvertera CAD till PDF”?** Att omvandla en CAD-ritning (t.ex. DXF, DWG) till ett PDF‑dokument som kan visas på vilken plattform som helst.  
- **Kan jag också exportera till TIFF?** Ja – använd `TiffOptions` för att skapa högupplösta rasterbilder.  
- **Vilket alternativ styr dukstorlek i Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Vad är automatisk layoutskalning?** En flagga (`setAutomaticLayoutsScaling(true)`) som bevarar de ursprungliga layoutproportionerna när dukstorleken ändras.  
- **Behöver jag en licens för Aspose.CAD?** En tillfällig eller permanent licens krävs för produktionsbruk.

## Vad är **konvertera CAD till PDF**?

Att konvertera CAD till PDF innebär att ta vektorbaserade ingenjörsritningar och rendera dem som PDF‑sidor, bevara linjearbete, lager och geometri samtidigt som filen blir universellt åtkomlig.

## Varför ställa in dukstorlek **java**?

Att ställa in dukstorlek i Java låter dig definiera utskriftsupplösning och sidmått, så att den resulterande PDF‑ eller TIFF‑filen matchar dina tryck‑ eller visningskrav. Det ger dig också kontroll över skalningsbeteende, vilket är avgörande för stora formatritningar.

## Förutsättningar

Innan du dyker ner i handledningen, se till att du har följande förutsättningar på plats:

- Aspose.CAD för Java: Säkerställ att du har Aspose.CAD‑biblioteket installerat i din Java‑miljö. Du kan ladda ner det [här](https://releases.aspose.com/cad/java/).

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

## Steg 2: Ställ in **CadRasterizationOptions**‑egenskaper (ställ in dukstorlek java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Här skapar vi en instans av `CadRasterizationOptions` och konfigurerar egenskaper som sidbredd, sidhöjd och **automatisk layoutskalning**. Detta är kärnan i **konfigurera dukläge** för din konvertering.

## Steg 3: Skapa PdfOptions och sätt VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nu skapar vi en `PdfOptions`‑instans och sätter dess `VectorRasterizationOptions`‑egenskap till den tidigare konfigurerade `CadRasterizationOptions`.

## Steg 4: Exportera till PDF (konvertera cad till pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Slutligen sparar vi CAD‑bilden till en PDF‑fil med de angivna alternativen, vilket fullbordar **konvertera CAD till PDF**‑processen.

## Steg 5: Skapa TiffOptions och sätt VectorRasterizationOptions (exportera cad till tiff)

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

Till sist sparar vi CAD‑bilden till en TIFF‑fil med de angivna alternativen, och demonstrerar hur du **exporterar CAD till TIFF** efter att ha konfigurerat dukstorlek.

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|---------|-------|----------|
| Utdata-PDF är tom | `setNoScaling(true)` inaktiverar rendering för vissa ritningar | Ta bort `setNoScaling(true)` eller sätt den till `false`. |
| TIFF-upplösning ser låg ut | Sidbredd/sidhöjd för liten | Öka värdena för `setPageWidth` / `setPageHeight`. |
| Layouten ser förvrängd ut | Automatisk layoutskalning inaktiverad | Säkerställ att `setAutomaticLayoutsScaling(true)` är aktiverad. |

## Slutsats

Grattis! Du har framgångsrikt **konverterat CAD till PDF** och **exporterat CAD till TIFF** medan du **ställde in dukstorlek java**, aktiverade **automatisk layoutskalning**, och lärde dig hur du **konfigurerar dukläge** för högkvalitativa resultat. Denna handledning ger en solid grund för dina CAD‑konverteringsprojekt. Utforska fler funktioner och möjligheter i [Aspose.CAD‑dokumentationen](https://reference.aspose.com/cad/java/).

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD för Java med andra Java‑ramverk?

A1: Ja, Aspose.CAD är designat för att sömlöst integreras med olika Java‑ramverk.

### Q2: Finns en tillfällig licens för Aspose.CAD?

A2: Ja, du kan skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

### Q3: Var kan jag få community‑support för Aspose.CAD?

A3: Besök [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19) för community‑support och diskussioner.

### Q4: Kan jag prova Aspose.CAD gratis?

A4: Absolut! Få en gratis provversion [här](https://releases.aspose.com/).

### Q5: Hur köper jag Aspose.CAD för Java?

A5: Köp produkten [här](https://purchase.aspose.com/buy).

**Ytterligare Q&A**

**Q: Påverkar dukstorleken vektor­kvaliteten i PDF‑filen?**  
A: Nej. Dukstorleken styr sidmåtten; vektordata förblir upplösningsoberoende, vilket säkerställer skarp rendering vid alla zoomnivåer.

**Q: Kan jag ange ett annat DPI‑värde för TIFF‑utdata?**  
A: Ja. Justera `rasterizationOptions.setResolution(dpiValue)` innan du skapar `TiffOptions`.

---

**Senast uppdaterad:** 2025-12-10  
**Testad med:** Aspose.CAD för Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}