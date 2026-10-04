---
date: 2026-10-04
description: Apprenez à convertir rapidement le dwg en png et à exporter le CAD en
  png ou d'autres formats raster avec Aspose.CAD for Java. Obtenez des résultats de
  haute qualité rapidement.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: Convertir la mise en page CAD en format d'image raster
og_description: Convertir DWG en PNG rapidement avec Aspose.CAD for Java. Apprenez
  étape par étape comment exporter le CAD en PNG, JPEG, TIFF, et plus.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Convertir DWG en PNG et autres formats raster avec Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Convertir DWG en PNG et autres formats raster avec Aspose.CAD for Java
url: /fr/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWG en PNG et autres formats raster avec Aspose.CAD pour Java

## Introduction

`Aspose.CAD for Java` est une bibliothèque qui permet la conversion programmatique de fichiers CAD en images raster telles que PNG, JPEG et TIFF. Convertir DWG en PNG (ou d’autres formats d’image raster) est une exigence courante lorsque vous devez partager des dessins CAD avec des collègues qui n’ont pas de visionneuse CAD, intégrer des conceptions dans la documentation ou générer des miniatures pour des galeries web. Dans ce guide, vous apprendrez à convertir dwg en png rapidement et de manière fiable, que vous travailliez avec un fichier de dessin complet ou simplement avec une mise en page spécifique. Vous pouvez également avoir besoin de **convertir le CAD en raster** pour des aperçus web, des outils de reporting ou des applications mobiles.

## Réponses rapides
- **Quelle bibliothèque gère la conversion DWG en PNG ?** Aspose.CAD for Java fournit le moteur de conversion.  
- **Quels formats raster puis‑je exporter ?** PNG, JPEG, TIFF, PDF, BMP et plus de 30 formats supplémentaires.  
- **Ai‑je besoin d’une licence pour les tests ?** Un essai gratuit fonctionne pour le développement ; une licence commerciale est requise pour la production.  
- **Puis‑je choisir une mise en page spécifique ?** Oui – utilisez `setLayouts` pour cibler « Model », « Layout1 », etc.  
- **Une sortie haute résolution est‑elle possible ?** Absolument – ajustez `setPageWidth` et `setPageHeight` (ou `setResolution`) pour contrôler le DPI.

## Qu’est-ce que « convertir dwg en png » ?

Convertir dwg en png signifie transformer un dessin vectoriel DWG en une image PNG basée sur des pixels qui peut être affichée par n’importe quel visualiseur d’image standard. Ce processus rasterise les entités vectorielles, en conservant l’épaisseur des lignes, les couleurs et les calques tout en les traduisant en un bitmap à résolution fixe. Le résultat est idéal pour l’intégrer dans des PDF, des documents Word ou des pages web où la prise en charge des vecteurs est limitée.

## Pourquoi exporter le CAD en PNG (ou d’autres formats raster) ?

Exporter le CAD en PNG vous offre une compatibilité universelle, un chargement rapide et une intégration facile sur toutes les principales plateformes. Les images raster se chargent instantanément comparées à l’ouverture d’un fichier DWG volumineux, et la compression sans perte du PNG garantit la fidélité visuelle. En contrôlant la résolution, la couleur d’arrière‑plan et la mise en page, vous assurez que chaque partie prenante voit la même apparence, que le fichier soit consulté sur un ordinateur de bureau, un appareil mobile ou dans un navigateur.

## Cas d’utilisation courants

| Scénario | Pourquoi la sortie raster aide |
|----------|-------------------------------|
| **Documentation de projet** | L’intégration de PNG dans les PDF ou les documents Word évite d’exiger un logiciel CAD pour les examinateurs. |
| **Portails web** | Les miniatures générées à partir de fichiers DWG se chargent instantanément et améliorent l’expérience utilisateur. |
| **Applications mobiles** | Les images raster s’affichent correctement sur les appareils qui ne disposent pas de visionneuse CAD. |
| **Reporting automatisé** | Convertir par lots plusieurs mises en page en PNG/JPEG pour les inclure dans des graphiques ou des tableaux de bord. |

## Prérequis

1. **Environnement de développement Java** – JDK 8 ou version ultérieure installé et configuré.  
2. **Aspose.CAD for Java** – Téléchargez le JAR le plus récent depuis la [documentation Aspose.CAD for Java](https://reference.aspose.com/cad/java/).  

## Importer les espaces de noms

`com.aspose.cad.Image` est la classe principale qui représente tout fichier CAD en mémoire. `com.aspose.cad.imageoptions.*` fournit des objets d’options pour chaque format raster. Importez les classes dont vous avez besoin pour charger un dessin, configurer la rasterisation et enregistrer la sortie.

> **Astuce :** Si vous prévoyez de **exporter le CAD en PNG** au lieu de TIFF, remplacez `TiffOptions` par `PngOptions` (trouvé dans `com.aspose.cad.imageoptions.PngOptions`).

## Guide étape par étape

### Étape 1 : configurer le répertoire des ressources

Remplacez `"Your Document Directory"` par le chemin absolu où résident vos fichiers CAD. Ce répertoire sera utilisé à la fois pour les fichiers d’entrée et de sortie.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Étape 2 : charger le fichier CAD

`Image.load` analyse le fichier source et crée une représentation en mémoire que vous pouvez rasteriser. Vous pouvez charger n’importe quel format pris en charge (DWG, DXF, DGN, etc.) – c’est la partie **comment convertir le CAD**.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Étape 3 : configurer les options de rasterisation

`CadRasterizationOptions` définit comment les données vectorielles sont transformées en pixels. `setPageWidth` et `setPageHeight` contrôlent la résolution de sortie (des valeurs plus grandes = DPI plus élevé). `setLayouts` vous permet de **convertir le CAD en raster** pour des mises en page spécifiques ; omettez‑le pour rasteriser le dessin complet.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Étape 4 : définir les options d’image

`TiffOptions` (ou `PngOptions` pour PNG) indique à Aspose quel format raster générer et vous permet d’ajuster finement la compression, la profondeur de couleur et d’autres paramètres spécifiques au format. Choisissez la classe d’options qui correspond à la sortie souhaitée.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Étape 5 : enregistrer l’image résultante

Appelez `save` sur l’instance `Image`, en passant le nom du fichier de sortie et l’objet d’options. Changez l’extension du fichier en `.png` (et utilisez `PngOptions`) pour **enregistrer le CAD en PNG**. Le même schéma fonctionne pour JPEG, BMP ou PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Erreur fréquente :** Oublier d’associer l’extension du fichier à la classe d’options entraînera une `UnsupportedFormatException`. Gardez‑les toujours synchronisés.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Image de sortie vide** | Vérifiez que les noms de mise en page dans `setLayouts` correspondent exactement à ceux du fichier CAD source. |
| **PNG à basse résolution** | Augmentez `setPageWidth` / `setPageHeight` ou définissez `setResolution` dans les options de rasterisation. |
| **Version DWG non prise en charge** | Assurez‑vous d’utiliser la dernière version d’Aspose.CAD ; les versions plus anciennes peuvent ne pas prendre en charge les nouvelles versions de DWG. |
| **Erreurs de mémoire sur les gros fichiers** | Traitez les pages une à une ou augmentez le tas JVM (`-Xmx2g`). |

## Questions fréquemment posées

**Q : Aspose.CAD est‑il compatible avec différents formats de fichiers CAD ?**  
R : Oui, il prend en charge plus de 30 formats CAD et raster, y compris DWG, DXF, DGN et SVG.

**Q : Puis‑je personnaliser la résolution de l’image raster de sortie ?**  
R : Absolument. Ajustez `setPageWidth`, `setPageHeight` ou `setResolution` dans `CadRasterizationOptions` pour obtenir le DPI souhaité.

**Q : Comment convertir plusieurs mises en page CAD en une seule exécution ?**  
R : Fournissez un tableau contenant tous les noms de mise en page à `setLayouts`, par ex., `new String[]{"Model","Layout1","Layout2"}`.

**Q : Existe‑t‑il des formats de sortie autres que le TIFF pris en charge ?**  
R : Oui — PNG, JPEG, BMP, PDF et d’autres sont disponibles via leurs classes `*Options` respectives.

**Q : Où puis‑je obtenir de l’aide ou partager mon expérience avec Aspose.CAD ?**  
R : Consultez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire et l’assistance officielle.

## Conclusion

En suivant ces étapes, vous pouvez **convertir DWG en PNG**, **exporter le CAD en PNG**, **enregistrer le CAD en JPEG**, ou générer tout autre format raster dont vous avez besoin. Aspose.CAD for Java se charge du travail lourd, vous permettant de vous concentrer sur l’intégration d’images de haute qualité dans vos applications, votre documentation ou vos portails web. La prise en charge par la bibliothèque de plus de 30 formats et sa capacité à rendre des dessins de plusieurs centaines de pages sans charger le fichier complet en mémoire en font un choix robuste pour la rasterisation CAD de niveau entreprise.

---

**Dernière mise à jour :** 2026-10-04  
**Testé avec :** Aspose.CAD for Java 24.12  
**Auteur :** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Tutoriels associés

- [Exporter rapidement DWG en PDF ou raster en utilisant la bibliothèque Java CAD Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Convertir DWG en BMP avec Aspose.CAD for Java](/cad/java/cad-export-options/export-to-bmp/)
- [Exporter DWG en PDF : mise en page spécifique avec Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}