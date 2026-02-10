---
date: 2025-12-18
description: Explorez comment exporter des DWG en PDF ou en images raster en Java
  avec Aspose.CAD. Ce guide étape par étape garantit précision, efficacité et conversion
  facile des fichiers DWG.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Exporter DWG vers PDF ou raster avec Aspose.CAD pour Java
url: /fr/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter DWG en PDF ou en image raster avec Aspose.CAD pour Java

## Introduction

Dans le monde dynamique de la conception assistée par ordinateur (CAO), la gestion efficace des dessins est cruciale. Avec **Aspose.CAD pour Java**, vous pouvez **exporter dwg en pdf** — ou en images raster — en quelques lignes de code seulement. Ce tutoriel vous guide à travers l’ensemble du processus, du chargement d’un fichier DWG à la génération d’un PDF de haute qualité, tout en soulignant pourquoi Aspose.CAD Java est la bibliothèque de référence pour les tâches de conversion CAO.

## Réponses rapides
- **Que couvre ce tutoriel ?** Exportation de fichiers DWG vers PDF ou images raster à l’aide d’Aspose.CAD pour Java.  
- **Ai‑je besoin d’une licence ?** Une licence temporaire gratuite est disponible pour l’évaluation ; une licence complète est requise en production.  
- **Quelle version de Java est prise en charge ?** Tout environnement Java 8+ fonctionne avec la dernière API Aspose.CAD Java.  
- **Puis‑je convertir DWG vers d’autres formats d’image ?** Oui – les mêmes options de rasterisation permettent de produire PNG, JPEG, BMP, etc.  
- **Combien de temps dure la conversion ?** Généralement moins d’une seconde pour les dessins standards ; les fichiers plus volumineux peuvent prendre quelques secondes.

## Qu’est‑ce que « export dwg to pdf » ?
Exporter DWG en PDF signifie convertir un dessin AutoCAD natif en un document PDF portable et indépendant du dispositif. Le PDF résultant conserve les données vectorielles, les calques et l’échelle, ce qui le rend idéal pour le partage, l’impression ou l’archivage.

## Pourquoi utiliser Aspose.CAD Java pour cette conversion ?
- **Aucune dépendance externe** – pur Java, aucune DLL native.  
- **Gestion précise des unités** – respecte automatiquement les unités métriques ou impériales.  
- **Sortie raster de haute qualité** – contrôle fin du DPI et de la taille de page.  
- **Support complet du PDF** – génération de PDF vectoriel sans bibliothèques supplémentaires.

## Prérequis

Avant de plonger dans le code, assurez‑vous de disposer de :

- Connaissances de base en programmation Java.  
- Bibliothèque Aspose.CAD pour Java installée. Si vous ne l’avez pas encore téléchargée, obtenez‑la **[ici](https://releases.aspose.com/cad/java/)**.  
- Un fichier DWG pour les tests – l’exemple **Bottom_plate.dwg** est utilisé dans ce guide.

## Importer les espaces de noms

Dans votre projet Java, importez les classes nécessaires pour lancer la conversion :

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Guide étape par étape

### Étape 1 : Charger le fichier DWG

Tout d’abord, chargez votre dessin DWG à l’aide de la classe `Image`. Cela crée une représentation en mémoire avec laquelle Aspose.CAD peut travailler.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Étape 2 : Déterminer le type d’unité

Comprendre si le dessin utilise des unités métriques ou impériales est essentiel pour un bon dimensionnement. La méthode d’assistance `IsMetric` (implémentation omise pour la brièveté) renvoie un booléen.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Étape 3 : Configurer les options de rasterisation

En fonction du système d’unités, configurez la taille de page, le facteur d’échelle et le type d’unité cible. Ces options déterminent comment le DWG est rasterisé avant d’être intégré dans un PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Étape 4 : Configurer les options PDF

Créez une instance de `PdfOptions` et associez‑y les paramètres de rasterisation. Cela indique à Aspose.CAD comment incorporer le contenu rasterisé dans le PDF final.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Étape 5 : Enregistrer en PDF

Enfin, exportez le dessin vers un fichier PDF. La méthode `save` prend le chemin de sortie et les `PdfOptions` configurés.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Lorsque le code se termine, vous trouverez **Saved.pdf** dans votre dossier `DWGDrawings`, prêt à être distribué ou archivé.

## Problèmes courants et conseils

- **Taille de page incorrecte** – Vérifiez la logique de conversion d’unités ; des coefficients mal assortis peuvent produire des pages surdimensionnées.  
- **Polices ou épaisseurs de ligne manquantes** – Assurez‑vous que le DWG référence toutes les ressources externes avant la conversion.  
- **Performance sur de gros dessins** – Augmentez le paramètre `DPI` dans `CadRasterizationOptions` uniquement lorsque vous avez besoin d’une qualité supérieure ; un DPI plus bas accélère le traitement.

## Questions fréquentes

**Q : Puis‑je utiliser Aspose.CAD pour Java avec d’autres frameworks Java ?**  
R : Oui, Aspose.CAD pour Java s’intègre parfaitement aux frameworks Java populaires tels que Spring, Jakarta EE et Android.

**Q : Une licence temporaire est‑elle disponible pour Aspose.CAD pour Java ?**  
R : Oui, vous pouvez obtenir une licence temporaire **[ici](https://purchase.aspose.com/temporary-license/)**.

**Q : Où puis‑je trouver du support pour Aspose.CAD pour Java ?**  
R : Consultez le **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)** pour obtenir de l’aide de la communauté et des ingénieurs Aspose.

**Q : Comment acheter une licence pour Aspose.CAD pour Java ?**  
R : Vous pouvez acheter une licence **[ici](https://purchase.aspose.com/buy)**.

**Q : Quelles unités Aspose.CAD pour Java prend‑il en charge ?**  
R : Aspose.CAD pour Java supporte à la fois les unités métriques et impériales, détectant automatiquement le système d’unités du dessin.

**Q : Puis‑je convertir DWG vers d’autres formats d’image (par ex. PNG, JPEG) avec la même API ?**  
R : Absolument. Remplacez `PdfOptions` par les options d’image raster appropriées (par ex. `PngOptions`) et réutilisez les mêmes `CadRasterizationOptions`.

## Conclusion

Ce tutoriel a démontré comment **exporter dwg en pdf** et en images raster à l’aide d’Aspose.CAD pour Java. En suivant le guide étape par étape, vous pouvez intégrer une conversion CAO fiable dans n’importe quelle application Java, que vous ayez besoin de PDF pour la documentation ou d’images raster pour l’affichage web.

---

**Dernière mise à jour :** 2025-12-18  
**Testé avec :** Aspose.CAD pour Java 24.10  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}