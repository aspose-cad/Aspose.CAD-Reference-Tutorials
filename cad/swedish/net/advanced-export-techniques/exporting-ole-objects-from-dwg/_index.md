---
description: Lär dig hur du konverterar DWG till PNG och extraherar OLE‑objekt från
  DWG‑filer med Aspose.CAD för .NET – en snabb, kodfokuserad guide.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konvertera DWG till PNG och exportera OLE-objekt – Aspose.CAD-handledning
url: /sv/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

 produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera OLE-objekt från DWG-filer - Aspose.CAD-handledning

## Introduktion

Om du behöver **konvertera DWG till PNG** samtidigt som du drar ut inbäddade OLE-objekt, har du kommit till rätt ställe. Aspose.CAD för .NET gör denna tvåstegsprocess enkel, så att du kan automatisera extrahering och rasterisering med bara några rader C#. Under de kommande minuterna går vi igenom hela arbetsflödet, från att konfigurera din miljö till att spara varje DWG som en PNG som innehåller de extraherade OLE-data.

## Snabba svar
- **Vad täcker den här handledningen?** Konvertera DWG till PNG och extrahera OLE-objekt med Aspose.CAD för .NET.  
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Vilka .NET-versioner stöds?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Kan jag bearbeta flera DWG-filer samtidigt?** Ja – exemplet loopar igenom en array av filnamn.  
- **Var kan jag hitta fler exempel?** Se den officiella Aspose.CAD-dokumentationen och forumlänkarna nedan.

## Vad är **convert DWG to PNG**?
Att konvertera en DWG (AutoCAD-ritning) till en PNG-bild rasteriserar vektordatan, vilket gör det enkelt att visa eller bädda in i webbsidor, rapporter eller andra applikationer som inte har inbyggt stöd för DWG. När OLE-objekt finns kan de extraheras och sparas som separata resurser under konverteringen.

## Varför extrahera OLE-objekt från CAD-filer?
Många DWG-ritningar bäddar in kalkylblad, diagram eller andra Office-dokument som OLE-objekt. Att extrahera dem gör att du kan återanvända originaldata, automatisera rapportering eller migrera innehåll till nyare format utan att förlora inbäddad information.

## Förutsättningar

- Aspose.CAD for .NET Library: Se till att du har biblioteket installerat. Du kan ladda ner det från [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).
- Document Directory: Skapa en katalog där dina DWG-filer lagras. Ersätt `"Your Document Directory"` i det medföljande kodexemplet med den faktiska sökvägen.

## Importera namnrymder

I ditt .NET-projekt, importera de nödvändiga namnrymderna:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Steg‑för‑steg guide

### Steg 1: Ange dokumentkatalogen

```csharp
string MyDir = "Your Document Directory";
```

Byt ut `"Your Document Directory"` mot sökvägen där dina DWG-filer finns.

### Steg 2: Lista de DWG-filer du vill bearbeta

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Steg 3: Konfigurera exportalternativ för PNG-konvertering

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Du kan justera `CadRasterizationOptions` (t.ex. `PageWidth`, `PageHeight`, `BackgroundColor`) för att matcha den önskade utskriftsupplösningen.

### Steg 4: Iterera genom varje DWG och utför konverteringen

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Under denna loop extraherar biblioteket automatiskt **OLE-objekt** som är inbäddade i varje ritning och inkluderar dem i den genererade PNG‑filen. Om du behöver de råa OLE‑strömmarna kan du komma åt samlingen `cadImage.OleObjects` – ett praktiskt sätt att **how to extract ole** data programatiskt.

## Vanliga problem & felsökning

- **Missing layout name** – Se till att den layout du anger (`"Layout1"` i exemplet) finns i käll‑DWG; annars återgår rasteriseraren till standard‑modelrummet.
- **Large files cause memory pressure** – Bearbeta filer en i taget (som visat) och frigör `CadImage`‑objekt omedelbart med `using`.
- **Unexpected colors** – Ställ in `rasterizationOptions.BackgroundColor` så att den matchar ritningens bakgrund om transparens krävs.

## Vanliga frågor

### Q1: Är Aspose.CAD för .NET lämplig för både junior- och senior-CAD-filer?
A1: Ja, Aspose.CAD för .NET är mångsidig och kan hantera ett brett spektrum av CAD-filer, inklusive både junior- och seniorvarianter.

### Q2: Kan jag anpassa exportalternativ för olika layouter?
A2: Absolut! Som visas i handledningen kan du skräddarsy exportalternativ, inklusive layouter, för att passa dina specifika behov.

### Q3: Var kan jag hitta detaljerad dokumentation för Aspose.CAD för .NET?
A3: Utforska [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/) för djupgående information och exempel.

### Q4: Finns det en gratis provversion tillgänglig?
A4: Ja, du kan prova funktionerna i Aspose.CAD för .NET med en gratis provversion. Besök [this link](https://releases.aspose.com/) för att komma igång.

### Q5: Hur kan jag få support eller ansluta till communityn?
A5: För support och gemenskap, besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q6: Hur extraherar jag **OLE från CAD**-filer utan att konvertera till PNG?
A6: Använd samlingen `CadImage.OleObjects` efter att ha laddat DWG; du kan iterera genom varje `OleObject` och spara dess rådata till en fil.

## Slutsats

Du har nu sett hur du **konverterar DWG till PNG** samtidigt som du sömlöst **extraherar OLE-objekt** med Aspose.CAD för .NET. Detta tillvägagångssätt sparar tid, eliminerar manuella kopiera‑och‑klistra‑steg och integreras smidigt i automatiserade pipelines. Känn dig fri att experimentera med andra rasterformat (JPEG, BMP) eller utforska det rika utbudet av CAD-manipuleringsfunktioner som Aspose erbjuder.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}