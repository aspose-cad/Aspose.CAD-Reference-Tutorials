---
title: Exportera DGN som en del av DWG i Aspose.CAD för .NET
linktitle: Exportera DGN som en del av DWG
second_title: Aspose.CAD .NET - CAD- och BIM-filformat
description: Lär dig hur du exporterar DGN som en del av DWG i Aspose.CAD för .NET. Följ vår steg-för-steg-guide för sömlös integration.
weight: 11
url: /sv/net/cad-export-formats/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera DGN som en del av DWG i Aspose.CAD för .NET

## Introduktion

en värld av .NET-utveckling framstår Aspose.CAD som ett kraftfullt bibliotek för att arbeta med CAD-filer (Computer-Aided Design). Denna handledning guidar dig genom processen att exportera en DGN-fil (Design) som en del av en DWG-fil (ritning) med Aspose.CAD för .NET. Oavsett om du är en erfaren utvecklare eller precis har börjat, hjälper den här steg-för-steg-guiden dig att utnyttja kapaciteten hos Aspose.CAD för att utföra denna specifika uppgift effektivt.

## Förutsättningar

Innan du dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.CAD för .NET: Se till att du har Aspose.CAD-biblioteket för .NET installerat. Du kan ladda ner den[här](https://releases.aspose.com/cad/net/).

- Utvecklingsmiljö: Konfigurera din föredragna .NET-utvecklingsmiljö, som Visual Studio.

- Grundläggande kunskaper i C#: Bekanta dig med programmeringsspråket C#.

## Importera namnområden

I ditt C#-projekt, inkludera de nödvändiga namnområdena för att komma åt Aspose.CAD-funktionaliteten. Lägg till följande med hjälp av direktiv i början av din kodfil:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Låt oss nu dela upp den tillhandahållna koden i flera steg:

## Steg 1: Definiera filsökvägar

```csharp
//Inmatnings- och utdatafilsökvägar
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Steg 2: Skapa PdfOptions-instans

```csharp
// Skapa en instans av klassen PdfOptions för att exportera DWG till PDF
PdfOptions exportOptions = new PdfOptions();
```

## Steg 3: Ladda DWG-fil

```csharp
// Ladda den befintliga DWG-filen som en bild och konvertera den till CadImage-typ
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Steg 4: Iterera genom enheter

```csharp
// Iterera genom varje entitet i DWG-filen
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Steg 5: Kontrollera enhetstyp

```csharp
// Kontrollera om enheten är en bilddefinition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Steg 6: Skaffa Underlay Path

```csharp
// Om det är en bilddefinition, hämta den externa referensen till objektet
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Steg 7: Definiera rasteriseringsalternativ

```csharp
// Definiera inställningar för CadRasterizationOptions-objektet
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Steg 8: Exportera DWG till PDF

```csharp
// Exportera DWG till PDF genom att anropa Save method
cadImage.Save(outPath, exportOptions);
```

## Slutsats

Grattis! Du har framgångsrikt gått igenom processen att exportera en DGN-fil som en del av en DWG-fil med Aspose.CAD för .NET. Den här handledningen har försett dig med de grundläggande stegen och kodavsnitten för att utföra denna specifika uppgift sömlöst.

## FAQ's

### F1: Kan jag använda Aspose.CAD för .NET i mina kommersiella projekt?
 A1: Ja, det kan du. Besök[här](https://purchase.aspose.com/buy) för att utforska licensalternativ.

### F2: Finns det några begränsningar för storleken på DWG-filer jag kan bearbeta?
S2: Aspose.CAD stöder hantering av stora DWG-filer, men hårdvarubegränsningar kan gälla.

### F3: Finns det en testversion tillgänglig?
A3: Ja, du kan få en gratis provperiod[här](https://releases.aspose.com/).

### F4: Hur kan jag få tillfälliga licenser?
 A4: Tillfälliga licenser kan erhållas[här](https://purchase.aspose.com/temporary-license/).

### F5: Var kan jag söka hjälp om jag stöter på problem?
 S5: Du kan besöka Aspose.CAD-forumet[här](https://forum.aspose.com/c/cad/19) för support.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
