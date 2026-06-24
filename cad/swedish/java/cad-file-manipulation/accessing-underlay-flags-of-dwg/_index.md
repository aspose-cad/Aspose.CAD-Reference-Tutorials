---
date: 2026-02-23
description: Lär dig hur du laddar dwg‑filer med Aspose CAD DWG för Java och extraherar
  underlagflaggor – en steg‑för‑steg‑guide för utvecklare.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – Ladda DWG och åtkomst till underlagsflaggor (Java)
url: /sv/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ladda DWG-fil & få åtkomst till underlagflaggor – Aspose.CAD för Java

I moderna CAD-arbetsflöden kan du med aspose cad dwg snabbt ladda en DWG-fil och hämta underlagsdetaljer som ofta är dolda för vanliga betraktare. Oavsett om du bygger en Java DWG‑visare, automatiserar en batch‑process‑dwg‑pipeline eller extraherar metadata för GIS‑integration, ger Aspose.CAD för Java dig ett rent, kod‑först sätt att göra det. I den här handledningen går vi igenom de exakta stegen för att **ladda en DWG-fil**, iterera dess entiteter och läsa underlagsflaggorna som många utvecklare förbiser.

## Quick Answers
- **Vad är den primära klassen för att öppna en DWG?** `com.aspose.cad.Image.load()` returnerar en `CadImage`.
- **Vilket objekt innehåller underlagsinformation?** `CadUnderlay` (eller dess avledda typer som `CadDgnUnderlay`).
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.
- **Kan jag bearbeta flera DWG-filer i en loop?** Ja – bara upprepa mönstret load‑and‑iterate.
- **Är detta tillvägagångssätt kompatibelt med Java 11+?** Absolut, Aspose.CAD stödjer Java 8 och senare LTS‑utgåvor.

## aspose cad dwg – Loading a DWG File (Java)

`Image.load()` läser det binära DWG-innehållet och skapar ett `CadImage`‑objekt i minnet. Därifrån kan du utforska lager, block och underlagsentiteter utan att själv behöva hantera DWG‑filformatet.

## Why extract underlay flags from a DWG?

Underlagsflaggor visar hur en extern referens (t.ex. ett DGN‑ eller PDF‑underlag) är placerad, skalad och roterad i ritningen. Att känna till dessa värden låter dig:

- Återskapa den exakta visuella layouten i en anpassad **java dwg viewer**.
- Konvertera underlag till inhemska CAD‑entiteter för vidare redigering.
- Generera rapporter som inkluderar underlagsmetadata för efterlevnad eller dokumentation.
- **Batch‑processa dwg**‑filer och lagra deras underlagsmetadata i en databas för senare analys.

## Prerequisites
- **Aspose.CAD Library** – ladda ner från [releases](https://releases.aspose.com/cad/java/) sidan.  
- **Java Development Kit** – JDK 8 eller nyare.  
- **En mapp** som innehåller de DWG-filer du vill analysera. Ersätt `"Your Document Directory"` i koden med din faktiska sökväg.

## Import Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Step‑by‑Step Guide

### Step 1: Set the Resource Directory
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Definiera var dina DWG-filer finns. Att använda en dedikerad mapp håller exemplet rent och portabelt.

### Step 2: Load the DWG File
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Här **laddar vi dwg-filen** `BlockRefDgn.dwg` i en `CadImage`‑instans, klar för inspektion.

### Step 3: Iterate Through DWG Entities
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
Loopen går igenom varje entitet—linjer, cirklar, block och underlag—så att vi kan plocka ut de vi behöver.

### Step 4: Identify CadDgnUnderlay Entities
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Endast `CadDgnUnderlay`‑objekt innehåller de underlagsflaggor vi söker, så vi filtrerar efter dem.

### Step 5: Access Underlay Information
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
När vi har ett `CadUnderlay` kan vi läsa dess sökväg, namn, insättningspunkt, rotation, skalningsfaktorer och `UnderlayFlags`‑enum som indikerar synlighet, beskärning och andra renderingsalternativ.

## How to load dwg files in a batch process

Om du behöver **batch‑processa dwg**‑filer, omslut stegen ovan i en enkel `for`‑loop som itererar över alla filer i `dataDir`. Samma `Image.load()`‑anrop fungerar för varje fil, och du kan lagra de extraherade flaggorna i en CSV‑fil eller en databas för efterföljande rapportering.

## Common Issues & Tips
- **Null underlay path** – Säkerställ att DWG faktiskt refererar till en extern fil; annars blir sökvägen tom.
- **Unsupported underlay type** – Aspose.CAD stödjer för närvarande DGN‑underlag; PDF‑underlag är ännu inte exponerade via API:t.
- **License exceptions** – Att köra koden utan en giltig licens kommer att lägga till ett vattenmärke på alla exporterade bilder.
- **Performance tip:** Återanvänd en enda `Image`‑instans när du bearbetar många filer i en batch för att minska GC‑belastningen.

## Frequently Asked Questions

**Q: Kan jag använda Aspose.CAD för Java med andra CAD‑filformat?**  
A: Aspose.CAD fokuserar främst på DWG‑formatet, men stödjer även DXF, DWF och andra CAD‑format.

**Q: Finns det en provversion tillgänglig för Aspose.CAD för Java?**  
A: Ja, du kan utforska funktionerna med en gratis provversion från [here](https://releases.aspose.com/).

**Q: Hur kan jag få support eller söka hjälp med Aspose.CAD för Java?**  
A: Besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för community‑support och diskussioner.

**Q: Finns tillfälliga licenser tillgängliga för Aspose.CAD för Java?**  
A: Ja, du kan skaffa en tillfällig licens [here](https://purchase.aspose.com/temporary-license/).

**Q: Var kan jag hitta den omfattande dokumentationen för Aspose.CAD för Java?**  
A: Se [documentation](https://reference.aspose.com/cad/java/) för detaljerad information.

---

**Senast uppdaterad:** 2026-02-23  
**Testat med:** Aspose.CAD 24.12 for Java  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}