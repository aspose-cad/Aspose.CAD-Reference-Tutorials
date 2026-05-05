---
date: 2026-03-21
description: Apprenez à créer un PDF à partir de DWG et à exporter le DGN dans le
  DWG à l'aide d'Aspose.CAD pour .NET. Ce guide montre également comment convertir
  un DWG en PDF et définir les options PDF.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Créer un PDF à partir de DWG et exporter DGN comme partie de DWG – Aspose.CAD
  pour .NET
url: /fr/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer un PDF à partir de DWG et exporter DGN dans le cadre du DWG – Aspose.CAD pour .NET

## Introduction

Si vous devez **créer un PDF à partir de fichiers DWG** tout en incorporant un design DGN dans le DWG, Aspose.CAD pour .NET rend cela simple. Dans ce tutoriel, nous parcourrons l’ensemble du flux de travail : charger un DWG, localiser le sous‑couche DGN incorporée, configurer les options de rastérisation, puis exporter le résultat dans un document PDF. Que vous construisiez un outil de conversion par lots, un moteur de génération de rapports ou un service d’intégration CAD‑BIM, les étapes ci‑dessous vous fourniront une base solide et prête pour la production.

## Quick Answers
- **What library handles DWG → PDF conversion?** Aspose.CAD for .NET  
- **Can I export a DGN underlay while creating the PDF?** Yes – the underlay is accessed via `CadDgnUnderlay`.  
- **Which method sets PDF options?** `PdfOptions` together with `CadRasterizationOptions`.  
- **Do I need a license for commercial use?** Yes, a valid Aspose.CAD license is required.  
- **Supported .NET versions?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## What is “create PDF from DWG”?

Créer un PDF à partir d’un fichier DWG signifie rendre le dessin vectoriel sous forme de document PDF raster ou vectoriel. Ce processus est utile pour partager des dessins avec des parties prenantes qui n’ont pas de logiciel CAD, pour l’archivage ou la génération de rapports imprimables. Aspose.CAD simplifie la tâche en prenant en charge l’analyse des entités DWG et en offrant un contrôle fin sur la sortie via `PdfOptions`.

## Why export DGN as part of a DWG?

Une sous‑couche DGN représente souvent une géométrie de référence provenant de projets MicroStation. En exportant le DGN avec le DWG, vous conservez le contexte de conception original, garantissant que les consommateurs en aval voient l’ensemble complet du jeu de dessins. Cela est particulièrement précieux dans les projets multidisciplinaires où les fichiers DWG et DGN coexistent.

## Prerequisites

- **Aspose.CAD for .NET** – download it [here](https://releases.aspose.com/cad/net/).  
- **Development Environment** – Visual Studio (any recent version) or your preferred .NET IDE.  
- **Basic C# knowledge** – you should be comfortable with C# syntax and .NET project structure.

## Import Namespaces

Add the required `using` directives at the top of your C# source file:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Step‑by‑Step Guide

### Step 1: Define File Paths

Set the input DWG file and the output PDF name.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Step 2: Create `PdfOptions` Instance (set pdf options)

`PdfOptions` lets you control how the PDF is generated, such as page size, compression, and metadata.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Step 3: Load the DWG File

Load the DWG as a `CadImage` so you can inspect its entities.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Step 4: Iterate Through Entities

Walk through every entity in the drawing to locate the DGN underlay.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Step 5: Check Entity Type (how to export dgn)

Identify whether the current entity is a DGN underlay.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Step 6: Get Underlay Path

Retrieve the external reference path of the DGN file.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Step 7: Define Rasterization Options (convert dwg to pdf)

Configure how the DWG is rasterized before being placed into the PDF.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Step 8: Export DWG to PDF

Finally, save the rendered image as a PDF file.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Common Issues and Solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| **`Image.Load` throws “File not found”** | Chemin incorrect ou fichier manquant. | Utilisez un chemin absolu ou assurez‑vous que le DWG est copié dans le dossier de sortie. |
| **Underlay path is empty** | DGN underlay not embedded or reference broken. | Verify the DWG actually contains a DGN underlay and that the external DGN file is accessible. |
| **PDF output is blank** | Rasterization options set to zero size. | Adjust `PageWidth`/`PageHeight` or set `NoScaling = false`. |
| **License exception** | Running without a valid Aspose.CAD license. | Apply the license before loading the image: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for .NET in my commercial projects?
**R1:** Yes, you can. Visit [here](https://purchase.aspose.com/buy) to explore licensing options.

### Q2: Are there any limitations on the size of DWG files I can process?
**R2:** Aspose.CAD supports handling large DWG files, but hardware limitations may apply.

### Q3: Is there a trial version available?
**R3:** Yes, you can get a free trial [here](https://releases.aspose.com/).

### Q4: How can I get temporary licenses?
**R4:** Temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).

### Q5: Where can I seek assistance if I encounter issues?
**R5:** You can visit the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19) for support.

**Q: How do I set additional PDF metadata (author, title, etc.)?**  
**R:** Use `exportOptions.Metadata` properties before calling `Save`.

**Q: Can I export multiple layouts into separate PDF pages?**  
**R:** Yes – set `Layouts = new string[] { "Layout1", "Layout2" }` in `CadRasterizationOptions`.

**Q: Does Aspose.CAD support converting DWG to other image formats?**  
**R:** Absolutely. You can export to PNG, JPEG, SVG, and more by using the corresponding `Image.Save` overloads.

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}