---
date: 2026-03-13
description: Leer hoe u CAD‑rasterisatie‑opties instelt en specifieke DWG‑indelingen
  exporteert naar PDF met Aspose.CAD voor .NET – de definitieve gids om een PDF te
  maken van een CAD‑bestand.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Stel CAD-rasterisatieopties in – Exporteer specifieke lay-outs naar PDF - Aspose.CAD-gids
url: /nl/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporteren van specifieke lay-outs naar PDF - Aspose.CAD-gids

## Inleiding

In deze tutorial ontdek je **hoe je CAD-rasterisatie‑opties instelt** zodat je een enkele lay-out – of meerdere lay-outs – uit een DWG‑bestand direct naar PDF kunt exporteren. Aspose.CAD voor .NET maakt het *dwg to pdf conversion c#* proces eenvoudig, en geeft je volledige controle over paginagrootte, resolutie en lay-outselectie. Aan het einde van de gids kun je **PDF maken van CAD‑bestand** met slechts een paar regels code.

## Snelle antwoorden
- **Wat doet “set cad rasterization options”?**  
  Het vertelt Aspose.CAD hoe vectorgegevens (lay-outs, lagen, lijndiktes) te renderen naar gerasterde PDF‑pagina's.  
- **Welke methode exporteert een DWG‑lay-out naar PDF?**  
  Gebruik `Image.Save` met een geconfigureerde `PdfOptions` die jouw `CadRasterizationOptions` bevat.  
- **Kan ik meer dan één lay-out tegelijk exporteren?**  
  Ja – geef een array met lay-outnamen op in de `Layouts`‑eigenschap.  
- **Heb ik een licentie nodig voor productiegebruik?**  
  Een commerciële licentie is vereist; een gratis proefversie is beschikbaar voor evaluatie.  
- **Welke .NET‑versies worden ondersteund?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 en later.

## Wat is “set cad rasterization options”?
`CadRasterizationOptions` is de klasse die bepaalt hoe CAD‑entiteiten worden gerasterd bij het converteren naar raster‑gebaseerde formaten zoals PDF. Door zijn eigenschappen te configureren – paginagrootte, lay-outselectie, achtergrondkleur, enz. – bepaal je het visuele resultaat van de **export dwg layout to pdf** operatie.

## Waarom CAD‑rasterisatie‑opties instellen?
- **Precisie** – Behoud lijndiktes en schalen precies zoals ze in de originele CAD‑tekening verschijnen.  
- **Prestaties** – Render alleen de lay-outs die je nodig hebt, waardoor bestandsgrootte en verwerkingstijd verminderen.  
- **Flexibiliteit** – Pas paginabreedte/hoogte, DPI en achtergrond aan om te voldoen aan je rapportage‑normen.  

## Voorvereisten

Voordat we in de code duiken, zorg ervoor dat je het volgende hebt:

- **Aspose.CAD for .NET** geïnstalleerd. Je kunt het downloaden [hier](https://releases.aspose.com/cad/net/).  
- Een .NET‑ontwikkelomgeving (Visual Studio, VS Code, of een IDE naar keuze).  
- Een DWG‑bestand dat minstens één lay-out bevat (het voorbeeldbestand dat hier wordt gebruikt is `visualization_-_conference_room.dwg`).

## Importeren van namespaces

Importeer in je .NET-project de benodigde namespaces voor Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stapsgewijze handleiding

### Stap 1: Laad het DWG‑bestand

Geef eerst Aspose.CAD het bron‑DWG‑bestand dat je wilt converteren.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Stap 2: Stel **CadRasterizationOptions** in

Hier configureren we de rasterisatie‑instellingen die de PDF‑paginagrootte en resolutie bepalen.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Pro tip:** Pas `PageWidth` en `PageHeight` aan zodat ze overeenkomen met de afmetingen van je doel‑PDF‑lay-out. Grotere waarden verhogen de detail, maar ook de bestandsgrootte.

### Stap 3: Specificeer de lay-outnaam

Geef Aspose.CAD aan welke lay-out(s) gerenderd moeten worden. Vervang `"Layout1"` door de exacte naam van de lay-out in je DWG‑bestand.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Waarom dit belangrijk is:** Door de `Layouts`‑array te beperken, voorkom je het exporteren van ongewenste bladen, waardoor de **dwg to pdf conversion c#** operatie sneller wordt en de resulterende PDF schoner.

### Stap 4: Maak `PdfOptions` aan

Koppel de rasterisatie‑instellingen aan de PDF‑exportopties.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Stap 5: Exporteren naar PDF

Sla tenslotte de gerenderde lay-out op als een PDF‑bestand.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Stap 6: Toon een succesbericht

Een korte console‑uitvoer bevestigt dat de operatie geslaagd is.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Veelvoorkomende problemen & oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **Geen PDF gegenereerd** | `Layouts`‑array komt niet overeen met een lay-outnaam in de DWG. | Controleer de lay-outnamen met een CAD‑viewer en werk de `Layouts`‑eigenschap bij. |
| **Lege pagina's** | `PageWidth`/`PageHeight` ingesteld op 0 of extreem kleine waarden. | Gebruik realistische afmetingen (bijv. 1600 × 1600) of laat Aspose automatisch berekenen door die eigenschappen weg te laten. |
| **Onjuiste schaal** | DPI niet ingesteld wanneer een hoge resolutie‑output vereist is. | Stel `rasterizationOptions.Resolution = 300;` (of gewenste DPI) in vóór het exporteren. |

## Veelgestelde vragen

**V: Kan ik meerdere lay-outs tegelijk exporteren?**  
A: Ja, wijzig eenvoudig de `Layouts`‑array in Stap 3 om alle gewenste lay-outnamen op te nemen, bijv. `new string[] { "Layout1", "Layout2" }`.

**V: Is Aspose.CAD compatibel met andere CAD‑bestandsformaten?**  
A: Absoluut. Het ondersteunt DWG, DXF, DWF, DGN en nog veel meer formaten.

**V: Hoe kan ik de PDF‑outputinstellingen aanpassen naast paginagrootte?**  
A: Verken extra eigenschappen van `CadRasterizationOptions` zoals `Resolution`, `BackgroundColor` en `DrawType` om het resultaat fijn af te stemmen.

**V: Waar kan ik extra Aspose.CAD‑documentatie vinden?**  
A: Bezoek de [documentatie](https://reference.aspose.com/cad/net/) voor uitgebreide API‑referenties en voorbeelden.

**V: Is er een gratis proefversie beschikbaar?**  
A: Ja, je kunt de gratis proefversie [hier](https://releases.aspose.com/) benaderen.

## Conclusie

Je hebt nu geleerd hoe je **CAD‑rasterisatie‑opties instelt** en deze gebruikt om **specifieke DWG‑lay-outs naar PDF te exporteren** met Aspose.CAD voor .NET. Deze aanpak geeft je precieze controle over het conversieproces, waardoor je CAD‑naar‑PDF‑functionaliteit snel en betrouwbaar in elke C#‑applicatie kunt integreren.

---

**Laatst bijgewerkt:** 2026-03-13  
**Getest met:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}