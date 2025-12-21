---
date: 2025-12-21
description: Convertissez IFC en PNG sans effort avec Aspose.CAD pour Java. Suivez
  notre tutoriel étape par étape.
linktitle: Export IFC to PNG
second_title: Aspose.CAD Java API
title: Convertir IFC en PNG avec Aspose.CAD pour Java
url: /fr/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir IFC en PNG avec Aspose.CAD pour Java

## Introduction

Dans ce tutoriel, vous apprendrez **comment convertir IFC en PNG** en utilisant la puissante bibliothèque Aspose.CAD pour Java. Que vous construisiez un visualiseur BIM, génériez des miniatures pour un portail de construction, ou automatisiez des pipelines de documentation, convertir des fichiers IFC (Industry Foundation Classes) en images raster est une exigence courante. Nous parcourrons chaque étape, expliquerons le raisonnement derrière les paramètres et vous donnerons des astuces pour obtenir les meilleurs résultats visuels.

## Réponses rapides
- **Quelle bibliothèque est nécessaire ?** Aspose.CAD pour Java (essai gratuit disponible).  
- **Versions IFC prises en charge ?** La plupart des fichiers IFC 2x3 et IFC4 sont gérés.  
- **Temps de conversion typique ?** Quelques secondes pour des modèles standards ; dépend de la taille du fichier.  
- **Ai‑je besoin d’une licence ?** Une licence temporaire est requise pour une utilisation en production.  
- **Puis‑je personnaliser la taille de l’image ?** Oui – utilisez `CadRasterizationOptions` pour définir la largeur et la hauteur.

## Qu’est‑ce que « convertir IFC en PNG » ?
Convertir IFC en PNG signifie rasteriser un modèle 3‑D de bâtiment (IFC) en une image bitmap 2‑D (PNG). Ce processus aplatit la géométrie, applique des styles visuels par défaut et produit une image portable qui peut être affichée dans les navigateurs, les rapports ou les applications mobiles sans nécessiter de visualiseur CAD.

## Pourquoi utiliser Aspose.CAD pour Java ?
- **Pas de logiciel CAD externe** – API Java pure, fonctionne sur n’importe quelle plateforme.  
- **Rendu haute fidélité** – préserve les épaisseurs de ligne, les couleurs et les calques.  
- **Contrôle total** – les options de rasterisation vous permettent de définir la résolution, l’arrière‑plan, etc.  
- **Licence facile** – les licences d’essai et temporaires simplifient l’évaluation.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Bibliothèque Aspose.CAD** – téléchargez‑la et installez‑la depuis le [lien de téléchargement](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK)** – version 8 ou supérieure.  
- **Un dossier** contenant le fichier IFC que vous souhaitez convertir.

## Importer les espaces de noms

Dans votre projet Java, importez les classes nécessaires :

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Guide étape par étape

### Étape 1 : Charger le fichier IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Ici nous chargeons le fichier IFC source dans un objet `IfcImage`. Aspose.CAD analyse automatiquement la structure IFC et la prépare pour la rasterisation.

### Étape 2 : Définir les options vectorielles (rasterisation)

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

`CadRasterizationOptions` contrôle la façon dont la géométrie 3‑D est aplatie. Ajustez `PageWidth` et `PageHeight` pour correspondre à la résolution PNG souhaitée. Des valeurs plus élevées donnent des images plus détaillées mais augmentent l’utilisation de mémoire.

### Étape 3 : Configurer les paramètres d’exportation PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

`PngOptions` indique à Aspose.CAD de produire un fichier PNG et lie les paramètres de rasterisation définis à l’étape précédente.

### Étape 4 : Enregistrer l’image au format PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

La méthode `save` écrit l’image rasterisée sur le disque. Après l’exécution de cette ligne, vous trouverez `example.png` dans le même répertoire que votre fichier IFC source.

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **PNG blanc** | Les options de rasterisation ont une largeur/hauteur à 0 ou très petite. | Assurez‑vous que `PageWidth` et `PageHeight` sont des entiers positifs (par ex., 1500). |
| **Calques ou couleurs manquants** | La vue par défaut peut masquer certains calques. | Utilisez `vectorOptions.setRenderMode(CadRenderMode.Wireframe)` ou ajustez la visibilité des calques via l’API (si nécessaire). |
| **Erreurs de mémoire insuffisante** pour des fichiers IFC volumineux | Une résolution très élevée consomme beaucoup de RAM. | Réduisez la résolution ou traitez le modèle par sections. |

## FAQ

### Q1 : Aspose.CAD est‑il compatible avec toutes les versions de fichiers IFC ?

R1 : Aspose.CAD prend en charge diverses versions de fichiers IFC. Consultez la [documentation](https://reference.aspose.com/cad/java/) pour les détails de compatibilité.

### Q2 : Puis‑je personnaliser davantage les options de rasterisation ?

R2 : Absolument ! Explorez la [documentation](https://reference.aspose.com/cad/java/) pour les options de personnalisation avancées.

### Q3 : Existe‑t‑il une version d’essai disponible ?

R3 : Oui, vous pouvez accéder à la version d’essai gratuite [ici](https://releases.aspose.com/).

### Q4 : Comment obtenir une licence temporaire pour Aspose.CAD ?

R4 : Obtenez une licence temporaire via [ce lien](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis‑je demander de l’aide ou discuter des problèmes ?

R5 : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire.

## Questions fréquentes (supplémentaires)

**Q : Puis‑je convertir plusieurs fichiers IFC en lot ?**  
R : Oui. Enveloppez la logique de chargement et d’enregistrement dans une boucle qui parcourt une liste de chemins de fichiers.

**Q : Comment changer la couleur d’arrière‑plan du PNG ?**  
R : Définissez `vectorOptions.setBackgroundColor(Color.getWhite())` (ou toute `java.awt.Color`) avant de créer `PngOptions`.

**Q : Est‑il possible d’exporter vers d’autres formats raster comme JPEG ou BMP ?**  
R : Absolument. Remplacez `PngOptions` par `JpegOptions` ou `BmpOptions` et ajustez les paramètres spécifiques au format.

**Q : Dois‑je libérer les ressources après la conversion ?**  
R : Appelez `cadImage.dispose()` une fois terminé pour libérer la mémoire native.

---

**Dernière mise à jour :** 2025-12-21  
**Testé avec :** Aspose.CAD pour Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}