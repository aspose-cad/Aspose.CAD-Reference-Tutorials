---
title: Exporter des fichiers IFC vers PNG - Tutoriel Aspose.CAD
linktitle: Exportation de fichiers IFC au format PNG
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Explorez Aspose.CAD pour .NET, une solution robuste pour une conversion transparente IFC vers PNG. Téléchargez-le maintenant pour un traitement efficace des fichiers CAO.
weight: 10
url: /fr/net/exporting-to-image-formats/exporting-ifc-files-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter des fichiers IFC vers PNG - Tutoriel Aspose.CAD

## Introduction

Dans le monde dynamique de la conception assistée par ordinateur (CAO), une conversion efficace des fichiers est cruciale. Aspose.CAD pour .NET apparaît comme un outil puissant, offrant des capacités transparentes pour exporter des fichiers IFC (Industry Foundation Classes) au format PNG. Ce didacticiel étape par étape vous guidera tout au long du processus, garantissant une expérience fluide avec Aspose.CAD.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

### 1. Installation d'Aspose.CAD

 Assurez-vous que Aspose.CAD pour .NET est installé. Vous pouvez le télécharger depuis la page de version[ici](https://releases.aspose.com/cad/net/).

### 2. Répertoire de documents

 Créez un répertoire désigné pour vos documents. Dans l'exemple fourni, la variable`MyDir` représente le répertoire des documents.

## Importer des espaces de noms

Maintenant que vous avez configuré les prérequis, importons les espaces de noms nécessaires dans votre application .NET pour utiliser les fonctionnalités d'Aspose.CAD.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## Étape 1 : Charger le fichier IFC

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

 Dans cette étape, nous initialisons le Aspose.CAD`IfcImage` objet et chargez-y le fichier IFC.

## Étape 2 : définir les options de rastérisation

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

Définissez les options de rastérisation pour configurer la largeur et la hauteur de la page pour la sortie PNG.

## Étape 3 : Définir les options PNG

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

Créez des options PNG et associez les options de rastérisation précédemment définies.

## Étape 4 : Spécifier le chemin de sortie

```csharp
    // Définir également le chemin de sortie
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

Définissez le chemin de sortie du fichier PNG, en vous assurant qu'il porte le même nom que le fichier source avec l'extension ".png". Enfin, enregistrez l'image convertie.

## Conclusion

Grâce à ces étapes simples, vous avez réussi à exporter un fichier IFC au format PNG à l'aide d'Aspose.CAD pour .NET. Cet outil polyvalent simplifie le processus de conversion CAO, le rendant accessible aux développeurs et aux ingénieurs.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour .NET sur macOS ou Linux ?

A1 : Non, Aspose.CAD pour .NET est spécifiquement conçu pour les environnements Windows.

### Q2 : Une licence temporaire est-elle disponible à des fins de test ?

 A2 : Oui, vous pouvez obtenir une licence temporaire auprès de[ici](https://purchase.aspose.com/temporary-license/) pour évaluation.

### Q3 : Comment puis-je obtenir de l'aide pour Aspose.CAD ?

 A3 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien et les discussions de la communauté.

### Q4 : Où puis-je trouver une documentation complète ?

 A4 : Reportez-vous au[Documentation Aspose.CAD](https://reference.aspose.com/cad/net/) pour des informations détaillées et des exemples.

### Q5 : Que faire si je rencontre des problèmes lors de l'installation ?

 A5 : Vérifiez la documentation ou demandez de l'aide sur le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
