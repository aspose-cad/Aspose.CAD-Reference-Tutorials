---
date: 2025-12-18
description: Apprenez à convertir DWG en PNG et d’autres formats d’image raster avec
  Aspose.CAD pour Java. Exportez le CAD en PNG avec des résultats de haute qualité.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Convertir DWG en PNG et autres formats raster avec Aspose.CAD pour Java
url: /fr/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWG en PNG et autres formats raster avec Aspose.CAD pour Java

## Introduction

Convertir un fichier DWG en PNG (ou d’autres formats d’image raster) est une exigence fréquente lorsque vous devez partager des dessins CAO avec des collègues qui n’ont pas de visionneur CAO, intégrer des conceptions dans de la documentation ou générer des vignettes pour des galeries web. Aspose.CAD pour Java rend cette conversion simple, que vous travailliez avec un fichier complet ou uniquement avec une mise en page spécifique. Dans ce tutoriel, nous parcourrons les étapes exactes pour **convertir une mise en page CAO en image raster** — la même technique que vous pouvez appliquer pour produire des sorties PNG, JPEG, TIFF ou PDF.

## Réponses rapides
- **Quelle bibliothèque gère la conversion DWG → PNG ?** Aspose.CAD pour Java  
- **Quels formats peuvent être exportés ?** PNG, JPEG, TIFF, PDF, BMP, et plus encore  
- **Une licence est‑elle nécessaire pour les tests ?** Une version d’essai gratuite suffit pour le développement ; une licence est requise en production  
- **Puis‑je choisir une mise en page spécifique ?** Oui, utilisez `setLayouts` pour cibler « Model », « Layout1 », etc.  
- **Est‑il possible d’obtenir une sortie haute résolution ?** Absolument — ajustez `setPageWidth` et `setPageHeight` pour contrôler le DPI  

## Qu’est‑ce que “convert dwg to png” ?

L’expression « convert dwg to png » décrit le processus consistant à prendre un fichier DWG vectoriel (le format natif de nombreuses applications CAO) et à le rasteriser en une image PNG basée sur des pixels. Les images raster sont idéales pour l’affichage web, le partage par e‑mail et l’intégration dans des logiciels non‑CAO.

## Pourquoi exporter la CAO en PNG (ou autres formats raster) ?

- **Compatibilité universelle :** PNG et JPEG sont pris en charge par pratiquement tous les visionneurs d’images et navigateurs.  
- **Chargement rapide :** Les images raster s’affichent instantanément comparées à l’ouverture d’un fichier DWG volumineux.  
- **Intégration facile :** Insérez des PNG directement dans Word, PowerPoint ou HTML sans plugins supplémentaires.  
- **Aspect cohérent :** Vous contrôlez la résolution, l’arrière‑plan et la mise en page, garantissant que chaque partie prenante voit le même rendu.  

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

1. **Environnement de développement Java** – JDK 8 ou version ultérieure installé et configuré.  
2. **Aspose.CAD pour Java** – Téléchargez le JAR le plus récent depuis la [documentation Aspose.CAD pour Java](https://reference.aspose.com/cad/java/).  

## Importer les espaces de noms

Tout d’abord, importez les classes dont vous aurez besoin. Ces imports vous donnent accès au chargement d’image, aux options de rasterisation et aux paramètres de sortie TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Astuce :** Si vous prévoyez d’exporter en PNG au lieu de TIFF, remplacez `TiffOptions` par `PngOptions` (disponible dans `com.aspose.cad.imageoptions.PngOptions`).  

## Guide étape par étape

### Étape 1 : Configurer le répertoire des ressources

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Remplacez `"Your Document Directory"` par le chemin absolu où se trouvent vos fichiers CAO.

### Étape 2 : Charger le fichier CAO

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Vous pouvez charger n’importe quel format supporté (DWG, DXF, DGN, etc.). C’est la partie **how to convert cad** — il suffit de pointer vers le fichier et de laisser Aspose gérer l’analyse.

### Étape 3 : Configurer les options de rasterisation

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` contrôlent la résolution de sortie (des valeurs plus grandes = DPI plus élevé).  
- `setLayouts` vous permet de **convert cad to raster** pour des mises en page spécifiques ; omettez‑le pour rasteriser le dessin complet.

### Étape 4 : Définir les options d’image

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Si vous préférez le PNG, créez une instance de `PngOptions` au lieu de `TiffOptions`. C’est ici que vous **export cad as png**.

### Étape 5 : Enregistrer l’image résultante

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Modifiez l’extension du fichier en `.png` (et l’objet d’options en `PngOptions`) pour **save CAD as JPEG/PNG**.

> **Erreur fréquente :** Oublier d’associer l’extension du fichier à la classe d’options entraîne une `UnsupportedFormatException`. Gardez toujours les deux en accord.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Image de sortie vide** | Vérifiez que les noms de mise en page dans `setLayouts` correspondent exactement à ceux du fichier CAO source. |
| **PNG basse résolution** | Augmentez `setPageWidth` / `setPageHeight` ou définissez `setResolution` dans les options de rasterisation. |
| **Version DWG non prise en charge** | Assurez‑vous d’utiliser la dernière version d’Aspose.CAD ; les versions plus anciennes peuvent ne pas supporter les nouvelles versions DWG. |
| **Erreurs de mémoire sur de gros fichiers** | Traitez les pages une à une ou augmentez le tas JVM (`-Xmx2g`). |

## Questions fréquentes

**Q : Aspose.CAD est‑il compatible avec différents formats de fichiers CAO ?**  
R : Oui, il prend en charge DWG, DXF, DGN et bien d’autres.

**Q : Puis‑je personnaliser la résolution de l’image raster de sortie ?**  
R : Absolument. Ajustez `setPageWidth`, `setPageHeight` ou `setResolution` dans `CadRasterizationOptions`.

**Q : Comment convertir plusieurs mises en page CAO en une seule exécution ?**  
R : Fournissez un tableau contenant tous les noms de mise en page à `setLayouts`, par ex. `new String[]{"Model","Layout1","Layout2"}`.

**Q : Existe‑t‑il d’autres formats de sortie que le TIFF ?**  
R : Oui — PNG, JPEG, BMP, PDF et d’autres sont disponibles via leurs classes `*Options` respectives.

**Q : Où puis‑je obtenir de l’aide ou partager mon expérience avec Aspose.CAD ?**  
R : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire et l’assistance officielle.

## Conclusion

En suivant ces étapes, vous pouvez **convertir DWG en PNG**, **exporter la CAO en PNG**, **enregistrer la CAO en JPEG**, ou générer tout autre format raster dont vous avez besoin. Aspose.CAD pour Java se charge du travail lourd, vous permettant de vous concentrer sur l’intégration d’images de haute qualité dans vos applications, documentation ou portails web.

---

**Dernière mise à jour :** 2025-12-18  
**Testé avec :** Aspose.CAD pour Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}