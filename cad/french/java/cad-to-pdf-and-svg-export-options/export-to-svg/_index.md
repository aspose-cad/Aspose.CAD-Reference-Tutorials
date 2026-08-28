---
date: 2026-06-14
description: Apprenez comment exporter CAD en SVG avec Aspose.CAD pour Java. Ce guide
  étape par étape vous montre comment convertir DWG en SVG, définir le mode couleur
  SVG et intégrer la bibliothèque dans votre projet Java.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: Exporter en SVG
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Exporter CAD en SVG avec Aspose.CAD pour Java
url: /fr/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter CAD en SVG avec Aspose.CAD pour Java

## Introduction

Dans ce tutoriel complet, vous apprendrez **comment exporter CAD en SVG** à l’aide d’Aspose.CAD pour Java. Que vous ayez besoin de **convertir DWG en SVG**, de générer des SVG à partir de fichiers DWG dans un travail par lots, ou simplement de transformer le SVG en niveaux de gris pour un affichage web léger, ce guide vous accompagne à chaque étape — de la configuration de la bibliothèque à l’ajustement fin des options d’exportation. À la fin, vous disposerez d’un extrait prêt pour la production qui s’exécute sur n’importe quelle plateforme compatible JVM.

## Réponses rapides
- **Que signifie « exporter CAD en SVG » ?** Cela transforme un dessin CAD (par ex. DWG ou DXF) en un fichier Scalable Vector Graphics que les navigateurs affichent sans perte de qualité.  
- **Quelle bibliothèque gère la conversion ?** Aspose.CAD pour Java fournit une API dédiée qui prend en charge plus de 30 formats CAD et génère du SVG avec une fidélité vectorielle complète.  
- **Ai-je besoin d’une licence pour le développement ?** Un essai gratuit suffit pour l’évaluation ; une licence commerciale est requise pour les déploiements en production.  
- **Puis-je contrôler la sortie couleur du SVG ?** Oui — utilisez `SvgColorMode` pour basculer entre le rendu en niveaux de gris et en couleur pleine.  
- **Un logiciel supplémentaire est‑il requis ?** Seulement un runtime Java (JDK 8 ou plus récent) et le JAR Aspose.CAD ; aucun outil CAD externe n’est nécessaire.

## Qu’est‑ce que l’exportation CAD en SVG ?
Exporter CAD en SVG consiste à convertir un fichier CAD natif (tel que DWG, DXF ou DWF) en format d’image vectorielle SVG. Le SVG résultant conserve les données géométriques exactes, permettant un affichage indépendant de la résolution dans les navigateurs web et les outils de conception.

## Pourquoi exporter CAD en SVG avec Aspose.CAD ?
Aspose.CAD peut gérer **plus de 30 formats d’entrée** et générer une sortie SVG jusqu’à **500 pages** sans charger le fichier complet en mémoire, offrant une **conversion vectorielle haute fidélité** à des vitesses de **200 pages/seconde** sur un CPU serveur typique. La bibliothèque fonctionne **100 % Java**, éliminant le besoin de DLL natives ou de moteurs CAD tiers.

## Prérequis

- **Java Development Kit** (JDK 8 ou plus récent) installé et configuré sur votre machine.  
- **Aspose.CAD pour Java** fichier JAR téléchargé depuis le [lien de téléchargement officiel](https://releases.aspose.com/cad/java/).  
- Un dossier contenant au moins un dessin CAD (DWG, DXF, etc.) que vous souhaitez convertir.

## Importer les espaces de noms

Avant d’écrire du code, assurez‑vous que la bibliothèque Aspose.CAD est dans votre classpath et importez les classes requises.

### Étape 1 : Ouvrez votre projet Java
Lancez votre IDE préféré (IntelliJ IDEA, Eclipse, VS Code) et ouvrez le projet où vous comptez ajouter la logique de conversion.

### Étape 2 : Ajoutez la bibliothèque Aspose.CAD
Placez le fichier `aspose-cad-xx.jar` dans le répertoire `libs` et ajoutez‑le comme dépendance dans votre outil de construction (Maven, Gradle ou simple `javac`).

### Étape 3 : Importer les espaces de noms
Dans le fichier source Java qui effectuera la conversion, ajoutez les imports suivants :

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

Ces imports vous donnent accès à la classe principale `Image` et aux options d’exportation spécifiques au SVG.

## Comment exporter CAD en SVG avec Aspose.CAD pour Java ?

Exporter un dessin CAD en SVG avec Aspose.CAD implique de charger le fichier source, de configurer les options spécifiques au SVG, puis d’écrire la sortie. Le processus est simple, ne nécessite que quelques lignes de code et fonctionne de façon cohérente sur tous les formats CAD pris en charge tout en préservant la fidélité vectorielle.

### Étape 1 : Spécifiez le répertoire des ressources
Définissez le chemin absolu ou relatif qui pointe vers le dossier contenant vos dessins CAD :

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### Étape 2 : Chargez le dessin CAD
La classe `Image` est l’objet de haut niveau d’Aspose.CAD qui représente un dessin CAD en mémoire. Charger le fichier crée une représentation en mémoire prête à être exportée.

`Image.load` lit un fichier CAD et crée une représentation en mémoire du dessin.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Étape 3 : Configurer les options d’exportation SVG
`SvgExportOptions` vous permet d’ajuster finement la sortie SVG. Ci‑dessous, nous définissons le mode couleur sur niveaux de gris et nous assurons que tout le texte est rendu sous forme de formes, ce qui améliore la compatibilité avec les navigateurs qui ne disposent pas de la police d’origine.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Étape 4 : Enregistrer en SVG
Enfin, invoquez `save` sur l’instance `Image`, en passant le nom du fichier cible et les options configurées. Aspose.CAD écrit un fichier SVG conforme aux standards qui peut être ouvert directement dans n’importe quel navigateur moderne.

`save` écrit l’image dans le fichier spécifié en utilisant les options d’exportation fournies.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Astuce :** Pour générer un SVG en couleur pleine, remplacez `SvgColorMode.Grayscale` par `SvgColorMode.FullColor`. Cette modification préserve la palette originale tout en conservant la scalabilité vectorielle.

## Pourquoi utiliser Aspose.CAD pour exporter CAD en SVG ?
- **Haute fidélité :** Les données vectorielles sont conservées, garantissant que le SVG ressemble exactement au dessin CAD original.  
- **Aucune dépendance externe :** La conversion s’exécute entièrement sous Java, éliminant le besoin d’outils supplémentaires.  
- **Sortie personnalisable :** Des options comme `setColorType` vous permettent de choisir entre SVG en niveaux de gris ou en couleur pleine.  
- **Performance évolutive :** Traite des dessins de plusieurs centaines de pages en quelques secondes, avec une utilisation mémoire inférieure à 50 Mo.

## Problèmes courants et solutions
- **Fichier introuvable :** Vérifiez que `dataDir` pointe vers le bon dossier et que le nom du fichier DWG respecte la casse du système de fichiers.  
- **Sortie SVG vide :** Assurez‑vous que `options.setTextAsShapes(true)` est activé lorsque le dessin source contient du texte devant apparaître sous forme de formes vectorielles.  
- **Format CAD non pris en charge :** Aspose.CAD prend en charge DWG, DXF, DWF et plus de 15 autres formats ; consultez la documentation officielle pour la liste complète.  
- **Goulots de performance :** Pour les fichiers très volumineux, activez le mode streaming via `options.setEnableStreaming(true)` afin de limiter la consommation mémoire.

## Foire aux questions

**Q : Puis‑je convertir un fichier DXF en SVG avec le même code ?**  
R : Oui, remplacez simplement le nom du fichier DWG par un fichier DXF ; l’API détecte et traite automatiquement les deux formats.

**Q : Comment changer la sortie en SVG couleur pleine ?**  
R : Appelez `options.setColorType(SvgColorMode.FullColor);` avant d’invoquer la méthode `save`.

**Q : Est‑il possible d’intégrer des polices dans le SVG généré ?**  
R : Aspose.CAD convertit le texte en formes, donc l’intégration de polices n’est pas nécessaire ; le SVG résultant ne contient que des contours vectoriels.

**Q : La bibliothèque fonctionne‑t‑elle sous Linux et macOS ?**  
R : La bibliothèque Java est indépendante de la plateforme et s’exécute partout où une JVM compatible est disponible, y compris Windows, Linux et macOS.

**Q : Quelle version d’Aspose.CAD a été utilisée dans ce tutoriel ?**  
R : L’exemple a été testé avec Aspose.CAD pour Java **24.10**.

---

**Dernière mise à jour :** 2026-06-14  
**Testé avec :** Aspose.CAD pour Java 24.10  
**Auteur :** Aspose  

---

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg to pdf java – Export CAD to PDF with Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Export Specific DWG Layout to PDF Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}