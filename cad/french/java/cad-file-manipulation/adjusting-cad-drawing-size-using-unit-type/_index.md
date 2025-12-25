---
date: 2025-12-25
description: Apprenez à exporter des fichiers DWG au format BMP en utilisant Aspose.CAD
  pour Java. Ce guide étape par étape montre comment ajuster la taille du dessin CAD
  et convertir le CAD en BMP de manière efficace.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: Exporter DWG en BMP – Ajuster la taille du CAD selon le type d’unité (Java)
url: /fr/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter DWG en BMP – Ajuster la taille du dessin CAD en utilisant le type d'unité avec Aspose.CAD pour Java

## Introduction

Lorsque vous devez **exporter DWG en BMP**, contrôler la taille de sortie et l'unité de mesure est essentiel pour le traitement en aval ou l'impression. Dans ce tutoriel, vous apprendrez comment ajuster la taille du dessin CAD et convertir le CAD en BMP avec Aspose.CAD pour Java, en utilisant la propriété `UnitType` pour définir l'unité de mesure. Les étapes sont expliquées en termes simples, afin que vous puissiez suivre même si vous êtes novice avec la bibliothèque.

## Quick Answers
- **Que signifie « exporter DWG en BMP » ?** Conversion d'un dessin DWG en image raster BMP.  
- **Quelle propriété contrôle la taille de sortie ?** `CadRasterizationOptions.setUnitType()` définit l'unité (par ex., centimètre).  
- **Ai-je besoin d'une licence pour exécuter le code ?** Un essai gratuit suffit pour l'évaluation ; une licence est requise pour la production.  
- **Puis-je choisir d'autres mises en page ?** Oui, utilisez `setLayouts()` pour spécifier les mises en page du modèle ou de l'espace papier.  
- **Quels formats de sortie sont pris en charge ?** En plus du BMP, vous pouvez exporter en PNG, JPEG, TIFF, etc., en modifiant la classe d'options.

## What is **export DWG to BMP**?

Exporter DWG en BMP signifie rasteriser un fichier DWG basé sur des vecteurs en une image bitmap (BMP). Cela est utile lorsque vous avez besoin d'une représentation pixel‑parfaite pour des systèmes hérités, des pipelines de traitement d'images ou des scénarios d'affichage simples.

## Why adjust CAD drawing size with **Unit Type**?

Définir le type d'unité vous permet de contrôler les dimensions physiques de l'image exportée sans calculer manuellement les facteurs d'échelle. Cela garantit que le bitmap correspond aux mesures réelles (par ex., centimètres), ce qui est crucial pour les dessins d'ingénierie et la documentation imprimée.

## Prerequisites

- **Environnement de développement Java** – Un JDK fonctionnel (8 ou supérieur) et un IDE ou un outil de construction (Maven/Gradle).  
- **Bibliothèque Aspose.CAD pour Java** – Téléchargez et intégrez la bibliothèque Aspose.CAD dans votre projet Java. Vous pouvez obtenir la bibliothèque [ici](https://releases.aspose.com/cad/java/).

## Import Namespaces

Dans votre code Java, incluez les espaces de noms nécessaires pour accéder aux fonctionnalités d'Aspose.CAD. Ajoutez les imports suivants :

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Maintenant, décomposons le processus d'ajustement de la taille du dessin CAD en utilisant le type d'unité en étapes gérables :

## Step 1: Define Data Directory

### Étape 1 : Définir le répertoire de données

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Définissez le chemin du répertoire où se trouvent vos fichiers CAD.

## Step 2: Load CAD Drawing

### Étape 2 : Charger le dessin CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Chargez le dessin CAD en utilisant la classe `Image` d'Aspose.CAD.

## Step 3: Create BMP Options

### Étape 3 : Créer les options BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

Instanciez la classe `BmpOptions` pour exporter la mise en page CAD au format BMP.

## Step 4: Configure Rasterization Options

### Étape 4 : Configurer les options de rasterisation

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Créez une instance de `CadRasterizationOptions` et associez‑la aux `BmpOptions` pour la rasterisation vectorielle.

## Step 5: Set Unit Type

### Étape 5 : Définir le type d'unité

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Spécifiez le type d'unité souhaité pour le dessin CAD. Dans cet exemple, nous l'avons défini sur **Centimeter**, ce qui influence directement la taille de l'image exportée lorsque vous **ajustez la taille du dessin CAD**.

## Step 6: Set Layouts

### Étape 6 : Définir les mises en page

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Définissez les mises en page à prendre en compte lors de l'exportation. Dans ce cas, nous avons sélectionné la mise en page **"Model"**, mais vous pouvez passer aux mises en page d'espace papier si nécessaire.

## Step 7: Export to BMP

### Étape 7 : Exporter en BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Enfin, enregistrez le dessin CAD modifié au format BMP. Cette étape finalise le flux de travail **exporter DWG en BMP** tout en conservant les ajustements de taille que vous avez configurés.

## Common Issues and Solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| **L'image de sortie est trop petite** | Type d'unité non défini ou valeur par défaut (pixel) utilisée | Appelez `setUnitType()` avec la mesure souhaitée (par ex., `UnitType.Centimeter`). |
| **Mauvaise mise en page exportée** | Erreur de frappe du nom de la mise en page | Vérifiez les noms de mise en page avec un visualiseur CAD ; utilisez la chaîne exacte dans `setLayouts()`. |
| **Exception de licence** | Exécution sans licence valide en production | Appliquez une licence temporaire ou permanente comme décrit dans la FAQ. |

## Frequently Asked Questions (Extended)

**Q : Puis‑je utiliser Aspose.CAD pour Java avec d'autres langages de programmation ?**  
R : Aspose.CAD prend principalement en charge Java, mais des versions sont disponibles pour d'autres langages comme .NET.

**Q : Existe‑t‑il des options de licence pour Aspose.CAD ?**  
R : Oui, vous pouvez explorer les options de licence et acheter Aspose.CAD [ici](https://purchase.aspose.com/buy).

**Q : Un essai gratuit est‑il disponible pour Aspose.CAD ?**  
R : Bien sûr, vous pouvez accéder à un essai gratuit [ici](https://releases.aspose.com/).

**Q : Comment obtenir du support pour Aspose.CAD pour Java ?**  
R : Consultez le forum Aspose.CAD [ici](https://forum.aspose.com/c/cad/19) pour un support complet.

**Q : Puis‑je obtenir une licence temporaire pour Aspose.CAD ?**  
R : Oui, vous pouvez acquérir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

---

**Dernière mise à jour :** 2025-12-25  
**Testé avec :** Aspose.CAD for Java 24.10  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}