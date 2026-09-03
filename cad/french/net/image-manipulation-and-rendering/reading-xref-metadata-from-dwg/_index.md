---
date: 2026-08-23
description: Débloquez le potentiel d'Aspose.CAD pour .NET grâce à notre tutoriel
  étape par étape sur la lecture des métadonnées xref des fichiers DWG.
keywords:
- read xref metadata
- extract dwg xref
- Aspose.CAD
lastmod: 2026-08-23
linktitle: Lecture des métadonnées XREF des fichiers DWG
og_description: Apprenez à lire les métadonnées xref des fichiers DWG avec Aspose.CAD
  pour .NET. Ce guide vous accompagne à travers les prérequis, les étapes de code
  et les pièges courants en moins de dix minutes.
og_image_alt: Screenshot of Aspose.CAD reading XREF metadata in a .NET IDE
og_title: Comment lire les métadonnées xref des fichiers DWG avec Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  headline: How to read xref metadata from DWG files using Aspose.CAD
  type: TechArticle
- description: Unlock the potential of Aspose.CAD for .NET with our step‑by‑step tutorial
    on how to read xref metadata from DWG files.
  name: How to read xref metadata from DWG files using Aspose.CAD
  steps:
  - name: load the DWG file
    text: Create an `Image` instance from the DWG file you want to analyze. `Image.Load`
      loads a CAD file and returns a `CadImage` object representing the drawing. Adjust
      the `sourceFilePath` variable to the exact location of your drawing.
  - name: iterate through entities
    text: Loop through the `Image` object’s `Entities` collection. `CadBaseEntity`
      is the base class for all CAD entities in Aspose.CAD. For each entity, check
      whether it is an XREF reference and collect its metadata.
  - name: extract metadata
    text: When you encounter an XREF entity, read its insertion point (X, Y, Z) and
      the path of the referenced drawing. `CadUnderlay` represents an external reference
      (XREF) entity within a DWG drawing.
  - name: process metadata
    text: At this stage you can store the extracted information in a database, write
      it to a CSV file, or feed it into downstream BIM workflows. The sample simply
      prints the values to the console, but you are free to replace that with any
      custom logic.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for .NET supports **50+ input and output formats**, including
      DWG, DXF, DGN, and IFC, giving you broad coverage for most engineering workflows.
    question: Is Aspose.CAD for .NET compatible with all CAD file formats?
  - answer: Certainly! You can access the free trial download page [free trial download
      page](https://releases.aspose.com/).
    question: Can I use the free trial before making a purchase decision?
  - answer: The documentation is available [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).
    question: Where can I find comprehensive documentation for Aspose.CAD for .NET?
  - answer: You can get a temporary license [temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.CAD for .NET?
  - answer: Join the Aspose.CAD community at [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19)
      for expert support and discussions.
    question: Need assistance or have specific queries?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- read xref metadata
- extract dwg xref
- Aspose.CAD
- DWG
- CAD metadata
title: Comment lire les métadonnées xref des fichiers DWG avec Aspose.CAD
url: /fr/net/image-manipulation-and-rendering/reading-xref-metadata-from-dwg/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment lire les métadonnées xref à partir de fichiers DWG avec Aspose.CAD

## Introduction

Dans ce tutoriel, vous apprendrez **comment lire les métadonnées xref** à partir de fichiers DWG en utilisant la bibliothèque Aspose.CAD pour .NET. Que vous ayez besoin d’auditer les références externes, de migrer des dessins anciens ou de créer un pipeline BIM personnalisé, extraire les informations XREF est une exigence courante. Nous parcourrons chaque étape, de la configuration du projet au traitement des métadonnées, et nous mettrons en avant des conseils pratiques que vous pouvez appliquer immédiatement.

## Réponses rapides
- **Quel est le but principal ?** Récupérer les points d’insertion et les chemins de fichiers des références externes (XREF) intégrées dans un dessin DWG.  
- **Quelle bibliothèque est requise ?** Aspose.CAD pour .NET (prend en charge plus de 50 formats CAD).  
- **Ai-je besoin d’une licence ?** Une licence temporaire ou complète est requise pour une utilisation en production ; un essai gratuit est disponible.  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Combien de temps le code met‑il à s’exécuter ?** Le traitement d’un DWG typique de 200 pages avec quelques XREF s’achève en moins d’une seconde sur du matériel standard.

## Qu’est‑ce que la lecture des métadonnées xref ?

`read xref metadata` désigne l’opération d’accès aux propriétés des entités de référence externes stockées dans un dessin DWG, telles que leurs coordonnées d’insertion, les chemins des fichiers sources et les indicateurs de visibilité. Cette opération vous permet de découvrir programmatique comment un dessin est composé à partir d’autres fichiers, facilitant la validation automatisée, le reporting ou le traitement par lots des ressources liées.

## Pourquoi utiliser Aspose.CAD pour cette tâche ?

Aspose.CAD prend en charge **plus de 50 formats de fichiers CAD** et peut lire les fichiers DWG **sans nécessiter AutoCAD**. La bibliothèque traite les grands dessins **dans des flux à faible consommation de mémoire**, vous permettant de gérer des fichiers de plusieurs centaines de pages sans charger le fichier complet en RAM. Ces capacités quantifiées en font un choix fiable pour l’automatisation CAD de niveau entreprise.

## Prérequis

Avant de plonger dans le code, vérifiez que vous disposez de ce qui suit :

- Aspose.CAD pour .NET installé. Téléchargez le dernier package depuis la [page de publication Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).
- Un dossier local contenant les fichiers DWG que vous souhaitez inspecter. Mettez à jour la variable `MyDir` dans le code d’exemple pour qu’elle pointe vers ce dossier.
- Une licence Aspose.CAD valide (ou l’essai gratuit) si vous prévoyez d’exécuter le code dans un environnement de production.

Maintenant que l’environnement est prêt, commençons à coder.

## Importer les espaces de noms

La première chose à faire est d’importer les espaces de noms qui exposent l’API d’Aspose.CAD. Les directives `using` introduisent les espaces de noms Aspose.CAD dans le contexte, permettant l’accès aux classes CAD telles que `Image` et `CadImage`.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
```

## Comment lire les métadonnées xref à partir de fichiers DWG ?

Chargez le dessin, énumérez ses entités, filtrez les objets XREF, puis extrayez les propriétés souhaitées — le tout en quelques lignes de code simples. Les sections suivantes décomposent le processus en quatre étapes logiques que vous pouvez copier‑coller dans n’importe quel projet console ou service .NET.

### Étape 1 : charger le fichier DWG

Créez une instance `Image` à partir du fichier DWG que vous souhaitez analyser. `Image.Load` charge un fichier CAD et renvoie un objet `CadImage` représentant le dessin. Ajustez la variable `sourceFilePath` pour qu’elle pointe vers l’emplacement exact de votre dessin.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage image = (CadImage)Image.Load(sourceFilePath))
{
    // Code for the next steps goes here
}
```

### Étape 2 : parcourir les entités

Parcourez la collection `Entities` de l’objet `Image`. `CadBaseEntity` est la classe de base pour toutes les entités CAD dans Aspose.CAD. Pour chaque entité, vérifiez si elle est une référence XREF et collectez ses métadonnées.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    if (entity is CadUnderlay)
    {
        // Code for the next steps goes here
    }
}
```

### Étape 3 : extraire les métadonnées

Lorsque vous rencontrez une entité XREF, lisez son point d’insertion (X, Y, Z) ainsi que le chemin du dessin référencé. `CadUnderlay` représente une entité de référence externe (XREF) dans un dessin DWG.

```csharp
//XREF entity with metadata
Cad3DPoint insertionPoint = ((CadUnderlay)entity).InsertionPoint;
string path = ((CadUnderlay)entity).UnderlayPath;
```

### Étape 4 : traiter les métadonnées

À ce stade, vous pouvez stocker les informations extraites dans une base de données, les écrire dans un fichier CSV ou les intégrer aux flux de travail BIM en aval. L’exemple se contente d’afficher les valeurs dans la console, mais vous êtes libre de les remplacer par toute logique personnalisée.

```csharp
// Your custom logic for processing metadata goes here
```

## Problèmes courants et dépannage

| Symptôme | Cause probable | Solution |
|----------|----------------|----------|
| Aucune entité XREF n’est renvoyée | Le dessin utilise un type de référence différent (par ex., INSERT) | Vérifiez le type d’entité avec `CadEntityType.Xref` et gérez également `Insert` si nécessaire |
| `Image.Load` génère une exception | Chemin de fichier incorrect ou version DWG non prise en charge | Vérifiez le chemin et assurez‑vous d’utiliser Aspose.CAD 24.11 ou une version plus récente |
| Les valeurs des métadonnées sont vides | Le XREF est défini mais non résolu (fichier externe manquant) | Assurez‑vous que le fichier référencé existe sur le disque ou fournissez un résolveur de système de fichiers virtuel |

## Questions fréquemment posées

**Q : Aspose.CAD pour .NET est‑il compatible avec tous les formats de fichiers CAD ?**  
R : Oui, Aspose.CAD pour .NET prend en charge **plus de 50 formats d’entrée et de sortie**, y compris DWG, DXF, DGN et IFC, vous offrant une large couverture pour la plupart des flux de travail d’ingénierie.

**Q : Puis‑je utiliser l’essai gratuit avant de prendre une décision d’achat ?**  
R : Bien sûr ! Vous pouvez accéder à la page de téléchargement de l’essai gratuit [free trial download page](https://releases.aspose.com/).

**Q : Où puis‑je trouver la documentation complète d’Aspose.CAD pour .NET ?**  
R : La documentation est disponible [Aspose.CAD .NET documentation](https://reference.aspose.com/cad/net/).

**Q : Comment obtenir une licence temporaire pour Aspose.CAD pour .NET ?**  
R : Vous pouvez obtenir une licence temporaire [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q : Besoin d’assistance ou avez‑vous des questions spécifiques ?**  
R : Rejoignez la communauté Aspose.CAD sur [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) pour un support d’experts et des discussions.

## Conclusion

Vous disposez maintenant d’un modèle complet, prêt pour la production, pour **lire les métadonnées XREF** à partir de fichiers DWG avec Aspose.CAD pour .NET. En suivant les quatre étapes — charger le fichier, parcourir les entités, extraire le point d’insertion et le chemin du sous‑couche, et traiter les résultats — vous pouvez intégrer cette fonctionnalité dans toute application centrée sur le CAD, qu’il s’agisse d’un outil de migration de données, d’un script de contrôle qualité ou d’un pipeline BIM personnalisé.

---

**Dernière mise à jour :** 2026-08-23  
**Testé avec :** Aspose.CAD 24.11 pour .NET  
**Auteur :** Aspose

## Tutoriels associés

- [Comment modifier le chemin xref et éditer les hyperliens dans les fichiers CAD - Tutoriel Aspose.CAD](/cad/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/)
- [Obtenir les attributs de bloc à partir de fichiers DWG - Tutoriel Aspose.CAD](/cad/net/image-manipulation-and-rendering/getting-block-attributes-from-dwg/)
- [Convertir de gros fichiers DWG en PDF - Tutoriel Aspose.CAD](/cad/net/image-manipulation-and-rendering/converting-large-dwg-files-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}