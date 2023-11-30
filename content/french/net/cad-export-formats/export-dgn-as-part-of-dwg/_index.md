---
title: Exporter DGN dans le cadre de DWG dans Aspose.CAD pour .NET
linktitle: Exporter DGN dans le cadre de DWG
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez comment exporter du DGN dans le cadre de DWG dans Aspose.CAD pour .NET. Suivez notre guide étape par étape pour une intégration transparente.
type: docs
weight: 11
url: /fr/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## Introduction

Dans le monde du développement .NET, Aspose.CAD se distingue comme une bibliothèque puissante pour travailler avec des fichiers de conception assistée par ordinateur (CAO). Ce didacticiel vous guidera tout au long du processus d'exportation d'un fichier DGN (Conception) dans le cadre d'un fichier DWG (Dessin) à l'aide d'Aspose.CAD pour .NET. Que vous soyez un développeur chevronné ou tout juste débutant, ce guide étape par étape vous aidera à exploiter les capacités d'Aspose.CAD pour accomplir efficacement cette tâche spécifique.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.CAD pour .NET : assurez-vous que la bibliothèque Aspose.CAD pour .NET est installée. Vous pouvez le télécharger[ici](https://releases.aspose.com/cad/net/).

- Environnement de développement : configurez votre environnement de développement .NET préféré, tel que Visual Studio.

- Connaissance de base de C# : Familiarisez-vous avec le langage de programmation C#.

## Importer des espaces de noms

Dans votre projet C#, incluez les espaces de noms nécessaires pour accéder à la fonctionnalité Aspose.CAD. Ajoutez les directives using suivantes au début de votre fichier de code :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Maintenant, décomposons le code fourni en plusieurs étapes :

## Étape 1 : Définir les chemins de fichiers

```csharp
//Chemins des fichiers d’entrée et de sortie
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Étape 2 : Créer une instance PDFOptions

```csharp
// Créer une instance de la classe PdfOptions pour exporter un DWG au format PDF
PdfOptions exportOptions = new PdfOptions();
```

## Étape 3 : Charger le fichier DWG

```csharp
// Chargez le fichier DWG existant en tant qu'image et convertissez-le au type CadImage
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Étape 4 : Parcourir les entités

```csharp
// Parcourez chaque entité dans le fichier DWG
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Étape 5 : Vérifier le type d'entité

```csharp
// Vérifiez si l'entité est une définition d'image
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Étape 6 : Obtenir le chemin de la sous-couche

```csharp
// S'il s'agit d'une définition d'image, récupérez la référence externe à l'objet
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Étape 7 : Définir les options de rastérisation

```csharp
// Définir les paramètres de l'objet CadRasterizationOptions
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Étape 8 : Exporter un fichier DWG au format PDF

```csharp
// Exportez le DWG au format PDF en appelant la méthode Save
cadImage.Save(outPath, exportOptions);
```

## Conclusion

Toutes nos félicitations! Vous avez suivi avec succès le processus d'exportation d'un fichier DGN dans le cadre d'un fichier DWG à l'aide d'Aspose.CAD pour .NET. Ce didacticiel vous a fourni les étapes fondamentales et les extraits de code pour réaliser cette tâche spécifique de manière transparente.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour .NET dans mes projets commerciaux ?
 A1 : Oui, vous pouvez. Visite[ici](https://purchase.aspose.com/buy) pour explorer les options de licence.

### Q2 : Existe-t-il des limites quant à la taille des fichiers DWG que je peux traiter ?
A2 : Aspose.CAD prend en charge la gestion des fichiers DWG volumineux, mais des limitations matérielles peuvent s'appliquer.

### Q3 : Existe-t-il une version d'essai disponible ?
 A3 : Oui, vous pouvez bénéficier d'un essai gratuit[ici](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir des licences temporaires ?
 A4 : Des licences temporaires peuvent être obtenues[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis-je demander de l'aide si je rencontre des problèmes ?
 A5 : Vous pouvez visiter le forum Aspose.CAD[ici](https://forum.aspose.com/c/cad/19) pour le soutien.