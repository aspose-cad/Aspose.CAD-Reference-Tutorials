---
title: Exporter DGN vers une image raster dans Aspose.CAD pour .NET
linktitle: Exporter un DGN vers une image raster
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Convertissez facilement des DGN en images raster à l'aide d'Aspose.CAD pour .NET. Explorez le guide étape par étape et libérez la puissance de .NET dans la manipulation de fichiers CAO.
type: docs
weight: 13
url: /fr/net/cad-export-formats/export-dgn-to-raster-image/
---
## Introduction

Dans le domaine dynamique du développement .NET, Aspose.CAD apparaît comme un outil puissant pour gérer les fichiers de conception assistée par ordinateur (CAO). Ce didacticiel plonge dans le processus d'exportation de fichiers DGN vers des images raster à l'aide d'Aspose.CAD pour .NET. Si vous souhaitez transformer de manière transparente vos fichiers DGN en images raster visuellement attrayantes, vous êtes au bon endroit.

## Conditions préalables

Avant de nous lancer dans ce voyage, assurez-vous d’avoir les conditions préalables suivantes en place :

-  Aspose.CAD pour .NET : assurez-vous que la bibliothèque Aspose.CAD est installée dans votre projet .NET. Vous pouvez trouver la bibliothèque et la documentation pertinente sur le[site web](https://reference.aspose.com/cad/net/).

- Exemple de fichier DGN : préparez un fichier DGN pour la conversion. Dans notre exemple, nous utiliserons « Nikon_D90_Camera.dgn ».

Passons maintenant au guide étape par étape.

## Importer des espaces de noms

Dans votre projet .NET, commencez par importer les espaces de noms nécessaires pour Aspose.CAD. Cette étape vous permet d'accéder aux classes et méthodes requises pour la conversion d'images DGN en images raster.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Étape 1 : Charger le fichier DGN

 Commencez par charger le fichier DGN dans un`CadImage` objet. Cela constitue une base pour les opérations ultérieures.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Votre code pour un traitement ultérieur va ici
}
```

## Étape 2 : Définir les options de rastérisation

 Créer un`CadRasterizationOptions` objet et définissez diverses propriétés pour personnaliser le processus de rastérisation en fonction de vos besoins.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Étape 3 : Créer un objet JpegOptions

 Puisque nous visons à convertir le fichier DGN en JPEG, créez un`JpegOptions` objet et attribuer le paramètre précédemment défini`CadRasterizationOptions` à cela.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 4 : Enregistrez l'image raster

 Utiliser le`Save` méthode du`CadImage` classe pour exporter le fichier DGN vers une image raster au format souhaité, dans ce cas, un JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Conclusion

Toutes nos félicitations! Vous avez suivi avec succès les étapes d'exportation d'un fichier DGN vers une image raster à l'aide d'Aspose.CAD pour .NET. Ce tutoriel vous a doté des connaissances essentielles pour intégrer cette fonctionnalité dans vos projets .NET sans effort.

## FAQ

### Q1 : Puis-je exporter des fichiers DGN vers des formats autres que JPEG ?

A1 : Oui, Aspose.CAD pour .NET prend en charge différents formats de sortie. Vous pouvez modifier les options en conséquence à l'étape 3.

### Q2 Comment puis-je gérer les exceptions pendant le processus de conversion ?

A2 : assurez-vous que vous disposez d'une gestion appropriée des exceptions, comme démontré dans le code fourni, pour résoudre les problèmes potentiels.

### Q3 : Existe-t-il une version d'essai disponible pour Aspose.CAD pour .NET ?

 A3 : Oui, vous pouvez explorer le produit avec un essai gratuit. Visite[ici](https://releases.aspose.com/) pour plus d'informations.

### Q4 : Où puis-je demander de l'aide ou discuter des problèmes liés à Aspose.CAD for .NET ?

 A4 : Rendez-vous au[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien et les discussions de la communauté.

### Q5 : Comment puis-je obtenir une licence temporaire pour Aspose.CAD pour .NET ?

 A5 : Visite[ce lien](https://purchase.aspose.com/temporary-license/)pour acquérir une licence temporaire pour vos besoins de développement.