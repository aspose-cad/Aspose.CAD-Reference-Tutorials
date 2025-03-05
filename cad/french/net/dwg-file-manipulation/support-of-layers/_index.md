---
title: Gestion des calques dans des fichiers DWG avec C# - Tutoriel Aspose.CAD
linktitle: Gestion des calques dans les fichiers DWG avec C#
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Apprenez à gérer les calques dans les fichiers DWG à l'aide de C# avec Aspose.CAD pour .NET. Guide étape par étape pour une manipulation efficace des fichiers CAO.
type: docs
weight: 11
url: /fr/net/dwg-file-manipulation/support-of-layers/
---
## Introduction

Bienvenue dans notre didacticiel approfondi sur la gestion des calques dans les fichiers DWG à l'aide de C# avec Aspose.CAD pour .NET. Aspose.CAD est une bibliothèque puissante qui permet aux développeurs de travailler de manière transparente avec les formats de fichiers CAO. Dans ce didacticiel, nous vous guiderons étape par étape tout au long du processus de gestion des calques dans les fichiers DWG.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Connaissance de base du langage de programmation C#.
- Visual Studio installé sur votre ordinateur.
-  Bibliothèque Aspose.CAD pour .NET, que vous pouvez télécharger à partir du[Site Web Aspose.CAD](https://releases.aspose.com/cad/net/).

## Importer des espaces de noms

Pour commencer, importez les espaces de noms nécessaires dans votre projet C#. Ces espaces de noms fournissent les fonctionnalités requises pour travailler avec des fichiers CAO.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Étape 1 : Charger le fichier DWG

Commencez par charger le fichier DWG dans votre application C# à l'aide de la bibliothèque Aspose.CAD.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Votre code pour les étapes suivantes va ici
}
```

## Étape 2 : configurer les options de rastérisation

 Créer une instance de`CadRasterizationOptions` et définissez ses propriétés pour définir la manière dont le fichier DWG doit être rastérisé.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Étape 3 : Spécifier les calques

Ajoutez les calques souhaités aux options de rastérisation. Dans cet exemple, nous avons ajouté « LayerA ».

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Étape 4 : configurer les options d'exportation d'images

 Créez les options d'exportation d'images nécessaires. Ici, nous utilisons`JpegOptions` pour exporter au format JPEG.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 5 : Enregistrez l'image exportée

Spécifiez le chemin de sortie et enregistrez le fichier DWG pixellisé au format JPEG.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

Vous avez maintenant géré avec succès les calques dans un fichier DWG en utilisant C# avec Aspose.CAD pour .NET.

## Conclusion

Dans ce didacticiel, nous avons parcouru le processus de gestion des calques dans les fichiers DWG à l'aide de C# et de la bibliothèque Aspose.CAD. En suivant ces étapes, vous pouvez travailler efficacement avec des fichiers CAO dans vos applications .NET.

## FAQ

### Q1 : Puis-je gérer plusieurs couches simultanément ?

 A1 : Oui, vous pouvez. Ajoutez simplement les noms des calques au`rasterizationOptions.Layers` tableau.

### Q2 : Une version d’essai d’Aspose.CAD est-elle disponible ?

 A2 : Oui, vous pouvez obtenir une version d'essai gratuite auprès de[ici](https://releases.aspose.com/).

### Q3 : Où puis-je trouver la documentation ?

 A3 : La documentation est disponible[ici](https://reference.aspose.com/cad/net/).

### Q4 : Comment puis-je obtenir de l'aide pour Aspose.CAD ?

 A4 : Vous pouvez demander de l'aide sur le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5 : Quelles sont les options de licence pour Aspose.CAD ?

 A5 : Vous pouvez explorer les options de licence et acheter les détails[ici](https://purchase.aspose.com/buy).