---
date: 2026-01-04
description: Apprenez à **enregistrer des fichiers CAD au format PNG** et à exporter
  facilement des objets OLE à partir de fichiers CAD avec Aspose.CAD pour Java. Installation
  rapide, exemple de code complet et conseils de bonnes pratiques.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Enregistrer le CAD au format PNG et exporter les objets OLE avec Aspose.CAD
  pour Java
url: /fr/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer CAD au format PNG et exporter les objets OLE avec Aspose.CAD pour Java

## Introduction

Dans le monde en évolution rapide de la Conception Assistée par Ordinateur (CAD), pouvoir **enregistrer CAD au format PNG** tout en extrayant les objets OLE (Object Linking and Embedding) intégrés peut considérablement rationaliser votre flux de travail. Que vous construisiez un outil de conversion par lots, génériez des miniatures pour un portail web, ou ayez simplement besoin d'archiver le contenu OLE, Aspose.CAD pour Java vous offre une méthode propre et programmatique pour le faire. Dans ce tutoriel, nous parcourrons l'ensemble du processus, de la configuration de votre projet à l'exportation de chaque objet OLE sous forme d'image PNG.

## Quick Answers
- **Puis-je exporter les objets OLE directement en PNG ?** Oui – Aspose.CAD charge le fichier CAD et vous permet de rasteriser chaque mise en page en PNG.  
- **Quelle version de Java est requise ?** Java 8 ou supérieure.  
- **Ai-je besoin d'une licence pour cette fonctionnalité ?** Un essai gratuit suffit pour l'évaluation ; une licence est requise pour la production.  
- **Les données vectorielles seront-elles conservées ?** La rasterisation en PNG conserve la fidélité visuelle, mais la sortie est raster, pas vectorielle.  
- **Le traitement par lots est-il supporté ?** Absolument – parcourez un tableau de fichiers comme indiqué dans l'exemple de code.

## Prerequisites

Avant de commencer, assurez-vous d'avoir les éléments suivants :

- **Java Development Kit (JDK)** – Java 8+ installé et configuré.  
- **Aspose.CAD pour Java** – Téléchargez la dernière bibliothèque depuis le [lien de téléchargement](https://releases.aspose.com/cad/java/).  
- **Fichiers source CAD** – Tous les fichiers DWG/DXF/DGN contenant les objets OLE que vous souhaitez exporter.

## Import Namespaces

Pour travailler avec des fichiers CAD, vous devez importer les classes principales d'Aspose.CAD. Conservez le bloc d'importation exactement tel qu'il est affiché – il fournit les classes utilisées plus tard dans le tutoriel.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## How to Save CAD as PNG

Voici un guide concis, étape par étape, qui montre **comment exporter les objets OLE et enregistrer CAD au format PNG**. Chaque étape comprend une brève explication suivie du code exact à copier dans votre projet.

### Step 1: Set Your Document Directory

Définissez le dossier qui contient vos dessins CAD. Remplacez le texte de substitution par le chemin réel sur votre machine.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Step 2: Define CAD File Names

Listez chaque fichier CAD que vous souhaitez traiter. Vous pouvez ajouter autant d'entrées que nécessaire.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Step 3: Set PNG Export Options

Configurez les paramètres de rasterisation. Ici nous ciblons une mise en page spécifique (`Layout1`) et utilisons les options PNG par défaut.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Step 4: Iterate Through CAD Files and Save as PNG

Chargez chaque fichier CAD, rasterisez les objets OLE et écrivez le fichier PNG de sortie. Le suffixe `_out.png` vous aide à identifier les images générées.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Common Issues and Solutions

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **`Image.load` lance `FileNotFoundException`** | Le chemin `dataDir` est incorrect ou le nom du fichier comporte une faute de frappe. | Vérifiez la chaîne du répertoire et assurez‑vous que les noms de fichiers correspondent exactement, espaces compris. |
| **Le PNG de sortie est vide** | Le nom de la mise en page n'existe pas dans le fichier CAD source. | Utilisez `cadImage.getLayouts()` pour lister les mises en page disponibles, puis mettez à jour `rasterizationOptions.setLayouts(...)`. |
| **Les gros fichiers CAD provoquent OutOfMemoryError** | La rasterisation d'images haute résolution consomme beaucoup de mémoire du tas. | Augmentez le tas JVM (`-Xmx2g`) ou réduisez la résolution de rasterisation via `rasterizationOptions.setResolution(...)`. |

## FAQ's

### Q1 : Aspose.CAD est‑il compatible avec tous les formats de fichiers CAD ?

R1 : Aspose.CAD prend en charge divers formats CAD, dont DWG, DXF et DGN. Consultez la [documentation](https://reference.aspose.com/cad/java/) pour la liste complète.

### Q2 : Puis‑je personnaliser les paramètres d'exportation des objets OLE ?

R2 : Oui, Aspose.CAD offre de nombreuses options pour personnaliser les paramètres d'exportation, vous permettant d'adapter la sortie à vos exigences spécifiques.

### Q3 : Existe‑t‑il un essai gratuit pour Aspose.CAD ?

R3 : Oui, vous pouvez explorer les capacités d'Aspose.CAD en obtenant un essai gratuit [ici](https://releases.aspose.com/).

### Q4 : Où puis‑je obtenir du support communautaire pour Aspose.CAD ?

R4 : Rejoignez la communauté Aspose.CAD sur le [forum](https://forum.aspose.com/c/cad/19) pour demander de l'aide et partager vos expériences.

### Q5 : Comment puis‑je acheter une licence pour Aspose.CAD ?

R5 : Visitez la [page d'achat](https://purchase.aspose.com/buy) pour acquérir une licence adaptée à vos besoins de développement.

## Conclusion

En suivant ces cinq étapes simples, vous pouvez **enregistrer CAD au format PNG** et extraire chaque objet OLE intégré avec seulement quelques lignes de code Java. Cette approche est idéale pour les conversions par lots, les rapports automatisés, ou tout scénario où vous avez besoin d'images raster du contenu CAD sans exportation manuelle. N'hésitez pas à expérimenter avec différentes options de rasterisation pour correspondre à vos exigences de qualité et de performance.

---

**Last Updated:** 2026-01-04  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}