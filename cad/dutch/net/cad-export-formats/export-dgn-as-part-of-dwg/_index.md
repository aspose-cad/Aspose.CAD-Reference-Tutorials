---
title: Exporteer DGN als onderdeel van DWG in Aspose.CAD voor .NET
linktitle: Exporteer DGN als onderdeel van DWG
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Leer hoe u DGN kunt exporteren als onderdeel van DWG in Aspose.CAD voor .NET. Volg onze stapsgewijze handleiding voor een naadloze integratie.
weight: 11
url: /nl/net/cad-export-formats/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporteer DGN als onderdeel van DWG in Aspose.CAD voor .NET

## Invoering

In de wereld van .NET-ontwikkeling onderscheidt Aspose.CAD zich als een krachtige bibliotheek voor het werken met Computer-Aided Design (CAD)-bestanden. Deze tutorial leidt u door het proces van het exporteren van een DGN-bestand (ontwerp) als onderdeel van een DWG-bestand (tekening) met behulp van Aspose.CAD voor .NET. Of u nu een doorgewinterde ontwikkelaar bent of net begint, deze stapsgewijze handleiding helpt u de mogelijkheden van Aspose.CAD te benutten om deze specifieke taak efficiënt uit te voeren.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.CAD voor .NET: Zorg ervoor dat de Aspose.CAD-bibliotheek voor .NET is geïnstalleerd. Je kunt het downloaden[hier](https://releases.aspose.com/cad/net/).

- Ontwikkelomgeving: Stel de .NET-ontwikkelomgeving van uw voorkeur in, zoals Visual Studio.

- Basiskennis van C#: Maak uzelf vertrouwd met de programmeertaal C#.

## Naamruimten importeren

Neem in uw C#-project de benodigde naamruimten op om toegang te krijgen tot de Aspose.CAD-functionaliteit. Voeg het volgende toe met behulp van richtlijnen aan het begin van uw codebestand:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Laten we nu de verstrekte code in meerdere stappen opsplitsen:

## Stap 1: Definieer bestandspaden

```csharp
//Invoer- en uitvoerbestandspaden
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Stap 2: Maak een PdfOptions-instantie

```csharp
// Maak een exemplaar van de klasse PdfOptions voor het exporteren van DWG naar PDF
PdfOptions exportOptions = new PdfOptions();
```

## Stap 3: Laad het DWG-bestand

```csharp
// Laad het bestaande DWG-bestand als afbeelding en converteer het naar het CadImage-type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Stap 4: Herhaal de entiteiten

```csharp
// Doorloop elke entiteit in het DWG-bestand
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Stap 5: Controleer het entiteitstype

```csharp
// Controleer of de entiteit een afbeeldingsdefinitie is
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Stap 6: Haal het onderlaagpad op

```csharp
// Als het een afbeeldingsdefinitie is, haal dan de externe verwijzing naar het object op
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Stap 7: Definieer rasterisatieopties

```csharp
// Definieer instellingen voor het CadRasterizationOptions-object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Stap 8: Exporteer DWG naar PDF

```csharp
// Exporteer de DWG naar PDF door de Save-methode aan te roepen
cadImage.Save(outPath, exportOptions);
```

## Conclusie

Gefeliciteerd! U hebt het proces van het exporteren van een DGN-bestand als onderdeel van een DWG-bestand met Aspose.CAD voor .NET met succes doorlopen. Deze tutorial heeft u de fundamentele stappen en codefragmenten gegeven om deze specifieke taak naadloos uit te voeren.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor .NET gebruiken in mijn commerciële projecten?
 A1: Ja, dat kan. Bezoek[hier](https://purchase.aspose.com/buy) om licentiemogelijkheden te verkennen.

### Vraag 2: Zijn er beperkingen op de grootte van de DWG-bestanden die ik kan verwerken?
A2: Aspose.CAD ondersteunt het verwerken van grote DWG-bestanden, maar er kunnen hardwarebeperkingen van toepassing zijn.

### Q3: Is er een proefversie beschikbaar?
A3: Ja, u kunt een gratis proefperiode krijgen[hier](https://releases.aspose.com/).

### Vraag 4: Hoe kan ik tijdelijke licenties krijgen?
 A4: Er kunnen tijdelijke licenties worden verkregen[hier](https://purchase.aspose.com/temporary-license/).

### Vraag 5: Waar kan ik hulp zoeken als ik problemen tegenkom?
 A5: U kunt het Aspose.CAD-forum bezoeken[hier](https://forum.aspose.com/c/cad/19) Voor ondersteuning.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
