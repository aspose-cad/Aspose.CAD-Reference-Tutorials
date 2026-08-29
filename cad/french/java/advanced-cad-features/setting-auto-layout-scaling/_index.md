---
date: 2026-08-29
description: Apprenez comment définir une taille de page PDF personnalisée et créer
  un PDF à partir de CAD en utilisant Aspose.CAD pour Java. Ce guide étape par étape
  couvre l'exportation de CAD vers PDF avec Auto Layout Scaling.
keywords:
- custom pdf page size
- create pdf from cad
- dwg to pdf java
- custom page size pdf
- java convert cad pdf
lastmod: 2026-08-29
linktitle: Configuration d'Auto Layout Scaling
og_description: Définissez une taille de page PDF personnalisée lors de la conversion
  de fichiers CAD en PDF avec Aspose.CAD pour Java. Suivez le guide étape par étape
  pour utiliser Auto Layout Scaling et obtenir des résultats de mise en page parfaits.
og_image_alt: 'Tutorial: set custom pdf page size for CAD to PDF conversion using
  Aspose.CAD Java'
og_title: Définir une taille de page PDF personnalisée pour l'exportation PDF CAD
  – Aspose.CAD Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  headline: How to set custom pdf page size for CAD PDF export
  type: TechArticle
- description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  name: How to set custom pdf page size for CAD PDF export
  steps:
  - name: load the CAD file
    text: Loading the source file is the first step in **how to export CAD** to a
      PDF document.
  - name: create rasterization options
    text: The `CadRasterizationOptions` class defines how the CAD drawing is rasterized
      and which page dimensions to use. It also lets you control DPI, background color,
      and other rendering details.
  - name: set auto layout scaling
    text: Enable the automatic scaling feature. This is the core of **how to set scaling**
      for a CAD‑to‑PDF conversion.
  - name: create PDF options
    text: Link the rasterization settings to the PDF export options.
  - name: export to PDF
    text: Finally, save the rendered image as a PDF file. This step completes the
      **convert dxf to pdf** workflow. Repeat the steps above for any additional CAD
      files you need to process, whether they are **DWG**, **DWF**, or other supported
      formats.
  type: HowTo
- questions:
  - answer: Aspose.CAD for Java supports a broad range of formats, including DWG,
      DXF, DWF, and more than 30 additional CAD types.
    question: Is Aspose.CAD for Java compatible with all CAD file formats?
  - answer: Yes, the `CadRasterizationOptions` class provides properties for fine‑tuning
      scaling, DPI, background color, and other rasterization settings.
    question: Can I customize the scaling options further?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      in‑depth information and examples.
    question: Where can I find additional documentation for Aspose.CAD for Java?
  - answer: Yes, you can explore a [free trial](https://releases.aspose.com/) to experience
      the capabilities of Aspose.CAD for Java.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect
      with the community and seek support.
    question: How can I seek assistance or engage in discussions about Aspose.CAD
      for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
title: Comment définir une taille de page PDF personnalisée pour l'exportation PDF
  CAD
url: /fr/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir une taille de page PDF personnalisée – créer un PDF à partir de CAD avec mise à l'échelle automatique de la mise en page

## Introduction

Si vous devez **définir une taille de page PDF personnalisée** tout en **créant un PDF à partir de CAD** rapidement et avec un redimensionnement parfait, Aspose.CAD for Java répond à vos besoins. Auto Layout Scaling redimensionne automatiquement les mises en page CAD pour remplir les dimensions de la page cible, garantissant que le PDF résultant correspond à la taille de feuille prévue quel que soit le dessin source. Dans ce tutoriel, nous parcourrons le processus complet — du chargement d'un fichier DXF à l'exportation d'un PDF — tout en mettant en avant les capacités d'**export CAD to PDF** de la bibliothèque et en montrant comment vous pouvez également **convertir DWG en PDF** ou **augmenter la résolution du PDF** si nécessaire.

## Réponses rapides
- **Que fait Auto Layout Scaling ?** Il redimensionne automatiquement les mises en page CAD pour s'adapter aux dimensions de la page cible lors du rastérisation.  
- **Quels formats CAD puis‑je convertir ?** Tout format pris en charge par Aspose.CAD (par ex., DXF, DWG, DWF) peut être converti en PDF.  
- **Ai‑je besoin d'une licence pour la production ?** Oui, une licence commerciale est requise pour une utilisation non‑évaluative.  
- **Combien de temps prend une conversion typique ?** Sur du matériel moderne, un fichier standard se convertit en moins d'une seconde.  
- **Puis‑je changer la taille de la page ?** Absolument – utilisez `CadRasterizationOptions` pour définir des dimensions de page personnalisées.

## Qu’est‑ce que « créer un PDF à partir de CAD » ?

Créer un PDF à partir de CAD signifie prendre un dessin d'ingénierie vectoriel (DXF, DWG, etc.) et le rasteriser dans un document PDF. Le PDF conserve la fidélité visuelle du dessin original tout en étant largement visualisable sur n'importe quelle plateforme, et il peut être ouvert sur des appareils qui ne supportent pas les formats CAD natifs.

## Pourquoi utiliser la mise à l'échelle automatique de la mise en page ?

Auto Layout Scaling garantit que chaque mise en page occupe entièrement la page PDF sans calculs manuels, vous faisant gagner du temps et éliminant les erreurs de mise à l'échelle. Il assure également que les épaisseurs de ligne et les couleurs sont préservées avec précision à travers différentes tailles de sortie. Il fournit un rendu cohérent et de haute qualité pour des dizaines de fichiers CAD et prend en charge le traitement par lots pour les grands projets.

## Prérequis
1. **Bibliothèque Aspose.CAD for Java** – téléchargez la dernière version depuis la [page de téléchargement](https://releases.aspose.com/cad/java/).  
2. **Répertoire de ressources** – créez un dossier sur votre machine pour stocker les fichiers CAD ; remplacez `"Your Document Directory"` dans le code par ce chemin.  
3. **Fichier CAD d'exemple** – pour ce guide nous utiliserons `conic_pyramid.dxf`, qui est inclus dans le jeu de données d'exemple d'Aspose.

## Importer les espaces de noms

Tout d'abord, importez les classes requises. Cela nous donne accès aux fonctionnalités de chargement d'images, de rastérisation et d'exportation PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Comment définir une taille de page personnalisée pour le PDF à partir de CAD

Avant de plonger dans le code étape par étape, clarifions pourquoi les dimensions de page personnalisées sont importantes. Définir une **taille de page PDF personnalisée** vous permet d'aligner les tailles de feuille standard de l'industrie (A4, A1, Letter) ou de définir une toile sur mesure, ce qui est essentiel pour les soumissions réglementaires, les manuels techniques ou les travaux d'impression haute résolution.

### Étape 1 : charger le fichier CAD

Le chargement du fichier source est la première étape de **comment exporter CAD** vers un document PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Étape 2 : créer les options de rastérisation

La classe `CadRasterizationOptions` définit comment le dessin CAD est rasterisé et quelles dimensions de page utiliser. Elle vous permet également de contrôler le DPI, la couleur d'arrière‑plan et d'autres détails de rendu.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Étape 3 : définir la mise à l'échelle automatique de la mise en page

Activez la fonction de mise à l'échelle automatique. C'est le cœur de **comment définir la mise à l'échelle** pour une conversion CAD‑vers‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Étape 4 : créer les options PDF

Liez les paramètres de rastérisation aux options d'exportation PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Étape 5 : exporter en PDF

Enfin, enregistrez l'image rendue en tant que fichier PDF. Cette étape finalise le flux de travail **convert dxf to pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Répétez les étapes ci‑dessus pour tout fichier CAD supplémentaire que vous devez traiter, qu'il s'agisse de **DWG**, **DWF**, ou d'autres formats pris en charge.

## Cas d'utilisation courants

| Scénario | Pourquoi définir une taille de page personnalisée ? |
|----------|-----------------------------|
| **Soumission de dessins de construction** | Aligne le PDF avec les tailles de feuille standard A1/A2 requises par les organismes de réglementation. |
| **Intégration dans les manuels techniques** | Garantit que le dessin s'adapte à la mise en page prédéfinie du manuel sans mise à l'échelle supplémentaire. |
| **Impression haute résolution** | Vous permet d'augmenter le DPI (par ex., `rasterizationOptions.setResolution(300)`) tout en conservant des dimensions de page cohérentes. |

## Problèmes courants & dépannage

| Symptôme | Cause probable | Solution |
|----------|----------------|----------|
| Sortie PDF vide | Options de rastérisation non définies ou chemin de fichier incorrect | Vérifiez le chemin `srcFile` et assurez‑vous que `setPageWidth/Height` ne sont pas à zéro |
| Mise à l'échelle déformée | `setAutomaticLayoutsScaling` laissé à `false` | Activez la mise à l'échelle automatique ou calculez manuellement le facteur de mise à l'échelle |
| Couches manquantes | Le DXF source contient des entités non prises en charge | Consultez les notes de version d'Aspose.CAD pour les types d'entités pris en charge |

Aspose.CAD prend en charge la conversion de **plus de 30 formats CAD** et peut traiter des fichiers jusqu'à **500 Mo** sans charger l'intégralité du document en mémoire, offrant des conversions rapides et économes en mémoire pour les charges de travail d'entreprise.

## Questions fréquemment posées

**Q : Aspose.CAD for Java est‑il compatible avec tous les formats de fichiers CAD ?**  
R : Aspose.CAD for Java prend en charge un large éventail de formats, y compris DWG, DXF, DWF, et plus de 30 types CAD supplémentaires.

**Q : Puis‑je personnaliser davantage les options de mise à l'échelle ?**  
R : Oui, la classe `CadRasterizationOptions` offre des propriétés pour affiner la mise à l'échelle, le DPI, la couleur d'arrière‑plan et d'autres paramètres de rastérisation.

**Q : Où puis‑je trouver une documentation supplémentaire pour Aspose.CAD for Java ?**  
R : Reportez‑vous à la [documentation](https://reference.aspose.com/cad/java/) pour des informations détaillées et des exemples.

**Q : Une version d'essai gratuite est‑elle disponible pour Aspose.CAD for Java ?**  
R : Oui, vous pouvez essayer une [version d'essai gratuite](https://releases.aspose.com/) pour découvrir les capacités d'Aspose.CAD for Java.

**Q : Comment puis‑je obtenir de l'aide ou participer à des discussions sur Aspose.CAD for Java ?**  
R : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour vous connecter à la communauté et demander du support.

### Questions supplémentaires courantes

**Q : Comment convertir un fichier DWG en PDF au lieu de DXF ?**  
R : Le même code fonctionne ; il suffit de changer l'extension du fichier dans `srcFile` en `.dwg`.

**Q : Puis‑je définir un DPI personnalisé pour des PDF haute résolution ?**  
R : Oui, utilisez `rasterizationOptions.setResolution(300);` (ou tout DPI dont vous avez besoin).

**Q : Est‑il possible d'incorporer des polices dans le PDF généré ?**  
R : Aspose.CAD rasterise le dessin, donc les polices sont rendues en vecteurs ; aucune incorporation de police séparée n'est requise.

## Conclusion

En suivant ce guide, vous savez maintenant comment **définir une taille de page PDF personnalisée** et **créer un PDF à partir de CAD** en utilisant Aspose.CAD for Java avec Auto Layout Scaling. Le processus rationalise le flux de travail **export CAD to PDF**, assure une mise à l'échelle cohérente et vous fait gagner un temps de développement précieux. N'hésitez pas à expérimenter différentes tailles de page, résolutions et formats CAD pour répondre aux besoins de votre projet, que vous **convertissiez DWG en PDF**, **augmentiez la résolution du PDF**, ou construisiez un processeur par lots **java CAD to PDF**.

---

**Last updated:** 2026-08-29  
**Tested with:** Aspose.CAD for Java 24.12 (latest)  
**Author:** Aspose

## Tutoriels associés

- [Comment définir la taille de page PDF et activer le suivi du processus de rendu CAD avec Aspose.CAD for Java](/cad/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/)
- [Définir la taille de page PDF – Convertir CAD en PDF (Java)](/cad/java/advanced-cad-features/set-canvas-size-and-mode/)
- [Exporter rapidement DWG en PDF ou raster en utilisant la bibliothèque Java CAD Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}