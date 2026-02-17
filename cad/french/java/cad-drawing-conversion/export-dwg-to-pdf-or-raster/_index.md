---
date: 2026-02-17
description: Découvrez comment la bibliothèque Java CAD Aspose.CAD pour Java peut
  exporter les fichiers DWG en PDF ou en images raster rapidement et avec précision.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Exporter DWG vers PDF ou raster à l'aide de la bibliothèque Java CAD Aspose.CAD.
url: /fr/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG en PDF ou en image raster avec la bibliothèque java cad Aspose.CAD pour Java

## Introduction

Dans le monde dynamique de la conception assistée par ordinateur (CAO), la gestion efficace des dessins est cruciale. Avec la **bibliothèque java cad** **Aspose.CAD for Java** vous pouvez **exporter dwg en pdf** — ou des images raster — en quelques lignes de code seulement. Ce tutoriel vous guide à travers le processus complet, du chargement d’un fichier DWG à la génération d’un PDF de haute qualité, tout en soulignant pourquoi Aspose.CAD Java est la bibliothèque de référence pour les tâches de conversion CAO.

## Quick Answers
- **Que couvre ce tutoriel ?** Exportation de fichiers DWG en PDF ou en images raster à l’aide d’Aspose.CAD for Java.  
- **Ai-je besoin d’une licence ?** Une licence temporaire gratuite est disponible pour l’évaluation ; une licence complète est requise pour la production.  
- **Quelle version de Java est prise en charge ?** Tout environnement d’exécution Java 8+ fonctionne avec la dernière API Aspose.CAD Java.  
- **Puis-je convertir DWG vers d’autres formats d’image ?** Oui – les mêmes options de rasterisation vous permettent de produire PNG, JPEG, BMP, etc.  
- **Combien de temps prend la conversion ?** Généralement moins d’une seconde pour les dessins standards ; les fichiers plus volumineux peuvent prendre quelques secondes.

## Why java cad library is the best choice for DWG conversion?

- **Implémentation pure Java** – aucune DLL native ni outil externe.  
- **Gestion précise des unités** – les unités métriques et impériales sont détectées automatiquement.  
- **Sortie raster de haute qualité** – DPI finement réglé et contrôle de la taille de page.  
- **Support complet du PDF** – génération de PDF préservant les vecteurs sans dépendances supplémentaires.  
- **Licence flexible** – commencez avec une **temporary license aspose** pour les tests, puis passez à une licence complète lors du déploiement.

## What is “export dwg to pdf”?

Exporter DWG en PDF signifie convertir un dessin AutoCAD natif en un document PDF portable et indépendant du dispositif. Le PDF résultant préserve les données vectorielles, les calques et l’échelle, ce qui le rend idéal pour le partage, l’impression ou l’archivage.

## Why use Aspose.CAD Java for this conversion?

Parce que la **bibliothèque java cad** gère tout, de la conversion d’unités à la rasterisation, en interne ; vous évitez la complexité des outils tiers et obtenez des résultats cohérents sur toutes les plateformes.

## Prerequisites

- Connaissances de base en programmation Java.  
- Bibliothèque Aspose.CAD for Java installée. Si vous ne l’avez pas encore téléchargée, obtenez‑la **[here](https://releases.aspose.com/cad/java/)**.  
- Un fichier DWG pour les tests – l’exemple **Bottom_plate.dwg** est utilisé dans ce guide.

## Import Namespaces

Dans votre projet Java, importez les classes nécessaires pour démarrer la conversion :

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG File

Tout d’abord, chargez votre dessin DWG à l’aide de la classe `Image`. Cela crée une représentation en mémoire avec laquelle Aspose.CAD peut travailler.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Step 2: Determine Unit Type

Comprendre si le dessin utilise des unités métriques ou impériales est essentiel pour un bon redimensionnement. La méthode d’assistance `IsMetric` (implémentation omise pour la concision) renvoie un booléen.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Step 3: Set Rasterization Options

En fonction du système d’unités, configurez la taille de page, le facteur d’échelle et le type d’unité cible. Ces options déterminent la façon dont le DWG est rasterisé avant d’être intégré dans un PDF.

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

### Step 4: Configure PDF Options (pdf options cad)

Créez une instance `PdfOptions` et associez‑y les paramètres de rasterisation. Cela indique à Aspose.CAD comment incorporer le contenu rasterisé dans le PDF final.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Step 5: Save as PDF

Enfin, exportez le dessin vers un fichier PDF. La méthode `save` prend le chemin de sortie et les `PdfOptions` configurés.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Lorsque le code se termine, vous trouverez **Saved.pdf** dans votre dossier `DWGDrawings`, prêt à être distribué ou archivé.

## How to convert dwg raster images with java cad library

Si vous avez besoin d’images raster au lieu d’un PDF, remplacez simplement `PdfOptions` par les options d’image raster appropriées (par ex., `PngOptions`, `JpegOptions`). La même instance `CadRasterizationOptions` peut être réutilisée, vous permettant de **convertir dwg raster** avec peu de modifications de code.

## How to generate pdf dwg using pdf options cad

L’exemple ci‑dessus génère déjà une sortie **pdf dwg**. En ajustant `pdfOptions` — par exemple en appelant `pdfOptions.setCompress(true)` — vous pouvez contrôler la taille et la qualité du PDF. Cela montre la flexibilité de l’API **pdf options cad**.

## Common Issues & Tips

- **Taille de page incorrecte** – Vérifiez la logique de conversion d’unités ; des coefficients mal assortis peuvent produire des pages surdimensionnées.  
- **Polices ou épaisseurs de ligne manquantes** – Assurez‑vous que le DWG référence toutes les ressources externes avant la conversion.  
- **Performance sur de gros dessins** – Augmentez le paramètre `DPI` dans `CadRasterizationOptions` uniquement lorsque une qualité supérieure est requise ; un DPI plus bas accélère le traitement.  
- **Problèmes de licence** – Pour l’évaluation, vous pouvez utiliser une **temporary license aspose** ; une licence complète est nécessaire pour les déploiements en production.

## Frequently Asked Questions

**Q : Puis‑je utiliser Aspose.CAD for Java avec d’autres frameworks Java ?**  
A : Oui, Aspose.CAD for Java s’intègre parfaitement aux frameworks Java populaires tels que Spring, Jakarta EE et Android.

**Q : Une licence temporaire est‑elle disponible pour Aspose.CAD for Java ?**  
A : Oui, vous pouvez obtenir une licence temporaire **[here](https://purchase.aspose.com/temporary-license/)**.

**Q : Où puis‑je trouver du support pour Aspose.CAD for Java ?**  
A : Consultez le **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** pour obtenir de l’aide de la communauté et des ingénieurs Aspose.

**Q : Comment puis‑je acheter une licence pour Aspose.CAD for Java ?**  
A : Vous pouvez acheter une licence **[here](https://purchase.aspose.com/buy)**.

**Q : Quelles unités Aspose.CAD for Java prend‑il en charge ?**  
A : Aspose.CAD for Java prend en charge les unités métriques et impériales, détectant automatiquement le système d’unités du dessin.

**Q : Puis‑je convertir DWG vers d’autres formats d’image (par ex., PNG, JPEG) avec la même API ?**  
A : Absolument. Remplacez `PdfOptions` par les options d’image raster appropriées (par ex., `PngOptions`) et réutilisez le même `CadRasterizationOptions`.

## Conclusion

Ce tutoriel a démontré comment **exporter dwg en pdf** et en images raster à l’aide de la **bibliothèque java cad** Aspose.CAD for Java. En suivant le guide étape par étape, vous pouvez intégrer une conversion CAO fiable dans n’importe quelle application Java, que vous ayez besoin de PDF pour la documentation ou d’images raster pour l’affichage Web.

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}