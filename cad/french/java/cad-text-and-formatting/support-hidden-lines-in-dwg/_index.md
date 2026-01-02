---
date: 2026-01-02
description: Apprenez à exporter DWG en PDF, activer les lignes cachées et convertir
  DWG en PDF avec Aspose.CAD pour Java dans ce tutoriel étape par étape.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: Exporter DWG en PDF avec lignes cachées – Aspose.CAD pour Java
url: /fr/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter DWG en PDF avec lignes cachées – Aspose.CAD for Java

## Introduction

Dans ce tutoriel, vous apprendrez comment **exporter DWG en PDF** tout en préservant les lignes cachées à l’aide d’Aspose.CAD for Java. Que vous ayez besoin de **convertir DWG en PDF**, de créer un guide de type **dwg to pdf tutorial**, ou simplement de **sauvegarder DWG en PDF** avec prise en charge des lignes cachées, nous vous accompagnerons étape par étape. À la fin, vous disposerez d’une solution prête à l’emploi que vous pourrez intégrer à n’importe quel projet Java.

## Quick Answers
- **What does this tutorial cover?** Activation du rendu des lignes cachées lors de l’exportation de DWG en PDF avec Aspose.CAD for Java.  
- **Which primary operation is performed?** `export dwg as pdf`.  
- **Do I need a license?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.  
- **What are the prerequisites?** Environnement de développement Java, bibliothèque Aspose.CAD for Java et fichiers DWG.  
- **How long does implementation take?** Environ 10‑15 minutes pour une configuration de base.

## What is “export dwg as pdf”?
Exporter un fichier DWG en PDF convertit le dessin CAD vectoriel en format de document portable tout en conservant les calques, les types de lignes et, éventuellement, le rendu des lignes cachées. Cela facilite le partage des conceptions CAD avec des parties prenantes qui ne disposent pas de logiciel CAD.

## Why enable hidden lines when exporting?
Les lignes cachées offrent une représentation visuelle plus claire des modèles 3D complexes sur une page 2D, en veillant à ce que seules les arêtes visibles soient mises en avant. Cela améliore la lisibilité et est souvent exigé pour la documentation d’ingénierie.

## Prerequisites

1. **Aspose.CAD for Java** – téléchargez la bibliothèque depuis le site officiel [here](https://releases.aspose.com/cad/java/).  
2. **DWG files** – disposez des dessins DWG sources stockés dans un répertoire connu.  
3. **Java development environment** – JDK 8+ et votre IDE préféré (Eclipse, IntelliJ, etc.).  

Maintenant que tout est prêt, passons au code.

## Import Namespaces

Commencez par importer les classes nécessaires afin de travailler avec les images CAD et les options PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Step 1: Set Up Your Project

Créez un projet Java et ajoutez le JAR Aspose.CAD à votre chemin de construction. Puis définissez le répertoire contenant vos fichiers DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Pro tip:** Utilisez un chemin absolu ou configurez un chemin relatif basé sur le dossier des ressources de votre projet.

## Step 2: Load DWG File

Chargez le fichier DWG source dans un objet `CadImage` afin de pouvoir le manipuler.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Step 3: Configure Rasterization Options

Sélectionnez les calques à inclure et définissez la taille de page pour correspondre au dessin original. C’est ici que nous activons le rendu des lignes cachées en spécifiant la mise en page.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Step 4: Set PDF Options

Indiquez à Aspose.CAD de rasteriser les données vectorielles dans un PDF, en utilisant la mise en page « Model » pour garder les lignes cachées invisibles.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 5: Save the Result

Enfin, exportez le DWG en fichier PDF. Les lignes cachées seront respectées selon la mise en page que vous avez définie.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Common Pitfall:** Oublier de définir la mise en page sur `"Model"` entraînera l’affichage de toutes les lignes (y compris les cachées) en traits pleins dans le PDF.

## Conclusion

Vous disposez maintenant d’une méthode complète, prête pour la production, afin de **exporter DWG en PDF** avec prise en charge des lignes cachées en utilisant Aspose.CAD for Java. Cette approche peut être intégrée à des outils de traitement par lots, des services web ou des applications de bureau pour automatiser la conversion CAD‑vers‑PDF.

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other CAD file formats?
A1: Oui, Aspose.CAD prend en charge divers formats CAD tels que DWG, DXF, DWF, et plus encore.

### Q2: Is there a free trial available for Aspose.CAD for Java?
A2: Oui, vous pouvez trouver l’essai gratuit [here](https://releases.aspose.com/).

### Q3: How do I get support for Aspose.CAD for Java?
A3: Visitez le forum Aspose.CAD [here](https://forum.aspose.com/c/cad/19) pour obtenir de l’aide communautaire.

### Q4: Where can I find detailed documentation for Aspose.CAD for Java?
A4: Consultez la documentation [here](https://reference.aspose.com/cad/java/).

### Q5: Can I purchase a temporary license for Aspose.CAD for Java?
A5: Oui, vous pouvez obtenir une licence temporaire [here](https://purchase.aspose.com/temporary-license/).

### Q6: Does this method also work for converting DWG to PDF in a headless server environment?
A6: Absolument. Puisque le code utilise uniquement l’API Aspose.CAD, il s’exécute sans aucune dépendance UI, ce qui le rend idéal pour l’automatisation côté serveur.

---

**Last Updated:** 2026-01-02  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}