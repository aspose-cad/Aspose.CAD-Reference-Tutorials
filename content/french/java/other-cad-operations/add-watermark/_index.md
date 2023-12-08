---
title: Ajouter des filigranes aux dessins CAO - Tutoriel Aspose.CAD for Java
linktitle: Ajouter un filigrane
second_title: API Java Aspose.CAD
description: Améliorez vos dessins CAO avec des filigranes personnalisés à l'aide d'Aspose.CAD pour Java. Suivez notre guide étape par étape pour une intégration transparente.
type: docs
weight: 12
url: /fr/java/other-cad-operations/add-watermark/
---
## Introduction

Bienvenue dans ce guide complet sur l'ajout de filigranes aux dessins CAO à l'aide d'Aspose.CAD pour Java. Dans ce didacticiel, vous apprendrez à intégrer efficacement des filigranes, en améliorant vos documents CAO avec des messages personnalisés ou une image de marque. Aspose.CAD pour Java fournit un ensemble puissant de fonctionnalités, simplifiant le processus d'ajout de filigrane.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous de disposer des prérequis suivants :

-  Aspose.CAD pour Java : assurez-vous que la bibliothèque Aspose.CAD est installée dans votre environnement Java. Vous pouvez le télécharger[ici](https://releases.aspose.com/cad/java/).
- Kit de développement Java (JDK) : assurez-vous que la dernière version de JDK est installée sur votre système.

## Importer des packages

Dans votre projet Java, importez les packages Aspose.CAD nécessaires pour commencer :

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Étape 1 : Ajouter un nouveau MTEXT

```java
//ajouter un nouveau MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Étape 2 : Ajouter une entité simple comme du texte

Vous pouvez également ajouter une entité plus simple comme du texte :

```java
// ou ajoutez une entité plus simple comme Text
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Étape 3 : Exporter au format PDF

Exportez le dessin CAO avec le filigrane ajouté vers un fichier PDF :

```java
// exporter en pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Conclusion

Toutes nos félicitations! Vous avez ajouté avec succès des filigranes à vos dessins CAO à l'aide d'Aspose.CAD pour Java. Ce processus simple mais puissant vous permet de personnaliser vos créations ou de les protéger avec une image de marque.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec tous les formats de fichiers CAO ?

A1 : Aspose.CAD prend en charge divers formats de CAO, notamment DWG, DXF, DWT et DWF.

### Q2 : Puis-je personnaliser l’apparence du texte du filigrane ?

A2 : Oui, vous avez un contrôle total sur l’apparence du filigrane, y compris la taille, la couleur et la position du texte.

### Q3 : Existe-t-il une version d'essai disponible pour Aspose.CAD pour Java ?

 A3 : Oui, vous pouvez télécharger la version d'essai[ici](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir de l'aide pour Aspose.CAD ?

 A4 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien de la communauté.

### Q5 : Où puis-je trouver la documentation complète d'Aspose.CAD pour Java ?

 A5 : Reportez-vous au[Documentation](https://reference.aspose.com/cad/java/) pour des informations détaillées.