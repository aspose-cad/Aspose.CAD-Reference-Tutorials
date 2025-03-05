---
title: Conversion de DWG en PDF avec des coordonnées en C# - Tutoriel Aspose.CAD
linktitle: Conversion de DWG en PDF avec des coordonnées en C#
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez comment convertir un DWG en PDF avec des coordonnées spécifiques en C# à l'aide d'Aspose.CAD. Suivez notre guide étape par étape pour des conversions de fichiers CAO précises et efficaces.
type: docs
weight: 11
url: /fr/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---
## Introduction

Bienvenue dans ce didacticiel complet sur la conversion de fichiers DWG en PDF avec des coordonnées spécifiées à l'aide d'Aspose.CAD pour .NET. Aspose.CAD est une bibliothèque puissante qui permet aux développeurs de travailler de manière transparente avec les formats de fichiers CAO dans leurs applications .NET. Dans ce didacticiel, nous vous guiderons tout au long du processus de conversion d'un fichier DWG en PDF tout en fournissant des coordonnées spécifiques pour améliorer la précision.

## Conditions préalables

Avant de commencer, assurez-vous d'avoir les prérequis suivants :

- Bibliothèque Aspose.CAD : téléchargez et installez la bibliothèque Aspose.CAD pour .NET. Vous pouvez trouver la bibliothèque[ici](https://releases.aspose.com/cad/net/).

- Environnement de développement : assurez-vous que vous disposez d'un environnement de développement compatible, y compris Visual Studio ou tout autre IDE préféré.

- Fichier DWG : préparez un fichier DWG pour la conversion. Vous pouvez utiliser le fichier d'exemple fourni ou votre fichier DWG personnalisé.

## Importer des espaces de noms

Dans votre projet C#, importez les espaces de noms nécessaires :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Décomposons le code en un guide étape par étape pour une meilleure compréhension :

## Étape 1 : Définir le répertoire des documents

```csharp
string MyDir = "Your Document Directory";
```

## Étape 2 : définir le chemin du fichier DWG source

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Étape 3 : charger le fichier DWG et configurer les options de rastérisation

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Étape 4 : Définir les coordonnées et la fenêtre

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Étape 5 : appliquer les paramètres de la fenêtre

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Étape 6 : Configurer les options PDF et exporter

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Étape 7 : Afficher le message de réussite

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusion

Toutes nos félicitations! Vous avez converti avec succès un fichier DWG en PDF avec les coordonnées spécifiées à l'aide d'Aspose.CAD pour .NET. Ce didacticiel couvrait les étapes essentielles et fournissait un guide clair aux développeurs.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD avec d’autres formats de fichiers CAO ?

A1 : Oui, Aspose.CAD prend en charge divers formats de CAO, notamment DWG, DXF, DWF, etc.

### Q2 : Comment puis-je gérer les erreurs pendant le processus de conversion ?

A2 : implémentez des mécanismes de gestion des erreurs à l'aide de blocs try-catch pour capturer et gérer les exceptions.

### Q3 : Aspose.CAD est-il adapté aux environnements Windows et Linux ?

A3 : Oui, Aspose.CAD est compatible avec les plateformes Windows et Linux.

### Q4 : Puis-je personnaliser davantage la sortie PDF ?

A4 : Certainement ! Explorez les nombreuses options fournies par Aspose.CAD pour adapter la sortie PDF à vos besoins spécifiques.

### Q5 : Où puis-je trouver une assistance supplémentaire ou des discussions communautaires ?

A5 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien et les discussions de la communauté.