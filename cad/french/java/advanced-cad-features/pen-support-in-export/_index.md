---
date: 2025-12-10
description: Apprenez à créer un PDF à partir de CAD en utilisant Aspose.CAD pour
  Java avec la personnalisation du stylo. Ce guide étape par étape montre comment
  exporter efficacement le CAD en PDF.
linktitle: Pen Support in Export
second_title: Aspose.CAD Java API
title: Comment créer un PDF à partir de CAD avec prise en charge du stylet lors de
  l'exportation
url: /fr/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Support du stylo lors de l'exportation

## Introduction

Dans le monde en évolution rapide des conversions CAD, les développeurs ont souvent besoin de **create PDF from CAD** tout en préservant la fidélité visuelle. Aspose.CAD for Java rend cela simple, offrant des options riches telles que la personnalisation du stylo qui vous permettent d’ajuster finement les styles de ligne pendant le processus d’exportation. Dans ce guide, nous parcourrons un exemple complet et pratique montrant comment **export CAD to PDF** avec des paramètres de stylo personnalisés, afin que vous puissiez générer des PDF soignés directement à partir de dessins DXF.

## Réponses rapides
- **What does “create PDF from CAD” mean?** Conversion d’un dessin CAD (par ex., DXF) en document PDF tout en conservant la qualité vectorielle.  
- **Which library handles pen customization?** La classe `PenOptions` d’Aspose.CAD for Java.  
- **Can I use this for other formats?** Oui – les mêmes paramètres de stylo s’appliquent à PNG, BMP, TIFF, etc.  
- **Do I need a license?** Une licence valide Aspose.CAD est requise pour une utilisation en production.  
- **What’s the minimum Java version?** Java 8 ou supérieur.

## Qu'est-ce que « créer un PDF à partir de CAD » ?
Créer un PDF à partir de CAD signifie rasteriser ou rendre vectoriellement un dessin CAD dans un fichier PDF. Cela permet de partager, d’imprimer et d’archiver facilement des conceptions d’ingénierie sans nécessiter le logiciel CAD chez le destinataire.

## Pourquoi utiliser le support du stylo lors de l'exportation de CAD vers PDF ?
Le support du stylo vous permet de contrôler les extrémités, les jointures et l’épaisseur des lignes, vous offrant la possibilité d’aligner le rendu sur la charte graphique de l’entreprise ou sur les normes de dessin technique. C’est particulièrement utile lorsque le rendu de ligne par défaut ne répond pas à vos exigences visuelles.

## Prérequis

- **Java Development Environment** – un JDK fonctionnel (8 ou plus récent) et un IDE ou un outil de construction de votre choix.  
- **Aspose.CAD Library** – téléchargez le JAR le plus récent depuis le site officiel [here](https://releases.aspose.com/cad/java/).  
- **A sample DXF file** – pour ce tutoriel, nous utiliserons `conic_pyramid.dxf`.

Maintenant que le contexte est posé, plongeons dans le code.

## Importer les espaces de noms

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## Étape 1 : Définir votre répertoire de documents

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

> **Pro tip:** Remplacez `"Your Document Directory"` par le chemin absolu où résident vos fichiers DXF.

## Étape 2 : Charger le fichier CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

La méthode `Image.load` lit le fichier DXF et crée un objet `CadImage` que nous pouvons manipuler.

## Étape 3 : Configurer les options de rasterisation

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

Ajustez les dimensions de la page pour contrôler la résolution du PDF résultant. Multiplier par 100 donne une sortie haute résolution adaptée à l’impression.

## Étape 4 : Personnaliser les options du stylo

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

Ici, nous définissons à la fois les caps de départ et de fin du stylo sur `Flat`. Vous pouvez expérimenter d’autres valeurs `LineCap` (par ex., `Round`, `Square`) pour obtenir différents effets visuels.

## Étape 5 : Configurer les options d'exportation PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

L’objet `PdfOptions` lie les paramètres de rasterisation au processus d’exportation PDF.

## Étape 6 : Enregistrer le PDF exporté

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

L’exécution de cette ligne écrit un fichier PDF nommé `9LHATT-A56_generated.pdf` dans votre dossier `dataDir`, complet avec le style de stylo personnalisé que vous avez défini.

## Cas d'utilisation courants

- **Technical documentation** – intégrer des dessins d’ingénierie précis dans des manuels PDF.  
- **Automated reporting** – générer des PDF à partir de données CAD à la volée dans des services web.  
- **Quality control** – appliquer des caps de ligne personnalisés pour mettre en évidence des lignes de mesure ou des tolérances.

## Dépannage et astuces

- **Incorrect file path** – assurez‑vous que `dataDir` se termine par un séparateur de fichier (`/` ou `\\`).  
- **Missing license** – sans licence valide, la bibliothèque fonctionne en mode évaluation, ce qui peut ajouter des filigranes.  
- **Unexpected line styles** – vérifiez que les `PenOptions` sont définies avant d’appeler `save` ; sinon les valeurs par défaut sont utilisées.

## FAQ

### Q1 : Puis-je personnaliser les options du stylo pour des formats autres que PDF ?

A1 : Oui, la personnalisation du stylo présentée dans ce tutoriel s’applique à divers formats d’image, y compris PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF et WMF.

### Q2 : Comment gérer différentes extrémités de départ et d'arrivée pour les stylos ?

A2 : Utilisez la classe `PenOptions` pour définir les caps de départ et de fin souhaités, offrant ainsi une flexibilité dans la définition de l’apparence des lignes.

### Q3 : Que se passe-t-il si je ne spécifie pas d'options de stylo ?

A3 : Si les options de stylo ne sont pas explicitement définies, le système utilisera ses stylos par défaut, qui peuvent varier selon les contextes.

### Q4 : Y a-t-il des considérations spécifiques pour les options de rasterisation ?

A4 : Ajustez la largeur et la hauteur de la page dans les options de rasterisation pour contrôler les dimensions de l’image exportée.

### Q5 : Où puis‑je trouver un support supplémentaire ou des discussions communautaires ?

A5 : Explorez le forum communautaire Aspose.CAD à [here](https://forum.aspose.com/c/cad/19) pour obtenir de l’aide et participer aux discussions.

---

**Dernière mise à jour :** 2025-12-10  
**Testé avec :** Aspose.CAD 24.11 for Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}