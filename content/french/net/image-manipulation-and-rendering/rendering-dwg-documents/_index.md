---
title: Rendu de documents DWG en C# - Guide Aspose.CAD
linktitle: Rendu de documents DWG en C#
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez comment restituer des documents DWG en C# à l'aide d'Aspose.CAD. Ce guide étape par étape couvre l'importation, la configuration et l'enregistrement avec des exemples de code.
type: docs
weight: 17
url: /fr/net/image-manipulation-and-rendering/rendering-dwg-documents/
---
## Introduction

Bienvenue dans le guide complet sur le rendu des documents DWG en C# à l'aide d'Aspose.CAD. Que vous soyez un développeur chevronné ou que vous débutiez tout juste avec .NET, ce didacticiel vous guidera tout au long du processus d'exploitation d'Aspose.CAD pour restituer efficacement les fichiers DWG. Aspose.CAD est une API puissante qui fournit des fonctionnalités robustes pour travailler avec des formats de fichiers CAO, ce qui en fait un choix incontournable pour les développeurs travaillant avec des fichiers DWG.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous de disposer des prérequis suivants :

- Connaissance de base du langage de programmation C#.
- Visual Studio installé sur votre ordinateur.
-  Bibliothèque Aspose.CAD intégrée à votre projet. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/cad/net/).
- Un exemple de fichier DWG, tel que « Bottom_plate.dwg », à suivre avec les exemples.

## Importer des espaces de noms

Pour commencer, assurez-vous d'importer les espaces de noms nécessaires au début de votre code C# :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Maintenant, décomposons l'exemple fourni en plusieurs étapes :

## Étape 1 : Charger le fichier DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //Votre code pour charger le fichier DWG va ici.
}
```

## Étape 2 : configurer les options de rastérisation

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Des configurations de rastérisation supplémentaires peuvent être ajoutées ici.
```

## Étape 3 : Définir la région à dessiner

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Étape 4 : Créer une nouvelle fenêtre

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Étape 5 : Remplacer la fenêtre active

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Étape 6 : Configurer les options PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 7 : Enregistrez le DWG rendu au format PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Conclusion

Toutes nos félicitations! Vous avez réussi le rendu d'un document DWG au format PDF à l'aide d'Aspose.CAD en C#. N'hésitez pas à explorer plus de fonctionnalités et à personnaliser le code en fonction de vos besoins spécifiques.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD avec d’autres formats de fichiers CAO ?

A1 : Oui, Aspose.CAD prend en charge divers formats de CAO, notamment DWG, DXF, DWF, etc.

### Q2 : Aspose.CAD est-il compatible avec .NET Core ?

A2 : Oui, Aspose.CAD est compatible avec .NET Framework et .NET Core.

### Q3 : Comment puis-je gérer différentes mises en page dans un fichier DWG ?

 A3 : Vous pouvez spécifier la disposition souhaitée dans le`Layouts` propriété de`CadRasterizationOptions`.

### Q4 : Y a-t-il des considérations en matière de licence pour l'utilisation d'Aspose.CAD ?

 A4 : Pour plus de détails sur la licence, visitez[ici](https://purchase.aspose.com/buy).

### Q5 : Où puis-je trouver une assistance supplémentaire ?

 A5 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien et les discussions de la communauté.