---
title: Eén PDF maken met verschillende lay-outs - Aspose.CAD-handleiding
linktitle: Eén PDF maken met verschillende lay-outs
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Maak één PDF met verschillende lay-outs met Aspose.CAD voor .NET. Volg onze stapsgewijze handleiding voor naadloze integratie en efficiënte PDF-generatie.
weight: 13
url: /nl/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Eén PDF maken met verschillende lay-outs - Aspose.CAD-handleiding

## Invoering

Wilt u één PDF-document genereren op basis van een CAD-tekening met verschillende lay-outs met behulp van Aspose.CAD voor .NET? Deze stapsgewijze handleiding leidt u door het proces en helpt u een naadloze integratie en efficiënte PDF-creatie te realiseren. Aspose.CAD voor .NET biedt krachtige functies om CAD-tekeningen programmatisch te manipuleren, en in deze tutorial zullen we ons concentreren op het maken van één PDF met verschillende lay-outs.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:

-  Aspose.CAD voor .NET: Zorg ervoor dat Aspose.CAD voor .NET is geïnstalleerd. Je kunt het downloaden van[hier](https://releases.aspose.com/cad/net/).

- Ontwikkelomgeving: Zet een .NET-ontwikkelomgeving op en heb een basiskennis van C#-programmeren.

## Naamruimten importeren

Neem in uw C#-project de benodigde naamruimten op om de functionaliteiten van Aspose.CAD voor .NET te benutten:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Stap 1: Laad de CAD-afbeelding

```csharp
// Het pad naar de documentenmap.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Uw code voor stap 1 komt hier terecht
}
```

## Stap 2: Rasterisatie-opties aanpassen

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Aangepaste formaten voor verschillende lay-outs
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Stap 3: PDF-opties definiëren

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## Stap 4: Opslaan als PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Nu hebt u met succes één PDF-document met verschillende lay-outs gemaakt met behulp van Aspose.CAD voor .NET. Ontdek gerust meer functies en pas de code aan volgens uw specifieke vereisten.

## Conclusie

In deze zelfstudie hebben we het proces besproken van het maken van één PDF van een CAD-tekening met verschillende lay-outs met behulp van Aspose.CAD voor .NET. Deze krachtige bibliotheek vereenvoudigt CAD-manipulatietaken en biedt flexibiliteit voor verschillende scenario's.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor .NET gebruiken met andere CAD-formaten?

A1: Ja, Aspose.CAD voor .NET ondersteunt verschillende CAD-formaten zoals DWG, DXF, DGN en meer.

### Vraag 2: Is er een gratis proefversie beschikbaar?

 A2: Ja, u kunt een gratis proefperiode uitproberen[hier](https://releases.aspose.com/).

### V3: Hoe kan ik ondersteuning krijgen voor Aspose.CAD voor .NET?

 A3: Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19) voor gemeenschapssteun.

### Vraag 4: Waar kan ik gedetailleerde documentatie vinden?

 A4: Raadpleeg de documentatie[hier](https://reference.aspose.com/cad/net/).

### V5: Kan ik een licentie kopen voor Aspose.CAD voor .NET?

 A5: Ja, u kunt een licentie kopen[hier](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
