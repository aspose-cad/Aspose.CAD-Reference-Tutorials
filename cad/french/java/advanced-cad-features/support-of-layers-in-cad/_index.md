---
date: 2025-12-13
description: Apprenez à enregistrer un fichier CAD au format JPEG en Java avec Aspose.CAD,
  à ajouter plusieurs calques et à ajuster les dimensions du CAD pour une conversion
  d'image précise.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Enregistrer le CAD au format JPEG avec prise en charge des calques en Java
url: /fr/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer CAD en JPEG avec prise en charge des calques en Java

## Introduction

Dans ce tutoriel, vous découvrirez comment **enregistrer CAD en JPEG** tout en tirant pleinement parti de la prise en charge des calques dans Aspose.CAD for Java. Les calques vous permettent d’isoler des parties spécifiques d’un dessin, facilitant ainsi l’exportation uniquement de ce dont vous avez besoin. Nous parcourrons chaque étape, de la configuration de l’environnement à l’exportation d’un JPEG contenant uniquement les calques que vous choisissez.

## Quick Answers
- **Que signifie « enregistrer CAD en JPEG » ?** Cela convertit un dessin CAD en une image raster JPEG.  
- **Puis‑je n’inclure que des calques sélectionnés ?** Oui – utilisez la méthode `setLayers` pour spécifier les calques à rendre.  
- **Comment modifier la taille de l’image ?** Ajustez `setPageWidth` et `setPageHeight` dans `CadRasterizationOptions`.  
- **S’agit‑il d’une solution uniquement Java ?** L’exemple utilise Aspose.CAD for Java, mais les mêmes concepts s’appliquent à d’autres langages.  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.

## Prerequisites

Avant de commencer, assurez‑vous de disposer de ce qui suit :

1. **Aspose.CAD for Java Library** – téléchargez‑la depuis le [website](https://releases.aspose.com/cad/java/). Suivez le guide d’installation pour ajouter les fichiers JAR à votre classpath.  
2. **Java Development Environment** – un JDK récent (8 ou supérieur) installé sur votre machine.

Maintenant que tout est prêt, explorons le code nécessaire pour **enregistrer CAD en JPEG** avec un rendu sélectif des calques.

## Import Namespaces

Commencez par importer les classes Aspose.CAD requises ainsi que les utilitaires Java standards :

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Step‑by‑Step Guide

### Step 1: Set Up File Paths

Définissez l’emplacement du fichier DWF source et celui où le JPEG de sortie sera écrit.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Step 2: Load the DWF Image

Utilisez la méthode `Image.load` d’Aspose.CAD pour lire le dessin CAD.

```java
Image image = Image.load(srcFile);
```

### Step 3: Configure Rasterization Options (Adjust CAD Dimensions)

Créez une instance de `CadRasterizationOptions` et définissez la taille de sortie souhaitée. Modifier ces valeurs vous permet de **ajuster les dimensions du CAD** pour le JPEG final.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Step 4: Specify Layers (Add Multiple Layers)

Si vous souhaitez rendre plusieurs calques, ajoutez simplement leurs noms à la liste. Ici, nous commençons avec un seul calque nommé « LayerA ».

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Pro tip :* Pour **ajouter plusieurs calques**, développez l’appel `Arrays.asList`, par ex., `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Step 5: Configure JPEG Options (Java Convert CAD Image)

Liez les paramètres de rasterisation au format de sortie JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 6: Export to JPG (Save CAD as JPEG)

Enfin, écrivez l’image sur le disque. Cette étape **enregistre le dessin CAD en tant que fichier JPEG** contenant uniquement les calques sélectionnés.

```java
image.save(outFile, jpegOptions);
```

En suivant ces étapes, vous avez réussi à **enregistrer CAD en JPEG** tout en contrôlant les calques affichés et en personnalisant les dimensions de l’image.

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **Layers not appearing** | Vérifiez que les noms des calques correspondent exactement à ceux stockés dans le fichier DWF (sensible à la casse). |
| **Output image is blank** | Assurez‑vous que `setPageWidth` et `setPageHeight` sont suffisamment grands pour couvrir l’étendue du dessin. |
| **License exception** | Utilisez une licence d’essai pour les tests ; obtenez une licence complète pour les environnements de production. |

## Frequently Asked Questions

**Q : Puis‑je ajouter plusieurs calques aux options de rasterisation ?**  
R : Absolument. Étendez la `stringList` avec d’autres noms de calques, par ex., `Arrays.asList("LayerA", "LayerB")`.

**Q : Aspose.CAD est‑il compatible avec d’autres formats CAD ?**  
R : Oui, il prend en charge DWG, DXF, DWF et de nombreux autres formats.

**Q : Comment puis‑je modifier les dimensions de l’image de sortie ?**  
R : Modifiez `setPageWidth` et `setPageHeight` dans l’instance `CadRasterizationOptions`.

**Q : Où puis‑je acheter une licence pour Aspose.CAD ?**  
R : Vous pouvez explorer les options de licence [here](https://purchase.aspose.com/buy).

**Q : Où puis‑je obtenir du support communautaire ?**  
R : Rejoignez la communauté Aspose.CAD sur le [forum](https://forum.aspose.com/c/cad/19) pour obtenir de l’aide et participer aux discussions.

---

**Dernière mise à jour :** 2025-12-13  
**Testé avec :** Aspose.CAD for Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}