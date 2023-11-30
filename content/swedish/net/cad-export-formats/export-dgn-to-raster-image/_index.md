---
title: Exportera DGN till rasterbild i Aspose.CAD för .NET
linktitle: Exportera DGN till rasterbild
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Konvertera DGN till rasterbilder utan ansträngning med Aspose.CAD för .NET. Utforska steg-för-steg-guiden och släpp lös kraften i .NET i CAD-filmanipulation.
type: docs
weight: 13
url: /sv/net/cad-export-formats/export-dgn-to-raster-image/
---
## Introduktion

I den dynamiska sfären av .NET-utveckling framstår Aspose.CAD som ett kraftfullt verktyg för att hantera datorstödd design (CAD)-filer. Denna handledning dyker in i processen att exportera DGN-filer till rasterbilder med Aspose.CAD för .NET. Om du är sugen på att omvandla dina DGN-filer till visuellt övertygande rasterbilder sömlöst, är du på rätt plats.

## Förutsättningar

Innan vi ger oss ut på denna resa, se till att du har följande förutsättningar på plats:

-  Aspose.CAD för .NET: Se till att du har Aspose.CAD-biblioteket installerat i ditt .NET-projekt. Du hittar biblioteket och relevant dokumentation på[hemsida](https://reference.aspose.com/cad/net/).

- Exempel på DGN-fil: Ha en DGN-fil redo för konvertering. I vårt exempel kommer vi att använda "Nikon_D90_Camera.dgn."

Låt oss nu dyka in i steg-för-steg-guiden.

## Importera namnområden

I ditt .NET-projekt börjar du med att importera de nödvändiga namnrymden för Aspose.CAD. Det här steget låter dig komma åt de klasser och metoder som krävs för konvertering av DGN till rasterbild.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Steg 1: Ladda DGN-fil

 Börja med att ladda DGN-filen i en`CadImage` objekt. Detta ger en grund för efterföljande operationer.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Din kod för vidare bearbetning kommer här
}
```

## Steg 2: Definiera rasteriseringsalternativ

 Skapa en`CadRasterizationOptions` objekt och ställ in olika egenskaper för att anpassa rastreringsprocessen enligt dina krav.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Steg 3: Skapa JpegOptions-objekt

 Eftersom vi strävar efter att konvertera DGN-filen till JPEG, skapa en`JpegOptions` objekt och tilldela det tidigare definierade`CadRasterizationOptions` till det.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 4: Spara rasterbilden

 Använd`Save` metod för`CadImage` klass för att exportera DGN-filen till en rasterbild i önskat format, i detta fall en JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Slutsats

Grattis! Du har framgångsrikt navigerat genom stegen för att exportera en DGN-fil till en rasterbild med Aspose.CAD för .NET. Denna handledning har utrustat dig med den grundläggande kunskapen för att enkelt kunna integrera denna funktion i dina .NET-projekt.

## FAQ's

### F1: Kan jag exportera DGN-filer till andra format än JPEG?

S1: Ja, Aspose.CAD för .NET stöder olika utdataformat. Du kan ändra alternativen i enlighet med detta i steg 3.

### F2 Hur kan jag hantera undantag under konverteringsprocessen?

S2: Se till att du har rätt undantagshantering, som visas i den medföljande koden, för att lösa potentiella problem.

### F3: Finns det en testversion tillgänglig för Aspose.CAD för .NET?

 S3: Ja, du kan utforska produkten med en gratis provperiod. Besök[här](https://releases.aspose.com/) för mer information.

### F4: Var kan jag söka hjälp eller diskutera frågor relaterade till Aspose.CAD för .NET?

 A4: Gå över till[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) för samhällsstöd och diskussioner.

### F5: Hur får jag en tillfällig licens för Aspose.CAD för .NET?

 A5: Besök[den här länken](https://purchase.aspose.com/temporary-license/)att skaffa en tillfällig licens för dina utvecklingsbehov.