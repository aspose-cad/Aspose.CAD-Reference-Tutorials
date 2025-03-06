---
title: Exporter des mises en page CAO vers des formats d'image raster dans Aspose.CAD pour .NET
linktitle: Exporter des mises en page CAO vers des formats d'image raster
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez comment exporter des mises en page CAO vers des images raster à l'aide d'Aspose.CAD pour .NET. Suivez notre guide étape par étape pour une conversion transparente.
weight: 10
url: /fr/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter des mises en page CAO vers des formats d'image raster dans Aspose.CAD pour .NET

## Introduction

Cherchez-vous à convertir efficacement des mises en page CAO en formats d'image raster à l'aide d'Aspose.CAD pour .NET ? Ce guide étape par étape vous guidera tout au long du processus, en fournissant des instructions détaillées et des extraits de code pour rendre la tâche transparente. Que vous soyez un développeur chevronné ou un nouveau venu sur Aspose.CAD, ce tutoriel s'adresse à tous les niveaux d'expertise.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir les éléments suivants :

- Bibliothèque Aspose.CAD pour .NET : assurez-vous que la bibliothèque Aspose.CAD est installée. Sinon, vous pouvez le télécharger depuis le[Site Web Aspose.CAD](https://releases.aspose.com/cad/net/).

- Fichier de dessin CAO : préparez un fichier de dessin CAO (par exemple, conic_pyramid.dxf) que vous souhaitez convertir aux formats d'image raster.

## Importer des espaces de noms

Dans votre projet .NET, importez les espaces de noms nécessaires pour exploiter les fonctionnalités d'Aspose.CAD. Incluez les espaces de noms suivants au début de votre code :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Étape 1 : Charger le dessin CAO

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Charger un dessin CAO dans une instance d'Image
using (var image = Image.Load(sourceFilePath))
{
    // Votre code pour charger le dessin CAO va ici
}
```

## Étape 2 : Créer des options de cadrastérisation

```csharp
// Créer une instance de CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Étape 3 : Spécifier les calques

```csharp
// Ajoutez le nom du calque à la liste des calques de CadRasterizationOptions
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Étape 4 : Créer des options Jpeg

```csharp
// Créez une instance de JpegOptions (ou de n'importe quelle ImageOptions pour les formats raster)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 5 : Exporter au format Jpeg

```csharp
// Exporter chaque calque au format Jpeg
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Étape supplémentaire : convertir tous les calques

Si vous souhaitez convertir tous les calques, utilisez la méthode suivante :

```csharp
ConvertAllLayersToRasterImageFormats();
```

Cette méthode parcourt tous les calques du dessin CAO, exportant chaque calque vers un fichier Jpeg distinct.

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment exporter des mises en page CAO vers des formats d'image raster à l'aide d'Aspose.CAD pour .NET. Ce didacticiel fournit un guide complet aux développeurs recherchant des solutions efficaces et fiables pour la conversion CAO.

## FAQ

### Q1 : Puis-je utiliser d’autres formats d’image pour l’exportation ?

 A1 : Oui, vous pouvez. Remplacez simplement`JpegOptions` avec les options du format souhaité, telles que`PngOptions` ou`BmpOptions`.

### Q2 : Existe-t-il une version d'essai disponible ?

 A2 : Oui, vous pouvez explorer les fonctionnalités d'Aspose.CAD en téléchargeant la version d'essai[ici](https://releases.aspose.com/).

### Q3 : Comment puis-je obtenir de l'aide pour Aspose.CAD ?

 A3 : Visitez Aspose.CAD[forum](https://forum.aspose.com/c/cad/19) pour le support de la communauté ou envisagez d'acheter une licence pour un support dédié.

### Q4 : Des licences temporaires sont-elles disponibles ?

 A4 : Oui, vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis-je trouver la documentation ?

 A5 : Reportez-vous à la documentation détaillée[ici](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
