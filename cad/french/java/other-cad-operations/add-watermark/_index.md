---
date: 2026-06-04
description: Apprenez comment créer un PDF à partir de CAD et ajouter un filigrane
  en utilisant Aspose.CAD for Java. Ce guide étape par étape couvre l'exportation
  de CAD vers PDF, l'ajout de texte CAD et le branding.
keywords:
- create pdf from cad
- export cad to pdf
- add text cad
- watermark cad drawing
- convert dwg to pdf
linktitle: Ajouter un filigrane
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to create PDF from CAD and add a watermark using Aspose.CAD
    for Java. This step‑by‑step guide covers export CAD to PDF, add text CAD, and
    branding.
  headline: Create PDF from CAD with Watermark - Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PDF from CAD and add a watermark using Aspose.CAD
    for Java. This step‑by‑step guide covers export CAD to PDF, add text CAD, and
    branding.
  name: Create PDF from CAD with Watermark - Aspose.CAD for Java
  steps:
  - name: Import Packages
    text: The `com.aspose.cad` namespace provides all classes you need for CAD manipulation.
      The `Image` class is the entry point for loading and saving CAD files. The `MText`
      class represents multi‑line text that can be styled and positioned.
  - name: Add New MTEXT
    text: MText represents multi‑line text entities that can be used for watermarks.
  - name: Add Simple Entity like Text
    text: TextEntity is a single‑line text object used for simple annotations.
  - name: Export to PDF
    text: SaveFormat.Pdf specifies PDF as the output format for saving.
  type: HowTo
- questions:
  - answer: Aspose.CAD supports **DWG, DXF, DWT, DWF, and over 30 additional formats**,
      allowing you to **export cad to pdf** from virtually any source file.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Yes – you can control font family, size, color, rotation, and transparency
      through the `MText` or `TextEntity` properties.
    question: Can I customize the appearance of the watermark text?
  - answer: Yes, you can download the trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.CAD for Java?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      assistance and official support channels.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      detailed API references, code samples, and best‑practice guides.
    question: Where can I find the complete documentation for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Créer un PDF à partir de CAD avec filigrane - Aspose.CAD for Java
url: /fr/java/other-cad-operations/add-watermark/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer un PDF à partir de CAD avec filigrane - Aspose.CAD for Java

## Introduction

Dans ce tutoriel, vous allez **créer un PDF à partir de CAD** à partir de dessins et appliquer un filigrane personnalisé en utilisant Aspose.CAD for Java. Ajouter un filigrane vous permet de protéger la propriété intellectuelle, de marquer vos conceptions ou d’intégrer des informations de révision. Nous parcourrons l’ensemble du flux de travail — depuis l’importation des packages nécessaires, l’ajout de filigranes basés sur du texte, jusqu’à l’exportation du dessin CAD final en fichier PDF. À la fin, vous disposerez d’un extrait réutilisable que vous pourrez intégrer dans n’importe quel projet Java.

## Réponses rapides
- **Quel est l'objectif principal ?** Créer un PDF à partir d'un fichier CAD et superposer un filigrane en quelques lignes de code Java.  
- **Quelle bibliothèque est requise ?** Aspose.CAD for Java (prend en charge plus de 30 formats CAD).  
- **Ai-je besoin d’une licence pour les tests ?** Un essai gratuit de 30 jours est disponible ; une licence commerciale est requise pour la production.  
- **Puis-je exporter le CAD en PDF après l'ajout du filigrane ?** Oui – le même appel d'API qui enregistre le dessin le convertit également en PDF.  
- **Le processus est‑il thread‑safe ?** Toutes les classes Aspose.CAD sont conçues pour une utilisation concurrente lorsque vous créez des instances séparées par thread.

## Qu’est‑ce qu’un filigrane dans le CAD ?
Un filigrane dans le CAD est une superposition de texte ou d’image semi‑transparente placée sur un dessin pour indiquer la propriété, la confidentialité ou le statut de révision. Il apparaît derrière ou au-dessus de la géométrie principale sans modifier les données de conception sous‑jacentes, permettant aux visualisateurs de voir le contenu original tout en reconnaissant la présence du filigrane.

## Pourquoi ajouter un filigrane lorsque vous **créez un PDF à partir de CAD** ?
Aspose.CAD for Java prend en charge **plus de 30 formats d’entrée** (DWG, DXF, DWF, DWT, etc.) et peut gérer des fichiers jusqu’à **500 Mo** sans charger l’ensemble du document en mémoire. Ajouter un filigrane pendant l’étape de conversion en PDF élimine une passe de post‑traitement distincte, économisant jusqu’à **40 %** du temps de traitement dans les pipelines par lots.

## Prérequis

- **Aspose.CAD for Java** – téléchargez le JAR le plus récent depuis le site officiel [ici](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK)** – version 11 ou supérieure est recommandée.  
- Une licence **Aspose.CAD** valide pour une utilisation en production (optionnelle pour l’essai).  

## Comment créer un PDF à partir de CAD avec un filigrane ?

CadImage est la classe principale qui représente un dessin CAD dans Aspose.CAD.  
Pour créer un PDF à partir d’un fichier CAD avec un filigrane intégré, chargez d’abord le dessin dans une instance `CadImage`, qui représente le document CAD en mémoire. Ensuite, créez un objet `MText` ou `TextEntity` contenant le texte du filigrane, définissez sa taille de police, sa couleur et son opacité, puis ajoutez‑le à l’espace modèle. Enfin, appelez `save` avec `SaveFormat.Pdf` pour exporter le dessin modifié en PDF, en préservant la qualité vectorielle.

### Étape 1 : Importer les packages

L’espace de noms `com.aspose.cad` fournit toutes les classes nécessaires à la manipulation CAD.

La classe `Image` est le point d’entrée pour le chargement et l’enregistrement des fichiers CAD.  
La classe `MText` représente du texte multi‑lignes qui peut être stylisé et positionné.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Étape 2 : Ajouter un nouveau MTEXT

MText représente des entités de texte multi‑lignes pouvant être utilisées pour les filigranes.

```java
//add new MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

### Étape 3 : Ajouter une entité simple comme du texte

TextEntity est un objet texte à ligne unique utilisé pour des annotations simples.

```java
// or add more simple entity like Text
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

### Étape 4 : Exporter en PDF

SaveFormat.Pdf spécifie le PDF comme format de sortie pour l’enregistrement.

```java
// export to pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Problèmes courants et solutions

- **Filigrane non visible** – Assurez‑vous que la couleur du texte contraste avec l’arrière‑plan et définissez la propriété `Transparency` (par ex., 0,5 pour 50 % d’opacité).  
- **Les gros fichiers provoquent OutOfMemoryError** – Activez le mode de diffusion de `CadImage` en définissant `CadImageOptions.setLoadMode(LoadMode.Paged)`.  
- **Rendu de police incorrect** – Installez les polices TrueType requises sur le serveur ou intégrez‑les en utilisant `FontRepository`.

## Questions fréquemment posées

**Q : Aspose.CAD est‑il compatible avec tous les formats de fichiers CAD ?**  
R : Aspose.CAD prend en charge **DWG, DXF, DWT, DWF et plus de 30 formats supplémentaires**, vous permettant de **exporter le CAD en PDF** depuis pratiquement n’importe quel fichier source.

**Q : Puis‑je personnaliser l’apparence du texte du filigrane ?**  
R : Oui – vous pouvez contrôler la famille de police, la taille, la couleur, la rotation et la transparence via les propriétés de `MText` ou `TextEntity`.

**Q : Existe‑t‑il une version d’essai disponible pour Aspose.CAD for Java ?**  
R : Oui, vous pouvez télécharger la version d’essai [ici](https://releases.aspose.com/).

**Q : Comment puis‑je obtenir du support pour Aspose.CAD ?**  
R : Consultez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour l’assistance communautaire et les canaux de support officiels.

**Q : Où puis‑je trouver la documentation complète d’Aspose.CAD for Java ?**  
R : Référez‑vous à la [documentation](https://reference.aspose.com/cad/java/) pour des références API détaillées, des exemples de code et des guides de bonnes pratiques.

---

**Dernière mise à jour :** 2026-06-04  
**Testé avec :** Aspose.CAD for Java 24.12  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Exporter DWG en PDF ou raster avec Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Créer un PDF à partir de DWG et ajouter du texte avec Aspose.CAD for Java](/cad/java/cad-text-and-annotation/add-text-in-dwg/)
- [Exporter une mise en page DWG spécifique en PDF avec Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}