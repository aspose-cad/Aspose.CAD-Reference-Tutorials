---
date: 2026-03-16
description: Apprenez à convertir DWG en PDF ou en images raster avec Aspose.CAD pour
  .NET. Ce tutoriel pas à pas de conversion CAD en PDF couvre l'exportation de DWG
  vers des formats d'image tels que PNG et montre comment exporter efficacement les
  fichiers DWG en images.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Comment convertir des fichiers DWG en PDF et images raster en utilisant Aspose.CAD
  pour .NET
url: /fr/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

top-button >}}

All good.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportation de DWG vers PDF ou images raster - Guide Aspose.CAD

## Introduction

Si vous devez **convertir DWG en PDF** (ou vers des formats raster tels que PNG) directement depuis une application .NET, vous êtes au bon endroit. Dans ce tutoriel, nous parcourrons les étapes exactes nécessaires pour utiliser Aspose.CAD pour .NET afin d'effectuer la conversion, expliquer pourquoi la bibliothèque est un choix solide, et vous montrer comment gérer à la fois la sortie PDF et image avec seulement quelques lignes de code.

## Quick Answers
- **Quelle bibliothèque gère la conversion DWG ?** Aspose.CAD for .NET  
- **Puis-je exporter DWG en PNG ainsi qu'en PDF ?** Oui – les mêmes options de rasterisation fonctionnent pour les deux formats.  
- **Ai-je besoin d'une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **La conversion d'unités est‑elle gérée automatiquement ?** Vous pouvez définir le système d'unités manuellement (métrique ou impérial) comme montré dans le code.

## What is “convert DWG to PDF”?

Convertir DWG en PDF signifie prendre un dessin CAD (DWG) et le rendre sous forme de document portable, en lecture seule (PDF). Cela est utile pour partager des conceptions avec des parties prenantes qui n'ont pas de logiciel CAD, créer de la documentation imprimable ou archiver des dessins dans un format lisible universellement.

## Why use Aspose.CAD for this conversion?
- **Aucune dépendance externe** – la bibliothèque fonctionne entièrement en code géré.  
- **Haute fidélité** – conserve les calques, les épaisseurs de ligne et les informations de mise en page.  
- **Options de raster intégrées** – vous permet d'exporter en PNG, JPEG, BMP, etc., avec un seul objet de configuration.  
- **Multi‑plateforme** – fonctionne sous Windows, Linux et macOS avec .NET Core.

## Prerequisites

Avant de plonger dans le tutoriel, assurez‑vous d'avoir les éléments suivants en place :

- Une compréhension de base de la programmation .NET.  
- Bibliothèque Aspose.CAD for .NET installée. Sinon, téléchargez‑la [ici](https://releases.aspose.com/cad/net/).  
- Votre environnement de développement intégré (IDE) préféré configuré pour le développement .NET.

## Import Namespaces

Commençons par importer les espaces de noms nécessaires dans votre projet .NET. Cela garantit que vous avez accès aux fonctionnalités Aspose.CAD dans votre code.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Step 1: Load DWG File

Commencez par charger le fichier DWG que vous souhaitez convertir. Remplacez `"Your Document Directory"` par le chemin vers votre fichier DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Step 2: Set up PDF Export (How to export DWG to PDF)

Ensuite, configurons les paramètres d'exportation PDF. Cet exemple montre comment définir la mise en page et gérer les conversions d'unités.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Step 3: Export to PDF

Exécutez l'exportation vers PDF en utilisant les paramètres configurés.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Step 4: Export to Raster Images (export dwg to image)

Étendez la fonctionnalité pour exporter vers des images raster, comme le PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Common Issues and Solutions

| Problème | Pourquoi cela se produit | Comment résoudre |
|----------|--------------------------|------------------|
| **Pages blanches dans le PDF** | Mise en page non spécifiée correctement | Assurez‑vous que `rasterizationOptions.Layouts` inclut le nom de mise en page correct (par ex., `"Model"`). |
| **Dimensions incorrectes** | Mauvaise correspondance DPI ou taille de page | Ajustez les valeurs `PageHeight`, `PageWidth` et DPI dans `CadRasterizationOptions`. |
| **Les unités apparaissent incorrectes** | Conversion d'unités non définie | Utilisez `DefineUnitSystem` pour définir `currentUnitIsMetric` et `currentUnitCoefficient` en fonction de `cadImage.UnitType`. |
| **Exception de licence** | Limitations de la version d'essai | Appliquez une licence temporaire ou permanente avant d'appeler `Image.Load`. |

## Frequently Asked Questions

### Q1: Puis‑je utiliser Aspose.CAD pour .NET dans mes projets commerciaux?
A1: Oui, vous le pouvez. Consultez [purchase.aspose.com/buy](https://purchase.aspose.com/buy) pour les détails de licence.

### Q2: Existe‑t‑il un essai gratuit disponible?
A2: Bien sûr ! Obtenez votre essai gratuit [ici](https://releases.aspose.com/).

### Q3: Comment puis‑je obtenir du support pour Aspose.CAD pour .NET?
A3: Rendez‑vous sur le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire.

### Q4: Puis‑je obtenir une licence temporaire à des fins de test?
A4: Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

### Q5: Où puis‑je trouver la documentation détaillée?
A5: La documentation est disponible sur [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: Comment **enregistrer un CAD en PNG** avec une haute qualité?
A6: Définissez `PageHeight` et `PageWidth` aux dimensions en pixels souhaitées et choisissez un DPI de 300 ou plus dans `CadRasterizationOptions`.

### Q7: Quelle est la meilleure façon de **convertir dwg** lorsque le fichier source contient plusieurs mises en page?
A7: Remplissez `rasterizationOptions.Layouts` avec tous les noms de mise en page que vous souhaitez exporter, puis bouclez sur chaque mise en page et appelez `Save` pour chaque format de sortie.

**Dernière mise à jour:** 2026-03-16  
**Testé avec:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}