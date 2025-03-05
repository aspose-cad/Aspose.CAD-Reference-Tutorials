---
title: Exporter un fichier DWG au format PDF ou Raster à l'aide d'Aspose.CAD pour Java
linktitle: Exporter un DWG au format PDF ou Raster
second_title: API Java Aspose.CAD
description: Explorez le processus transparent d'exportation de fichiers DWG au format PDF ou d'images raster en Java à l'aide d'Aspose.CAD. Ce guide étape par étape garantit précision et efficacité.
type: docs
weight: 13
url: /fr/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---
## Introduction

Dans le monde dynamique de la conception assistée par ordinateur (CAO), une gestion efficace des dessins est cruciale. Aspose.CAD pour Java fournit une solution puissante pour exporter des fichiers DWG au format PDF ou images raster. Ce didacticiel vous guidera tout au long du processus, vous assurant d'exploiter tout le potentiel d'Aspose.CAD pour Java.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir les éléments suivants :

- Compréhension de base de la programmation Java.
-  Bibliothèque Aspose.CAD pour Java installée. Sinon, téléchargez-le[ici](https://releases.aspose.com/cad/java/).
- Un fichier DWG à des fins de test. Vous pouvez utiliser le fichier "Bottom_plate.dwg" fourni.

## Importer des espaces de noms

Dans votre projet Java, importez les espaces de noms nécessaires pour lancer le processus :

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Étape 1 : Charger le fichier DWG

 Commencez par charger votre fichier DWG à l'aide de Aspose.CAD`Image` classe:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Étape 2 : Déterminer le type d'unité

Vérifiez ensuite le type d'unité du fichier DWG chargé :

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Étape 3 : Définir les options de rastérisation

En fonction du type d'unité, configurez les options de rastérisation :

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Unités métriques
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // unités impériales
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Étape 4 : Configurer les options PDF

Configurez les options d'exportation PDF :

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Étape 5 : Enregistrer au format PDF

Enfin, enregistrez le fichier DWG au format PDF :

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Et voila! Vous avez exporté avec succès un fichier DWG au format PDF à l'aide d'Aspose.CAD pour Java.

## Conclusion

Ce didacticiel fournit un guide étape par étape sur l'utilisation d'Aspose.CAD pour Java pour exporter des fichiers DWG au format PDF ou images raster. Cette bibliothèque simplifie le processus, vous permettant de gérer efficacement les dessins CAO dans vos applications Java.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour Java avec d’autres frameworks Java ?

A1 : Oui, Aspose.CAD pour Java s'intègre de manière transparente aux frameworks Java populaires.

### Q2 : Une licence temporaire est-elle disponible pour Aspose.CAD pour Java ?

 A2 : Oui, vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).

### Q3 : Où puis-je trouver de l'assistance pour Aspose.CAD pour Java ?

 A3 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour obtenir l'aide de la communauté.

### Q4 : Comment puis-je acheter une licence pour Aspose.CAD pour Java ?

 A4 : Vous pouvez acheter une licence[ici](https://purchase.aspose.com/buy).

### Q5 : Quelles unités Aspose.CAD pour Java prend-il en charge ?

R5 : Aspose.CAD pour Java prend en charge les unités métriques et impériales.