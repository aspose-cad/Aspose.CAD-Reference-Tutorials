---
date: 2026-02-17
description: Apprenez comment convertir dwg en png et exporter cad en png ou d’autres
  formats raster en utilisant Aspose.CAD pour Java. Obtenez des résultats de haute
  qualité rapidement.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Convertir DWG en PNG et autres formats raster avec Aspose.CAD pour Java
url: /fr/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

 produce French translation.

We'll translate each paragraph.

Be careful with bullet points, tables: translate content inside cells.

Also keep code block placeholders unchanged.

Let's start.

We'll output the whole content with same structure.

Proceed.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWG en PNG et autres formats raster avec Aspose.CAD pour Java

## Introduction

Convertir DWG en PNG (ou d’autres formats d’image raster) est une exigence courante lorsque vous devez partager des dessins CAO avec des collègues qui n’ont pas de visionneur CAO, intégrer des conceptions dans de la documentation, ou générer des vignettes pour des galeries web. **Dans ce guide, vous apprendrez à convertir dwg en png rapidement et de manière fiable**, que vous travailliez avec un fichier de dessin complet ou simplement avec une mise en page spécifique. Vous pouvez également avoir besoin de **convertir CAD en raster** pour des aperçus web, des outils de reporting ou des applications mobiles. Aspose.CAD pour Java rend cette conversion simple et vous offre un contrôle total sur la résolution, la sélection de la mise en page et le format de sortie.

## Réponses rapides
- **Quelle bibliothèque gère DWG vers PNG ?** Aspose.CAD pour Java  
- **Quels formats peuvent être exportés ?** PNG, JPEG, TIFF, PDF, BMP, et plus encore  
- **Ai‑je besoin d’une licence pour les tests ?** Un essai gratuit suffit pour le développement ; une licence est requise en production  
- **Puis‑je choisir une mise en page spécifique ?** Oui, utilisez `setLayouts` pour cibler “Model”, “Layout1”, etc.  
- **Une sortie haute résolution est‑elle possible ?** Absolument—ajustez `setPageWidth` et `setPageHeight` pour contrôler le DPI  

## Qu’est‑ce que “convert dwg to png” ?

L’expression “convert dwg to png” décrit le processus consistant à prendre un fichier DWG basé sur des vecteurs (le format natif de nombreuses applications CAO) et à le rasteriser en une image PNG basée sur des pixels. Les images raster sont idéales pour l’affichage web, le partage par e‑mail et l’intégration dans des logiciels non‑CAO.

## Pourquoi exporter CAD en PNG (ou autres formats raster) ?

- **Compatibilité universelle :** PNG et JPEG sont pris en charge par pratiquement tous les visionneurs d’image et navigateurs.  
- **Chargement rapide :** Les images raster se chargent instantanément comparées à l’ouverture d’un fichier DWG lourd.  
- **Intégration facile :** Insérez des PNG directement dans Word, PowerPoint ou HTML sans plugins supplémentaires.  
- **Aspect cohérent :** Vous contrôlez la résolution, l’arrière‑plan et la mise en page, garantissant que chaque partie prenante voit le même rendu.  

## Cas d’utilisation courants

| Scénario | Pourquoi la sortie raster aide |
|----------|--------------------------------|
| **Documentation de projet** | Intégrer des PNG dans des PDF ou des documents Word évite d’exiger un logiciel CAO pour les relecteurs. |
| **Portails web** | Les vignettes générées à partir de fichiers DWG se chargent instantanément et améliorent l’expérience utilisateur. |
| **Applications mobiles** | Les images raster s’affichent correctement sur des appareils qui ne disposent pas de visionneurs CAO. |
| **Reporting automatisé** | Convertir en lot plusieurs mises en page en PNG/JPEG pour les inclure dans des graphiques ou tableaux de bord. |

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

> **Astuce :** Si vous prévoyez d’**exporter CAD en PNG** au lieu de TIFF, remplacez `TiffOptions` par `PngOptions` (disponible dans `com.aspose.cad.imageoptions.PngOptions`).

## Guide étape par étape

### Étape 1 : Configurer le répertoire des ressources

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Remplacez `"Your Document Directory"` par le chemin absolu où résident vos fichiers CAD.

### Étape 2 : Charger le fichier CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Vous pouvez charger n’importe quel format pris en charge (DWG, DXF, DGN, etc.). C’est la **partie comment convertir cad** — il suffit de pointer vers le fichier et de laisser Aspose gérer l’analyse.

### Étape 3 : Configurer les options de rasterisation

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` contrôlent la résolution de sortie (des valeurs plus grandes = DPI plus élevé).  
- `setLayouts` vous permet de **convertir CAD en raster** pour des mises en page spécifiques ; omettez‑le pour rasteriser le dessin complet.

### Étape 4 : Définir les options d’image

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Si vous préférez PNG, instanciez `PngOptions` au lieu de `TiffOptions`. C’est ici que vous **exportez CAD en PNG**.

### Étape 5 : Enregistrer l’image résultante

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Modifiez l’extension du fichier en `.png` (et l’objet d’options en `PngOptions`) pour **enregistrer CAD en JPEG/PNG**.

> **Erreur fréquente :** Oublier d’associer l’extension du fichier à la classe d’options provoque une `UnsupportedFormatException`. Gardez toujours les deux en synchronisation.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Image de sortie vide** | Vérifiez que les noms de mise en page dans `setLayouts` correspondent exactement à ceux du fichier CAD source. |
| **PNG à basse résolution** | Augmentez `setPageWidth` / `setPageHeight` ou définissez `setResolution` sur les options de rasterisation. |
| **Version DWG non prise en charge** | Assurez‑vous d’utiliser la dernière version d’Aspose.CAD ; les versions plus anciennes peuvent ne pas supporter les nouvelles versions DWG. |
| **Erreurs de mémoire sur fichiers volumineux** | Traitez les pages une à une ou augmentez le tas JVM (`-Xmx2g`). |

## Questions fréquentes

**Q : Aspose.CAD est‑il compatible avec différents formats de fichiers CAD ?**  
R : Oui, il prend en charge DWG, DXF, DGN et bien d’autres.

**Q : Puis‑je personnaliser la résolution de l’image raster de sortie ?**  
R : Absolument. Ajustez `setPageWidth`, `setPageHeight` ou `setResolution` dans `CadRasterizationOptions`.

**Q : Comment convertir plusieurs mises en page CAD en une seule exécution ?**  
R : Fournissez un tableau contenant tous les noms de mise en page à `setLayouts`, par ex. `new String[]{"Model","Layout1","Layout2"}`.

**Q : Existe‑t‑il d’autres formats de sortie que le TIFF ?**  
R : Oui—PNG, JPEG, BMP, PDF, et d’autres sont disponibles via leurs classes `*Options` respectives.

**Q : Où puis‑je obtenir de l’aide ou partager mon expérience avec Aspose.CAD ?**  
R : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire et l’assistance officielle.

## Conclusion

En suivant ces étapes, vous pouvez **convertir DWG en PNG**, **exporter CAD en PNG**, **enregistrer CAD en JPEG**, ou générer tout autre format raster dont vous avez besoin. Aspose.CAD pour Java effectue le travail lourd, vous permettant de vous concentrer sur l’intégration d’images de haute qualité dans vos applications, documentation ou portails web.

---

**Dernière mise à jour :** 2026-02-17  
**Testé avec :** Aspose.CAD pour Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}