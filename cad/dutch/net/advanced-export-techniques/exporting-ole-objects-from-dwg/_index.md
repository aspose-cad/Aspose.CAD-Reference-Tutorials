---
title: OLE-objecten exporteren uit DWG-bestanden - Aspose.CAD-zelfstudie
linktitle: OLE-objecten exporteren uit DWG-bestanden
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Verken de stapsgewijze handleiding voor het exporteren van OLE-objecten uit DWG-bestanden met Aspose.CAD voor .NET. Verbeter moeiteloos uw vaardigheden op het gebied van CAD-bestandsmanipulatie.
weight: 12
url: /nl/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# OLE-objecten exporteren uit DWG-bestanden - Aspose.CAD-zelfstudie

## Invoering

Wilt u OLE-objecten eenvoudig uit DWG-bestanden extraheren? Aspose.CAD voor .NET is er om het proces voor u te stroomlijnen. In deze zelfstudie begeleiden we u stap voor stap bij het exporteren van OLE-objecten, zodat u optimaal gebruik kunt maken van deze krachtige .NET-bibliotheek. 

## Vereisten

Voordat we in de tutorial duiken, moet je ervoor zorgen dat je aan de volgende vereisten voldoet:

-  Aspose.CAD voor .NET Library: Zorg ervoor dat de bibliotheek is geïnstalleerd. Je kunt het downloaden van de[Aspose.CAD voor .NET-downloadpagina](https://releases.aspose.com/cad/net/).

-  Documentmap: stel een map in waarin uw DWG-bestanden worden opgeslagen. Vervangen`"Your Document Directory"` in het opgegeven codefragment met het daadwerkelijke pad.

## Naamruimten importeren

In uw .NET-project moet u de benodigde naamruimten importeren om de Aspose.CAD-functionaliteiten te kunnen benutten. Gebruik het volgende codefragment:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Stap 1: Stel de documentmap in

```csharp
string MyDir = "Your Document Directory";
```

 Vervangen`"Your Document Directory"` met het pad waar uw DWG-bestanden zich bevinden.

## Stap 2: Geef DWG-bestanden op

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Maak een lijst van de DWG-bestanden die u binnen de array wilt verwerken.

## Stap 3: Configureer exportopties

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Pas de exportopties aan op basis van uw vereisten. In dit voorbeeld configureren we de PNG-export met een opgegeven lay-out.

## Stap 4: Blader door bestanden en exporteer

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Blader door de opgegeven DWG-bestanden, laad ze allemaal en sla het geëxporteerde PNG-bestand op met de gedefinieerde opties.

## Conclusie

Gefeliciteerd! U hebt met succes OLE-objecten uit DWG-bestanden geëxporteerd met Aspose.CAD voor .NET. Deze krachtige bibliotheek vereenvoudigt complexe taken en biedt efficiëntie en flexibiliteit bij het manipuleren van CAD-bestanden.

## Veelgestelde vragen

### V1: Is Aspose.CAD voor .NET geschikt voor zowel junior als senior CAD-bestanden?

A1: Ja, Aspose.CAD voor .NET is veelzijdig en kan een breed scala aan CAD-bestanden verwerken, inclusief zowel junior- als seniorvarianten.

### Vraag 2: Kan ik de exportopties voor verschillende lay-outs aanpassen?

A2: Absoluut! Zoals u in de zelfstudie ziet, kunt u de exportopties, inclusief lay-outs, aanpassen aan uw specifieke behoeften.

### V3: Waar kan ik gedetailleerde documentatie vinden voor Aspose.CAD voor .NET?

 A3: Ontdek de[Aspose.CAD voor .NET-documentatie](https://reference.aspose.com/cad/net/) voor uitgebreide informatie en voorbeelden.

### Vraag 4: Is er een gratis proefversie beschikbaar?

 A4: Ja, u kunt de mogelijkheden van Aspose.CAD voor .NET ervaren met een gratis proefperiode. Bezoek[deze link](https://releases.aspose.com/) starten.

### Vraag 5: Hoe kan ik ondersteuning krijgen of contact maken met de community?

 A5: Bezoek voor ondersteuning en betrokkenheid van de gemeenschap de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
