---
title: Travailler avec des fichiers DWG en C# - Obtenir la taille de la mise en page DWF
linktitle: Travailler avec des fichiers DWG en C# - Obtenir la taille de la mise en page DWF
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez la puissance d'Aspose.CAD pour .NET dans la gestion des fichiers DWG. Apprenez à extraire facilement les tailles de mise en page DWF à l’aide de C#.
type: docs
weight: 10
url: /fr/net/dwg-file-manipulation/get-size-of-dwf-layout/
---
## Introduction

Dans le domaine de la conception assistée par ordinateur (CAO) et du développement .NET, Aspose.CAD se présente comme un outil puissant pour gérer les fichiers DWG. Ce didacticiel vous guidera tout au long du processus d'utilisation des fichiers DWG en C# et d'extraction de la taille d'une mise en page DWF. Avant de plonger dans le code, assurons-nous que vous avez tout mis en place pour vous lancer dans ce voyage.

## Conditions préalables

Pour suivre ce didacticiel en toute transparence, assurez-vous d'avoir les prérequis suivants en place :

-  Aspose.CAD pour .NET : assurez-vous qu'Aspose.CAD pour .NET est installé. Vous pouvez le télécharger depuis le[Page de téléchargement d'Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).

Maintenant que vous disposez des outils nécessaires, passons à l’arène du codage.

## Importer des espaces de noms

Avant de commencer à travailler avec le code, importons les espaces de noms requis :

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Ces espaces de noms fourniront les classes et méthodes essentielles pour gérer les fichiers CAO avec Aspose.CAD dans votre application C#.

## Étape 1 : Configurez votre environnement

Commencez par vous assurer que vous disposez de l’environnement approprié pour votre projet. Référencez la bibliothèque Aspose.CAD dans votre projet C#.

## Étape 2 : Définir les chemins de fichiers

Définissez les chemins de votre fichier DWG et le répertoire de sortie des fichiers JPG générés :

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Étape 3 : Charger l'image DWF

Chargez l'image DWF à l'aide d'Aspose.CAD :

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Le code pour les étapes ultérieures sera ici
}
```

## Étape 4 : Parcourir les pages

Parcourez les pages de l'image DWF :

```csharp
foreach (var page in image.Pages)
{
    // Le code pour les étapes ultérieures sera ici
}
```

## Étape 5 : obtenir des informations sur la mise en page

Obtenez des informations sur la mise en page de chaque page :

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Étape 6 : Configurer les options JPG

Configurez les options pour enregistrer la mise en page sous forme de fichier JPG :

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Le code pour les étapes ultérieures sera ici
}
```

## Étape 7 : Déterminer la taille de la page

Déterminez la taille de la présentation DWF :

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Le code pour les étapes ultérieures sera ici
```

## Étape 8 : Configurer les dimensions de la page

Configurez les dimensions de la page en fonction du type d'unité :

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Étape 9 : Enregistrez le fichier JPG

Enregistrez le fichier JPG avec les options spécifiées :

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Vous avez maintenant réussi à extraire la taille de la mise en page DWF du fichier DWG à l'aide d'Aspose.CAD en C#. N'hésitez pas à explorer davantage de fonctionnalités et de fonctionnalités offertes par Aspose.CAD pour le développement .NET.

## Conclusion

Dans ce didacticiel, nous avons expliqué le processus d'utilisation des fichiers DWG en C# à l'aide d'Aspose.CAD. En suivant ces étapes, vous pouvez non seulement obtenir la taille d'une mise en page DWF, mais également exploiter les capacités d'Aspose.CAD pour diverses tâches liées à la CAO dans vos projets .NET.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec les derniers formats de fichiers DWG ?

 A1 : Aspose.CAD prend en charge différents formats de fichiers DWG, y compris les dernières versions. Se référer au[Documentation](https://reference.aspose.com/cad/net/) pour des détails de compatibilité spécifiques.

### Q2 : Puis-je utiliser Aspose.CAD pour des projets commerciaux et personnels ?

A2 : Oui, Aspose.CAD propose des options de licence flexibles pour un usage commercial et personnel. Visiter le[page d'achat](https://purchase.aspose.com/buy) pour plus de détails.

### Q3 : Comment puis-je obtenir une licence temporaire pour Aspose.CAD ?

 A3 : Vous pouvez obtenir une licence temporaire auprès de[ici](https://purchase.aspose.com/temporary-license/) à des fins d’évaluation.

### Q4 : Où puis-je trouver de l'assistance pour Aspose.CAD ?

 A4 : Pour toute question ou assistance, visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5 : Existe-t-il un essai gratuit disponible pour Aspose.CAD ?

 A5 : Oui, vous pouvez accéder à une version d'essai gratuite d'Aspose.CAD[ici](https://releases.aspose.com/).