---
title: Point de vue gratuit dans les dessins CAO - Guide Aspose.CAD
linktitle: Point de vue gratuit dans les dessins CAO
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Explorez la liberté de la visualisation CAO avec Aspose.CAD pour .NET. Suivez notre guide étape par étape pour un point de vue unique.
weight: 11
url: /fr/net/advanced-cad-techniques/free-point-of-view-in-cad-drawings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Point de vue gratuit dans les dessins CAO - Guide Aspose.CAD

Dans le domaine de la conception assistée par ordinateur (CAO), obtenir un point de vue libre dans les dessins est un aspect crucial de la visualisation et de la présentation de conceptions complexes. Aspose.CAD for .NET fournit une solution robuste pour atteindre cette liberté, permettant aux utilisateurs de manipuler et d'optimiser facilement les dessins CAO. Dans ce guide étape par étape, nous explorerons le processus d'obtention d'un point de vue gratuit dans les dessins CAO à l'aide d'Aspose.CAD pour .NET.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

1. Installation d'Aspose.CAD
 Assurez-vous que Aspose.CAD pour .NET est installé dans votre environnement de développement. Sinon, vous pouvez le télécharger depuis le[Site Web Aspose.CAD](https://releases.aspose.com/cad/net/).

2. Fichier de dessin CAO
Préparez un fichier de dessin CAO que vous souhaitez manipuler. Pour ce guide, nous utiliserons un exemple de fichier nommé « conic_pyramid.dxf ».

3. Environnement de développement
Disposez d'un environnement de développement .NET fonctionnel configuré avec Visual Studio ou tout autre IDE préféré.

## Importer des espaces de noms

Dans votre projet .NET, importez les espaces de noms nécessaires à la fonctionnalité Aspose.CAD. Ajoutez l'extrait de code suivant en haut de votre fichier :

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```


## Étape 1 : Définir le répertoire des documents

```csharp
// Le chemin d'accès au répertoire des documents.
string MyDir = "Your Document Directory";
```

Assurez-vous de remplacer « Votre répertoire de documents » par le chemin réel d'accès à votre répertoire de documents.

## Étape 2 : Spécifier le fichier source

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

Indiquez le chemin d'accès à votre fichier de dessin CAO.

## Étape 3 : Définir le chemin de sortie

```csharp
var outPath = Path.Combine(MyDir, "FreePointOfView_out.jpg");
```

Définissez le chemin où le dessin CAO manipulé sera enregistré.

## Étape 4 : Charger l'image CAO

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
```

Chargez le dessin CAO à l'aide d'Aspose.CAD.

## Étape 5 : Configurer les options JPEG

```csharp
JpegOptions options = new JpegOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500, PageHeight = 1500
    }
};
```

Configurez les options d'exportation du dessin CAO au format JPEG.

## Étape 6 : Définir les angles de rotation

```csharp
float xAngle = 10; //Angle de rotation le long de l'axe X
float yAngle = 30; //Angle de rotation le long de l'axe Y
float zAngle = 40; //Angle de rotation le long de l'axe Z
((CadRasterizationOptions)(options.VectorRasterizationOptions)).ObserverPoint = new ObserverPoint(xAngle, yAngle, zAngle);
```

Spécifiez les angles de rotation le long des axes X, Y et Z pour obtenir le point de vue souhaité.

## Étape 7 : Enregistrez le dessin CAO manipulé

```csharp
cadImage.Save(outPath, options);
}
```

Enregistrez le dessin CAO manipulé dans le chemin de sortie spécifié.

## Étape 8 : Afficher le message de réussite

```csharp
Console.WriteLine("\n3D images exported successfully to JPEG.\nFile saved at " + outPath);
```

Informez l'utilisateur de l'exportation réussie de l'image 3D.

## Conclusion

Dans ce didacticiel, nous avons exploré le processus d'obtention d'un point de vue gratuit dans les dessins CAO à l'aide d'Aspose.CAD pour .NET. En suivant ces instructions étape par étape, vous pouvez améliorer vos capacités de visualisation CAO et présenter vos conceptions avec une nouvelle perspective.


## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour .NET avec d’autres formats de fichiers CAO ?

A1 : Oui, Aspose.CAD pour .NET prend en charge divers formats de fichiers CAO, notamment DWG et DXF.

### Q2 : Existe-t-il une version d’essai d’Aspose.CAD disponible ?

 A2 : Oui, vous pouvez télécharger une version d'essai gratuite à partir de[ici](https://releases.aspose.com/).

### Q3 : Comment puis-je obtenir une licence temporaire pour Aspose.CAD ?

 A3 : Vous pouvez acquérir une licence temporaire auprès de[ici](https://purchase.aspose.com/temporary-license/).

### Q4 : Où puis-je trouver une assistance supplémentaire pour Aspose.CAD ?

 A4 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien et les discussions de la communauté.

### Q5 : Puis-je personnaliser les options d'exportation pour différents formats d'image ?

A5 : Certainement ! Aspose.CAD propose une gamme d'options de personnalisation, vous permettant d'adapter le processus d'exportation à vos besoins spécifiques.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
