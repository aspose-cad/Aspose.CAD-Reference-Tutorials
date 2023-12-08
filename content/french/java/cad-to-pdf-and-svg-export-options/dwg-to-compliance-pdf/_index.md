---
title: DWG vers PDF de conformité à l'aide d'Aspose.CAD pour Java
linktitle: DWG vers PDF de conformité
second_title: API Java Aspose.CAD
description: Convertissez sans effort des dessins DWG en fichiers compatibles PDF/A1a et PDF/A1b à l'aide d'Aspose.CAD pour Java. Rationalisez votre flux de travail avec précision et facilité.
type: docs
weight: 11
url: /fr/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
---
## Introduction

Dans le monde en constante évolution de la conception numérique, la nécessité de convertir les dessins DWG aux formats PDF conformes est cruciale pour une collaboration transparente et une documentation standardisée. Aspose.CAD pour Java apparaît comme un outil puissant, offrant efficacité et précision dans ce processus. Dans ce didacticiel, nous explorerons comment utiliser Aspose.CAD pour Java pour convertir sans effort des fichiers DWG en PDF conformes, garantissant le respect des normes PDF/A1a et PDF/A1b.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Environnement de développement Java : assurez-vous d'avoir configuré un environnement de développement Java fonctionnel sur votre système.
-  Bibliothèque Aspose.CAD : téléchargez et installez la bibliothèque Aspose.CAD pour Java à partir du[lien de téléchargement](https://releases.aspose.com/cad/java/).
- Répertoire de documents : créez un répertoire pour stocker vos dessins DWG.

## Importer des espaces de noms

Dans votre projet Java, importez les espaces de noms nécessaires pour accéder aux fonctionnalités d'Aspose.CAD. Ajoutez les lignes suivantes au début de votre fichier Java :

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Étape 1 : définir le répertoire des ressources

Définissez le chemin d'accès à votre répertoire de ressources dans lequel les dessins DWG sont stockés.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## Étape 2 : charger le fichier DWG

Chargez le fichier DWG à l'aide de la bibliothèque Aspose.CAD.

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Étape 3 : Créer des options PDF

Créez une instance de PdfOptions et définissez les options de rastérisation vectorielle.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Étape 4 : Définir les options PDF de base

Définissez les options PDF principales, en spécifiant la norme de conformité (PDF/A1a ou PDF/A1b).

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## Étape 5 : Enregistrez le PDF avec la conformité A1a

Enregistrez le fichier PDF avec la conformité A1a.

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## Étape 6 : Changer la conformité en A1b

Modifiez la conformité en PDF/A1b et enregistrez le PDF.

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Répétez ces étapes pour chaque fichier DWG que vous souhaitez convertir.

## Conclusion

En conclusion, Aspose.CAD pour Java fournit une solution robuste pour convertir des fichiers DWG en PDF conformes. En suivant ce guide étape par étape, vous pouvez rationaliser le processus de conversion et garantir que vos documents respectent les normes de l'industrie.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec toutes les versions de fichiers DWG ?

 A1 : Aspose.CAD prend en charge différentes versions de fichiers DWG, y compris les dernières. Se référer au[Documentation](https://reference.aspose.com/cad/java/) pour des informations détaillées sur la compatibilité.

### Q2 : Puis-je personnaliser les paramètres de sortie PDF à l’aide d’Aspose.CAD ?

A2 : Absolument ! Aspose.CAD offre une gamme d'options de personnalisation, vous permettant d'adapter la sortie PDF à vos besoins spécifiques.

### Q3 : Une licence temporaire est-elle disponible pour Aspose.CAD ?

 A3 : Oui, vous pouvez obtenir une licence temporaire à des fins de test auprès de[ce lien](https://purchase.aspose.com/temporary-license/).

### Q4 : Où puis-je demander de l'aide ou interagir avec la communauté pour Aspose.CAD ?

 A4 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien et les discussions de la communauté.

### Q5 : Puis-je essayer Aspose.CAD gratuitement avant d’effectuer un achat ?

 A5 : Certainement ! Téléchargez la version d'essai gratuite à partir de[ici](https://releases.aspose.com/) explorer les capacités avant de prendre une décision.