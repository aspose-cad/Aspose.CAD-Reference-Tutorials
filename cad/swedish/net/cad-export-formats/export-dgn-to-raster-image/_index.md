---
date: 2026-03-24
description: Lär dig hur du konverterar DGN till PNG och sparar CAD som JPEG med Aspose.CAD
  för .NET – en snabb guide för CAD‑till‑bild‑konvertering.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hur man konverterar DGN till PNG i Aspose.CAD för .NET
url: /sv/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera DGN till PNG i Aspose.CAD för .NET

I modern .NET-utveckling är **convert dgn to png** ett vanligt krav när du behöver visa CAD-ritningar på webben eller bädda in dem i rapporter. Aspose.CAD för .NET gör denna konvertering enkel, så att du kan omvandla en DGN‑fil till en högkvalitativ rasterbild med bara några rader kod. I den här guiden går vi igenom hela processen, från att konfigurera projektet till att spara den slutgiltiga PNG‑ (eller JPEG‑) filen.

## Snabba svar
- **Kan jag konvertera DGN till PNG med Aspose.CAD?** Ja – konfigurera bara rasteriseringsalternativen och välj PNG‑ eller JPEG‑utdata.  
- **Behöver jag en licens för produktionsanvändning?** En giltig Aspose.CAD‑licens krävs för icke‑testdistributioner.  
- **Vilka .NET‑versioner stöds?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Vilka bildformat är tillgängliga?** PNG, JPEG, BMP, GIF, TIFF och mer.  
- **Är undantagshantering nödvändig?** Absolut – omslut konverteringen med try/catch för att hantera filåtkomstproblem.

## Vad är “convert dgn to png”?
Att konvertera en DGN‑fil (MicroStation) till PNG innebär att rasterisera vektordata från CAD till en pixelbaserad bild. Detta är användbart för att skapa förhandsgranskningar, bädda in ritningar i HTML‑mail eller skapa miniatyrbilder för dokumenthanteringssystem.

## Varför använda Aspose.CAD för CAD‑till‑bild‑konvertering?
- **Inga externa beroenden** – fungerar enbart i hanterad kod.  
- **Hög trohet** – bevarar linjebredder, lager och färger.  
- **Flexibel utdata** – byt mellan PNG, JPEG, BMP osv. genom att ändra ett enda alternativ.  
- **Prestandaoptimerad** – rasterisering är snabb även för stora ritningar.

## Förutsättningar

Innan vi börjar, se till att du har:

- **Aspose.CAD för .NET** installerat i ditt projekt. Du kan ladda ner det från [webbplatsen](https://reference.aspose.com/cad/net/).  
- En exempel‑DGN‑fil (t.ex. `Nikon_D90_Camera.dgn`) placerad i en känd katalog.

## Importera namnrymder

Börja med att lägga till de nödvändiga `using`‑satserna så att du kan komma åt Aspose.CAD‑klasser.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Steg 1: Läs in DGN‑filen

Läs in käll‑DGN‑filen i ett `CadImage`‑objekt. Detta objekt representerar CAD‑ritningen i minnet och blir källan för rasteriseringen.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Steg 2: Definiera rasteriseringsalternativ

Konfigurera hur CAD‑ritningen ska rasteriseras. Här kan du styra bildstorlek, skalning och bakgrundsfärg.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Steg 3: Välj utdataformat (PNG eller JPEG)

Även om handledningen fokuserar på PNG kan du också vilja **save cad as jpeg**. Skapa det lämpliga bildalternativ‑objektet och koppla rasteriseringsinställningarna.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Proffstips:** För att generera en PNG‑fil, ersätt `new JpegOptions()` med `new PngOptions()`.

## Steg 4: Spara rasterbilden

Slutligen anropar du `Save` på `CadImage`‑instansen och anger önskat filnamn samt det alternativ‑objekt du konfigurerat.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Om du bytte till `PngOptions` sparas filen som `ExportDGNToRasterImage_out.png`.

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|-------|-------|-----|
| **Tomt utdata‑bild** | `NoScaling` är felaktigt inställt eller layout ej vald | Sätt `AutomaticLayoutsScaling = true` eller specificera önskad layout. |
| **Out‑of‑memory för stora filer** | Laddar enorm DGN utan streaming | Använd `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Ej stöd för DGN‑version** | Äldre MicroStation‑versioner | Säkerställ att du har den senaste Aspose.CAD‑versionen som stödjer äldre format. |

## Vanliga frågor

**Q: Kan jag exportera DGN‑filer till andra format än JPEG?**  
A: Ja, Aspose.CAD för .NET stödjer PNG, BMP, GIF, TIFF och mer – byt bara options‑klassen (t.ex. `new PngOptions()`).

**Q: Hur bör jag hantera undantag under konverteringen?**  
A: Omslut konverteringskoden med ett `try/catch`‑block och logga `Aspose.CAD.CadException` för detaljerad felinformation.

**Q: Finns det en provversion av Aspose.CAD för .NET?**  
A: Ja, du kan prova produkten med en gratis provperiod. Besök [här](https://releases.aspose.com/) för mer information.

**Q: Vart kan jag få hjälp eller diskutera problem relaterade till Aspose.CAD för .NET?**  
A: Gå till [Aspose.CAD‑forumet](https://forum.aspose.com/c/cad/19) för community‑stöd och diskussioner.

**Q: Hur får jag en tillfällig licens för Aspose.CAD för .NET?**  
A: Besök [denna länk](https://purchase.aspose.com/temporary-license/) för att skaffa en tillfällig licens för dina utvecklingsbehov.

## Slutsats

Du har nu lärt dig hur du **convert dgn to png** (eller JPEG) med Aspose.CAD för .NET. Genom att justera rasteriseringsalternativen och byta bild‑options‑klassen kan du anpassa utdata efter alla projektkrav. Känn dig fri att experimentera med olika sidstorlekar, DPI‑inställningar och filformat för att få den perfekta rasterbilden för din applikation.

---

**Senast uppdaterad:** 2026-03-24  
**Testad med:** Aspose.CAD 24.11 för .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}