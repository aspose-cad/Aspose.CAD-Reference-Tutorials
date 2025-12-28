---
date: 2025-12-28
description: Apprenez à charger des fichiers DWG dans des projets Java et à définir
  le nom de la police principale à l'aide d'Aspose.CAD pour Java. Guide étape par
  étape pour des visuels CAD parfaits.
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: Comment charger un fichier DWG en Java et substituer la police avec Aspose.CAD
url: /fr/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment charger un fichier DWG en Java et remplacer la police avec Aspose.CAD

## Introduction

Si vous devez **charger un fichier DWG en Java** dans vos applications et donner à vos dessins un aspect soigné, remplacer la police est une solution rapide. Avec Aspose.CAD pour Java, vous pouvez remplacer le style de texte par défaut par n'importe quelle police installée sur le système, garantissant que chaque annotation apparaît exactement comme vous l'attendez. Dans ce tutoriel, nous parcourrons l'ensemble du processus — du chargement d'un fichier DWG en Java à l'utilisation de la méthode `setPrimaryFontName` pour changer la police.

## Quick Answers
- **Quelle bibliothèque dois-je utiliser ?** Aspose.CAD for Java.
- **Puis-je charger un fichier DWG en Java ?** Oui, il suffit d'appeler `Image.load()` sur le chemin du DWG.
- **Quelle méthode change la police ?** `setPrimaryFontName`.
- **Ai-je besoin d'une licence pour la production ?** Oui, une licence commerciale est requise.
- **Le traitement par lots est-il possible ?** Absolument – parcourez plusieurs fichiers avec le même code.

## What is “load dwg file java”?

Charger un fichier DWG dans un environnement Java signifie lire les données binaires CAD dans un objet `Image` qu'Aspose.CAD peut manipuler. Une fois le fichier chargé, vous avez un accès programmatique complet aux calques, aux styles et aux entités texte.

## Why substitute fonts in a DWG file?

- **Cohérence :** Garantit que tous les collaborateurs voient la même police, quel que soit leur paramétrage local de polices.  
- **Lisibilité :** Certaines polices CAD par défaut sont difficiles à lire à l'écran ; passer à une police claire comme Arial améliore la clarté.  
- **Image de marque :** Aligne les dessins techniques avec les guides de style de l'entreprise.

## Prerequisites

- **Java Development Kit (JDK)** – toute version récente (8+ recommandée).  
- **Aspose.CAD for Java** – téléchargez depuis le [site web](https://releases.aspose.com/cad/java/).  
- **Fichier DWG d'exemple** – un dessin que vous souhaitez modifier (vous pouvez utiliser n'importe quel fichier DWG ou DXF pour les tests).

## Import Namespaces

Dans votre projet Java, importez les classes nécessaires pour travailler avec Aspose.CAD. Ces importations vous donnent accès au chargement d'images, aux objets spécifiques CAD et à la manipulation des styles.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Step‑by‑step guide to substitute the font

### Step 1: Load your DWG file (load dwg file java)

Tout d'abord, indiquez à l'API l'emplacement de votre fichier DWG (ou DXF) et chargez-le dans un objet `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Conseil pro :** Si vous travaillez directement avec des fichiers DWG, remplacez l'extension `.dxf` par `.dwg` dans la variable `srcFile`.

### Step 2: Iterate over the style table and set primary font name

Chaque dessin CAD contient une collection d'objets de style. Parcourez-les et utilisez la méthode `setPrimaryFontName` (l'appel d'API qui **définit le nom de la police principale**) pour remplacer la police.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Vous pouvez remplacer `"Arial"` par n'importe quelle police installée sur la machine exécutant le code.

### Step 3: Save the modified drawing

Après avoir mis à jour la police, écrivez les modifications dans un nouveau fichier DWG (ou écrasez l'original).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Le fichier enregistré utilise désormais la police que vous avez spécifiée, et toute annotation texte sera rendue avec cette police.

## Common Issues and Solutions

| Problème | Solution |
|----------|----------|
| **Police non appliquée** | Vérifiez que la police est installée sur le système d'exploitation hôte et que l'orthographe correspond exactement. |
| **`Image.load` génère une exception** | Assurez-vous que le chemin du fichier est correct et que le fichier est un format DWG/DXF pris en charge. |
| **Ralentissement des performances sur les gros fichiers** | Traitez les fichiers dans un thread séparé ou en lot pour éviter le blocage de l'interface utilisateur. |

## FAQ's

### Q1: Puis-je rétablir les substitutions de police dans mon fichier DWG ?

A1: Oui, vous pouvez rétablir les substitutions de police en rechargeant le fichier DWG original ou en utilisant la fonction d'annulation dans votre logiciel CAD.

### Q2: Existe-t-il des limitations aux substitutions de police dans Aspose.CAD pour Java ?

A2: Les capacités de substitution de police dépendent des polices disponibles sur le système. Assurez-vous que la police souhaitée est accessible ou envisagez de l'intégrer dans le fichier DWG.

### Q3: Comment gérer les ajustements de taille de police lors de la substitution ?

A3: Les ajustements de taille de police peuvent être effectués en accédant aux propriétés de style dans Aspose.CAD et en modifiant la taille de la police en conséquence.

### Q4: Puis-je automatiser la substitution de police dans un processus par lots ?

A4: Oui, Aspose.CAD pour Java prend en charge le traitement par lots. Vous pouvez automatiser les substitutions de police sur plusieurs fichiers DWG à l'aide de scripts ou de programmation.

### Q5: Aspose.CAD pour Java est-il compatible avec les derniers formats de fichiers CAD ?

A5: Oui, Aspose.CAD pour Java est régulièrement mis à jour pour prendre en charge les derniers formats de fichiers CAD, assurant la compatibilité avec les normes de l'industrie.

## Frequently Asked Questions

**Q : La méthode `setPrimaryFontName` affecte-t-elle uniquement les entités texte ?**  
R : Elle met à jour la police principale pour la table de styles, ce qui influence à son tour tous les objets texte qui font référence à ce style.

**Q : Puis-je utiliser une police personnalisée qui n'est pas installée sur le système ?**  
R : Aspose.CAD s'appuie sur le registre de polices du système d'exploitation. Pour utiliser une police personnalisée, installez‑la sur la machine exécutant le code.

**Q : Est‑il possible de changer la police pour une seule couche uniquement ?**  
R : Oui, vous pouvez filtrer les styles par nom de couche avant d'appeler `setPrimaryFontName`.

**Q : Quelle version d'Aspose.CAD est requise pour les fichiers DWG 2022 ?**  
R : La dernière version (en 2025) prend pleinement en charge DWG 2022. Vérifiez toujours les notes de version pour le support des formats spécifiques.

**Q : Comment gérer la licence dans un environnement de développement ?**  
R : Utilisez une licence d'évaluation temporaire pour les tests. En production, intégrez votre fichier de licence acheté en utilisant `License.setLicense("Aspose.Total.Java.lic");`.

---

**Dernière mise à jour :** 2025-12-28  
**Testé avec :** Aspose.CAD for Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}