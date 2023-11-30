---
title: Importation d'images dans des fichiers DWG avec C# - Guide Aspose.CAD
linktitle: Importation d'images dans des fichiers DWG avec C#
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Apprenez à importer des images dans des fichiers DWG en utilisant C# avec Aspose.CAD pour .NET. Suivez notre guide étape par étape pour une intégration transparente.
type: docs
weight: 11
url: /fr/net/image-manipulation-and-rendering/importing-images-into-dwg/
---
## Introduction

Dans le domaine de la conception assistée par ordinateur (CAO), l'incorporation d'images dans des fichiers DWG est une tâche courante et cruciale. Aspose.CAD for .NET fournit un ensemble d'outils puissants pour rationaliser ce processus, le rendant accessible aux développeurs C#. Dans ce didacticiel, nous verrons étape par étape comment importer des images dans des fichiers DWG.

## Conditions préalables

Avant de plonger dans le guide, assurez-vous d'avoir les éléments suivants :

- Connaissance de base de la programmation C#.
-  Aspose.CAD pour .NET installé. Vous pouvez le télécharger[ici](https://releases.aspose.com/cad/net/).
- Un environnement de développement mis en place.

## Importer des espaces de noms

Assurez-vous d'inclure les espaces de noms nécessaires dans votre projet C# :

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Étape 1 : Configurez votre répertoire de documents

```csharp
string MyDir = "Your Document Directory";
```

## Étape 2 : charger le fichier DWG

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## Étape 3 : définir les propriétés de l'image

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## Étape 4 : Définir le point d'insertion et les vecteurs

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## Étape 5 : Créer et configurer l'image raster

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## Étape 6 : ajouter une image au fichier DWG

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## Étape 7 : Enregistrer au format PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## Conclusion

L'intégration d'images dans des fichiers DWG à l'aide de C# et Aspose.CAD pour .NET est un processus transparent, permettant aux développeurs d'améliorer sans effort leurs projets de CAO avec des éléments visuels.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour .NET avec d’autres langages de programmation ?

A1 : Aspose.CAD est principalement conçu pour .NET, mais Aspose fournit des bibliothèques pour divers langages de programmation.

### Q2 : Un essai gratuit est-il disponible pour Aspose.CAD pour .NET ?

 A2 : Oui, vous pouvez explorer un essai gratuit[ici](https://releases.aspose.com/).

### Q3 : Où puis-je trouver une documentation détaillée pour Aspose.CAD ?

 A3 : La documentation est disponible[ici](https://reference.aspose.com/cad/net/).

### Q4 : Comment puis-je obtenir une licence temporaire pour Aspose.CAD pour .NET ?

 A4 : Visite[ce lien](https://purchase.aspose.com/temporary-license/) pour obtenir un permis temporaire.

### Q5 : Existe-t-il des forums communautaires pour le support d'Aspose.CAD ?

 A5 : Oui, vous pouvez demander du soutien et vous engager auprès de la communauté.[ici](https://forum.aspose.com/c/cad/19).