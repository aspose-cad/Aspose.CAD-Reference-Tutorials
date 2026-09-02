---
date: 2026-07-04
description: Apprenez comment définir la taille de la page PDF lors de la conversion
  de fichiers OBJ en PDF en utilisant Aspose.CAD pour .NET. Guide étape par étape
  avec les prérequis, les options de rasterisation et les options PDF.
keywords:
- set pdf page size
- load obj file
- save cad as pdf
- 3d model to pdf
- how to convert obj
linktitle: Prise en charge du format OBJ dans Aspose.CAD - Tutoriel
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size while converting OBJ files to PDF using
    Aspose.CAD for .NET. Step‑by‑step guide with prerequisites, rasterization options,
    and PDF options.
  headline: Set PDF Page Size for OBJ Files with Aspose.CAD - Tutorial
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports over **30** input formats—including DWG, DXF,
      DGN, and STL—and can export to more than **20** raster and vector formats.
    question: Is Aspose.CAD compatible with other CAD file formats?
  - answer: Absolutely! You can explore a free trial version [here](https://releases.aspose.com/).
    question: Can I try Aspose.CAD before purchasing?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to ask
      questions and share experiences with the community.
    question: How do I obtain support for Aspose.CAD?
  - answer: Yes, temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for testing?
  - answer: You can purchase Aspose.CAD [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full license?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Définir la taille de la page PDF pour les fichiers OBJ avec Aspose.CAD - Tutoriel
url: /fr/net/3d-model-support/supporting-obj-format-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir la taille de la page PDF pour les fichiers OBJ avec Aspose.CAD - Tutoriel

## Introduction

Si vous développez des applications CAD en .NET et que vous devez **définir la taille de la page PDF** lors de la conversion de modèles OBJ, Aspose.CAD pour .NET offre une API propre, orientée code, qui gère la rasterisation et la génération de PDF en un seul flux. Dans ce tutoriel, nous verrons comment installer la bibliothèque, charger un fichier OBJ, configurer les dimensions de la page, puis enregistrer le résultat au format PDF. À la fin, vous disposerez d’un modèle réutilisable pour transformer n’importe quel modèle 3 D en un document PDF parfaitement dimensionné.

## Réponses rapides
- **Aspose.CAD peut‑il convertir OBJ en PDF ?** Oui – chargez l’OBJ avec `Image.Load` et rasterisez‑le en PDF.
- **Comment définir une taille de page PDF personnalisée ?** Utilisez `PdfOptions` → `PageSize` ou définissez la largeur/hauteur dans `RasterizationOptions`.
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Une licence est‑elle nécessaire pour le développement ?** Un essai gratuit suffit pour l’évaluation ; une licence est requise en production.
- **La conversion est‑elle efficace en mémoire ?** Aspose.CAD diffuse les données et peut gérer des PDF de plusieurs centaines de pages sans charger le fichier complet en mémoire.

## Qu’est‑ce que le format OBJ ?
Le format OBJ est une définition géométrique 3‑D textuelle largement utilisée qui stocke les positions des sommets, les coordonnées de texture et les définitions de faces. Il est supporté par la plupart des outils de modélisation 3‑D et est idéal pour l’échange entre les environnements CAD et les pipelines de rendu.

## Pourquoi définir une taille de page PDF personnalisée ?
Aspose.CAD peut rendre un dessin CAD à n’importe quelle taille raster. En définissant explicitement les dimensions de la page PDF, vous vous assurez que le document final correspond à vos normes de reporting, s’adapte aux formats de papier standards (A4, Letter) ou respecte des mises en page d’impression personnalisées. Avantage quantifié : l’API peut générer des PDF jusqu’à **200 mm × 200 mm** en un seul appel, en traitant des fichiers de plus de **500 Mo** sans dépasser 250 Mo de RAM.

## Prérequis

- **Bibliothèque Aspose.CAD** – Assurez‑vous que la bibliothèque Aspose.CAD est installée dans votre projet .NET. Vous pouvez la télécharger [ici](https://releases.aspose.com/cad/net/) et consulter la référence complète de l’API dans la [documentation](https://reference.aspose.com/cad/net/).
- **Répertoire de documents** – Créez un dossier pour vos actifs CAD ; nous le désignerons « Your Document Directory » tout au long du guide.
- **Environnement de développement .NET** – Visual Studio 2022 ou tout IDE supportant .NET 6+.

## Comment définir la taille de page PDF lors de la conversion d’OBJ en PDF ?

Chargez le fichier OBJ, configurez les options de rasterisation avec la largeur et la hauteur souhaitées, associez ces options à une instance de `PdfOptions`, puis appelez `Save`. Ce modèle en deux étapes garantit que la page PDF correspond aux dimensions que vous spécifiez tout en préservant les détails du modèle.

## Étape 1 : Importer les espaces de noms

La classe `Image` gère tous les formats CAD, et la classe `PdfOptions` contrôle la sortie PDF.  
`Image` représente un document CAD et fournit des méthodes pour charger et enregistrer des fichiers. `PdfOptions` définit les paramètres de génération du PDF tels que la taille de la page et la compression.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Étape 2 : Charger le fichier OBJ

Chargez le fichier OBJ dans l’objet image Aspose.CAD. Remplacez `"example-580-W.obj"` par le nom de votre fichier OBJ.

```csharp
string MyDir = "Your Document Directory";
using (Aspose.CAD.Image CADDoc = Aspose.CAD.Image.Load(MyDir + "example-580-W.obj"))
{
    // Your code for further processing goes here
}
```

## Étape 3 : Configurer les options de rasterisation

`RasterizationOptions` définit la taille raster qui devient finalement la taille de la page PDF. Le réglage de `PageWidth` et `PageHeight` vous permet de contrôler les dimensions exactes du PDF généré.  
`CadRasterizationOptions` (exposé via `RasterizationOptions`) spécifie les paramètres de rasterisation tels que les dimensions de la page et la résolution.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();

rasterizationOptions.PageWidth = CADDoc.Size.Width;
rasterizationOptions.PageHeight = CADDoc.Size.Height;
```

## Étape 4 : Créer les options PDF

`PdfOptions` lie les paramètres de rasterisation à l’écrivain PDF. En assignant l’instance `RasterizationOptions`, vous assurez que le PDF hérite de la taille de page que vous avez définie.

```csharp
Aspose.CAD.ImageOptions.PdfOptions CADf = new Aspose.CAD.ImageOptions.PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 5 : Enregistrer en PDF

Appelez la méthode `Save` sur l’objet `Image`, en passant le nom du fichier cible et les `PdfOptions` configurés. La bibliothèque écrit un PDF avec la taille de page exacte que vous avez spécifiée.  
`Save` écrit l’image dans un fichier en utilisant le format et les options spécifiés.

```csharp
CADDoc.Save(MyDir + "example-580-W_custom.pdf", CADf);
```

## Problèmes courants et solutions

- **Dimensions de page incorrectes** – Vérifiez que `PageWidth` et `PageHeight` sont définis en **pixels** ; utilisez `Resolution` pour convertir les pouces ou millimètres en pixels (par ex., 300 dpi → 1 pouce = 300 px).
- **Textures manquantes** – Les fichiers OBJ référencent souvent des fichiers `.mtl` externes ; assurez‑vous que le fichier de matériau se trouve dans le même répertoire que l’OBJ.
- **Utilisation mémoire élevée pour les gros fichiers** – Activez `Image.SaveOptions.Compression` pour réduire la pression mémoire lors de rendus haute résolution.

## Questions fréquemment posées

**Q : Aspose.CAD est‑il compatible avec d’autres formats de fichiers CAD ?**  
R : Oui, Aspose.CAD prend en charge plus de **30** formats d’entrée — dont DWG, DXF, DGN et STL — et peut exporter vers plus de **20** formats raster et vectoriels.

**Q : Puis‑je essayer Aspose.CAD avant d’acheter ?**  
R : Absolument ! Vous pouvez explorer une version d’essai gratuite [ici](https://releases.aspose.com/).

**Q : Comment obtenir du support pour Aspose.CAD ?**  
R : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour poser des questions et partager vos expériences avec la communauté.

**Q : Des licences temporaires sont‑elles disponibles pour les tests ?**  
R : Oui, des licences temporaires peuvent être obtenues [ici](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je acheter une licence complète ?**  
R : Vous pouvez acheter Aspose.CAD [ici](https://purchase.aspose.com/buy).

---

**Dernière mise à jour :** 2026-07-04  
**Testé avec :** Aspose.CAD 24.11 pour .NET  
**Auteur :** Aspose

## Tutoriels associés

- [Exportation de fichiers IGES vers PDF - Guide Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [Exportation de DXF au format PDF - Tutoriel Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Exportation de dessins CAD vers PDF - Tutoriel Aspose.CAD](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}