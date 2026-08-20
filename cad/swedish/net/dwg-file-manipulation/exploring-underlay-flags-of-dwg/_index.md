---
date: 2026-04-09
description: Lär dig hur du konverterar DWG till bild och hur du läser underlagflaggor
  med Aspose.CAD för .NET i den här steg‑för‑steg‑guiden.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: Utforska underlagsflaggor i DWG-filer
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konvertera DWG till bild – Utforska underlagsflaggor i DWG-filer – Aspose.CAD-handledning
url: /sv/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utforska underlagflaggor i DWG-filer - Aspose.CAD-handledning

## Introduktion

Om du fördjupar dig i den komplexa världen av CAD-filer, specifikt DWG-filer, och du vill **konvertera DWG till bild** samtidigt som du upptäcker **hur man läser underlag**-flaggor, är du på rätt plats. Denna handledning guidar dig genom varje steg med det kraftfulla Aspose.CAD för .NET-biblioteket, så att du kan extrahera underlagsinformation och rendera ritningen som en bild med förtroende.

## Snabba svar
- **Vad betyder “convert DWG to image”?**  
  Det betyder att rendera en DWG-ritning till ett rasterformat (PNG, JPEG osv.) med Aspose.CAD.
- **Vilken metod avslöjar underlagflaggor?**  
  Åtkomst till `CadUnderlay`-objektets `Flags`-egenskap efter att DWG har laddats.
- **Behöver jag en licens för Aspose.CAD?**  
  En tillfällig licens finns tillgänglig för utvärdering; en full licens krävs för produktion.
- **Vilka .NET-versioner stöds?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 och senare.
- **Kan jag extrahera underlagsgeometri?**  
  Ja – underlagssökvägen, infogningspunkten, skala, rotation och flaggstatus är alla åtkomliga.

## Vad är “convert DWG to image” och varför är det viktigt?

Att konvertera en DWG-fil till en bild gör det möjligt att visa CAD-ritningar i webbläsare, bädda in dem i rapporter eller dela dem med intressenter som inte har en CAD-visare. Vid rendering behöver du ofta inspektera **underlag**-objekt (t.ex. DGN-referenser) för att säkerställa att de visas korrekt. Att förstå underlagflaggorna hjälper dig att felsöka beskärning, monokrom rendering och synlighetsproblem innan du genererar den slutgiltiga bilden.

## Förutsättningar

- En grundläggande förståelse för C# och .NET-programmering.  
- **Aspose.CAD for .NET**-biblioteket installerat. Om du ännu inte har det, ladda ner det **[here](https://releases.aspose.com/cad/net/)**.  
- En DWG-fil för testning – exempelfilen **“BlockRefDgn.dwg”** används genom hela guiden.

## Importera namnrymder

För att komma igång, importera de nödvändiga namnrymderna:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Steg 1: Ladda DWG-fil och konvertera till `CadImage`

Först, ladda DWG-filen och kasta den till en `CadImage`. Detta objekt ger dig åtkomst till alla ritningsentiteter, inklusive underlag.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Steg 2: Iterera genom entiteter

Därefter, loopa igenom varje entitet i ritningen. Här hittar du underlagsobjekten.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Steg 3: Kontrollera för `CadDgnUnderlay`-typ

Identifiera underlagsentiteter genom att kontrollera deras körningstyp. Klassen `CadDgnUnderlay` representerar DGN-underlag inbäddade i en DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Steg 4: Åtkomst till underlagflaggor

När du har ett `CadDgnUnderlay`, kasta det till `CadUnderlay` för att läsa dess egenskaper och flaggstatus. Flaggan visar om underlaget är synligt, beskuret eller renderat i monokrom.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### Vad utskriften visar

- **UnderlayPath / UnderlayName** – var den externa DGN-filen finns.  
- **InsertionPoint (X, Y)** – koordinater där underlaget placeras i DWG-rymden.  
- **RotationAngle** – rotation som tillämpas på underlaget.  
- **ScaleX / ScaleY / ScaleZ** – skalningsfaktorer för varje axel.  
- **Flags** – booleska värden som indikerar synlighet (`UnderlayIsOn`), beskärning (`ClippingIsOn`) och monokrom rendering (`Monochrome`).

## Vanliga problem & lösningar

| Problem | Orsak | Lösning |
|-------|--------|-----|
| Ingen utskrift för flaggkontroller | Underlagsflaggorna är standardiserade till 0 när underlaget är avstängt. | Säkerställ att DWG faktiskt innehåller ett aktivt underlag eller växla synlighet i käll-CAD-filen. |
| `Invalid cast`-undantag | Entiteten är inte en `CadDgnUnderlay`. | Verifiera att `if (entity is CadDgnUnderlay)`-villkoret är sant innan du kastar. |
| Bildrendering misslyckas efter flaggextraktion | Underlaget kan vara beskuret eller avstängt, vilket leder till ett tomt område. | Justera flaggorna (`UnderlayIsOn = true`, `ClippingIsOn = false`) innan du renderar den slutgiltiga bilden. |

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD för .NET med andra CAD-filformat?

A1: Aspose.CAD stöder olika CAD-format, inklusive DWG, DXF, DGN och fler. Kontrollera dokumentationen för den fullständiga listan.

### Q2: Finns en tillfällig licens tillgänglig för Aspose.CAD för .NET?

A2: Ja, du kan få en tillfällig licens **[here](https://purchase.aspose.com/temporary-license/)**.

### Q3: Var kan jag hitta support för Aspose.CAD för .NET?

A3: Besök supportforumet **[here](https://forum.aspose.com/c/cad/19)** för hjälp.

### Q4: Hur köper jag Aspose.CAD för .NET?

A4: Köp biblioteket **[here](https://purchase.aspose.com/buy)**.

### Q5: Finns en gratis provversion tillgänglig?

A5: Ja, du kan komma åt den gratis provversionen **[here](https://releases.aspose.com/)**.

## Slutsats

Grattis! Du har framgångsrikt lärt dig **hur man konverterar DWG till bild** samtidigt som du behärskar **hur man läser underlag**-flaggor med Aspose.CAD för .NET. Med denna kunskap kan du:

- Rendera DWG-ritningar som rasterbilder för webb- eller rapporteringsscenarier.  
- Inspektera och manipulera underlagsegenskaper för att säkerställa korrekt visning.  
- Felsöka synlighet, beskärning och monokroma problem innan den slutgiltiga bildgenereringen.

Känn dig fri att utforska andra Aspose.CAD-funktioner såsom lagerhantering, textutdrag och batchkonvertering för att ytterligare utöka dina CAD-automatiseringsarbetsflöden.

---

**Senast uppdaterad:** 2026-04-09  
**Testad med:** Aspose.CAD for .NET 24.11  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}