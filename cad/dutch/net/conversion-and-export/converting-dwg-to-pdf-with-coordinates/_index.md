---
title: DWG naar PDF converteren met coördinaten in C# - Aspose.CAD Tutorial
linktitle: DWG naar PDF converteren met coördinaten in C#
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Leer hoe u DWG naar PDF kunt converteren met specifieke coördinaten in C# met behulp van Aspose.CAD. Volg onze stapsgewijze handleiding voor nauwkeurige en efficiënte CAD-bestandsconversies.
weight: 11
url: /nl/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG naar PDF converteren met coördinaten in C# - Aspose.CAD Tutorial

## Invoering

Welkom bij deze uitgebreide tutorial over het converteren van DWG-bestanden naar PDF met gespecificeerde coördinaten met behulp van Aspose.CAD voor .NET. Aspose.CAD is een krachtige bibliotheek waarmee ontwikkelaars naadloos met CAD-bestandsindelingen in hun .NET-applicaties kunnen werken. In deze zelfstudie leiden we u door het proces van het converteren van een DWG-bestand naar PDF, waarbij we specifieke coördinaten opgeven om de precisie te verbeteren.

## Vereisten

Voordat we beginnen, zorg ervoor dat u aan de volgende vereisten voldoet:

- Aspose.CAD-bibliotheek: Download en installeer de Aspose.CAD-bibliotheek voor .NET. Je kunt de bibliotheek vinden[hier](https://releases.aspose.com/cad/net/).

- Ontwikkelomgeving: Zorg ervoor dat u een compatibele ontwikkelomgeving hebt ingesteld, inclusief Visual Studio of een andere gewenste IDE.

- DWG-bestand: Zorg ervoor dat u een DWG-bestand gereed heeft voor conversie. U kunt het meegeleverde voorbeeldbestand of uw aangepaste DWG-bestand gebruiken.

## Naamruimten importeren

Importeer in uw C#-project de benodigde naamruimten:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Laten we de code opsplitsen in een stapsgewijze handleiding voor een beter begrip:

## Stap 1: Definieer de documentmap

```csharp
string MyDir = "Your Document Directory";
```

## Stap 2: Stel het bron-DWG-bestandspad in

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Stap 3: Laad het DWG-bestand en configureer de rasterisatie-opties

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Stap 4: Definieer coördinaten en viewport

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Stap 5: Pas Viewport-instellingen toe

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Stap 6: PDF-opties configureren en exporteren

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Stap 7: Succesbericht weergeven

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusie

Gefeliciteerd! U hebt met succes een DWG-bestand naar PDF geconverteerd met opgegeven coördinaten met behulp van Aspose.CAD voor .NET. Deze tutorial behandelde essentiële stappen en bood een duidelijke handleiding voor ontwikkelaars.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD gebruiken met andere CAD-bestandsindelingen?

A1: Ja, Aspose.CAD ondersteunt verschillende CAD-formaten, waaronder DWG, DXF, DWF en meer.

### Vraag 2: Hoe kan ik omgaan met fouten tijdens het conversieproces?

A2: Implementeer mechanismen voor foutafhandeling met behulp van try-catch-blokken om uitzonderingen vast te leggen en te beheren.

### V3: Is Aspose.CAD geschikt voor zowel Windows- als Linux-omgevingen?

A3: Ja, Aspose.CAD is compatibel met zowel Windows- als Linux-platforms.

### Vraag 4: Kan ik de PDF-uitvoer verder aanpassen?

A4: Zeker! Ontdek de uitgebreide mogelijkheden van Aspose.CAD om de PDF-uitvoer aan uw specifieke vereisten aan te passen.

### Vraag 5: Waar kan ik aanvullende ondersteuning of communitydiscussies vinden?

A5: Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor gemeenschapsondersteuning en discussies.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
