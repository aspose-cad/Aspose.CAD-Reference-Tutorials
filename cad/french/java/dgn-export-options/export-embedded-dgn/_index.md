---
title: Exporter le DGN intégré au format PDF avec Aspose.CAD pour Java
linktitle: Exporter le DGN intégré
second_title: API Java Aspose.CAD
description: Explorez le guide étape par étape sur l'exportation de fichiers DGN intégrés au format PDF à l'aide d'Aspose.CAD pour Java. Améliorez vos applications Java grâce à une manipulation transparente des fichiers CAO.
weight: 11
url: /fr/java/dgn-export-options/export-embedded-dgn/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter le DGN intégré au format PDF avec Aspose.CAD pour Java

## Introduction

Bienvenue dans ce didacticiel complet sur l'exportation de fichiers DGN intégrés à l'aide d'Aspose.CAD pour Java. Aspose.CAD est une bibliothèque puissante qui permet aux développeurs Java de travailler de manière transparente avec des fichiers CAO. Dans ce didacticiel, nous vous guiderons tout au long du processus d'exportation de fichiers DGN intégrés au format PDF à l'aide d'instructions étape par étape. Que vous soyez un développeur chevronné ou débutant, ce didacticiel vous aidera à exploiter les capacités d'Aspose.CAD pour améliorer vos applications Java.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous de disposer des prérequis suivants :
- Environnement de développement Java : assurez-vous qu'un environnement de développement Java est configuré sur votre ordinateur.
-  Aspose.CAD pour Java : téléchargez et installez la bibliothèque Aspose.CAD pour Java à partir de[ici](https://releases.aspose.com/cad/java/).

## Importer des packages

Pour commencer, vous devez importer les packages nécessaires dans votre projet Java. Ajoutez les instructions d'importation suivantes à votre code :

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Maintenant, décomposons l'exemple de code en plusieurs étapes :

## Étape 1 : configurer les chemins d'entrée et de sortie

Définissez le chemin du répertoire dans lequel se trouve votre document et spécifiez le nom du fichier DWG d'entrée.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Étape 2 : Charger le fichier DWG

 Chargez le fichier DWG dans un`Image` objet en utilisant Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Étape 3 : configurer les options de rastérisation

Configurez les options de rastérisation, telles que les mises en page à inclure dans l'exportation.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Étape 4 : Configurer les options PDF

Configurez les options PDF, y compris les options de rastérisation vectorielle.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Étape 5 : Enregistrer le fichier PDF

Enregistrez le fichier PDF avec les options configurées.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Conclusion

Toutes nos félicitations! Vous avez exporté avec succès un fichier DGN incorporé au format PDF à l'aide d'Aspose.CAD pour Java. Ce didacticiel a couvert les étapes essentielles pour intégrer Aspose.CAD dans votre application Java pour une manipulation efficace des fichiers CAO.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour Java dans un projet commercial ?

 A1 : Oui, Aspose.CAD pour Java est une bibliothèque commerciale. Vous pouvez obtenir une licence auprès de[ici](https://purchase.aspose.com/buy).

### Q2 : Un essai gratuit est-il disponible ?

 A2 : Oui, vous pouvez accéder à un essai gratuit d'Aspose.CAD pour Java[ici](https://releases.aspose.com/).

### Q3 : Comment puis-je obtenir de l'assistance pour Aspose.CAD pour Java ?

A3 : Vous pouvez demander l'aide de la communauté Aspose.CAD sur le[forum](https://forum.aspose.com/c/cad/19).

### Q4 : Et si j'ai besoin d'une licence temporaire ?

 A4 : Vous pouvez obtenir un permis temporaire[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis-je trouver la documentation ?

 A5 : La documentation est disponible[ici](https://reference.aspose.com/cad/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
