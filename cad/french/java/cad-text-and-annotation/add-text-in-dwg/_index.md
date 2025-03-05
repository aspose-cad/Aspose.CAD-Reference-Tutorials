---
title: Ajouter du texte dans DWG à l'aide d'Aspose.CAD pour Java
linktitle: Ajouter du texte dans DWG
second_title: API Java Aspose.CAD
description: Améliorez vos dessins DWG sans effort avec Aspose.CAD pour Java. Ajoutez du texte en toute transparence grâce à notre guide étape par étape.
type: docs
weight: 10
url: /fr/java/cad-text-and-annotation/add-text-in-dwg/
---
## Introduction

Dans le domaine de la conception assistée par ordinateur (CAO), Aspose.CAD pour Java se distingue comme un outil puissant pour manipuler et convertir des dessins DWG. L'une de ses fonctionnalités pratiques est la possibilité d'ajouter du texte aux fichiers DWG de manière transparente. Dans ce didacticiel, nous vous guiderons tout au long du processus d'ajout de texte à vos dessins DWG à l'aide d'Aspose.CAD pour Java.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Bibliothèque Aspose.CAD pour Java : téléchargez et installez la bibliothèque à partir du[Page Aspose.CAD pour Java](https://releases.aspose.com/cad/java/).

- Kit de développement Java (JDK) : assurez-vous que le dernier JDK est installé sur votre système.

- Dessin DWG : préparez un fichier de dessin DWG dans lequel vous souhaitez ajouter du texte.

## Importer des espaces de noms

Dans votre code Java, importez les espaces de noms nécessaires pour Aspose.CAD :

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Maintenant, décomposons l'extrait de code fourni en plusieurs étapes :

## Étape 1 : Configurer le répertoire de documents et le chemin du fichier DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Étape 2 : Charger l'image DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Étape 3 : Créer un objet CadText

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);
cadText.setScaleX(0);
```

## Étape 4 : ajouter du texte à CadImage

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Étape 5 : Configurer les options PDF

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Étape 6 : Configurer les options de CadRasterization

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Étape 7 : Enregistrez le DWG modifié au format PDF

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

En suivant ces étapes, vous pourrez ajouter en toute transparence du texte à vos dessins DWG à l'aide d'Aspose.CAD pour Java.

## Conclusion

Aspose.CAD pour Java permet aux développeurs d'améliorer et de modifier les dessins DWG par programmation. Ce didacticiel a fourni un guide clair, étape par étape, pour ajouter du texte à vos fichiers DWG, mettant en valeur la simplicité et la puissance d'Aspose.CAD.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec toutes les versions de fichiers DWG ?

A1 : Aspose.CAD prend en charge différentes versions de fichiers DWG, garantissant la compatibilité avec une large gamme de logiciels de CAO.

### Q2 : Puis-je personnaliser la police et le formatage du texte ajouté ?

A2 : Oui, vous pouvez personnaliser la police, le style et d'autres options de formatage du texte ajouté aux fichiers DWG à l'aide d'Aspose.CAD.

### Q3 : Existe-t-il un essai gratuit disponible pour Aspose.CAD pour Java ?

 A3 : Oui, vous pouvez explorer les fonctionnalités d'Aspose.CAD en obtenant un essai gratuit auprès de[ici](https://releases.aspose.com/).

### Q4 : Où puis-je trouver une documentation détaillée pour Aspose.CAD pour Java ?

 A4 : Se référer à la documentation[ici](https://reference.aspose.com/cad/java/) pour des informations détaillées et des exemples.

### Q5 : Comment puis-je obtenir de l'aide ou demander de l'aide avec Aspose.CAD ?

A5 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour obtenir de l'aide et entrer en contact avec la communauté.