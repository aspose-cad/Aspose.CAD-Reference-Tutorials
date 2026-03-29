---
date: 2026-03-29
description: Lär dig hur du konverterar DGN till PNG med Aspose.CAD för .NET. Denna
  guide täcker också stöd för CAD‑filformat och hela uppsättningen av stödda DGN‑element.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konvertera DGN till PNG med Aspose.CAD för .NET
url: /sv/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera DGN till PNG med Aspose.CAD för .NET

## Introduktion

Är du en .NET‑utvecklare som vill **konvertera DGN till PNG** sömlöst? Aspose.CAD för .NET erbjuder en robust lösning för att hantera DGN‑filer effektivt. I den här handledningen kommer vi att gå igenom de stödjade DGN‑elementen, guida dig genom processen att arbeta med Aspose.CAD för .NET och visa exakt hur du exporterar dessa element till PNG‑bilder.

## Snabba svar
- **Vad gör Aspose.CAD?** Den läser, modifierar och konverterar CAD/BIM‑filer (inklusive DGN) till rasterformat såsom PNG.  
- **Kan jag konvertera 2D‑ och 3D‑DGN‑element?** Ja – både 2‑D‑ och 3‑D‑entiteter stöds.  
- **Vilka .NET‑versioner krävs?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Behöver jag en licens för testning?** En gratis provversion finns tillgänglig; en licens krävs för produktion.  
- **Var kan jag hämta biblioteket?** Ladda ner det från den officiella Aspose‑sidan (länken nedan).

## Vad betyder “konvertera DGN till PNG”?
Att konvertera DGN till PNG innebär att rendera den vektorbaserade DGN‑ritningen (2‑D eller 3‑D) till ett rasterbildformat (PNG). Detta är användbart när du behöver visa CAD‑ritningar på webben, bädda in dem i rapporter eller generera miniatyrbilder utan att behöva en CAD‑visare.

## Varför använda Aspose.CAD för .NET för CAD‑filformatstöd?
- **Fullständigt stöd för CAD‑filformat** – DGN, DWG, DXF, DWF och mer.  
- **Inga externa beroenden** – ren .NET‑bibliotek, inga inhemska CAD‑installationer.  
- **Högupplöst rendering** – bevarar linjebredd, färger och 3‑D‑geometri.  
- **Batch‑behandling** – loopa enkelt igenom många filer i en server‑sidig applikation.

## Förutsättningar

Innan vi börjar, se till att du har följande:

- Grundläggande kunskap om .NET‑programmering.  
- Visual Studio installerat på din maskin.  
- Aspose.CAD för .NET‑biblioteket, som du kan ladda ner [här](https://releases.aspose.com/cad/net/).

## Importera namnrymder

För att kickstarta ditt projekt, importera de nödvändiga namnrymderna i din .NET‑applikation. Detta steg säkerställer att du har tillgång till funktionerna som tillhandahålls av Aspose.CAD för .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Hur man konverterar DGN till PNG

Nedan följer en steg‑för‑steg‑guide som visar hur du laddar en DGN‑fil, itererar dess element, hanterar både 2‑D‑ och 3‑D‑entiteter och slutligen exporterar resultatet till en PNG‑rasterbild.

### Steg 1: Ladda DGN‑filen

Börja med att ladda en befintlig DGN‑fil som ett `DgnImage` i din .NET‑applikation.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Steg 2: Iterera genom DGN‑element

Iterera genom DGN‑elementen med en `foreach`‑loop. Aspose.CAD för .NET tillhandahåller en mängd olika DGN‑elementtyper som du kan arbeta med.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Steg 3: Hantera tidigare stödjade 2‑D‑entiteter

Dessa entiteter stöds nu även för 3‑D‑rendering. Switch‑satsen låter dig styra logiken baserat på elementtypen.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Steg 4: Hantera stödjade 3‑D‑entiteter

Aspose.CAD lägger till fullt stöd för flera 3‑D‑DGN‑element. Utöka switch‑satsen för att bearbeta dem vid behov.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Steg 5: Exportera och spara som PNG

Efter eventuell nödvändig manipulation, exportera DGN‑ritningen till en PNG‑rasterbild och spara den i den angivna katalogen.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Proffstips:** Använd `Image.Save` med `new PngOptions()` för att kontrollera upplösning, bakgrundsfärg och andra PNG‑specifika inställningar.

## Översikt över CAD‑filformatstöd

Aspose.CAD för .NET är inte begränsat till DGN. Det stödjer även DWG, DXF, DWF och många andra CAD‑format, vilket ger dig ett enda API för att hantera ett brett spektrum av ingenjörsritningar. Detta gör det idealiskt för projekt som kräver **CAD‑filformatstöd** över flera standarder.

## Vanliga problem & lösningar

| Problem | Orsak | Lösning |
|-------|--------|-----|
| **Bild visas tom** | Exporterad med noll DPI | Ange `ResolutionX` och `ResolutionY` i `PngOptions`. |
| **Saknad 3‑D‑geometri** | Elementtyp hanteras inte i switch | Lägg till den saknade `DgnElementType`‑fallet och rendera därefter. |
| **Minnesbrist vid stora filer** | Laddar hela filen på en gång | Bearbeta element i batcher eller använd streaming när det är möjligt. |

## Vanliga frågor

### Q1: Var kan jag hitta dokumentationen för Aspose.CAD för .NET?
A1: Du kan hitta dokumentationen [här](https://reference.aspose.com/cad/net/).

### Q2: Hur laddar jag ner Aspose.CAD för .NET?
A2: Du kan ladda ner biblioteket [här](https://releases.aspose.com/cad/net/).

### Q3: Finns det en gratis provversion för Aspose.CAD för .NET?
A3: Ja, du kan komma åt den gratis provversionen [här](https://releases.aspose.com/).

### Q4: Var kan jag få tillfälliga licenser för Aspose.CAD för .NET?
A4: Tillfälliga licenser finns tillgängliga [här](https://purchase.aspose.com/temporary-license/).

### Q5: Behöver du hjälp eller har du frågor?
A5: Besök Aspose.CAD för .NET‑communityns [supportforum](https://forum.aspose.com/c/cad/19).

---

**Senast uppdaterad:** 2026-03-29  
**Testad med:** Aspose.CAD for .NET 24.11  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}