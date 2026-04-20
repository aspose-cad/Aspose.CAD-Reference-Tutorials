---
date: 2026-01-22
description: Apprenez à créer des PDF à partir de dessins CAO, à convertir des DWG
  en PDF et à personnaliser la taille des pages PDF en utilisant Aspose.CAD pour Java.
linktitle: Single PDF with Different Layouts
second_title: Aspose.CAD Java API
title: Comment créer un PDF à partir de dessins CAO avec Aspose.CAD pour Java
url: /fr/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer un PDF à partir de dessins CAD avec Aspose.CAD pour Java

## Introduction

Dans ce tutoriel, vous découvrirez **comment créer un PDF à partir de dessins CAD** en utilisant la bibliothèque Aspose.CAD pour Java. Que vous ayez besoin de **convertir DWG en PDF**, d’exporter un fichier CAD complexe, ou d’appliquer une **taille de page PDF personnalisée**, les étapes ci‑dessous vous guideront vers une solution propre et programmatique. Parcourons le processus ensemble, afin que vous puissiez générer même PDF ?** page des mises en page avant l’enregistrement.
- **Quels formats CAD sont pris en charge ?** DWG, DXF, DWF, DGN et bien d’autres.
- **Ai‑je besoin d’une licence pour la production ?** Une licence temporaire suffit pour les tests ; une licence complète est requise pour un usage commercial.
- **Quelle version de Java est requise ?** Java 8 ou ultérieure.

## Qu’est‑ce que « créer un PDF à partir de CAD » ?
Créer un PDF à partir de CAD signifie rasteriser des dessins CAD vectoriels en un document à mise en page fixe (PDF) qui peut être visualisé sur n’importe quel appareil sans nécessiter de logiciel CAD. C’est idéal pour partager des conceptions, imprimer des plans ou archiver des travaux d’ingénierie.

## Pourquoi utiliser Aspose.CAD pour Java ?
- **Aucune dépendance externe** – Java pur, pas de DLL natives.
- **Contrôle fin** sur les options de rasterisation telles que le DPI, la taille de page et la sélection de mise en page.
- **Traitement par lots** – gérez de nombreux dessins en une seule exécution.
- **Conversion précise** – préserve les épaisseurs de ligne, les couleurs et les calques.

## Prérequis

Avant de commencer, assurez‑vous d’avoir les éléments suivants :

- **Environnement Java** – JDK 8 ou plus récent installé.
- **Bibliothèque Aspose.CAD** – Téléchargez et installez la bibliothèque Aspose.CAD pour Java depuis le [lien de téléchargement](https://releases.aspose.com/cad/java/).
- **Répertoire de documents** – Un dossier contenant les dessins DWG (ou autres CAD) que vous souhaitez convertir.

## Importer les packages

Dans votre projet Java, importez les classes nécessaires :

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Guide étape par étape

### Étape 1 : Charger le dessin CAD

Tout d’abord, chargez le fichier CAD source (par ex., un DWG) dans un objet `CadImage`. C’est le point d’entrée pour toute opération **export CAD to PDF**.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

### Étape 2 : Configurer les options de rasterisation

Définissez comment les données CAD doivent être rasterisées. Ici, nous fixons une largeur et une hauteur de page de base qui seront utilisées pour les mises en page n’ayant pas de taille personnalisée.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

### Étape 3 : Personnaliser les tailles de page des mises en page

Si vous avez besoin d’une **taille de page PDF personnalisée**, ajoutez des entrées pour chaque mise en page que vous souhaitez voir apparaître dans le PDF final. Cela vous permet de **convertir DWG en PDF** avec des dimensions différentes selon la mise en page.

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

### Étape 4 : Définir les options PDF

Combinez les paramètres de rasterisation avec les options spécifiques au PDF. La propriété `VectorRasterizationOptions` indique à Aspose.CAD d’utiliser les tailles de mise en page que nous venons de définir.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Étape 5 : Enregistrer en PDF

Enfin, exportez le dessin CAD vers un fichier PDF unique contenant toutes les mises en page spécifiées. Cette étape **sauvegarde CAD as PDF** en un seul appel.

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

> **Astuce pro :** Réutilisez le même objet `PdfOptions` si vous devez exporter plusieurs dessins en lot – cela réduit la surcharge de création d’objets.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Pages blanches dans le PDF de sortie** | Vérifiez que les noms de mise en page (`"ANSI C Plot"`, `"8.5 x 11 Plot"`) correspondent exactement à ceux définis dans le fichier CAD. |
| **Résolution de sortie faible** | Augmentez le DPI en appelant `rasterizationOptions.setResolution(300);` avant l’enregistrement. |
| **Licence non appliquée** | Chargez votre licence temporaire ou complète avant tout appel Aspose.CAD : `License license = new License(); license.setLicense("Aspose.CAD.lic");` |

## Foire aux questions

### Q1 : Puis‑je utiliser Aspose.CAD pour Java avec d’autres bibliothèques Java ?

R1 : Oui, Aspose.CAD pour Java est conçue pour s’intégrer de façon transparente avec d’autres bibliothèques Java, offrant une fonctionnalité étendue.

### Q2 : Existe‑t‑il une version d’essai ?

R2 : Absolument ! Vous pouvez accéder à une version d’essai gratuite [ici](https://releases.aspose.com/).

### Q3 : Où puis‑je obtenir un support supplémentaire ?

R3 : Consultez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire et les discussions.

### Q4 : Comment obtenir une licence temporaire ?

R4 : Vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis‑je acheter la version complète ?

R5 : Achetez la version complète d’Aspose.CAD pour Java [ici](https://purchase.aspose.com/buy).

---

**Dernière mise à jour :** 2026-01-22  
**Testé avec :** Aspose.CAD pour Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}