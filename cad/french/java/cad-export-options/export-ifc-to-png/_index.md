---
date: 2026-10-19
description: Apprenez à créer des fichiers PNG vignette d'IFC avec Aspose.CAD for
  Java en quelques lignes de code seulement.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: Exporter IFC en PNG
og_description: Créez des fichiers PNG vignette d'IFC sans effort avec Aspose.CAD
  for Java. Ce guide étape par étape vous montre comment charger, rasteriser et enregistrer
  des modèles IFC en images PNG de haute qualité.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Créer une vignette PNG d'IFC avec Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Comment créer une vignette PNG d'IFC avec Aspose.CAD for Java
url: /fr/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter IFC en PNG avec Aspose.CAD pour Java

## Introduction

Dans ce tutoriel, vous apprendrez comment **créer des vignettes PNG IFC** avec Aspose.CAD pour Java. Que vous ayez besoin d'aperçus rapides pour un portail BIM, de générer des vignettes pour un système de gestion de documents, ou d'automatiser des conversions par lots, les étapes ci‑dessous vous permettent de rasteriser un modèle IFC 3‑D en une image PNG 2‑D nette en quelques lignes de code Java.

## Réponses rapides
- **Quelle bibliothèque est requise ?** Aspose.CAD for Java.  
- **Puis-je créer une vignette PNG IFC en quelques lignes de code ?** Oui – le flux complet tient en moins de 20 lignes.  
- **Ai-je besoin d'une licence pour la production ?** Une licence temporaire fonctionne pour les tests ; une licence complète est requise pour le déploiement commercial.  
- **Le rendu est‑il évolutif ?** Vous pouvez définir n'importe quelles dimensions en pixels, ainsi le PNG s'adapte à la taille souhaitée.  
- **Quelle version de Java est prise en charge ?** Java 8 ou supérieure.

## Qu’est‑ce que « convertir IFC en PNG » ?
Convertir IFC (Industry Foundation Classes) en PNG signifie rasteriser le modèle de bâtiment 3‑D en une image bitmap 2‑D. Ce processus crée une vignette visuelle pouvant être affichée dans les navigateurs, les rapports ou les applications mobiles sans nécessiter de visionneuse CAD complète.

## Pourquoi utiliser Aspose.CAD pour Java ?
Aspose.CAD prend en charge **plus de 30 formats CAD et BIM**, dont IFC, DWG, DXF et DGN, et peut traiter des fichiers jusqu'à **2 Go** sans charger le document complet en mémoire. La bibliothèque est pure Java, ne possède **aucune dépendance externe**, et fonctionne sous Windows, Linux et macOS, ce qui la rend idéale pour la génération d'images côté serveur.  
Elle offre une rasterisation haute performance, une prise en charge étendue des formats et une intégration facile dans les applications Java.

## Prérequis
- **Bibliothèque Aspose.CAD** – téléchargez le dernier JAR depuis le [lien de téléchargement](https://releases.aspose.com/cad/java/).  
- **Kit de développement Java** – JDK 8 ou plus récent installé sur votre machine.  
- **Fichier source IFC** – placez le fichier dans un dossier que vous pouvez référencer depuis votre code.

## Importer les espaces de noms
Le package `com.aspose.cad` fournit toutes les classes dont vous avez besoin. `CadImage` est le point d'entrée pour charger les fichiers CAD, tandis que `PngOptions` configure les paramètres de rasterisation.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Comment créer une vignette PNG IFC en Java ?
Chargez le fichier IFC, définissez les options de rasterisation, et enregistrez le résultat en tant qu'image PNG – c’est le flux complet de conversion. Les sections suivantes détaillent chaque étape, afin que vous puissiez copier‑coller les extraits dans votre projet et les exécuter immédiatement.

### Étape 1 : charger le fichier IFC
Tout d'abord, indiquez le dossier où se trouve votre fichier IFC et chargez‑le avec `CadImage.load`.  
`CadImage.load` lit un fichier CAD et renvoie un objet image qui peut être rasterisé.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Pourquoi c’est important :** Charger le fichier en tant que `CadImage` vous donne accès aux options de conversion vecteur‑raster qui contrôlent la résolution, la couleur d'arrière‑plan et l'épaisseur des lignes.

### Étape 2 : définir les options de rasterisation
Définissez les dimensions de sortie et tout autre paramètre lié aux vecteurs via `VectorRasterizationOptions`.  
`VectorRasterizationOptions` vous permet de spécifier la taille de sortie, la couleur d'arrière‑plan et d'autres paramètres de rasterisation.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> Ajustez `PageWidth` et `PageHeight` pour contrôler la résolution finale du PNG, ce qui est essentiel lorsque vous **enregistrez des fichiers PNG java** pour des impressions haute qualité ou des vignettes web.

### Étape 3 : configurer les options PNG
Liez les options de rasterisation à l'exportateur PNG en créant une instance de `PngOptions`.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Étape 4 : enregistrer l'image en PNG
Enfin, écrivez l'image rasterisée sur le disque en utilisant la méthode `save`.  
`save` écrit l'image rasterisée vers le chemin de fichier spécifié dans le format choisi.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Après cette étape, vous avez créé avec succès une **vignette PNG IFC** et pouvez utiliser le `example.png` résultant partout où vous avez besoin d'une image raster.

## Cas d’utilisation courants
- **Générer des vignettes** pour les modèles BIM dans les portails web.  
- **Intégrer des instantanés de plans d'étage** dans les rapports PDF ou Word.  
- **Conversion par lots automatisée** de grandes bibliothèques IFC pour des projets d'archivage ou de migration.

## Dépannage & astuces
- **Problèmes de mémoire :** Pour les fichiers IFC très volumineux, augmentez le tas JVM (`-Xmx2g` ou plus).  
- **Textures manquantes :** Assurez‑vous que les ressources externes du fichier IFC sont accessibles depuis le `dataDir`.  
- **Astuce pro :** Utilisez `vectorOptions.setBackgroundColor(Color.getWhite())` si vous préférez un arrière‑plan blanc au lieu du PNG transparent par défaut.

## FAQ

### Q1 : Aspose.CAD est‑il compatible avec toutes les versions de fichiers IFC ?
R1 : Aspose.CAD prend en charge diverses versions d'IFC. Consultez la [documentation](https://reference.aspose.com/cad/java/) pour des informations détaillées sur la compatibilité.

### Q2 : Puis‑je personnaliser davantage les options de rasterisation ?
R2 : Absolument ! Explorez la [documentation](https://reference.aspose.com/cad/java/) pour des paramètres avancés tels que le contrôle du DPI, l'anti‑aliasing et l'épaisseur des lignes.

### Q3 : Une version d'essai est‑elle disponible ?
R3 : Oui, vous pouvez télécharger la version d'essai gratuite depuis le [Essai gratuit Aspose.CAD](https://releases.aspose.com/).

### Q4 : Comment obtenir une licence temporaire pour les tests ?
R4 : Obtenez une licence temporaire depuis la [page de licence temporaire Aspose.CAD](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis‑je poser des questions ou signaler des problèmes ?
R5 : Rejoignez la communauté sur le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour obtenir de l'aide des ingénieurs Aspose et d'autres développeurs.

## Questions fréquemment posées

**Q : Puis‑je utiliser cette approche pour convertir d’autres formats CAD en PNG ?**  
R : Oui, Aspose.CAD prend en charge de nombreux formats (DWG, DXF, DGN, etc.). Il suffit de changer l'extension du fichier et de charger la classe d'image appropriée.

**Q : La bibliothèque me permet‑elle de définir un DPI personnalisé ?**  
R : Le DPI est contrôlé indirectement via `PageWidth`/`PageHeight`. Ajustez ces valeurs en fonction de la taille physique souhaitée pour obtenir le DPI requis.

**Q : La sortie PNG est‑elle sans perte ?**  
R : PNG est un format sans perte, donc l'image rasterisée conserve toute la fidélité visuelle des données vectorielles d'origine.

## Conclusion
Vous disposez maintenant d’une méthode complète et prête pour la production afin de **créer des fichiers PNG thumbnail IFC** en utilisant Aspose.CAD pour Java. Intégrez ces étapes dans des outils de bureau, des services côté serveur ou des fonctions cloud pour automatiser les pipelines de visualisation BIM et fournir des vignettes rapides et de haute qualité aux utilisateurs finaux.

---

**Dernière mise à jour :** 2026-10-19  
**Testé avec :** Aspose.CAD for Java 24.11  
**Auteur :** Aspose

## Tutoriels associés

- [Comment convertir STL en PNG avec Aspose.CAD pour Java](/cad/java/cad-export-options/export-stl-to-png/)
- [Convertir DWG en PNG – Enregistrer CAD en PNG avec Aspose.CAD pour Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [Exporter DWG en PDF en Java – Définir la taille de page PDF avec Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}