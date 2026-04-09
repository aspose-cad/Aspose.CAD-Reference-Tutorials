---
date: 2026-04-09
description: Apprenez à charger un fichier DWFX en C# et à convertir le CAD en PDF
  avec Aspose.CAD pour .NET. Guide étape par étape pour une intégration fluide.
keywords:
- load dwfx file c#
- c# convert cad to pdf
- aspose.cad dwfx
linktitle: Ouverture et accès aux fichiers DWFX en C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Comment charger un fichier DWFX en C# avec le guide Aspose.CAD
url: /fr/net/dwg-file-manipulation/opening-and-accessing-dwfx-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment charger un fichier DWFX en C# avec le guide Aspose.CAD

## Introduction

Si vous devez **charger un fichier DWFX en C#** et le convertir en PDF, vous êtes au bon endroit. Dans ce tutoriel, nous parcourrons les étapes exactes nécessaires pour ouvrir un dessin DWFX avec Aspose.CAD pour .NET, configurer la rasterisation, et enfin **c# convertir CAD en PDF**. Que vous construisiez un utilitaire de bureau ou un service web, l'approche reste la même et fonctionne avec toute version .NET prise en charge par Aspose.CAD.

## Réponses rapides
- **Quelle bibliothèque faut‑il ?** Aspose.CAD for .NET  
- **Puis‑je convertir DWFX en PDF ?** Oui – il suffit de configurer `CadRasterizationOptions` et d'utiliser `PdfOptions`.  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Ai‑je besoin d’une licence pour les tests ?** Un essai gratuit suffit pour le développement ; une licence permanente est requise pour la production.  
- **Combien de temps le code met‑il à s’exécuter ?** Le chargement et la conversion d’un fichier DWFX typique se terminent en moins d’une seconde sur un CPU moderne.

## Qu’est‑ce qu’un fichier DWFX ?

DWFX (Design Web Format XPS) est une représentation basée sur XML d’un dessin CAD qui peut être affichée dans les navigateurs et autres visionneuses. Parce qu’il stocke des données vectorielles, il est idéal pour une conversion PDF de haute qualité sans perte de détails.

## Pourquoi utiliser Aspose.CAD pour charger des fichiers DWFX en C# ?

* **Prise en charge complète des formats** – Aspose.CAD comprend le DWFX ainsi que des dizaines d’autres formats CAD.  
* **Aucune dépendance externe** – Pure .NET, pas besoin d’AutoCAD ou d’autres composants natifs.  
* **Conversion facile raster‑vers‑vecteur** – Passez des images raster aux PDF vectoriels en quelques lignes de code.  

## Prérequis

Avant de plonger dans le code, assurez-vous d’avoir :

1. **Aspose.CAD for .NET** installé. Vous pouvez le télécharger [ici](https://releases.aspose.com/cad/net/).  
2. Un dossier contenant les fichiers DWFX que vous souhaitez traiter. Notez le chemin complet pour les emplacements source et de sortie.

## Comment charger un fichier DWFX en C#

Voici le guide étape par étape. Chaque étape est accompagnée d’une brève explication, suivie du bloc de code exact à copier.

### Importer les espaces de noms

```csharp
using Aspose.CAD.ImageOptions;
using System;
```

Ces espaces de noms vous donnent accès à la classe `Image` pour charger les fichiers CAD ainsi qu’aux options nécessaires à la rasterisation et à la génération de PDF.

### Étape 1 : Configurer les répertoires source et de sortie

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";
```

Remplacez `"Your Document Directory"` par le chemin où se trouve votre fichier DWFX et où vous souhaitez enregistrer le PDF.

### Étape 2 : Charger le fichier DWFX

```csharp
using (Image cadDrawing = Image.Load(SourceDir + "Tyrannosaurus.dwfx"))
```

`Image.Load` lit le fichier DWFX dans un objet `Image` avec lequel Aspose.CAD peut travailler. Changez `"Tyrannosaurus.dwfx"` par le nom de votre propre dessin.

### Étape 3 : Configurer les options de rasterisation

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

Les options de rasterisation indiquent à Aspose.CAD la taille de la page résultante. Utiliser les dimensions originales du dessin préserve l’échelle exacte.

### Étape 4 : Enregistrer en PDF (c# convertir CAD en PDF)

```csharp
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
cadDrawing.Save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

Ici nous **c# convertissons CAD en PDF** en attachant les paramètres de rasterisation à un objet `PdfOptions` et en appelant `Save`. Le fichier de sortie sera placé dans le dossier que vous avez spécifié.

### Étape 5 : Afficher le message de succès

```csharp
Console.WriteLine("OpenDwfxFile executed successfully");
```

Un simple message console vous indique que la conversion s’est terminée sans erreur.

## Problèmes courants et astuces

* **Fichier non trouvé** – Vérifiez à nouveau le chemin `SourceDir` et assurez‑vous que le nom du fichier correspond exactement, y compris la casse.  
* **PDF vide** – Assurez‑vous que le fichier DWFX contient réellement des données vectorielles ; certains outils d’exportation génèrent des dessins vides.  
* **Performance** – Pour des dessins très volumineux, envisagez de réduire `PageWidth`/`PageHeight` ou de définir une résolution plus basse dans `CadRasterizationOptions`.  

## Questions fréquemment posées

### Q1 : Aspose.CAD pour .NET est‑il compatible avec tous les fichiers DWFX ?

R1 : Aspose.CAD pour .NET prend en charge un large éventail de formats CAD, y compris le DWFX. Cependant, il est conseillé de consulter la documentation pour les détails de compatibilité spécifiques.

### Q2 : Où puis‑je trouver la documentation d’Aspose.CAD pour .NET ?

R2 : La documentation est disponible [ici](https://reference.aspose.com/cad/net/).

### Q3 : Puis‑je essayer Aspose.CAD pour .NET avant d’acheter ?

R3 : Oui, vous pouvez télécharger une version d’essai gratuite [ici](https://releases.aspose.com/).

### Q4 : Comment obtenir une licence temporaire pour Aspose.CAD pour .NET ?

R4 : Les licences temporaires peuvent être obtenues [ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Besoin d’assistance ou avez‑vous d’autres questions ?

R5 : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour obtenir de l’aide.

### Q6 : Puis‑je traiter par lots plusieurs fichiers DWFX ?

R6 : Absolument. Enveloppez la logique de chargement et d’enregistrement dans une boucle `foreach` qui parcourt les fichiers d’un répertoire.

### Q7 : La conversion préserve‑t‑elle les calques et les couleurs ?

R7 : Les informations vectorielles telles que les calques et les couleurs sont conservées dans le PDF lorsque le DWFX source contient ces données.

---

**Dernière mise à jour :** 2026-04-09  
**Testé avec :** Aspose.CAD for .NET 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}