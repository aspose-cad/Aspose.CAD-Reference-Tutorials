---
date: 2026-04-06
description: Apprenez à convertir DWF en JPG en C# à l'aide d'Aspose.CAD et découvrez
  comment extraire la taille de la mise en page DWF à partir de fichiers DWG.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: Travailler avec les fichiers DWG en C# – Obtenir la taille de la mise en
  page DWF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Convertir DWF en JPG en C# – Obtenir la taille de la mise en page DWF à partir
  de DWG
url: /fr/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWF en JPG en C# – Obtenir la taille de la mise en page DWF à partir de DWG

## Introduction

If you need to **convert DWF to JPG** while also figuring out the exact layout dimensions, you’re in the right place. In this tutorial we’ll walk through a complete, end‑to‑end example that uses Aspose.CAD for .NET to open a DWG‑derived DWF file, read each layout’s size, and save the layout as a high‑quality JPG image. By the end you’ll not only know how to extract DWF layout information but also have a reusable code snippet you can drop into any C# project.

## Réponses rapides
- **What does “convert DWF to JPG” mean?** It means rasterizing a vector DWF layout into a bitmap JPEG image.  
- **Why read layout size first?** Knowing the exact extents lets you set the correct page dimensions, avoiding stretched or clipped output.  
- **Which library handles this?** Aspose.CAD for .NET provides full support for DWG, DWF and raster image conversion.  
- **Do I need a license?** A temporary license works for evaluation; a full license is required for production.  
- **What .NET versions are supported?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Qu’est‑ce que “convertir DWF en JPG” et pourquoi est‑ce important ?

Converting a DWF (Design Web Format) file to JPG creates a portable image that can be displayed in browsers, embedded in reports, or shared with stakeholders who don’t have CAD software. The conversion also gives you the flexibility to manipulate the image (resize, compress, watermark) using standard image‑processing tools.

## Pourquoi extraire la taille de la mise en page DWF ?

A DWF file can contain multiple layouts, each with its own coordinate system and units (inches, millimeters, etc.). Extracting the layout size lets you:

1. Preserve the original aspect ratio when rasterizing.  
2. Choose the correct DPI for high‑resolution output.  
3. Automate batch processing of many layouts without manual tweaking.

## Prérequis

To follow this tutorial seamlessly, make sure you have the following prerequisites in place:

- Aspose.CAD for .NET: Ensure that you have Aspose.CAD for .NET installed. You can download it from the [page de téléchargement d'Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).

Having the library ready means you can focus on the code rather than hunting down dependencies.

## Importer les espaces de noms

Before we start coding, import the required namespaces. These provide the classes we’ll need to work with CAD files, rasterization options, and file I/O.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Étape 1 : Configurer votre environnement

Create a new C# console or class‑library project, add a reference to the **Aspose.CAD.dll**, and ensure the project targets a compatible .NET version.

## Étape 2 : Définir les chemins de fichiers (comment extraire le DWF)

Specify where your source DWF file lives and where the generated JPG files should be written.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Pro tip:** Use `Path.Combine(MyDir, "blocks_and_tables.dwf")` for safer path handling on different OSes.

## Étape 3 : Charger l’image DWF

Load the DWF file into an `Aspose.CAD.Image` object. We cast it to `DwfImage` because we need access to page‑specific properties.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Étape 4 : Parcourir les pages

A DWF can contain several pages (layouts). Loop through each one so we can process them individually.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Étape 5 : Obtenir les informations de mise en page

Inside the loop, retrieve the layout name. This name will be used both for logging and for naming the output JPG file.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Étape 6 : Configurer les options JPG

Create a `JpegOptions` instance and configure rasterization options. The `Layouts` property tells Aspose.CAD which layout to render.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Étape 7 : Déterminer la taille de la page (convertir dwg en jpg)

Calculate the width and height of the layout in its native units. This information is essential for setting the raster page size correctly.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Étape 8 : Configurer les dimensions de la page

Convert the native units (inch or millimeter) to pixels using the helper methods provided by Aspose.CAD. If the unit type is neither, we fall back to using the raw values.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Étape 9 : Enregistrer le fichier JPG

Finally, bind the rasterization options to the JPEG options and save the image to disk.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

When the loop finishes, you’ll have a JPG file for each layout, each sized exactly to match the original DWF dimensions.

## Problèmes courants et solutions

| Symptôme | Cause probable | Solution |
|----------|----------------|----------|
| Empty JPG output | `options.Layouts` not set correctly | Verify the layout name matches `page.Name`. |
| Distorted image | Wrong DPI conversion | Use `CommonHelper.DPI = 300` (or your target DPI) before conversion. |
| File not found | Incorrect `MyDir` path | Use absolute paths or `Path.Combine`. |
| License exception | No license applied | Load a temporary or permanent license before calling `Image.Load`. |

## Questions fréquemment posées

### Q1 : Aspose.CAD est‑il compatible avec les derniers formats de fichiers DWG ?

A1: Aspose.CAD supports various DWG file formats, including the latest versions. Refer to the [documentation](https://reference.aspose.com/cad/net/) for specific compatibility details.

### Q2 : Puis‑je utiliser Aspose.CAD pour des projets commerciaux et personnels ?

A2: Yes, Aspose.CAD offers flexible licensing options for both commercial and personal use. Visit the [page d'achat](https://purchase.aspose.com/buy) for more details.

### Q3 : Comment obtenir une licence temporaire pour Aspose.CAD ?

A3: You can get a temporary license from [ici](https://purchase.aspose.com/temporary-license/) for evaluation purposes.

### Q4 : Où puis‑je trouver du support pour Aspose.CAD ?

A4: For any queries or assistance, visit the [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5 : Une version d’essai gratuite est‑elle disponible pour Aspose.CAD ?

A5: Yes, you can access a free trial version of Aspose.CAD [ici](https://releases.aspose.com/).

### Q6 : Comment convertir directement un fichier DWG en JPG sans extraire le DWF au préalable ?

A6: You can load the DWG file with `Aspose.CAD.Image.Load` and use the same rasterization workflow; just set `options.Layouts` to the desired layout name(s) from the DWG.

### Q7 : La conversion préserve‑t‑elle la qualité vectorielle ?

A7: Once rasterized to JPG, the image is bitmap‑based, so vector scalability is lost. For lossless scaling, consider exporting to PNG or SVG instead.

---

**Dernière mise à jour:** 2026-04-06  
**Testé avec:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}