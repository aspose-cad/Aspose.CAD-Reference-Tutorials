---
date: 2026-08-23
description: Apprenez à créer un viewport dwg c# en utilisant Aspose.CAD. Ce guide
  couvre le chargement d'un fichier DWG, la configuration de la rasterisation, la
  définition d'un viewport et l'enregistrement du résultat au format PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: Rendu de documents DWG en C#
og_description: Apprenez à créer un viewport dwg c# en utilisant Aspose.CAD dans .NET.
  Ce guide étape par étape montre le chargement, la rasterisation, la définition de
  viewports et l'enregistrement au format PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Comment créer un viewport dwg c# avec Aspose.CAD pour .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Comment créer un viewport dwg c# avec Aspose.CAD pour .NET
url: /fr/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rendu de documents DWG en C# – créer un viewport dwg c# tutoriel

## Introduction

Dans ce tutoriel complet, vous apprendrez à **créer viewport dwg c#** avec Aspose.CAD et à rendre un fichier DWG en PDF. Que vous ayez besoin d’extraire une mise en page spécifique, de générer une feuille imprimable ou d’intégrer une vue CAD dans un rapport, le contrôle du viewport vous offre une précision de rendu. Aspose.CAD prend en charge **plus de 20 formats CAD** et peut traiter des fichiers contenant des milliers d’entités sans charger le document complet en mémoire, ce qui le rend idéal pour des applications .NET haute performance.

## Réponses rapides
- **Quelle est la première étape ?** Charger le fichier DWG avec `CadImage.Load`.
- **Quelle classe définit la zone de visualisation ?** `Viewport` dans `CadRasterizationOptions`.
- **Puis-je sortir en PDF ?** Oui, en utilisant `PdfOptions` après la rasterisation.
- **Ai-je besoin d’une licence pour la production ?** Une licence commerciale est requise ; un essai gratuit suffit pour l’évaluation.
- **.NET Core est‑il pris en charge ?** Absolument – Aspose.CAD fonctionne avec .NET Framework, .NET Core et .NET 5/6.

## Prérequis

Avant de plonger dans le code, assurez‑vous d’avoir :

- Des connaissances de base en programmation C#.
- Visual Studio (toute version récente) installé.
- La bibliothèque Aspose.CAD ajoutée à votre projet. Vous pouvez la télécharger depuis la [page de téléchargement Aspose.CAD](https://releases.aspose.com/cad/net/).
- Un fichier DWG d’exemple tel que **Bottom_plate.dwg** pour suivre le tutoriel.

## Importer les espaces de noms

Ajoutez les directives `using` requises en haut de votre fichier C# afin que le compilateur puisse localiser les types Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Maintenant que l’environnement est prêt, parcourons l’implémentation étape par étape.

## Comment créer un viewport dwg c# ?

Pour créer un viewport personnalisé, chargez d’abord le fichier DWG dans un objet `CadImage`, puis configurez `CadRasterizationOptions` avec la mise en page et l’échelle souhaitées. Définissez la région que vous voulez afficher, créez un `CadVportTableObject` avec le centre, la hauteur et le rapport d’aspect calculés, remplacez le viewport actif, définissez les options PDF éventuelles, puis enregistrez le résultat.

## Étape 1 : charger le fichier dwg

`CadImage.Load` charge un fichier DWG dans un objet `CadImage`, qui représente le dessin CAD en mémoire.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Étape 2 : configurer les options de rasterisation

`CadRasterizationOptions` spécifie comment le dessin CAD est rasterisé, y compris la sélection de la mise en page, l’échelle et la taille de sortie.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Étape 3 : définir la région à dessiner

`Point` définit les coordonnées X et Y du coin supérieur gauche de la région à rendre.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Étape 4 : créer un nouveau viewport

`CadVportTableObject` représente un objet viewport qui contrôle la zone visible et le rapport d’aspect du dessin rendu.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Étape 5 : remplacer le viewport actif

La boucle remplace le viewport actif par celui nouvellement créé afin d’appliquer les paramètres de vue personnalisés.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Étape 6 : configurer les options PDF

`PdfOptions` configure les paramètres de sortie PDF tels que la compression et les métadonnées.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 7 : enregistrer le dwg rendu en PDF

`image.Save` écrit l’image rendue dans un fichier en utilisant les options de format spécifiées.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Pourquoi utiliser un viewport personnalisé lors du rendu de DWG ?

Un viewport personnalisé vous permet d’isoler une mise en page ou une région spécifique, réduisant la taille du fichier et améliorant la vitesse de rendu. Aspose.CAD peut rendre un DWG de 300 pages en moins de 2 secondes lorsqu’un viewport ciblé est utilisé, contre plusieurs secondes de plus pour le rendu complet du dessin.

## Problèmes courants et solutions

- **Sortie blanche** – Assurez‑vous que les coordonnées du viewport se trouvent à l’intérieur des limites du dessin ; utilisez `CadImage.Size` pour vérifier les bordures.
- **Couches manquantes** – Définissez `CadRasterizationOptions.Layouts` avec le nom de la mise en page correcte ; sinon la mise en page par défaut peut être vide.
- **Ralentissement des performances** – Désactivez l’anti‑aliasing dans `CadRasterizationOptions` si vous avez seulement besoin d’un aperçu rapide.

## Questions fréquemment posées

### Q1 : Puis-je utiliser Aspose.CAD avec d’autres formats de fichiers CAD ?

R1 : Oui, Aspose.CAD prend en charge divers formats, dont DWG, DXF, DWF et plus de 20 types CAD supplémentaires.

### Q2 : Aspose.CAD est‑il compatible avec .NET Core ?

R2 : Oui, Aspose.CAD fonctionne avec .NET Framework, .NET Core et les dernières versions de .NET.

### Q3 : Comment gérer différentes mises en page dans un fichier DWG ?

R3 : Spécifiez la mise en page souhaitée à l’aide de la propriété `Layouts` de `CadRasterizationOptions` avant le rendu.

### Q4 : Y a‑t‑il des considérations de licence pour l’utilisation d’Aspose.CAD ?

R4 : Pour les détails de licence, consultez la [page de licence Aspose.CAD](https://purchase.aspose.com/buy).

### Q5 : Où puis‑je trouver un support supplémentaire ?

R5 : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour obtenir de l’aide communautaire et des discussions.

### Q6 : Puis‑je rendre directement en PNG au lieu de PDF ?

R6 : Oui, remplacez `PdfOptions` par `PngOptions` et appelez `image.Save("output.png", pngOptions)`.

### Q7 : Comment intégrer l’image rendue dans une application Windows Forms ?

R7 : Chargez l’image enregistrée dans un contrôle `PictureBox` à l’aide de `Image.FromFile("output.png")`.

## Conclusion

Vous savez maintenant comment **créer viewport dwg c#** et rendre un fichier DWG en PDF (ou d’autres formats raster) à l’aide d’Aspose.CAD. En maîtrisant la manipulation du viewport, vous obtenez un contrôle fin de la sortie visuelle, essentiel pour générer des dessins d’ingénierie précis, des rapports ou des vignettes. Explorez les paramètres de rasterisation supplémentaires, expérimentez différents formats de sortie et intégrez le code dans des services .NET plus vastes ou des utilitaires de bureau.

---

**Dernière mise à jour :** 2026-08-23  
**Testé avec :** Aspose.CAD 24.11 for .NET  
**Auteur :** Aspose

## Tutoriels associés

- [Comment définir le viewport lors de la conversion de DWG en PDF avec coordonnées en C# - Tutoriel Aspose.CAD](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Apprendre à définir les options de rasterisation CAD – Exporter des mises en page spécifiques en PDF avec Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Comment convertir DWG en PDF et images rasterisées en utilisant Aspose.CAD pour .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}