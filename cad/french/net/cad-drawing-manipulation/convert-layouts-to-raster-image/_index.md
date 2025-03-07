---
title: Convertir des mises en page en image raster dans Aspose.CAD pour .NET
linktitle: Convertir des mises en page en image raster
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Convertissez sans effort les mises en page CAO en images raster à l'aide d'Aspose.CAD pour .NET. Améliorez votre développement grâce à de puissantes capacités de manipulation CAO.
weight: 12
url: /fr/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir des mises en page en image raster dans Aspose.CAD pour .NET

## Introduction

Cherchez-vous à convertir sans effort des mises en page en images raster dans vos applications .NET ? Cherchez pas plus loin! Ce guide étape par étape vous guidera tout au long du processus d'utilisation d'Aspose.CAD pour .NET, une bibliothèque puissante qui simplifie les tâches de conception assistée par ordinateur (CAO).

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Aspose.CAD for .NET Library : téléchargez et installez la bibliothèque à partir du[Page de téléchargement d'Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).

- Environnement de développement : assurez-vous de disposer d'un environnement de développement .NET fonctionnel configuré sur votre ordinateur.

- Document à convertir : préparez un document CAO contenant les mises en page que vous souhaitez convertir en images raster.

- Votre répertoire de documents : remplacez l'espace réservé "Votre répertoire de documents" dans le code par le chemin d'accès à votre répertoire de documents.

## Importer des espaces de noms

Tout d'abord, importons les espaces de noms nécessaires pour rendre les fonctionnalités Aspose.CAD accessibles dans votre code.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Étape 1 : Charger le document CAO

Commencez par charger le document CAO à l'aide de la bibliothèque Aspose.CAD.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //Votre code pour les étapes ultérieures sera ici
}
```

## Étape 2 : configurer les options de rastérisation

 Créer une instance de`CadRasterizationOptions` pour définir la largeur et la hauteur de la page et spécifier les mises en page que vous souhaitez convertir.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Étape 3 : configurer TiffOptions pour l'image résultante

 Créer une instance de`TiffOptions`pour définir le format de l'image résultante.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 4 : Enregistrez l'image résultante

Spécifiez le chemin de sortie et enregistrez l'image convertie.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Conclusion

Toutes nos félicitations! Vous avez réussi à convertir les mises en page CAO en format d'image raster à l'aide d'Aspose.CAD pour .NET. Les possibilités sont vastes et ce guide sert de point de départ pour vos efforts liés à la CAO.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec tous les formats de CAO ?

 A1 : Aspose.CAD prend en charge une large gamme de formats de CAO, notamment DWG, DXF, DWF, STL, etc. Vérifier la[Documentation](https://reference.aspose.com/cad/net/) pour une liste complète.

### Q2 : Comment puis-je obtenir une licence temporaire pour Aspose.CAD ?

 A2 : Visitez le[page de licence temporaire](https://purchase.aspose.com/temporary-license/) d'acquérir une licence temporaire à des fins de tests et d'évaluation.

### Q3 : Où puis-je trouver de l'assistance pour Aspose.CAD ?

 A3 : Les forums sont un excellent endroit pour demander de l’aide. Visiter le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour se connecter avec la communauté et obtenir de l'aide.

### Q4 : Puis-je essayer Aspose.CAD gratuitement ?

 A4 : Absolument ! Prenez votre[essai gratuit](https://releases.aspose.com/) pour explorer les fonctionnalités et les capacités d'Aspose.CAD.

### Q5 : Où puis-je acheter une licence pour Aspose.CAD ?

 A5 : Accédez au[page d'achat](https://purchase.aspose.com/buy) pour acheter une licence et libérer tout le potentiel d'Aspose.CAD.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
