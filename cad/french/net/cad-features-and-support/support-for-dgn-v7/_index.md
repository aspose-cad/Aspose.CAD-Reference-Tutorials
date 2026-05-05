---
date: 2026-03-29
description: Apprenez à convertir le DGN en JPEG avec Aspose.CAD pour .NET, offrant
  une prise en charge complète du DGN V7 et vous permettant de convertir facilement
  les fichiers CAD en images raster.
linktitle: Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Convertir DGN en JPEG avec Aspose.CAD pour .NET – prise en charge de la V7
url: /fr/net/cad-features-and-support/support-for-dgn-v7/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DGN en JPEG avec Aspose.CAD pour .NET – Prise en charge V7

## Introduction

Dans ce tutoriel, vous apprendrez comment **convertir DGN en JPEG** avec Aspose.CAD pour .NET, en tirant parti de la prise en charge complète du DGN V7 par la bibliothèque. Convertir des fichiers DGN en images raster telles que JPEG est une exigence courante lorsque vous devez intégrer des dessins CAD dans des pages Web, des applications mobiles ou des outils de reporting. Aspose.CAD vous permet également de **convertir CAD en raster** efficacement, vous offrant une flexibilité dans la façon dont vous présentez les données de conception.

## Réponses rapides
- **Quel est le sujet du tutoriel ?** Conversion d'un fichier DGN V7 en image raster JPEG à l'aide d'Aspose.CAD pour .NET.  
- **Quelle version de la bibliothèque est requise ?** Toute version récente d'Aspose.CAD pour .NET incluant la prise en charge du DGN V7.  
- **Ai-je besoin d'une licence ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production.  
- **Puis-je modifier la taille de sortie ?** Oui – les options de rasterisation vous permettent de définir la largeur, la hauteur et le facteur d'échelle de la page.  
- **Le JPEG est-il le seul format de sortie ?** Non – Aspose.CAD prend en charge de nombreux formats raster (PNG, BMP, TIFF, etc.).

## Qu'est-ce que le DGN V7 ?
DGN (Design) est un format de fichier créé à l'origine par Bentley Systems pour MicroStation. La version 7 ajoute une géométrie et des métadonnées plus riches, ce qui en fait un choix populaire pour les projets de génie civil et d'infrastructures. Aspose.CAD pour .NET peut lire directement les fichiers DGN V7, exposant leur contenu sous forme d'objets `CadImage` que vous pouvez rasteriser ou convertir en d'autres formats.

## Pourquoi convertir DGN en JPEG ?
- **Web‑ready :** Les images JPEG sont légères et s'affichent instantanément dans les navigateurs sans nécessiter de plugins spéciaux.  
- **Cross‑platform :** Le JPEG peut être visualisé sur n'importe quel appareil, ce qui le rend idéal pour partager des dessins CAD avec des parties prenantes non techniques.  
- **Simplified workflows :** La conversion en format raster élimine le besoin de visionneuses spécifiques à la CAD dans les processus en aval.

## Prérequis
Avant de plonger dans l'implémentation, assurez-vous de disposer de ce qui suit :

- **Aspose.CAD for .NET** – téléchargez-le depuis le [website](https://releases.aspose.com/cad/net/).  
- **Environnement de développement** – Visual Studio (ou tout IDE supportant .NET).  

Avoir ces éléments prêts vous permettra de suivre les étapes sans interruption.

## Importer les espaces de noms
Commencez par importer les espaces de noms nécessaires à la gestion de CadImage et à la rasterisation.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Étape 1 : Charger le fichier DGN
Chargez le fichier DGN source dans un objet `CadImage`. Remplacez le chemin de substitution par le dossier contenant votre fichier DGN.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Subsequent steps will be placed here.
}
```

## Étape 2 : Configurer les options de rasterisation
Définissez la manière dont le dessin DGN doit être rasterisé. Vous pouvez contrôler les dimensions de sortie et le comportement de mise à l'échelle.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## Étape 3 : Définir les options de rasterisation vectorielle
Créez un objet `JpegOptions` (ou toute autre option de format raster) et associez les paramètres de rasterisation.

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## Étape 4 : Enregistrer l'image rasterisée
Enfin, exportez le dessin DGN vers un fichier JPEG en utilisant la méthode `Save`.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

Lorsque le code s'exécute correctement, vous trouverez une représentation JPEG du dessin DGN V7 original dans le dossier spécifié.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Fichier non trouvé** | Vérifiez que `MyDir` se termine par un séparateur de chemin (`\\` ou `/`) et que le nom du fichier est correct. |
| **Image de sortie vide** | Assurez-vous que `NoScaling` est correctement défini ; réglez-le sur `false` si vous souhaitez que le dessin remplisse la page. |
| **Entités non prises en charge** | Aspose.CAD prend en charge la plupart des entités DGN, mais les objets très anciens ou personnalisés peuvent être ignorés. Consultez le journal de conversion pour les avertissements. |

## Questions fréquemment posées

### Q1 : Aspose.CAD est‑il compatible avec les dernières spécifications DGN V7 ?
**A:** Oui, Aspose.CAD prend pleinement en charge le DGN V7, en gérant à la fois la géométrie et les métadonnées selon les dernières normes.

### Q2 : Puis‑je personnaliser les options de rasterisation pour la conversion de fichiers DGN ?
**A:** Absolument. La classe `CadRasterizationOptions` vous permet d'ajuster la taille de la page, l'échelle, l'épaisseur des lignes, la couleur d'arrière‑plan, etc.

### Q3 : Existe‑t‑il d'autres formats de sortie pris en charge en plus du JPEG ?
**A:** Oui, Aspose.CAD peut exporter vers PNG, BMP, TIFF et plusieurs autres formats raster. Utilisez simplement la classe `*Options` correspondante (par ex., `PngOptions`).

### Q4 : Comment obtenir de l'aide pour les questions liées à Aspose.CAD ?
**A:** Consultez le [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pour le support communautaire et les réponses officielles.

### Q5 : Existe‑t‑il une version d'essai gratuite pour Aspose.CAD pour .NET ?
**A:** Oui, vous pouvez télécharger une version d'essai depuis [here](https://releases.aspose.com/).

---

**Dernière mise à jour :** 2026-03-29  
**Testé avec :** Aspose.CAD 24.12 for .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}