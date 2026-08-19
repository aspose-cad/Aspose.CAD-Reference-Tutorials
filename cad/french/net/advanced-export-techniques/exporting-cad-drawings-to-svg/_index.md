---
date: 2026-03-07
description: Apprenez à exporter le CAD en SVG en utilisant Aspose.CAD pour .NET,
  personnalisez la couleur du SVG et convertissez les fichiers DWG en SVG efficacement.
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Exporter le CAD vers SVG – Exportation des dessins CAD au format SVG - Guide
  Aspose.CAD
url: /fr/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter CAD en SVG – Exportation de dessins CAD au format SVG

## Introduction

Exporter des dessins CAD au format SVG est une exigence courante lorsque vous avez besoin de graphiques indépendants de la résolution pour les pages web, les rapports ou les visualisations interactives. Dans ce tutoriel, vous apprendrez **comment exporter CAD en SVG** avec Aspose.CAD pour .NET, explorerez les options pour **personnaliser la couleur SVG**, et verrez comment **convertir DWG en SVG** (ou DXF en SVG) en quelques lignes de code seulement. Les étapes sont rapides, l'API est intuitive, et les fichiers SVG résultants s'adaptent parfaitement à tout appareil.

## Réponses rapides
- **Quelle bibliothèque gère la conversion ?** Aspose.CAD for .NET.  
- **Puis-je changer le mode couleur ?** Oui – utilisez `SvgColorMode` pour définir grayscale, black‑white, ou full‑color.  
- **Quels formats CAD sont pris en charge ?** DWG, DXF, et bien d'autres (see Aspose.CAD docs).  
- **Ai‑je besoin d'une licence pour le développement ?** Une licence temporaire est disponible pour les tests.  
- **Combien de temps prend la conversion ?** Typiquement moins d'une seconde pour les dessins standards.

## Qu’est‑ce que « exporter CAD en SVG » ?

Exporter CAD en SVG signifie prendre un fichier CAD natif (tel que DWG ou DXF) et le rendre au format Scalable Vector Graphics. SVG est basé sur XML, léger, et peut être stylisé avec CSS—ce qui le rend idéal pour les applications web et mobiles modernes.

## Pourquoi utiliser Aspose.CAD pour exporter CAD en SVG ?

- **Aucune dépendance externe** – API .NET pure, aucune installation AutoCAD requise.  
- **Contrôle fin** – vous pouvez **personnaliser la couleur SVG**, décider si le texte est conservé sous forme de formes, et choisir les options de rasterisation.  
- **Large prise en charge des formats** – le même code fonctionne pour **convertir DWG en SVG**, **convertir DXF en SVG**, et d’autres formats, simplifiant votre base de code.  
- **Haute performance** – optimisé pour la vitesse et une faible consommation mémoire, adapté au traitement par lots.

## Prérequis

- **Aspose.CAD for .NET** installé. Vous pouvez télécharger la bibliothèque [ici](https://releases.aspose.com/cad/net/).  
- Un environnement de développement .NET (Visual Studio, Rider, ou le .NET CLI).  
- Un fichier CAD (DWG ou DXF) que vous souhaitez convertir.

## Importer les espaces de noms

Tout d'abord, importez les espaces de noms requis dans votre projet afin que les classes soient disponibles.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Guide étape par étape

### Étape 1 : Définir le répertoire du document  
Définissez le dossier où se trouve votre fichier CAD source et où le fichier SVG de sortie sera enregistré.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### Étape 2 : Charger le dessin CAD  
Utilisez `Image.Load` pour lire le fichier DWG (ou DXF). Cela fonctionne pour les scénarios **load DWG .NET**.

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### Étape 3 : Configurer les options d’exportation SVG  
Ajustez les paramètres d’exportation selon vos besoins. Ici, nous définissons le mode couleur en niveaux de gris et forçons tout le texte à être rendu sous forme de formes vectorielles.

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### Étape 4 : Enregistrer le fichier SVG  
Enfin, écrivez le fichier SVG sur le disque. Cette étape **enregistre le CAD en SVG** et finalise la conversion.

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

En suivant ces quatre étapes concises, vous pouvez **convertir DWG en SVG** (ou **convertir DXF en SVG**) avec un contrôle total sur l’apparence du résultat.

## Problèmes courants et solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| **Sortie SVG vide** | Le chemin du fichier source est incorrect ou le fichier est corrompu. | Vérifiez `MyDir` et assurez‑vous que le fichier CAD s’ouvre sans erreurs. |
| **Les couleurs sont incorrectes** | `SvgColorMode` défini en niveaux de gris par inadvertance. | Changez `options.ColorType` en `SvgColorMode.FullColor` pour conserver les couleurs originales. |
| **Texte manquant** | `TextAsShapes` défini sur `false` et le visualiseur ne prend pas en charge les polices intégrées. | Conservez `TextAsShapes = true` ou intégrez les polices requises dans le SVG. |

## FAQ

### Q1 : Aspose.CAD est‑il compatible avec tous les formats CAD ?
A1 : Aspose.CAD prend en charge divers formats CAD, y compris DWG et DXF, garantissant une large compatibilité.

### Q2 : Puis‑je personnaliser le mode couleur lors de l’exportation en SVG ?
A2 : Oui, Aspose.CAD vous permet de choisir le mode couleur, offrant une flexibilité dans le résultat.

### Q3 : Des licences temporaires sont‑elles disponibles à des fins de test ?
A3 : Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/) pour évaluation.

### Q4 : Où puis‑je trouver la documentation détaillée d’Aspose.CAD ?
A4 : La documentation est disponible [ici](https://reference.aspose.com/cad/net/).

### Q5 : Comment puis‑je obtenir du support ou poser des questions liées à Aspose.CAD ?
A5 : Visitez le forum communautaire [ici](https://forum.aspose.com/c/cad/19) pour le support et les discussions.

## Questions fréquemment posées

**Q : Puis‑je utiliser ce code avec .NET Core ou .NET 6 ?**  
A : Absolument. Aspose.CAD pour .NET est compatible avec .NET Framework, .NET Core, et .NET 5/6+.

**Q : Est‑il possible d’exporter uniquement une mise en page ou un calque spécifique ?**  
A : Oui. Utilisez `SvgOptions` pour définir `PageIndex` ou filtrer les calques avant l’enregistrement.

**Q : Comment intégrer des styles CSS personnalisés dans le SVG généré ?**  
A : Après l’enregistrement, vous pouvez post‑traiter le XML du SVG pour injecter des éléments `<style>`, ou utiliser `options.CustomCss` si disponible dans les versions plus récentes.

**Q : Quelles sont les limites de taille du fichier CAD source ?**  
A : La bibliothèque gère les gros fichiers, mais la consommation de mémoire augmente avec la complexité. Pour des dessins très volumineux, envisagez de traiter les pages individuellement.

**Q : La conversion préserve‑t‑elle les épaisseurs et les types de ligne ?**  
A : Par défaut, les épaisseurs de ligne sont conservées. Vous pouvez ajuster les options de rendu dans `SvgOptions` pour un contrôle plus fin.

---

**Dernière mise à jour :** 2026-03-07  
**Testé avec :** Aspose.CAD for .NET 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}