---
date: 2026-03-02
description: Lås upp potentialen i Aspose.CAD för Java. Exportera OLE‑objekt enkelt
  och **spara CAD som PNG**. Ladda ner nu för sömlös CAD‑datamanagement.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Spara CAD som PNG – Exportera OLE-objekt med Aspose.CAD för Java
url: /sv/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara CAD som PNG – Exportera OLE-objekt med Aspose.CAD för Java

## Introduktion

I den dynamiska världen av Computer-Aided Design (CAD) är hantering och extrahering av OLE (Object Linking and Embedding)-objekt på ett effektivt sätt—och att kunna **save CAD as PNG**—avgörande för efterföljande arbetsflöden såsom rapportering, webb‑förhandsgranskning eller arkivering. Aspose.CAD för Java tillhandahåller en kraftfull, kod‑först lösning som låter dig både exportera OLE‑objekt och konvertera CAD‑ritningar till högkvalitativa PNG‑bilder med bara några rader kod.

## Snabba svar
- **Vad gör Aspose.CAD?** Det läser, manipulerar och konverterar CAD‑filer (DWG, DXF, DGN osv.) utan att behöva inbyggd CAD‑programvara.  
- **Kan jag save CAD as PNG?** Ja—använd `PngOptions` tillsammans med `CadRasterizationOptions` för att rasterisera vilken layout som helst.  
- **Hur exporterar jag OLE‑objekt?** Ladda CAD‑filen med `Image.load` och spara varje layout som innehåller OLE som PNG.  
- **Behöver jag en licens?** En gratis provversion finns tillgänglig; en kommersiell licens tar bort begränsningarna i utvärderingsversionen.  
- **Vilken Java‑version krävs?** Java 8 eller högre stöds fullt ut.

## Vad är **save CAD as PNG**?
Att spara CAD som PNG betyder att rasterisera vektorbaserade CAD‑ritningar till en pixelbaserad PNG‑bild. Denna konvertering är användbar när du behöver ett lättviktigt, universellt visningsbart format för webbsidor, mobilappar eller dokumentation.

## Varför använda Aspose.CAD för Java för att **convert CAD to PNG**?
- **No CAD installation needed** – biblioteket fungerar helt i Java.  
- **Preserves layout fidelity** – du kan välja specifika layouter, kontrollera DPI och behålla linjekvaliteten.  
- **Batch processing** – iterera över flera filer med en enkel loop.  
- **Export OLE objects** – OLE‑innehåll som är inbäddat i DWG/DXF‑filer renderas automatiskt i PNG‑utdata.

## Förutsättningar

Innan du dyker ner i handledningen, se till att du har följande förutsättningar på plats:

- **Java Environment** – Se till att du har en Java‑utvecklingsmiljö installerad på din maskin.  
- **Aspose.CAD for Java** – Ladda ner och installera Aspose.CAD för Java‑biblioteket. Du hittar biblioteket på [download link](https://releases.aspose.com/cad/java/).  
- **CAD Files** – Förbered CAD‑filerna som innehåller OLE‑objekt som du vill exportera.

## Importera namnrymder

För att börja, importera de nödvändiga namnrymderna i ditt Java‑projekt. Dessa namnrymder tillhandahåller de nödvändiga klasserna och funktionerna som krävs för att arbeta med CAD‑filer med Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Nu ska vi gå igenom processen för att exportera OLE‑objekt från CAD i flera steg:

## Hur man **save CAD as PNG** och exportera OLE‑objekt

### Steg 1: Ange din dokumentkatalog

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Se till att ersätta `"Your Document Directory"` med sökvägen till katalogen som innehåller dina CAD‑filer.

### Steg 2: Definiera CAD‑filnamn

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Ange namnen på de CAD‑filer du vill bearbeta i `files`‑arrayen.

### Steg 3: Ställ in PNG‑exportalternativ

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Konfigurera PNG‑exportalternativen, inklusive vektor‑rasterisering och layoutinställningar. Dessa alternativ möjliggör att **convert CAD to PNG** med önskad kvalitet.

### Steg 4: Iterera genom CAD‑filer

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Iterera genom varje specificerad CAD‑fil, ladda den med Aspose.CAD och spara OLE‑objekten som PNG‑bilder. Denna loop visar ett enkelt sätt att **convert DWG to PNG** i bulk.

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|-------|-------|----------|
| **Blank PNG output** | Layout name mismatch | Verify that the layout name (`"Layout1"`) exists in the source DWG. |
| **Missing OLE graphics** | OLE objects are stored in a different layout | Include all relevant layouts in `rasterizationOptions.setLayouts(...)`. |
| **Out‑of‑memory error on large files** | High DPI settings | Reduce DPI via `rasterizationOptions.setResolution(...)` or process files one at a time. |

## Vanliga frågor

**Q: Är Aspose.CAD kompatibel med alla CAD‑filformat?**  
A: Aspose.CAD stöder olika CAD‑format, inklusive DWG, DXF och DGN. Se [dokumentation](https://reference.aspose.com/cad/java/) för den kompletta listan.

**Q: Kan jag anpassa exportinställningarna för OLE‑objekt?**  
A: Ja, Aspose.CAD erbjuder omfattande alternativ för att anpassa exportinställningarna, så att du kan skräddarsy resultatet efter dina specifika krav.

**Q: Finns det en gratis provversion av Aspose.CAD?**  
A: Ja, du kan utforska funktionerna i Aspose.CAD genom att skaffa en gratis provversion från [här](https://releases.aspose.com/).

**Q: Var kan jag få community‑support för Aspose.CAD?**  
A: Gå med i Aspose.CAD‑communityn på [forum](https://forum.aspose.com/c/cad/19) för att få hjälp och dela dina erfarenheter.

**Q: Hur kan jag köpa en licens för Aspose.CAD?**  
A: Besök [köpsidan](https://purchase.aspose.com/buy) för att skaffa en licens som passar dina utvecklingsbehov.

## Slutsats

Med dessa enkla men kraftfulla steg kan du sömlöst **save CAD as PNG** samtidigt som du exporterar OLE‑objekt från CAD‑filer med Aspose.CAD för Java. Detta mångsidiga verktyg ger utvecklare möjlighet att hantera CAD‑data effektivt, vilket öppnar nya möjligheter inom CAD‑applikationsutveckling och efterföljande bild‑baserade arbetsflöden.

---

**Senast uppdaterad:** 2026-03-02  
**Testat med:** Aspose.CAD for Java 24.12  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}