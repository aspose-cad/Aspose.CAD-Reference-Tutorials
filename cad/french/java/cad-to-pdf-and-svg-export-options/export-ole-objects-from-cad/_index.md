---
title: Exporter des objets OLE depuis la CAO à l'aide d'Aspose.CAD pour Java
linktitle: Exporter des objets OLE depuis la CAO
second_title: API Java Aspose.CAD
description: Libérez le potentiel d’Aspose.CAD pour Java. Exportez sans effort des objets OLE à partir de fichiers CAO. Téléchargez-le dès maintenant pour une gestion transparente des données CAO.
weight: 10
url: /fr/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter des objets OLE depuis la CAO à l'aide d'Aspose.CAD pour Java

## Introduction

Dans le monde dynamique de la conception assistée par ordinateur (CAO), la gestion et l'extraction efficaces des objets OLE (Object Linking and Embedding) sont cruciales. Aspose.CAD pour Java fournit une solution puissante pour exporter des objets OLE à partir de fichiers CAO. Ce guide étape par étape vous guidera tout au long du processus, vous assurant d'exploiter tout le potentiel de cet outil.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Environnement Java : assurez-vous d'avoir un environnement de développement Java configuré sur votre ordinateur.
-  Aspose.CAD pour Java : téléchargez et installez la bibliothèque Aspose.CAD pour Java. Vous pouvez trouver la bibliothèque au[lien de téléchargement](https://releases.aspose.com/cad/java/).
- Fichiers CAO : préparez les fichiers CAO contenant les objets OLE que vous souhaitez exporter.

## Importer des espaces de noms

Pour commencer, importez les espaces de noms nécessaires dans votre projet Java. Ces espaces de noms fournissent les classes et fonctionnalités essentielles requises pour travailler avec des fichiers CAO à l'aide d'Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Maintenant, décomposons le processus d'exportation d'objets OLE à partir de CAO en plusieurs étapes :

## Étape 1 : définissez votre répertoire de documents

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Assurez-vous de remplacer « Votre répertoire de documents » par le chemin d'accès au répertoire contenant vos fichiers CAO.

## Étape 2 : Définir les noms des fichiers CAO

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

 Spécifiez les noms des fichiers CAO que vous souhaitez traiter dans le`files` tableau.

## Étape 3 : Définir les options d'exportation PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Configurez les options d'exportation PNG, y compris les paramètres de rastérisation vectorielle et de mise en page.

## Étape 4 : Parcourir les fichiers CAO

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Parcourez chaque fichier CAO spécifié, chargez-le à l'aide d'Aspose.CAD et enregistrez les objets OLE sous forme d'images PNG.

## Conclusion

Avec ces étapes simples mais puissantes, vous pouvez exporter en toute transparence des objets OLE à partir de fichiers CAO à l'aide d'Aspose.CAD pour Java. Cet outil polyvalent permet aux développeurs de gérer efficacement les données de CAO, ouvrant ainsi de nouvelles possibilités dans le développement d'applications de CAO.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec tous les formats de fichiers CAO ?

 A1 : Aspose.CAD prend en charge divers formats de CAO, notamment DWG, DXF et DGN. Se référer au[Documentation](https://reference.aspose.com/cad/java/) pour la liste complète.

### Q2 : Puis-je personnaliser les paramètres d’exportation des objets OLE ?

A2 : Oui, Aspose.CAD propose des options étendues pour personnaliser les paramètres d'exportation, vous permettant d'adapter la sortie à vos besoins spécifiques.

### Q3 : Existe-t-il un essai gratuit disponible pour Aspose.CAD ?

 A3 : Oui, vous pouvez explorer les capacités d'Aspose.CAD en obtenant un essai gratuit auprès de[ici](https://releases.aspose.com/).

### Q4 : Où puis-je obtenir l'assistance de la communauté pour Aspose.CAD ?

 A4 : Rejoignez la communauté Aspose.CAD au[forum](https://forum.aspose.com/c/cad/19) pour demander de l'aide et partager vos expériences.

### Q5 : Comment puis-je acheter une licence pour Aspose.CAD ?

A5 : Visitez le[page d'achat](https://purchase.aspose.com/buy) pour acquérir une licence adaptée à vos besoins de développement.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
