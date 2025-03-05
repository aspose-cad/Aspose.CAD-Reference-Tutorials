---
title: Exportation DGN vers PDF AutoCAD sans effort avec Aspose.CAD pour Java
linktitle: Exportation de DGN au format AutoCAD vers PDF
second_title: API Java Aspose.CAD
description: Explorez le guide étape par étape sur l'exportation de fichiers DGN au format AutoCAD au format PDF à l'aide d'Aspose.CAD pour Java. Élevez les capacités de gestion CAO de votre application Java sans effort.
type: docs
weight: 12
url: /fr/java/dgn-export-options/exporting-dgn-to-pdf/
---
## Introduction

Bienvenue dans ce didacticiel complet sur l'utilisation d'Aspose.CAD pour Java pour exporter des fichiers DGN au format AutoCAD au format PDF. Si vous cherchez à améliorer la capacité de votre application Java à gérer les fichiers CAO, Aspose.CAD est un excellent choix. Dans ce didacticiel, nous vous guiderons étape par étape tout au long du processus d'exportation de fichiers DGN.


## Conditions préalables
Avant de plonger dans le didacticiel, assurez-vous de disposer des prérequis suivants :
-  Bibliothèque Aspose.CAD : assurez-vous que la bibliothèque Aspose.CAD pour Java est installée. Vous pouvez le télécharger[ici](https://releases.aspose.com/cad/java/).
- Répertoire de documents : configurez un répertoire de documents dans lequel vos fichiers d'entrée et de sortie seront stockés.

## Importer des packages

Dans votre projet Java, importez les packages nécessaires pour accéder aux fonctionnalités d'Aspose.CAD :

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Maintenant, décomposons l'exemple de code en plusieurs étapes :

## Étape 1 : Définir les chemins de fichiers

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Assurez-vous de remplacer « Votre répertoire de documents » par le chemin réel où se trouvent vos fichiers.

## Étape 2 : Charger l'image DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Chargez le fichier DGN à l'aide d'Aspose.CAD.

## Étape 3 : Définir les options d'exportation PDF

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Exporter des vues spécifiques
options.setVectorRasterizationOptions(vectorOptions);
```

Définissez les options d'exportation PDF, y compris les dimensions de la page et les préférences de mise en page.

## Étape 4 : Enregistrer le fichier PDF

```java
objImage.save(outFile, options);
```

Enregistrez le fichier PDF exporté.

Répétez ces étapes pour tous les fichiers DGN supplémentaires que vous souhaitez convertir. Toutes nos félicitations! Vous avez exporté avec succès des fichiers DGN au format AutoCAD au format PDF à l'aide d'Aspose.CAD pour Java.

## Conclusion

Dans ce didacticiel, nous avons exploré comment exploiter Aspose.CAD pour Java pour améliorer les capacités de gestion des fichiers CAO de votre application. Grâce à des étapes faciles à suivre et des exemples de code, vous pouvez désormais exporter en toute transparence des fichiers DGN au format AutoCAD au format PDF.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec tous les formats de fichiers CAO ?

A1 : Oui, Aspose.CAD prend en charge une large gamme de formats de CAO, garantissant une polyvalence dans la gestion de différents types de fichiers.

### Q2 : Puis-je personnaliser les paramètres d'exportation PDF ?

A2 : Absolument. Comme le montre le didacticiel, vous pouvez ajuster des options telles que les dimensions et la mise en page des pages en fonction de vos besoins.

### Q3 : Où puis-je trouver une assistance ou une assistance supplémentaire ?

 A3 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien et les discussions de la communauté.

### Q4 : Existe-t-il un essai gratuit ?

 A4 : Oui, vous pouvez accéder à l'essai gratuit[ici](https://releases.aspose.com/).

### Q5 : Comment puis-je obtenir une licence temporaire ?

 A5 : Obtenez un permis temporaire[ici](https://purchase.aspose.com/temporary-license/).