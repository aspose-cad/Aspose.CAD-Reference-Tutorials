---
date: 2026-04-09
description: Apprenez à exporter les calques DWG, à convertir une image DWG et à enregistrer
  le JPEG d’un fichier DWG en utilisant C# avec Aspose.CAD pour .NET. Guide étape
  par étape pour une manipulation efficace des fichiers CAD.
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: Gestion des calques dans les fichiers DWG avec C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Exporter les calques DWG avec C# – Tutoriel Aspose.CAD
url: /fr/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter les calques DWG avec C# – Tutoriel Aspose.CAD

## Introduction

Dans ce guide complet, vous apprendrez **comment exporter les calques DWG** en utilisant C# et la bibliothèque Aspose.CAD. Que vous ayez besoin de **convertir des images DWG**, de contrôler la **visibilité des calques DWG**, ou simplement de **sauvegarder des fichiers DWG JPEG**, les étapes ci‑dessous vous montreront exactement comment le faire efficacement. À la fin du tutoriel, vous disposerez d’un extrait de code prêt à l’emploi qui isole un calque spécifique et le rend sous forme de JPEG de haute qualité.

## Réponses rapides
- **Que signifie « export dwg layers » ?** Cela signifie rasteriser les calques sélectionnés d’un fichier DWG en un format d’image tel que JPEG ou PNG.  
- **Quelle bibliothèque est la meilleure pour cette tâche ?** Aspose.CAD pour .NET offre un support complet sans nécessiter AutoCAD.  
- **Puis‑je exporter plusieurs calques à la fois ?** Oui – transmettez un tableau de noms de calques aux options de rasterisation.  
- **Ai‑je besoin d’une licence pour une utilisation en production ?** Une licence commerciale est requise ; un essai gratuit est disponible pour l’évaluation.  
- **Quels formats de sortie sont pris en charge ?** JPEG, PNG, BMP, TIFF et plusieurs autres via les classes ImageOptions.

## Qu'est‑ce que l'exportation de calques DWG ?
Exporter les calques DWG consiste à prendre les données vectorielles appartenant à un ou plusieurs calques d’un dessin DWG et à les rasteriser en une image bitmap. Cela est utile lorsque vous souhaitez partager une vue d’une partie spécifique d’un dessin sans exposer le fichier CAD complet.

## Pourquoi contrôler la visibilité des calques DWG ?
Contrôler la visibilité des calques vous permet de :

- Créer des actifs visuels propres pour des présentations ou de la documentation.  
- Réduire la taille du fichier en n’exportant que la géométrie nécessaire.  
- Protéger les détails de conception propriétaires en masquant les calques confidentiels.  

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- Des connaissances de base en langage de programmation C#.  
- Visual Studio installé sur votre machine.  
- La bibliothèque Aspose.CAD pour .NET, que vous pouvez télécharger depuis le site [Aspose.CAD website](https://releases.aspose.com/cad/net/).

## Importer les espaces de noms

Pour commencer, importez les espaces de noms qui vous donnent accès aux fonctionnalités de rasterisation et d’exportation d’image.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Étape 1 : Charger le fichier DWG

Chargez le fichier DWG (ou DWF) source dans un objet `Image`. Cet objet représente le dessin complet en mémoire.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*Pourquoi c’est important :* Charger le fichier une seule fois vous permet de réutiliser la même instance `image` pour n’importe quel nombre d’exportations spécifiques à un calque, améliorant ainsi les performances.

## Étape 2 : Configurer les options de rasterisation

Créez une instance `CadRasterizationOptions` pour indiquer à Aspose.CAD comment rendre le dessin. Ici, nous définissons une haute résolution (1600 × 1600) afin que le JPEG exporté soit net.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

Vous pouvez également ajuster la couleur d’arrière‑plan, l’échelle du poids des lignes ou les paramètres d’anti‑aliasing si nécessaire.

## Étape 3 : Spécifier les calques (Visibilité des calques DWG)

Ajoutez les calques que vous souhaitez **exporter**. Dans cet exemple, nous exportons uniquement « LayerA ». Pour exporter plusieurs calques, il suffit de les lister dans le tableau.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*Astuce :* Utilisez le nom exact du calque tel qu’il apparaît dans le dessin ; les noms de calques sont sensibles à la casse.

## Étape 4 : Configurer les options d'exportation d'image

Choisissez le format d’image que vous souhaitez créer. Nous utiliserons `JpegOptions` car le JPEG offre un bon équilibre entre qualité et taille de fichier, idéal lorsque vous devez **sauvegarder des DWG JPEG** pour un aperçu web.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

Si vous devez **convertir une image DWG** en PNG ou TIFF, remplacez `JpegOptions` par la classe d’options correspondante.

## Étape 5 : Enregistrer l'image exportée

Définissez le chemin du fichier de sortie et invoquez `Save`. Le moteur de rasterisation respecte la liste de calques que vous avez fournie, de sorte que seul « LayerA » apparaît dans le JPEG final.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

Après l’exécution de cette ligne, vous trouverez `for_layers_test.jpg` dans votre répertoire de documents, contenant uniquement le calque sélectionné.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Nom de calque introuvable** | Vérifiez l’orthographe exacte et la casse du calque dans le DWG original. Utilisez un visualiseur CAD pour lister les noms de calques. |
| **Image de sortie vide** | Assurez‑vous que les options de rasterisation ont un arrière‑plan non transparent et que les calques sélectionnés contiennent réellement de la géométrie. |
| **Sortie à basse résolution** | Augmentez `PageWidth` et `PageHeight` ou définissez `Resolution` dans `CadRasterizationOptions`. |
| **Version DWG non prise en charge** | Mettez à jour vers la dernière version d’Aspose.CAD ; elle ajoute la prise en charge des versions plus récentes d’AutoCAD. |

## Questions fréquemment posées

### Q1 : Puis‑je gérer plusieurs calques simultanément ?
R1 : Oui, vous pouvez. Ajoutez simplement les noms de calques au tableau `rasterizationOptions.Layers`.

### Q2 : Une version d’essai d’Aspose.CAD est‑elle disponible ?
R2 : Oui, vous pouvez obtenir une version d’essai gratuite [ici](https://releases.aspose.com/).

### Q3 : Où puis‑je trouver la documentation ?
R3 : La documentation est disponible [ici](https://reference.aspose.com/cad/net/).

### Q4 : Comment obtenir du support pour Aspose.CAD ?
R4 : Vous pouvez demander de l’aide sur le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5 : Quelles sont les options de licence pour Aspose.CAD ?
R5 : Vous pouvez explorer les options de licence et les détails d’achat [ici](https://purchase.aspose.com/buy).

**Q supplémentaires**

**Q : Puis‑je exporter le dessin en PNG au lieu de JPEG ?**  
R : Absolument. Remplacez `JpegOptions` par `PngOptions` et ajustez l’extension du fichier en conséquence.

**Q : La bibliothèque préserve‑t‑elle les styles de ligne et les couleurs ?**  
R : Oui. Toutes les propriétés vectorielles sont rendues fidèlement lors de la rasterisation.

---

**Dernière mise à jour :** 2026-04-09  
**Testé avec :** Aspose.CAD pour .NET (dernière version)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}