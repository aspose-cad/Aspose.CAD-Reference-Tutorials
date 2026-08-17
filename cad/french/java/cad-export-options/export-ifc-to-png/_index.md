---
date: 2026-02-20
description: Convertissez facilement les fichiers IFC en PNG avec Aspose.CAD pour
  Java. Suivez notre tutoriel étape par étape.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Comment convertir un IFC en PNG avec Aspose.CAD pour Java
url: /fr/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter IFC en PNG avec Aspose.CAD pour Java

## Introduction

Bienvenue dans ce tutoriel étape par étape sur **comment convertir IFC en PNG** en utilisant Aspose.CAD pour Java. Que vous construisiez un pipeline BIM‑vers‑image ou que vous ayez besoin d’aperçus visuels rapides des modèles IFC, ce guide vous accompagne dans chaque détail afin que vous puissiez **convertir IFC en PNG** de manière fiable dans vos applications Java.

## Réponses rapides
- **Quelle bibliothèque est requise ?** Aspose.CAD for Java  
- **Puis-je convertir IFC en PNG en quelques lignes de code ?** Oui – le processus principal tient en moins de 20 lignes.  
- **Ai-je besoin d’une licence pour la production ?** Une licence temporaire fonctionne pour les tests ; une licence complète est requise pour une utilisation commerciale.  
- **La sortie est‑elle évolutive ?** Les options de rasterisation vous permettent de définir toutes les dimensions de pixels dont vous avez besoin.  
- **Quelle version de Java est prise en charge ?** Java 8 ou supérieur.

## Qu’est‑ce que « convertir IFC en PNG » ?
Convertir IFC (Industry Foundation Classes) en PNG signifie rasteriser les données du modèle de bâtiment 3 D en une image bitmap 2 D. Cela est utile pour générer des vignettes, intégrer des modèles dans des rapports ou créer des visualisations prêtes pour le web sans nécessiter de visionneuse CAD complète.

## Pourquoi utiliser Aspose.CAD pour Java ?
- **Full‑featured** prise en charge de nombreux formats CAD, y compris IFC.  
- **No external dependencies** – pure Java, facile à intégrer.  
- **Fine‑grained control** sur la rasterisation (résolution, arrière‑plan, épaisseur des lignes).  
- **Cross‑platform** – fonctionne sous Windows, Linux et macOS.

## Prérequis

Avant de commencer, assurez‑vous d’avoir les éléments suivants :
- **Aspose.CAD Library** – téléchargez et installez la bibliothèque Aspose.CAD pour Java depuis le [download link](https://releases.aspose.com/cad/java/).  
- **Document Directory** – un dossier sur votre système contenant le fichier IFC que vous souhaitez convertir.

## Importer les espaces de noms

Dans votre projet Java, importez les classes nécessaires :

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Guide étape par étape

### Étape 1 : Charger le fichier IFC
Tout d’abord, indiquez le dossier où se trouve votre fichier IFC et chargez‑le.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Pourquoi c’est important :** Charger le fichier en tant qu'`IfcImage` vous donne accès aux options de rasterisation spécifiques à Cad ultérieurement.

### Étape 2 : Définir les options vectorielles (Rasterisation)
Définissez les dimensions de sortie et tout autre paramètre lié au vecteur.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> Vous pouvez ajuster `PageWidth` et `PageHeight` pour contrôler la résolution finale du PNG, ce qui est essentiel lorsque vous **save PNG java** files for high‑quality prints.

### Étape 3 : Configurer les options PNG
Liez les options de rasterisation à l'exportateur PNG.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Étape 4 : Enregistrer l’image en PNG
Enfin, écrivez l’image rasterisée sur le disque.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Après cette étape, vous avez réussi à **convertir IFC en PNG** et pouvez utiliser le fichier `example.png` résultant partout où vous avez besoin d’une image raster.

## Cas d’utilisation courants
- **Generating thumbnails** pour les modèles BIM dans les portails web.  
- **Embedding floor‑plan snapshots** dans les rapports PDF.  
- **Automated batch conversion** de grandes bibliothèques IFC pour l'archivage.

## Dépannage & astuces
- **Memory issues** : lors de la conversion de fichiers IFC très volumineux, augmentez le tas JVM (`-Xmx2g` ou plus).  
- **Missing textures** : assurez‑vous que le fichier IFC référence des ressources externes accessibles depuis `dataDir`.  
- **Pro tip** : utilisez `vectorOptions.setBackgroundColor(Color.getWhite())` si vous avez besoin d’un arrière‑plan blanc au lieu du PNG transparent par défaut.

## FAQ

### Q1 : Aspose.CAD compatible avec toutes les versions de fichiers IFC ?
A1 : Aspose.CAD prend en charge diverses versions de fichiers IFC. Consultez la [documentation](https://reference.aspose.com/cad/java/) pour les détails de compatibilité.

### Q2 : Puis‑je personnaliser davantage les options de rasterisation ?
A2 : Absolument ! Explorez la [documentation](https://reference.aspose.com/cad/java/) pour les options de personnalisation avancées.

### Q3 : Une version d’essai est‑elle disponible ?
A3 : Oui, vous pouvez accéder à la version d’essai gratuite [ici](https://releases.aspose.com/).

### Q4 : Comment obtenir une licence temporaire pour Aspose.CAD ?
A4 : Obtenez une licence temporaire via [ce lien](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis‑je obtenir de l’aide ou discuter des problèmes ?
A5 : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire.

## Questions fréquemment posées

**Q : Puis‑je utiliser cette approche pour convertir d’autres formats CAD en PNG ?**  
A : Oui, Aspose.CAD prend en charge de nombreux formats (DWG, DXF, DGN, etc.). Il suffit de changer l’extension du fichier et de le caster dans la classe d’image appropriée.

**Q : La bibliothèque me permet‑elle de définir un DPI personnalisé ?**  
A : Vous pouvez contrôler le DPI indirectement en ajustant `PageWidth`/`PageHeight` par rapport à la taille physique souhaitée.

**Q : La sortie PNG est‑elle sans perte ?**  
A : PNG est un format sans perte, ainsi l’image rasterisée conserve toute la fidélité visuelle des données vectorielles.

## Conclusion

Vous avez maintenant appris comment **convertir IFC en PNG** efficacement avec Aspose.CAD pour Java. En suivant ces étapes, vous pouvez intégrer la conversion IFC‑vers‑PNG dans n’importe quel flux de travail basé sur Java, qu’il s’agisse d’un outil de bureau, d’un service côté serveur ou d’une fonction cloud.

---

**Dernière mise à jour :** 2026-02-20  
**Testé avec :** Aspose.CAD for Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}