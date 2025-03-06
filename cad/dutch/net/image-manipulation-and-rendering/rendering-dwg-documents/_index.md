---
title: DWG-documenten renderen in C# - Aspose.CAD-handleiding
linktitle: DWG-documenten renderen in C#
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Leer hoe u DWG-documenten in C# kunt renderen met Aspose.CAD. Deze stapsgewijze handleiding behandelt het importeren, configureren en opslaan met codevoorbeelden.
weight: 17
url: /nl/net/image-manipulation-and-rendering/rendering-dwg-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG-documenten renderen in C# - Aspose.CAD-handleiding

## Invoering

Welkom bij de uitgebreide handleiding over het renderen van DWG-documenten in C# met behulp van Aspose.CAD. Of u nu een doorgewinterde ontwikkelaar bent of net begint met .NET, deze tutorial begeleidt u bij het gebruik van Aspose.CAD om DWG-bestanden efficiënt weer te geven. Aspose.CAD is een krachtige API die robuuste functionaliteiten biedt voor het werken met CAD-bestandsformaten, waardoor het een favoriete keuze is voor ontwikkelaars die met DWG-bestanden werken.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

- Basiskennis van de programmeertaal C#.
- Visual Studio is op uw computer geïnstalleerd.
-  Aspose.CAD-bibliotheek geïntegreerd in uw project. Je kunt het downloaden van[hier](https://releases.aspose.com/cad/net/).
- Een voorbeeld van een DWG-bestand, zoals 'Bottom_plate.dwg', om samen met de voorbeelden te volgen.

## Naamruimten importeren

Zorg ervoor dat u aan het begin van uw C#-code de benodigde naamruimten importeert om aan de slag te gaan:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Laten we het gegeven voorbeeld nu in meerdere stappen opsplitsen:

## Stap 1: Laad het DWG-bestand

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Hier vindt u uw code voor het laden van het DWG-bestand.
}
```

## Stap 2: Configureer rasterisatieopties

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//Hier kunnen aanvullende rasterconfiguraties worden toegevoegd.
```

## Stap 3: Definieer de regio die u wilt tekenen

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Stap 4: Maak een nieuwe viewport

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Stap 5: Vervang Actieve Viewport

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Stap 6: Configureer PDF-opties

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Stap 7: Sla de gerenderde DWG op als PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Conclusie

Gefeliciteerd! U hebt met succes een DWG-document naar PDF weergegeven met Aspose.CAD in C#. Ontdek gerust meer functies en pas de code aan op basis van uw specifieke vereisten.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD gebruiken met andere CAD-bestandsindelingen?

A1: Ja, Aspose.CAD ondersteunt verschillende CAD-formaten, waaronder DWG, DXF, DWF en meer.

### V2: Is Aspose.CAD compatibel met .NET Core?

A2: Ja, Aspose.CAD is compatibel met zowel .NET Framework als .NET Core.

### Vraag 3: Hoe kan ik omgaan met verschillende lay-outs in een DWG-bestand?

 A3: U kunt de gewenste indeling opgeven in het`Layouts` eigendom van`CadRasterizationOptions`.

### V4: Zijn er licentieoverwegingen voor het gebruik van Aspose.CAD?

 A4: Ga voor licentiegegevens naar[hier](https://purchase.aspose.com/buy).

### Vraag 5: Waar kan ik aanvullende ondersteuning vinden?

A5: Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor gemeenschapsondersteuning en discussies.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
