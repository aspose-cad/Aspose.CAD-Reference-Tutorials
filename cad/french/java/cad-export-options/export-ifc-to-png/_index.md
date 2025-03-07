---
title: Exporter IFC vers PNG avec Aspose.CAD pour Java
linktitle: Exporter IFC vers PNG
second_title: API Java Aspose.CAD
description: Convertissez facilement IFC en PNG avec Aspose.CAD pour Java. Suivez notre tutoriel étape par étape.
weight: 18
url: /fr/java/cad-export-options/export-ifc-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter IFC vers PNG avec Aspose.CAD pour Java

## Introduction

Bienvenue dans ce didacticiel étape par étape sur l'exportation d'IFC (Industry Foundation Classes) vers PNG à l'aide d'Aspose.CAD pour Java. Aspose.CAD est une puissante bibliothèque Java qui offre des fonctionnalités étendues pour travailler avec des fichiers CAO, y compris le format IFC. Dans ce didacticiel, nous vous guiderons tout au long du processus de conversion d'un fichier IFC en image PNG avec des explications détaillées à chaque étape.

## Conditions préalables

Avant de commencer, assurez-vous que les conditions préalables suivantes sont remplies :

-  Bibliothèque Aspose.CAD : téléchargez et installez la bibliothèque Aspose.CAD pour Java à partir du[lien de téléchargement](https://releases.aspose.com/cad/java/).

- Répertoire de documents : préparez un répertoire sur votre système où se trouve votre fichier IFC.

## Importer des espaces de noms

Dans votre projet Java, importez les espaces de noms nécessaires comme indiqué ci-dessous :

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Étape 1 : Chargez le fichier IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Cette étape consiste à charger le fichier IFC à l'aide d'Aspose.CAD.

## Étape 2 : Définir les options vectorielles

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Configurez les options vectorielles pour la rastérisation, en spécifiant la largeur et la hauteur de la page.

## Étape 3 : Définir les options PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Définissez les options PNG, y compris les options de rastérisation vectorielle.

## Étape 4 : Enregistrer au format PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

Enregistrez l'image traitée au format PNG.

## Conclusion

Toutes nos félicitations! Vous avez converti avec succès un fichier IFC en PNG à l'aide d'Aspose.CAD pour Java. Ce didacticiel a fourni un guide complet, garantissant que vous pouvez intégrer de manière transparente cette fonctionnalité dans vos projets.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec toutes les versions des fichiers IFC ?

 A1 : Aspose.CAD prend en charge différentes versions de fichiers IFC. Se référer au[Documentation](https://reference.aspose.com/cad/java/) pour les détails de compatibilité.

### Q2 : Puis-je personnaliser davantage les options de rastérisation ?

 A2 : Absolument ! Explore le[Documentation](https://reference.aspose.com/cad/java/) pour des options de personnalisation avancées.

### Q3 : Existe-t-il une version d'essai disponible ?

A3 : Oui, vous pouvez accéder à la version d'essai gratuite[ici](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir une licence temporaire pour Aspose.CAD ?

 A4 : Obtenir une licence temporaire auprès de[ce lien](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis-je demander de l'aide ou discuter de problèmes ?

A5 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien de la communauté.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
