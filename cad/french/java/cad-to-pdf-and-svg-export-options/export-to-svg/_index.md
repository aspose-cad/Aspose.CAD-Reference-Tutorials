---
date: 2026-01-07
description: Apprenez à exporter des fichiers CAD au format SVG avec Aspose.CAD pour
  Java. Ce guide étape par étape vous montre comment convertir des DWG en SVG, définir
  le mode couleur du SVG et intégrer la bibliothèque dans votre projet Java.
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: Exporter le CAD vers SVG à l'aide d'Aspose.CAD pour Java
url: /fr/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export CAD to SVG Using Aspose.CAD for Java

## Introduction

Bienvenue dans l'univers d'Aspose.CAD pour Java, une bibliothèque puissante qui permet aux développeurs de manipuler facilement les dessins CAD. Que vous soyez un développeur chevronné ou un novice dans le domaine du CAD, ce guide complet vous accompagnera pas à pas dans le **export CAD to SVG**, vous montrant comment convertir DWG en SVG, définir le mode couleur SVG et intégrer l'API dans votre projet Java.

## Quick Answers

- **What does “export CAD to SVG” mean?** Il convertit un dessin CAD (par ex., DWG) en un fichier Scalable Vector Graphics qui peut être affiché dans les navigateurs.  
- **Which library handles the conversion?** Aspose.CAD for Java fournit une API simple pour cette tâche.  
- **Do I need a license for development?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Can I control the SVG color output?** Oui, vous pouvez définir le mode couleur SVG (par ex., niveaux de gris).  
- **Is any additional software required?** Seul un runtime Java et le fichier JAR d'Aspose.CAD sont nécessaires.

## Prerequisites

Avant de plonger dans le tutoriel, assurez‑vous de disposer des prérequis suivants :

- Environnement de développement Java : Vérifiez que Java est installé sur votre système.  
- Bibliothèque Aspose.CAD : Téléchargez et installez la bibliothèque Aspose.CAD pour Java depuis le [download link](https://releases.aspose.com/cad/java/).  
- Répertoire de documents : Créez un répertoire pour vos dessins CAD et notez son chemin.

## Import Namespaces

Dans cette étape, nous allons importer les espaces de noms nécessaires pour démarrer notre aventure avec Aspose.CAD. Suivez ces étapes :

### Step 1: Open Your Java Project

Ouvrez votre projet Java dans l'IDE de votre choix.

### Step 2: Add Aspose.CAD Library

Ajoutez la bibliothèque Aspose.CAD à votre projet. Vous pouvez le faire en incluant le fichier JAR dans les dépendances de votre projet.

### Step 3: Import Namespaces

Dans votre classe Java, importez les espaces de noms requis :

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## Export CAD to SVG

Maintenant que le cadre est posé, plongeons dans le processus étape par étape du **export CAD to SVG** avec Aspose.CAD pour Java.

### Step 1: Specify the Resource Directory

Définissez le chemin vers votre répertoire de ressources, où se trouvent vos dessins CAD :

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Step 2: Load the CAD Drawing

Chargez le dessin CAD à l'aide de la bibliothèque Aspose.CAD :

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Step 3: Configure SVG Export Options

Configurez les options d'exportation SVG pour personnaliser la sortie. Ici, nous **set SVG color mode** en niveaux de gris et indiquons à l'exportateur de convertir le texte en formes :

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### Step 4: Save as SVG

Enregistrez le dessin CAD au format SVG :

```java
image.save(dataDir + "meshes.svg");
```

> **Pro tip:** Si vous devez **convert DWG to SVG** tout en conservant les couleurs, remplacez `SvgColorMode.Grayscale` par `SvgColorMode.FullColor`.

Félicitations ! Vous avez exporté avec succès un dessin CAD en SVG en utilisant Aspose.CAD pour Java.

## Why Use Aspose.CAD to Export CAD to SVG?

- **High fidelity:** Les données vectorielles sont conservées, garantissant que le SVG ressemble exactement au dessin CAD original.  
- **No external dependencies:** La conversion s'exécute entièrement dans Java, éliminant le besoin d'outils supplémentaires.  
- **Customizable output:** Des options telles que `setColorType` vous permettent de choisir entre un SVG en niveaux de gris ou en couleur complète.

## Common Issues and Solutions

- **File not found:** Vérifiez que `dataDir` pointe vers le bon dossier et que le nom du fichier DWG correspond.  
- **Blank SVG output:** Assurez‑vous d'avoir défini `options.setTextAsShapes(true)` si le dessin contient du texte devant apparaître sous forme de formes.  
- **Unsupported CAD format:** Aspose.CAD prend en charge DWG, DXF, DWF et plusieurs autres formats ; consultez la documentation pour la liste exacte.

## Conclusion

Dans ce tutoriel, nous avons exploré le processus fluide d’utilisation d’Aspose.CAD pour Java afin de **export CAD to SVG**. Grâce à son API intuitive et à ses fonctionnalités robustes, Aspose.CAD simplifie les tâches complexes, offrant aux développeurs un outil polyvalent pour la manipulation de CAD.

## FAQ's

### Q1: Can I use Aspose.CAD for Java with other CAD formats?

A1 : Oui, Aspose.CAD prend en charge divers formats CAD, notamment DWG, DXF, DWF et plus encore.

### Q2: Is Aspose.CAD suitable for both beginners and experienced developers?

A2 : Absolument ! Aspose.CAD propose une API conviviale, accessible aux débutants, tout en offrant des fonctionnalités avancées pour les développeurs expérimentés.

### Q3: Where can I find additional support or community discussions?

A3 : Visitez le [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) pour obtenir de l'aide et participer aux discussions.

### Q4: Is there a free trial available?

A4 : Oui, vous pouvez explorer Aspose.CAD avec un [free trial](https://releases.aspose.com/).

### Q5: How can I purchase a license for Aspose.CAD for Java?

A5 : Vous pouvez acheter une licence depuis la [purchase page](https://purchase.aspose.com/buy).

## Frequently Asked Questions

**Q: Can I convert a DXF file to SVG using the same code?**  
A: Oui, il suffit de remplacer le nom du fichier par un fichier DXF ; l'API gère les deux formats.

**Q: How do I change the output to full‑color SVG?**  
A: Définissez `options.setColorType(SvgColorMode.FullColor);` avant l'enregistrement.

**Q: Is it possible to embed fonts in the generated SVG?**  
A: Aspose.CAD convertit actuellement le texte en formes ; l'intégration de polices n'est pas requise.

**Q: Does the library work on Linux and macOS?**  
A: La bibliothèque Java est indépendante de la plateforme et fonctionne partout où une JVM compatible est disponible.

**Q: What version of Aspose.CAD was used in this tutorial?**  
A: L'exemple a été testé avec Aspose.CAD for Java 24.10.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

---