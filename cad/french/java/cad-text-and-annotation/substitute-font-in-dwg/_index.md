---
date: 2026-05-04
description: Apprenez à convertir le DXF en DWG et à définir la police principale
  en Java avec Aspose.CAD. Guide étape par étape pour des visuels CAD parfaits.
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: Remplacer la police dans DWG
second_title: Aspose.CAD Java API
title: Convertir le DXF en DWG et changer la police dans le DWG Aspose.CAD Java
url: /fr/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment charger un fichier DWG en Java et remplacer la police avec Aspose.CAD

## Introduction

Si vous devez **convertir dxf en dwg** dans des applications Java et donner à vos dessins un aspect soigné, remplacer la police est une solution rapide. Avec Aspose.CAD pour Java, vous pouvez remplacer le style de texte par défaut par n’importe quelle police installée sur le système, garantissant que chaque annotation apparaît exactement comme vous le souhaitez. Dans ce tutoriel, nous parcourrons l’ensemble du processus — du chargement d’un fichier DWG en Java à l’utilisation de la méthode `setPrimaryFontName` pour changer la police.

## Quick Answers
- **Quelle bibliothèque faut‑il ?** Aspose.CAD pour Java.  
- **Puis‑je charger un fichier DWG en Java ?** Oui, il suffit d’appeler `Image.load()` sur le chemin du DWG.  
- **Quelle méthode change la police ?** `setPrimaryFontName`.  
- **Ai‑je besoin d’une licence pour la production ?** Oui, une licence commerciale est requise.  
- **Le traitement par lots est‑il possible ?** Absolument — bouclez sur plusieurs fichiers avec le même code.

## Qu’est‑ce que **convert dxf to dwg** ?

« Convert dxf to dwg » désigne la transformation d’un fichier DXF (Drawing Exchange Format) en format DWG natif utilisé par de nombreuses applications CAD. La conversion vous permet de prendre un dessin DXF largement supporté, de l’intégrer dans un flux de travail DWG, puis d’appliquer un style avancé — tel que le remplacement de police—à l’aide d’Aspose.CAD.

## Pourquoi remplacer les polices dans un fichier DWG ?

- **Cohérence :** Garantit que tous les collaborateurs voient la même police, quel que soit leur paramètre local.  
- **Lisibilité :** Certaines polices CAD par défaut sont difficiles à lire à l’écran ; passer à une police claire comme Arial améliore la clarté.  
- **Image de marque :** Aligne les dessins techniques avec les guides de style de l’entreprise.  

## Cas d’utilisation courants

| Scénario | Pourquoi c’est important |
|----------|---------------------------|
| **Conversion par lots d’anciennes dessins DXF** | Vous pouvez les convertir en DWG et appliquer une police d’entreprise en une seule passe. |
| **Préparer des dessins pour des présentations client** | Des polices cohérentes et lisibles donnent un aspect professionnel aux documents. |
| **Pipelines CAD automatisés** | L’intégration du remplacement de police élimine les étapes manuelles de post‑traitement. |

## Prérequis

- **Java Development Kit (JDK)** – toute version récente (8+ recommandée).  
- **Aspose.CAD pour Java** – téléchargez-le depuis le [site web](https://releases.aspose.com/cad/java/).  
- **Fichier DWG/DXF d’exemple** – un dessin que vous souhaitez modifier (vous pouvez utiliser n’importe quel fichier DWG ou DXF pour les tests).

## Importer les espaces de noms

Dans votre projet Java, importez les classes nécessaires pour travailler avec Aspose.CAD. Ces imports vous donnent accès au chargement d’images, aux objets spécifiques CAD et à la manipulation des styles.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## Guide étape par étape pour remplacer la police

### Étape 1 : Charger votre fichier DWG (load dwg file java)

Tout d’abord, indiquez à l’API l’emplacement de votre fichier DWG (ou DXF) et chargez‑le dans un objet `CadImage`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **Astuce :** Si vous travaillez directement avec des fichiers DWG, remplacez l’extension `.dxf` par `.dwg` dans la variable `srcFile`.

### Étape 2 : Parcourir la table de styles et définir le nom de la police principale

Chaque dessin CAD contient une collection d’objets de style. Parcourez‑les et utilisez la méthode `setPrimaryFontName` (l’appel d’API qui **définit le nom de la police principale**) pour remplacer la police.

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

Vous pouvez changer `"Arial"` par n’importe quelle police installée sur la machine exécutant le code.

### Étape 3 : Enregistrer le dessin modifié

Après avoir mis à jour la police, écrivez les modifications dans un nouveau fichier DWG (ou écrasez l’original).

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

Le fichier enregistré utilise désormais la police que vous avez spécifiée, et toute annotation texte sera rendue avec cette police.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Police non appliquée** | Vérifiez que la police est installée sur le système d’exploitation et que l’orthographe correspond exactement. |
| **`Image.load` lève une exception** | Assurez‑vous que le chemin du fichier est correct et que le fichier est au format DWG/DXF pris en charge. |
| **Ralentissement des performances sur de gros fichiers** | Traitez les fichiers dans un thread séparé ou regroupez‑les par lots pour éviter le blocage de l’interface. |

## Foire aux questions

**Q : La méthode `setPrimaryFontName` n’affecte‑t‑elle que les entités texte ?**  
R : Elle met à jour la police principale de la table de styles, ce qui influence tous les objets texte qui référencent ce style.

**Q : Puis‑je utiliser une police personnalisée qui n’est pas installée sur le système ?**  
R : Aspose.CAD s’appuie sur le registre de polices du système d’exploitation. Pour utiliser une police personnalisée, installez‑la sur la machine exécutant le code.

**Q : Est‑il possible de changer la police pour une seule couche uniquement ?**  
R : Oui, vous pouvez filtrer les styles par nom de couche avant d’appeler `setPrimaryFontName`.

**Q : Quelle version d’Aspose.CAD est requise pour les fichiers DWG 2022 ?**  
R : La dernière version (en 2025) prend pleinement en charge DWG 2022. Consultez toujours les notes de version pour le support de formats spécifiques.

**Q : Comment gérer la licence dans un environnement de développement ?**  
R : Utilisez une licence d’évaluation temporaire pour les tests. En production, intégrez votre fichier de licence acheté avec `License.setLicense("Aspose.Total.Java.lic");`.

---

**Dernière mise à jour :** 2026-05-04  
**Testé avec :** Aspose.CAD pour Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}