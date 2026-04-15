---
date: 2026-01-07
description: Apprenez à exporter des fichiers CAD au format SVG avec Aspose.CAD pour
  Java. Ce guide étape par étape vous montre comment convertir des DWG en SVG, définir
  le mode couleur du SVG et intégrer la bibliothèque dans votre projet Java.
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: Exporter le CAD vers SVG à l'aide d'Aspose.CAD pour Java
url: /fr/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter la CAO vers SVG à l'aide d'Aspose.CAD pour Java

## Introduction

Bienvenue dans l'univers d'Aspose.CAD pour Java, une bibliothèque puissante qui permet aux développeurs de manipuler facilement les dessins CAD. Que vous soyez un développeur chevronné ou un novice dans le domaine du CAD, ce guide complet vous accompagnera pas à pas dans le **export CAD to SVG**, vous montrant comment convertir DWG en SVG, définir le mode couleur SVG et intégrer l'API dans votre projet Java.

## Réponses rapides

- **Que signifie « exporter CAD to SVG » ?** Il convertit un dessin CAD (par ex., DWG) en un fichier Scalable Vector Graphics qui peut être affiché dans les navigateurs.
- **Quelle bibliothèque gère la conversion ?** Aspose.CAD for Java fournit une API simple pour cette tâche.
- **Ai-je besoin d'une licence pour développer ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.
- **Puis-je contrôler la sortie couleur SVG ?** Oui, vous pouvez définir le mode couleur SVG (par ex., niveaux de gris).
- **Un logiciel supplémentaire est-il requis ?** Seul un runtime Java et le fichier JAR d'Aspose.CAD sont nécessaires.

## Prérequis

Avant de Sous-marin dans le tutoriel, assurez-vous de disposer des prérequis suivants :

- Environnement de développement Java : Vérifiez que Java est installé sur votre système.
- Bibliothèque Aspose.CAD : Téléchargez et installez la bibliothèque Aspose.CAD pour Java depuis le [lien de téléchargement](https://releases.aspose.com/cad/java/).
- Répertoire de documents : Créez un répertoire pour vos dessins CAD et notez son chemin.

## Importer des espaces de noms

Dans cette étape, nous allons importer les espaces de noms nécessaires pour démarrer notre aventure avec Aspose.CAD. Suivez ces étapes :

### Étape 1 : Ouvrez votre projet Java

Ouvrez votre projet Java dans l'IDE de votre choix.

### Étape 2 : Ajouter la bibliothèque Aspose.CAD

Ajoutez la bibliothèque Aspose.CAD à votre projet. Vous pouvez le faire en incluant le fichier JAR dans les dépendances de votre projet.

### Étape 3 : Importer les espaces de noms

Dans votre classe Java, importez les espaces de noms requis :

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## Exporter un fichier CAO au format SVG

Maintenant que le cadre est posé, plongeons dans le processus étape par étape du **export CAD to SVG** avec Aspose.CAD pour Java.

### Étape 1 : Spécifier le répertoire de ressources

Définissez le chemin vers votre répertoire de ressources, où se trouvent vos dessins CAD :

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Étape 2 : Charger le dessin CAO

Chargez le dessin CAD à l'aide de la bibliothèque Aspose.CAD :

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Étape 3 : Configurer les options d’exportation SVG

Configurez les options d'exportation SVG pour personnaliser la sortie. Ici, nous **set SVG color mode** en niveaux de gris et indiquons à l'exportateur de convertir le texte en formes :

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### Étape 4 : Enregistrer au format SVG

Enregistrez le dessin CAD au format SVG :

```java
image.save(dataDir + "meshes.svg");
```

> **Pro tip:** Si vous devez **convert DWG to SVG** tout en conservant les couleurs, remplacez `SvgColorMode.Grayscale` par `SvgColorMode.FullColor`.

Félicitations ! Vous avez exporté avec succès un dessin CAD en SVG en utilisant Aspose.CAD pour Java.

## Pourquoi utiliser Aspose.CAD pour exporter la CAO vers SVG ?

- **Haute fidélité :** Les données sont conservées, garantissant que le SVG ressemble exactement au dessin CAD original.
- **Pas de dépendances externes :** La conversion s'exécute entièrement dans Java, éliminant le besoin d'outils supplémentaires.
- **Sortie personnalisable :** Des options telles que `setColorType` vous permettent de choisir entre un SVG en niveaux de gris ou en couleur complète.

## Problèmes courants et solutions

- **File not found:** Vérifiez que `dataDir` pointe vers le bon dossier et que le nom du fichier DWG correspond.
- **Sortie SVG vierge :** Assurez-vous d'avoir défini `options.setTextAsShapes(true)` si le dessin contient du texte devant apparaître sous forme de formes.
- **Format CAO non pris en charge :** Aspose.CAD prend en charge les formats DWG, DXF, DWF et plusieurs autres; consultez la documentation pour la liste exacte.

## Conclusion

Dans ce tutoriel, nous avons exploré le processus fluide d’utilisation d’Aspose.CAD pour Java afin de **export CAD to SVG**. Grâce à son API intuitive et à ses fonctionnalités robustes, Aspose.CAD simplifie les tâches complexes, offrant aux développeurs un outil polyvalent pour la manipulation de CAO.

## Questions fréquemment posées

**Q : Puis-je convertir un fichier DXF en SVG en utilisant le même code ?**
R : Oui, il suffit de remplacer le nom du fichier par un fichier DXF ; l'API gère les deux formats.

**Q : Comment puis-je modifier la sortie en SVG couleur ?**
R : Définissez `options.setColorType(SvgColorMode.FullColor);` avant l'enregistrement.

**Q : Est-il possible d'intégrer des polices dans le SVG généré ?**
R : Aspose.CAD convertit actuellement le texte en formes ; l'intégration de politiques n'est pas requise.

**Q : La bibliothèque fonctionne-t-elle sous Linux et macOS ?**
R : La bibliothèque Java est indépendante de la plateforme et fonctionne partout où une JVM compatible est disponible.

**Q : Quelle version d'Aspose.CAD a été utilisée dans ce didacticiel ?**
R : L'exemple a été testé avec Aspose.CAD pour Java 24.10.

---

**Dernière mise à jour :** 2026-01-07
**Testé avec :** Aspose.CAD pour Java 24.10
**Auteur :** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
