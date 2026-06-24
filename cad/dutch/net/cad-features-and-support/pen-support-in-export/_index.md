---
date: 2026-03-26
description: Leer hoe u PDF's maakt vanuit CAD en DXF naar PDF converteert met Aspose.CAD
  voor .NET. Pas penopties aan voor verbluffende visuals in PDF, PNG, BMP en meer.
linktitle: Pen Support in Export
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: PDF maken vanuit CAD met aangepaste penopties – Aspose.CAD voor .NET
url: /nl/net/cad-features-and-support/pen-support-in-export/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Verhoog CAD-export met aangepaste penopties in Aspose.CAD voor .NET

## Introductie

Als u **PDF vanuit CAD** snel en met volledige visuele controle wilt **creëren**, biedt Aspose.CAD voor .NET precies dat. Door gebruik te maken van de pen‑ondersteuningsfunctie van de bibliotheek kunt u start‑ en eindcaps, lijnverbindingen en andere teken‑attributen definiëren, waardoor PDF‑bestanden ontstaan die er precies uitzien zoals u wilt. Deze tutorial leidt u door het volledige proces — van het laden van een DXF‑bestand tot het exporteren van een gepolijste PDF — en laat tevens zien hoe dezelfde instellingen opnieuw kunnen worden gebruikt wanneer u **CAD naar PNG exporteert** of **CAD‑afbeeldingsgegevens rasteriseert** voor andere formaten.

## Snelle antwoorden
- **Wat betekent “create PDF from CAD”?** Het converteert vector‑gebaseerde CAD‑tekeningen (bijv. DXF) naar een PDF‑document terwijl geometrie en opmaak behouden blijven.  
- **Welke formaten ondersteunen penopties?** PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF en WMF.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Kan ik lijncaps wijzigen voor andere formaten?** Ja — penopties zijn van toepassing op elk rasterisatiedoel dat door Aspose.CAD wordt ondersteund.  
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Wat is penondersteuning bij CAD-export?

Penondersteuning stelt u in staat om aan te passen hoe lijnen worden getekend wanneer een CAD‑tekening wordt gerasterd of vector‑gerasterd. U kunt eigenschappen instellen zoals `StartCap`, `EndCap`, `LineJoin` en `DashStyle`. Deze instellingen beïnvloeden het uiteindelijke uiterlijk van de geëxporteerde afbeelding of PDF, waardoor u fijnmazige controle over de visuele kwaliteit krijgt.

## Waarom aangepaste penopties gebruiken wanneer u **create PDF from CAD**?

- **Consistente branding** – zorg voor uniforme lijnstijlen in alle documenten.  
- **Verbeterde leesbaarheid** – dikkere caps en verbindingen maken technische tekeningen duidelijker op scherm en papier.  
- **Cross‑formaat flexibiliteit** – dezelfde penconfiguratie werkt voor PNG, BMP en andere rasterformaten, waardoor u tijd bespaart.

## Vereisten

- Aspose.CAD voor .NET geïnstalleerd (download van de [release page](https://releases.aspose.com/cad/net/)).  
- Basiskennis van DXF (Drawing Exchange Format).  
- Vertrouwdheid met C#‑programmering.

## Importeren van namespaces

Zorg ervoor dat u de benodigde namespaces in uw C#‑project importeert:

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

## Stap 1: Stel uw documentmap in

Definieer de map die het bron‑CAD‑bestand bevat:

```csharp
string MyDir = "Your Document Directory";
```

## Stap 2: Laad de CAD‑afbeelding

Laad de CAD‑tekening (bijvoorbeeld een DXF‑bestand) in een `Aspose.CAD.Image`‑object:

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Stap 3: Configureer rasterisatie‑opties

Maak rasterisatie‑ en PDF‑optie‑objecten aan. Deze objecten laten u bepalen hoe de CAD‑gegevens worden omgezet naar een rasterafbeelding of PDF‑pagina:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Stap 4: Pas penopties aan

Hier stelt u de pen in die de lijnen tekent. U kunt de start‑ en eindcaps instellen op `Flat`, `Round`, `Square`, enz. Dit is de kern van “hoe CAD exporteren” met de gewenste visuele stijl:

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

*Pro tip:* Experimenteer met `LineCap.Round` voor soepelere lijneinden wanneer u **CAD naar PNG exporteert**.

## Stap 5: Pas vectorrasterisatie‑opties toe

Koppel de rasterisatie‑instellingen aan de PDF‑opties zodat het exportproces weet welke penconfiguratie moet worden gebruikt:

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Stap 6: Sla de geëxporteerde PDF op

Genereer tenslotte het PDF‑bestand. Deze stap **creëert PDF vanuit CAD** met de aangepaste peninstellingen toegepast:

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

U kunt `PdfOptions` vervangen door `PngOptions`, `BmpOptions`, enz., om **CAD naar PNG** of andere rasterformaten te exporteren terwijl u dezelfde penconfiguratie behoudt.

## Veelvoorkomende gebruikssituaties

- **Technische documentatie** – integreer precieze lijnstijlen in engineering‑PDF’s.  
- **Geautomatiseerde rapportgeneratie** – batch‑verwerk vele DXF‑bestanden naar PDF’s met één penprofiel.  
- **Webservices** – exposeer een API die geüploade DXF‑bestanden on‑the‑fly naar PDF converteert, met consistente opmaak.

## Probleemoplossing & veelvoorkomende valkuilen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| Geëxporteerde lijnen lijken dikker dan verwacht | DPI is hoger dan bedoeld | Stel `rasterizationOptions.PageWidth` / `PageHeight` in of pas `Resolution` aan. |
| Penopties worden genegeerd bij PNG‑output | `ImageOptions` in plaats van `VectorRasterizationOptions` gebruikt | Zorg ervoor dat u `rasterizationOptions.PenOptions` toewijst vóór het opslaan. |
| PDF‑bestand is leeg | Pad naar bron‑DXF is onjuist of bestand is corrupt | Controleer `sourceFilePath` en bevestig dat de DXF zonder uitzonderingen wordt geladen. |

## Veelgestelde vragen

### Q1: Kan ik deze penopties gebruiken voor andere afbeeldingsformaten naast PDF?

A1: Ja, de penopties kunnen worden toegepast op diverse afbeeldingsformaten zoals PNG, BMP, GIF, JPEG en meer.

### Q2: Waar vind ik aanvullende documentatie voor Aspose.CAD voor .NET?

A2: Raadpleeg de [documentation](https://reference.aspose.com/cad/net/) voor uitgebreide informatie en voorbeelden.

### Q3: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor .NET?

A3: Ja, u kunt een gratis proefversie krijgen [hier](https://releases.aspose.com/).

### Q4: Hoe kan ik tijdelijke licenties verkrijgen voor Aspose.CAD voor .NET?

A4: Bezoek de [temporary license page](https://purchase.aspose.com/temporary-license/) voor tijdelijke licentie‑opties.

### Q5: Waar kan ik community‑ondersteuning vinden voor Aspose.CAD voor .NET?

A5: Neem deel aan de community op het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

## Aanvullende veelgestelde vragen

**Q: Hoe **convert DXF to PDF** programmeermatig?**  
A: Laad de DXF met `Image.Load`, configureer `CadRasterizationOptions` en `PdfOptions`, en roep vervolgens `Save` aan zoals in de bovenstaande stappen.

**Q: Kan ik een CAD‑afbeelding rasteriseren zonder een PDF te maken?**  
A: Ja — gebruik `PngOptions`, `BmpOptions` of een andere rasterformaat‑klasse en wijs dezelfde `rasterizationOptions` toe voor hoogwaardige rasterisatie.

**Q: Is het mogelijk de lijndikte te wijzigen bij het maken van een PDF vanuit CAD?**  
A: Pas `rasterizationOptions.CustomLineWidth` aan of wijzig de eigenschap `PenOptions.Width` vóór het opslaan.

**Q: Ondersteunt de bibliotheek 3D‑DXF‑bestanden?**  
A: Aspose.CAD richt zich op 2D‑vectorgegevens; 3D‑entiteiten worden genegeerd tijdens rasterisatie.

**Q: Welke versie van Aspose.CAD is vereist voor deze functies?**  
A: Penondersteuning is beschikbaar sinds versie 20.9; elke nieuwere versie werkt.

---

**Laatst bijgewerkt:** 2026-03-26  
**Getest met:** Aspose.CAD voor .NET 24.12  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}