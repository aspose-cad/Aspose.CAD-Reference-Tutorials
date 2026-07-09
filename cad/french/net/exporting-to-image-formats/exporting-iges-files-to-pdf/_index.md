---
date: 2026-07-09
description: Apprenez à convertir IGES en PDF en utilisant Aspose.CAD pour .NET. Suivez
  ce guide étape par étape pour exporter les fichiers IGES au format PDF rapidement
  et avec précision.
keywords:
- convert iges to pdf
- export iges as pdf
- create pdf from iges
- convert cad file to pdf
- generate pdf from cad
lastmod: 2026-07-09
linktitle: Exportation de fichiers IGES vers PDF
og_description: Convertissez IGES en PDF avec Aspose.CAD pour .NET. Ce tutoriel montre
  comment exporter les fichiers IGES en PDF efficacement avec des étapes sans code.
og_image_alt: Guide showing conversion of IGES files to PDF with Aspose.CAD in .NET
og_title: Convertir IGES en PDF – Guide rapide Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-07-09'
  description: Learn how to convert IGES to PDF using Aspose.CAD for .NET. Follow
    this step‑by‑step guide to export IGES files as PDF quickly and accurately.
  headline: Convert IGES to PDF with Aspose.CAD – Quick Guide
  type: TechArticle
- description: Learn how to convert IGES to PDF using Aspose.CAD for .NET. Follow
    this step‑by‑step guide to export IGES files as PDF quickly and accurately.
  name: Convert IGES to PDF with Aspose.CAD – Quick Guide
  steps:
  - name: Set up Your Project
    text: Create a new .NET console or class‑library project, or open an existing
      one where you want to add the conversion feature.
  - name: Add Aspose.CAD Reference
    text: Add the downloaded Aspose.CAD DLL to your project references. In Visual
      Studio, right‑click **References → Add Reference → Browse** and select the DLL.
  - name: Initialize the Path
    text: Define the folder that contains your IGES file and the output location.
  - name: Load the CAD Image
    text: '`Image.Load` reads the IGES file and creates an in‑memory representation.
      The `Image` class is Aspose.CAD''s primary entry point for any CAD format.'
  - name: Configure Rasterization Options
    text: '`PdfOptions` (derived from `CadRasterizationOptions`) lets you set page
      size, resolution, and vector‑preserving flags. The `PdfOptions` class defines
      how the CAD drawing is rasterized and saved as PDF.'
  - name: Save as PDF
    text: Finally, write the PDF file to disk. With these six straightforward steps,
      you have successfully **convert iges to pdf** using Aspose.CAD for .NET.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD works in ASP.NET, ASP.NET Core, and other web frameworks,
      providing server‑side conversion without UI dependencies.
    question: Can I use Aspose.CAD for .NET in a web application?
  - answer: Explore the comprehensive documentation [here](https://reference.aspose.com/cad/net/)
      for detailed insights into all supported features.
    question: Where can I find additional documentation for Aspose.CAD?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/)
      to evaluate the library before purchasing.
    question: Is there a free trial available?
  - answer: For temporary licenses, visit [this link](https://purchase.aspose.com/temporary-license/)
      to get the required licensing information.
    question: How can I obtain a temporary license?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      for prompt help and discussions.
    question: Need assistance or have questions?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- convert iges to pdf
- Aspose.CAD
- .NET CAD conversion
title: Convertir IGES en PDF avec Aspose.CAD – Guide rapide
url: /fr/net/exporting-to-image-formats/exporting-iges-files-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir IGES en PDF avec Aspose.CAD

## Introduction

Dans le monde en évolution rapide de la conception assistée par ordinateur, **convertir IGES en PDF** est une tâche courante que les ingénieurs et les architectes effectuent quotidiennement. Que vous ayez besoin d’un document imprimable pour la révision client ou d’une archive légère pour le contrôle de version, l’exportation de fichiers IGES vers PDF préserve la géométrie originale tout en rendant le fichier universellement accessible. Ce tutoriel vous guide à travers les étapes exactes pour convertir IGES en PDF à l’aide d’Aspose.CAD pour .NET, afin que vous puissiez automatiser le processus dans n’importe quelle application .NET.

## Réponses rapides
- **Quelle bibliothèque gère la conversion ?** Aspose.CAD for .NET.  
- **Combien de lignes de code sont nécessaires ?** En général deux lignes : charger le fichier IGES et appeler `Save`.  
- **Puis-je contrôler la taille de la page et la qualité ?** Oui, via `CadRasterizationOptions`.  
- **Une licence est‑elle nécessaire pour la production ?** Une licence commerciale est requise ; un essai gratuit est disponible. Vous pouvez obtenir une licence temporaire [this link](https://purchase.aspose.com/temporary-license/).  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Qu’est‑ce que « convertir IGES en PDF » ?
*Convertir IGES en PDF* signifie prendre un fichier d’échange CAD neutre (IGES) et le rendre sous forme de Portable Document Format (PDF) qui peut être ouvert sur n’importe quel appareil sans logiciel CAD. La conversion préserve la géométrie vectorielle, les calques et les annotations tout en les aplatissant dans un document à mise en page fixe.

## Pourquoi utiliser Aspose.CAD pour cette conversion ?
Aspose.CAD prend en charge **plus de 30 formats CAD et BIM** et peut traiter des fichiers jusqu’à **2 Go** sans charger l’ensemble du document en mémoire, offrant une conversion rapide côté serveur sans dépendances tierces. Cette performance quantifiée le rend idéal pour les pipelines de traitement par lots et les services cloud.

## Prérequis

Avant de commencer, assurez-vous de disposer de :

1. **Bibliothèque Aspose.CAD pour .NET** – téléchargez‑la depuis [here](https://releases.aspose.com/cad/net/). Vous pouvez également consulter la référence API [here](https://reference.aspose.com/cad/net/).  
2. **Environnement de développement .NET** – Visual Studio, Rider, ou tout IDE supportant .NET 5+.

Maintenant que les prérequis sont couverts, importons les espaces de noms requis pour la conversion.

## Importer les espaces de noms

La classe `Image` est la classe principale représentant un dessin CAD en mémoire. `CadRasterizationOptions` définit comment le dessin CAD est rasterisé pour la sortie vectorielle. La classe `PdfOptions` spécifie les paramètres de sortie pour les fichiers PDF.

``` 
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Ces espaces de noms fournissent la fonctionnalité de base pour charger, rasteriser et enregistrer les dessins CAD.

## Comment convertir IGES en PDF avec Aspose.CAD ?

Chargez le fichier IGES avec `Image.Load` et appelez immédiatement `Save` avec une option de rasterisation PDF — c’est la conversion complète en deux instructions. La bibliothèque gère le rendu vectoriel, l’incorporation des polices et le redimensionnement des pages automatiquement, vous obtenez ainsi une réplique PDF fidèle du modèle IGES original.

### Étape 1 : Configurer votre projet

Créez un nouveau projet console ou bibliothèque de classes .NET, ou ouvrez un projet existant où vous souhaitez ajouter la fonctionnalité de conversion.

### Étape 2 : Ajouter la référence Aspose.CAD

Ajoutez le DLL Aspose.CAD téléchargé aux références de votre projet. Dans Visual Studio, faites un clic droit sur **References → Add Reference → Browse** et sélectionnez le DLL.

### Étape 3 : Initialiser le chemin

``` 
string sourceDir = @"C:\CAD\Source";
string outputDir = @"C:\CAD\Output";
string igesFile = Path.Combine(sourceDir, "sample.iges");
string pdfFile = Path.Combine(outputDir, "sample.pdf");
```

### Étape 4 : Charger l’image CAD

``` 
Image cadImage = Image.Load(igesFile);
```

La classe `Image` est le point d’entrée principal d’Aspose.CAD pour tout format CAD.

### Étape 5 : Configurer les options de rasterisation

`PdfOptions` (dérivé de `CadRasterizationOptions`) vous permet de définir la taille de la page, la résolution et les indicateurs de préservation vectorielle.

``` 
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 842,      // A4 width in points
        PageHeight = 595,     // A4 height in points
        Resolution = 300      // 300 DPI for high‑quality output
    }
};
```

La classe `PdfOptions` définit comment le dessin CAD est rasterisé et enregistré en PDF.

### Étape 6 : Enregistrer en PDF

``` 
cadImage.Save(pdfFile, pdfOptions);
```

Avec ces six étapes simples, vous avez réussi à **convertir IGES en PDF** à l’aide d’Aspose.CAD pour .NET.

## Pièges courants & conseils

- **Fichiers volumineux :** augmentez `Resolution` uniquement si vous avez besoin de plus de détails ; un DPI plus élevé consomme plus de mémoire.  
- **Polices manquantes :** assurez‑vous que toutes les polices personnalisées utilisées dans le fichier IGES sont installées sur le serveur ; sinon, elles seront remplacées.  
- **Conversion par lots :** encapsulez la logique de chargement‑enregistrement dans une boucle `foreach` pour traiter plusieurs fichiers IGES automatiquement.

## Questions fréquentes

**Q : Puis‑je utiliser Aspose.CAD pour .NET dans une application web ?**  
**R :** Oui, Aspose.CAD fonctionne sous ASP.NET, ASP.NET Core et d’autres frameworks web, offrant une conversion côté serveur sans dépendances UI.

**Q : Où puis‑je trouver la documentation supplémentaire pour Aspose.CAD ?**  
**R :** Explorez la documentation complète [here](https://reference.aspose.com/cad/net/) pour des informations détaillées sur toutes les fonctionnalités prises en charge.

**Q : Existe‑t‑il un essai gratuit ?**  
**R :** Oui, vous pouvez accéder à un essai gratuit [here](https://releases.aspose.com/) pour évaluer la bibliothèque avant l’achat.

**Q : Comment obtenir une licence temporaire ?**  
**R :** Pour les licences temporaires, visitez [this link](https://purchase.aspose.com/temporary-license/) afin d’obtenir les informations de licence requises.

**Q : Besoin d’aide ou avez‑vous des questions ?**  
**R :** Rejoignez la communauté Aspose.CAD sur le [support forum](https://forum.aspose.com/c/cad/19) pour obtenir de l’aide rapide et des discussions.

---

**Dernière mise à jour :** 2026-07-09  
**Testé avec :** Aspose.CAD 24.11 for .NET  
**Auteur :** Aspose

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;
```
```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "figa2.igs";
```
```csharp
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code goes here
}
```
```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1000,
    PageWidth = 1000,
};

PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```
```csharp
cadImage.Save(MyDir + "figa2.pdf", pdfOptions);
```

Pour des ressources supplémentaires, consultez la page principale des releases [here](https://releases.aspose.com/). Si vous avez besoin d’assistance, visitez le [support forum](https://forum.aspose.com/c/cad/19).

## Tutoriels associés

- [Exportation de DWG en PDF ou images raster - Guide Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Exportation de DXF au format PDF - Tutoriel Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Exportation de DGN en PDF avec Aspose.CAD pour .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}