---
date: 2026-03-19
description: Lär dig hur du ändrar storlek på CAD-ritningar i .NET med Aspose.CAD,
  inklusive hur du skalar CAD-ritningsenheter och justerar layoutstorlek. Följ vår
  steg‑för‑steg‑guide.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Hur man ändrar storlek på CAD-ritningar med Aspose.CAD för .NET
url: /sv/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man ändrar storlek på CAD-ritningar med Aspose.CAD för .NET

## Introduktion

Om du behöver **how to resize CAD**-filer direkt från din .NET-applikation, har du kommit till rätt ställe. I den här handledningen visar vi hur du ändrar CAD-enhetsinställningar, skalar CAD-ritningsdimensioner och justerar CAD-storlek programmässigt med Aspose.CAD för .NET. I slutet av guiden har du en solid, produktionsklar lösning för att ändra storlek på alla stödda CAD-format.

## Snabba svar
- **Vilket bibliotek krävs?** Aspose.CAD for .NET  
- **Kan jag ändra enhetstypen?** Ja – sätt `UnitType` i `CadRasterizationOptions`  
- **Behövs en licens för produktion?** En giltig Aspose.CAD-licens krävs för icke‑trial use  
- **Vilket bildformat exporterar exemplet till?** BMP (men alla stödda rasterformat fungerar)  
- **Hur många kodrader?** Mindre än 30 rader för en komplett resize operation  

## Vad betyder “how to resize CAD” i praktiken?
Att ändra storlek på en CAD-ritning innebär att konvertera vektordata till en rasterbild med en specifik skala eller enhet (t.ex. centimeter, tum). Detta är användbart när du behöver bädda in ritningar i rapporter, skapa miniatyrbilder eller integrera CAD‑visualiseringar i webbsidor.

## Varför justera CAD-storlek med Aspose.CAD?
- **Ingen extern CAD‑programvara** – allt körs inom din .NET‑kod.  
- **Finjusterad kontroll** över enheter, layouter och rasteriseringsalternativ.  
- **Stöd för flera format** – samma kod fungerar för DWG, DXF, DWF och fler.  

## Förutsättningar

Innan vi dyker ner, se till att du har:

- Aspose.CAD for .NET-biblioteket: Ladda ner och installera biblioteket från [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Exempel på CAD-ritning: En fil som `sample.dwg` placerad i ditt projekts dokumentkatalog.  

## Importera namnrymder

Först importerar du namnrymderna som ger dig åtkomst till Aspose.CAD:s klasser.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Steg 1: Ladda CAD-ritningen

Ladda källfilen i ett `Image`-objekt. Detta objekt representerar CAD-ritningen i minnet och kommer att vara grunden för alla vidare operationer.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Steg 2: Skapa BmpOptions (eller något annat rasterformat)

`BmpOptions` talar om för Aspose.CAD hur vektordatan ska renderas när du sparar den som en bitmap. Du kan byta ut detta mot `PngOptions`, `JpegOptions` osv., beroende på ditt målformat.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Steg 3: Ställ in CadRasterizationOptions

`CadRasterizationOptions` innehåller de grundläggande inställningarna för skalning, enhetskonvertering och layoutval. Genom att länka den till egenskapen `VectorRasterizationOptions` i `BmpOptions` säkerställer du att rasteriseraren använder dina anpassade inställningar.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Steg 4: Ställ in UnitType (ändra CAD-enhet)

Här ändrar vi CAD-enheten från standard till centimeter. Det är här nyckelordet **change cad unit** finns, och det påverkar direkt den slutliga bildstorleken.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Steg 5: Välj layouter (ange CAD‑layouter)

Om din ritning innehåller flera layouter (t.ex. Model, Sheet1), ange vilka du vill rasterisera. Att välja rätt layout är avgörande när du **set cad layouts** för en storleksändrad utdata.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Steg 6: Exportera till BMP (ändra storlek på CAD-ritning)

Spara slutligen den rasteriserade bilden. Utdatafilen återspeglar den nya storleken, enheten och layouten du konfigurerade – vilket effektivt slutför **resize CAD drawing**-operationen.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Du har nu en BMP-fil som representerar den storleksändrade CAD-ritningen, redo för vidare bearbetning eller visning.

## Vanliga problem och lösningar

| Problem | Varför det händer | Lösning |
|---------|-------------------|---------|
| Utdata är suddig | Lågt DPI (dots per inch) som standard | Ställ `cadRasterizationOptions.Resolution = 300;` innan du sparar |
| Fel layout visas | Felstavning av layoutnamn | Verifiera det exakta layoutnamnet med en CAD‑visare eller `Layouts`‑samlingen |
| Enhetskonvertering ser felaktig ut | Blandning av metriska och imperiella enheter | Se till att `UnitType` matchar det önskade mätsystemet |

## Vanliga frågor

### Q1: Är Aspose.CAD för .NET kompatibel med alla CAD-format?

A1: Aspose.CAD för .NET stöder ett brett spektrum av CAD-format, inklusive DWG, DXF, DWF och fler. Se [documentation](https://reference.aspose.com/cad/net/) för den kompletta listan.

### Q2: Kan jag ändra storlek på flera layouter samtidigt?

A2: Ja, du kan ändra storlek på flera layouter genom att justera `Layouts`‑arrayen i `CadRasterizationOptions`.

### Q3: Var kan jag få support för Aspose.CAD för .NET?

A3: Besök [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för community‑support och hjälp.

### Q4: Finns det en gratis provperiod tillgänglig?

A4: Ja, du kan prova en [free trial](https://releases.aspose.com/) för att utvärdera funktionerna i Aspose.CAD för .NET.

### Q5: Hur kan jag skaffa en tillfällig licens för Aspose.CAD för .NET?

A5: Skaffa en tillfällig licens för teständamål [here](https://purchase.aspose.com/temporary-license/).

## Vanliga frågor

**Q: Hur skalar jag en CAD-ritning utan att ändra enhetstypen?**  
A: Justera `Zoom`‑egenskapen i `CadRasterizationOptions` (t.ex. `cadRasterizationOptions.Zoom = 2.0;`) för att dubbla storleken samtidigt som du behåller originalenheten.

**Q: Kan jag exportera till andra format än BMP?**  
A: Absolut. Byt ut `BmpOptions` mot `PngOptions`, `JpegOptions` eller någon annan stödjande rasterformatklass.

**Q: Är det möjligt att batch‑processa en mapp med ritningar?**  
A: Ja. Loopa igenom filerna i en katalog, tillämpa samma rasteriseringslogik och spara varje utdata med ett unikt namn.

---

**Senast uppdaterad:** 2026-03-19  
**Testat med:** Aspose.CAD for .NET 24.11 (senaste vid skrivtillfället)  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}