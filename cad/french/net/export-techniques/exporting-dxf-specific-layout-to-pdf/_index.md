---
title: Exportation d'une mise en page spécifique DXF au format PDF - Guide Aspose.CAD
linktitle: Exportation d'une mise en page spécifique DXF au format PDF
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez comment exporter des mises en page spécifiques DXF au format PDF à l'aide d'Aspose.CAD pour .NET. Suivez notre guide étape par étape pour des conversions efficaces et de haute qualité.
weight: 11
url: /fr/net/export-techniques/exporting-dxf-specific-layout-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportation d'une mise en page spécifique DXF au format PDF - Guide Aspose.CAD

## Introduction

Bienvenue dans le didacticiel Aspose.CAD sur l'exportation de mises en page spécifiques DXF au format PDF à l'aide des puissantes fonctionnalités d'Aspose.CAD pour .NET. Ce guide étape par étape vous guidera tout au long du processus de conversion de fichiers DXF en PDF, en vous concentrant sur une mise en page spécifique nommée « Modèle ». Aspose.CAD fournit des outils et des fonctionnalités efficaces pour rationaliser le processus de conversion, garantissant ainsi une sortie de haute qualité pour vos dessins CAO.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Aspose.CAD pour .NET : assurez-vous que la bibliothèque Aspose.CAD est installée dans votre projet .NET. Vous pouvez le télécharger[ici](https://releases.aspose.com/cad/net/) et suivez les instructions d'installation fournies dans la documentation.

- Environnement de développement : configurez un environnement de développement .NET fonctionnel, y compris Visual Studio ou tout autre IDE préféré.

- Fichier DXF : préparez un fichier DXF que vous souhaitez convertir en PDF. Pour ce guide, nous utiliserons un exemple de fichier nommé « conic_pyramid.dxf ».

## Importer des espaces de noms

Dans votre projet .NET, incluez les espaces de noms nécessaires pour exploiter les fonctionnalités d'Aspose.CAD. Ajoutez les lignes suivantes au début de votre code :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
namespace Aspose.CAD.Examples.CSharp.DXF_Drawings

```

## Étape 1 : Charger le fichier DXF

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Votre code pour les étapes ultérieures sera ici
}
```

## Étape 2 : définir les options de rastérisation

```csharp
// Créez une instance de CadRasterizationOptions et définissez ses différentes propriétés
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
// Spécifiez le nom de la mise en page souhaitée
rasterizationOptions.Layouts = new string[] { "Model" };
```

## Étape 3 : Définir les options PDF

```csharp
// Créer une instance de PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Définir la propriété VectorRasterizationOptions
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 4 : Définir le chemin de sortie

```csharp
MyDir = MyDir + "conic_pyramid_layout_out.pdf";
```

## Étape 5 : Exporter le DXF au format PDF

```csharp
// Exporter le DXF au format PDF
image.Save(MyDir, pdfOptions);
```

## Étape 6 : Afficher le message de réussite

```csharp
// Afficher le message de réussite
Console.WriteLine("\nThe DXF file with the specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment exporter un fichier DXF avec une mise en page spécifique au format PDF à l'aide d'Aspose.CAD pour .NET. Ce guide couvre les étapes essentielles, du chargement du fichier DXF à la définition des options de rastérisation et à l'exportation au format PDF.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec toutes les versions de fichiers DXF ?

 A1 : Aspose.CAD prend en charge différentes versions de fichiers DXF. Se référer au[Documentation](https://reference.aspose.com/cad/net/) pour la liste des versions prises en charge.

### Q2 : Puis-je personnaliser les paramètres de sortie PDF ?

A2 : Oui, vous pouvez personnaliser les paramètres de sortie PDF en ajustant les propriétés de`CadRasterizationOptions` et`PdfOptions` selon vos exigences.

### Q3 : Existe-t-il un essai gratuit disponible pour Aspose.CAD ?

 A3 : Oui, vous pouvez explorer Aspose.CAD avec un essai gratuit en visitant[ici](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir de l'aide pour Aspose.CAD ?

 A4 : Pour toute assistance ou question, visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5 : Où puis-je acheter une licence pour Aspose.CAD ?

 A5 : Vous pouvez acheter une licence pour Aspose.CAD[ici](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
