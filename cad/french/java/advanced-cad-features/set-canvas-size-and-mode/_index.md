---
date: 2025-12-10
description: Apprenez à convertir des fichiers CAD en PDF avec Aspose.CAD pour Java
  tout en définissant la taille du canevas, le redimensionnement automatique de la
  mise en page et l'exportation vers TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: Convertir CAD en PDF – Définir la taille et le mode du canevas (Java)
url: /fr/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir la taille du canevas et le mode

## Introduction

Vous cherchez à **convert CAD to PDF** tout en gardant le contrôle total sur la taille du canevas et le mode de rendu ? Ce guide complet vous accompagne pas à pas pour définir la taille du canevas en Java, activer le redimensionnement automatique de la mise en page, puis exporter le résultat aux formats PDF et TIFF à l’aide d’Aspose.CAD. Que vous raffiniez une chaîne de production ou que vous expérimentiez un prototype, vous trouverez ici des instructions claires et concrètes.

## Réponses rapides
- **Que signifie « convert CAD to PDF » ?** Transformer un dessin CAD (par ex. DXF, DWG) en un document PDF consultable sur n’importe quelle plateforme.  
- **Puis-je également exporter vers TIFF ?** Oui — utilisez `TiffOptions` pour créer des images raster haute résolution.  
- **Quelle option contrôle la taille du canevas en Java ?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Qu’est‑ce que le redimensionnement automatique de la mise en page ?** Un drapeau (`setAutomaticLayoutsScaling(true)`) qui préserve les proportions d’origine de la mise en page lorsque la taille du canevas change.  
- **Ai‑je besoin d’une licence pour Aspose.CAD ?** Une licence temporaire ou permanente est requise pour une utilisation en production.

## Qu’est‑ce que **convert CAD to PDF** ?

Convertir CAD en PDF consiste à prendre des dessins d’ingénierie basés sur des vecteurs et à les rendre sous forme de pages PDF, en conservant les traits, les calques et la géométrie tout en rendant le fichier universellement accessible.

## Pourquoi définir la taille du canevas **java** ?

Définir la taille du canevas en Java vous permet de spécifier la résolution de sortie et les dimensions de la page, garantissant que le PDF ou le TIFF résultant correspond à vos exigences d’impression ou d’affichage. Cela vous donne également le contrôle du comportement de mise à l’échelle, essentiel pour les dessins grand format.

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous d’avoir les prérequis suivants :

- Aspose.CAD for Java : assurez‑vous que la bibliothèque Aspose.CAD est installée dans votre environnement Java. Vous pouvez la télécharger [ici](https://releases.aspose.com/cad/java/).

- Répertoire de documents : créez un répertoire de documents pour stocker vos fichiers CAD. Ce répertoire sera référencé dans les étapes du tutoriel.

Maintenant, commençons le guide étape par étape.

## Importer les espaces de noms

Dans cette étape, nous allons importer les espaces de noms nécessaires pour lancer votre projet Aspose.CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Étape 1 : Importer les classes Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Dans cet extrait, nous configurons le chemin vers le répertoire des ressources et chargeons un fichier DXF à l’aide de la classe `Image` d’Aspose.CAD.

## Étape 2 : Définir les propriétés de **CadRasterizationOptions** (définir la taille du canevas java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Ici, nous créons une instance de `CadRasterizationOptions` et configurons des propriétés telles que la largeur de page, la hauteur de page et le **redimensionnement automatique de la mise en page**. C’est le cœur de la **configuration du mode du canevas** pour votre conversion.

## Étape 3 : Créer PdfOptions et définir VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Nous créons maintenant une instance de `PdfOptions` et définissons sa propriété `VectorRasterizationOptions` avec les `CadRasterizationOptions` configurées précédemment.

## Étape 4 : Exporter en PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Enfin, nous enregistrons l’image CAD dans un fichier PDF en utilisant les options spécifiées, complétant ainsi le processus **convert CAD to PDF**.

## Étape 5 : Créer TiffOptions et définir VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Dans cette étape, nous configurons une instance de `TiffOptions` et définissons sa propriété `VectorRasterizationOptions`.

## Étape 6 : Exporter en TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Enfin, nous enregistrons l’image CAD dans un fichier TIFF en utilisant les options spécifiées, démontrant comment **export CAD to TIFF** après avoir configuré la taille du canevas.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| Le PDF de sortie est vide | `setNoScaling(true)` désactive le rendu pour certains dessins | Supprimez `setNoScaling(true)` ou définissez‑le sur `false`. |
| La résolution du TIFF semble basse | Largeur/hauteur de page trop petite | Augmentez les valeurs de `setPageWidth` / `setPageHeight`. |
| La mise en page apparaît déformée | Redimensionnement automatique de la mise en page désactivé | Assurez‑vous que `setAutomaticLayoutsScaling(true)` est activé. |

## Conclusion

Félicitations ! Vous avez réussi à **convert CAD to PDF** et à **export CAD to TIFF** tout en **définissant la taille du canevas java**, en activant le **redimensionnement automatique de la mise en page**, et en apprenant à **configurer le mode du canevas** pour des sorties de haute qualité. Ce tutoriel constitue une base solide pour vos projets de conversion CAD. Explorez davantage de fonctionnalités et de possibilités dans la [documentation Aspose.CAD](https://reference.aspose.com/cad/java/).

## FAQ

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

**Questions supplémentaires**

**Q : La taille du canevas affecte‑t‑elle la qualité vectorielle du PDF ?**  
R : Non. La taille du canevas contrôle les dimensions de la page ; les données vectorielles restent indépendantes de la résolution, garantissant un rendu net à n’importe quel niveau de zoom.

**Q : Puis‑je définir un DPI différent pour la sortie TIFF ?**  
R : Oui. Ajustez `rasterizationOptions.setResolution(dpiValue)` avant de créer `TiffOptions`.

---

**Dernière mise à jour :** 2025-12-10  
**Testé avec :** Aspose.CAD for Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}