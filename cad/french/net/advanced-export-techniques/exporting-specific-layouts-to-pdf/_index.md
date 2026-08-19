---
date: 2026-03-13
description: Apprenez à définir les options de rasterisation CAD et à exporter des
  mises en page DWG spécifiques en PDF à l’aide d’Aspose.CAD pour .NET – le guide
  définitif pour créer un PDF à partir d’un fichier CAD.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Définir les options de rasterisation CAD – Exporter des mises en page spécifiques
  en PDF - Guide Aspose.CAD
url: /fr/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportation de mises en page spécifiques vers PDF - Guide Aspose.CAD

## Introduction

Dans ce tutoriel, vous découvrirez **comment définir les options de rasterisation CAD** afin de pouvoir exporter une mise en page unique — ou plusieurs mises en page — d’un fichier DWG directement vers PDF. Aspose.CAD pour .NET rend le processus de *dwg to pdf conversion c#* simple, vous offrant un contrôle total sur la taille de la page, la résolution et la sélection de la mise en page. À la fin du guide, vous serez capable de **créer un PDF à partir d’un fichier CAD** en quelques lignes de code.

## Réponses rapides
- **Que fait « set cad rasterization options » ?**  
  Il indique à Aspose.CAD comment rendre les données vectorielles (mises en page, calques, épaisseurs de ligne) en pages PDF rasterisées.  
- **Quelle méthode exporte une mise en page DWG vers PDF ?**  
  Utilisez `Image.Save` avec un `PdfOptions` configuré contenant votre `CadRasterizationOptions`.  
- **Puis-je exporter plusieurs mises en page à la fois ?**  
  Oui – fournissez un tableau de noms de mises en page dans la propriété `Layouts`.  
- **Ai-je besoin d’une licence pour une utilisation en production ?**  
  Une licence commerciale est requise ; un essai gratuit est disponible pour l’évaluation.  
- **Quelles versions de .NET sont prises en charge ?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 et ultérieures.

## Qu’est‑ce que « set cad rasterization options » ?

`CadRasterizationOptions` est la classe qui contrôle la façon dont les entités CAD sont rasterisées lors de la conversion vers des formats basés sur le raster tels que le PDF. En configurant ses propriétés — dimensions de la page, sélection de la mise en page, couleur d’arrière‑plan, etc. — vous déterminez le résultat visuel de l’opération **export dwg layout to pdf**.

## Pourquoi définir les options de rasterisation CAD ?

- **Précision** – Conservez les épaisseurs de ligne et les échelles exactement comme elles apparaissent dans le dessin CAD original.  
- **Performance** – Rendu uniquement des mises en page dont vous avez besoin, réduisant la taille du fichier et le temps de traitement.  
- **Flexibilité** – Ajustez la largeur/hauteur de la page, le DPI et l’arrière‑plan pour correspondre à vos normes de reporting.  

## Prérequis

Avant de plonger dans le code, assurez‑vous d’avoir :

- **Aspose.CAD for .NET** installé. Vous pouvez le télécharger [ici](https://releases.aspose.com/cad/net/).  
- Un environnement de développement .NET (Visual Studio, VS Code, ou tout IDE de votre choix).  
- Un fichier DWG contenant au moins une mise en page (le fichier d’exemple utilisé ici est `visualization_-_conference_room.dwg`).

## Importer les espaces de noms

Dans votre projet .NET, importez les espaces de noms nécessaires pour Aspose.CAD :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Guide étape par étape

### Étape 1 : Charger le fichier DWG

Tout d’abord, indiquez à Aspose.CAD le fichier DWG source que vous souhaitez convertir.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Étape 2 : Définir **CadRasterizationOptions**

Ici nous configurons les paramètres de rasterisation qui déterminent la taille de la page PDF et la résolution.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Conseil pro :** Ajustez `PageWidth` et `PageHeight` pour correspondre aux dimensions de la mise en page PDF cible. Des valeurs plus grandes augmentent le détail mais aussi la taille du fichier.

### Étape 3 : Spécifier le nom de la mise en page

Indiquez à Aspose.CAD quelle(s) mise(s) en page rendre. Remplacez `"Layout1"` par le nom exact de la mise en page dans votre fichier DWG.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Pourquoi c’est important :** En limitant le tableau `Layouts`, vous évitez d’exporter des feuilles indésirables, rendant l’opération **dwg to pdf conversion c#** plus rapide et le PDF résultant plus propre.

### Étape 4 : Créer `PdfOptions`

Liez les paramètres de rasterisation aux options d’exportation PDF.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Étape 5 : Exporter vers PDF

Enfin, enregistrez la mise en page rendue sous forme de fichier PDF.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Étape 6 : Afficher un message de succès

Une sortie console rapide confirme que l’opération a réussi.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Problèmes courants & solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **Aucun PDF généré** | Le tableau `Layouts` ne correspond à aucun nom de mise en page dans le DWG. | Vérifiez les noms des mises en page à l’aide d’un visualiseur CAD et mettez à jour la propriété `Layouts`. |
| **Pages blanches** | `PageWidth`/`PageHeight` définis à 0 ou à des valeurs extrêmement petites. | Utilisez des dimensions réalistes (par ex., 1600 × 1600) ou laissez Aspose calculer automatiquement en omettant ces propriétés. |
| **Échelle incorrecte** | Le DPI n’est pas défini lorsque une sortie haute résolution est requise. | Définissez `rasterizationOptions.Resolution = 300;` (ou le DPI souhaité) avant l’exportation. |

## Questions fréquemment posées

**Q : Puis‑je exporter plusieurs mises en page simultanément ?**  
A : Oui, il suffit de modifier le tableau `Layouts` à l’étape 3 pour inclure tous les noms de mises en page souhaités, par ex., `new string[] { "Layout1", "Layout2" }`.

**Q : Aspose.CAD est‑il compatible avec d’autres formats de fichiers CAD ?**  
A : Absolument. Il prend en charge DWG, DXF, DWF, DGN et de nombreux autres formats.

**Q : Comment puis‑je ajuster les paramètres de sortie PDF au‑delà de la taille de la page ?**  
A : Explorez les propriétés supplémentaires de `CadRasterizationOptions` telles que `Resolution`, `BackgroundColor` et `DrawType` pour affiner le résultat.

**Q : Où puis‑je trouver de la documentation supplémentaire sur Aspose.CAD ?**  
A : Visitez la [documentation](https://reference.aspose.com/cad/net/) pour des références API détaillées et des exemples.

**Q : Un essai gratuit est‑il disponible ?**  
A : Oui, vous pouvez accéder à l’essai gratuit [ici](https://releases.aspose.com/).

## Conclusion

Vous avez maintenant appris comment **définir les options de rasterisation CAD** et les utiliser pour **exporter des mises en page DWG spécifiques vers PDF** avec Aspose.CAD pour .NET. Cette approche vous offre un contrôle précis du processus de conversion, vous permettant d’intégrer rapidement et de manière fiable la fonctionnalité CAD‑vers‑PDF dans n’importe quelle application C#.

---

**Dernière mise à jour :** 2026-03-13  
**Testé avec :** Aspose.CAD 24.11 for .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}