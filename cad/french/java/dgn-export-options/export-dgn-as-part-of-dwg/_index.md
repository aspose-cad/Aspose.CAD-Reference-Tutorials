---
date: 2026-01-10
description: Apprenez à exporter le DGN en DWG et à convertir les fichiers MicroStation
  DGN en DWG AutoCAD à l'aide d'Aspose.CAD pour Java. Guide étape par étape.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Exporter DGN vers DWG avec Aspose.CAD pour Java
url: /fr/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter DGN vers DWG avec Aspose.CAD pour Java

## Introduction

Dans ce tutoriel, vous apprendrez comment **exporter dgn vers dwg** et intégrer un dessin MicroStation DGN à l'intérieur d'un fichier AutoCAD DWG en utilisant la bibliothèque Aspose.CAD pour Java. Que vous migriez des dessins MicroStation hérités ou que vous ayez besoin de combiner des sous‑couches DGN avec des mises en page DWG, ce guide vous accompagne à chaque étape — de la configuration de l'environnement à la génération d'un aperçu PDF du DWG final.

## Réponses rapides
- **Quel est l’objectif de “export dgn to dwg” ?** Il intègre une sous‑couche DGN dans un DWG, permettant une visualisation fluide dans AutoCAD.
- **Quel format puis‑je exporter pour un aperçu rapide ?** Vous pouvez **exporter le fichier CAD en pdf** en utilisant `PdfOptions`.
- **Ai‑je besoin d’une licence pour exécuter le code ?** Une licence Aspose.CAD temporaire ou payante est requise pour une utilisation en production.
- **Quelle version de Java est prise en charge ?** Java 8 ou ultérieure fonctionne avec la dernière version d’Aspose.CAD pour Java.
- **Une version d’essai gratuite est‑elle disponible ?** Oui – téléchargez une version d’essai depuis le site d’Aspose.

## Qu’est‑ce que “export dgn to dwg” ?
Exporter DGN vers DWG signifie convertir ou intégrer un dessin MicroStation DGN en tant que sous‑couche dans un dessin AutoCAD DWG. Cela permet aux professionnels du CAO de réutiliser les actifs DGN existants sans recréer la géométrie à partir de zéro.

## Pourquoi convertir MicroStation DGN en AutoCAD DWG ?
- **Collaboration :** Les équipes utilisant AutoCAD peuvent visualiser et modifier le contenu DGN directement.
- **Standardisation :** DWG est le format de facto pour de nombreux flux de travail en aval (par ex., génération de PDF, rendu 3D).
- **Préservation :** Conserve les références DGN originales intactes, réduisant la perte de données.

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous d’avoir les prérequis suivants en place :

1. **Bibliothèque Aspose.CAD :** Téléchargez et installez la bibliothèque Aspose.CAD pour Java. Vous pouvez trouver la bibliothèque [ici](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK) :** Assurez‑vous d’avoir Java installé sur votre système.
3. **Environnement de développement intégré (IDE) :** Choisissez un IDE Java tel qu’Eclipse ou IntelliJ pour une expérience de développement plus fluide.

## Importer les packages

Dans votre projet Java, importez les packages Aspose.CAD nécessaires pour permettre la manipulation de fichiers CAD. Voici un exemple :

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Étape 1 : Définir les chemins de fichiers

Définissez les chemins d’accès d’entrée et de sortie pour le fichier DWG. Mettez à jour les variables `dataDir`, `fileName` et `outPath` en conséquence.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Étape 2 : Créer une instance de PdfOptions

Créez une instance de la classe `PdfOptions`, car nous **exportons le fichier CAD en PDF** pour une vérification rapide.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Étape 3 : Charger le fichier DWG

Chargez le fichier DWG existant en tant qu’image et convertissez‑le en type `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Étape 4 : Parcourir les entités

Parcourez chaque entité du fichier DWG et vérifiez s’il s’agit d’une définition d’image. Si c’est le cas, récupérez la référence externe de l’objet.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Étape 5 : Définir les options de rasterisation

Définissez les paramètres de l’objet `CadRasterizationOptions`, incluant la largeur et la hauteur de la page, les mises en page et la couleur d’arrière‑plan.

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

## Étape 6 : Définir les options de rasterisation vectorielle

Définissez les options de rasterisation vectorielle pour l’exportation.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Étape 7 : Exporter le DWG en PDF

Enfin, exportez le DWG en PDF en appelant la méthode `save`.

```java
cadImage.save(outPath, exportOptions);
```

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **Aucune sous‑couche DGN n’apparaît** | Le DWG ne contient pas d’entité `DGNUNDERLAY`. | Vérifiez que le DWG source inclut une référence DGN. |
| **Le PDF est vide** | Les options de rasterisation sont définies à une taille zéro ou à une mauvaise mise en page. | Assurez‑vous que `setPageWidth`/`setPageHeight` sont positifs et que `setLayouts` correspond au nom de la mise en page DWG. |
| **Exception de licence** | Exécution sans licence Aspose.CAD valide. | Appliquez une licence temporaire ou achetée avant d’appeler toute méthode API. |

## Questions fréquentes

### Q1 : Où puis‑je trouver la documentation d’Aspose.CAD pour Java ?
R1 : La documentation est disponible [ici](https://reference.aspose.com/cad/java/).

### Q2 : Comment télécharger la bibliothèque Aspose.CAD pour Java ?
R2 : Vous pouvez télécharger la bibliothèque depuis [ce lien](https://releases.aspose.com/cad/java/).

### Q3 : Une version d’essai gratuite est‑elle disponible pour Aspose.CAD pour Java ?
R3 : Oui, vous pouvez trouver la version d’essai [ici](https://releases.aspose.com/).

### Q4 : Où puis‑je obtenir une licence temporaire pour Aspose.CAD pour Java ?
R4 : Obtenez une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Besoin d’aide ou avez‑vous des questions ?
R5 : Visitez le forum de support communautaire Aspose.CAD [ici](https://forum.aspose.com/c/cad/19).

### Q6 : Puis‑je reconvertir le PDF résultant en DWG ?
R6 : Le PDF est un aperçu raster ; la conversion vers DWG nécessite un outil de rétro‑ingénierie séparé.

### Q7 : Cette approche fonctionne‑t‑elle avec d’autres formats CAD comme DWF ou DXF ?
R7 : Oui, Aspose.CAD prend en charge de nombreux formats ; vous devez simplement ajuster les extensions de fichiers et les paramètres de rasterisation en conséquence.

---

**Dernière mise à jour :** 2026-01-10  
**Testé avec :** Aspose.CAD for Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}