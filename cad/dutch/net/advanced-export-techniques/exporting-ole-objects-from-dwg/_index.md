---
description: Leer hoe u DWG naar PNG kunt converteren en OLE‑objecten uit DWG‑bestanden
  kunt extraheren met Aspose.CAD voor .NET – een snelle, code‑gerichte gids.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: DWG naar PNG converteren & OLE‑objecten exporteren – Aspose.CAD‑tutorial
url: /nl/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporteren van OLE-objecten uit DWG-bestanden - Aspose.CAD Tutorial

## Introductie

Als je **DWG naar PNG moet converteren** terwijl je ingebedde OLE-objecten eruit haalt, ben je hier aan het juiste adres. Aspose.CAD for .NET maakt dit twee‑stappenproces eenvoudig, zodat je extractie en rasterisatie kunt automatiseren met slechts een paar regels C#. In de komende minuten lopen we de volledige workflow door, van het instellen van je omgeving tot het opslaan van elke DWG als een PNG die de geëxtraheerde OLE-gegevens bevat.

## Snelle antwoorden
- **Waar gaat deze tutorial over?** Converting DWG to PNG and extracting OLE objects using Aspose.CAD for .NET.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Welke .NET-versies worden ondersteund?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Kan ik meerdere DWG-bestanden tegelijk verwerken?** Ja – het voorbeeld doorloopt een array met bestandsnamen.  
- **Waar kan ik meer voorbeelden vinden?** Bekijk de officiële Aspose.CAD-documentatie en forumlinks hieronder.

## Wat is **convert DWG to PNG**?
Het converteren van een DWG (AutoCAD-tekening) naar een PNG-afbeelding rastert de vectordata, waardoor het gemakkelijk te bekijken of in te sluiten is in webpagina's, rapporten of andere applicaties die DWG niet native ondersteunen. Wanneer OLE-objecten aanwezig zijn, kunnen ze tijdens de conversie worden geëxtraheerd en opgeslagen als afzonderlijke assets.

## Waarom OLE-objecten uit CAD-bestanden extraheren?
Veel DWG-tekeningen bevatten spreadsheets, grafieken of andere Office-documenten als OLE-objecten. Het extraheren ervan stelt je in staat de oorspronkelijke gegevens opnieuw te gebruiken, rapportage te automatiseren of inhoud naar nieuwere formaten te migreren zonder de ingebedde informatie te verliezen.

## Voorvereisten

- Aspose.CAD for .NET Library: Zorg ervoor dat je de bibliotheek geïnstalleerd hebt. Je kunt deze downloaden van de [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).
- Document Directory: Maak een map aan waar je DWG‑bestanden worden opgeslagen. Vervang `"Your Document Directory"` in de meegeleverde code‑snippet door het daadwerkelijke pad.

## Importer namespaces

Importeer in je .NET‑project de vereiste namespaces:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Stapsgewijze handleiding

### Stap 1: Stel de Document Directory in

```csharp
string MyDir = "Your Document Directory";
```

Vervang `"Your Document Directory"` door het pad waar je DWG‑bestanden zich bevinden.

### Stap 2: Lijst de DWG‑bestanden die je wilt verwerken

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Stap 3: Configureer exportopties voor PNG-conversie

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Je kunt `CadRasterizationOptions` aanpassen (bijv. `PageWidth`, `PageHeight`, `BackgroundColor`) om overeen te komen met de gewenste uitvoerresolutie.

### Stap 4: Doorloop elke DWG en voer de conversie uit

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Tijdens deze lus extraheert de bibliotheek automatisch **OLE-objecten** die in elke tekening zijn ingebed en voegt ze toe aan de gegenereerde PNG. Als je de ruwe OLE‑streams nodig hebt, kun je de `cadImage.OleObjects`‑collectie benaderen – een handige manier om **how to extract ole**-gegevens programmatisch te verkrijgen.

## Veelvoorkomende problemen & probleemoplossing

- **Ontbrekende lay-outnaam** – Zorg ervoor dat de lay-out die je opgeeft (`"Layout1"` in het voorbeeld) bestaat in de bron‑DWG; anders valt de rasterizer terug op de standaard modelspace.
- **Grote bestanden veroorzaken geheugenbelasting** – Verwerk bestanden één voor één (zoals getoond) en maak `CadImage`‑objecten direct vrij met `using`.
- **Onverwachte kleuren** – Stel `rasterizationOptions.BackgroundColor` in op de achtergrond van de tekening als transparantie vereist is.

## Veelgestelde vragen

### Q1: Is Aspose.CAD for .NET geschikt voor zowel junior- als senior-CAD‑bestanden?
A1: Ja, Aspose.CAD for .NET is veelzijdig en kan een breed scala aan CAD‑bestanden aan, inclusief zowel junior- als senior‑varianten.

### Q2: Kan ik exportopties aanpassen voor verschillende lay-outs?
A2: Absoluut! Zoals in de tutorial getoond, kun je exportopties, inclusief lay-outs, aanpassen aan je specifieke behoeften.

### Q3: Waar kan ik gedetailleerde documentatie vinden voor Aspose.CAD for .NET?
A3: Bekijk de [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/) voor diepgaande informatie en voorbeelden.

### Q4: Is er een gratis proefversie beschikbaar?
A4: Ja, je kunt de mogelijkheden van Aspose.CAD for .NET uitproberen met een gratis proefversie. Bezoek [this link](https://releases.aspose.com/) om te beginnen.

### Q5: Hoe kan ik ondersteuning krijgen of contact maken met de community?
A5: Voor ondersteuning en community‑interactie, bezoek het [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q6: Hoe kan ik **OLE uit CAD**-bestanden extraheren zonder naar PNG te converteren?
A6: Gebruik de `CadImage.OleObjects`‑collectie na het laden van de DWG; je kunt door elk `OleObject` itereren en de ruwe gegevens opslaan naar een bestand.

## Conclusie

Je hebt nu gezien hoe je **DWG naar PNG kunt converteren** terwijl je naadloos **OLE-objecten extraheert** met Aspose.CAD for .NET. Deze aanpak bespaart tijd, elimineert handmatige copy‑paste‑stappen en integreert soepel in geautomatiseerde pipelines. Voel je vrij om te experimenteren met andere rasterformaten (JPEG, BMP) of de uitgebreide set CAD‑bewerkingsfuncties van Aspose te verkennen.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}