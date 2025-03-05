---
title: 3D-afbeeldingen exporteren naar PDF - Aspose.CAD-zelfstudie
linktitle: 3D-afbeeldingen exporteren naar PDF
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Converteer moeiteloos 3D CAD-afbeeldingen naar PDF met Aspose.CAD voor .NET. Volg onze stapsgewijze handleiding voor een naadloze PDF-export.
type: docs
weight: 10
url: /nl/net/3d-image-export/exporting-3d-images-to-pdf/
---
## Invoering

Wilt u 3D-afbeeldingen naadloos naar PDF exporteren met Aspose.CAD voor .NET? Deze stapsgewijze zelfstudie leidt u door het proces en zorgt ervoor dat u de kracht van Aspose.CAD kunt benutten om uw 3D-afbeeldingen moeiteloos naar PDF-formaat te converteren.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.CAD voor .NET: Zorg ervoor dat de Aspose.CAD-bibliotheek voor .NET is geïnstalleerd. Als dit niet het geval is, kunt u deze downloaden van de[Aspose.CAD voor .NET-downloadpagina](https://releases.aspose.com/cad/net/).

- Documentmap: stel een map in waarin uw CAD-bestanden worden opgeslagen en noteer het pad.

## Naamruimten importeren

Importeer in uw .NET-project de benodigde naamruimten voor het werken met Aspose.CAD. Voeg de volgende regels toe bovenaan uw codebestand:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Stap 1: Laad de CAD-afbeelding

 Begin met het laden van de CAD-afbeelding die u naar PDF wilt exporteren. Gebruik de`Load` methode uit de Aspose.CAD-bibliotheek. Vervangen`"conic_pyramid.dxf"` met het pad naar uw CAD-bestand.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Hier vindt u uw code voor het laden van de CAD-afbeelding
}
```

## Stap 2: Configureer rasterisatieopties

 Configureer de rasteropties voor de CAD-afbeelding. Stel parameters in zoals paginabreedte, paginahoogte en lay-outs. Verwijder het commentaar op de regel die verband houdt met`TypeOfEntities` als uw entiteiten 3D zijn.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## Stap 3: Stel PDF-opties in

Maak PDF-opties en koppel deze aan de rasteropties.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Stap 4: Opslaan als PDF

Sla de CAD-afbeelding op als PDF-bestand met behulp van de geconfigureerde opties. Geef het uitvoerpad voor het PDF-bestand op.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Conclusie

Gefeliciteerd! U hebt 3D-afbeeldingen met succes naar PDF geëxporteerd met Aspose.CAD voor .NET. Deze eenvoudige tutorial zorgt ervoor dat u uw CAD-bestanden moeiteloos naar een toegankelijker formaat converteert.

## Veelgestelde vragen

### V1: Is Aspose.CAD compatibel met alle CAD-bestandsformaten?

A1: Ja, Aspose.CAD ondersteunt een breed scala aan CAD-formaten, waardoor flexibiliteit bij het verwerken van verschillende bestandstypen wordt gegarandeerd.

### Vraag 2: Kan ik de paginaafmetingen aanpassen bij het exporteren naar PDF?

A2: Absoluut. De tutorial laat zien hoe u de paginabreedte en -hoogte kunt configureren volgens uw vereisten.

### V3: Zijn er tijdelijke licenties beschikbaar voor Aspose.CAD?

 A3: Ja, u kunt tijdelijke licenties voor Aspose.CAD verkrijgen door te bezoeken[Tijdelijke licentie](https://purchase.aspose.com/temporary-license/).

### V4: Waar kan ik aanvullende ondersteuning of communitydiscussies vinden?

 A4: Ga naar de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor ondersteuning en betrokkenheid bij de gemeenschap.

### V5: Is er een gratis proefversie van Aspose.CAD beschikbaar?

 A5: Ja, u kunt de functies van Aspose.CAD verkennen door naar het[gratis proefperiode](https://releases.aspose.com/).