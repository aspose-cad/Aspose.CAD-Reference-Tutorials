---
title: Exportation de dessins CAO au format SVG - Guide Aspose.CAD
linktitle: Exportation de dessins CAO au format SVG
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Explorez le processus transparent d'exportation de dessins CAO vers SVG à l'aide d'Aspose.CAD pour .NET. Améliorez votre développement CAO avec flexibilité et personnalisation.
type: docs
weight: 15
url: /fr/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
---
## Introduction

Dans le monde dynamique de la CAO (Conception Assistée par Ordinateur), la capacité d'exporter des dessins dans différents formats est une compétence cruciale. SVG (Scalable Vector Graphics) est l'un de ces formats qui a gagné en popularité en raison de son évolutivité et de sa polyvalence. Dans ce didacticiel, nous explorerons comment exporter des dessins CAO au format SVG à l'aide de la puissante bibliothèque Aspose.CAD pour .NET.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Bibliothèque Aspose.CAD pour .NET : téléchargez et installez la bibliothèque Aspose.CAD pour .NET. Vous pouvez trouver la bibliothèque[ici](https://releases.aspose.com/cad/net/).

- Environnement de développement : configurez un environnement de développement approprié avec Visual Studio ou tout autre outil de développement .NET.

## Importer des espaces de noms

Pour commencer, importez les espaces de noms nécessaires dans votre projet :

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Étape 1 : Définir le répertoire des documents

```csharp
// Le chemin d'accès au répertoire des documents.
string MyDir = "Your Document Directory";
```

## Étape 2 : Charger le dessin CAO

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

## Étape 3 : Configurer les options d'exportation SVG

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;
    options.TextAsShapes = true;
```

## Étape 4 : Enregistrez le fichier SVG

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

En suivant ces étapes simples, vous pouvez exporter en toute transparence des dessins CAO au format SVG à l'aide d'Aspose.CAD pour .NET. La bibliothèque offre des options de flexibilité et de personnalisation, vous permettant d'adapter la sortie en fonction de vos besoins.

## Conclusion

En conclusion, Aspose.CAD pour .NET simplifie le processus d'exportation de dessins CAO vers SVG. Son API intuitive et ses fonctionnalités robustes en font un outil précieux pour les développeurs travaillant avec des applications de CAO.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec tous les formats de CAO ?

A1 : Aspose.CAD prend en charge divers formats de CAO, notamment DWG et DXF, garantissant une large compatibilité.

### Q2 : Puis-je personnaliser le mode couleur lors de l’exportation au format SVG ?

A2 : Oui, Aspose.CAD vous permet de choisir le mode couleur, offrant ainsi une flexibilité dans la sortie.

### Q3 : Des licences temporaires sont-elles disponibles à des fins de test ?

 A3 : Oui, vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/) pour évaluation.

### Q4 : Où puis-je trouver une documentation détaillée pour Aspose.CAD ?

 A4 : La documentation est disponible[ici](https://reference.aspose.com/cad/net/).

### Q5 : Comment puis-je obtenir de l'aide ou poser des questions relatives à Aspose.CAD ?

 A5 : Visitez le forum de la communauté[ici](https://forum.aspose.com/c/cad/19) pour du soutien et des discussions.