---
title: Définir la taille et le mode du canevas
linktitle: Définir la taille et le mode du canevas
second_title: API Java Aspose.CAD
description: Découvrez la puissance d'Aspose.CAD pour Java avec notre guide étape par étape sur la définition de la taille et du mode du canevas. Convertissez sans effort les fichiers CAO aux formats PDF et TIFF.
type: docs
weight: 16
url: /fr/java/advanced-cad-features/set-canvas-size-and-mode/
---
## Introduction

Cherchez-vous à exploiter la puissance d’Aspose.CAD pour Java pour améliorer votre processus de conversion CAO ? Ce guide complet vous guidera à travers les étapes de définition de la taille et du mode du canevas à l'aide d'Aspose.CAD pour Java. Que vous soyez un développeur chevronné ou que vous débutiez tout juste, ce didacticiel vous fournira les informations dont vous avez besoin.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.CAD pour Java : assurez-vous que la bibliothèque Aspose.CAD est installée dans votre environnement Java. Vous pouvez le télécharger[ici](https://releases.aspose.com/cad/java/).

- Répertoire de documents : configurez un répertoire de documents pour stocker vos fichiers CAO. Ce répertoire sera référencé dans les étapes du didacticiel.

Commençons maintenant par le guide étape par étape.

## Importer des espaces de noms

Dans cette étape, nous importerons les espaces de noms nécessaires pour démarrer votre projet Aspose.CAD.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Étape 1 : Importer les classes Aspose.CAD

```java
// Le chemin d'accès au répertoire de ressources.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 Dans cet extrait, nous définissons le chemin d'accès au répertoire de ressources et chargeons un fichier DXF à l'aide de Aspose.CAD.`Image` classe.

## Étape 2 : Définir les propriétés CadRasterizationOptions

```java
// Créez une instance de CadRasterizationOptions et définissez ses différentes propriétés
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Ici, nous créons une instance de`CadRasterizationOptions` et configurez les propriétés telles que la largeur de la page, la hauteur de la page et les options de mise à l'échelle.

## Étape 3 : Créer des options PDF et définir des options de rastérisation vectorielle

```java
// Créer une instance de PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Définir la propriété VectorRasterizationOptions
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Maintenant, nous créons un`PdfOptions` instance et définir son`VectorRasterizationOptions` propriété à la propriété précédemment configurée`CadRasterizationOptions`.

## Étape 4 : Exporter au format PDF

```java
// Exporter la CAO au format PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Enfin, nous enregistrons l'image CAO dans un fichier PDF en utilisant les options spécifiées.

## Étape 5 : Créer des TiffOptions et définir des VectorRasterizationOptions

```java
// Créer une instance de TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Définir la propriété VectorRasterizationOptions
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Dans cette étape, nous mettons en place un`TiffOptions` instance et configurer son`VectorRasterizationOptions` propriété.

## Étape 6 : Exporter au format TIFF

```java
// Exporter la CAO au format TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Enfin, nous enregistrons l'image CAO dans un fichier TIFF en utilisant les options spécifiées.

## Conclusion

 Toutes nos félicitations! Vous avez défini avec succès la taille et le mode du canevas à l'aide d'Aspose.CAD pour Java. Ce didacticiel fournit une base solide pour vos projets de conversion CAO. Explorez plus de fonctionnalités et de possibilités dans le[Documentation Aspose.CAD](https://reference.aspose.com/cad/java/).

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour Java avec d’autres frameworks Java ?

A1 : Oui, Aspose.CAD est conçu pour s'intégrer de manière transparente à divers frameworks Java.

### Q2 : Une licence temporaire est-elle disponible pour Aspose.CAD ?

 A2 : Oui, vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).

### Q3 : Où puis-je obtenir l'assistance de la communauté pour Aspose.CAD ?

 A3 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien et les discussions de la communauté.

### Q4 : Puis-je essayer Aspose.CAD gratuitement ?

 A4 : Absolument ! Obtenez un essai gratuit[ici](https://releases.aspose.com/).

### Q5 : Comment puis-je acheter Aspose.CAD pour Java ?

 A5 : Acheter le produit[ici](https://purchase.aspose.com/buy).