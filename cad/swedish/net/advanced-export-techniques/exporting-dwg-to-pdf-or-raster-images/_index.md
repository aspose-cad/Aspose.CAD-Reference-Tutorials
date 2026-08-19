---
date: 2026-03-16
description: Lär dig hur du konverterar DWG till PDF eller rasterbilder med Aspose.CAD
  för .NET. Denna steg‑för‑steg CAD‑till‑PDF‑handledning täcker export av DWG till
  bildformat som PNG och visar hur du effektivt exporterar DWG till bildfiler.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hur man konverterar DWG till PDF och rasterbilder med Aspose.CAD för .NET
url: /sv/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

}}

All good.

Now produce final content with same structure. Ensure no extra spaces that could break formatting. Keep markdown.

Let's assemble.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera DWG till PDF eller rasterbilder - Aspose.CAD Guide

## Introduktion

Om du behöver **konvertera DWG till PDF** (eller till rasterformat som PNG) direkt från en .NET-applikation, är du på rätt plats. I den här handledningen går vi igenom de exakta stegen som krävs för att använda Aspose.CAD för .NET för att utföra konverteringen, förklarar varför biblioteket är ett bra val och visar hur du hanterar både PDF- och bildutdata med bara några rader kod.

## Snabba svar
- **Vilket bibliotek hanterar DWG-konvertering?** Aspose.CAD for .NET  
- **Kan jag exportera DWG till PNG såväl som PDF?** Ja – samma rasteriseringsalternativ fungerar för båda formaten.  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för testning; en kommersiell licens krävs för produktion.  
- **Vilka .NET-versioner stöds?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Hanteras enhetskonvertering automatiskt?** Du kan definiera enhetssystemet manuellt (metrisk eller imperial) som visas i koden.

## Vad betyder “konvertera DWG till PDF”?
Att konvertera DWG till PDF innebär att ta en CAD-ritning (DWG) och rendera den till ett portabelt, endast‑visningsdokument (PDF). Detta är användbart för att dela designer med intressenter som inte har CAD‑programvara, skapa utskrivbar dokumentation eller arkivera ritningar i ett universellt läsbart format.

## Varför använda Aspose.CAD för denna konvertering?
- **Inga externa beroenden** – biblioteket fungerar helt i hanterad kod.  
- **Hög noggrannhet** – behåller lager, linjebredd och layoutinformation.  
- **Inbyggda rasteralternativ** – låter dig exportera till PNG, JPEG, BMP, etc., med ett enda konfigurationsobjekt.  
- **Plattformsoberoende** – fungerar på Windows, Linux och macOS med .NET Core.

## Förutsättningar

Innan vi dyker ner i handledningen, se till att du har följande på plats:

- Grundläggande förståelse för .NET-programmering.  
- Aspose.CAD för .NET-biblioteket installerat. Om inte, ladda ner det [här](https://releases.aspose.com/cad/net/).  
- Din föredragna integrerade utvecklingsmiljö (IDE) konfigurerad för .NET-utveckling.

## Importera namnrymder

Låt oss börja med att importera de nödvändiga namnrymderna i ditt .NET‑projekt. Detta säkerställer att du har åtkomst till Aspose.CAD‑funktionaliteten i din kod.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Steg 1: Läs in DWG‑fil

Börja med att läsa in DWG‑filen du vill konvertera. Ersätt `"Your Document Directory"` med sökvägen till din DWG‑fil.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Steg 2: Ställ in PDF‑export (Hur man exporterar DWG till PDF)

Nu ska vi konfigurera PDF‑exportinställningarna. Detta exempel visar hur du anger layouten och hanterar enhetskonverteringar.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Steg 3: Exportera till PDF

Utför exporten till PDF med de konfigurerade inställningarna.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Steg 4: Exportera till rasterbilder (exportera dwg till bild)

Utöka funktionaliteten för att exportera till rasterbilder, såsom PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Vanliga problem och lösningar

| Problem | Varför det händer | Hur man åtgärdar |
|-------|----------------|------------|
| **Tomma sidor i PDF** | Layout inte specificerad korrekt | Se till att `rasterizationOptions.Layouts` inkluderar rätt layoutnamn (t.ex. `"Model"`). |
| **Felaktiga dimensioner** | DPI eller sidstorlek matchar inte | Justera `PageHeight`, `PageWidth` och DPI‑värden i `CadRasterizationOptions`. |
| **Enheter visas fel** | Enhetskonvertering inte definierad | Använd `DefineUnitSystem` för att sätta `currentUnitIsMetric` och `currentUnitCoefficient` baserat på `cadImage.UnitType`. |
| **Licensundantag** | Begränsningar i provversionen | Applicera en tillfällig eller permanent licens innan du anropar `Image.Load`. |

## Vanliga frågor

### Q1: Kan jag använda Aspose.CAD för .NET i mina kommersiella projekt?
A1: Ja, det kan du. Besök [purchase.aspose.com/buy](https://purchase.aspose.com/buy) för licensinformation.

### Q2: Finns det en gratis provversion tillgänglig?
A2: Självklart! Hämta din gratis provversion [här](https://releases.aspose.com/).

### Q3: Hur kan jag få support för Aspose.CAD för .NET?
A3: Gå till [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19) för gemenskapsstöd.

### Q4: Kan jag få en tillfällig licens för teständamål?
A4: Ja, du kan få en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

### Q5: Var kan jag hitta den detaljerade dokumentationen?
A5: Dokumentationen finns på [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: Hur sparar jag **CAD som PNG** med hög kvalitet?
A6: Ställ in `PageHeight` och `PageWidth` till önskade pixeldimensioner och välj en DPI på 300 eller högre i `CadRasterizationOptions`.

### Q7: Vad är det bästa sättet att **konvertera dwg** när källfilen innehåller flera layouter?
A7: Fyll `rasterizationOptions.Layouts` med alla layoutnamn du vill exportera, loopa sedan igenom varje layout och anropa `Save` för varje utdataformat.

---

**Senast uppdaterad:** 2026-03-16  
**Testat med:** Aspose.CAD 24.11 for .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}