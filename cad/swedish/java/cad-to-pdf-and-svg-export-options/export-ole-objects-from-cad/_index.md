---
date: 2026-01-04
description: Lär dig hur du **sparar CAD som PNG** och enkelt exporterar OLE‑objekt
  från CAD‑filer med Aspose.CAD för Java. Snabb installation, komplett kodexempel
  och bästa‑praxis‑tips.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Spara CAD som PNG och exportera OLE‑objekt med Aspose.CAD för Java
url: /sv/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara CAD som PNG och exportera OLE-objekt med Aspose.CAD för Java

## Introduktion

I den snabbrörliga världen av Computer‑Aided Design (CAD) kan möjligheten att **spara CAD som PNG** samtidigt som du extraherar inbäddade OLE (Object Linking and Embedding)-objekt dramatiskt förenkla ditt arbetsflöde. Oavsett om du bygger ett batch‑konverteringsverktyg, genererar miniatyrbilder för en webbportal eller helt enkelt behöver arkivera OLE‑innehåll, ger Aspose.CAD för Java dig ett rent, programmerbart sätt att göra det. I den här handledningen går vi igenom hela processen, från att konfigurera ditt projekt till att exportera varje OLE‑objekt som en PNG‑bild.

## Snabba svar
- **Kan jag exportera OLE‑objekt direkt till PNG?** Ja – Aspose.CAD läser in CAD‑filen och låter dig rasterisera varje layout till PNG.  
- **Vilken Java‑version krävs?** Java 8 eller senare.  
- **Behöver jag en licens för den här funktionen?** En gratis provversion fungerar för utvärdering; en licens krävs för produktion.  
- **Kommer vektordata att bevaras?** PNG‑rasteriseringen behåller den visuella kvaliteten, men resultatet är raster, inte vektor.  
- **Stöds batch‑behandling?** Absolut – iterera över en array av filer som visas i kodexemplet.

## Förutsättningar

Innan du börjar, se till att du har följande:

- **Java Development Kit (JDK)** – Java 8+ installerat och konfigurerat.  
- **Aspose.CAD for Java** – Ladda ner det senaste biblioteket från [nedladdningslänk](https://releases.aspose.com/cad/java/).  
- **CAD‑källfiler** – Alla DWG/DXF/DGN‑filer som innehåller OLE‑objekt du vill exportera.

## Importera namnrymder

För att arbeta med CAD‑filer måste du importera de centrala Aspose.CAD‑klasserna. Behåll importblocket exakt som det visas – det tillhandahåller de klasser som används senare i handledningen.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Så sparar du CAD som PNG

Nedan följer en koncis, steg‑för‑steg‑guide som visar **hur du exporterar OLE‑objekt och sparar CAD som PNG**. Varje steg innehåller en kort förklaring följt av exakt kod som du behöver kopiera in i ditt projekt.

### Steg 1: Ange din dokumentkatalog

Definiera mappen som innehåller dina CAD‑ritningar. Ersätt platshållaren med den faktiska sökvägen på din maskin.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Steg 2: Definiera CAD‑filnamn

Lista varje CAD‑fil du vill bearbeta. Du kan lägga till så många poster som behövs.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Steg 3: Ställ in PNG‑exportalternativ

Konfigurera rasteriseringsinställningarna. Här riktar vi in oss på en specifik layout (`Layout1`) och använder standard‑PNG‑alternativen.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Steg 4: Iterera genom CAD‑filer och spara som PNG

Läs in varje CAD‑fil, rasterisera OLE‑objekten och skriv ut PNG‑filen. Suffixet `_out.png` hjälper dig att identifiera de genererade bilderna.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Vanliga problem och lösningar

| Problem | Varför det händer | Lösning |
|---------|-------------------|--------|
| **`Image.load` kastar `FileNotFoundException`** | `dataDir`‑sökvägen är felaktig eller filnamnet har ett stavfel. | Dubbelkolla katalogsträngen och säkerställ att filnamnen matchar exakt, inklusive mellanslag. |
| **Utdata‑PNG är tom** | Layout‑namnet finns inte i käll‑CAD‑filen. | Använd `cadImage.getLayouts()` för att lista tillgängliga layouter, uppdatera sedan `rasterizationOptions.setLayouts(...)`. |
| **Stora CAD‑filer orsakar OutOfMemoryError** | Rasterisering av högupplösta bilder förbrukar mycket heap‑minne. | Öka JVM‑heapen (`-Xmx2g`) eller sänk rasteriseringsupplösningen via `rasterizationOptions.setResolution(...)`. |

## Vanliga frågor

### Q1: Är Aspose.CAD kompatibel med alla CAD‑filformat?

A1: Aspose.CAD stöder olika CAD‑format, inklusive DWG, DXF och DGN. Se [documentation](https://reference.aspose.com/cad/java/) för den kompletta listan.

### Q2: Kan jag anpassa exportinställningarna för OLE‑objekt?

A2: Ja, Aspose.CAD tillhandahåller omfattande alternativ för att anpassa exportinställningarna, så att du kan skräddarsy resultatet efter dina specifika krav.

### Q3: Finns det en gratis provversion av Aspose.CAD?

A3: Ja, du kan utforska funktionerna i Aspose.CAD genom att skaffa en gratis provversion från [här](https://releases.aspose.com/).

### Q4: Var kan jag få community‑stöd för Aspose.CAD?

A4: Gå med i Aspose.CAD‑communityn på [forum](https://forum.aspose.com/c/cad/19) för att söka hjälp och dela dina erfarenheter.

### Q5: Hur kan jag köpa en licens för Aspose.CAD?

A5: Besök [purchase page](https://purchase.aspose.com/buy) för att skaffa en licens som passar dina utvecklingsbehov.

## Slutsats

Genom att följa dessa fem enkla steg kan du **spara CAD som PNG** och extrahera varje inbäddat OLE‑objekt med bara några rader Java‑kod. Detta tillvägagångssätt är idealiskt för batch‑konverteringar, automatiserad rapportering eller alla scenarier där du behöver rasterbilder av CAD‑innehåll utan manuell export. Känn dig fri att experimentera med olika rasteriseringsalternativ för att matcha dina kvalitets‑ och prestandakrav.

---

**Last Updated:** 2026-01-04  
**Testad med:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}