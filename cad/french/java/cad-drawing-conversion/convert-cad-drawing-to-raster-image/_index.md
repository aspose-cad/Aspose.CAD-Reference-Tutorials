---
date: 2026-10-25
description: Apprenez à convertir DWG en PNG et à enregistrer les fichiers CAD au
  format PNG avec Aspose.CAD pour Java, en gérant les fichiers DWG, DXF, DWF et autres
  fichiers CAD grâce à une rasterization haute performance.
keywords:
- convert dwg to png
- save cad as png
- cad to png conversion
- how to rasterize cad
- convert dwg raster image
lastmod: 2026-10-25
linktitle: Convertir le dessin CAD en format d'image raster
og_description: Convertissez rapidement DWG en PNG avec Aspose.CAD pour Java. Ce guide
  vous montre comment enregistrer les fichiers CAD au format PNG, configurer les options
  de rasterization et gérer les batch conversions — idéal pour les web previews et
  les reports.
og_image_alt: 'Developer guide: convert DWG to PNG using Aspose.CAD Java API'
og_title: Comment convertir DWG en PNG avec Aspose.CAD pour Java
schemas:
- author: Aspose
  dateModified: '2026-10-25'
  description: Learn how to convert DWG to PNG and save CAD as PNG using Aspose.CAD
    for Java, handling DWG, DXF, DWF and other CAD files with high‑performance rasterization.
  headline: How to convert DWG to PNG using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to convert DWG to PNG and save CAD as PNG using Aspose.CAD
    for Java, handling DWG, DXF, DWF and other CAD files with high‑performance rasterization.
  name: How to convert DWG to PNG using Aspose.CAD for Java
  steps:
  - name: '**Java Development Kit** – JDK 8 or later installed and configured.'
    text: '**Java Development Kit** – JDK 8 or later installed and configured.'
  - name: '**Aspose.CAD for Java** – download the latest JAR from the official Aspose.CAD
      for Java releases page [ Aspose.CAD for Java download page ](https://releases.aspose.com/cad/java/).'
    text: '**Aspose.CAD for Java** – download the latest JAR from the official Aspose.CAD
      for Java releases page [ Aspose.CAD for Java download page ](https://releases.aspose.com/cad/java/).'
  - name: '**A DWG file** – any valid DWG, DXF or DWF drawing you want to rasterize.'
    text: '**A DWG file** – any valid DWG, DXF or DWF drawing you want to rasterize.'
  type: HowTo
- questions:
  - answer: Set the `backgroundColor` property on `CadRasterizationOptions` before
      creating the `PngOptions` instance.
    question: How do I convert a DWG file to PNG with a custom background color?
  - answer: Yes—wrap the loading, rasterization, and saving steps inside a loop that
      iterates over your file collection.
    question: Can I process multiple CAD files in one batch operation?
  - answer: The default DPI of 96 produces screen‑quality PNGs; raise the DPI to 300
      for high‑resolution print output.
    question: What image quality can I expect from the default settings?
  - answer: Absolutely. PNGs are saved with an alpha channel by default, and you can
      explicitly set a transparent background in the rasterization options.
    question: Does Aspose.CAD support transparent backgrounds in PNG output?
  - answer: Yes—replace `PngOptions` with `JpegOptions` or `BmpOptions` while reusing
      the same `CadRasterizationOptions`.
    question: Can I convert CAD files to other raster formats like JPEG or BMP?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java CAD processing
- raster image conversion
title: Comment convertir DWG en PNG avec Aspose.CAD pour Java
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment convertir DWG en PNG avec Aspose.CAD pour Java

## Introduction

Dans ce tutoriel, vous apprendrez comment **convertir DWG en PNG** avec Aspose.CAD pour Java. Convertir des dessins CAO en formats d'image raster comme PNG est un besoin fréquent lorsque vous souhaitez intégrer des dessins dans des pages web, générer des vignettes ou les inclure dans des rapports PDF. Aspose.CAD propose une solution pure‑Java qui gère DWG, DXF, DWF et plus de 50 autres formats CAO sans aucune dépendance native, offrant des temps de conversion inférieurs à une seconde pour les dessins typiques.

## Réponses rapides
- **Quelle bibliothèque gère la conversion ?** Aspose.CAD for Java.  
- **Puis-je convertir DWG en PNG ?** Oui – la même API fonctionne pour DWG, DXF, DWF et de nombreux autres formats.  
- **Ai‑je besoin d'une licence pour la production ?** Une licence commerciale est requise pour une utilisation autre que l'évaluation.  
- **La taille du raster est‑elle configurable ?** Absolument – vous pouvez définir la largeur, la hauteur, le DPI et la couleur d'arrière‑plan via les options de rasterisation.  
- **Combien de temps prend la conversion ?** Typiquement moins d'une seconde pour les dessins standards ; les fichiers plus volumineux de plusieurs centaines de pages peuvent prendre quelques secondes.

## Comment convertir DWG en PNG avec Aspose.CAD

Chargez le fichier CAD, configurez les options de rasterisation, créez les options spécifiques à PNG, puis enregistrez l'image raster. Ce flux de bout en bout convertit les données DWG vectorielles en PNG pixelisé tout en conservant les épaisseurs de ligne, les calques et les couleurs.

## Pourquoi utiliser Aspose.CAD pour Java ?

Aspose.CAD prend en charge **plus de 50** formats d'entrée et de sortie — y compris DWG, DXF, DWF, SVG et les formats raster comme PNG, JPEG et BMP. Il peut traiter des fichiers jusqu'à **500 Mo** sans charger le document complet en mémoire, ce qui le rend idéal pour les pipelines batch. La bibliothèque fonctionne sur n'importe quel environnement Java 8+, ne nécessite aucune DLL externe et offre un contrôle fin sur la résolution, la couleur d'arrière‑plan et la qualité de rendu, le tout à partir de quelques lignes de code.

## Prérequis

Avant de commencer, assurez-vous d'avoir :

1. **Java Development Kit** – JDK 8 ou ultérieur installé et configuré.  
2. **Aspose.CAD for Java** – téléchargez le dernier JAR depuis la page officielle des versions d'Aspose.CAD for Java [ Aspose.CAD for Java download page ](https://releases.aspose.com/cad/java/).  
3. **Un fichier DWG** – tout dessin DWG, DXF ou DWF valide que vous souhaitez rasteriser.  

Ajoutez le JAR Aspose.CAD au classpath de votre projet (Maven, Gradle ou inclusion manuelle).

## Importer les espaces de noms

Le package `com.aspose.cad` contient toutes les classes dont vous avez besoin pour charger, rasteriser et enregistrer des dessins CAD.

La classe `Image` est le point d'entrée d'Aspose.CAD pour charger n'importe quel fichier CAD pris en charge en mémoire.  
La classe `CadRasterizationOptions` vous permet de définir comment les données vectorielles sont transformées en pixels (taille, DPI, arrière‑plan, etc.).  
La classe `PngOptions` spécifie les paramètres de sortie spécifiques à PNG tels que le niveau de compression et la gestion de la transparence.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Maintenant, détaillons le processus de conversion d'un dessin CAD en image raster en étapes détaillées :

## Étape 1 : charger le dessin CAD

La méthode `Image.load()` lit le fichier source et crée une représentation en mémoire que vous pourrez rasteriser ultérieurement.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Étape 2 : définir les options de rasterisation

Créez une instance de `CadRasterizationOptions` et configurez la largeur, la hauteur, le DPI et la couleur d'arrière‑plan. Ces paramètres déterminent la qualité et la taille du PNG résultant.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

## Étape 3 : créer les options d'image

Instanciez `PngOptions` et affectez-lui les options de rasterisation configurées précédemment. Cela lie les paramètres de conversion vecteur‑vers‑raster au format de sortie PNG.

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

## Étape 4 : enregistrer l'image raster

Appelez `image.save()` avec l'instance `PngOptions` et le chemin de fichier cible. La méthode écrit le PNG rasterisé sur le disque, finalisant la conversion.

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

Répétez ces étapes pour chaque fichier CAD que vous devez traiter, et vous disposerez d'un pipeline fiable de **conversion cad en png**.

## Cas d'utilisation courants et astuces

- **Génération d'aperçus web** – Convertissez de gros fichiers DWG en vignettes PNG légères pour un affichage instantané dans le navigateur.  
- **Intégration dans les rapports** – Utilisez la sortie PNG dans les rapports PDF ou Word où les formats CAD natifs ne sont pas pris en charge.  
- **Conversion par lots** – Parcourez un dossier de fichiers CAD, en appliquant les mêmes paramètres de rasterisation pour des résultats cohérents.  
- **Astuce pro :** augmentez `rasterizationOptions.setResolution()` à 300 DPI pour des images prêtes à l'impression ; le 96 DPI par défaut est optimal pour l'affichage à l'écran.  
- **Comment convertir DWG vers d'autres formats** – Remplacez `PngOptions` par `JpegOptions` ou `BmpOptions` tout en conservant la même configuration de rasterisation.

## Conclusion

En suivant les étapes ci‑dessus, vous pouvez efficacement **convertir DWG en PNG**, **enregistrer CAD en PNG**, ou effectuer toute **conversion cad en png** requise par votre application. Aspose.CAD for Java vous offre un contrôle total sur la résolution, la couleur d'arrière‑plan et le format de sortie, faisant de lui la solution de référence pour les aperçus web, les pipelines de documentation et le traitement par lots à grande échelle.

## Questions fréquentes

**Q : Comment convertir un fichier DWG en PNG avec une couleur d'arrière‑plan personnalisée ?**  
R : Définissez la propriété `backgroundColor` sur `CadRasterizationOptions` avant de créer l'instance `PngOptions`.

**Q : Puis‑je traiter plusieurs fichiers CAD en une seule opération batch ?**  
R : Oui — encapsulez les étapes de chargement, rasterisation et enregistrement dans une boucle qui parcourt votre collection de fichiers.

**Q : Quelle qualité d'image puis‑je attendre des paramètres par défaut ?**  
R : Le DPI par défaut de 96 produit des PNG de qualité écran ; augmentez le DPI à 300 pour une sortie d'impression haute résolution.

**Q : Aspose.CAD prend‑il en charge les arrière‑plans transparents dans la sortie PNG ?**  
R : Absolument. Les PNG sont enregistrés avec un canal alpha par défaut, et vous pouvez définir explicitement un arrière‑plan transparent dans les options de rasterisation.

**Q : Puis‑je convertir des fichiers CAD vers d'autres formats raster comme JPEG ou BMP ?**  
R : Oui — remplacez `PngOptions` par `JpegOptions` ou `BmpOptions` tout en réutilisant les mêmes `CadRasterizationOptions`.

---

**Dernière mise à jour :** 2026-10-25  
**Testé avec :** Aspose.CAD for Java 24.12 (latest)  
**Auteur :** Aspose

## Tutoriels associés

- [Ajuster automatiquement la taille du dessin CAD et convertir DWG en BMP avec Aspose.CAD for Java](/cad/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/)
- [Enregistrer DWG en JPEG avec prise en charge des calques en Java avec Aspose.CAD](/cad/java/advanced-cad-features/support-of-layers-in-cad/)
- [Enregistrer CAD en PNG – Exporter des objets OLE avec Aspose.CAD for Java](/cad/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}