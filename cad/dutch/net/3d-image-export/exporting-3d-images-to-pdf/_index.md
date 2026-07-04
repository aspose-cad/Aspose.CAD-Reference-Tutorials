---
date: 2026-07-04
description: Leer hoe u het PDF-paginaformaat instelt en PDF exporteert vanuit 3D
  CAD-afbeeldingen met Aspose.CAD voor .NET – een stapsgewijze handleiding om DWG
  naar PDF te converteren en CAD op te slaan als PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: 3D-afbeeldingen exporteren naar PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: PDF-paginaformaat instellen – 3D-afbeeldingen exporteren naar PDF met Aspose.CAD
url: /nl/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporteren van 3D-afbeeldingen naar PDF - Aspose.CAD Tutorial

## Inleiding

Als u de **PDF-paginaformaat moet instellen** tijdens het converteren van een 3‑D CAD-tekening naar PDF, bent u hier aan het juiste adres. Deze tutorial laat u stap voor stap zien hoe u een CAD‑bestand laadt, rasterisatie‑opties configureert — inclusief aangepaste paginadimensies — en een PDF van hoge kwaliteit genereert met Aspose.CAD voor .NET. Aan het einde kunt u **PDF exporteren vanuit CAD**, **CAD opslaan als PDF**, en elk lay‑outdetail beheren zonder AutoCAD te installeren.

## Snelle antwoorden
- **Wat betekent “PDF exporteren vanuit CAD”?** Het converteert een CAD‑tekening (DWG, DXF, DGN, enz.) naar een PDF die op elk apparaat geopend kan worden.  
- **Welke bibliotheek voert de conversie uit?** Aspose.CAD voor .NET biedt rasterisatie en PDF-export zonder externe afhankelijkheden.  
- **Heb ik een licentie nodig?** Voor productie is een tijdelijke of volledige licentie vereist; een gratis proefversie is beschikbaar.  
- **Kan ik aangepaste paginadimensies instellen?** Ja—gebruik `PageWidth` en `PageHeight` in `RasterizationOptions`.  
- **Wordt 3‑D geometrie behouden?** De 3‑D entiteiten worden gerasterd; schakel `TypeOfEntities.Entities3D` in voor volledige 3‑D-ondersteuning.

## Wat betekent “export PDF” in de context van CAD?

PDF exporteren vanuit CAD betekent dat u een CAD‑tekening (DWG, DXF, DGN, enz.) neemt en deze converteert naar een PDF‑bestand dat vectorafbeeldingen, gerasterde 3‑D‑weergaven en nauwkeurige paginalay‑outinformatie kan bevatten, waardoor het eenvoudig te delen is met iedereen die geen CAD‑software heeft.

## Waarom Aspose.CAD gebruiken om PDF te exporteren?

Aspose.CAD stelt u in staat om **PDF-paginaformaat in te stellen** en PDF's volledig in beheerde .NET-code te exporteren. Het ondersteunt meer dan 50 CAD-formaten, verwerkt bestanden tot 2 GB zonder het volledige document in het geheugen te laden, en behoudt lijndiktes, kleuren en optionele 3‑D‑entiteitweergave met een rasterisatie‑DPI tot 1200. De bibliotheek draait op Windows, Linux en macOS, zodat de gegenereerde PDF's op elk platform werken.

## Vereisten

- **Aspose.CAD for .NET** geïnstalleerd. Download het van de [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Een map die de CAD‑bestanden bevat die u wilt converteren (bijv. `C:\CAD\`).  
- .NET 6.0 of later (of .NET Framework 4.7.2).  

## Namespaces importeren

`using`-statements importeren de Aspose.CAD‑namespaces die nodig zijn om met rasterisatie‑ en PDF‑opties te werken.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Stapsgewijze handleiding

### Hoe PDF-paginaformaat instellen bij het exporteren van CAD naar PDF?

Laad uw CAD‑bestand, configureer de paginadimensies in `RasterizationOptions`, koppel die opties aan een `PdfOptions`‑instantie, en roep `Save` aan. Deze vier‑stappen‑stroom geeft u volledige controle over de uitvoergrootte en kwaliteit, terwijl de code beknopt blijft.

### Stap 1: Laad de CAD‑afbeelding

`Image`-klasse vertegenwoordigt een CAD‑tekening die in het geheugen is geladen, klaar voor rasterisatie.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Stap 2: Rasterisatie‑opties configureren (CAD opslaan als PDF)

`RasterizationOptions`-klasse definieert hoe de CAD‑gegevens worden gerasterd, inclusief paginagrootte, DPI en of 3‑D‑entiteiten worden weergegeven.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Stap 3: PDF‑opties instellen (PDF maken vanuit CAD)

`PdfOptions`-klasse bevat de instellingen voor het uitvoerformaat en koppelt de rasterisatie‑opties aan de PDF‑generatie.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Stap 4: Opslaan als PDF (PDF genereren vanuit 3D‑model)

`Save`-methode op het `Image`‑object schrijft de gerasterde inhoud naar het opgegeven PDF‑bestand, waardoor een kant‑en‑klaar‑deelbaar document ontstaat.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Reden | Oplossing |
|----------|-------|-----------|
| **Uitvoer-PDF is leeg** | Verkeerde lay-outnaam of ontbrekende `Model`-lay-out. | Controleer of `rasterizationOptions.Layouts` overeenkomt met een lay-out die aanwezig is in het CAD‑bestand. |
| **Lage resolutie** | Standaard rasterisatie‑DPI is laag. | Stel `rasterizationOptions.Resolution = 300;` in vóór het opslaan. |
| **3‑D entiteiten niet weergegeven** | `TypeOfEntities` is uitgecommentarieerd. | Verwijder de commentaartekens bij `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **Licentie‑fout** | Een proefversie gebruiken zonder licentie. | Pas een tijdelijke of permanente licentie toe via `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Veelgestelde vragen

**Q: Is Aspose.CAD compatibel met alle CAD‑bestandsformaten?**  
A: Ja, Aspose.CAD ondersteunt meer dan 50 invoer‑ en uitvoerformaten, waaronder DWG, DXF, DGN, STL en IFC, wat flexibiliteit voor elk project garandeert.

**Q: Kan ik de paginadimensies aanpassen bij het exporteren naar PDF?**  
A: Absoluut. Stel `PageWidth` en `PageHeight` in `RasterizationOptions` in op elke gewenste grootte in punten, inches of millimetres vóór het aanroepen van `Save`.

**Q: Zijn tijdelijke licenties beschikbaar voor Aspose.CAD?**  
A: Ja, u kunt tijdelijke licenties voor Aspose.CAD verkrijgen door naar [Temporary License](https://purchase.aspose.com/temporary-license/) te gaan.

**Q: Waar kan ik extra ondersteuning of community‑discussies vinden?**  
A: Ga naar het [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) voor deskundige hulp en peer‑to‑peer advies.

**Q: Is er een gratis proefversie van Aspose.CAD?**  
A: Ja, u kunt de functies van Aspose.CAD verkennen door de [free trial](https://releases.aspose.com/) te openen.

## Conclusie

U heeft nu een volledige, productie‑klare methode om **PDF-paginaformaat in te stellen** en **PDF te exporteren vanuit 3D CAD‑afbeeldingen** met Aspose.CAD voor .NET. Door rasterisatie‑opties aan te passen kunt u de resolutie, paginalay‑out en 3‑D‑entiteitweergave fijn afstemmen om aan elke documentatie‑vereiste te voldoen. Experimenteer met verschillende DPI‑instellingen en paginadimensies om de perfecte balans tussen bestandsgrootte en visuele getrouwheid te bereiken.

{{< blocks/products/products-backtop-button >}}

## Gerelateerde tutorials

- [Specifieke lay-outs exporteren naar PDF - Aspose.CAD-gids](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [DWG exporteren naar PDF of rasterafbeeldingen - Aspose.CAD-gids](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [DGN exporteren naar PDF in Aspose.CAD voor .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Laatst bijgewerkt:** 2026-07-04  
**Getest met:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose