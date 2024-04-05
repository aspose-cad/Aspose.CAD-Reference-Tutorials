---
title: Tekst toevoegen aan DWG-bestanden in C# - Aspose.CAD-zelfstudie
linktitle: Tekst toevoegen aan DWG-bestanden in C#
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Leer hoe u tekst aan DWG-bestanden kunt toevoegen met C# en Aspose.CAD. Volg deze stapsgewijze zelfstudie voor een naadloze integratie. Verken de Aspose.CAD-documentatie voor uitgebreide begeleiding.
type: docs
weight: 14
url: /nl/net/dwg-file-manipulation/adding-text-to-dwg/
---
## Invoering

In het dynamische domein van computerondersteund ontwerp (CAD) en .NET-ontwikkeling onderscheidt Aspose.CAD zich als een krachtig hulpmiddel voor het manipuleren van DWG-bestanden. Het toevoegen van tekst aan DWG-bestanden is een veel voorkomende vereiste, en in deze zelfstudie onderzoeken we hoe u dit kunt bereiken met C# en Aspose.CAD.

## Vereisten

Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u over het volgende beschikt:

-  Aspose.CAD-bibliotheek: Download en installeer de Aspose.CAD-bibliotheek van de[download link](https://releases.aspose.com/cad/net/).

-  Documentmap: Stel een map in voor uw documenten en noteer het pad ervan als`MyDir`.

Laten we het proces nu opsplitsen in beheersbare stappen.

## Naamruimten importeren

Neem in uw C#-code de benodigde naamruimten op om toegang te krijgen tot de Aspose.CAD-functionaliteiten.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Stap 1: Laad het DWG-bestand

 Laad het DWG-bestand in een`Image` object met behulp van de Aspose.CAD-bibliotheek.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Hier vindt u uw code voor de volgende stappen
}
```

## Stap 2: Maak een CadText-object

 Instantieer een`CadText` object dat de tekst weergeeft die u aan het DWG-bestand wilt toevoegen.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;
cadText.ScaleX = 0.0;
```

## Stap 3: tekst toevoegen aan DWG

 Voeg de gemaakte toe`CadText` bezwaar maken tegen het DWG-bestand met Aspose.CAD.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Stap 4: Configureer PDF-opties

Configureer PDF-opties om het gewijzigde DWG-bestand als PDF op te slaan.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Stap 5: Opslaan als PDF

Sla het gewijzigde DWG-bestand op als PDF met de toegevoegde tekst.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

Nu hebt u met succes tekst aan een DWG-bestand toegevoegd met C# en Aspose.CAD. Ontdek gerust meer functies en functionaliteiten van Aspose.CAD voor uw CAD-manipulatiebehoeften.

## Conclusie

In deze zelfstudie hebben we de essentiële stappen besproken voor het toevoegen van tekst aan DWG-bestanden met behulp van C# en Aspose.CAD. Deze krachtige combinatie opent mogelijkheden voor het dynamisch en op maat genereren van CAD-documenten.

## Veelgestelde vragen

### V1: Is Aspose.CAD compatibel met alle versies van DWG-bestanden?

A1: Aspose.CAD ondersteunt een breed scala aan DWG-bestandsversies, waardoor compatibiliteit met verschillende CAD-software wordt gegarandeerd.

### V2: Kan ik meerdere tekstentiteiten aan één DWG-bestand toevoegen met Aspose.CAD?

A2: Ja, u kunt meerdere tekstentiteiten aan een DWG-bestand toevoegen door het proces te herhalen dat in de zelfstudie wordt beschreven.

### V3: Hoe kan ik het lettertype en de tekststijl in Aspose.CAD wijzigen?

 A3: Om het lettertype en de tekststijl te wijzigen, past u de eigenschappen van het`CadText` object voordat u het aan het DWG-bestand toevoegt.

### V4: Zijn er licentieoverwegingen voor het gebruik van Aspose.CAD in een commercieel project?

 A4: Ja, zorg voor naleving van de licentievoorwaarden van Aspose.CAD. Verwijzen naar[Aspose.CAD-aankoop](https://purchase.aspose.com/buy) voor details.

### V5: Waar kan ik hulp zoeken of Aspose.CAD-gerelateerde vragen bespreken?

A5: Bezoek de[Aspose.CAD-forum](https://forum.aspose.com/c/cad/19)om verbinding te maken met de gemeenschap en steun te krijgen.