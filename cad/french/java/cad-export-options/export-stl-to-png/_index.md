---
date: 2025-12-21
description: Apprenez à exporter STL en PNG avec Aspose.CAD pour Java – un guide étape
  par étape qui simplifie la conversion des fichiers STL en PNG dans vos projets Java.
linktitle: Export STL to PNG
second_title: Aspose.CAD Java API
title: Exporter STL en PNG avec Aspose.CAD pour Java
url: /fr/java/cad-export-options/export-stl-to-png/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export STL en PNG avec Aspose.CAD pour Java

## Introduction

Si vous devez **export stl to png** rapidement et de manière fiable dans un environnement Java, Aspose.CAD pour Java est l’outil idéal. Dans ce tutoriel, nous passerons en revue tout ce dont vous avez besoin — de la configuration du projet à l’enregistrement d’une image PNG de haute qualité—afin que vous puissiez intégrer des actifs visuels 3 D dans vos applications en toute confiance.

## Réponses rapides
- **Que signifie « export stl to png » ?** Cela convertit un modèle STL 3 D en une image PNG raster 2 D.  
- **Quelle bibliothèque gère la conversion ?** Aspose.CAD pour Java fournit une prise en charge native des formats STL et PNG.  
- **Ai‑je besoin d’une licence ?** Une licence temporaire ou permanente Aspose.CAD est requise pour une utilisation en production.  
- **Combien de temps prend l’implémentation ?** Environ 10‑15 minutes pour un script de conversion basique.  
- **Puis‑je ajuster la taille de l’image ?** Oui – les options de rasterisation vous permettent de définir une largeur et une hauteur personnalisées.

## Qu’est‑ce que l’export stl to png ?

Exporter STL en PNG consiste à prendre un maillage 3 D (STL) et à le rendre sous forme d’image plane (PNG). Cela est utile lorsque vous souhaitez afficher des aperçus, générer des vignettes ou intégrer des modèles dans des rapports sans nécessiter de visionneuse 3 D.

## Pourquoi convertir STL en PNG en Java ?

- **Compatibilité multiplateforme** – PNG fonctionne sur les navigateurs, les applications mobiles et les interfaces graphiques de bureau.  
- **Performance** – Le rendu d’une image statique est beaucoup plus rapide que le chargement d’un modèle 3 D complet.  
- **Simplicité** – Aspose.CAD abstrait le processus complexe de rasterisation, vous permettant de vous concentrer sur la logique métier.  

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- Java Development Kit (JDK) installé sur votre machine.  
- Bibliothèque Aspose.CAD pour Java téléchargée. Vous pouvez l’obtenir [ici](https://releases.aspose.com/cad/java/).  
- Une licence valide ou une licence temporaire disponible [ici](https://purchase.aspose.com/temporary-license/).  

## Importer les espaces de noms

Ajoutez les classes Aspose.CAD requises à votre fichier source Java :

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Ces imports vous donnent accès au chargement d’image, à la rasterisation et aux options spécifiques PNG.

## Guide étape par étape

### Étape 1 : Configurer votre projet

Créez un nouveau projet Java (IDE de votre choix) et ajoutez le fichier JAR Aspose.CAD au classpath du projet.

### Étape 2 : Spécifier votre fichier STL (how to load stl)

Définissez le dossier contenant le modèle STL que vous souhaitez convertir :

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

> **Astuce :** Conservez vos fichiers STL dans un dossier de ressources dédié afin d’éviter les problèmes de chemin.

### Étape 3 : Charger le fichier STL (convert stl to png)

Utilisez la méthode `Image.load` pour lire le fichier STL dans un objet `CadImage` :

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

À ce stade, la géométrie 3 D est prête pour la rasterisation.

### Étape 4 : Configurer les options de rasterisation (convert 3d stl png)

Définissez les dimensions de sortie et les autres paramètres de raster. Ajustez la largeur/hauteur pour correspondre à la résolution PNG souhaitée :

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Vous pouvez également ajuster la couleur d’arrière‑plan, le poids des lignes ou l’anti‑aliasing ici.

### Étape 5 : Configurer les options PNG (java convert stl png)

Créez une instance `PngOptions` et (facultativement) associez‑lui les options de rasterisation :

```java
PngOptions pngOptions = new PngOptions();
// Uncomment the line below if you want to set vector rasterization options
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Laisser la ligne commentée utilise les paramètres de rasterisation par défaut, suffisants dans la plupart des cas.

### Étape 6 : Enregistrer en PNG

Enfin, écrivez l’image rendue sur le disque :

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

Vous disposez maintenant d’une représentation PNG de votre modèle STL original, prête à être utilisée dans des composants UI, des pages web ou de la documentation.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **Sortie PNG vide** | Options de rasterisation non définies ou taille zéro | Assurez‑vous que `setPageWidth` et `setPageHeight` ont des valeurs positives. |
| **OutOfMemoryError** | Fichiers STL très volumineux | Augmentez la taille du tas JVM (`-Xmx`) ou réduisez les dimensions de l’image. |
| **Licence introuvable** | Fichier de licence manquant ou incorrect | Placez le fichier de licence dans le classpath et chargez‑le avant tout appel Aspose. |

## Conclusion

Vous avez appris avec succès à **export stl to png** en utilisant Aspose.CAD pour Java. Ce flux de travail vous permet de générer des aperçus PNG de haute qualité à partir de n’importe quel modèle STL, simplifiant les tâches de visualisation dans les applications basées sur Java.

## FAQ

### Q1 : Aspose.CAD pour Java est‑il compatible avec toutes les versions de fichiers STL ?

R1 : Aspose.CAD pour Java prend en charge diverses versions de fichiers STL, assurant la compatibilité avec la plupart des formats courants.

### Q2 : Puis‑je utiliser Aspose.CAD pour Java dans un projet commercial ?

R2 : Oui. Il suffit d’obtenir une licence valide [ici](https://purchase.aspose.com/buy).

### Q3 : Ai‑je besoin d’une licence temporaire pour l’essai gratuit ?

R3 : Non, une licence temporaire n’est pas requise pour l’essai gratuit. Vous pouvez commencer immédiatement avec la version d’essai [ici](https://releases.aspose.com/).

### Q4 : Où puis‑je trouver un support supplémentaire ou poser des questions ?

R4 : Visitez le forum Aspose.CAD [ici](https://forum.aspose.com/c/cad/19) pour tout support ou toute requête.

### Q5 : Existe‑t‑il une documentation complète disponible ?

R5 : Oui, la documentation est disponible [ici](https://reference.aspose.com/cad/java/).

## Questions fréquemment posées

**Q : Comment contrôler la couleur d’arrière‑plan du PNG exporté ?**  
R : Utilisez `vectorOptions.setBackgroundColor(Color.getWhite())` avant d’assigner les options à `pngOptions`.

**Q : Puis‑je exporter plusieurs fichiers STL en traitement par lots ?**  
R : Absolument – placez la logique de conversion dans une boucle qui itère sur une liste de chemins de fichiers.

**Q : Le PNG conserve‑t‑il la transparence ?**  
R : Oui, le PNG supporte le canal alpha ; vous pouvez l’activer via `pngOptions.setTransparent(true)` si besoin.

**Q : Est‑il possible d’exporter vers d’autres formats raster (ex. : JPEG, BMP) ?**  
R : Aspose.CAD prend en charge de nombreux formats raster ; utilisez simplement `JpegOptions`, `BmpOptions`, etc., à la place de `PngOptions`.

**Q : Quelle version d’Aspose.CAD est requise pour la prise en charge du STL ?**  
R : La prise en charge du STL est disponible depuis Aspose.CAD 20.x ; l’utilisation de la dernière version garantit une compatibilité totale.

---

**Dernière mise à jour :** 2025-12-21  
**Testé avec :** Aspose.CAD pour Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}