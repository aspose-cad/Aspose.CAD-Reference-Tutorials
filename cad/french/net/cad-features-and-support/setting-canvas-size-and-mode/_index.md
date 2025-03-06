---
title: Définition de la taille et du mode du canevas dans Aspose.CAD pour .NET
linktitle: Définition de la taille et du mode du canevas
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Explorez le guide étape par étape sur la définition de la taille et du mode du canevas dans Aspose.CAD pour .NET. Optimisez facilement votre rendu CAO à l’aide de ce didacticiel complet.
weight: 16
url: /fr/net/cad-features-and-support/setting-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définition de la taille et du mode du canevas dans Aspose.CAD pour .NET

## Introduction

Êtes-vous prêt à libérer tout le potentiel d'Aspose.CAD pour .NET et à révolutionner votre expérience de rendu CAO ? Dans ce didacticiel étape par étape, nous aborderons les subtilités de la définition de la taille et du mode du canevas à l'aide de la puissante bibliothèque Aspose.CAD. Que vous soyez un développeur chevronné ou débutant, ce guide vous guidera tout au long du processus, vous assurant d'exploiter efficacement les capacités d'Aspose.CAD.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Bibliothèque Aspose.CAD : Téléchargez et installez la bibliothèque Aspose.CAD à partir du[Site Web Aspose.CAD](https://releases.aspose.com/cad/net/).

- Environnement de développement : assurez-vous d'avoir un environnement de développement .NET configuré sur votre ordinateur.

-  Exemple de fichier CAO : pour ce didacticiel, nous utiliserons un exemple de fichier DXF. Vous pouvez en trouver un dans le[Documentation Aspose.CAD](https://reference.aspose.com/cad/net/).

## Importer des espaces de noms

Pour commencer, importez les espaces de noms nécessaires au début de votre application .NET :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Étape 1 : Charger le fichier CAO

Commencez par charger le fichier CAO en utilisant le code suivant :

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Votre code pour les étapes ultérieures sera ici
}
```

## Étape 2 : Créer des options de cadrastérisation

 Créer une instance de`CadRasterizationOptions` et définissez ses propriétés :

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Étape 3 : Créer des options PDF

 Créer une instance de`PdfOptions` et définir son`VectorRasterizationOptions` propriété:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 4 : Exporter au format PDF

Exportez le fichier CAO au format PDF à l'aide des options configurées :

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Étape 5 : Créer des options Tiff

 Créer une instance de`TiffOptions` et définir son`VectorRasterizationOptions` propriété:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 6 : Exporter au format TIFF

Exportez le fichier CAO au format TIFF à l'aide des options configurées :

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Conclusion

Toutes nos félicitations! Vous avez défini avec succès la taille et le mode du canevas dans Aspose.CAD pour .NET. Cette fonctionnalité puissante ouvre un monde de possibilités pour le rendu CAO. Expérimentez différentes options et découvrez tout le potentiel d'Aspose.CAD dans vos applications .NET.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD avec d’autres bibliothèques .NET ?

A1 : Oui, Aspose.CAD s'intègre de manière transparente à d'autres bibliothèques .NET, offrant des fonctionnalités améliorées pour la manipulation CAO.

### Q2 : Un essai gratuit est-il disponible pour Aspose.CAD ?

 A2 : Oui, vous pouvez explorer les fonctionnalités d'Aspose.CAD avec un essai gratuit. Visite[ici](https://releases.aspose.com/) pour commencer.

### Q3 : Comment puis-je obtenir de l'aide pour Aspose.CAD ?

 A3 : Pour obtenir de l'aide et des discussions, visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q4 : Où puis-je trouver une documentation complète pour Aspose.CAD ?

 A4 : Reportez-vous au[Documentation Aspose.CAD](https://reference.aspose.com/cad/net/) pour des informations détaillées et des exemples.

### Q5 : Comment puis-je acheter Aspose.CAD pour .NET ?

 A5 : Pour acheter Aspose.CAD, visitez le[page d'achat](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
