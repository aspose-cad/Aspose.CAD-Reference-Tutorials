---
date: 2026-02-15
description: Apprenez à définir la taille de la page PDF et à convertir le CAD en
  PDF à l'aide d'Aspose.CAD pour Java, avec mise à l'échelle automatique de la mise
  en page et exportation TIFF.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: Définir la taille de page PDF – Convertir CAD en PDF (Java)
url: /fr/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir la taille du canevas et le mode

## Introduction

Si vous devez **définir la taille de la page PDF** lors de la conversion de dessins CAD en PDF, vous êtes au bon endroit. Dans ce tutoriel, nous vous montrerons comment utiliser Aspose.CAD for Java pour définir des dimensions précises du canevas, activer le redimensionnement automatique de la mise en page, puis exporter le résultat à la fois en PDF et en TIFF. Que vous prépariez des schémas d'ingénierie pour l'impression ou que vous génériez des miniatures pour une galerie web, contrôler la taille de la page et la résolution de sortie est essentiel.

## Quick Answers
- **Que signifie « convertir CAD en PDF » ?** Transformer un dessin CAD (par ex., DXF, DWG) en un document PDF qui peut être visualisé sur n'importe quelle plateforme.  
- **Puis‑je également exporter en TIFF ?** Oui — utilisez `TiffOptions` pour créer des images raster haute résolution.  
- **Quelle option contrôle la taille du canevas en Java ?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Qu’est‑ce que le redimensionnement automatique de la mise en page ?** Un drapeau (`setAutomaticLayoutsScaling(true)`) qui préserve les proportions d'origine de la mise en page lorsque la taille du canevas change.  
- **Ai‑je besoin d’une licence pour Aspose.CAD ?** Une licence temporaire ou permanente est requise pour une utilisation en production.

## How to Set PDF Page Size When Converting CAD to PDF (Java)

Définir la taille de la page PDF (ou la taille du canevas) vous permet de spécifier les dimensions finales du document, ce qui est particulièrement utile lorsque vous devez **modifier les dimensions du PDF** pour correspondre aux normes d’impression ou aux exigences d’interface utilisateur. Ci‑dessous, nous parcourons chaque étape en expliquant le *pourquoi* derrière chaque ligne de code.

## What is **convert CAD to PDF**?

Convertir CAD en PDF signifie prendre des dessins d’ingénierie basés sur des vecteurs et les rendre sous forme de pages PDF, en conservant les traits, les calques et la géométrie tout en rendant le fichier universellement accessible.

## Why set canvas size **java**?

Définir la taille du canevas en Java vous permet de spécifier la résolution de sortie et les dimensions de la page, garantissant que le PDF ou le TIFF résultant correspond à vos exigences d’impression ou d’affichage. Cela vous donne également le contrôle du comportement de mise à l’échelle, essentiel pour les dessins grand format.

## Prerequisites

Avant de plonger dans le tutoriel, assurez‑vous que les prérequis suivants sont en place :

- Aspose.CAD for Java : assurez‑vous d’avoir la bibliothèque Aspose.CAD installée dans votre environnement Java. Vous pouvez la télécharger [ici](https://releases.aspose.com/cad/java/).
- Répertoire de documents : créez un répertoire de documents pour stocker vos fichiers CAD. Ce répertoire sera référencé dans les étapes du tutoriel.

Passons maintenant au guide étape par étape.

## Import Namespaces

Dans cette étape, nous allons importer les espaces de noms nécessaires pour démarrer votre projet Aspose.CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Step 1: Import Aspose.CAD Classes

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Dans cet extrait, nous configurons le chemin du répertoire de ressources et chargeons un fichier DXF à l’aide de la classe `Image` d’Aspose.CAD.

## Step 2: Set **CadRasterizationOptions** Properties (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Ici, nous créons une instance de `CadRasterizationOptions` et configurons des propriétés telles que la largeur de page, la hauteur de page et le **redimensionnement automatique de la mise en page**. C’est le cœur de la **configuration du mode canevas** pour votre conversion.

## Step 3: Create PdfOptions and Set VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nous créons maintenant une instance de `PdfOptions` et définissons sa propriété `VectorRasterizationOptions` avec les `CadRasterizationOptions` configurées précédemment.

## Step 4: Export to PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Enfin, nous enregistrons l’image CAD dans un fichier PDF en utilisant les options spécifiées, complétant le processus de **conversion CAD en PDF**.

## Step 5: Create TiffOptions and Set VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Dans cette étape, nous configurons une instance de `TiffOptions` et définissons sa propriété `VectorRasterizationOptions`.

## Step 6: Export to TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Enfin, nous enregistrons l’image CAD dans un fichier TIFF en utilisant les options spécifiées, démontrant comment **exporter CAD en TIFF** après avoir configuré la taille du canevas.

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| Le PDF de sortie est blanc | `setNoScaling(true)` désactive le rendu pour certains dessins | Supprimez `setNoScaling(true)` ou définissez‑le sur `false`. |
| La résolution du TIFF semble basse | Largeur/hauteur de page trop petites | Augmentez les valeurs de `setPageWidth` / `setPageHeight`. |
| La mise en page est déformée | Redimensionnement automatique de la mise en page désactivé | Assurez‑vous que `setAutomaticLayoutsScaling(true)` est activé. |

## Why Adjust Canvas Size and DPI?

Modifier la taille du canevas influence directement la résolution de rasterisation du résultat. Si vous devez **augmenter la résolution du TIFF**, il suffit d’augmenter les valeurs de `setPageWidth` / `setPageHeight` ou d’appeler `rasterizationOptions.setResolution(300)` avant de créer le `TiffOptions`. Cela vous fournit des images raster de haute qualité, adaptées à l’impression ou à une inspection détaillée.

## Frequently Asked Questions

### Q1 : Puis‑je utiliser Aspose.CAD for Java avec d’autres frameworks Java ?

R1 : Oui, Aspose.CAD est conçu pour s’intégrer de façon transparente avec divers frameworks Java.

### Q2 : Une licence temporaire est‑elle disponible pour Aspose.CAD ?

R2 : Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

### Q3 : Où puis‑je obtenir du support communautaire pour Aspose.CAD ?

R3 : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire et les discussions.

### Q4 : Puis‑je essayer Aspose.CAD gratuitement ?

R4 : Absolument ! Obtenez un essai gratuit [ici](https://releases.aspose.com/).

### Q5 : Comment acheter Aspose.CAD for Java ?

R5 : Achetez le produit [ici](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q : La taille du canevas affecte‑t‑elle la qualité vectorielle du PDF ?**  
R : Non. La taille du canevas contrôle les dimensions de la page ; les données vectorielles restent indépendantes de la résolution, garantissant un rendu net à n’importe quel niveau de zoom.

**Q : Puis‑je définir un DPI différent pour la sortie TIFF ?**  
R : Oui. Ajustez `rasterizationOptions.setResolution(dpiValue)` avant de créer les `TiffOptions`.

**Q : Comment **modifier les dimensions du PDF** pour un PDF existant sans re‑rendre le CAD ?**  
R : Utilisez Aspose.PDF pour charger le PDF généré et appelez `pdf.getPages().setPageSize(PageSize.A4)` ou une taille personnalisée.

**Q : Quelle est la meilleure façon de **convertir dxf en pdf** tout en préservant les calques ?**  
R : Conservez `setAutomaticLayoutsScaling(true)` et évitez `setNoScaling(true)` ; cela maintient la visibilité des calques et la fidélité de la mise en page.

## Conclusion

Félicitations ! Vous avez réussi à **convertir CAD en PDF** et à **exporter CAD en TIFF** tout en **définissant la taille du canevas en Java**, en activant le **redimensionnement automatique de la mise en page**, et en apprenant à **configurer le mode canevas** pour des sorties de haute qualité. Ce tutoriel constitue une base solide pour vos projets de conversion CAD. Explorez davantage de fonctionnalités et de possibilités dans la [documentation Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**Dernière mise à jour :** 2026-02-15  
**Testé avec :** Aspose.CAD for Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}