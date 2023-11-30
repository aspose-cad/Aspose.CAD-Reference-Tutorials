---
title: Prise en charge de DGN V7 dans Aspose.CAD pour .NET
linktitle: Prise en charge de DGN V7
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez Aspose.CAD pour la prise en charge transparente de .NET pour DGN V7. Convertissez facilement des fichiers DGN en images raster grâce à des instructions étape par étape.
type: docs
weight: 19
url: /fr/net/cad-features-and-support/support-for-dgn-v7/
---
## Introduction

Dans le domaine du développement .NET, Aspose.CAD se distingue comme une puissante bibliothèque de gestion des fichiers de conception assistée par ordinateur (CAO). Ce didacticiel explore une fonctionnalité spécifique d'Aspose.CAD pour .NET : la prise en charge des fichiers DGN V7. DGN, abréviation de Design, est un format de fichier largement utilisé dans le domaine de la CAO. Aspose.CAD simplifie le processus de travail avec les fichiers DGN V7, offrant aux développeurs une expérience transparente.

## Conditions préalables

Avant de nous lancer dans la mise en œuvre, assurez-vous que les conditions préalables suivantes sont en place :

-  Aspose.CAD pour .NET : assurez-vous que la bibliothèque Aspose.CAD est installée. Vous pouvez le télécharger depuis le[site web](https://releases.aspose.com/cad/net/).

- Environnement de développement : configurez un environnement de développement .NET fonctionnel, y compris Visual Studio ou tout autre IDE préféré.

Maintenant que nous avons réglé les conditions préalables, explorons comment tirer parti de la prise en charge de DGN V7 dans Aspose.CAD pour .NET.

## Importer des espaces de noms

Commencez par importer les espaces de noms nécessaires pour accéder aux fonctionnalités d'Aspose.CAD :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Étape 1 : Charger le fichier DGN

 Commencez par charger un fichier DGN existant en tant que`CadImage` Remplacer`"Your Document Directory"` et`"Nikon_D90_Camera.dgn"` avec le chemin du répertoire et le nom de fichier appropriés.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Le code pour les étapes suivantes va ici...
}
```

## Étape 2 : configurer les options de rastérisation

 Créer un`CadRasterizationOptions` objet pour définir et définir diverses propriétés liées à la rastérisation.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Étape 3 : Définir les options de rastérisation vectorielle

 Créer un`JpegOptions` objet car nous avons l'intention de convertir le fichier DGN en JPEG. Attribuer le créé précédemment`CadRasterizationOptions` s'y opposer.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Étape 4 : Enregistrez l'image pixellisée

 Appeler le`Save` méthode du`CadImage` objet de classe pour exporter le fichier DGN vers une image raster, dans ce cas, un JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Une fois ces étapes terminées, le fichier DGN est exporté avec succès vers une image raster.

## Conclusion

Dans ce didacticiel, nous avons exploré la prise en charge transparente de DGN V7 dans Aspose.CAD pour .NET. En suivant le guide étape par étape, les développeurs peuvent facilement convertir des fichiers DGN en images raster, élargissant ainsi les capacités de leurs applications .NET.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec les dernières spécifications DGN V7 ?

R1 : Oui, Aspose.CAD est conçu pour gérer de manière transparente les fichiers DGN V7, garantissant ainsi la compatibilité avec les dernières spécifications.

### Q2 : Puis-je personnaliser les options de rastérisation pour la conversion de fichiers DGN ?

 A2 : Absolument. Le didacticiel montre comment créer et configurer`CadRasterizationOptions` pour adapter le processus de conversion.

### Q3 : Existe-t-il d'autres formats de sortie pris en charge en plus du JPEG ?

A3 : Oui, Aspose.CAD prend en charge différents formats de sortie. Vous pouvez explorer la documentation pour une liste complète.

### Q4 : Comment puis-je obtenir de l'aide pour les requêtes liées à Aspose.CAD ?

 A4 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien et les discussions de la communauté.

### Q5 : Existe-t-il un essai gratuit disponible pour Aspose.CAD pour .NET ?

 A5 : Oui, vous pouvez accéder à un essai gratuit[ici](https://releases.aspose.com/).