---
date: 2026-03-21
description: Apprenez comment obtenir la taille d’une mise en page CAD en .NET avec
  Aspose.CAD. Suivez notre guide étape par étape pour une manipulation efficace des
  fichiers CAD.
linktitle: Get Size of CAD Layout
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Obtenir la taille de la mise en page CAD dans Aspose.CAD pour .NET
url: /fr/net/cad-drawing-manipulation/get-size-of-cad-layout/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Obtenir la taille de la mise en page CAD dans Aspose.CAD pour .NET

## Introduction

Dans ce tutoriel complet, vous découvrirez **comment obtenir la taille de la mise en page CAD** en utilisant la bibliothèque Aspose.CAD pour .NET. Que vous construisiez un visualiseur CAD, génériez des miniatures ou ayez besoin de dimensions précises de la mise en page pour un traitement en aval, connaître la taille exacte de chaque mise en page est essentiel. Nous parcourrons l’ensemble du flux de travail — du chargement d’un dessin à l’extraction des dimensions de la mise en page et, éventuellement, à leur sauvegarde sous forme d’images — afin que vous puissiez intégrer cette fonctionnalité dans vos propres applications en toute confiance.

## Réponses rapides
- **Que signifie « obtenir la taille de la mise en page CAD » ?** Cela signifie récupérer la largeur et la hauteur (en unités du dessin) de chaque mise en page non vide dans un fichier CAD.  
- **Quelle bibliothèque prend en charge cela ?** Aspose.CAD pour .NET fournit une API simple pour accéder aux informations de mise en page.  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour l’évaluation ; une licence commerciale est requise pour une utilisation en production.  
- **Formats pris en charge ?** DWG, DXF et de nombreux autres formats CAD/BIM sont entièrement pris en charge.  
- **Temps d’implémentation typique ?** Environ 10‑15 minutes pour une routine de récupération de taille basique.

## Qu’est‑ce que « obtenir la taille de la mise en page CAD » ?
Obtenir la taille de la mise en page CAD signifie extraire les étendues géométriques de chaque mise en page (espace papier) définie dans un dessin CAD. Ces étendues sont exprimées dans les unités natives du dessin (généralement millimètres ou pouces) et sont utiles pour des tâches telles que le redimensionnement, l’impression ou la génération d’images de prévisualisation.

## Pourquoi récupérer la taille de la mise en page CAD avec Aspose.CAD ?
- **Aucun logiciel CAD requis** – Fonctionne entièrement côté serveur.  
- **Multiplateforme** – Fonctionne avec .NET Framework, .NET Core et .NET 5/6+.  
- **Mesures précises** – Retourne les étendues exactes telles qu’elles sont stockées dans le fichier, évitant l’analyse manuelle.  
- **Intégration facile** – Les appels d’API simples s’intègrent naturellement aux projets C# existants.

## Prérequis

Avant de plonger dans le code, assurez‑vous de disposer de ce qui suit :

- Aspose.CAD pour .NET installé. Vous pouvez le télécharger depuis la [page de téléchargement d’Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).
- Un ou plusieurs fichiers CAD (DWG, DXF, etc.) que vous souhaitez analyser. Ce guide utilise `conic_pyramid.dxf` et `Bottom_plate.dwg` comme fichiers d’exemple.

## Importer les espaces de noms

Dans votre projet .NET, commencez par importer les espaces de noms requis :

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## Étape 1 : Configurer le répertoire des documents

Définissez le dossier qui contient vos fichiers CAD. Remplacez le texte de substitution par le chemin réel sur votre machine.

```csharp
string MyDir = "Your Document Directory";
```

## Étape 2 : Spécifier les chemins des fichiers CAD

Créez un tableau qui pointe vers chaque fichier CAD que vous souhaitez traiter.

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## Étape 3 : Parcourir les fichiers CAD

Chargez chaque fichier, détectez son format et préparez‑vous à extraire les informations de mise en page.

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (continue to the next step)
    }
}
```

## Étape 4 : Obtenir les mises en page non vides

Nous avons besoin d’une méthode d’assistance qui ne renvoie que les mises en page contenant réellement des entités de dessin. Les mises en page vides sont ignorées car elles n’ont aucune taille à signaler.

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (continue to the next step)
}
```

## Étape 5 : Obtenir les mises en page pour les fichiers DWG

Les fichiers DWG stockent les informations de mise en page dans la table `HeaderVariables`. La méthode suivante extrait les noms de toutes les mises en page non vides d’un dessin DWG.

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Étape 6 : Obtenir les mises en page pour les fichiers DXF

Les fichiers DXF utilisent une structure différente. Cette méthode analyse la collection `Tables` pour trouver les mises en page d’espace papier qui contiennent des entités.

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (continue to the next step)
}
```

## Étape 7 : Récupérer la taille de la mise en page et enregistrer en image

Enfin, parcourez chaque mise en page découverte, lisez ses étendues et, éventuellement, rendez la mise en page sous forme de fichier image pour une vérification visuelle.

```csharp
foreach (string layout in layouts)
{
    // ... (continue to the next step)
}
```

## Problèmes courants et astuces

- **Noms de mise en page manquants :** Assurez‑vous que le fichier CAD contient réellement des mises en page papier ; certains fichiers n’ont que l’espace modèle.  
- **Unités incorrectes :** La taille est renvoyée dans les unités natives du dessin. Convertissez en millimètres ou en pouces si nécessaire.  
- **Performance :** Le chargement de fichiers DWG/DXF très volumineux peut être gourmand en mémoire ; envisagez de traiter les fichiers de façon asynchrone ou par lots.

## Questions fréquentes

**Q : Aspose.CAD est‑il compatible avec tous les formats de fichiers CAD ?**  
R : Oui, Aspose.CAD prend en charge un large éventail de formats, y compris DWG, DXF, DGN et de nombreux types de fichiers BIM.

**Q : Puis‑je personnaliser les options d’enregistrement d’image ?**  
R : Absolument ! Vous pouvez ajuster les `CadRasterizationOptions` (format, résolution, couleur d’arrière‑plan, etc.) pour répondre à vos besoins spécifiques.

**Q : Où puis‑je trouver de la documentation supplémentaire ?**  
R : Consultez la [documentation d’Aspose.CAD](https://reference.aspose.com/cad/net/) pour des références API détaillées et plus d’exemples.

**Q : Existe‑t‑il un essai gratuit ?**  
R : Oui, vous pouvez explorer Aspose.CAD avec un [essai gratuit](https://releases.aspose.com/).

**Q : Comment obtenir du support technique ?**  
R : Pour le support technique, rendez‑vous sur le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

**Dernière mise à jour :** 2026-03-21  
**Testé avec :** Aspose.CAD 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}