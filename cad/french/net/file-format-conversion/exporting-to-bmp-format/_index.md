---
title: Exporter au format BMP - Tutoriel Aspose.CAD
linktitle: Exportation au format BMP
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Explorez le monde transparent de l'exportation d'images 3D vers BMP à l'aide d'Aspose.CAD pour .NET. Suivez notre tutoriel pour une expérience sans tracas.
type: docs
weight: 11
url: /fr/net/file-format-conversion/exporting-to-bmp-format/
---
## Introduction

Dans le monde dynamique du développement de logiciels, Aspose.CAD for .NET s'impose comme un outil puissant pour gérer les fichiers de conception assistée par ordinateur (CAO). Si vous souhaitez exporter des images CAO au format BMP largement utilisé, ce didacticiel est votre guide incontournable. Dans cette procédure pas à pas, nous explorerons le processus d'exportation d'images 3D au format BMP à l'aide d'Aspose.CAD pour .NET. Allons-y !

## Conditions préalables

Avant de commencer ce didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.CAD pour .NET : téléchargez et installez la bibliothèque Aspose.CAD à partir de[ici](https://releases.aspose.com/cad/net/).
- Environnement de développement : configurez un environnement de développement .NET.
- Fichier CAO : préparez un fichier CAO pour l'exportation. Pour cet exemple, nous utiliserons "18-12-11 9644 - site.dwf".

## Importer des espaces de noms

Dans votre projet .NET, assurez-vous d'importer les espaces de noms nécessaires :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Étape 1 : Charger l'image CAO

Commencez par charger l'image CAO dans votre projet. Remplacez « Votre répertoire de documents » par le chemin du répertoire réel.

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    // Votre code pour charger l'image va ici
}
```

## Étape 2 : configurer les options d'exportation BMP

Configurez les options d'exportation BMP, y compris les options de rastérisation vectorielle pour les fichiers CAO.

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## Étape 3 : Exporter vers BMP

Exécutez le processus d'exportation en spécifiant le chemin de sortie du fichier BMP.

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## Conclusion

Toutes nos félicitations! Vous avez exporté avec succès une image 3D au format BMP à l'aide d'Aspose.CAD pour .NET. Ce didacticiel donne un aperçu de la polyvalence d'Aspose.CAD, qui permet de réaliser des tâches complexes comme un jeu d'enfant.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour .NET avec n’importe quel format de fichier CAO ?

A1 : Oui, Aspose.CAD prend en charge différents formats de fichiers CAO, offrant ainsi une flexibilité à vos projets.

### Q2 : Une licence temporaire est-elle disponible à des fins de test ?

 A2 : Certainement ! Vous pouvez obtenir un permis temporaire[ici](https://purchase.aspose.com/temporary-license/) pour évaluation.

### Q3 : Où puis-je trouver une documentation complète pour Aspose.CAD ?

 A3 : Se référer à la documentation[ici](https://reference.aspose.com/cad/net/) pour des informations détaillées et des exemples.

### Q4 : Comment puis-je rechercher du soutien ou me connecter avec la communauté ?

 A4 : Visitez le forum Aspose.CAD[ici](https://forum.aspose.com/c/cad/19) pour poser des questions et interagir avec la communauté.

### Q5 : Puis-je acheter Aspose.CAD pour .NET ?

 A5 : Oui, vous pouvez acheter Aspose.CAD[ici](https://purchase.aspose.com/buy) pour libérer tout son potentiel pour vos projets.
