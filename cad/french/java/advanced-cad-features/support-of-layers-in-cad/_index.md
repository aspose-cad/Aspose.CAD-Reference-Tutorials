---
date: 2026-02-17
description: Apprenez à enregistrer un DWG au format JPEG en Java avec Aspose.CAD,
  à ajouter plusieurs calques et à ajuster les dimensions CAD pour une conversion
  d'image précise.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Enregistrer un DWG en JPEG avec prise en charge des calques en Java
url: /fr/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

 produce final.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer DWG en JPEG avec prise en charge des calques en Java

## Introduction

Dans ce tutoriel, vous découvrirez comment **enregistrer DWG en JPEG** tout en tirant pleinement parti de la prise en charge des calques dans Aspose.CAD for Java. Les calques vous permettent d’isoler des parties spécifiques d’un dessin, facilitant ainsi l’exportation uniquement de ce dont vous avez besoin. Nous parcourrons chaque étape, de la configuration de l’environnement à l’exportation d’un JPEG incluant uniquement les calques que vous choisissez.

## Quick Answers
- **Que signifie « save DWG as JPEG » ?** Cela convertit un dessin DWG (ou autre CAD) en une image raster JPEG.  
- **Puis‑je n’inclure que des calques sélectionnés ?** Oui – utilisez la méthode `setLayers` pour spécifier quels calques rendre.  
- **Comment modifier la taille de l’image ?** Ajustez `setPageWidth` et `setPageHeight` dans `CadRasterizationOptions`.  
- **S’agit‑il d’une solution uniquement Java ?** L’exemple utilise Aspose.CAD for Java, mais les mêmes concepts s’appliquent à d’autres langages.  
- **Ai‑je besoin d’une licence ?** Une version d’essai gratuite suffit pour les tests ; une licence commerciale est requise pour la production.

## What is “save DWG as JPEG”?
Enregistrer DWG en JPEG signifie rasteriser un fichier CAD vectoriel (DWG, DWF, DXF, etc.) en un bitmap JPEG standard. Cela est utile lorsque vous devez intégrer des dessins CAD dans des pages web, des e‑mails ou des rapports qui ne prennent en charge que des images raster.

## Why use layer‑aware JPEG conversion?
- **Se concentrer sur les données pertinentes :** Exportez uniquement les calques dont vous avez besoin, réduisant ainsi la taille du fichier et le désordre visuel.  
- **Conserver l’intention de conception :** Les calques préservent le regroupement logique des objets, vous permettant de réutiliser le même fichier source pour différentes sorties.  
- **Contrôle total sur les dimensions :** En ajustant les options de rasterisation, vous pouvez produire des images haute résolution qui correspondent à vos exigences de publication.

## Prerequisites

Avant de commencer, assurez‑vous de disposer de ce qui suit :

1. **Bibliothèque Aspose.CAD for Java** – téléchargez‑la depuis le [site web](https://releases.aspose.com/cad/java/). Suivez le guide d’installation pour ajouter les fichiers JAR à votre classpath.  
2. **Environnement de développement Java** – un JDK récent (8 ou supérieur) installé sur votre machine.

Maintenant que tout est prêt, explorons le code nécessaire pour **enregistrer DWG en JPEG** avec un rendu sélectif des calques.

## Import Namespaces

Commencez par importer les classes Aspose.CAD requises ainsi que les utilitaires Java standard :

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

Définissez où se trouve le fichier source DWF et où le JPEG de sortie sera écrit.

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

Créez une instance de `CadRasterizationOptions` et définissez la taille de sortie souhaitée. Modifier ces valeurs vous permet de **ajuster les dimensions CAD** pour le JPEG final.

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

*Astuce :* Pour **ajouter plusieurs calques**, développez l’appel `Arrays.asList`, par ex., `Arrays.asList("LayerA", "LayerB", "LayerC")`. Cela vous permet de **sélectionner des calques CAD spécifiques** pour la conversion.

### Step 5: Configure JPEG Options (Java Convert CAD Image)

Associez les paramètres de rasterisation au format de sortie JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 6: Export to JPG (Save DWG as JPEG)

Enfin, écrivez l’image sur le disque. Cette étape **enregistre le dessin CAD en tant que fichier JPEG** contenant uniquement les calques sélectionnés.

```java
image.save(outFile, jpegOptions);
```

En suivant ces étapes, vous avez réussi à **enregistrer DWG en JPEG** tout en contrôlant quels calques apparaissent et en personnalisant les dimensions de l’image.

## How to Convert DWF to JPEG with Layer Selection

Bien que l’exemple utilise une source DWF, le même pipeline de rasterisation fonctionne pour tout format CAD pris en charge (DWG, DXF, DGN, etc.). Il suffit de changer l’extension du fichier dans `srcFile` et la bibliothèque gérera automatiquement l’opération **convert DWF to JPEG** (ou autre format).

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **Layers not appearing** | Vérifiez que les noms de calques correspondent exactement à ceux stockés dans le fichier DWF (sensible à la casse). |
| **Output image is blank** | Assurez‑vous que `setPageWidth` et `setPageHeight` sont suffisamment grands pour les étendues du dessin. |
| **License exception** | Utilisez une licence d’essai pour les tests ; obtenez une licence complète pour les environnements de production. |

## Frequently Asked Questions

**Q : Puis‑je ajouter plusieurs calques aux options de rasterisation ?**  
R : Absolument. Étendez la `stringList` avec des noms de calques supplémentaires, par ex., `Arrays.asList("LayerA", "LayerB")`.

**Q : Aspose.CAD est‑il compatible avec d’autres formats CAD ?**  
R : Oui, il prend en charge DWG, DXF, DWF et bien d’autres formats.

**Q : Comment modifier les dimensions de l’image de sortie ?**  
R : Modifiez `setPageWidth` et `setPageHeight` dans l’instance `CadRasterizationOptions`.

**Q : Où puis‑je acheter une licence pour Aspose.CAD ?**  
R : Vous pouvez explorer les options de licence [ici](https://purchase.aspose.com/buy).

**Q : Où puis‑je obtenir du support communautaire ?**  
R : Rejoignez la communauté Aspose.CAD sur le [forum](https://forum.aspose.com/c/cad/19) pour obtenir de l’aide et participer aux discussions.

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}