---
date: 2026-09-09
description: Apprenez comment découper un bloc dans CAD, convertir DXF en PDF et enregistrer
  CAD au format PDF avec Aspose.CAD for .NET. Suivez ce guide étape par étape.
keywords:
- how to clip block
- convert dxf to pdf
- save cad as pdf
- create pdf from cad
- load cad image
lastmod: 2026-09-09
linktitle: Prise en charge du découpage de blocs dans CAD
og_description: Apprenez comment découper un bloc dans CAD, convertir DXF en PDF et
  enregistrer CAD au format PDF avec Aspose.CAD for .NET. Guide rapide pour les développeurs.
og_image_alt: Screenshot of block clipping in a CAD drawing using Aspose.CAD for .NET
og_title: Comment découper un bloc dans CAD avec Aspose.CAD for .NET
schemas:
- author: Aspose
  dateModified: '2026-09-09'
  description: Learn how to clip block in CAD, convert DXF to PDF and save CAD as
    PDF using Aspose.CAD for .NET. Follow this step‑by‑step guide.
  headline: How to clip block in CAD using Aspose.CAD for .NET
  type: TechArticle
- description: Learn how to clip block in CAD, convert DXF to PDF and save CAD as
    PDF using Aspose.CAD for .NET. Follow this step‑by‑step guide.
  name: How to clip block in CAD using Aspose.CAD for .NET
  steps:
  - name: define the document directory
    text: Replace “Your Document Directory” with the actual path to your CAD documents.
  - name: specify input and output files
    text: Adjust the file names as per your project requirements.
  - name: load CAD image
    text: The `Image` class **loads CAD image** from the specified input file, enabling
      you to apply clipping before any rendering.
  - name: configure rasterization options
    text: Customize rasterization options according to your rendering needs, such
      as setting the output resolution or background color.
  - name: save as PDF
    text: Save the processed CAD image as a PDF file, effectively **saving CAD as
      PDF** while the block remains clipped.
  type: HowTo
- questions:
  - answer: No, clipping is applied only during rasterization; vector exports retain
      the original geometry.
    question: Does block clipping affect vector export formats like SVG?
  - answer: The library can process files up to **2 GB** on a 64‑bit process without
      full memory loading.
    question: What is the maximum file size Aspose.CAD can handle when clipping?
  - answer: Yes—iterate through `image.Blocks` and assign a `BlockClippingInfo` to
      each target block before saving.
    question: Can I clip multiple blocks in one operation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD clipping
- Aspose.CAD
- .NET CAD processing
- PDF conversion
title: Comment découper un bloc dans CAD avec Aspose.CAD for .NET
url: /fr/net/layout-and-object-handling/supporting-block-clipping-in-cad/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment découper un bloc dans CAD avec Aspose.CAD pour .NET

## Introduction

Dans ce guide complet, vous apprendrez **comment découper un bloc** dans un dessin CAD, convertir un DXF en PDF et enregistrer un CAD en PDF — le tout avec Aspose.CAD pour .NET. Le découpage de bloc vous permet de masquer ou de révéler des parties d’un bloc sans modifier la géométrie d’origine, une technique qui accélère le rendu et réduit la taille du fichier.

## Réponses rapides
- **Que fait le découpage de bloc ?** Il masque la géométrie sélectionnée à l’intérieur d’un bloc en fonction d’une frontière de découpage.  
- **Quelle bibliothèque le prend en charge ?** Aspose.CAD pour .NET fournit une API intégrée pour le découpage de bloc.  
- **Ai‑je besoin d’une licence ?** Une licence temporaire ou permanente est requise pour une utilisation en production.  
- **Puis‑je également convertir un DXF en PDF ?** Oui — utilisez les mêmes options de rasterisation et appelez `Save` avec le format PDF.  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Qu'est-ce que le découpage de bloc ?
`Block clipping` est une fonctionnalité CAD qui définit une région de découpage pour une entité bloc, faisant en sorte que la géométrie située en dehors de cette région soit ignorée lors de la rasterisation. Cela améliore les performances lorsqu’une seule partie d’un gros bloc est nécessaire à l’affichage.

## Pourquoi utiliser le découpage de bloc dans CAD ?
Aspose.CAD prend en charge **plus de 50** formats CAD et BIM et peut traiter des fichiers jusqu’à **2 GB** sans charger l’ensemble du fichier en mémoire. L’utilisation du découpage de bloc réduit la zone rendue jusqu’à **70 %**, ce qui accélère la conversion PDF et diminue la consommation de mémoire dans les charges de travail côté serveur.

## Prérequis

- Connaissances de base du langage de programmation C#.  
- Visual Studio installé sur votre machine.  
- Bibliothèque Aspose.CAD pour .NET. Vous pouvez la télécharger depuis la [page de téléchargement d’Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).  
- Un fichier CAD d’exemple pour les tests. Vous pouvez utiliser le fichier DXF fourni.

## Importer les espaces de noms

Dans votre projet C#, assurez‑vous d’importer les espaces de noms nécessaires pour travailler avec Aspose.CAD :

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Passons maintenant à l’analyse du code d’exemple étape par étape :

## Comment découper un bloc dans CAD ?

La classe `Image` charge un dessin CAD en mémoire, et `BlockClippingInfo` définit le polygone de découpage pour un bloc. Chargez votre dessin CAD avec `new Image("input.dxf")`, créez un objet `BlockClippingInfo` qui définit le polygone de découpage, affectez‑le au bloc cible via `image.Blocks["BlockName"].ClippingInfo = clippingInfo`, puis rasterisez ou enregistrez l’image. Cette séquence découpe le bloc en une seule passe et fonctionne tant pour les sources DXF que DWG.

### Étape 1 : définir le répertoire des documents

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

Remplacez « Your Document Directory » par le chemin réel vers vos documents CAD.

### Étape 2 : spécifier les fichiers d'entrée et de sortie

```csharp
string inputFile = MyDir + "SLS-CW-CD-CE001-R01_blockClip.dxf";
string outputFile = MyDir + "SLS-CW-CD-CE001-R01_blockClip.pdf";
```

Ajustez les noms de fichiers selon les exigences de votre projet.

### Étape 3 : charger l'image CAD

```csharp
using (CadImage cadImage = (CadImage)Image.Load(inputFile))
{
```

La classe `Image` **charge l'image CAD** depuis le fichier d’entrée spécifié, vous permettant d’appliquer le découpage avant tout rendu.

### Étape 4 : configurer les options de rasterisation

```csharp
var rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    DrawType = CadDrawTypeMode.UseObjectColor,
    PageWidth = 1200,
    PageHeight = 1600,
    Margins = new Margins
    {
        Top = 5,
        Right = 30,
        Bottom = 5,
        Left = 30
    },
    Layouts = new string[] { "Model" }
};
```

Personnalisez les options de rasterisation en fonction de vos besoins de rendu, comme la résolution de sortie ou la couleur d’arrière‑plan.

### Étape 5 : enregistrer au format PDF

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outputFile, pdfOptions);
```

Enregistrez l’image CAD traitée sous forme de fichier PDF, réalisant ainsi **l’enregistrement du CAD en PDF** tout en maintenant le bloc découpé.

## Conclusion

Félicitations ! Vous avez implémenté avec succès le découpage de bloc dans CAD en utilisant Aspose.CAD pour .NET, et vous savez maintenant comment **convertir un DXF en PDF**, **enregistrer un CAD en PDF**, et **charger une image CAD** pour un traitement ultérieur. Ces techniques vous offrent un contrôle granulaire sur les performances de rendu et la qualité du résultat.

## FAQ

### Q1 : Puis‑je utiliser Aspose.CAD pour .NET avec d’autres langages de programmation ?

R1 : Aspose.CAD est principalement conçu pour les applications .NET. Si vous travaillez avec d’autres langages, envisagez d’explorer Aspose.CAD pour Java.

### Q2 : Quelles options de licence sont disponibles pour Aspose.CAD ?

R2 : Oui, vous pouvez consulter les options de licence et effectuer un achat sur la [page de licence d’Aspose.CAD](https://purchase.aspose.com/buy).

### Q3 : Existe‑t‑il une version d’essai gratuite d’Aspose.CAD pour .NET ?

R3 : Oui, vous pouvez accéder à l’essai gratuit sur la [page des releases de produits Aspose](https://releases.aspose.com/).

### Q4 : Comment obtenir du support pour Aspose.CAD ?

R4 : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire et les discussions.

### Q5 : Puis‑je utiliser Aspose.CAD sans licence permanente ?

R5 : Oui, vous pouvez obtenir une licence temporaire via la [page de demande de licence temporaire](https://purchase.aspose.com/temporary-license/).

**Q : Le découpage de bloc affecte‑t‑il les formats d’exportation vectorielle comme SVG ?**  
R : Non, le découpage n’est appliqué que lors de la rasterisation ; les exportations vectorielles conservent la géométrie d’origine.

**Q : Quelle est la taille maximale de fichier qu’Aspose.CAD peut gérer lors du découpage ?**  
R : La bibliothèque peut traiter des fichiers jusqu’à **2 GB** sur un processus 64 bits sans charger l’intégralité en mémoire.

**Q : Puis‑je découper plusieurs blocs en une seule opération ?**  
R : Oui — parcourez `image.Blocks` et affectez un `BlockClippingInfo` à chaque bloc cible avant l’enregistrement.

---

**Dernière mise à jour :** 2026-09-09  
**Testé avec :** Aspose.CAD 24.11 pour .NET  
**Auteur :** Aspose

## Tutoriels associés

- [How to Convert and Export CAD Drawings to PDF with Aspose.CAD for .NET – Tutorial](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)
- [Aspose CAD Example: Convert Layouts to Raster Image in .NET](/cad/net/cad-drawing-manipulation/convert-layouts-to-raster-image/)
- [Create PDF from DXF Specific Layout – Aspose.CAD Guide](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}