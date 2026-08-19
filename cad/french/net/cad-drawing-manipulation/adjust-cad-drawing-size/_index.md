---
date: 2026-03-19
description: Apprenez à redimensionner les dessins CAD dans .NET avec Aspose.CAD,
  y compris comment mettre à l’échelle les unités de dessin CAD et ajuster la taille
  de la mise en page. Suivez notre guide étape par étape.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Comment redimensionner les dessins CAD avec Aspose.CAD pour .NET
url: /fr/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment redimensionner les dessins CAD avec Aspose.CAD pour .NET

## Introduction

Si vous devez **redimensionner des fichiers CAD** directement depuis votre application .NET, vous êtes au bon endroit. Dans ce tutoriel, nous vous montrerons comment modifier les paramètres d’unité CAD, mettre à l’échelle les dimensions d’un dessin CAD et ajuster la taille du CAD de manière programmatique en utilisant Aspose.CAD pour .NET. À la fin du guide, vous disposerez d’une solution solide, prête pour la production, pour redimensionner tout format CAD pris en charge.

## Réponses rapides
- **Quelle bibliothèque est requise ?** Aspose.CAD for .NET  
- **Puis-je changer le type d’unité ?** Oui – set `UnitType` in `CadRasterizationOptions`  
- **Une licence est‑elle nécessaire pour la production ?** Une licence Aspose.CAD valide est requise pour une utilisation hors période d’essai  
- **Quel format d’image l’exemple exporte‑t‑il ?** BMP (mais tout format raster pris en charge fonctionne)  
- **Combien de lignes de code ?** Moins de 30 lignes pour une opération de redimensionnement complète  

## Qu’est‑ce que « redimensionner CAD » en pratique ?

Redimensionner un dessin CAD signifie convertir les données vectorielles en une image raster à une échelle ou une unité spécifique (par ex., centimètres, pouces). Cela est utile lorsque vous devez intégrer des dessins dans des rapports, générer des vignettes ou intégrer des visuels CAD dans des pages web.

## Pourquoi ajuster la taille du CAD avec Aspose.CAD ?

- **Pas de logiciel CAD externe** – tout s’exécute à l’intérieur de votre code .NET.  
- **Contrôle fin** sur les unités, les mises en page et les options de rasterisation.  
- **Support multi‑format** – le même code fonctionne pour DWG, DXF, DWF, et plus encore.  

## Prerequisites

Avant de commencer, assurez-vous d’avoir :

- Bibliothèque Aspose.CAD pour .NET : téléchargez et installez la bibliothèque depuis la [page de téléchargement d’Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).  
- Dessins CAD d’exemple : un fichier tel que `sample.dwg` placé dans le répertoire de documents de votre projet.  

## Importer les espaces de noms

Tout d’abord, importez les espaces de noms qui vous donnent accès aux classes d’Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Étape 1 : Charger le dessin CAD

Chargez le fichier source dans un objet `Image`. Cet objet représente le dessin CAD en mémoire et servira de base à toutes les opérations ultérieures.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Étape 2 : Créer BmpOptions (ou tout autre format raster)

`BmpOptions` indique à Aspose.CAD comment rendre les données vectorielles lorsque vous les enregistrez sous forme de bitmap. Vous pouvez le remplacer par `PngOptions`, `JpegOptions`, etc., selon le format cible.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Étape 3 : Définir CadRasterizationOptions

`CadRasterizationOptions` contient les paramètres principaux pour le redimensionnement, la conversion d’unité et la sélection de mise en page. Le lier à la propriété `VectorRasterizationOptions` de `BmpOptions` garantit que le rasteriseur utilise vos paramètres personnalisés.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Étape 4 : Définir UnitType (modifier l’unité CAD)

Ici nous changeons l’unité CAD de sa valeur par défaut à centimètres. C’est ici que le mot‑clé **change cad unit** apparaît, et il influence directement la taille finale de l’image.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Étape 5 : Choisir les mises en page (définir les mises en page CAD)

Si votre dessin contient plusieurs mises en page (par ex., Model, Sheet1), spécifiez celles que vous souhaitez rasteriser. Sélectionner la bonne mise en page est essentiel lorsque vous **set cad layouts** pour une sortie redimensionnée.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Étape 6 : Exporter en BMP (redimensionner le dessin CAD)

Enfin, enregistrez l’image rasterisée. Le fichier de sortie reflète la nouvelle taille, l’unité et la mise en page que vous avez configurées—complétant ainsi l’opération **resize CAD drawing**.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Vous avez maintenant un fichier BMP qui représente le dessin CAD redimensionné, prêt pour un traitement ou un affichage ultérieur.

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| La sortie est floue | DPI (points par pouce) faible par défaut | Définissez `cadRasterizationOptions.Resolution = 300;` avant l’enregistrement |
| Une mauvaise mise en page apparaît | Erreur de frappe du nom de mise en page | Vérifiez le nom exact de la mise en page à l’aide d’un visualiseur CAD ou de la collection `Layouts` |
| La conversion d’unité semble incorrecte | Mélange d’unités métriques et impériales | Assurez‑vous que `UnitType` correspond au système de mesure souhaité |

## FAQ

### Q1 : Aspose.CAD pour .NET est‑il compatible avec tous les formats CAD ?

A1 : Aspose.CAD pour .NET prend en charge un large éventail de formats CAD, y compris DWG, DXF, DWF, et plus encore. Consultez la [documentation](https://reference.aspose.com/cad/net/) pour la liste complète.

### Q2 : Puis‑je redimensionner plusieurs mises en page simultanément ?

A2 : Oui, vous pouvez redimensionner plusieurs mises en page en ajustant le tableau `Layouts` dans `CadRasterizationOptions`.

### Q3 : Où puis‑je obtenir du support pour Aspose.CAD pour .NET ?

A3 : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire et l’assistance.

### Q4 : Une version d’essai gratuite est‑elle disponible ?

A4 : Oui, vous pouvez explorer un [essai gratuit](https://releases.aspose.com/) pour évaluer les fonctionnalités d’Aspose.CAD pour .NET.

### Q5 : Comment puis‑je obtenir une licence temporaire pour Aspose.CAD pour .NET ?

A5 : Obtenez une licence temporaire à des fins de test [ici](https://purchase.aspose.com/temporary-license/).

## Questions fréquentes

**Q : Comment mettre à l’échelle un dessin CAD sans changer le type d’unité ?**  
A : Ajustez la propriété `Zoom` de `CadRasterizationOptions` (par ex., `cadRasterizationOptions.Zoom = 2.0;`) pour doubler la taille tout en conservant l’unité d’origine.

**Q : Puis‑je exporter vers d’autres formats que le BMP ?**  
A : Absolument. Remplacez `BmpOptions` par `PngOptions`, `JpegOptions`, ou toute autre classe de format raster prise en charge.

**Q : Est‑il possible de traiter par lots un dossier de dessins ?**  
A : Oui. Parcourez les fichiers d’un répertoire, appliquez la même logique de rasterisation et enregistrez chaque sortie avec un nom unique.

---

**Dernière mise à jour :** 2026-03-19  
**Testé avec :** Aspose.CAD for .NET 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}