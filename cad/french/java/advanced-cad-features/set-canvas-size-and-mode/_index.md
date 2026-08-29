---
date: 2026-08-29
description: Apprenez à définir la taille de la page PDF et à convertir CAD en PDF
  à l'aide d'Aspose.CAD pour Java, avec mise à l'échelle automatique de la mise en
  page et exportation TIFF.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: Définir la taille de la page PDF – convertir CAD en PDF
og_description: Apprenez à définir la taille de la page PDF lors de la conversion
  de dessins CAD en PDF en Java avec Aspose.CAD. Ce guide couvre les dimensions du
  canevas, la mise à l'échelle automatique de la mise en page et l'exportation vers
  un TIFF haute résolution.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: Définir la taille de la page PDF – convertir CAD en PDF avec Aspose en Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: Définir la taille de la page PDF – convertir CAD en PDF (Java)
url: /fr/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir la taille de la page PDF – convertir CAD en PDF (Java)

## Introduction

Si vous devez **set pdf page size** lors de la conversion de dessins CAD en PDF, vous êtes au bon endroit. Dans ce tutoriel, nous vous montrerons comment utiliser Aspose.CAD for Java pour définir des dimensions de canevas précises, activer le redimensionnement automatique de la mise en page, puis exporter le résultat à la fois en PDF et en TIFF. Que vous prépariez des schémas d’ingénierie pour l’impression ou que vous génériez des miniatures pour une galerie web, contrôler la taille de la page et la résolution de sortie est essentiel.

## Réponses rapides
- **Qu’est‑ce que “convert CAD to PDF” signifie ?** Transformation d’un dessin CAD (par ex., DXF, DWG) en un document PDF pouvant être visualisé sur n’importe quelle plateforme.  
- **Puis‑je également exporter en TIFF ?** Oui—utilisez `TiffOptions` pour créer des images raster haute résolution.  
- **Quelle option contrôle la taille du canevas en Java ?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Qu’est‑ce que le redimensionnement automatique de la mise en page ?** Un drapeau (`setAutomaticLayoutsScaling(true)`) qui préserve les proportions d’origine de la mise en page lorsque la taille du canevas change.  
- **Ai‑je besoin d’une licence pour Aspose.CAD ?** Une licence temporaire ou permanente est requise pour une utilisation en production.

## Comment définir la taille de la page PDF lors de la conversion de CAD en PDF en Java

Chargez votre fichier CAD, configurez `CadRasterizationOptions` avec la largeur et la hauteur souhaitées, activez le redimensionnement automatique de la mise en page, puis enregistrez le résultat au format PDF. Cette approche en deux étapes vous permet de contrôler les dimensions exactes de la page de sortie sans sacrifier la qualité vectorielle.

## Qu’est‑ce que la conversion de CAD en PDF ?

Convertir CAD en PDF signifie prendre des dessins d’ingénierie basés sur des vecteurs et les rendre sous forme de pages PDF, en préservant les traits, les calques et la géométrie tout en rendant le fichier universellement accessible. Le processus rasterise le dessin selon les options spécifiées, produisant un PDF qui peut être ouvert sur n’importe quel appareil sans nécessiter de logiciel CAD, tout en conservant la fidélité visuelle du design original.

## Pourquoi définir la taille du canevas en Java ?

Définir la taille du canevas en Java vous permet de spécifier la résolution de sortie et les dimensions de la page, garantissant que le PDF ou le TIFF résultant correspond à vos exigences d’impression ou d’affichage. Cela vous donne également le contrôle du comportement de mise à l’échelle, essentiel pour les dessins grand format.

## Prérequis

- Aspose.CAD for Java : Assurez‑vous d’avoir la bibliothèque Aspose.CAD installée dans votre environnement Java. Vous pouvez télécharger la bibliothèque Aspose.CAD for Java [ici](https://releases.aspose.com/cad/java/).
- Répertoire de documents : Créez un répertoire de documents pour stocker vos fichiers CAD. Ce répertoire sera référencé dans les étapes du tutoriel.

Maintenant, commençons le guide étape par étape.

## Importer les espaces de noms

Dans cette étape, nous importerons les espaces de noms nécessaires pour lancer votre projet Aspose.CAD.

`Image` est la classe principale utilisée pour charger les fichiers CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Étape 1 : importer les classes Aspose.CAD

La classe `Image` fournit des méthodes pour charger et enregistrer des dessins CAD.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Dans cet extrait, nous configurons le chemin du répertoire des ressources et chargeons un fichier DXF à l’aide de la classe `Image` d’Aspose.CAD.

## Étape 2 : définir les propriétés de CadRasterizationOptions (set canvas size java)

`CadRasterizationOptions` spécifie les paramètres de rasterisation tels que la taille de la page et le redimensionnement pour la conversion CAD‑vers‑raster.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Ici, nous créons une instance de `CadRasterizationOptions` et configurons des propriétés telles que la largeur de la page, la hauteur de la page et **automatic layout scaling**. C’est le cœur de **configure canvas mode** pour votre conversion.

## Étape 3 : créer PdfOptions et définir vectorRasterizationOptions

`PdfOptions` définit les paramètres de sortie PDF pour la conversion.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Maintenant, nous créons une instance de `PdfOptions` et définissons sa propriété `VectorRasterizationOptions` sur le `CadRasterizationOptions` précédemment configuré.

## Étape 4 : exporter en PDF (convert CAD to PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Enfin, nous enregistrons l’image CAD dans un fichier PDF en utilisant les options spécifiées, complétant le processus **convert CAD to PDF**.

## Étape 5 : créer TiffOptions et définir vectorRasterizationOptions (export CAD to TIFF)

`TiffOptions` configure les paramètres de sortie TIFF tels que la compression et la résolution.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Étape 6 : exporter en TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Enfin, nous enregistrons l’image CAD dans un fichier TIFF en utilisant les options spécifiées, démontrant comment **export CAD to TIFF** après avoir configuré la taille du canevas.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| Le PDF de sortie est vide | `setNoScaling(true)` désactive le rendu pour certains dessins | Supprimez `setNoScaling(true)` ou définissez‑le sur `false`. |
| La résolution du TIFF semble basse | Largeur/hauteur de page trop petites | Augmentez les valeurs de `setPageWidth` / `setPageHeight`. |
| La mise en page semble déformée | Redimensionnement automatique de la mise en page désactivé | Assurez‑vous que `setAutomaticLayoutsScaling(true)` est activé. |

## Pourquoi ajuster la taille du canevas et le DPI ?

Modifier la taille du canevas influence directement la résolution de rasterisation de la sortie. Si vous devez **increase TIFF resolution**, il suffit d’augmenter les valeurs de `setPageWidth` / `setPageHeight` ou d’appeler `rasterizationOptions.setResolution(300)` avant de créer le `TiffOptions`. Cela vous fournit des images raster de haute qualité adaptées à l’impression ou à une inspection détaillée.

## Questions fréquemment posées

**Q1 : puis‑je utiliser Aspose.CAD for Java avec d’autres frameworks Java ?**  
A : Oui, Aspose.CAD est conçu pour s’intégrer de façon transparente avec divers frameworks Java.

**Q2 : une licence temporaire est‑elle disponible pour Aspose.CAD ?**  
A : Oui, vous pouvez obtenir une licence temporaire sur la page [ici](https://purchase.aspose.com/temporary-license/).

**Q3 : où puis‑je obtenir du support communautaire pour Aspose.CAD ?**  
A : Visitez le forum Aspose.CAD [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pour le support communautaire et les discussions.

**Q4 : puis‑je essayer Aspose.CAD gratuitement ?**  
A : Absolument ! Obtenez une page de téléchargement d’essai gratuit [ici](https://releases.aspose.com/).

**Q5 : comment acheter Aspose.CAD for Java ?**  
A : Achetez Aspose.CAD for Java [ici](https://purchase.aspose.com/buy).

**Q : la taille du canevas affecte‑t‑elle la qualité vectorielle dans le PDF ?**  
A : Non. La taille du canevas contrôle les dimensions de la page ; les données vectorielles restent indépendantes de la résolution, garantissant un rendu net à n’importe quel niveau de zoom.

**Q : puis‑je définir un DPI différent pour la sortie TIFF ?**  
A : Oui. Ajustez `rasterizationOptions.setResolution(dpiValue)` avant de créer `TiffOptions`.

**Q : comment changer les dimensions d’un PDF existant sans re‑rendre le CAD ?**  
A : Utilisez Aspose.PDF pour charger le PDF généré et appelez `pdf.getPages().setPageSize(PageSize.A4)` ou une taille personnalisée.

**Q : quelle est la meilleure façon de convertir dxf en pdf tout en préservant les calques ?**  
A : Conservez `setAutomaticLayoutsScaling(true)` et évitez `setNoScaling(true)` ; cela conserve la visibilité des calques et la fidélité de la mise en page.

## Conclusion

Félicitations ! Vous avez réussi à **convert CAD to PDF** et **export CAD to TIFF** tout en **set canvas size java**, en activant **automatic layout scaling**, et en apprenant comment **configure canvas mode** pour des sorties de haute qualité. Ce tutoriel fournit une base solide pour vos projets de conversion CAD. Explorez davantage de fonctionnalités et possibilités dans la [Aspose.CAD documentation](https://reference.aspose.com/cad/java/).

**Dernière mise à jour :** 2026-08-29  
**Testé avec :** Aspose.CAD for Java 24.12  
**Auteur :** Aspose

## Tutoriels associés

- [Définir la taille du canevas – fonctionnalités CAD avancées avec Aspose.CAD for Java](/cad/java/advanced-cad-features/)
- [Exporter DWG en PDF en Java – définir la taille de la page PDF avec Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Définir une taille de page personnalisée – PDF à partir de CAD avec redimensionnement automatique de la mise en page](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}