---
title: Convertir la mise en page CAO au format d'image raster à l'aide d'Aspose.CAD pour Java
linktitle: Convertir la mise en page CAO au format d'image raster
second_title: API Java Aspose.CAD
description: Convertissez sans effort les mises en page CAO en images raster à l'aide d'Aspose.CAD pour Java. Visualisation de haute qualité pour une collaboration améliorée.
type: docs
weight: 12
url: /fr/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
---
## Introduction

Dans le monde dynamique de la conception assistée par ordinateur (CAO), la capacité de convertir de manière transparente des mises en page CAO en formats d'images raster est une compétence précieuse. Aspose.CAD pour Java apparaît comme une solution robuste pour réaliser cette tâche efficacement. Dans ce didacticiel, nous vous guiderons étape par étape tout au long du processus de conversion d'une mise en page CAO en image raster, à l'aide d'Aspose.CAD pour Java.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

1. Environnement de développement Java : assurez-vous qu'un environnement de développement Java fonctionnel est installé sur votre système.

2.  Bibliothèque Aspose.CAD : Téléchargez et installez la bibliothèque Aspose.CAD. Vous pouvez l'obtenir auprès du[Documentation Aspose.CAD pour Java](https://reference.aspose.com/cad/java/).

## Importer des espaces de noms

Commencez par importer les espaces de noms nécessaires pour utiliser les fonctionnalités d'Aspose.CAD pour Java. Dans votre code Java, incluez les espaces de noms suivants :

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

Maintenant, décomposons l'exemple de code en une série d'étapes pour convertir une mise en page CAO en image raster.
## Étape 1 : Configurer le répertoire des ressources

```java
// Le chemin d'accès au répertoire de ressources.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Assurez-vous de remplacer « Votre répertoire de documents » par le chemin d'accès à votre répertoire de documents réel.

## Étape 2 : Charger le fichier CAO

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Spécifiez le chemin d'accès à votre fichier CAO et chargez-le à l'aide d'Aspose.CAD.

## Étape 3 : configurer les options de rastérisation

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

 Créer une instance de`CadRasterizationOptions` et définissez les dimensions et les mises en page de la page.

## Étape 4 : définir les options d'image

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

 Créer une instance de`ImageOptions` et associez-le aux options de rastérisation.

## Étape 5 : Enregistrez l'image résultante

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Enregistrez l'image raster finale au format et à l'emplacement souhaités.

Répétez ces étapes, en ajustant les paramètres si nécessaire, pour personnaliser la conversion en fonction de vos besoins spécifiques.

## Conclusion

Aspose.CAD pour Java rationalise le processus de conversion des mises en page CAO en images raster, offrant flexibilité et précision. La maîtrise de cette technique ouvre des possibilités de visualisation et de collaboration efficaces dans les projets de CAO.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec différents formats de fichiers CAO ?

R1 : Oui, Aspose.CAD prend en charge une variété de formats de CAO, notamment DWG, DXF et DGN.

### Q2 : Puis-je personnaliser la résolution de l’image raster en sortie ?

 A2 : Certainement. Ajuste le`setPageWidth` et`setPageHeight` paramètres dans`CadRasterizationOptions` pour la résolution souhaitée.

### Q3 : Comment puis-je convertir plusieurs mises en page CAO simultanément ?

 A3 : étendez simplement le tableau transmis à`setLayouts` avec les noms des mises en page que vous souhaitez convertir.

### Q4 : Existe-t-il d'autres formats de sortie que le TIFF pris en charge ?

A4 : Oui, Aspose.CAD prend en charge divers formats de sortie, tels que PNG, JPG et PDF.

### Q5 : Où puis-je demander de l'aide ou partager mes expériences avec Aspose.CAD ?

A5 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour s'engager avec la communauté et obtenir du soutien.