---
title: Exporter DGN vers DWG avec Aspose.CAD pour Java
linktitle: Exporter DGN dans le cadre de DWG
second_title: API Java Aspose.CAD
description: Découvrez comment exporter du DGN dans le cadre de DWG à l'aide d'Aspose.CAD pour Java. Suivez notre guide étape par étape pour une manipulation efficace des fichiers CAO.
type: docs
weight: 10
url: /fr/java/dgn-export-options/export-dgn-as-part-of-dwg/
---
## Introduction

Dans ce didacticiel, nous verrons comment utiliser Aspose.CAD pour Java pour exporter un fichier DGN (MicroStation Design) dans le cadre d'un fichier DWG (AutoCAD Drawing). Aspose.CAD est une bibliothèque puissante qui fournit des fonctionnalités complètes pour travailler avec les formats de fichiers CAO. Ce guide étape par étape vous aidera à comprendre le processus d'exportation de DGN dans le cadre de DWG à l'aide de Java.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :
1. Bibliothèque Aspose.CAD : téléchargez et installez la bibliothèque Aspose.CAD pour Java. Vous pouvez trouver la bibliothèque[ici](https://releases.aspose.com/cad/java/).
2. Kit de développement Java (JDK) : assurez-vous que Java est installé sur votre système.
3. Environnement de développement intégré (IDE) : choisissez un IDE Java comme Eclipse ou IntelliJ pour une expérience de développement plus fluide.

## Importer des packages

Dans votre projet Java, importez les packages Aspose.CAD nécessaires pour activer la manipulation des fichiers CAO. Voici un exemple :

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Étape 1 : Définir les chemins de fichiers

 Définissez les chemins d'accès aux fichiers d'entrée et de sortie pour le fichier DWG. Mettre à jour le`dataDir`, `fileName` , et`outPath` variables en conséquence.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Étape 2 : Créer une instance PDFOptions

 Créez une instance du`PdfOptions` classe, car nous exportons le fichier DWG au format PDF.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Étape 3 : Charger le fichier DWG

 Chargez le fichier DWG existant en tant qu'image et convertissez-le au format`CadImage` taper.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Étape 4 : Parcourir les entités

Parcourez chaque entité dans le fichier DWG et vérifiez s'il s'agit d'une définition d'image. Si tel est le cas, récupérez la référence externe à l’objet.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Étape 5 : Définir les options de rastérisation

 Définir les paramètres du`CadRasterizationOptions`objet, y compris la largeur, la hauteur, la mise en page et la couleur d'arrière-plan de la page.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Étape 6 : Définir les options de rastérisation vectorielle

Définissez les options de rastérisation vectorielle pour l'exportation.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Étape 7 : Exporter un fichier DWG au format PDF

 Enfin, exportez le DWG au format PDF en appelant le`save` méthode.

```java
cadImage.save(outPath, exportOptions);
```

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment exporter un fichier DGN dans le cadre d'un fichier DWG à l'aide d'Aspose.CAD pour Java. Cette puissante bibliothèque offre des fonctionnalités étendues pour travailler avec des fichiers CAO, rendant vos tâches de manipulation de fichiers CAO efficaces et simples.

## FAQ

### Q1 : Où puis-je trouver la documentation d'Aspose.CAD pour Java ?

 A1 : La documentation peut être trouvée[ici](https://reference.aspose.com/cad/java/).

### Q2 : Comment puis-je télécharger la bibliothèque Aspose.CAD pour Java ?

 A2 : Vous pouvez télécharger la bibliothèque depuis[ce lien](https://releases.aspose.com/cad/java/).

### Q3 : Existe-t-il un essai gratuit disponible pour Aspose.CAD pour Java ?

 A3 : Oui, vous pouvez trouver l'essai gratuit[ici](https://releases.aspose.com/).

### Q4 : Où puis-je obtenir une licence temporaire pour Aspose.CAD pour Java ?

 A4 : Obtenir un permis temporaire[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Besoin d'aide ou avez des questions ?

 A5 : Visitez le forum d'assistance de la communauté Aspose.CAD[ici](https://forum.aspose.com/c/cad/19).