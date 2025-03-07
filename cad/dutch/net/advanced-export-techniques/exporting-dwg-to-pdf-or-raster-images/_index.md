---
title: DWG exporteren naar PDF of rasterafbeeldingen - Aspose.CAD-handleiding
linktitle: DWG exporteren naar PDF of rasterafbeeldingen
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Ontdek een uitgebreide handleiding over het exporteren van DWG naar PDF of rasterafbeeldingen met Aspose.CAD voor .NET. Leer de stappen en vereisten en ga aan de slag met deze krachtige bibliotheek.
weight: 11
url: /nl/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG exporteren naar PDF of rasterafbeeldingen - Aspose.CAD-handleiding

## Invoering

Wilt u DWG-bestanden naadloos converteren naar PDF of rasterafbeeldingen in uw .NET-toepassing? Zoek niet verder! Deze stapsgewijze handleiding leidt u door het proces met behulp van de krachtige Aspose.CAD voor .NET-bibliotheek. Of je nu een doorgewinterde ontwikkelaar bent of net begint, deze tutorial is geschikt voor alle vaardigheidsniveaus.

## Vereisten

Voordat we ingaan op de tutorial, zorg ervoor dat je over het volgende beschikt:

- Een basiskennis van .NET-programmering.
-  Aspose.CAD voor .NET-bibliotheek geïnstalleerd. Zo niet, download het dan[hier](https://releases.aspose.com/cad/net/).
- Uw favoriete geïntegreerde ontwikkelomgeving (IDE), opgezet voor .NET-ontwikkeling.

## Naamruimten importeren

Laten we beginnen met het importeren van de benodigde naamruimten in uw .NET-project. Dit zorgt ervoor dat u toegang heeft tot de Aspose.CAD-functionaliteit in uw code.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Stap 1: Laad het DWG-bestand

Begin met het laden van het DWG-bestand dat u wilt converteren. Vervang "Uw documentenmap" door het pad naar uw DWG-bestand.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Uw code voor het laden van DWG komt hier terecht
}
```

## Stap 2: Stel PDF-export in

Laten we nu de PDF-exportinstellingen configureren. Dit voorbeeld laat zien hoe u de lay-out instelt en eenheidsconversies afhandelt.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Controleer en definieer het eenhedensysteem
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Hier vindt u uw code voor het instellen van PDF-export
```

## Stap 3: Exporteren naar PDF

Voer de export naar PDF uit met behulp van de geconfigureerde instellingen.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Stap 4: Exporteren naar rasterafbeeldingen

Breid de functionaliteit uit om te exporteren naar rasterafbeeldingen, zoals PNG.

```csharp
// A4-formaat bij 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Conclusie

Gefeliciteerd! U hebt met succes geleerd hoe u Aspose.CAD voor .NET kunt gebruiken om DWG-bestanden naar zowel PDF- als rasterafbeeldingen te exporteren. Deze krachtige bibliotheek stroomlijnt het proces, waardoor het efficiënt en ontwikkelaarsvriendelijk wordt.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor .NET gebruiken in mijn commerciële projecten?

 A1: Ja, dat kan. Bezoek[aankoop.aspose.com/kopen](https://purchase.aspose.com/buy) voor licentiegegevens.

### Vraag 2: Is er een gratis proefversie beschikbaar?

 A2: Zeker! Pak uw gratis proefperiode[hier](https://releases.aspose.com/).

### V3: Hoe kan ik ondersteuning krijgen voor Aspose.CAD voor .NET?

 A3: Ga naar de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor gemeenschapssteun.

### V4: Kan ik een tijdelijke licentie verkrijgen voor testdoeleinden?

 A4: Ja, u kunt een tijdelijke licentie krijgen[hier](https://purchase.aspose.com/temporary-license/).

### Vraag 5: Waar kan ik de gedetailleerde documentatie vinden?

 A5: De documentatie is beschikbaar op[Aspose.CAD](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
