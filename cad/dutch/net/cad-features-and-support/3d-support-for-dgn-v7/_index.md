---
date: 2026-03-24
description: Leer hoe je DGN naar PDF (en PNG) kunt converteren met 3D-ondersteuning
  voor DGN V7 met behulp van Aspose.CAD voor .NET – stapsgewijze handleiding.
linktitle: 3D Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DGN naar PDF converteren (3D-ondersteuning) met Aspose.CAD voor .NET
url: /nl/net/cad-features-and-support/3d-support-for-dgn-v7/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DGN naar PDF converteren (3D-ondersteuning) met Aspose.CAD voor .NET

## Inleiding

In moderne CAD‑workflows is het kunnen **DGN naar PDF converteren** snel en met behoud van 3‑D‑geometrie essentieel. Of je nu documentatie genereert, ontwerpen deelt met niet‑CAD‑belanghebbenden, of projecten archiveert, Aspose.CAD voor .NET biedt een betrouwbare manier om DGN V7‑bestanden om te zetten naar PDF‑output van hoge kwaliteit (en zelfs PNG). In deze tutorial lopen we stap voor stap door hoe je 3D‑ondersteuning inschakelt en een PDF maakt van een DGN‑bestand.

## Snelle antwoorden
- **Waar gaat de tutorial over?** Het inschakelen van 3D‑ondersteuning en het converteren van DGN V7 naar PDF met Aspose.CAD voor .NET.  
- **Welk primair formaat wordt geproduceerd?** PDF (met optionele PNG‑export).  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productie.  
- **Ondersteunde .NET‑versies?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basisconversie.

## Wat betekent “convert DGN to PDF”?

DGN naar PDF converteren houdt in dat de vectorgegevens in een MicroStation‑DGN‑bestand worden gerenderd naar een draagbaar documentformaat dat op elk apparaat kan worden bekeken zonder gespecialiseerde CAD‑software. Met de 3‑D‑rasterisatie‑engine van Aspose.CAD behoudt de conversie lay‑out, kleuren en diepte‑indicaties, waardoor een getrouwe visuele weergave ontstaat.

## Waarom Aspose.CAD gebruiken voor deze conversie?

- **Volledige 3‑D‑rasterisatie** – behoudt diepte‑ en lay‑outinformatie.  
- **Geen externe afhankelijkheden** – pure .NET‑bibliotheek, geen MicroStation nodig.  
- **Meerdere uitvoerformaten** – PDF, PNG, JPEG, TIFF, enz. (het secundaire trefwoord *convert dgn to png* wordt direct ondersteund).  
- **Cross‑platform** – werkt op Windows, Linux en macOS.

## Voorvereisten

Zorg ervoor dat je het volgende hebt:

- Aspose.CAD voor .NET geïnstalleerd. Je kunt het downloaden van de [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Een geldig DGN V7‑bestand dat je wilt verwerken.  
- Een .NET‑ontwikkelomgeving (Visual Studio, VS Code of de CLI). Installatie‑instructies zijn beschikbaar in de [.NET documentation](https://docs.microsoft.com/en-us/dotnet/core/install/).

## Namespaces importeren

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Deze namespaces geven je toegang tot de kernklassen van Aspose.CAD en standaard .NET‑hulpmiddelen.

## Stap 1: De omgeving instellen

Definieer waar je bron‑DGN‑bestand zich bevindt en waar de uitvoer‑PDF moet worden opgeslagen.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

> **Pro tip:** Gebruik `Path.Combine` voor platform‑onafhankelijke padconstructie.

## Stap 2: Het DGN‑bestand laden

Maak een `DgnImage`‑instantie door het bestand te laden met `Image.Load`. Deze stap bereidt de CAD‑gegevens voor rasterisatie voor.

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Code snippet continues...
}
```

## Stap 3: Exportopties configureren

Stel `PdfOptions` in samen met `CadRasterizationOptions`. Hier bepaal je paginagrootte, achtergrond en welke lay‑outs (views) moeten worden geëxporteerd.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Export specific views
    }
};
```

Als je in plaats daarvan **DGN naar PNG wilt converteren**, vervang je eenvoudig `PdfOptions` door `PngOptions` terwijl je dezelfde rasterisatie‑instellingen behoudt.

## Stap 4: Het resultaat opslaan

Schrijf tenslotte de gerenderde uitvoer naar de gewenste locatie.

```csharp
string outFile = "Your Output Directory"; // Specify the output directory
dgnImage.Save(outFile, options);
```

Na uitvoering vind je een PDF‑bestand (of PNG als je de opties hebt aangepast) dat een getrouwe weergave van de oorspronkelijke 3‑D‑DGN‑tekening biedt.

## Veelvoorkomende problemen & tips

- **Ontbrekende lay‑outs:** Zorg ervoor dat de lay‑outnamen in `Layouts` overeenkomen met die in het DGN‑bestand; anders worden ze genegeerd.  
- **Grote bestanden:** Verhoog `PageWidth`/`PageHeight` geleidelijk om overmatig geheugenverbruik te voorkomen.  
- **Kleuraccuratesse:** Als de achtergrond donker lijkt, controleer dan of `BackgroundColor` is ingesteld op de gewenste waarde (bijv. `Color.White`).

## Conclusie

Je hebt nu geleerd hoe je **DGN naar PDF kunt converteren** met volledige 3‑D‑ondersteuning met behulp van Aspose.CAD voor .NET. Deze workflow kan worden geïntegreerd in geautomatiseerde pipelines, desktop‑hulpmiddelen of webservices om CAD‑visualisaties aan elk publiek te leveren.

## Veelgestelde vragen

### Q1: Kan ik meerdere DGN‑bestanden tegelijk verwerken met deze aanpak?

A1: Ja, je kunt de code aanpassen om meerdere bestanden binnen een lus of als onderdeel van een batch‑verwerkingssysteem af te handelen.

### Q2: Welke andere exportformaten ondersteunt Aspose.CAD voor .NET?

A2: Aspose.CAD voor .NET ondersteunt diverse exportformaten, waaronder PDF, PNG, JPG en meer. Zie de [documentation](https://reference.aspose.com/cad/net/) voor details.

### Q3: Is Aspose.CAD voor .NET compatibel met de nieuwste .NET Core‑versies?

A3: Ja, Aspose.CAD voor .NET is ontworpen om compatibel te zijn met de nieuwste .NET Core‑versies. Zorg ervoor dat je de juiste versie in je omgeving hebt geïnstalleerd.

### Q4: Kan ik de exportinstellingen verder aanpassen voor mijn specifieke eisen?

A4: Absoluut! De geleverde code biedt een startpunt. Je kunt extra opties en configuraties verkennen in de [Aspose.CAD documentation](https://reference.aspose.com/cad/net/).

### Q5: Waar kan ik hulp zoeken of mijn ervaringen delen over Aspose.CAD voor .NET?

A5: Word lid van de Aspose.CAD‑community op het [forum](https://forum.aspose.com/c/cad/19) om met andere ontwikkelaars te communiceren en ondersteuning te krijgen.

---

**Last Updated:** 2026-03-24  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}