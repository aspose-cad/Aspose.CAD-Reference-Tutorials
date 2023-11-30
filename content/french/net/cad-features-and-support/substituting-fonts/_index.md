---
title: Remplacement des polices dans Aspose.CAD pour .NET
linktitle: Remplacement des polices
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Apprenez à remplacer les polices dans Aspose.CAD par .NET sans effort. Suivez notre guide étape par étape pour une personnalisation efficace des polices dans vos dessins CAO.
type: docs
weight: 17
url: /fr/net/cad-features-and-support/substituting-fonts/
---
## Introduction

Dans le domaine du développement CAO utilisant .NET, la capacité à manipuler les polices est une compétence cruciale. Aspose.CAD for .NET fournit à cet effet un ensemble d'outils robustes, permettant aux développeurs de remplacer de manière transparente les polices dans leurs dessins CAO. Dans ce didacticiel, nous explorerons le processus étape par étape, démontrant comment réaliser efficacement la substitution de polices.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir les éléments suivants :

- Connaissance de base de la programmation .NET.
-  Aspose.CAD pour .NET installé. Sinon, vous pouvez le télécharger[ici](https://releases.aspose.com/cad/net/).
- Un fichier de dessin CAO pour la pratique pratique.

## Importer des espaces de noms

Avant de commencer, importez les espaces de noms nécessaires pour accéder aux fonctionnalités Aspose.CAD dans votre application .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## Étape 1 : Charger le dessin CAO

 Commencez par charger le dessin CAO dans une instance de`CadImage`Assurez-vous de fournir le chemin correct vers votre répertoire de documents.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Votre code pour d'autres actions va ici
}
```

## Étape 2 : Parcourir les styles

 Ensuite, parcourez les styles du dessin CAO à l'aide d'un`foreach` boucle. Cela vous permet d'accéder et de manipuler des styles de police individuels.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Votre code pour la manipulation de style va ici
}
```

## Étape 3 : Remplacer les polices globalement

 Pour remplacer globalement les polices par tous les styles, définissez l'option`PrimaryFontName` propriété pour chaque style au nom de police souhaité, par exemple « Arial ».

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

## Étape 4 : Remplacer la police par le nom du style

Si vous souhaitez remplacer la police par un style spécifique, vous pouvez le faire en vérifiant le nom du style dans la boucle.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment remplacer les polices dans Aspose.CAD par .NET. Cette compétence est précieuse pour personnaliser l'apparence des dessins CAO selon vos préférences.

## FAQ

### Q1 : Puis-je annuler les modifications de police dans Aspose.CAD pour .NET ?

A1 : Oui, vous pouvez annuler les modifications de police en rechargeant le dessin CAO d'origine ou en conservant une sauvegarde.

### Q2 : Existe-t-il d'autres propriétés de police que je peux modifier ?

 A2 : Absolument, d’ailleurs`PrimaryFontName`, Aspose.CAD pour .NET donne accès à diverses propriétés liées aux polices pour une personnalisation avancée.

### Q3 : Aspose.CAD est-il compatible avec différents formats de CAO ?

A3 : Oui, Aspose.CAD prend en charge une large gamme de formats CAO, garantissant ainsi la flexibilité de vos projets de développement.

### Q4 : Puis-je automatiser la substitution de polices dans le traitement par lots ?

A4 : Vous pouvez certainement mettre en œuvre un traitement par lots pour automatiser la substitution de polices sur plusieurs dessins CAO.

### Q5 : Où puis-je trouver une assistance supplémentaire pour Aspose.CAD pour .NET ?

 A5 : Pour obtenir un soutien supplémentaire et des discussions communautaires, visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

