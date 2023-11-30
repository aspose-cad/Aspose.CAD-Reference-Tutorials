---
title: Ajout de filigranes aux dessins CAO - Guide Aspose.CAD
linktitle: Ajout de filigranes aux dessins CAO
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Améliorez vos dessins CAO avec des filigranes professionnels à l'aide d'Aspose.CAD pour .NET. Suivez notre guide étape par étape pour des conceptions personnalisées et attrayantes.
type: docs
weight: 11
url: /fr/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## Introduction

Cherchez-vous à améliorer vos dessins CAO en ajoutant des filigranes professionnels ? Aspose.CAD pour .NET fournit une solution robuste pour intégrer de manière transparente des filigranes dans vos fichiers CAO. Dans ce guide étape par étape, nous vous guiderons tout au long du processus d'ajout de filigranes à l'aide d'Aspose.CAD, garantissant que vos dessins transmettent non seulement des informations critiques, mais portent également votre marque unique.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir les éléments suivants :
-  Aspose.CAD pour .NET : assurez-vous que la bibliothèque Aspose.CAD est installée. Vous pouvez le télécharger[ici](https://releases.aspose.com/cad/net/).
- Votre répertoire de documents : configurez un répertoire pour stocker vos dessins CAO.
Commençons maintenant par ajouter des filigranes à vos dessins CAO !

## Importer des espaces de noms

Commencez par importer les espaces de noms nécessaires dans votre projet .NET :

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Étape 1 : Charger le dessin CAO

```csharp
// Le chemin d'accès au répertoire des documents.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Étape 2 : Ajouter un filigrane en tant que MTEXT

```csharp
// Ajouter un nouveau TEXTEMT
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## Étape 3 : Ou ajouter un filigrane sous forme de texte

```csharp
// Vous pouvez également ajouter une entité plus simple comme Text
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## Étape 4 : Exporter au format PDF

```csharp
// Exportez le dessin CAO avec filigrane au format PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Répétez ces étapes pour différents dessins et vous obtiendrez des fichiers CAO filigranés d'aspect professionnel en un rien de temps !

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment ajouter des filigranes à vos dessins CAO à l'aide d'Aspose.CAD for .NET. Ce processus simple mais puissant vous permet de personnaliser vos conceptions tout en préservant l'intégrité de vos dessins techniques.

## FAQ

### Q1 : Puis-je personnaliser l’apparence du filigrane ?

A1 : Oui, vous pouvez personnaliser le texte, la police, la taille et la position du filigrane selon vos préférences.

### Q2 : Aspose.CAD est-il compatible avec différents formats de fichiers CAO ?

A2 : Aspose.CAD prend en charge divers formats de fichiers CAO, notamment DWG et DXF, garantissant une large compatibilité.

### Q3 : Puis-je ajouter plusieurs filigranes à un seul dessin CAO ?

A3 : Absolument ! Vous pouvez ajouter autant de filigranes que nécessaire, offrant ainsi une flexibilité pour différents cas d'utilisation.

### Q4 : Aspose.CAD propose-t-il un essai gratuit ?

A4 : Oui, vous pouvez explorer les fonctionnalités d'Aspose.CAD avec un essai gratuit. L'obtenir[ici](https://releases.aspose.com/).

### Q5 : Où puis-je trouver de l'assistance pour Aspose.CAD ?

 A5 : Pour toute question ou assistance, visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).