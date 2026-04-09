---
date: 2026-04-09
description: Apprenez à convertir un DWG en image et à lire les drapeaux d’underlay
  à l’aide d’Aspose.CAD pour .NET dans ce guide pas à pas.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: Explorer les drapeaux d’incrustation des fichiers DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Convertir DWG en image – Explorer les drapeaux de sous-couche des fichiers
  DWG – Tutoriel Aspose.CAD
url: /fr/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exploration des indicateurs d'underlay des fichiers DWG - Tutoriel Aspose.CAD

## Introduction

Si vous vous plongez dans le monde complexe des fichiers CAD, en particulier les fichiers DWG, et que vous souhaitez **convertir DWG en image** tout en découvrant **comment lire les indicateurs d'underlay**, vous êtes au bon endroit. Ce tutoriel vous guide étape par étape en utilisant la puissante bibliothèque Aspose.CAD pour .NET, afin que vous puissiez extraire les informations d'underlay et rendre le dessin sous forme d'image en toute confiance.

## Réponses rapides
- **Que signifie « convertir DWG en image » ?**  
  Cela signifie rendre un dessin DWG dans un format raster (PNG, JPEG, etc.) à l'aide d'Aspose.CAD.
- **Quelle méthode révèle les indicateurs d'underlay ?**  
  Accédez à la propriété `Flags` de l'objet `CadUnderlay` après avoir chargé le DWG.
- **Ai‑je besoin d'une licence pour Aspose.CAD ?**  
  Une licence temporaire est disponible pour l'évaluation ; une licence complète est requise pour la production.
- **Quelles versions de .NET sont prises en charge ?**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 et versions ultérieures.
- **Puis‑je extraire la géométrie d'underlay ?**  
  Oui – le chemin d'underlay, le point d’insertion, l’échelle, la rotation et les états des indicateurs sont tous accessibles.

## Qu'est-ce que « convertir DWG en image » et pourquoi est‑ce important ?

Convertir un fichier DWG en image vous permet d'afficher les dessins CAD dans les navigateurs, de les intégrer dans des rapports ou de les partager avec des parties prenantes qui ne disposent pas d’un visualiseur CAD. Lors du rendu, il est souvent nécessaire d’inspecter les objets **underlay** (par ex. les références DGN) pour s’assurer qu’ils s’affichent correctement. Comprendre les indicateurs d'underlay vous aide à résoudre les problèmes de découpage, de rendu en monochrome et de visibilité avant de générer l’image finale.

## Prérequis

- Une compréhension de base du C# et de la programmation .NET.  
- Bibliothèque **Aspose.CAD for .NET** installée. Si vous ne l’avez pas encore, téléchargez‑la **[ici](https://releases.aspose.com/cad/net/)**.  
- Un fichier DWG pour les tests – le fichier d’exemple **« BlockRefDgn.dwg »** est utilisé tout au long de ce guide.

## Importer les espaces de noms

Pour commencer, importez les espaces de noms nécessaires :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Étape 1 : Charger le fichier DWG et le convertir en `CadImage`

Tout d'abord, chargez le fichier DWG et castiez‑le en `CadImage`. Cet objet vous donne accès à toutes les entités du dessin, y compris les underlays.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Étape 2 : Parcourir les entités

Ensuite, parcourez chaque entité du dessin. C’est ici que vous localiserez les objets underlay.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Étape 3 : Vérifier le type `CadDgnUnderlay`

Identifiez les entités underlay en vérifiant leur type d’exécution. La classe `CadDgnUnderlay` représente les underlays DGN incorporés dans un DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Étape 4 : Accéder aux indicateurs d'underlay

Une fois que vous avez un `CadDgnUnderlay`, castiez‑le en `CadUnderlay` pour lire ses propriétés et l’état de ses indicateurs. Les indicateurs indiquent si l’underlay est visible, découpé ou rendu en monochrome.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### Ce que indique la sortie

- **UnderlayPath / UnderlayName** – emplacement du fichier DGN externe.  
- **InsertionPoint (X, Y)** – coordonnées où l’underlay est placé dans l’espace DWG.  
- **RotationAngle** – rotation appliquée à l’underlay.  
- **ScaleX / ScaleY / ScaleZ** – facteurs d’échelle pour chaque axe.  
- **Flags** – valeurs booléennes indiquant la visibilité (`UnderlayIsOn`), le découpage (`ClippingIsOn`) et le rendu en monochrome (`Monochrome`).

## Problèmes courants et solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| Aucun résultat pour les vérifications d’indicateurs | Les indicateurs d’underlay sont à 0 par défaut lorsque l’underlay est désactivé. | Vérifiez que le DWG contient réellement un underlay actif ou activez la visibilité dans le fichier CAD source. |
| Exception `Invalid cast` | L’entité n’est pas un `CadDgnUnderlay`. | Assurez‑vous que la condition `if (entity is CadDgnUnderlay)` est vérifiée avant le cast. |
| Le rendu de l’image échoue après l’extraction des indicateurs | L’underlay peut être découpé ou désactivé, entraînant une zone blanche. | Ajustez les indicateurs (`UnderlayIsOn = true`, `ClippingIsOn = false`) avant de rendre l’image finale. |

## Questions fréquemment posées

### Q1 : Puis‑je utiliser Aspose.CAD pour .NET avec d'autres formats de fichiers CAD ?

R1 : Aspose.CAD prend en charge divers formats CAD, dont DWG, DXF, DGN et bien d’autres. Consultez la documentation pour la liste complète.

### Q2 : Une licence temporaire est‑elle disponible pour Aspose.CAD pour .NET ?

R2 : Oui, vous pouvez obtenir une licence temporaire **[ici](https://purchase.aspose.com/temporary-license/)**.

### Q3 : Où puis‑je trouver du support pour Aspose.CAD pour .NET ?

R3 : Visitez le forum de support **[ici](https://forum.aspose.com/c/cad/19)** pour obtenir de l’aide.

### Q4 : Comment acheter Aspose.CAD pour .NET ?

R4 : Achetez la bibliothèque **[ici](https://purchase.aspose.com/buy)**.

### Q5 : Une version d’essai gratuite est‑elle disponible ?

R5 : Oui, vous pouvez accéder à l’essai gratuit **[ici](https://releases.aspose.com/)**.

## Conclusion

Félicitations ! Vous avez appris à **convertir DWG en image** tout en maîtrisant **la lecture des indicateurs d'underlay** avec Aspose.CAD pour .NET. Grâce à ces connaissances, vous pouvez :

- Rendre des dessins DWG sous forme d’images raster pour le web ou les rapports.  
- Inspecter et manipuler les propriétés d’underlay afin d’assurer un affichage correct.  
- Déboguer les problèmes de visibilité, de découpage et de rendu monochrome avant la génération de l’image finale.

N’hésitez pas à explorer d’autres fonctionnalités d’Aspose.CAD telles que la gestion des calques, l’extraction de texte et la conversion par lots pour enrichir davantage vos flux de travail d’automatisation CAD.

---

**Last Updated:** 2026-04-09  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}