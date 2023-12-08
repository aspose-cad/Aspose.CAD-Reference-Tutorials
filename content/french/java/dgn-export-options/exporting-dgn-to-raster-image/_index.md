---
title: Conversion Java DGN en JPEG avec le didacticiel Aspose.CAD
linktitle: Exportation de DGN au format AutoCAD vers le format d'image raster
second_title: API Java Aspose.CAD
description: Découvrez comment exporter des fichiers DGN vers des images JPEG en Java à l'aide d'Aspose.CAD. Ce didacticiel étape par étape vous guide tout au long du processus sans effort.
type: docs
weight: 13
url: /fr/java/dgn-export-options/exporting-dgn-to-raster-image/
---
## Introduction

Bienvenue dans ce didacticiel complet sur l'exportation de fichiers DGN (Design) au format d'image raster à l'aide d'Aspose.CAD pour Java. Aspose.CAD est une bibliothèque puissante qui permet aux développeurs Java de travailler de manière transparente avec des fichiers CAO. Dans ce didacticiel, nous vous guiderons tout au long du processus de conversion de fichiers DGN en images JPEG, en vous fournissant des instructions étape par étape et des exemples de code.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :
1.  Bibliothèque Aspose.CAD : assurez-vous que la bibliothèque Aspose.CAD pour Java est installée. Vous pouvez le télécharger[ici](https://releases.aspose.com/cad/java/).
2. Kit de développement Java (JDK) : assurez-vous que Java est installé sur votre ordinateur.
3. Environnement de développement intégré (IDE) : utilisez un IDE compatible Java comme IntelliJ ou Eclipse.

## Importer des packages

Dans votre projet Java, importez les packages nécessaires pour Aspose.CAD. Ajoutez les lignes suivantes à votre code :

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Étape 1 : Charger le fichier DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Étape 2 : Créer un objet JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

## Étape 3 : attribuer des options de rastérisation

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Étape 4 : Enregistrez l'image convertie

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Répétez ces étapes pour vos fichiers DGN spécifiques, en ajustant les chemins d'accès aux fichiers en conséquence.

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment exporter des fichiers DGN au format d'image raster à l'aide d'Aspose.CAD pour Java. Ce didacticiel vous a doté des connaissances nécessaires pour intégrer cette fonctionnalité dans vos applications Java.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour Java avec d’autres formats de fichiers CAO ?

A1 : Oui, Aspose.CAD prend en charge différents formats de CAO, offrant ainsi une solution polyvalente aux développeurs Java.

### Q2 : Existe-t-il un essai gratuit disponible pour Aspose.CAD pour Java ?

 A2 : Oui, vous pouvez accéder à un essai gratuit[ici](https://releases.aspose.com/).

### Q3 : Où puis-je trouver la documentation pour Aspose.CAD pour Java ?

 A3 : Se référer à la documentation[ici](https://reference.aspose.com/cad/java/).

### Q4 : Comment puis-je obtenir de l'assistance pour Aspose.CAD pour Java ?

 A4 : Visitez le forum d'assistance[ici](https://forum.aspose.com/c/cad/19).

### Q5 : Où puis-je acheter une licence pour Aspose.CAD pour Java ?

 A5 : Vous pouvez acheter une licence[ici](https://purchase.aspose.com/buy).