---
title: Ajouter du texte aux fichiers DWG en C# - Tutoriel Aspose.CAD
linktitle: Ajout de texte aux fichiers DWG en C#
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez comment ajouter du texte aux fichiers DWG à l'aide de C# et Aspose.CAD. Suivez ce didacticiel étape par étape pour une intégration transparente. Explorez la documentation Aspose.CAD pour obtenir des conseils complets.
type: docs
weight: 14
url: /fr/net/dwg-file-manipulation/adding-text-to-dwg/
---
## Introduction

Dans le domaine dynamique de la conception assistée par ordinateur (CAO) et du développement .NET, Aspose.CAD se distingue comme un outil puissant pour manipuler les fichiers DWG. L'ajout de texte aux fichiers DWG est une exigence courante et, dans ce didacticiel, nous verrons comment y parvenir à l'aide de C# et Aspose.CAD.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir les éléments suivants en place :

-  Bibliothèque Aspose.CAD : Téléchargez et installez la bibliothèque Aspose.CAD à partir du[lien de téléchargement](https://releases.aspose.com/cad/net/).

-  Répertoire de documents : créez un répertoire pour vos documents et notez son chemin comme`MyDir`.

Maintenant, décomposons le processus en étapes gérables.

## Importer des espaces de noms

Dans votre code C#, incluez les espaces de noms nécessaires pour accéder aux fonctionnalités d'Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Étape 1 : Charger le fichier DWG

 Chargez le fichier DWG dans un`Image` objet à l’aide de la bibliothèque Aspose.CAD.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Votre code pour les étapes suivantes va ici
}
```

## Étape 2 : Créer un objet CadText

 Instancier un`CadText` objet pour représenter le texte que vous souhaitez ajouter au fichier DWG.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;
cadText.ScaleX = 0.0;
```

## Étape 3 : Ajouter du texte au DWG

 Ajouter le créé`CadText` objet au fichier DWG à l’aide d’Aspose.CAD.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Étape 4 : Configurer les options PDF

Configurez les options PDF pour enregistrer le fichier DWG modifié au format PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Étape 5 : Enregistrer au format PDF

Enregistrez le fichier DWG modifié au format PDF avec le texte ajouté.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

Vous avez maintenant ajouté avec succès du texte à un fichier DWG à l'aide de C# et Aspose.CAD. N'hésitez pas à explorer plus de fonctionnalités et de fonctionnalités d'Aspose.CAD pour vos besoins de manipulation CAO.

## Conclusion

Dans ce didacticiel, nous avons couvert les étapes essentielles pour ajouter du texte aux fichiers DWG à l'aide de C# et Aspose.CAD. Cette combinaison puissante ouvre des possibilités de génération de documents CAO dynamiques et personnalisés.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec toutes les versions de fichiers DWG ?

A1 : Aspose.CAD prend en charge une large gamme de versions de fichiers DWG, garantissant la compatibilité avec divers logiciels de CAO.

### Q2 : Puis-je ajouter plusieurs entités de texte à un seul fichier DWG à l'aide d'Aspose.CAD ?

A2 : Oui, vous pouvez ajouter plusieurs entités de texte à un fichier DWG en répétant le processus décrit dans le didacticiel.

### Q3 : Comment puis-je modifier la police et le style du texte dans Aspose.CAD ?

 A3 : Pour modifier la police et le style du texte, ajustez les propriétés du`CadText` objet avant de l’ajouter au fichier DWG.

### Q4 : Y a-t-il des considérations en matière de licence pour l'utilisation d'Aspose.CAD dans un projet commercial ?

 A4 : Oui, assurez-vous du respect des conditions de licence Aspose.CAD. Faire référence à[Achat Aspose.CAD](https://purchase.aspose.com/buy) pour plus de détails.

### Q5 : Où puis-je demander de l'aide ou discuter des requêtes liées à Aspose.CAD ?

 A5 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19)pour se connecter avec la communauté et obtenir du soutien.