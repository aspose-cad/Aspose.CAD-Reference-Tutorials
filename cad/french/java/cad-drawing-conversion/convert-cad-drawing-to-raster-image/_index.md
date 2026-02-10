---
date: 2025-12-19
description: Apprenez à enregistrer des fichiers CAD au format PNG avec Aspose.CAD
  pour Java, en convertissant efficacement les fichiers DWG, DXF et autres fichiers
  CAD en images raster.
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: Enregistrer le CAD au format PNG – Convertir un dessin CAD en format d'image
  raster à l'aide d'Aspose.CAD pour Java
url: /fr/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer CAD au format PNG – Convertir un dessin CAD en format d'image raster avec Aspose.CAD pour Java

## Introduction

Dans ce tutoriel, vous apprendrez comment **enregistrer CAD au format PNG** en utilisant Aspose.CAD pour Java. Convertir des dessins CAD en formats d'image raster comme PNG est une exigence fréquente pour les aperçus web, la documentation et les rapports. Aspose.CAD offre une méthode fiable et haute‑performance pour effectuer une **cad to png conversion** pour DWG, DXF, DWF et de nombreux autres types de fichiers CAD.

## Réponses rapides
- **Quelle bibliothèque gère la conversion ?** Aspose.CAD for Java.  
- **Puis-je convertir DWG en PNG ?** Oui – la même API fonctionne pour DWG, DXF et d'autres formats.  
- **Ai-je besoin d'une licence pour la production ?** Une licence commerciale est requise pour une utilisation non‑évaluation.  
- **La taille du raster est‑elle configurable ?** Absolument – vous pouvez définir la largeur, la hauteur et le DPI via les options de rasterisation.  
- **Combien de temps prend la conversion ?** Généralement moins d'une seconde pour les dessins standards ; les fichiers plus volumineux peuvent prendre plus de temps.

## Qu’est‑ce que « save CAD as PNG » ?
Enregistrer CAD au format PNG signifie rasteriser des données CAD vectorielles en une image basée sur des pixels (PNG). Ce processus, souvent appelé **convert cad to raster**, préserve la fidélité visuelle tout en créant un format facile à intégrer dans les pages web, les e‑mails ou les rapports.

## Pourquoi utiliser Aspose.CAD pour Java ?
- **Large prise en charge des formats** – fonctionne avec DWG, DXF, DWF, et plus.  
- **Aucune dépendance externe** – Java pur, pas de DLL natives.  
- **Contrôle fin** – personnalisez la résolution, la couleur d'arrière‑plan et la qualité de rendu.  
- **Performance évolutive** – adaptée au traitement par lots ou à la conversion à la volée.

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous que les prérequis suivants sont en place :

1. Environnement de développement Java : assurez‑vous d'avoir un environnement Java fonctionnel installé sur votre machine.  
2. Bibliothèque Aspose.CAD : téléchargez et intégrez la bibliothèque Aspose.CAD pour Java dans votre projet. Vous pouvez trouver la bibliothèque [ici](https://releases.aspose.com/cad/java/).

## Importer les espaces de noms

Dans votre code Java, importez les espaces de noms nécessaires pour exploiter efficacement les fonctionnalités d'Aspose.CAD pour Java. Cette étape est cruciale pour accéder aux classes et méthodes requises.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Décomposons maintenant le processus de conversion d'un dessin CAD en image raster en étapes détaillées :

## Étape 1 : Charger le dessin CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Dans cette étape, nous chargeons le dessin CAD depuis le chemin de fichier spécifié en utilisant la méthode `Image.load()`.

## Étape 2 : Définir les options de rasterisation

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

Créez une instance de `CadRasterizationOptions` et définissez la largeur et la hauteur de la page pour l'image rasterisée.

## Étape 3 : Créer les options d'image

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

Créez une instance de `PngOptions` pour l'image résultante et définissez les options de rasterisation vectorielle.

## Étape 4 : Enregistrer l'image raster

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

Enregistrez l'image raster résultante dans le répertoire spécifié en utilisant la méthode `image.save()`.

Répétez ces étapes pour vos fichiers CAD spécifiques, et vous aurez réussi à **convertir CAD drawing image** en PNG.

## Cas d’utilisation courants & astuces

- **Génération d’aperçus web** – Convertissez de gros fichiers DWG en miniatures PNG légères pour un affichage rapide dans le navigateur.  
- **Intégration dans les rapports** – Utilisez la sortie PNG dans les rapports PDF ou Word où les fichiers CAD vectoriels ne sont pas pris en charge.  
- **Conversion par lots** – Parcourez un dossier de fichiers CAD et appliquez les mêmes paramètres de rasterisation pour une sortie cohérente.  
- **Astuce pro :** Ajustez `rasterizationOptions.setResolution()` pour augmenter le DPI pour des impressions haute résolution.

## Conclusion

En conclusion, convertir des dessins CAD en images raster avec Aspose.CAD pour Java est un processus simple. En suivant les étapes décrites dans ce tutoriel, vous pouvez intégrer efficacement cette fonctionnalité dans vos applications Java et effectuer **convert dwg to png**, **export cad as png**, ou toute autre **cad to png conversion** dont vous avez besoin.

## Questions fréquemment posées

**Q : Comment convertir un fichier DWG en PNG avec une couleur d'arrière‑plan personnalisée ?**  
**R :** Définissez la propriété `backgroundColor` sur `CadRasterizationOptions` avant de créer l'instance `PngOptions`.

**Q : Est‑il possible de convertir plusieurs fichiers CAD en une seule opération par lots ?**  
**R :** Oui—encapsulez les étapes de chargement, rasterisation et sauvegarde dans une boucle qui parcourt votre collection de fichiers.

**Q : Quelle qualité d'image puis‑je attendre des paramètres par défaut ?**  
**R :** Le DPI par défaut (96) donne des PNG de qualité écran ; augmentez le DPI pour des résultats de qualité impression.

**Q : Aspose.CAD prend‑il en charge les arrière‑plans transparents dans la sortie PNG ?**  
**R :** Absolument. Par défaut, les PNG sont enregistrés avec un canal alpha ; vous pouvez également spécifier un arrière‑plan transparent dans les options de rasterisation.

**Q : Puis‑je convertir des fichiers CAD vers d'autres formats raster comme JPEG ou BMP ?**  
**R :** Oui—remplacez `PngOptions` par `JpegOptions` ou `BmpOptions` tout en conservant les mêmes paramètres de rasterisation.

**Dernière mise à jour :** 2025-12-19  
**Testé avec :** Aspose.CAD pour Java 24.12 (dernière version)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}