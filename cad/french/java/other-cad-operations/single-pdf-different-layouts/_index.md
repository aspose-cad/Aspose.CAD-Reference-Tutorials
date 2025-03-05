---
title: Création de PDF dynamiques avec Aspose.CAD pour Java
linktitle: PDF unique avec différentes mises en page
second_title: API Java Aspose.CAD
description: Créez de superbes PDF avec diverses mises en page à partir de dessins CAO à l'aide d'Aspose.CAD pour Java. Intégration facile et fonctionnalités puissantes pour les développeurs Java.
type: docs
weight: 16
url: /fr/java/other-cad-operations/single-pdf-different-layouts/
---
## Introduction

Bienvenue dans le monde d'Aspose.CAD pour Java, une bibliothèque puissante qui permet aux développeurs de manipuler des dessins CAO sans effort. Dans ce didacticiel, nous allons plonger dans la création de PDF uniques avec différentes mises en page à l'aide d'Aspose.CAD pour Java. Que vous soyez un développeur chevronné ou débutant, ce guide étape par étape vous guidera tout au long du processus.

## Conditions préalables

Avant de nous lancer dans cette aventure, assurez-vous d’avoir les conditions préalables suivantes en place :
- Environnement Java : assurez-vous que Java est installé sur votre ordinateur.
-  Bibliothèque Aspose.CAD : téléchargez et installez la bibliothèque Aspose.CAD pour Java à partir du[lien de téléchargement](https://releases.aspose.com/cad/java/).
- Répertoire de documents : configurez un répertoire pour vos dessins DWG.

## Importer des packages

Dans votre projet Java, importez les packages nécessaires :

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Étape 1 : Charger le dessin CAO

 Commencez par charger votre dessin CAO dans un`CadImage` objet:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Étape 2 : configurer les options de rastérisation

Configurez les options de rastérisation pour l'image CAO :

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Étape 3 : Personnaliser les tailles de page de mise en page

Définissez des tailles personnalisées pour plusieurs présentations dans le dessin CAO :

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Étape 4 : Définir les options PDF

Configurez les options PDF, en intégrant les paramètres de rastérisation :

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Étape 5 : Enregistrer au format PDF

Enregistrez l'image CAO traitée au format PDF :

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Toutes nos félicitations! Vous avez réussi à créer un seul PDF avec différentes mises en page à l'aide d'Aspose.CAD pour Java.

## Conclusion

Dans ce didacticiel, nous avons exploré l'intégration transparente d'Aspose.CAD pour Java pour générer des PDF avec diverses mises en page à partir de dessins CAO. La flexibilité et les fonctionnalités robustes de la bibliothèque en font un choix incontournable pour les tâches de manipulation de CAO.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour Java avec d’autres bibliothèques Java ?

R1 : Oui, Aspose.CAD pour Java est conçu pour s'intégrer de manière transparente à d'autres bibliothèques Java, offrant ainsi des fonctionnalités étendues.

### Q2 : Existe-t-il une version d'essai disponible ?

 A2 : Absolument ! Vous pouvez accéder à une version d'essai gratuite[ici](https://releases.aspose.com/).

### Q3 : Où puis-je trouver une assistance supplémentaire ?

 A3 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien et les discussions de la communauté.

### Q4 : Comment puis-je obtenir une licence temporaire ?

 A4 : Vous pouvez obtenir un permis temporaire[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis-je acheter la version complète ?

A5 : Achetez la version complète d'Aspose.CAD pour Java[ici](https://purchase.aspose.com/buy).