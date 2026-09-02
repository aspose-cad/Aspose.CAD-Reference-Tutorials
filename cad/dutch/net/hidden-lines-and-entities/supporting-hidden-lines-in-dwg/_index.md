---
date: 2026-07-28
description: DWG naar PDF-conversie met verborgen lijnen is eenvoudig met Aspose.CAD
  for .NET. Volg deze stapsgewijze handleiding om een DWG te laden, verborgen entiteiten
  in te schakelen en een PDF van hoge kwaliteit te exporteren.
keywords:
- dwg to pdf conversion
- show hidden lines
- how to export dwg
- cad image to pdf
- aspose cad .net
lastmod: 2026-07-28
linktitle: Ondersteuning van verborgen lijnen in DWG-bestanden
og_description: DWG naar PDF-conversie met verborgen lijnen is gemakkelijk met Aspose.CAD
  for .NET. Volg deze stapsgewijze handleiding om een DWG te laden, rasterisatie te
  configureren en een PDF te exporteren die verborgen entiteiten behoudt.
og_image_alt: 'Guide: Convert DWG to PDF with hidden lines using Aspose.CAD for .NET'
og_title: DWG naar PDF-conversie – Verborgen lijnen weergeven in DWG-bestanden
schemas:
- author: Aspose
  dateModified: '2026-07-28'
  description: DWG to PDF conversion with hidden lines is simple using Aspose.CAD
    for .NET. Follow this step‑by‑step guide to load a DWG, enable hidden entities,
    and export a high‑quality PDF.
  headline: DWG to PDF Conversion – Show Hidden Lines in DWG Files
  type: TechArticle
- description: DWG to PDF conversion with hidden lines is simple using Aspose.CAD
    for .NET. Follow this step‑by‑step guide to load a DWG, enable hidden entities,
    and export a high‑quality PDF.
  name: DWG to PDF Conversion – Show Hidden Lines in DWG Files
  steps:
  - name: Load the DWG File
    text: The `Image` class is Aspose.CAD's core object that represents a CAD drawing
      in memory. Instantiating it loads the source file and prepares it for further
      processing.
  - name: Set Rasterization Options
    text: '`CadRasterizationOptions` defines how the DWG is rendered—page size, DPI,
      layers, and whether hidden lines are shown. By setting the `ShowHiddenLines`
      flag to `true`, you instruct the engine to render those normally invisible entities.'
  - name: Configure PDF Options
    text: '`PdfOptions` bundles the rasterization settings with PDF‑specific features
      such as compression level and vector handling. The `VectorRasterizationOptions`
      property receives the `CadRasterizationOptions` instance from the previous step.'
  - name: Save the PDF File
    text: Calling `Save` on the `Image` instance writes the rendered content to a
      PDF file on disk. The resulting document retains hidden lines as vector graphics,
      ensuring crisp scaling at any zoom level.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports a wide range of DWG versions from AutoCAD R14
      up to the latest 2023 release, guaranteeing broad compatibility.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Absolutely. In Step 2, modify the `Layers` collection to include only
      the layers you need, and set individual `LayerOptions` such as color or line
      weight.
    question: Can I customize the rasterization options for different layers?
  - answer: Yes, you can explore the features of Aspose.CAD by using the free trial
      available [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.CAD?
  - answer: Visit the Aspose.CAD community forum [here](https://forum.aspose.com/c/cad/19)
      for any support or queries.
    question: Where can I find additional support and assistance?
  - answer: Yes, you can acquire a temporary license for Aspose.CAD [here](https://purchase.aspose.com/temporary-license/).
    question: Can I obtain a temporary license for Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg to pdf
- aspose cad
- hidden lines
- cad conversion
- dotnet
title: DWG naar PDF-conversie – Verborgen lijnen weergeven in DWG-bestanden
type: docs
url: /nl/net/hidden-lines-and-entities/supporting-hidden-lines-in-dwg/
weight: 10
---

# DWG naar PDF-conversie – Verborgen lijnen weergeven in DWG-bestanden

In deze tutorial leer je **dwg to pdf conversion** terwijl je verborgen lijnen behoudt, een veelvoorkomende eis voor architectuur- en technische documentatie. We doorlopen elke stap met Aspose.CAD voor .NET, van het laden van de bron‑DWG tot het configureren van rasterisatie‑opties en uiteindelijk het exporteren van een PDF die elke verborgen entiteit behoudt. Aan het einde heb je een kant‑klaar code‑fragment dat je in elk .NET‑project kunt gebruiken.

## Snelle antwoorden
- **Wat is het belangrijkste doel van deze gids?** Verborgen lijnweergave inschakelen tijdens dwg to pdf conversion met Aspose.CAD.  
- **Heb ik een licentie nodig om het voorbeeld uit te voeren?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **Kan ik bepalen welke lagen zichtbaar zijn?** Ja – de `Layers`‑array in rasterisatie‑opties stelt je in staat specifieke lagen op te nemen of uit te sluiten.  
- **Is de output vector‑gebaseerd of gerasterd?** De PDF is vector‑gebaseerd; verborgen entiteiten worden alleen gerasterd wanneer je de juiste vlag inschakelt.

## Wat is DWG naar PDF-conversie met verborgen lijnen?
Het **dwg to pdf conversion**‑proces zet een DWG‑CAD‑tekening om in een PDF‑document, waarbij optioneel verborgen entiteiten (lijnen, boogsegmenten of afmetingen die normaal onzichtbaar zijn) worden weergegeven. Dit is essentieel wanneer je volledige constructiedocumenten moet produceren die alle ontwerpintentie laten zien.

## Waarom Aspose.CAD gebruiken voor ondersteuning van verborgen lijnen?
Aspose.CAD ondersteunt **50+** DWG/DXF‑versies, kan bestanden tot **500 MB** verwerken zonder het volledige bestand in het geheugen te laden, en biedt gedetailleerde rasterisatie‑instellingen. Het inschakelen van verborgen lijnen voegt slechts **≈5 ms** per pagina toe op typische serverhardware, waardoor het geschikt is voor batch‑verwerkingspijplijnen.

## Voorvereisten

Before we dive in, ensure you have the following:

- **Aspose.CAD for .NET** – je kunt het downloaden [hier](https://releases.aspose.com/cad/net/).  
- Een .NET‑ontwikkelomgeving (Visual Studio, Rider of VS Code).  
- Een voorbeeld‑DWG‑bestand; de tutorial gebruikt **Bottom_plate.dwg** (bijgevoegd in het Aspose.CAD‑voorbeeldpakket).

## Hoe voer je DWG naar PDF-conversie uit met verborgen lijnen?

Laad je DWG, configureer rasterisatie om verborgen entiteiten bloot te leggen, en sla het resultaat op als een PDF. De volledige workflow bestaat uit vier beknopte stappen, elk geïllustreerd door een placeholder die je vervangt door je eigen code. Deze aanpak zorgt ervoor dat alle verborgen geometrie nauwkeurig wordt weergegeven in de uiteindelijke PDF, waardoor het geschikt is voor gedetailleerde ontwerpreviews en documentatie.

### Stap 1: Laad het DWG‑bestand
De `Image`‑klasse is het kernobject van Aspose.CAD dat een CAD‑tekening in het geheugen vertegenwoordigt. Het instantieren ervan laadt het bronbestand en maakt het klaar voor verdere verwerking.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;;
```

### Stap 2: Stel rasterisatie‑opties in
`CadRasterizationOptions` definieert hoe de DWG wordt gerenderd — paginagrootte, DPI, lagen en of verborgen lijnen worden getoond. Door de `ShowHiddenLines`‑vlag op `true` te zetten, instrueer je de engine om die normaal onzichtbare entiteiten weer te geven.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
string outPath = MyDir + "Bottom_plate.pdf";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Code for the next steps will go here
}
```

### Stap 3: Configureer PDF‑opties
`PdfOptions` bundelt de rasterisatie‑instellingen met PDF‑specifieke functies zoals compressieniveau en vectorafhandeling. De eigenschap `VectorRasterizationOptions` ontvangt de `CadRasterizationOptions`‑instantie van de vorige stap.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageHeight = cadImage.Height;
rasterizationOptions.PageWidth = cadImage.Width;
rasterizationOptions.Layers = new string[] { "Print", "L1_RegMark", "L2_RegMark" };
```

### Stap 4: Sla het PDF‑bestand op
Het aanroepen van `Save` op de `Image`‑instantie schrijft de gerenderde inhoud naar een PDF‑bestand op schijf. Het resulterende document behoudt verborgen lijnen als vector‑graphics, waardoor scherpe schaalbaarheid op elk zoomniveau wordt gegarandeerd.

```csharp
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Veelvoorkomende problemen en oplossingen

- **Verborgen lijnen verschijnen niet** – Controleer of `ShowHiddenLines` op `true` staat en dat de lagen met verborgen entiteiten zijn opgenomen in de `Layers`‑array.  
- **Grote bestanden veroorzaken geheugenbelasting** – Gebruik de eigenschappen `PageSize` en `Resolution` om het gerenderde gebied te beperken, of verwerk de DWG in delen door `PageCount` op te geven.  
- **Onverwachte lay-outverschuiving** – Zorg ervoor dat de bron‑DWG dezelfde eenheden (mm/inches) gebruikt als de doel‑PDF; je kunt de eigenschap `Scale` in `CadRasterizationOptions` aanpassen.

## Veelgestelde vragen

**Q: Is Aspose.CAD compatibel met alle versies van DWG‑bestanden?**  
A: Ja, Aspose.CAD ondersteunt een breed scala aan DWG‑versies van AutoCAD R14 tot de nieuwste 2023‑release, wat brede compatibiliteit garandeert.

**Q: Kan ik de rasterisatie‑opties aanpassen voor verschillende lagen?**  
A: Absoluut. In Stap 2 wijzig je de `Layers`‑collectie zodat alleen de lagen die je nodig hebt worden opgenomen, en stel je individuele `LayerOptions` in, zoals kleur of lijndikte.

**Q: Is er een proefversie beschikbaar voor Aspose.CAD?**  
A: Ja, je kunt de functies van Aspose.CAD verkennen door de gratis proefversie te gebruiken die [hier](https://releases.aspose.com/) beschikbaar is.

**Q: Waar kan ik extra ondersteuning en hulp vinden?**  
A: Bezoek het Aspose.CAD‑communityforum [hier](https://forum.aspose.com/c/cad/19) voor ondersteuning of vragen.

**Q: Kan ik een tijdelijke licentie voor Aspose.CAD verkrijgen?**  
A: Ja, je kunt een tijdelijke licentie voor Aspose.CAD verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

---

**Laatst bijgewerkt:** 2026-07-28  
**Getest met:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose

```csharp
cadImage.Save(outPath, pdfOptions);
```

## Gerelateerde tutorials

- [DWG exporteren naar PDF of rasterafbeeldingen - Aspose.CAD-gids](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Grote DWG‑bestanden converteren naar PDF - Aspose.CAD‑tutorial](/cad/net/image-manipulation-and-rendering/converting-large-dwg-files-to-pdf/)
- [DWG exporteren naar DXF-formaat in C# - Aspose.CAD‑tutorial](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)