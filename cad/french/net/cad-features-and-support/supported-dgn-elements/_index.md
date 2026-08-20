---
date: 2026-03-29
description: Apprenez à convertir DGN en PNG à l'aide d'Aspose.CAD pour .NET. Ce guide
  couvre également la prise en charge des formats de fichiers CAD et l'ensemble complet
  des éléments DGN pris en charge.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Convertir DGN en PNG avec Aspose.CAD pour .NET
url: /fr/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DGN en PNG avec Aspose.CAD pour .NET

## Introduction

Êtes-vous un développeur .NET cherchant à **convertir DGN en PNG** de manière fluide ? Aspose.CAD pour .NET offre une solution robuste pour gérer les fichiers DGN efficacement. Dans ce tutoriel, nous explorerons les éléments DGN pris en charge, vous guidant à travers le processus de travail avec Aspose.CAD pour .NET tout en vous montrant exactement comment exporter ces éléments en images PNG.

## Réponses rapides
- **Que fait Aspose.CAD ?** Il lit, modifie et convertit les fichiers CAD/BIM (y compris DGN) en formats raster tels que PNG.  
- **Puis-je convertir des éléments DGN 2D et 3D ?** Oui – les entités 2‑D et 3‑D sont prises en charge.  
- **Quelles versions de .NET sont requises ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Ai-je besoin d'une licence pour les tests ?** Un essai gratuit est disponible ; une licence est requise pour la production.  
- **Où puis-je obtenir la bibliothèque ?** Téléchargez-la depuis le site officiel d'Aspose (lien ci-dessous).

## Qu'est-ce que « convertir DGN en PNG » ?
Convertir DGN en PNG signifie rendre le dessin DGN vectoriel (2‑D ou 3‑D) sous forme de format d'image raster (PNG). Cela est utile lorsque vous devez afficher des dessins CAD sur le Web, les intégrer dans des rapports ou générer des miniatures sans nécessiter de visualiseur CAD.

## Pourquoi utiliser Aspose.CAD pour .NET pour la prise en charge des formats de fichiers CAD ?
- **Prise en charge complète des formats de fichiers CAD** – DGN, DWG, DXF, DWF, et plus.  
- **Aucune dépendance externe** – bibliothèque .NET pure, aucune installation CAD native.  
- **Rendu haute fidélité** – préserve les épaisseurs de ligne, les couleurs et la géométrie 3‑D.  
- **Traitement par lots** – boucle facilement sur de nombreux fichiers dans une application côté serveur.

## Prérequis

- Connaissances de base en programmation .NET.  
- Visual Studio installé sur votre machine.  
- Bibliothèque Aspose.CAD pour .NET, que vous pouvez télécharger [ici](https://releases.aspose.com/cad/net/).

## Importer les espaces de noms

Pour démarrer votre projet, importez les espaces de noms nécessaires dans votre application .NET. Cette étape garantit que vous avez accès aux fonctionnalités fournies par Aspose.CAD pour .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Comment convertir DGN en PNG

Voici un guide étape par étape qui vous montre comment charger un fichier DGN, parcourir ses éléments, gérer les entités 2‑D et 3‑D, puis exporter le résultat sous forme d'image raster PNG.

### Étape 1 : Charger le fichier DGN

Commencez par charger un fichier DGN existant en tant que `DgnImage` dans votre application .NET.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Étape 2 : Parcourir les éléments DGN

Parcourez les éléments DGN à l'aide d'une boucle `foreach`. Aspose.CAD pour .NET fournit une variété de types d'éléments DGN avec lesquels vous pouvez travailler.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Étape 3 : Gérer les entités 2‑D précédemment prises en charge

Ces entités sont désormais également prises en charge pour le rendu 3‑D. L'instruction switch vous permet de diriger la logique en fonction du type d'élément.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Étape 4 : Gérer les entités 3‑D prises en charge

Aspose.CAD ajoute une prise en charge complète de plusieurs éléments DGN 3‑D. Étendez le switch pour les traiter selon les besoins.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Étape 5 : Exporter et enregistrer en PNG

Après toute manipulation nécessaire, exportez le dessin DGN vers une image raster PNG et enregistrez‑la dans le répertoire spécifié.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Astuce :** Utilisez `Image.Save` avec `new PngOptions()` pour contrôler la résolution, la couleur d'arrière‑plan et d'autres paramètres spécifiques au PNG.

## Aperçu de la prise en charge des formats de fichiers CAD

Aspose.CAD pour .NET ne se limite pas à DGN. Il prend également en charge DWG, DXF, DWF et de nombreux autres formats CAD, vous offrant une API unique pour gérer un large éventail de dessins d'ingénierie. Cela le rend idéal pour les projets qui nécessitent une **prise en charge des formats de fichiers CAD** sur plusieurs normes.

## Problèmes courants & solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| **L'image apparaît vide** | Exporté avec un DPI nul | Spécifiez `ResolutionX` et `ResolutionY` dans `PngOptions`. |
| **Géométrie 3‑D manquante** | Type d'élément non géré dans le switch | Ajoutez le cas `DgnElementType` manquant et rendez-le en conséquence. |
| **Mémoire insuffisante sur les gros fichiers** | Chargement du fichier complet en une fois | Traitez les éléments par lots ou utilisez le streaming lorsque possible. |

## Questions fréquentes

### Q1 : Où puis‑je trouver la documentation d'Aspose.CAD pour .NET ?
R1 : Vous pouvez trouver la documentation [ici](https://reference.aspose.com/cad/net/).

### Q2 : Comment télécharger Aspose.CAD pour .NET ?
R2 : Vous pouvez télécharger la bibliothèque [ici](https://releases.aspose.com/cad/net/).

### Q3 : Existe‑t‑il un essai gratuit disponible pour Aspose.CAD pour .NET ?
R3 : Oui, vous pouvez accéder à l'essai gratuit [ici](https://releases.aspose.com/).

### Q4 : Où puis‑je obtenir des licences temporaires pour Aspose.CAD pour .NET ?
R4 : Les licences temporaires sont disponibles [ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Besoin d'aide ou avez‑vous des questions ?
R5 : Visitez le [forum d'assistance](https://forum.aspose.com/c/cad/19) de la communauté Aspose.CAD pour .NET.

---

**Dernière mise à jour :** 2026-03-29  
**Testé avec :** Aspose.CAD pour .NET 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}