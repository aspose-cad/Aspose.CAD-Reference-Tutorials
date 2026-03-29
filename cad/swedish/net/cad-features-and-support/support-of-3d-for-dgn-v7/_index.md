---
date: 2026-03-29
description: Lär dig hur du konfigurerar CAD‑rasteriseringsalternativ och exporterar
  DGN till PDF med 3D‑stöd med hjälp av Aspose.CAD för .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konfigurera CAD‑rasteriseringsalternativ för DGN V7 3D
url: /sv/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konfigurera CAD-rasteriseringsalternativ för DGN V7 3D

## Introduktion

I den här omfattande handledningen kommer du att lära dig **hur du konfigurerar CAD-rasteriseringsalternativ** för att exportera en 3‑D DGN V7-fil till PDF med Aspose.CAD för .NET. Oavsett om du bygger en CAD‑visare, ett rapportverktyg eller en automatiserad konverteringspipeline, ger behärskning av dessa inställningar dig exakt kontroll över sidstorlek, layout‑skalning, bakgrundsfärger och de specifika vyerna du vill rendera. Låt oss gå igenom processen steg för steg.

## Snabba svar
- **Vad betyder “configure CAD rasterization options”?**  
  Det avser att ställa in egenskaper såsom sidmått, skalning, bakgrundsfärg och layoutval innan en CAD‑fil konverteras till ett rasterformat (t.ex. PDF).
- **Hur exporterar man DGN till PDF med 3‑D‑stöd?**  
  Läs in DGN med `DgnImage`, definiera `PdfOptions` + `CadRasterizationOptions` och anropa sedan `Save`.
- **Behöver jag en licens för produktionsanvändning?**  
  Ja – en kommersiell licens krävs för distribution; en gratis provversion finns tillgänglig.
- **Vilka .NET‑versioner stöds?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Kan jag välja specifika vyer att exportera?**  
  Absolut – sätt `Layouts`‑arrayen i rasteriseringsalternativen.

## Vad är “configure CAD rasterization options”?

Att konfigurera CAD-rasteriseringsalternativ innebär att anpassa hur en CAD‑ritning rasteriseras (konverteras från vektor till bitmap eller PDF). Genom att justera dessa inställningar styr du den visuella utdata, prestanda och filstorlek för det resulterande dokumentet.

## Varför använda Aspose.CAD för 3‑D DGN V7‑export?

- **Full .NET-integration** – ingen COM eller inhemska DLL‑filer krävs.  
- **Stöder 3‑D‑geometri** – behåller djupinformation vid rendering till PDF.  
- **Fin‑granulär kontroll** – välj exakta layouter, skalning och bakgrundsfärger.  
- **Plattformsoberoende** – fungerar på Windows, Linux och macOS med .NET Core.

## Förutsättningar

Innan du börjar, se till att du har:

- **Aspose.CAD for .NET** – ladda ner det från [here](https://releases.aspose.com/cad/net/).  
- **Visual Studio** eller någon kompatibel .NET‑IDE.  
- **En exempel‑DGN‑fil** – för den här guiden använder vi `Nikon_D90_Camera.dgn` (inkluderad i Aspose‑exempelpaketet).  

Nu när allt är klart, låt oss dyka ner i koden.

## Importera namnrymder

I ditt .NET‑projekt, importera de nödvändiga namnrymderna:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Steg 1: Ställ in din dokumentkatalog

Skapa en variabel som pekar på mappen där din käll‑DGN och utdatafilerna kommer att ligga.

```csharp
string MyDir = "Your Document Directory";
```

## Steg 2: Läs in DGN‑filen

Läs in DGN‑filen som en `DgnImage`. Detta objekt ger dig åtkomst till CAD‑data och rasteriserings‑pipeline.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Steg 3: Konfigurera PDF‑exportalternativ (Configure CAD Rasterization Options)

Här **konfigurerar vi CAD-rasteriseringsalternativ** som bestämmer hur 3‑D‑modellen renderas till PDF. Du kan justera sidstorlek, aktivera automatisk layout‑skalning, ange en bakgrundsfärg och välja exakt vilka layouter (vyer) du vill exportera.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Steg 4: Spara rasterbilden

Slutligen exporterar du DGN till en PDF‑fil med de alternativ du just konfigurerat.

```csharp
dgnImage.Save(outFile, options);
```

## Vanliga problem och lösningar

| Problem | Lösning |
|-------|----------|
| **Tom PDF‑utdata** | Verifiera att `Layouts`‑arrayen innehåller de korrekta vyidentifierarna som finns i DGN‑filen. |
| **Felaktiga färger** | Se till att `BackgroundColor` är inställd på önskat värde; använd `Color.White` för en ljus bakgrund. |
| **Prestandaflaskhals på stora filer** | Aktivera `AutomaticLayoutsScaling` och överväg att minska `PageWidth/PageHeight` för en lägre rasterupplösning. |
| **Licensundantag** | Installera en giltig Aspose.CAD‑licens innan du läser in bilden för att undvika vattenstämplar från provversionen. |

## Vanliga frågor

**Q: Kan jag använda Aspose.CAD för .NET med andra CAD‑filformat?**  
A: Ja, Aspose.CAD stöder DWG, DXF, DWF, DGN och många fler format.

**Q: Hur kan jag hantera undantag när jag arbetar med Aspose.CAD?**  
A: Omge din kod med ett `try‑catch`‑block och inspektera `Aspose.CAD.CADException` för detaljerad felinformation.

**Q: Är Aspose.CAD lämplig för kommersiella projekt?**  
A: Absolut. Du kan köpa en licens [here](https://purchase.aspose.com/buy).

**Q: Kan jag prova Aspose.CAD för .NET innan jag köper?**  
A: Ja, en gratis provversion finns tillgänglig [here](https://releases.aspose.com/).

**Q: Var kan jag hitta community‑support för Aspose.CAD?**  
A: Gå med i diskussionsforumet [here](https://forum.aspose.com/c/cad/19).

---

**Senast uppdaterad:** 2026-03-29  
**Testad med:** Aspose.CAD 24.11 for .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}