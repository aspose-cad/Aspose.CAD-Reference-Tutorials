---
title: Éléments DGN pris en charge dans Aspose.CAD pour .NET
linktitle: Éléments DGN pris en charge
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Explorez les puissantes fonctionnalités d'Aspose.CAD for .NET pour la gestion des fichiers DGN. Suivez notre guide étape par étape pour travailler de manière transparente avec des éléments 2D et 3D.
weight: 18
url: /fr/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Éléments DGN pris en charge dans Aspose.CAD pour .NET

## Introduction

Êtes-vous un développeur .NET souhaitant travailler avec des fichiers DGN de manière transparente ? Aspose.CAD pour .NET fournit une solution robuste pour gérer efficacement les fichiers DGN. Dans ce didacticiel, nous examinerons les éléments DGN pris en charge, vous guidant tout au long du processus d'utilisation d'Aspose.CAD pour .NET.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les éléments suivants :

- Connaissance de base de la programmation .NET.
- Visual Studio installé sur votre ordinateur.
-  Bibliothèque Aspose.CAD pour .NET, que vous pouvez télécharger[ici](https://releases.aspose.com/cad/net/).

## Importer des espaces de noms

Pour démarrer votre projet, importez les espaces de noms nécessaires dans votre application .NET. Cette étape garantit que vous avez accès aux fonctionnalités fournies par Aspose.CAD for .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Étape 1 : Charger le fichier DGN

Commencez par charger un fichier DGN existant en tant que CadImage dans votre application .NET.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Votre code ici
}
```

## Étape 2 : Parcourir les éléments DGN

Parcourez les éléments DGN à l’aide d’une boucle foreach. Aspose.CAD pour .NET fournit une variété de types d'éléments DGN avec lesquels vous pouvez travailler.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Votre code ici
}
```

## Étape 3 : Gérer les entités précédemment prises en charge

Gérez les entités 2D précédemment prises en charge, qui sont désormais également prises en charge pour la 3D.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Cas supplémentaires
        {
            // Votre code ici
            break;
        }
}
```

## Étape 4 : Gérer les entités 3D prises en charge

Gérez les entités 3D prises en charge fournies par Aspose.CAD pour .NET.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Votre code ici
            break;
        }
}
```

## Étape 5 : Exporter et enregistrer

Enfin, exportez le fichier DGN modifié vers une image raster et enregistrez-le dans le répertoire spécifié.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## Conclusion

Dans ce didacticiel, nous avons exploré les capacités d'Aspose.CAD pour .NET en matière de gestion et de manipulation des fichiers DGN. En suivant le guide étape par étape, vous pouvez travailler efficacement avec les éléments DGN pris en charge, qu'il s'agisse d'entités 2D ou 3D. Aspose.CAD pour .NET vous permet d'intégrer de manière transparente le traitement des fichiers DGN dans vos applications .NET.

## FAQ

### Q1 : Où puis-je trouver la documentation d'Aspose.CAD pour .NET ?

 A1 : Vous pouvez trouver la documentation[ici](https://reference.aspose.com/cad/net/).

### Q2 : Comment télécharger Aspose.CAD pour .NET ?

 A2 : Vous pouvez télécharger la bibliothèque[ici](https://releases.aspose.com/cad/net/).

### Q3 : Existe-t-il un essai gratuit disponible pour Aspose.CAD pour .NET ?

 A3 : Oui, vous pouvez accéder à l'essai gratuit[ici](https://releases.aspose.com/).

### Q4 : Où puis-je obtenir des licences temporaires pour Aspose.CAD pour .NET ?

 A4 : Des licences temporaires sont disponibles[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Besoin d'aide ou avez des questions ?

 A5 : Visitez la communauté Aspose.CAD pour .NET[forum d'entraide](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
