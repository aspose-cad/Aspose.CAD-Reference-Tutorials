---
title: Création d'un seul PDF avec différentes mises en page - Guide Aspose.CAD
linktitle: Création d'un seul PDF avec différentes mises en page
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Créez un seul PDF avec différentes mises en page à l'aide d'Aspose.CAD pour .NET. Suivez notre guide étape par étape pour une intégration transparente et une génération efficace de PDF.
type: docs
weight: 13
url: /fr/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## Introduction

Cherchez-vous à générer un seul document PDF à partir d'un dessin CAO avec différentes mises en page à l'aide d'Aspose.CAD pour .NET ? Ce guide étape par étape vous guidera tout au long du processus, vous aidant à réaliser une intégration transparente et une création PDF efficace. Aspose.CAD pour .NET fournit des fonctionnalités puissantes pour manipuler les dessins CAO par programme, et dans ce didacticiel, nous nous concentrerons sur la création d'un seul PDF avec différentes mises en page.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir les prérequis suivants :

-  Aspose.CAD pour .NET : assurez-vous que Aspose.CAD pour .NET est installé. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/cad/net/).

- Environnement de développement : mettre en place un environnement de développement .NET et avoir une compréhension de base de la programmation C#.

## Importer des espaces de noms

Dans votre projet C#, incluez les espaces de noms nécessaires pour exploiter les fonctionnalités d'Aspose.CAD for .NET :

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Étape 1 : Charger l'image CAO

```csharp
// Le chemin d'accès au répertoire des documents.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Votre code pour l'étape 1 va ici
}
```

## Étape 2 : Personnaliser les options de rastérisation

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Tailles personnalisées pour plusieurs mises en page
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Étape 3 : Définir les options PDF

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## Étape 4 : Enregistrer au format PDF

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Vous avez maintenant créé avec succès un seul document PDF avec différentes mises en page à l'aide d'Aspose.CAD pour .NET. N'hésitez pas à explorer plus de fonctionnalités et à personnaliser le code en fonction de vos besoins spécifiques.

## Conclusion

Dans ce didacticiel, nous avons couvert le processus de création d'un seul PDF à partir d'un dessin CAO avec différentes mises en page à l'aide d'Aspose.CAD pour .NET. Cette puissante bibliothèque simplifie les tâches de manipulation CAO et offre une flexibilité pour divers scénarios.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour .NET avec d’autres formats de CAO ?

A1 : Oui, Aspose.CAD pour .NET prend en charge divers formats de CAO tels que DWG, DXF, DGN, etc.

### Q2 : Existe-t-il un essai gratuit ?

 A2 : Oui, vous pouvez explorer un essai gratuit[ici](https://releases.aspose.com/).

### Q3 : Comment puis-je obtenir une assistance pour Aspose.CAD pour .NET ?

 A3 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien de la communauté.

### Q4 : Où puis-je trouver une documentation détaillée ?

 A4 : Se référer à la documentation[ici](https://reference.aspose.com/cad/net/).

### Q5 : Puis-je acheter une licence pour Aspose.CAD pour .NET ?

 A5 : Oui, vous pouvez acheter une licence[ici](https://purchase.aspose.com/buy).