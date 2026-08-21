---
date: 2026-04-13
description: Apprenez à rasteriser une couche CAD en Java à l'aide d'Aspose.CAD pour
  Java. Ce guide étape par étape montre la conversion au niveau de la couche en images
  raster.
keywords:
- java rasterize cad layer
- Aspose CAD Java
- convert CAD layer to raster
linktitle: Convertir la couche CAD en format d'image raster
second_title: Aspose.CAD Java API
title: Java rasteriser la couche CAD – Tutoriel Aspose CAD
url: /fr/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tutoriel Aspose CAD Java : Convertir une couche CAD en format d'image raster

## Introduction

Si vous devez **java rasterize cad layer** des fichiers pour faciliter le partage, l'impression ou le traitement d'images en aval, vous êtes au bon endroit. Dans ce tutoriel, nous expliquerons comment Aspose.CAD pour Java vous permet de sélectionner des couches individuelles d'un dessin CAD et de les exporter en images raster de haute qualité telles que JPEG, PNG ou BMP. À la fin, vous comprendrez pourquoi la rasterisation sélective est importante, comment configurer les options de rasterisation et comment enregistrer le résultat en quelques lignes de code.

## Réponses rapides
- **Quel est le sujet de ce tutoriel ?** Conversion des couches CAD sélectionnées en images raster à l'aide d'Aspose.CAD pour Java.  
- **Quels formats sont pris en charge ?** Tout format raster supporté par Aspose (JPEG, PNG, BMP, etc.).  
- **Ai-je besoin d'une licence ?** Un essai gratuit fonctionne pour le développement ; une licence est requise pour la production.  
- **Quelles sont les conditions préalables ?** Environnement de développement Java et la bibliothèque Aspose.CAD Java.  
- **Combien de temps prend la mise en œuvre ?** Environ 10 à 15 minutes pour une conversion de base.

## Qu'est-ce que « java rasterize cad layer » ?

Rasteriser une couche CAD signifie convertir les données vectorielles de cette couche spécifique en une image basée sur des pixels. Ce processus préserve l'apparence visuelle de la couche tout en la rendant compatible avec tout système pouvant afficher des formats d'image standard.

## Pourquoi utiliser cette approche ?

- **Export sélectif** – Seules les couches dont vous avez besoin sont rendues, ce qui réduit la taille du fichier et le temps de traitement.  
- **Flexibilité de format** – Changez `JpegOptions` en `PngOptions`, `BmpOptions`, etc., sans modifier la logique principale.  
- **Rendu haute qualité** – Aspose.CAD préserve les épaisseurs de ligne, les couleurs et le texte exactement comme dans le fichier CAD original.  

## Prérequis

Avant de plonger dans le code, assurez‑vous de disposer de ce qui suit :

- **Environnement de développement Java** – JDK 8 ou supérieur installé et configuré.  
- **Bibliothèque Aspose.CAD** – Téléchargez et installez la bibliothèque Aspose.CAD pour Java depuis le [lien de téléchargement](https://releases.aspose.com/cad/java/).  

## Importer les espaces de noms

Dans cette étape, nous importerons les classes nécessaires pour commencer à travailler avec les fichiers CAD.

### Importer les classes Aspose.CAD

Dans votre fichier source Java, incluez les importations Aspose.CAD requises :

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Convertir une couche CAD en format d'image raster

Ci-dessous se trouve le processus complet, étape par étape. Chaque étape est expliquée en termes simples avant le bloc de code, afin que vous sachiez exactement ce qui se passe.

### Étape 1 : Configurer le fichier CAD

Tout d'abord, indiquez le chemin de votre fichier CAD et chargez‑le dans un objet `Image` :

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Étape 2 : Configurer les options de rasterisation

Créez une instance de `CadRasterizationOptions` pour définir la taille et la qualité de l'image de sortie :

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### Étape 3 : Spécifier les couches CAD

Ajoutez les noms des couches que vous souhaitez rasteriser. Dans cet exemple, nous exportons la couche par défaut `"0"` :

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### Étape 4 : Configurer les options JPEG

Créez un objet `JpegOptions` (ou toute autre option d'image raster) et liez‑le aux paramètres de rasterisation :

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### Étape 5 : Exporter en JPEG

Enfin, enregistrez la couche rasterisée sous forme de fichier JPEG :

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

Répétez les étapes ci‑dessus pour des couches supplémentaires ou ajustez les paramètres de rasterisation (résolution, couleur d'arrière‑plan, etc.) pour répondre à vos exigences spécifiques.

## Problèmes courants et dépannage

| Symptôme | Cause probable | Solution |
|----------|----------------|----------|
| Image vide en sortie | Aucune couche spécifiée ou nom de couche incorrect | Vérifiez que les noms de couches existent dans le fichier CAD ; utilisez `image.getLayers()` pour les lister. |
| Résolution basse | Le DPI par défaut est faible | Définissez `rasterizationOptions.setResolution(300);` (ou une valeur supérieure) avant d'enregistrer. |
| Format CAD non pris en charge | Utilisation d'une version ancienne d'Aspose.CAD | Mettez à jour vers la dernière version d'Aspose.CAD pour Java. |

## Questions fréquentes

**Q : Puis-je utiliser Aspose.CAD pour Java avec d'autres langages de programmation ?**  
R : Aspose.CAD prend principalement en charge Java, mais des versions .NET, C++ et d'autres langages sont disponibles.

**Q : Où puis‑je trouver un support ou une assistance supplémentaire ?**  
R : Pour toute question ou assistance, visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

**Q : Existe‑t‑il un essai gratuit disponible ?**  
R : Oui, vous pouvez explorer Aspose.CAD en obtenant un essai gratuit [ici](https://releases.aspose.com/).

**Q : Comment obtenir une licence temporaire pour Aspose.CAD ?**  
R : Obtenez une licence temporaire via [ce lien](https://purchase.aspose.com/temporary-license/).

**Q : Y a‑t‑il des exigences système spécifiques pour Aspose.CAD pour Java ?**  
R : Assurez‑vous de disposer d'un environnement de développement Java compatible ; consultez la documentation pour les exigences détaillées.

---

**Dernière mise à jour :** 2026-04-13  
**Testé avec :** Aspose.CAD for Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}