---
title: Öka CAD-exporten med anpassade pennalternativ i Aspose.CAD för .NET
linktitle: Pennstöd vid export
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Lär dig hur du förbättrar din CAD-bildexport med Aspose.CAD för .NET. Anpassa pennalternativ för fantastiska bilder i PDF, PNG, BMP och mer.
type: docs
weight: 12
url: /sv/net/cad-features-and-support/pen-support-in-export/
---
## Introduktion

Aspose.CAD för .NET tillhandahåller en kraftfull uppsättning verktyg för att arbeta med CAD-filer (Computer Aided Design), vilket gör det möjligt för utvecklare att manipulera och exportera CAD-bilder sömlöst. En anmärkningsvärd funktion är pennstödet under export, vilket gör att användare kan anpassa start- och slutkapsinställningar för pennor när de exporterar CAD-bilder till olika format som PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF och WMF.

I den här handledningen kommer vi att fördjupa oss i detaljerna för pennstöd vid export med Aspose.CAD för .NET. Vi delar upp varje steg och ger tydliga förklaringar och exempel som guidar dig genom processen.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:

- Aspose.CAD för .NET installerat i din utvecklingsmiljö. Du kan ladda ner den från[släpp sida](https://releases.aspose.com/cad/net/).

- En grundläggande förståelse för CAD-filformat, särskilt DXF (Drawing Exchange Format).

- Har praktiska kunskaper i programmeringsspråket C#.

## Importera namnområden

För att komma igång, se till att du importerar de nödvändiga namnrymden i ditt C#-projekt:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Steg 1: Konfigurera din dokumentkatalog

Definiera katalogen där ditt CAD-dokument finns:

```csharp
string MyDir = "Your Document Directory";
```

## Steg 2: Ladda CAD-bilden

Ladda CAD-bilden med Aspose.CAD:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Steg 3: Konfigurera rasteriseringsalternativ

Skapa rastrerings- och PDF-alternativ för att anpassa exportprocessen:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Steg 4: Anpassa pennalternativ

Ställ in start- och ändlocksalternativ för pennor:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

## Steg 5: Använd vektorrasteriseringsalternativ

Använd rastreringsalternativen på PDF-alternativen:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 6: Spara den exporterade PDF-filen

Spara CAD-bilden med anpassade pennalternativ som en PDF-fil:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

## Slutsats

I den här handledningen har vi utforskat funktionen för pennstöd i export av Aspose.CAD för .NET. Genom att följa den steg-för-steg-guiden kan du enkelt anpassa start- och slutkapslingsinställningarna för pennor, vilket ökar flexibiliteten i dina CAD-bildexporter.

Experimentera gärna med olika pennalternativ för att uppnå önskade visuella effekter i dina exporterade bilder.

## FAQ's

### F1: Kan jag använda dessa pennalternativ för andra bildformat än PDF?

S1: Ja, pennalternativen kan tillämpas på olika bildformat som PNG, BMP, GIF, JPEG och mer.

### F2: Var kan jag hitta ytterligare dokumentation för Aspose.CAD för .NET?

 A2: Se[dokumentation](https://reference.aspose.com/cad/net/) för omfattande information och exempel.

### F3: Finns det en gratis testversion tillgänglig för Aspose.CAD för .NET?

 S3: Ja, du kan få tillgång till en gratis provperiod[här](https://releases.aspose.com/).

### F4: Hur kan jag få tillfälliga licenser för Aspose.CAD för .NET?

 A4: Besök[sida för tillfällig licens](https://purchase.aspose.com/temporary-license/) för tillfälliga licensalternativ.

### F5: Var kan jag söka communitysupport för Aspose.CAD för .NET?

 S5: Engagera dig i samhället på[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19).