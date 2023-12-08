---
title: Prise en charge de la 3D pour DGN V7 dans Aspose.CAD pour .NET
linktitle: Prise en charge de la 3D pour DGN V7
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Libérez la puissance de la prise en charge 3D pour DGN V7 dans Aspose.CAD pour .NET. Suivez notre tutoriel étape par étape.
type: docs
weight: 20
url: /fr/net/cad-features-and-support/support-of-3d-for-dgn-v7/
---
## Introduction

Bienvenue dans notre didacticiel complet sur l'exploitation de la prise en charge de la 3D pour DGN V7 dans Aspose.CAD pour .NET ! Aspose.CAD est une bibliothèque puissante qui permet aux développeurs de travailler de manière transparente avec des fichiers CAO dans leurs applications .NET. Dans ce didacticiel, nous explorerons les étapes d'utilisation de la prise en charge 3D pour DGN V7, vous fournissant ainsi les connaissances nécessaires pour améliorer vos projets liés à la CAO.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.CAD pour .NET : assurez-vous qu'Aspose.CAD pour .NET est installé. Sinon, vous pouvez le télécharger depuis[ici](https://releases.aspose.com/cad/net/).

- Environnement de développement : configurez un environnement de développement approprié, tel que Visual Studio, pour le développement d'applications .NET.

- Exemple de fichier DGN : préparez un exemple de fichier DGN pour le test. Vous pouvez utiliser l'exemple de fichier fourni « Nikon_D90_Camera.dgn ».

Passons maintenant aux étapes pour obtenir la prise en charge 3D de DGN V7 à l'aide d'Aspose.CAD pour .NET !

## Importer des espaces de noms

Dans votre application .NET, commencez par importer les espaces de noms nécessaires :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Étape 1 : Configurez votre répertoire de documents

 Assurez-vous d'avoir un répertoire de documents configuré dans votre projet. Remplacer`"Your Document Directory"` avec le chemin réel vers votre répertoire de documents.

```csharp
string MyDir = "Your Document Directory";
```

## Étape 2 : charger le fichier DGN

Chargez le fichier DGN existant en tant que CadImage à l'aide du code suivant :

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Votre code pour un traitement ultérieur va ici
}
```

## Étape 3 : Configurer les options d'exportation PDF

Configurez les options d'exportation au format PDF, en spécifiant les options de rastérisation vectorielle telles que les dimensions de la page, la mise à l'échelle automatique des mises en page, la couleur d'arrière-plan et les mises en page à exporter.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Exporter uniquement les vues spécifiées
    }
};
```

## Étape 4 : Enregistrez l'image raster

Enregistrez le fichier DGN en tant qu'image raster avec les options configurées.

```csharp
dgnImage.Save(outFile, options);
```

## Conclusion

Toutes nos félicitations! Vous avez utilisé avec succès Aspose.CAD pour .NET pour exporter un fichier DGN avec prise en charge 3D vers une image raster. Ce tutoriel vous a fourni les étapes essentielles pour intégrer cette fonctionnalité dans vos projets CAO.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour .NET avec d’autres formats de fichiers CAO ?

A1 : Oui, Aspose.CAD prend en charge divers formats de fichiers CAO, notamment DWG et DXF.

### Q2 : Comment puis-je gérer les exceptions lorsque je travaille avec Aspose.CAD ?

A2 : Enveloppez votre code dans un bloc try-catch, comme démontré dans l'exemple fourni, pour gérer les exceptions avec élégance.

### Q3 : Aspose.CAD est-il adapté aux projets commerciaux ?

 A3 : Absolument ! Vous pouvez acheter Aspose.CAD pour .NET[ici](https://purchase.aspose.com/buy).

### Q4 : Puis-je essayer Aspose.CAD pour .NET avant d'acheter ?

A4 : Certainement ! Découvrez l'essai gratuit[ici](https://releases.aspose.com/).

### Q5 : Où puis-je trouver une assistance communautaire pour Aspose.CAD for .NET ?

 A5 : Visitez le forum de la communauté[ici](https://forum.aspose.com/c/cad/19).