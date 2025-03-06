---
title: Guide de conversion DGN en PDF - Aspose.CAD pour Java
linktitle: Prise en charge de DGN V7
second_title: API Java Aspose.CAD
description: Convertissez sans effort des fichiers DGN en PDF à l'aide d'Aspose.CAD pour Java. Suivez notre guide étape par étape pour une intégration transparente et un flux de travail efficace.
weight: 11
url: /fr/java/other-cad-operations/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guide de conversion DGN en PDF - Aspose.CAD pour Java

## Introduction

Dans le monde dynamique de la CAO (Conception Assistée par Ordinateur), la conversion efficace des fichiers DGN (Conception) en PDF (Portable Document Format) est une exigence cruciale. Aspose.CAD pour Java apparaît comme une solution puissante, offrant une intégration transparente et des fonctionnalités robustes. Ce guide étape par étape vise à vous guider tout au long du processus d'exportation de fichiers DGN au format PDF à l'aide d'Aspose.CAD pour Java, garantissant ainsi un flux de travail fluide et efficace.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :
-  Bibliothèque Aspose.CAD pour Java : téléchargez et installez la bibliothèque à partir du[Page de téléchargement d'Aspose.CAD pour Java](https://releases.aspose.com/cad/java/).
- Environnement de développement Java : assurez-vous d'avoir configuré un environnement de développement Java sur votre machine.

## Importer des packages

Commencez par importer les packages nécessaires dans votre projet Java :

## Étape 1 : Importer les packages nécessaires

Dans votre projet Java, importez les packages requis pour Aspose.CAD for Java.
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## Étape 2 : Définir les chemins de fichiers

Définissez les chemins de votre fichier DGN d'entrée et du fichier PDF de sortie.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## Étape 3 : Charger l'image DGN

Chargez l'image DGN à l'aide de la bibliothèque Aspose.CAD.

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## Étape 4 : Configurer les options d'exportation PDF

Configurez les options d'exportation au format PDF, notamment les dimensions de la page, la mise à l'échelle automatique de la mise en page, la couleur d'arrière-plan et les mises en page spécifiques à exporter.

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //exporter uniquement 4 vues (1,2,3 et 9)
options.setVectorRasterizationOptions(vectorOptions);
```

## Étape 5 : Enregistrer le fichier PDF

Enregistrez l'image DGN en tant que fichier PDF avec les options spécifiées.

```java
objImage.save(outFile, options);
```

Répétez ces étapes pour différents fichiers DGN, en ajustant les chemins d'accès et les options des fichiers selon vos besoins.

## Conclusion

Avec Aspose.CAD pour Java, la conversion de fichiers DGN en PDF devient un processus simple. Ce guide vous donne les connaissances nécessaires pour intégrer de manière transparente la bibliothèque dans vos projets Java, facilitant ainsi des conversions efficaces de fichiers CAO.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour Java avec d’autres formats de fichiers CAO ?

A1 : Oui, Aspose.CAD prend en charge divers formats de CAO, offrant des fonctionnalités polyvalentes au-delà de la conversion DGN en PDF.

### Q2 : Une licence temporaire est-elle disponible pour Aspose.CAD pour Java ?

 A2 : Oui, vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/) à des fins de tests.

### Q3 : Comment puis-je demander de l'aide ou poser des questions sur Aspose.CAD pour Java ?

 A3 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19)pour entrer en contact avec la communauté et demander de l'aide.

### Q4 : Quelles mises en page puis-je exporter lors de la conversion DGN en PDF ?

 A4 : Vous pouvez spécifier les mises en page à exporter en personnalisant le`setLayouts` tableau dans le code.

### Q5 : Où puis-je trouver une documentation complète pour Aspose.CAD pour Java ?

 A5 : Reportez-vous au[Documentation Aspose.CAD pour Java](https://reference.aspose.com/cad/java/) pour des informations détaillées.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
