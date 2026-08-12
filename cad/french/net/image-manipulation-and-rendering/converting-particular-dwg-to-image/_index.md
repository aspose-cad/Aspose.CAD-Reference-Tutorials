---
date: 2026-08-12
description: Extraire du texte d'un DWG et convertir un DWG spécifique en image en
  C# à l'aide d'Aspose.CAD pour .NET. Apprenez étape par étape avec des extraits de
  code.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Conversion d'un DWG particulier en image en C#
og_description: Extraire du texte d'un DWG et convertir un DWG spécifique en image
  en C# avec Aspose.CAD. Suivez ce guide concis pour une mise en œuvre rapide.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Extraire du texte d'un DWG et convertir un DWG spécifique en image en C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: Extraire du texte d'un DWG et convertir un DWG spécifique en image en C#
url: /fr/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Conversion d'un DWG particulier en image en C# - Guide Aspose.CAD

## Introduction

Dans les applications d'ingénierie modernes, vous devez souvent **extraire du texte à partir de fichiers DWG** et **convertir des DWG spécifiques en formats image** pour les rapports ou la visualisation. Aspose.CAD pour .NET vous fournit une API complète qui gère les deux tâches sans nécessiter de logiciel CAD externe. Dans ce tutoriel, vous apprendrez comment charger un DWG, filtrer les entités texte, rasteriser le dessin, puis enregistrer le résultat sous forme d'image PDF — le tout en code C# propre.

## Quick answers
- **Quelle est la première étape ?** Chargez le fichier DWG avec `new CadImage("file.dwg")`.  
- **Quelle classe filtre le texte ?** Utilisez `CadEntityFilter` pour sélectionner les entités `Text`.  
- **Comment définir la taille de l'image ?** Définissez `Width` et `Height` sur `CadRasterizationOptions`.  
- **Quel format de sortie est utilisé ?** L'exemple enregistre en PDF, qui intègre l'image raster.  
- **Ai-je besoin d'une licence pour la production ?** Oui – une licence commerciale Aspose.CAD supprime les limites d'évaluation.

## How to extract text from dwg?

Comment extraire le texte d'un dwg ?

Chargez le DWG, appliquez un filtre qui ne sélectionne que les entités texte, puis lisez la propriété `TextString` de chaque entité. Cette approche renvoie chaque annotation, libellé ou texte de cote présent dans le dessin, vous permettant de le réutiliser pour la recherche, l'indexation ou le reporting.

## Why convert specific dwg to image?

Pourquoi convertir un dwg spécifique en image ?

Convertir un DWG en image raster vous permet d'intégrer le dessin dans des documents, pages web ou applications mobiles qui ne peuvent pas rendre les formats CAD natifs. Aspose.CAD traite **plus de 50 formats CAD** et peut rasteriser des dessins de plusieurs centaines de pages tout en utilisant moins de 200 Mo de mémoire, ce qui le rend adapté aux scénarios serveur à haut débit.

## Prerequisites

- Visual Studio (toute version récente) pour compiler et exécuter des projets C#.
- Aspose.CAD pour .NET – assurez‑vous que la bibliothèque est installée. Vous pouvez trouver le lien de téléchargement sur la **[page de téléchargement Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/)**.
- Un fichier DWG avec lequel vous souhaitez travailler ; le fichier d'exemple *visualization_-_conference_room.dwg* est utilisé dans les extraits de code.

## Import namespaces

Les espaces de noms suivants vous donnent accès aux classes CAD de base, aux options de rasterisation et aux aides à la sortie PDF :

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Step 1: load the dwg file

Étape 1 : charger le fichier dwg

Créez une instance `CadImage` en passant le chemin de votre fichier DWG. L'objet `CadImage` représente le dessin complet en mémoire et fournit l'accès à ses calques, entités et métadonnées.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Step 2: filter entities

Étape 2 : filtrer les entités

`CadEntityFilter` vous permet de ne sélectionner que les entités dont vous avez besoin. Dans ce guide, nous le configurons pour conserver les objets **texte**, en éliminant les lignes, cercles et autres géométries que vous ne souhaitez pas dans l'image finale.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Step 3: set rasterization options

Étape 3 : définir les options de rasterisation

`CadRasterizationOptions` contrôle la façon dont le dessin est transformé en bitmap. Vous pouvez définir la taille de sortie, la couleur d'arrière‑plan et la résolution (DPI). L'ancre de définition suivante présente la classe :

La classe `CadRasterizationOptions` spécifie les dimensions de l'image, la résolution et les paramètres de rendu pour convertir les dessins CAD en formats raster.

Définissez la largeur, la hauteur et la couleur d'arrière‑plan souhaitées avant de transmettre les options à l'exportateur PDF.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Step 4: set PDF options

Étape 4 : définir les options PDF

`PdfOptions` regroupe les paramètres de rasterisation avec les fonctionnalités spécifiques au PDF telles que la compression. L'ancre de définition de cette classe apparaît en premier :

`PdfOptions` encapsule les paramètres de génération de PDF, y compris les options de rasterisation qui déterminent comment les données CAD sont rendues à l'intérieur du document PDF.

Attribuez l'instance `CadRasterizationOptions` précédemment créée à la propriété `VectorRasterizationOptions`.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Step 5: save as PDF

Étape 5 : enregistrer en PDF

Enfin, appelez la méthode `Save` sur l'objet `CadImage`, en passant le nom du fichier cible et les `PdfOptions` configurés. Le PDF contiendra une image de haute qualité du dessin filtré.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Common issues and troubleshooting

Problèmes courants et dépannage

- **Texte manquant après filtrage** – Assurez‑vous que le DWG contient réellement des entités `Text` ; certains dessins stockent les annotations sous forme de `MText`. Ajustez le filtre pour inclure `MText` si nécessaire.  
- **Image de sortie vide** – Vérifiez que le DPI de rasterisation est suffisamment élevé (300 DPI est une valeur sûre) et que la couleur d'arrière‑plan n’est pas définie comme transparente lors de la visualisation du PDF.  
- **Erreurs de mémoire insuffisante sur les gros fichiers** – Utilisez la surcharge `LoadOptions` qui active le streaming, ce qui empêche le chargement complet du fichier en mémoire d’un seul coup.

## Frequently asked questions

Questions fréquemment posées

**Q : Aspose.CAD est‑il compatible avec toutes les versions de fichiers DWG ?**  
R : Aspose.CAD prend en charge les versions DWG d’AutoCAD 2000 jusqu’à la dernière version 2024, couvrant plus de 90 % des fichiers créés dans le domaine.

**Q : Puis‑je personnaliser les options de rasterisation pour différentes sorties ?**  
R : Oui – vous pouvez modifier la résolution, le format d’image, l’anti‑aliasing et la couleur d’arrière‑plan pour les cibles PNG, JPEG ou PDF.

**Q : Où puis‑je trouver des exemples supplémentaires et de la documentation ?**  
R : Explorez la documentation complète [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) pour plus d’exemples de code et de détails sur l’API.

**Q : Existe‑t‑il une version d’essai gratuite pour Aspose.CAD ?**  
R : Absolument – vous pouvez télécharger une version d’essai sur la **[page de téléchargement d’essai Aspose](https://releases.aspose.com/)** et évaluer toutes les fonctionnalités sans restriction pendant 30 jours.

**Q : Comment obtenir du support ou rejoindre la communauté ?**  
R : Rejoignez le forum actif [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) où les développeurs partagent des solutions et l’équipe Aspose répond aux questions.

---

**Dernière mise à jour :** 2026-08-12  
**Testé avec :** Aspose.CAD 24.11 pour .NET  
**Auteur :** Aspose

## Related Tutorials

Tutoriels associés

- [Recherche de texte dans les fichiers DWG avec C# - Tutoriel Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Convertir un dessin CAD en image raster avec Aspose.CAD pour .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Rendu de documents DWG en C# - Guide Aspose.CAD](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}