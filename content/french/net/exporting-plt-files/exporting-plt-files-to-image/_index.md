---
title: Exporter des fichiers PLT vers une image - Tutoriel Aspose.CAD
linktitle: Exportation de fichiers PLT vers une image
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Convertissez sans effort des fichiers PLT en images à l'aide d'Aspose.CAD pour .NET. Explorez des options flexibles et une intégration transparente pour vos besoins en matière de manipulation de fichiers CAO.
type: docs
weight: 10
url: /fr/net/exporting-plt-files/exporting-plt-files-to-image/
---
## Introduction

Bienvenue dans ce didacticiel complet sur l'exportation de fichiers PLT vers des images à l'aide d'Aspose.CAD pour .NET ! Si vous cherchez à convertir de manière transparente des fichiers PLT en différents formats d'image, vous êtes au bon endroit. Aspose.CAD pour .NET offre des fonctionnalités puissantes et une flexibilité pour une manipulation efficace des fichiers CAO. Dans ce didacticiel, nous vous guiderons pas à pas tout au long du processus.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.CAD pour .NET : assurez-vous que la bibliothèque Aspose.CAD est installée. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/cad/net/).

-  Répertoire de documents : créez un répertoire pour vos documents et notez son chemin. Ceci sera appelé`MyDir` dans les exemples de code.

Maintenant, commençons par le didacticiel.

## Importer des espaces de noms

Commencez par importer les espaces de noms nécessaires dans votre projet .NET pour accéder à la fonctionnalité Aspose.CAD. Ajoutez les lignes suivantes au début de votre code :

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

## Étape 1 : Charger le fichier PLT

```csharp
string sourceFilePath = MyDir + "50states.plt";

using (Image cadImage = Image.Load(sourceFilePath))
{
    // Votre code pour les étapes suivantes ira ici.
}
```

 Dans cette étape, nous chargeons le fichier PLT en utilisant le`Image.Load` méthode fournie par Aspose.CAD.

## Étape 2 : configurer les options d'exportation d'images

```csharp
ImageOptionsBase imageOptions = new JpegOptions();
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 500,
    PageWidth = 1000,
    // Ajoutez des options supplémentaires si nécessaire.
};
imageOptions.VectorRasterizationOptions = options;
```

 Ici, nous configurons les options d'exportation d'images. Dans cet exemple, nous utilisons JpegOptions, mais vous pouvez choisir d'autres formats en fonction de vos besoins. Ajuste le`PageHeight` et`PageWidth` selon les besoins de votre image de sortie.

## Étape 3 : Enregistrez l'image

```csharp
cadImage.Save(MyDir + "50states.jpg", imageOptions);
```

 Enfin, enregistrez l'image convertie à l'aide du`Save` méthode, en spécifiant le chemin de sortie et les options d’image précédemment configurées.

Répétez ces étapes pour d'autres fichiers PLT ou personnalisez les options en fonction de vos besoins spécifiques.

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment exporter des fichiers PLT vers des images à l'aide d'Aspose.CAD pour .NET. Cette puissante bibliothèque offre flexibilité et efficacité pour la manipulation de fichiers CAO, ce qui en fait un outil précieux pour vos projets.

## FAQ

### Q1 : Puis-je exporter des fichiers PLT vers des formats autres que JPEG ?

A1 : Absolument ! Vous pouvez choisir parmi différents formats d'image pris en charge par Aspose.CAD, tels que PNG, GIF, BMP, etc.

### Q2 : Comment puis-je personnaliser les options de rastérisation pour plus de contrôle ?

 A2 : Ajustez simplement les propriétés du`CadRasterizationOptions` classe à l’étape 2 pour adapter le résultat à vos besoins spécifiques.

### Q3 : Existe-t-il une version d'essai disponible ?

 A3 : Oui, vous pouvez explorer les capacités d'Aspose.CAD en obtenant un essai gratuit[ici](https://releases.aspose.com/).

### Q4 : Où puis-je trouver une documentation détaillée ?

 A4 : La documentation complète est disponible[ici](https://reference.aspose.com/cad/net/).

### Q5 : Besoin d'aide ou avez des questions ?

 A5 : Visitez notre communauté[forum](https://forum.aspose.com/c/cad/19) pour du soutien et des discussions.
