---
date: 2026-03-29
description: Apprenez à créer un PDF à partir de CAD, à définir la taille du canevas
  et à exporter le CAD en PDF ou TIFF à l’aide d’Aspose.CAD pour .NET dans ce guide
  étape par étape.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Comment créer un PDF à partir de CAD : définir la taille du canevas et le
  mode dans Aspose.CAD pour .NET'
url: /fr/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir la taille et le mode du canevas dans Aspose.CAD pour .NET

## Introduction

Prêt à **créer un PDF à partir de fichiers CAD** tout en contrôlant les dimensions de sortie ? Dans ce tutoriel, nous parcourrons la configuration de la taille et du mode du canevas, le chargement d’un fichier CAD, et son exportation en PDF ou TIFF avec Aspose.CAD pour .NET. Que vous ayez besoin de **convertir DXF en PDF**, de générer des dessins haute résolution, ou simplement d’ajuster la zone de rastérisation, les étapes ci‑dessous vous fourniront une solution solide, prête pour la production.

## Réponses rapides
- **Que signifie « créer PDF à partir de CAD » ?** Conversion d’un dessin CAD (par ex., DXF, DWG) en document PDF qui préserve les détails vectoriels et raster.  
- **Quelle option contrôle la taille de sortie ?** `CadRasterizationOptions.PageWidth` et `PageHeight` (taille du canevas).  
- **Puis‑je également exporter en TIFF ?** Oui – utilisez `TiffOptions` avec les mêmes paramètres de rastérisation.  
- **Ai‑je besoin d’une licence pour la production ?** Une licence commerciale est requise ; une version d’essai gratuite est disponible.  
- **Versions .NET prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Qu’est‑ce que « créer PDF à partir de CAD » ?
Créer un PDF à partir de CAD signifie rendre le dessin CAD dans un format orienté page (PDF) qui peut être visualisé, imprimé ou partagé sans nécessiter de logiciel CAD. Aspose.CAD se charge du travail lourd, vous permettant de définir la taille du canevas, le redimensionnement et le format de sortie.

## Pourquoi définir la taille du canevas lors de la création d’un PDF à partir de CAD ?
Définir la taille du canevas vous donne un contrôle précis sur la résolution et les dimensions du PDF ou du TIFF résultant. Ceci est particulièrement utile lorsque :
- Vous préparez des dessins pour l’impression sur des formats de papier spécifiques.  
- Vous générez des vignettes ou des images haute résolution pour un aperçu web.  
- Vous assurez une mise en page cohérente entre plusieurs documents.

## Prérequis

- Bibliothèque Aspose.CAD : Téléchargez et installez la bibliothèque Aspose.CAD depuis le site [Aspose.CAD website](https://releases.aspose.com/cad/net/).
- Environnement de développement : Assurez‑vous d’avoir un environnement de développement .NET configuré sur votre machine.
- Fichier CAD d’exemple : Pour ce tutoriel, nous utiliserons un fichier DXF d’exemple. Vous pouvez en trouver un dans la [documentation Aspose.CAD](https://reference.aspose.com/cad/net/).

## Importer les espaces de noms

Tout d’abord, importez les espaces de noms requis pour le traitement CAD :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Comment créer un PDF à partir de CAD avec une taille de canevas personnalisée

### Étape 1 : Charger le fichier CAD

Nous commençons par **charger le fichier CAD** (par ex., un DXF) dans un objet `Image`. C’est à ce moment que vous **chargez le fichier CAD** en mémoire.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Étape 2 : Créer CadRasterizationOptions

Créez une instance de `CadRasterizationOptions` et définissez la taille du canevas. Les propriétés `PageWidth` et `PageHeight` vous permettent de **définir la taille du canevas** aux dimensions exactes dont vous avez besoin.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Étape 3 : Créer PdfOptions (Exporter CAD en PDF)

Liez les paramètres de rastérisation à un objet `PdfOptions`. Cette configuration vous permet de **exporter le CAD en PDF** avec le canevas personnalisé que vous avez défini.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Étape 4 : Exporter en PDF (Convertir DXF en PDF)

Enregistrez maintenant l’image au format PDF. Cette étape **crée un PDF à partir de CAD** en utilisant les options que nous avons définies.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Étape 5 : Créer TiffOptions (Exporter CAD en TIFF)

Si vous avez également besoin d’une image raster, configurez `TiffOptions`. Les mêmes options de rastérisation sont réutilisées, de sorte que **l’exportation du CAD en TIFF** respecte la taille du canevas.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Étape 6 : Exporter en TIFF

Enfin, enregistrez le dessin au format TIFF.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Problèmes courants et solutions

- **Le canevas apparaît recadré** – Vérifiez que `AutomaticLayoutsScaling` est réglé sur `true` et que `NoScaling` est `false` afin que le dessin s’ajuste au canevas.  
- **PDF basse résolution** – Augmentez `PageWidth`/`PageHeight` ou définissez `Resolution` sur `CadRasterizationOptions`.  
- **Erreur fichier introuvable** – Assurez‑vous que `MyDir` pointe vers un répertoire valide et que le nom du fichier DXF correspond exactement.

## Questions fréquemment posées

### Q1 : Puis‑je utiliser Aspose.CAD avec d’autres bibliothèques .NET ?
R1 : Oui, Aspose.CAD s’intègre parfaitement avec d’autres bibliothèques .NET, offrant des capacités améliorées pour la manipulation CAD.

### Q2 : Une version d’essai gratuite est‑elle disponible pour Aspose.CAD ?
R2 : Oui, vous pouvez explorer les fonctionnalités d’Aspose.CAD avec une version d’essai gratuite. Visitez [ici](https://releases.aspose.com/) pour commencer.

### Q3 : Comment obtenir du support pour Aspose.CAD ?
R3 : Pour le support et les discussions, rendez‑vous sur le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q4 : Où trouver une documentation complète pour Aspose.CAD ?
R4 : Consultez la [documentation Aspose.CAD](https://reference.aspose.com/cad/net/) pour des informations détaillées et des exemples.

### Q5 : Comment acheter Aspose.CAD pour .NET ?
R5 : Pour acheter Aspose.CAD, visitez la [page d’achat](https://purchase.aspose.com/buy).

**Questions supplémentaires**

**Q : Puis‑je exporter un dessin CAD multi‑pages vers un seul PDF ?**  
R : Oui. Définissez `PageCount` dans `CadRasterizationOptions` et la bibliothèque concaténera les pages en un seul PDF.

**Q : La taille du canevas affecte‑t‑elle la qualité des données vectorielles ?**  
R : Les données vectorielles restent indépendantes de la résolution ; la taille du canevas n’influence que les éléments rasterisés et la résolution de l’image.

---

**Dernière mise à jour :** 2026-03-29  
**Testé avec :** Aspose.CAD 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}