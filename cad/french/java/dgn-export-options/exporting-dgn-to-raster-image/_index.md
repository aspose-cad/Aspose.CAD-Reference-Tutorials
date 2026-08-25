---
date: 2026-05-25
description: Apprenez à exporter des fichiers DGN vers des images JPEG avec Aspose.CAD
  for Java. Ce guide étape par étape vous montre comment convertir DGN en JPEG efficacement.
keywords:
- how to export dgn
- convert dgn to jpeg
- java convert cad to image
linktitle: Exportation de DGN au format AutoCAD vers un format d'image raster
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  headline: How to Export DGN to JPEG with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  name: How to Export DGN to JPEG with Aspose.CAD for Java
  steps:
  - name: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
    text: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
  - name: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
    text: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports over 30 vector formats, including DWG, DXF, DWF,
      and SVG, enabling a single API for many conversion scenarios.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Refer to the official docs [here](https://reference.aspose.com/cad/java/).
    question: Where can I find documentation for Aspose.CAD for Java?
  - answer: Visit the support forum [here](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can buy a license [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Comment exporter DGN en JPEG avec Aspose.CAD for Java
url: /fr/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Conversion Java DGN en JPEG avec le tutoriel Aspose.CAD

## Introduction

Dans ce guide complet, vous découvrirez **how to export dgn** fichiers en images JPEG à l'aide d'Aspose.CAD pour Java. Que vous construisiez un service de traitement par lots ou que vous ajoutiez une génération d'aperçu à la volée à un visualiseur CAD, ce tutoriel vous accompagne à chaque étape, du chargement du fichier source à l'enregistrement du rendu raster. Vous verrez également des conseils pratiques pour garder votre code propre et performant.

## Réponses rapides
- **Quelle bibliothèque faut‑il ?** Aspose.CAD for Java (téléchargez [ici](https://releases.aspose.com/cad/java/)).
- **Puis‑je convertir DGN en JPEG en une seule ligne ?** Oui – chargez avec `CadImage.load` et appelez `save` avec `JpegOptions`.
- **Une licence est‑elle requise pour la production ?** Oui, une licence commerciale supprime le filigrane d'évaluation.
- **Quelle version de Java est prise en charge ?** Java 8 à 17 sont entièrement supportées.
- **Quelle taille de DGN puis‑je traiter ?** Les fichiers jusqu'à 2 GB sont gérés sans charger le fichier complet en mémoire.

## Qu’est‑ce que “how to export dgn” ?
*“How to export dgn”* désigne le processus de conversion d'un fichier de conception MicroStation DGN en un autre format, généralement une image raster telle que JPEG, pour faciliter la visualisation ou le partage. Cette conversion permet aux parties prenantes qui ne disposent pas de logiciel CAD d'inspecter les conceptions, d'intégrer des images dans des documents ou de générer des miniatures pour des galeries web, améliorant ainsi l'accessibilité et la collaboration entre les équipes.

## Pourquoi utiliser Aspose.CAD pour Java ?
Aspose.CAD prend en charge **plus de 30 formats CAD** (y compris DGN, DWG, DXF) et peut rendre des fichiers **jusqu’à 2 GB** sans nécessiter l'application CAD d'origine. Son moteur raster traite les dessins multi‑pages à **> 50 fps** sur du matériel serveur standard, offrant une sortie JPEG de haute qualité avec un appel d'API unique.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

1. **Bibliothèque Aspose.CAD** – téléchargez le dernier JAR depuis le site officiel [ici](https://releases.aspose.com/cad/java/). Vous pouvez également explorer d'autres versions de produits [ici](https://releases.aspose.com/).  
2. **Kit de développement Java (JDK)** – Java 8 ou version supérieure installé sur votre machine.  
3. **IDE** – IntelliJ IDEA, Eclipse ou tout éditeur compatible Java de votre choix.

## Importer les packages

Dans votre projet Java, importez les classes Aspose.CAD nécessaires :

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Comment exporter dgn en JPEG avec Aspose.CAD en Java ?

La classe `CadImage` représente un document CAD chargé en mémoire, offrant des méthodes de rendu et d’enregistrement.

Chargez votre fichier DGN avec `CadImage.load("source.dgn")`, configurez `JpegOptions` (qualité et résolution), définissez les `RasterizationOptions` appropriées telles que les dimensions de la page et la couleur d’arrière‑plan, puis appelez `image.save("output.jpg", jpegOptions)`. Ce flux en trois étapes gère la conversion vecteur‑vers‑raster, préserve les épaisseurs de ligne et écrit un fichier JPEG de haute qualité en moins d’une seconde pour les dessins typiques.

## Étape 1 : Charger le fichier DGN

La classe `CadImage` représente un document CAD chargé en mémoire.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Étape 2 : Créer l’objet JpegOptions

`JpegOptions` définit les paramètres spécifiques à la sortie JPEG, tels que la qualité de compression et la résolution.

```java
ImageOptionsBase options = new JpegOptions();
```

## Étape 3 : Attribuer les options de rasterisation

`RasterizationOptions` détermine la façon dont les graphiques vectoriels sont rasterisés, incluant la taille de la page, le DPI, la couleur d’arrière‑plan et l’anticrénelage.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Étape 4 : Enregistrer l’image convertie

L’appel à `save` écrit l’image raster sur le disque en utilisant les options que vous avez fournies.

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

### Cas d’utilisation courants

- **Génération d’aperçus web** – Convertir les dessins d’ingénierie en miniatures JPEG légères pour un affichage rapide dans les navigateurs.  
- **Archivage par lots** – Automatiser la conversion de milliers de fichiers DGN en JPEG pour un stockage à long terme sans nécessiter MicroStation.  
- **Reporting** – Intégrer des instantanés CAD dans des rapports PDF ou HTML directement depuis le code Java.

### Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **L’image apparaît vide** | Assurez‑vous que `RasterizationOptions.setPageWidth/Height` correspond aux dimensions du dessin, et définissez un arrière‑plan non transparent. |
| **Qualité de sortie faible** | Augmentez `JpegOptions.setQuality(100)` et choisissez un DPI plus élevé (par ex., `RasterizationOptions.setResolution(300)`). |
| **Erreurs de mémoire insuffisante** | Utilisez `CadImage.load` avec `loadOptions.setLoadMode(LoadMode.Memory)` pour diffuser les gros fichiers. |

## Questions fréquentes

**Q : Puis‑je utiliser Aspose.CAD pour Java avec d’autres formats de fichiers CAD ?**  
R : Oui, Aspose.CAD prend en charge plus de 30 formats vectoriels, dont DWG, DXF, DWF et SVG, permettant une API unique pour de nombreux scénarios de conversion.

**Q : Existe‑t‑il un essai gratuit d’Aspose.CAD pour Java ?**  
R : Oui, vous pouvez accéder à un essai gratuit [ici](https://releases.aspose.com/).

**Q : Où puis‑je trouver la documentation d’Aspose.CAD pour Java ?**  
R : Consultez la documentation officielle [ici](https://reference.aspose.com/cad/java/).

**Q : Comment obtenir du support pour Aspose.CAD pour Java ?**  
R : Visitez le forum de support [ici](https://forum.aspose.com/c/cad/19).

**Q : Où puis‑je acheter une licence pour Aspose.CAD pour Java ?**  
R : Vous pouvez acheter une licence [ici](https://purchase.aspose.com/buy).

---

**Dernière mise à jour :** 2026-05-25  
**Testé avec :** Aspose.CAD 24.11 pour Java  
**Auteur :** Aspose

## Tutoriels associés

- [Exportation sans effort de DGN vers PDF AutoCAD avec Aspose.CAD pour Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [Exporter DGN vers DWG avec Aspose.CAD pour Java – Tutoriel](/cad/java/dgn-export-options/)
- [Enregistrer CAD en PNG – Convertir un dessin CAD en format d'image raster avec Aspose.CAD pour Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}