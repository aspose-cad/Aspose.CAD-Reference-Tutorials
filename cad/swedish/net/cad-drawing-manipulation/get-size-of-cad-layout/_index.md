---
date: 2026-03-21
description: Lär dig hur du får CAD‑layoutens storlek i .NET med Aspose.CAD. Följ
  vår steg‑för‑steg‑guide för effektiv CAD‑filhantering.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hämta CAD‑layoutstorlek i Aspose.CAD för .NET
url: /sv/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hämta CAD‑layoutstorlek i Aspose.CAD för .NET

## Introduktion

I den här omfattande handledningen kommer du att upptäcka **hur du får CAD‑layoutstorlek** med hjälp av Aspose.CAD‑biblioteket för .NET. Oavsett om du bygger en CAD‑visare, genererar miniatyrbilder eller behöver exakta layoutmått för efterföljande bearbetning, är det avgörande att känna till den exakta storleken på varje layout. Vi går igenom hela arbetsflödet – från att ladda en ritning till att extrahera layoutmått och eventuellt spara dem som bilder – så att du kan integrera denna funktion i dina egna applikationer med förtroende.

## Snabba svar
- **Vad betyder “get CAD layout size”?** Det innebär att hämta bredd och höjd (i ritningsenheter) för varje icke‑tom layout i en CAD‑fil.  
- **Vilket bibliotek stöder detta?** Aspose.CAD för .NET erbjuder ett enkelt API för att komma åt layoutinformation.  
- **Behöver jag en licens?** En gratis provversion fungerar för utvärdering; en kommersiell licens krävs för produktionsanvändning.  
- **Stödda format?** DWG, DXF och många andra CAD/BIM‑format stöds fullt ut.  
- **Typisk implementeringstid?** Ungefär 10‑15 minuter för ett grundläggande rutinskript som hämtar storlek.

## Vad betyder “get CAD layout size”?
Att hämta CAD‑layoutstorlek betyder att extrahera de geometriska gränserna för varje layout (paperspace) som definierats i en CAD‑ritning. Dessa gränser uttrycks i ritningens ursprungliga enheter (vanligtvis millimeter eller tum) och är användbara för uppgifter som skalning, utskrift eller generering av förhandsgranskningsbilder.

## Varför hämta CAD‑layoutstorlek med Aspose.CAD?
- **Ingen CAD‑programvara krävs** – Fungerar helt på serversidan.  
- **Cross‑platform** – Fungerar med .NET Framework, .NET Core och .NET 5/6+.  
- **Exakta mätningar** – Returnerar exakt de gränser som lagrats i filen, utan manuell parsning.  
- **Enkel integration** – Enkla API‑anrop passar naturligt in i befintliga C#‑projekt.

## Förutsättningar

Innan vi dyker ner i koden, se till att du har följande:

- Aspose.CAD för .NET installerat. Du kan ladda ner det från [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).
- En eller flera CAD‑filer (DWG, DXF, etc.) som du vill analysera. Denna guide använder `conic_pyramid.dxf` och `Bottom_plate.dwg` som exempel.

## Importera namnrymder

I ditt .NET‑projekt, börja med att importera de nödvändiga namnrymderna:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Steg 1: Ställ in dokumentkatalogen

Definiera mappen som innehåller dina CAD‑filer. Ersätt platshållaren med den faktiska sökvägen på din maskin.

```csharp
string MyDir = "Your Document Directory";
```

## Steg 2: Ange CAD‑filvägar

Skapa en array som pekar på varje CAD‑fil du vill bearbeta.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Steg 3: Iterera genom CAD‑filer

Läs in varje fil, identifiera dess format och förbered för att extrahera layoutinformation.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## Steg 4: Hämta icke‑tomma layouter

Vi behöver en hjälpfunktion som returnerar endast de layouter som faktiskt innehåller ritningsobjekt. Tomma layouter ignoreras eftersom de saknar storlek att rapportera.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## Steg 5: Hämta layouter för DWG‑filer

DWG‑filer lagrar layoutinformation i tabellen `HeaderVariables`. Följande metod extraherar namnen på alla icke‑tomma layouter för en DWG‑ritning.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Steg 6: Hämta layouter för DXF‑filer

DXF‑filer använder en annan struktur. Denna metod parsar samlingen `Tables` för att hitta paperspace‑layouter som innehåller entiteter.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Steg 7: Hämta layoutstorlek och spara som bild

Slutligen, loopa igenom varje upptäckt layout, läs dess gränser och rendera eventuellt layouten till en bildfil för visuell verifiering.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## Vanliga problem & tips

- **Saknade layoutnamn:** Säkerställ att CAD‑filen faktiskt innehåller paperspace‑layouter; vissa filer har bara modelspace.  
- **Fel enheter:** Storleken returneras i ritningens ursprungliga enheter. Konvertera till millimeter eller tum vid behov.  
- **Prestanda:** Inläsning av mycket stora DWG/DXF‑filer kan vara minnesintensiv; överväg att bearbeta filer asynkront eller i batcher.

## Vanliga frågor

**Q: Är Aspose.CAD kompatibel med alla CAD‑filformat?**  
A: Ja, Aspose.CAD stöder ett brett spektrum av format, inklusive DWG, DXF, DGN och många BIM‑filtyper.

**Q: Kan jag anpassa bild‑sparalternativen?**  
A: Absolut! Du kan justera `CadRasterizationOptions` (format, upplösning, bakgrundsfärg, etc.) för att möta dina specifika behov.

**Q: Var kan jag hitta ytterligare dokumentation?**  
A: Se [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) för detaljerade API‑referenser och fler exempel.

**Q: Finns det en gratis provversion?**  
A: Ja, du kan utforska Aspose.CAD med en [free trial](https://releases.aspose.com/).

**Q: Hur får jag teknisk support?**  
A: För teknisk support, besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

---

**Senast uppdaterad:** 2026-03-21  
**Testat med:** Aspose.CAD 24.11 för .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}