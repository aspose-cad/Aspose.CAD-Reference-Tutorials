---
title: Werken met DWG-bestanden in C# - Verkrijg de grootte van de DWF-indeling
linktitle: Werken met DWG-bestanden in C# - Verkrijg de grootte van de DWF-indeling
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Ontdek de kracht van Aspose.CAD voor .NET bij het verwerken van DWG-bestanden. Leer moeiteloos DWF-lay-outformaten extraheren met C#.
type: docs
weight: 10
url: /nl/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## Invoering

Op het gebied van computerondersteund ontwerp (CAD) en .NET-ontwikkeling is Aspose.CAD een krachtig hulpmiddel voor het verwerken van DWG-bestanden. Deze tutorial leidt u door het proces van het werken met DWG-bestanden in C# en het extraheren van de grootte van een DWF-lay-out. Voordat we in de code duiken, moeten we ervoor zorgen dat je alles hebt ingesteld om aan deze reis te beginnen.

## Vereisten

Om deze tutorial naadloos te kunnen volgen, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.CAD voor .NET: Zorg ervoor dat Aspose.CAD voor .NET is geïnstalleerd. Je kunt het downloaden van de[Aspose.CAD voor .NET-downloadpagina](https://releases.aspose.com/cad/net/).

Nu u over de benodigde hulpmiddelen beschikt, gaan we de codeerarena betreden.

## Naamruimten importeren

Voordat we met de code gaan werken, importeren we de vereiste naamruimten:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Deze naamruimten bieden de essentiële klassen en methoden voor het verwerken van CAD-bestanden met Aspose.CAD in uw C#-toepassing.

## Stap 1: Stel uw omgeving in

Zorg er eerst voor dat u de juiste omgeving voor uw project heeft ingesteld. Verwijs naar de Aspose.CAD-bibliotheek in uw C#-project.

## Stap 2: Definieer bestandspaden

Definieer de paden voor uw DWG-bestand en de uitvoermap voor de gegenereerde JPG-bestanden:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Stap 3: Laad de DWF-afbeelding

Laad de DWF-afbeelding met Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code voor verdere stappen vindt u hier
}
```

## Stap 4: Blader door pagina's

Blader door de pagina's van de DWF-afbeelding:

```csharp
foreach (var page in image.Pages)
{
    // Code voor verdere stappen vindt u hier
}
```

## Stap 5: Ontvang lay-outinformatie

Ontvang lay-outinformatie van elke pagina:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Stap 6: JPG-opties instellen

Opties instellen voor het opslaan van de lay-out als JPG-bestand:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code voor verdere stappen vindt u hier
}
```

## Stap 7: Bepaal het paginaformaat

Bepaal de grootte van de DWF-lay-out:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code voor verdere stappen vindt u hier
```

## Stap 8: Paginaafmetingen instellen

Stel de paginaafmetingen in op basis van het eenheidstype:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Stap 9: Sla het JPG-bestand op

Sla het JPG-bestand op met de opgegeven opties:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Nu hebt u met succes de grootte van de DWF-lay-out uit het DWG-bestand geëxtraheerd met behulp van Aspose.CAD in C#. Ontdek gerust meer functies en functionaliteiten die Aspose.CAD biedt voor .NET-ontwikkeling.

## Conclusie

In deze zelfstudie hebben we het proces doorlopen van het werken met DWG-bestanden in C# met behulp van Aspose.CAD. Door deze stappen te volgen, krijgt u niet alleen de grootte van een DWF-lay-out, maar kunt u ook de mogelijkheden van Aspose.CAD benutten voor verschillende CAD-gerelateerde taken in uw .NET-projecten.

## Veelgestelde vragen

### V1: Is Aspose.CAD compatibel met de nieuwste DWG-bestandsindelingen?

 A1: Aspose.CAD ondersteunt verschillende DWG-bestandsformaten, inclusief de nieuwste versies. Verwijs naar de[documentatie](https://reference.aspose.com/cad/net/) voor specifieke compatibiliteitsdetails.

### V2: Kan ik Aspose.CAD gebruiken voor zowel commerciële als persoonlijke projecten?

 A2: Ja, Aspose.CAD biedt flexibele licentieopties voor zowel commercieel als persoonlijk gebruik. Bezoek de[aankooppagina](https://purchase.aspose.com/buy) voor meer details.

### V3: Hoe kan ik een tijdelijke licentie voor Aspose.CAD verkrijgen?

 A3: U kunt een tijdelijke licentie krijgen van[hier](https://purchase.aspose.com/temporary-license/) voor evaluatiedoeleinden.

### V4: Waar kan ik ondersteuning vinden voor Aspose.CAD?

A4: Ga voor vragen of hulp naar de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19).

### V5: Is er een gratis proefversie beschikbaar voor Aspose.CAD?

 A5: Ja, u heeft toegang tot een gratis proefversie van Aspose.CAD[hier](https://releases.aspose.com/).