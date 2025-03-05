---
title: Exportation de mises en page spécifiques au format PDF - Guide Aspose.CAD
linktitle: Exportation de mises en page spécifiques au format PDF
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez comment exporter des mises en page spécifiques au format PDF à l'aide d'Aspose.CAD pour .NET. Guide étape par étape pour une intégration transparente.
type: docs
weight: 13
url: /fr/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
---
## Introduction

Bienvenue dans notre guide étape par étape sur l'exportation de mises en page spécifiques au format PDF à l'aide d'Aspose.CAD pour .NET. Aspose.CAD est une bibliothèque puissante qui permet aux développeurs de travailler de manière transparente avec les formats de fichiers CAO. Dans ce didacticiel, nous nous concentrerons sur l'exportation de mises en page spécifiques d'un fichier DWG vers un PDF à l'aide d'Aspose.CAD dans un environnement .NET.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Bibliothèque Aspose.CAD pour .NET : assurez-vous que la bibliothèque Aspose.CAD est installée. Vous pouvez le télécharger[ici](https://releases.aspose.com/cad/net/).

- Environnement de développement : configurez un environnement de développement .NET, tel que Visual Studio.

## Importer des espaces de noms

Dans votre projet .NET, importez les espaces de noms nécessaires pour Aspose.CAD :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Étape 1 : Charger le fichier DWG

```csharp
// Le chemin d'accès au répertoire des documents.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Votre code pour les étapes suivantes se trouve ici.
}
```

## Étape 2 : Définir les options de CadRasterization

```csharp
// Créez une instance de CadRasterizationOptions et définissez ses différentes propriétés
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Étape 3 : Spécifiez le nom de la mise en page

```csharp
// Spécifiez le nom de la mise en page souhaitée
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

## Étape 4 : Créer des options PDF

```csharp
// Créer une instance de PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Définir la propriété VectorRasterizationOptions
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 5 : Exporter au format PDF

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Exporter le DWG au format PDF
image.Save(MyDir, pdfOptions);
```

## Étape 6 : Afficher le message de réussite

```csharp
// Afficher le message de réussite
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment exporter des mises en page spécifiques au format PDF à l'aide d'Aspose.CAD pour .NET. Ce guide fournit une présentation détaillée, garantissant que vous pouvez intégrer cette fonctionnalité dans vos projets sans effort.

## FAQ

### Q1 : Puis-je exporter plusieurs mises en page simultanément ?

 A1 : Oui, modifiez simplement le`Layouts` tableau à l’étape 3 pour inclure les noms de toutes les mises en page souhaitées.

### Q2 : Aspose.CAD est-il compatible avec d’autres formats de fichiers CAO ?

A2 : Oui, Aspose.CAD prend en charge divers formats de CAO, notamment DWG, DXF, DWF, etc.

### Q3 : Comment puis-je ajuster les paramètres de sortie PDF ?

 A3 : Explorer les propriétés de`CadRasterizationOptions` à l'étape 2 pour les options de personnalisation.

### Q4 : Où puis-je trouver de la documentation supplémentaire sur Aspose.CAD ?

 A4 : Visitez le[Documentation](https://reference.aspose.com/cad/net/) pour des informations détaillées.

### Q5 : Existe-t-il un essai gratuit ?

 A5 : Oui, vous pouvez accéder à l'essai gratuit[ici](https://releases.aspose.com/).