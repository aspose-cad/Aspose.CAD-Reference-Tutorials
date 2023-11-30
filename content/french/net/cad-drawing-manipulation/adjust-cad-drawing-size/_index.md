---
title: Ajustement de la taille du dessin CAO dans Aspose.CAD pour .NET
linktitle: Ajustement de la taille du dessin CAO
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez comment ajuster sans effort les tailles des dessins CAO dans .NET à l'aide d'Aspose.CAD. Suivez notre guide étape par étape pour un redimensionnement fluide.
type: docs
weight: 10
url: /fr/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## Introduction

Cherchez-vous à ajuster de manière transparente la taille des dessins CAO dans vos applications .NET ? Aspose.CAD pour .NET fournit une solution robuste, vous permettant de gérer sans effort le redimensionnement des dessins CAO. Dans ce didacticiel, nous vous guiderons tout au long du processus, en décomposant chaque étape pour vous assurer de comprendre les subtilités du redimensionnement des dessins CAO à l'aide d'Aspose.CAD.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Aspose.CAD for .NET Library : téléchargez et installez la bibliothèque à partir du[Page de téléchargement d'Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).
- Exemple de dessin CAO : assurez-vous d'avoir un exemple de fichier de dessin CAO (par exemple, "sample.dwg") dans votre répertoire de documents.

## Importer des espaces de noms

Commencez par importer les espaces de noms nécessaires dans votre application .NET. Cette étape est cruciale pour accéder aux fonctionnalités fournies par Aspose.CAD for .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Étape 1 : Charger le dessin CAO

Commencez par charger le dessin CAO dans une instance de la classe Aspose.CAD.Image. Assurez-vous que vous disposez du chemin de fichier correct pour votre exemple de dessin.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Charger un dessin CAO dans une instance d'Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Votre code ici...
}
```

## Étape 2 : Créer des options Bmp

Créez une instance de la classe BmpOptions, chargée de spécifier les options lors de l'enregistrement du dessin CAO en tant que fichier BMP.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Étape 3 : Définir les options de CadRasterization

Instanciez la classe CadRasterizationOptions et configurez ses propriétés pour la rastérisation vectorielle.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Étape 4 : Définir la propriété UnitType

Définissez la propriété UnitType de CadRasterizationOptions pour spécifier le type d'unité à redimensionner. Dans cet exemple, il est défini sur Centimètre.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Étape 5 : Définir la propriété des mises en page

Spécifiez les présentations que vous souhaitez inclure dans le dessin redimensionné en définissant la propriété Layouts.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Étape 6 : Exporter vers BMP

Enfin, enregistrez la mise en page redimensionnée sous forme de fichier BMP à l'aide de la méthode Save.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Vous avez maintenant réussi à ajuster la taille de votre dessin CAO à l'aide d'Aspose.CAD pour .NET !

## Conclusion

Dans ce didacticiel, nous avons parcouru le processus de redimensionnement des dessins CAO dans .NET à l'aide d'Aspose.CAD. En suivant ces étapes, vous pouvez intégrer de manière transparente cette fonctionnalité dans vos applications, offrant ainsi une expérience utilisateur fluide.

## FAQ

### Q1 : Aspose.CAD pour .NET est-il compatible avec tous les formats de CAO ?

 A1 : Aspose.CAD pour .NET prend en charge un large éventail de formats de CAO, notamment DWG, DXF, DWF, etc. Vérifier la[Documentation](https://reference.aspose.com/cad/net/) pour la liste complète.

### Q2 : Puis-je redimensionner plusieurs mises en page simultanément ?

A2 : Oui, vous pouvez redimensionner plusieurs mises en page en ajustant le tableau des mises en page dans CadRasterizationOptions.

### Q3 : Où puis-je obtenir de l'assistance pour Aspose.CAD pour .NET ?

 A3 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien et l’assistance de la communauté.

### Q4 : Existe-t-il un essai gratuit ?

 A4 : Oui, vous pouvez explorer un[essai gratuit](https://releases.aspose.com/) pour évaluer les fonctionnalités d'Aspose.CAD pour .NET.

### Q5 : Comment puis-je obtenir une licence temporaire pour Aspose.CAD pour .NET ?

 A5 : Obtenir une licence temporaire à des fins de test[ici](https://purchase.aspose.com/temporary-license/).