---
title: Afbeeldingen importeren in DWG-bestanden met C# - Aspose.CAD-handleiding
linktitle: Afbeeldingen importeren in DWG-bestanden met C#
second_title: Aspose.CAD .NET - CAD- en BIM-bestandsindeling
description: Leer afbeeldingen importeren in DWG-bestanden met C# met Aspose.CAD voor .NET. Volg onze stapsgewijze handleiding voor een naadloze integratie.
type: docs
weight: 11
url: /nl/net/image-manipulation-and-rendering/importing-images-into-dwg/
---
## Invoering

Op het gebied van computerondersteund ontwerp (CAD) is het opnemen van afbeeldingen in DWG-bestanden een veel voorkomende en cruciale taak. Aspose.CAD voor .NET biedt een krachtige set tools om dit proces te stroomlijnen, waardoor het toegankelijk wordt voor C#-ontwikkelaars. In deze zelfstudie onderzoeken we stap voor stap hoe u afbeeldingen in DWG-bestanden kunt importeren.

## Vereisten

Voordat u in de gids duikt, moet u ervoor zorgen dat u over het volgende beschikt:

- Basiskennis van programmeren in C#.
-  Aspose.CAD voor .NET geïnstalleerd. Je kunt het downloaden[hier](https://releases.aspose.com/cad/net/).
- Een ontwikkelomgeving opgezet.

## Naamruimten importeren

Zorg ervoor dat u de benodigde naamruimten in uw C#-project opneemt:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Stap 1: Stel uw documentenmap in

```csharp
string MyDir = "Your Document Directory";
```

## Stap 2: Laad het DWG-bestand

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## Stap 3: Definieer de afbeeldingseigenschappen

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## Stap 4: Stel het invoegpunt en de vectoren in

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## Stap 5: Maak en configureer de rasterafbeelding

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## Stap 6: Afbeelding toevoegen aan DWG-bestand

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## Stap 7: Opslaan als PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Conclusie

Het integreren van afbeeldingen in DWG-bestanden met behulp van C# en Aspose.CAD voor .NET is een naadloos proces, waardoor ontwikkelaars hun CAD-projecten moeiteloos kunnen verbeteren met visuele elementen.

## Veelgestelde vragen

### V1: Kan ik Aspose.CAD voor .NET gebruiken met andere programmeertalen?

A1: Aspose.CAD is voornamelijk ontworpen voor .NET, maar Aspose biedt bibliotheken voor verschillende programmeertalen.

### V2: Is er een gratis proefversie beschikbaar voor Aspose.CAD voor .NET?

 A2: Ja, u kunt een gratis proefperiode uitproberen[hier](https://releases.aspose.com/).

### V3: Waar kan ik gedetailleerde documentatie voor Aspose.CAD vinden?

 A3: De documentatie is beschikbaar[hier](https://reference.aspose.com/cad/net/).

### V4: Hoe kan ik een tijdelijke licentie verkrijgen voor Aspose.CAD voor .NET?

 A4: Bezoek[deze link](https://purchase.aspose.com/temporary-license/) om een tijdelijke vergunning te verkrijgen.

### V5: Zijn er communityforums voor Aspose.CAD-ondersteuning?

 A5: Ja, u kunt steun zoeken en betrokken raken bij de gemeenschap[hier](https://forum.aspose.com/c/cad/19).