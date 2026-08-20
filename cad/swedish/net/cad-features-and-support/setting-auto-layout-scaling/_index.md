---
date: 2026-03-26
description: Lär dig hur du skapar PDF från CAD och konverterar DXF till PDF med Aspose.CAD
  för .NET med automatisk layoutskalning för exakt, anpassningsbar rendering.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Skapa PDF från CAD: Automatisk layoutskalning – Aspose.CAD'
url: /sv/net/cad-features-and-support/setting-auto-layout-scaling/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa PDF från CAD: Auto Layout Scaling – Aspose.CAD

I moderna .NET‑applikationer är det vanligt att omvandla CAD‑ritningar till högkvalitativa PDF‑filer — oavsett om du behöver **create PDF from CAD** för rapportering, delning eller arkivering. Denna handledning visar hur du använder Aspose.CAD för .NET för att aktivera Auto Layout Scaling, vilket ger dig pixelperfekta resultat samt visar hur du **convert DXF to PDF** och **export CAD to PDF** med minimal kod.

## Snabba svar
- **Vad gör Auto Layout Scaling?** Det justerar automatiskt layouten så att den passar sidstorleken och bevarar geometrins noggrannhet.  
- **Vilka format stöds?** Alla format som Aspose.CAD kan läsa (DXF, DWG, DGN, etc.) kan exporteras till PDF.  
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Kan jag ändra sidstorlek?** Ja — ange `PageWidth` och `PageHeight` i `CadRasterizationOptions`.  
- **Är den kompatibel med .NET Core?** Absolut, fungerar med .NET Framework och .NET Core/5/6+.

## Vad betyder “create PDF from CAD”?
Att skapa en PDF från en CAD‑fil innebär att rasterisera vektordata till ett portabelt dokumentformat. Denna konvertering behåller lager, linjebredder och färger samtidigt som filen kan visas på vilken enhet som helst utan CAD‑programvara.

## Varför använda Auto Layout Scaling?
Auto Layout Scaling säkerställer att hela ritningen passar snyggt på utskrifts‑sidan, utan att du manuellt måste beräkna skalningsfaktorer. Det är särskilt användbart när du arbetar med ritningar av varierande dimensioner, såsom arkitektoniska plan eller mekaniska scheman.

## Förutsättningar
Innan du börjar, se till att du har:

1. **Aspose.CAD for .NET** – ladda ner det senaste biblioteket från [download page](https://releases.aspose.com/cad/net/).  
2. **En .NET‑utvecklingsmiljö** – Visual Studio, Rider eller någon editor som stödjer C#.  
3. **En exempel‑DXF‑fil** – t.ex. `conic_pyramid.dxf`, eller någon annan CAD‑fil du vill konvertera.

## Importera namnrymder
Lägg till de nödvändiga namnrymderna så att du kan komma åt Aspose.CAD‑klasser.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Steg 1: Läs in CAD‑filen
Läs in källritningen i ett `Image`‑objekt. Detta är startpunkten för all vidare bearbetning.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Steg 2: Konfigurera rasteriseringsalternativ
Definiera utskriftssidans dimensioner. Justera dessa värden för att matcha önskad PDF‑storlek.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Steg 3: Aktivera Auto Layout Scaling
Slå på automatisk skalning så att ritningen passar sidan utan beskärning.

```csharp
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Steg 4: Skapa PDF‑alternativ
Koppla rasteriseringsinställningarna till PDF‑exportören.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Steg 5: Spara resultatet – create PDF from CAD
Ange utdatavägen och spara bilden som en PDF. Detta steg **creates PDF from CAD** med den skalning du konfigurerat.

```csharp
MyDir = MyDir + "result_out.pdf";
image.Save(MyDir, pdfOptions);
```

## Vanliga problem & tips
- **Saknas teckensnitt eller linjestilar?** Säkerställ att CAD‑filens referenser är inbäddade eller tillgängliga på servern.  
- **Stora filer ger minnespress?** Bearbeta ritningen i delar eller öka applikationens minnesgräns.  
- **Utdatan ser suddig ut?** Öka `PageWidth`/`PageHeight` för högre DPI, eller sätt `Resolution` i `CadRasterizationOptions`.

## Vanliga frågor

**Q: Kan jag använda Auto Layout Scaling för andra filformat än DXF?**  
A: Ja, Aspose.CAD stödjer DWG, DGN och många andra CAD‑format för automatisk skalning.

**Q: Hur kan jag hantera fel under renderingsprocessen?**  
A: Omge konverteringskoden med ett `try‑catch`‑block och fånga `Aspose.CAD.CadException` för detaljerad felinformation.

**Q: Finns det någon gräns för filstorleken som Aspose.CAD kan hantera?**  
A: Biblioteket är byggt för stora filer, men prestandan beror på tillgängligt RAM och CPU. Överväg att bearbeta mycket stora ritningar på en server med rikliga resurser.

**Q: Kan jag ytterligare anpassa den exporterade PDF‑filen (t.ex. lägga till vattenstämplar eller metadata)?**  
A: Absolut. Efter sparandet kan du använda Aspose.PDF för att modifiera PDF‑filen — lägga till vattenstämplar, sätta dokumentegenskaper eller slå ihop sidor.

**Q: Var kan jag hitta ytterligare resurser och support för Aspose.CAD?**  
A: Utforska [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) för community‑hjälp, och se [documentation](https://reference.aspose.com/cad/net/) för djupare API‑detaljer.

## Slutsats
Du har nu lärt dig hur du **create PDF from CAD**, aktiverar **Auto Layout Scaling** och effektivt **convert DXF to PDF** med Aspose.CAD för .NET. Detta tillvägagångssätt ger dig full kontroll över renderingskvaliteten samtidigt som implementeringen förblir enkel.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2026-03-26  
**Testad med:** Aspose.CAD for .NET 24.12 (latest)  
**Författare:** Aspose  

---