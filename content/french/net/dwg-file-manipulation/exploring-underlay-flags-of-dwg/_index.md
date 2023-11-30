---
title: Explorer les indicateurs de calque sous-jacents des fichiers DWG - Tutoriel Aspose.CAD
linktitle: Exploration des indicateurs de calque sous-jacent des fichiers DWG
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Libérez la puissance d'Aspose.CAD pour .NET en explorant les indicateurs sous-jacents des fichiers DWG. Suivez notre guide étape par étape.
type: docs
weight: 13
url: /fr/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
---
## Introduction

Si vous plongez dans le monde complexe des fichiers CAO, en particulier des fichiers DWG, et que vous souhaitez percer les mystères des drapeaux sous-jacents, vous êtes au bon endroit. Ce didacticiel vous guidera tout au long du processus d'exploration des indicateurs de calque sous-jacents dans les fichiers DWG à l'aide de la puissante bibliothèque Aspose.CAD pour .NET.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir les éléments suivants :

- Une compréhension de base de la programmation C# et .NET.
-  Aspose.CAD pour la bibliothèque .NET installée. Sinon, vous pouvez le télécharger[ici](https://releases.aspose.com/cad/net/).
- Un fichier DWG pour les tests. Vous pouvez utiliser l'exemple de fichier "BlockRefDgn.dwg" fourni dans le didacticiel.

## Importer des espaces de noms

Pour commencer, vous devez importer les espaces de noms nécessaires. Voici un extrait pour vous aider :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;

```

## Étape 1 : charger le fichier DWG et le convertir en CadImage

Commencez par charger le fichier DWG existant et convertissez-le en CadImage :

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Charger le fichier DWG et le convertir en CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Votre code pour les étapes suivantes sera ici
}
```

## Étape 2 : Parcourir les entités

Ensuite, parcourez chaque entité dans le fichier DWG :

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Votre code pour les étapes suivantes sera ici
}
```

## Étape 3 : Vérifiez le type CadDgnUnderlay

Vérifiez si l'entité est de type CadDgnUnderlay :

```csharp
if (entity is CadDgnUnderlay)
{
    // Votre code pour les étapes suivantes sera ici
}
```

## Étape 4 : accéder aux indicateurs de sous-couche

Accédez à différents indicateurs de sous-couche et extrayez les informations pertinentes :

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

## Conclusion

Toutes nos félicitations! Vous avez exploré avec succès les indicateurs de calque sous-jacents des fichiers DWG à l'aide d'Aspose.CAD pour .NET. Ce didacticiel vous a doté des connaissances nécessaires pour naviguer dans les entités et extraire des informations cruciales sur les sous-couches.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour .NET avec d’autres formats de fichiers CAO ?

A1 : Aspose.CAD prend en charge divers formats de CAO, notamment DWG, DXF, DGN, etc. Consultez la documentation pour la liste complète.

### Q2 : Une licence temporaire est-elle disponible pour Aspose.CAD pour .NET ?

 A2 : Oui, vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).

### Q3 : Où puis-je trouver de l'assistance pour Aspose.CAD pour .NET ?

 A3 : Visitez le forum d'assistance[ici](https://forum.aspose.com/c/cad/19) à l'aide.

### Q4 : Comment puis-je acheter Aspose.CAD pour .NET ?

 A4 : Acheter la bibliothèque[ici](https://purchase.aspose.com/buy).

### Q5 : Existe-t-il un essai gratuit ?

 A5 : Oui, vous pouvez accéder à l'essai gratuit[ici](https://releases.aspose.com/).
