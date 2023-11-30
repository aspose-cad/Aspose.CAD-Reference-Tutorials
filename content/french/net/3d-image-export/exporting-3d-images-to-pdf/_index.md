---
title: Exporter des images 3D au format PDF - Tutoriel Aspose.CAD
linktitle: Exportation d'images 3D au format PDF
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Convertissez sans effort des images CAO 3D en PDF avec Aspose.CAD pour .NET. Suivez notre didacticiel étape par étape pour une exportation PDF transparente.
type: docs
weight: 10
url: /fr/net/3d-image-export/exporting-3d-images-to-pdf/
---
## Introduction

Cherchez-vous à exporter de manière transparente des images 3D au format PDF à l’aide d’Aspose.CAD pour .NET ? Ce didacticiel étape par étape vous guidera tout au long du processus, garantissant que vous exploitez la puissance d'Aspose.CAD pour convertir sans effort vos images 3D au format PDF.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.CAD pour .NET : assurez-vous que la bibliothèque Aspose.CAD pour .NET est installée. Sinon, vous pouvez le télécharger depuis le[Page de téléchargement d'Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).

- Répertoire de documents : créez un répertoire dans lequel vos fichiers CAO sont stockés et notez le chemin.

## Importer des espaces de noms

Dans votre projet .NET, importez les espaces de noms nécessaires pour travailler avec Aspose.CAD. Ajoutez les lignes suivantes en haut de votre fichier de code :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Étape 1 : Charger l'image CAO

 Commencez par charger l'image CAO que vous souhaitez exporter au format PDF. Utilisez le`Load` méthode de la bibliothèque Aspose.CAD. Remplacer`"conic_pyramid.dxf"` avec le chemin d'accès à votre fichier CAO.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Votre code pour charger l'image CAO va ici
}
```

## Étape 2 : configurer les options de rastérisation

 Configurez les options de rastérisation pour l'image CAO. Définissez des paramètres tels que la largeur de la page, la hauteur de la page et les mises en page. Décommentez la ligne relative à`TypeOfEntities` si vos entités sont en 3D.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
//rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## Étape 3 : Définir les options PDF

Créez des options PDF et associez-les aux options de rastérisation.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 4 : Enregistrer au format PDF

Enregistrez l'image CAO sous forme de fichier PDF à l'aide des options configurées. Spécifiez le chemin de sortie du fichier PDF.

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Conclusion

Toutes nos félicitations! Vous avez exporté avec succès des images 3D au format PDF à l'aide d'Aspose.CAD pour .NET. Ce didacticiel simple garantit que vous convertissez sans effort vos fichiers CAO dans un format plus accessible.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec tous les formats de fichiers CAO ?

A1 : Oui, Aspose.CAD prend en charge une large gamme de formats CAO, garantissant une flexibilité dans la gestion de différents types de fichiers.

### Q2 : Puis-je personnaliser les dimensions de la page lors de l'exportation au format PDF ?

A2 : Absolument. Le didacticiel montre comment configurer la largeur et la hauteur de la page en fonction de vos besoins.

### Q3 : Des licences temporaires sont-elles disponibles pour Aspose.CAD ?

A3 : Oui, vous pouvez obtenir des licences temporaires pour Aspose.CAD en visitant[Permis temporaire](https://purchase.aspose.com/temporary-license/).

### Q4 : Où puis-je trouver une assistance supplémentaire ou des discussions communautaires ?

 A4 : Dirigez-vous vers le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien et l’engagement avec la communauté.

### Q5 : Existe-t-il une version d’essai gratuite d’Aspose.CAD disponible ?

 A5 : Oui, vous pouvez explorer les fonctionnalités d'Aspose.CAD en accédant au[essai gratuit](https://releases.aspose.com/).