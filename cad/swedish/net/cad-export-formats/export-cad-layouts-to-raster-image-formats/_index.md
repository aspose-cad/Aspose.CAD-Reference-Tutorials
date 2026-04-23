---
date: 2026-03-21
description: Lär dig hur du konverterar dxf till png och andra rasterformat med Aspose.CAD
  för .NET. Följ vår steg‑för‑steg‑guide för sömlös CAD‑lagrexport.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konvertera DXF till PNG med Aspose.CAD för .NET
url: /sv/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportera CAD‑layouter till rasterbildformat i Aspose.CAD för .NET

## Introduktion

Letar du efter ett effektivt sätt att **convert dxf to png** och andra rasterbildformat med Aspose.CAD för .NET? Denna steg‑för‑steg‑guide leder dig genom processen, ger detaljerade instruktioner och kodexempel för att göra uppgiften smidig. Oavsett om du är en erfaren utvecklare eller nybörjare på Aspose.CAD, så riktar sig denna handledning till alla kunskapsnivåer.

### Snabba svar
- **Vilket bibliotek hanterar konverteringen?** Aspose.CAD för .NET  
- **Primärt format som stöds direkt?** JPEG, PNG, BMP och TIFF rasterbilder  
- **Kan jag exportera specifika CAD‑lager?** Ja – använd `CadRasterizationOptions.Layers` för att rikta in dig på enskilda lager  
- **Behöver jag en licens för produktion?** En giltig Aspose.CAD‑licens krävs för icke‑testanvändning  
- **Stödda .NET‑versioner?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## Vad är **convert dxf to png**?

Att konvertera en DXF‑fil (Drawing Exchange Format) till PNG innebär att rasterisera vektorbaserad CAD‑data till en pixelbaserad bild. Detta är användbart när du behöver bädda in CAD‑ritningar i webbsidor, rapporter eller någon miljö som endast stödjer rastergrafik.

## Varför exportera CAD‑lager separat?

Att exportera CAD‑lager individuellt ger dig fin kontroll över den visuella utdata, minskar filstorleken för varje bild och låter dig tillämpa lager‑specifik stil eller efterbehandling. Detta är särskilt praktiskt för stora ingenjörsritningar där endast ett urval av lager är relevant för en viss målgrupp.

## Förutsättningar

Innan du dyker ner i handledningen, se till att du har följande:

- **Aspose.CAD för .NET‑bibliotek** – ladda ner det från [Aspose.CAD‑webbplatsen](https://releases.aspose.com/cad/net/).  
- **CAD‑ritningsfil** – en DXF‑fil (t.ex. `conic_pyramid.dxf`) som du vill konvertera till rasterformat.  

## Importera namnrymder

I ditt .NET‑projekt importerar du de nödvändiga namnrymderna för att utnyttja Aspose.CAD‑funktionaliteten. Inkludera följande namnrymder i början av din kod:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Hur du **convert dxf to png** – Steg‑för‑steg‑guide

### Steg 1: Läs in CAD‑ritning

Först läser du in DXF‑filen i ett `Image`‑objekt. Detta objekt representerar hela CAD‑ritningen i minnet.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### Steg 2: Skapa `CadRasterizationOptions`

Konfigurera rasteriseringsinställningarna såsom utskriftsdimensioner och upplösning. Dessa alternativ styr hur vektordatan rasteriseras.

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### Steg 3: Ange lager (Exportera CAD‑lager)

Om du bara behöver ett specifikt lager, lista dess namn här. Detta demonstrerar **export cad layers** individuellt.

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### Steg 4: Välj bildformat – Spara CAD som PNG (eller JPEG)

Skapa ett bildformat‑specifikt alternativobjekt. Ersätt `JpegOptions` med `PngOptions` när du vill **save cad as png**.

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** För att generera PNG‑filer, skapa helt enkelt `new PngOptions()` istället för `JpegOptions`.

### Steg 5: Exportera till JPEG (eller PNG)-format

Slutligen sparar du den rasteriserade bilden till disk. Filändelsen bestämmer utdataformatet.

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

När du ersätter `JpegOptions` med `PngOptions` kommer samma kod att **convert dxf to png** och producera en `.png`‑fil.

### Ytterligare steg: Konvertera alla lager

Om du behöver **convert cad to raster** för varje lager i ritningen, anropa hjälpfunktionen nedan. Den itererar över alla lager och sparar varje som en separat bild.

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *Obs:* Implementeringen av `ConvertAllLayersToRasterImageFormats` är en del av hela Aspose.CAD‑exempelsviten och demonstrerar batch‑bearbetning av lager.

## Vanliga problem & felsökning

| Symtom | Trolig orsak | Åtgärd |
|--------|--------------|-------|
| Tom eller vit bild | Rasteriseringsalternativ är inte inställda (t.ex. `PageWidth`/`PageHeight` = 0) | Se till att `PageWidth` och `PageHeight` har positiva värden |
| Saknade lager | Fel lager namn i `Layers`‑arrayen | Verifiera exakt lager namn i CAD‑filen (skiftlägeskänsligt) |
| Lågkvalitets‑PNG | Standard‑DPI är låg | Ställ in `rasterizationOptions.Resolution = 300;` för högre kvalitet |

## Vanliga frågor (Original)

### Q1: Kan jag använda andra bildformat för export?

A1: Ja, det kan du. Byt helt enkelt `JpegOptions` mot önskad formats alternativ, såsom `PngOptions` eller `BmpOptions`.

### Q2: Finns det en provversion tillgänglig?

A2: Ja, du kan utforska funktionaliteten i Aspose.CAD genom att ladda ner provversionen [här](https://releases.aspose.com/).

### Q3: Hur kan jag få support för Aspose.CAD?

A3: Besök Aspose.CAD‑[forumet](https://forum.aspose.com/c/cad/19) för community‑support eller överväg att köpa en licens för dedikerad support.

### Q4: Finns tillfälliga licenser tillgängliga?

A4: Ja, du kan skaffa en tillfällig licens [här](https://purchase.aspose.com/temporary-license/).

### Q5: Var kan jag hitta dokumentationen?

A5: Se den detaljerade dokumentationen [här](https://reference.aspose.com/cad/net/).

## Ytterligare FAQ

**Q: Kan jag exportera alla lager i ett kommando?**  
A: Ja, använd metoden `ConvertAllLayersToRasterImageFormats` som visas ovan.

**Q: Stöder Aspose.CAD vektorformat som SVG?**  
A: Det fokuserar främst på rasterformat, men du kan exportera till PDF som behåller vektordata.

**Q: Hur styr jag bakgrundsfärgen på den exporterade PNG‑filen?**  
A: Ställ in `rasterizationOptions.BackgroundColor` till önskad `Color` innan du sparar.

**Q: Är det möjligt att exportera en enskild layout istället för hela ritningen?**  
A: Ja, konfigurera `rasterizationOptions.Layouts` för att ange de layout‑namn du vill rasterisera.

## Slutsats

Du har nu lärt dig hur du **convert dxf to png**, **export cad layers** och **save cad as png** eller JPEG med Aspose.CAD för .NET. Genom att justera `CadRasterizationOptions` och byta bildformat‑alternativ kan du anpassa konverteringen till praktiskt taget vilken rasterutdata du än behöver. Utforska de andra formatalternativen i Aspose.CAD‑API:n för att bredda ditt CAD‑till‑raster‑arbetsflöde.

---

**Senast uppdaterad:** 2026-03-21  
**Testad med:** Aspose.CAD för .NET 24.11 (senaste vid skrivtillfället)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}