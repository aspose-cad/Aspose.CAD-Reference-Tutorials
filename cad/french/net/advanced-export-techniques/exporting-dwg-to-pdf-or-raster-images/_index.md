---
title: Exportation de DWG vers des images PDF ou raster - Guide Aspose.CAD
linktitle: Exportation de DWG au format PDF ou images raster
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez un guide complet sur l'exportation d'images DWG au format PDF ou raster à l'aide d'Aspose.CAD pour .NET. Apprenez les étapes, les prérequis et familiarisez-vous avec cette puissante bibliothèque.
type: docs
weight: 11
url: /fr/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## Introduction

Souhaitez-vous convertir de manière transparente des fichiers DWG en images PDF ou raster dans votre application .NET ? Cherchez pas plus loin! Ce guide étape par étape vous guidera tout au long du processus à l'aide de la puissante bibliothèque Aspose.CAD pour .NET. Que vous soyez un développeur chevronné ou débutant, ce tutoriel s'adresse à tous les niveaux de compétence.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir les éléments suivants en place :

- Une compréhension de base de la programmation .NET.
-  Aspose.CAD pour la bibliothèque .NET installée. Sinon, téléchargez-le[ici](https://releases.aspose.com/cad/net/).
- Votre environnement de développement intégré (IDE) préféré configuré pour le développement .NET.

## Importer des espaces de noms

Commençons par importer les espaces de noms nécessaires dans votre projet .NET. Cela garantit que vous avez accès à la fonctionnalité Aspose.CAD dans votre code.

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

## Étape 1 : Charger le fichier DWG

Commencez par charger le fichier DWG que vous souhaitez convertir. Remplacez "Votre répertoire de documents" par le chemin d'accès à votre fichier DWG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Votre code pour charger DWG va ici
}
```

## Étape 2 : Configurer l'exportation PDF

Maintenant, configurons les paramètres d'exportation PDF. Cet exemple montre comment définir la disposition et gérer les conversions d'unités.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Vérifier et définir le système d'unités
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Votre code pour configurer l'exportation PDF va ici
```

## Étape 3 : Exporter au format PDF

Exécutez l'exportation au format PDF en utilisant les paramètres configurés.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Étape 4 : Exporter vers des images raster

Étendez la fonctionnalité pour exporter vers des images raster, telles que PNG.

```csharp
// Format A4 à 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès à utiliser Aspose.CAD pour .NET pour exporter des fichiers DWG vers des images PDF et raster. Cette puissante bibliothèque rationalise le processus, le rendant efficace et convivial pour les développeurs.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour .NET dans mes projets commerciaux ?

 A1 : Oui, vous pouvez. Visite[achat.aspose.com/acheter](https://purchase.aspose.com/buy) pour les détails de la licence.

### Q2 : Existe-t-il un essai gratuit ?

 A2 : Certainement ! Profitez de votre essai gratuit[ici](https://releases.aspose.com/).

### Q3 : Comment puis-je obtenir une assistance pour Aspose.CAD pour .NET ?

 A3 : Rendez-vous au[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien de la communauté.

### Q4 : Puis-je obtenir une licence temporaire à des fins de test ?

 A4 : Oui, vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis-je trouver la documentation détaillée ?

 A5 : La documentation est disponible sur[Aspose.CAD](https://reference.aspose.com/cad/net/).