---
date: 2025-12-22
description: Lär dig hur du laddar en DWG‑fil och extraherar underlagsinformation
  med Aspose.CAD för Java – en steg‑för‑steg‑guide som täcker underlagsflaggor.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: Läs in DWG‑fil och få åtkomst till underlagsflaggor – Aspose.CAD för Java
url: /sv/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ladda DWG-fil & få åtkomst till underlagflaggor – Aspose.CAD för Java

I moderna CAD-arbetsflöden är **laddning av en DWG-fil** snabbt och att hämta underlagsdetaljer ett vanligt krav. Oavsett om du bygger en visare, automatiserar batch‑behandling eller extraherar metadata för GIS‑integration, ger Aspose.CAD för Java dig ett rent, kod‑först sätt att göra det. I den här handledningen går vi igenom de exakta stegen för att **ladda DWG-fil**, iterera dess entiteter och läsa underlagsflaggorna som många utvecklare förbiser.

## Snabba svar
- **Vad är den primära klassen för att öppna en DWG?** `com.aspose.cad.Image.load()` returnerar en `CadImage`.
- **Vilket objekt innehåller underlagsinformation?** `CadUnderlay` (eller dess avledda typer som `CadDgnUnderlay`).
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.
- **Kan jag bearbeta flera DWG-filer i en loop?** Ja – upprepa bara mönstret för laddning‑och‑iteration.
- **Är detta tillvägagångssätt kompatibelt med Java 11+?** Absolut, Aspose.CAD stöder Java 8 och senare LTS‑utgåvor.

## Vad är “ladda dwg-fil” i Aspose.CAD?
`Image.load()` läser det binära DWG-innehållet och skapar ett `CadImage`‑objekt i minnet. Därifrån kan du utforska lager, block och underlagsentiteter utan att själv behöva hantera DWG‑filformatet.

## Varför extrahera underlagsflaggor från en DWG?
Underlagsflaggor visar hur en extern referens (t.ex. en DGN- eller PDF‑underlag) är placerad, skalad och roterad i ritningen. Att känna till dessa värden låter dig:
- Återskapa den exakta visuella layouten i en anpassad visare.
- Konvertera underlag till inhemska CAD‑entiteter för vidare redigering.
- Generera rapporter som inkluderar underlagsmetadata för efterlevnad eller dokumentation.

## Förutsättningar
- **Aspose.CAD Library** – ladda ner från sidan [releases](https://releases.aspose.com/cad/java/).
- **Java Development Kit** – JDK 8 eller nyare.
- **En mapp** som innehåller de DWG-filer du vill analysera. Ersätt `"Your Document Directory"` i koden med din faktiska sökväg.

## Importera namnrymder

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Steg‑för‑steg‑guide

### Steg 1: Ange resurskatalogen
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Definiera var dina DWG-filer finns. Att använda en dedikerad mapp håller exemplet rent och portabelt.

### Steg 2: Ladda DWG-filen
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Här **laddar vi dwg-fil** `BlockRefDgn.dwg` till en `CadImage`‑instans, redo för inspektion.

### Steg 3: Iterera genom DWG‑entiteter
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
Loopen går igenom varje entitet—linjer, cirklar, block och underlag—så att vi kan plocka ut de vi behöver.

### Steg 4: Identifiera CadDgnUnderlay‑entiteter
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Endast `CadDgnUnderlay`‑objekt innehåller de underlagsflaggor vi söker, så vi filtrerar efter dem.

### Steg 5: Få åtkomst till underlagsinformation
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
När vi har ett `CadUnderlay` kan vi läsa dess sökväg, namn, infogningspunkt, rotation, skalningsfaktorer och `UnderlayFlags`‑enum som indikerar synlighet, beskärning och andra renderingsalternativ.

## Vanliga problem & tips
- **Null underlay‑sökväg** – Säkerställ att DWG faktiskt refererar en extern fil; annars blir sökvägen tom.
- **Ej stödd underlagstyp** – Aspose.CAD stödjer för närvarande DGN‑underlag; PDF‑underlag är ännu inte exponerade via API‑t.
- **Licensundantag** – Att köra koden utan en giltig licens kommer att lägga till ett vattenmärke på alla exporterade bilder.

## Vanliga frågor

**Q: Kan jag använda Aspose.CAD för Java med andra CAD‑filformat?**  
A: Aspose.CAD fokuserar främst på DWG‑formatet, men det stödjer även DXF, DWF och andra CAD‑format.

**Q: Finns det en provversion tillgänglig för Aspose.CAD för Java?**  
A: Ja, du kan utforska funktionerna med en gratis provversion från [här](https://releases.aspose.com/).

**Q: Hur kan jag få support eller söka hjälp med Aspose.CAD för Java?**  
A: Besök [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad19) för gemenskapsstöd och diskussioner.

**Q: Finns tillfälliga licenser tillgängliga för Aspose.CAD för Java?**  
A: Ja, du kan skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

**Q: Var kan jag hitta den omfattande dokumentationen för Aspose.CAD för Java?**  
A: Se [dokumentationen](https://reference.aspose.com/cad/java/) för detaljerad information.

---

**Senast uppdaterad:** 2025-12-22  
**Testad med:** Aspose.CAD 24.12 for Java  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}