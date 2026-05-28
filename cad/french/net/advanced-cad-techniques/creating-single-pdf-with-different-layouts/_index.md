---
date: 2026-03-02
description: Apprenez à créer un PDF unique avec différentes mises en page en utilisant
  Aspise.CAD pour .NET – convertir le CAD en PDF, exporter le DWG en PDF et enregistrer
  le CAD en PDF efficacement.
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Comment créer un PDF unique avec différentes mises en page - Guide Aspose.CAD
url: /fr/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer un PDF unique avec différentes mises en page - Guide Aspose.CAD

## Introduction

Si vous devez **créer un PDF unique** contenant plusieurs mises en page CAD, vous êtes au bon endroit. Dans ce tutoriel, nous parcourrons les étapes exactes nécessaires pour convertir des dessins CAD en un seul document PDF, en gérant plusieurs mises en page au passage. Vous verrez comment Aspose.CAD for .NET facilite la **conversion CAD en PDF**, l'**exportation DWG en PDF**, et la **sauvegarde CAD en PDF** avec seulement quelques lignes de code C#.

## Réponses rapides
- **Quel est le sujet de ce tutoriel ?** Générer un PDF qui inclut plusieurs mises en page CAD.  
- **Quelle bibliothèque est utilisée ?** Aspose.CAD for .NET.  
- **Ai-je besoin d’une licence ?** Un essai gratuit suffit pour l'évaluation ; une licence est requise pour la production.  
- **Formats CAD pris en charge ?** DWG, DXF, DGN et bien d'autres.  
- **Temps d'implémentation typique ?** Environ 10‑15 minutes pour une conversion de base.

## Qu’est‑ce que « créer un PDF unique » dans un contexte CAD ?

Créer un PDF unique signifie prendre un fichier source CAD qui peut contenir plusieurs définitions de mise en page (espaces papier) et fusionner chaque mise en page en pages séparées d'un même document PDF. Cela est particulièrement utile pour les plans architecturaux, les schémas d'ingénierie ou tout scénario où le client attend un paquet PDF consolidé.

## Pourquoi utiliser Aspose.CAD pour cette tâche ?

- **Pas de dépendances externes** – pur .NET, aucune installation d’AutoCAD requise.  
- **Contrôle total sur la rasterisation** – vous pouvez définir la taille de page, le DPI et les dimensions personnalisées de la mise en page.  
- **Rendu haute fidélité** – les données vectorielles sont conservées lorsque possible, garantissant une sortie nette.  
- **Prêt pour le traitement par lots** – le même code peut être placé dans une boucle pour traiter automatiquement de nombreux dessins.

## Prérequis

- Aspose.CAD for .NET : assurez‑vous d’avoir Aspose.CAD for .NET installé. Vous pouvez le télécharger depuis [ici](https://releases.aspose.com/cad/net/).  
- Environnement de développement : configurez un environnement de développement .NET et possédez une compréhension de base de la programmation C#.

## Importer les espaces de noms

Dans votre projet C#, incluez les espaces de noms nécessaires pour exploiter les fonctionnalités d’Aspose.CAD for .NET :

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Guide étape par étape

### Étape 1 : Charger l’image CAD

Tout d'abord, chargez le fichier CAD source (par exemple, un dessin DWG). La classe `CadImage` vous donne accès à toutes les mises en page du fichier.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### Étape 2 : Personnaliser les options de rasterisation

Définissez comment chaque mise en page doit être rasterisée. Vous pouvez définir une taille de page par défaut puis la remplacer pour des mises en page spécifiques à l’aide de `LayoutPageSizes`.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **Conseil pro :** ajustez le DPI (`rasterizationOptions.Resolution`) si vous avez besoin d’une sortie à plus haute résolution pour des dessins détaillés.

### Étape 3 : Définir les options PDF

Enveloppez les paramètres de rasterisation dans un objet `PdfOptions`. Cela indique à Aspose.CAD de rendre les données CAD directement dans un flux PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### Étape 4 : Enregistrer en PDF

Enfin, invoquez `Save` sur l’instance `CadImage`, en passant le nom du fichier PDF cible et les options préparées. La bibliothèque générera un PDF unique contenant une page pour chaque mise en page que vous avez configurée.

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

Après cet appel, vous disposerez d’un PDF qui combine les mises en page « ANSI C Plot » et « 8.5 x 11 Plot » en un seul document cohérent.

## Problèmes courants & dépannage

| Problème | Raison | Solution |
|----------|--------|----------|
| Mises en page manquantes dans le PDF | `LayoutPageSizes` non défini pour un nom de mise en page | Vérifiez les noms exacts des mises en page dans le fichier CAD (sensible à la casse). |
| Sortie de faible qualité | Le DPI par défaut est 96 | Définissez `rasterizationOptions.Resolution = 300` (ou plus) avant l’enregistrement. |
| Fichier non trouvé | Chemin `MyDir` incorrect | Utilisez `Path.Combine` pour créer des chemins indépendants de la plateforme. |

## Foire aux questions

### Q1 : Puis‑je utiliser Aspose.CAD for .NET avec d’autres formats CAD ?

Oui, Aspose.CAD for .NET prend en charge divers formats CAD tels que DWG, DXF, DGN, et plus encore.

### Q2 : Une version d’essai gratuite est‑elle disponible ?

Oui, vous pouvez explorer une version d’essai gratuite [ici](https://releases.aspose.com/).

### Q3 : Comment obtenir du support pour Aspose.CAD for .NET ?

Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire.

### Q4 : Où puis‑je trouver la documentation détaillée ?

Reportez‑vous à la documentation [ici](https://reference.aspose.com/cad/net/).

### Q5 : Puis‑je acheter une licence pour Aspose.CAD for .NET ?

Oui, vous pouvez acheter une licence [ici](https://purchase.aspose.com/buy).

**Questions supplémentaires & réponses**

**Q :** Comment **exporter DWG en PDF** avec des tailles de page personnalisées ?  
**R :** Utilisez `CadRasterizationOptions.LayoutPageSizes` pour associer chaque mise en page DWG aux dimensions de page PDF souhaitées, comme illustré à l’étape 2.

**Q :** Est‑il possible de **enregistrer CAD en PDF** sans rasteriser les données vectorielles ?  
**R :** Aspose.CAD rasterise toujours lors de la création d’un PDF, mais vous pouvez augmenter le DPI pour conserver la fidélité visuelle.

## Conclusion

Dans ce guide, nous avons démontré comment **créer un PDF unique** à partir de dessins CAD contenant plusieurs mises en page, en utilisant Aspose.CAD for .NET. Vous disposez désormais des blocs de construction pour **convertir CAD en PDF**, **exporter DWG en PDF**, et **sauvegarder CAD en PDF** dans un flux de travail automatisé. Expérimentez avec différents paramètres de rasterisation pour répondre aux exigences de qualité de votre projet, et intégrez ce code dans des pipelines de traitement par lots plus larges selon vos besoins.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-03-02  
**Testé avec :** Aspose.CAD for .NET 24.11  
**Auteur :** Aspose