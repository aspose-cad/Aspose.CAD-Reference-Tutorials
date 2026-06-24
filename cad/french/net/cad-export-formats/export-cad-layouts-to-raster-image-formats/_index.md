---
date: 2026-03-21
description: Apprenez à convertir le DXF en PNG et d’autres formats raster à l’aide
  d’Aspose.CAD pour .NET. Suivez notre guide pas à pas pour une exportation fluide
  des calques CAD.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Convertir DXF en PNG avec Aspose.CAD pour .NET
url: /fr/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter des mises en page CAD vers des formats d'image raster dans Aspose.CAD pour .NET

## Introduction

Vous cherchez à **convertir dxf en png** et d'autres formats d'image raster de manière efficace avec Aspose.CAD pour .NET ? Ce guide pas à pas vous accompagnera tout au long du processus, en fournissant des instructions détaillées et des extraits de code pour rendre la tâche fluide. Que vous soyez un développeur chevronné ou un novice d’Aspose.CAD, ce tutoriel s'adresse à tous les niveaux d'expertise.

### Réponses rapides
- **Quelle bibliothèque gère la conversion ?** Aspose.CAD pour .NET  
- **Format principal pris en charge immédiatement ?** Images raster JPEG, PNG, BMP et TIFF  
- **Puis-je exporter des calques CAD spécifiques ?** Oui – utilisez `CadRasterizationOptions.Layers` pour cibler des calques individuels  
- **Ai‑je besoin d’une licence pour la production ?** Une licence valide d’Aspose.CAD est requise pour une utilisation non‑essai  
- **Versions .NET prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  

## Qu’est‑ce que **convert dxf to png** ?

Convertir un fichier DXF (Drawing Exchange Format) en PNG signifie rasteriser des données CAD vectorielles en une image à base de pixels. Cela est utile lorsque vous devez intégrer des dessins CAD dans des pages web, des rapports ou tout environnement ne supportant que les graphiques raster.

## Pourquoi exporter les calques CAD séparément ?

Exporter les calques CAD individuellement vous donne un contrôle granulaire sur le rendu visuel, réduit la taille du fichier pour chaque image et vous permet d'appliquer un style ou un post‑traitement spécifique à chaque calque. Ceci est particulièrement pratique pour les grands dessins d’ingénierie où seul un sous‑ensemble de calques est pertinent pour un public donné.

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous de disposer de :

- **Bibliothèque Aspose.CAD pour .NET** – téléchargez‑la depuis le [site Aspose.CAD](https://releases.aspose.com/cad/net/).  
- **Fichier de dessin CAD** – un fichier DXF (par ex., `conic_pyramid.dxf`) que vous souhaitez convertir en formats raster.  

## Importer les espaces de noms

Dans votre projet .NET, importez les espaces de noms nécessaires pour exploiter les fonctionnalités d’Aspose.CAD. Ajoutez les espaces de noms suivants au début de votre code :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Comment **convert dxf to png** – Guide étape par étape

### Étape 1 : Charger le dessin CAD

Chargez d’abord le fichier DXF dans un objet `Image`. Cet objet représente l’ensemble du dessin CAD en mémoire.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### Étape 2 : Créer `CadRasterizationOptions`

Configurez les paramètres de rasterisation tels que les dimensions de sortie et la résolution. Ces options contrôlent la façon dont les données vectorielles sont rasterisées.

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### Étape 3 : Spécifier les calques (Exporter les calques CAD)

Si vous ne avez besoin que d’un calque particulier, indiquez son nom ici. Cela montre comment **exporter les calques CAD** individuellement.

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### Étape 4 : Choisir un format d'image – Enregistrer le CAD en PNG (ou JPEG)

Créez un objet d’options spécifique au format d’image. Remplacez `JpegOptions` par `PngOptions` lorsque vous voulez **enregistrer le CAD en png**.

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Astuce :** Pour générer des fichiers PNG, il suffit d’instancier `new PngOptions()` au lieu de `JpegOptions`.

### Étape 5 : Exporter au format JPEG (ou PNG)

Enfin, enregistrez l’image rasterisée sur le disque. L’extension du fichier détermine le format de sortie.

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

Lorsque vous remplacez `JpegOptions` par `PngOptions`, le même code **convertira dxf en png** et produira un fichier `.png`.

### Étape supplémentaire : Convertir tous les calques

Si vous devez **convertir le CAD en raster** pour chaque calque du dessin, appelez la méthode d’assistance ci‑dessous. Elle parcourt tous les calques et enregistre chacun comme une image séparée.

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *Remarque :* L’implémentation de `ConvertAllLayersToRasterImageFormats` fait partie de la suite d’exemples complète d’Aspose.CAD et montre le traitement par lots des calques.

## Problèmes courants & Dépannage

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| Image blanche ou vide | Options de rasterisation non définies (ex. `PageWidth`/`PageHeight` = 0) | Assurez‑vous que `PageWidth` et `PageHeight` ont des valeurs positives |
| Calques manquants | Nom de calque incorrect dans le tableau `Layers` | Vérifiez le nom exact du calque dans le fichier CAD (sensible à la casse) |
| PNG de mauvaise qualité | DPI par défaut trop bas | Définissez `rasterizationOptions.Resolution = 300;` pour une meilleure qualité |

## Questions fréquentes (Original)

### Q1 : Puis‑je utiliser d’autres formats d’image pour l’exportation ?

R1 : Oui, vous pouvez. Remplacez simplement `JpegOptions` par les options du format souhaité, comme `PngOptions` ou `BmpOptions`.

### Q2 : Existe‑t‑il une version d’essai disponible ?

R2 : Oui, vous pouvez explorer les fonctionnalités d’Aspose.CAD en téléchargeant la version d’essai [ici](https://releases.aspose.com/).

### Q3 : Comment obtenir du support pour Aspose.CAD ?

R3 : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire ou envisagez d’acheter une licence pour un support dédié.

### Q4 : Des licences temporaires sont‑elles disponibles ?

R4 : Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Où trouver la documentation ?

R5 : Consultez la documentation détaillée [ici](https://reference.aspose.com/cad/net/).

## FAQ supplémentaire

**Q : Puis‑je exporter tous les calques en une seule commande ?**  
R : Oui, utilisez la méthode `ConvertAllLayersToRasterImageFormats` présentée ci‑dessus.

**Q : Aspose.CAD prend‑il en charge les formats vectoriels comme SVG ?**  
R : Il cible principalement les formats raster, mais vous pouvez exporter en PDF qui conserve les données vectorielles.

**Q : Comment contrôler la couleur d’arrière‑plan du PNG exporté ?**  
R : Définissez `rasterizationOptions.BackgroundColor` sur la `Color` souhaitée avant l’enregistrement.

**Q : Est‑il possible d’exporter une seule mise en page au lieu du dessin complet ?**  
R : Oui, configurez `rasterizationOptions.Layouts` pour spécifier le(s) nom(s) de mise en page à rasteriser.

## Conclusion

Vous avez maintenant appris comment **convertir dxf en png**, **exporter les calques CAD** et **enregistrer le CAD en png** ou JPEG avec Aspose.CAD pour .NET. En ajustant `CadRasterizationOptions` et en échangeant les options de format d’image, vous pouvez adapter la conversion à pratiquement n’importe quel rendu raster dont vous avez besoin. Explorez les autres options de format dans l’API Aspose.CAD pour élargir votre flux de travail CAD‑vers‑raster.

---

**Dernière mise à jour :** 2026-03-21  
**Testé avec :** Aspose.CAD pour .NET 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}