---
title: Exporteer DGN naar PDF in Aspose.CAD voor .NET
linktitle: Exporteer DGN naar PDF
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Leer hoe u DGN-bestanden moeiteloos naar PDF kunt exporteren met Aspose.CAD voor .NET. Een stapsgewijze handleiding voor naadloze manipulatie van CAD-bestanden.
weight: 12
url: /nl/net/cad-export-formats/export-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporteer DGN naar PDF in Aspose.CAD voor .NET

## Invoering

In de wereld van .NET-ontwikkeling is Aspose.CAD een krachtige bibliotheek die de manipulatie en conversie van CAD-bestanden vergemakkelijkt. Een veel voorkomende taak die ontwikkelaars vaak tegenkomen is het exporteren van DGN-bestanden naar PDF-formaat. In deze zelfstudie doorlopen we het proces stap voor stap met behulp van Aspose.CAD voor .NET.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u over het volgende beschikt:

- Een praktische kennis van C# en het .NET-framework.
-  Aspose.CAD voor .NET-bibliotheek geïnstalleerd. Je kunt het downloaden[hier](https://releases.aspose.com/cad/net/).
- Een voorbeeld van een DGN-bestand, bijvoorbeeld "Nikon_D90_Camera.dgn" voor deze zelfstudie.

## Naamruimten importeren

Begin in uw C#-project met het importeren van de benodigde naamruimten:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Stap 1: Laad het DGN-bestand

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Jouw code hier...
}
```

## Stap 2: Configureer rasterisatieopties

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Stap 3: Maak PDF-opties

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Stap 4: Opslaan als PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Conclusie

Gefeliciteerd! U hebt met succes een DGN-bestand naar PDF geëxporteerd met Aspose.CAD voor .NET. In deze tutorial werden de essentiële stappen behandeld, van het laden van het DGN-bestand tot het configureren van rasteropties en het opslaan van de uitvoer als PDF.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor .NET gebruiken zonder voorafgaande CAD-kennis?

A1: Absoluut! Aspose.CAD vereenvoudigt complexe CAD-taken, waardoor het toegankelijk wordt voor ontwikkelaars met diverse achtergronden.

### V2: Waar kan ik meer voorbeelden en documentatie voor Aspose.CAD vinden?

 A2: Ontdek de[documentatie](https://reference.aspose.com/cad/net/) voor uitgebreide handleidingen en voorbeelden.

### V3: Is er een gratis proefversie beschikbaar voor Aspose.CAD?

A3: Ja, u kunt een gratis proefperiode krijgen[hier](https://releases.aspose.com/).

### V4: Hoe kan ik tijdelijke licenties krijgen voor Aspose.CAD?

 A4: Tijdelijke licenties verkrijgen[hier](https://purchase.aspose.com/temporary-license/).

### Q5: Hulp nodig of vragen?

A5: Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor gemeenschapssteun.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
