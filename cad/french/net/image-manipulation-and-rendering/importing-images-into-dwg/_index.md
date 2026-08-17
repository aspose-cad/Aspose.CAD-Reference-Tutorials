---
date: 2026-08-17
description: Apprenez comment ajouter une image aux fichiers dwg en utilisant C# et
  Aspose.CAD pour .NET. Ce guide vous accompagne dans l'importation d'images, la définition
  des points d'insertion et l'exportation vers PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Importation d'images dans les fichiers DWG avec C#
og_description: Apprenez comment ajouter une image aux fichiers dwg en utilisant C#.
  Ce tutoriel couvre l'importation d'images, la définition des points d'insertion
  et la conversion de dwg en PDF avec Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Comment ajouter une image aux fichiers dwg avec C# en utilisant Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: Comment ajouter une image aux fichiers dwg avec C# en utilisant Aspose.CAD
url: /fr/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajouter une image aux fichiers dwg avec C# en utilisant Aspose.CAD

## Introduction

Ajouter une image à un fichier DWG est une exigence courante lorsque vous devez enrichir les dessins CAD avec des logos, des photos ou des graphiques raster. Dans ce tutoriel, vous apprendrez comment **ajouter une image à un dwg** de manière programmatique en utilisant C# et Aspose.CAD pour .NET, puis éventuellement convertir le résultat en PDF. Les étapes sont détaillées afin que vous puissiez copier‑coller chaque section dans votre propre projet.

## Réponses rapides
- **Quelle bibliothèque gère la tâche ?** Aspose.CAD pour .NET.
- **Puis‑je intégrer des fichiers PNG ?** Oui – PNG, JPEG, BMP et autres formats raster sont pris en charge.
- **Ai‑je besoin d’une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.
- **L’exportation PDF est‑elle supportée ?** Absolument – vous pouvez convertir le DWG mis à jour en PDF en une seule ligne.
- **Quelles versions .NET sont compatibles ?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Qu’est‑ce qu’un fichier DWG ?

Un fichier DWG est le format binaire natif des dessins Autodesk AutoCAD, stockant la géométrie vectorielle, les calques et les métadonnées. Il est largement utilisé dans l’architecture, l’ingénierie et la construction, et Aspose.CAD peut lire et écrire ce format sans nécessiter l’installation d’AutoCAD.

## Pourquoi ajouter une image à un dwg avec Aspose.CAD ?

Aspose.CAD prend en charge **plus de 50 formats d’entrée et de sortie**, peut traiter des fichiers de plus de 500 Mo sans charger l’ensemble du document en mémoire, et fournit une API déterministe qui fonctionne dans des environnements serveur sans interface graphique. Cela rend le traitement en masse des dessins DWG rapide et fiable.

## Prérequis
- Connaissances de base en programmation C#.
- Aspose.CAD pour .NET installé. Vous pouvez le télécharger depuis la [page de téléchargement d’Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/). Vous pouvez également explorer d’autres produits Aspose sur la [page des releases Aspose](https://releases.aspose.com/).
- Un environnement de développement tel que Visual Studio 2022 ou version ultérieure.

## Comment ajouter une image à un dwg avec Aspose.CAD ?

Chargez le DWG cible, créez un objet image raster qui décrit la photo que vous souhaitez intégrer, définissez le point d’insertion et les vecteurs d’échelle, puis attachez l’image au dessin. Enfin, enregistrez le DWG modifié ou exportez‑le directement en PDF. L’ensemble du flux de travail ne nécessite que quelques appels d’API et s’exécute en moins d’une seconde pour des dessins typiques de 2 pages.

### Importer les espaces de noms
Incluez les espaces de noms qui exposent les classes CAD dont vous aurez besoin.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Étape 1 : configurer le répertoire de votre document
Préparez le dossier contenant le DWG source et l’image que vous souhaitez intégrer.

```csharp
string MyDir = "Your Document Directory";
```

### Étape 2 : charger le fichier dwg
La classe `CadImage` représente un dessin DWG et donne accès à ses entités, calques et métadonnées.

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Étape 3 : définir les propriétés de l’image
Créez un objet `Image` qui pointe vers le fichier raster (par ex., PNG) et spécifiez son format.

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Étape 4 : définir le point d’insertion du dwg et les vecteurs
Spécifiez où l’image doit apparaître dans le dessin et comment elle doit être mise à l’échelle. Le point d’insertion est défini par une coordonnée 2‑D, tandis que les vecteurs contrôlent la largeur et la hauteur.

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Étape 5 : créer et configurer l’image raster
Instanciez un objet `RasterImage`, affectez les données de l’image et définissez les options de rendu supplémentaires.

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Étape 6 : ajouter l’image au fichier dwg
Insérez l’image raster configurée dans la collection d’entités du DWG afin qu’elle devienne partie intégrante du dessin.

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Étape 7 : enregistrer en pdf (exporter le dwg vers pdf)
Après avoir intégré l’image, vous pouvez **convertir le dwg en pdf** ou **enregistrer le dwg en pdf** avec un appel unique. Cela est utile pour partager le dessin avec des parties prenantes qui ne possèdent pas de logiciel CAD.

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

## Comment convertir le dwg en pdf après avoir intégré une image ?

Appelez la méthode `Save` sur l’instance `CadImage`, en passant `SaveFormat.Pdf` et éventuellement un objet `PdfOptions` pour contrôler la taille de la page, la rasterisation et les métadonnées. Aspose.CAD préserve l’image raster intégrée, les calques et les épaisseurs de ligne, produisant une représentation PDF fidèle qui peut être ouverte dans n’importe quel visualiseur. Cette conversion s’effectue en une seule ligne de code.

## Problèmes courants et solutions
- **L’image apparaît au mauvais endroit** – vérifiez les coordonnées du point d’insertion et les vecteurs de direction ; ils sont relatifs à l’origine du dessin.
- **Les images volumineuses provoquent des pics de mémoire** – utilisez l’option `Resize` sur l’image raster avant l’insertion, ou travaillez avec une copie à résolution inférieure.
- **L’export PDF perd la qualité vectorielle** – assurez‑vous d’enregistrer avec des `PdfOptions` qui conservent les données vectorielles ; les images raster sont toujours intégrées telles quelles.

## Questions fréquemment posées

**Q : Puis‑je utiliser Aspose.CAD pour .NET avec d’autres langages de programmation ?**  
R : La bibliothèque principale est spécifique à .NET, mais Aspose propose des API équivalentes pour Java, Python et d’autres plateformes.

**Q : Une version d’essai gratuite est‑elle disponible pour Aspose.CAD ?**  
R : Oui, vous pouvez explorer une version d’essai gratuite sur la [page d’essai gratuit d’Aspose](https://releases.aspose.com/).

**Q : Où puis‑je trouver la documentation détaillée d’Aspose.CAD ?**  
R : La documentation est disponible dans la [référence API .NET d’Aspose.CAD](https://reference.aspose.com/cad/net/).

**Q : Comment obtenir une licence temporaire pour Aspose.CAD ?**  
R : Rendez‑vous sur la [page de licence temporaire](https://purchase.aspose.com/temporary-license/) pour obtenir une licence temporaire.

**Q : Existe‑t‑il des forums communautaires pour le support d’Aspose.CAD ?**  
R : Oui, vous pouvez demander de l’aide et interagir avec la communauté dans le [forum communautaire Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Dernière mise à jour :** 2026-08-17  
**Testé avec :** Aspose.CAD 24.11 pour .NET  
**Auteur :** Aspose

## Tutoriels associés

- [Exportation DWG vers PDF ou images raster - Guide Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Exportation DWG vers le format DXF en C# - Tutoriel Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Exportation de mises en page spécifiques vers PDF - Guide Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}