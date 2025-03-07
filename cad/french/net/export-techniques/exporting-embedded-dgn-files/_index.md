---
title: Exporter des fichiers DGN intégrés - Tutoriel Aspose.CAD
linktitle: Exportation de fichiers DGN intégrés
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez la puissance d'Aspose.CAD pour .NET. Apprenez à exporter des fichiers DGN intégrés au format PDF sans effort grâce à ce didacticiel étape par étape.
weight: 14
url: /fr/net/export-techniques/exporting-embedded-dgn-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter des fichiers DGN intégrés - Tutoriel Aspose.CAD

## Introduction

Dans le monde dynamique du développement de logiciels, Aspose.CAD for .NET s'impose comme un outil puissant pour gérer les fichiers de conception assistée par ordinateur (CAO). Ce didacticiel vous guidera tout au long du processus d'exportation de fichiers DGN intégrés à l'aide d'Aspose.CAD pour .NET. Que vous soyez un développeur chevronné ou un débutant curieux, ce guide étape par étape vous aidera à exploiter efficacement les capacités d'Aspose.CAD.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

1.  Aspose.CAD pour .NET : téléchargez et installez la bibliothèque à partir de[Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).

2. Environnement de développement : configurez un environnement de développement .NET avec Visual Studio ou tout autre IDE préféré.

3. Exemple de fichier DXF : pour ce didacticiel, nous utiliserons le fichier "conic_pyramid.dxf". Assurez-vous de l'avoir disponible dans votre répertoire de documents désigné.

## Importer des espaces de noms

Dans votre code C#, assurez-vous d'importer les espaces de noms nécessaires :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Étape 1 : Charger le fichier DXF

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //Votre code pour les étapes ultérieures sera ici
}
```

## Étape 2 : définir les options de rastérisation

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## Étape 3 : Définir les options PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 4 : Enregistrer au format PDF

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## Étape 5 : Afficher le message de réussite

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## Conclusion

Toutes nos félicitations! Vous avez exporté avec succès un fichier DGN intégré au format PDF à l'aide d'Aspose.CAD pour .NET. Ce didacticiel a couvert les étapes essentielles, vous fournissant une base pour explorer les fonctionnalités plus avancées offertes par Aspose.CAD.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour .NET avec d’autres langages de programmation ?

A1 : Aspose.CAD prend principalement en charge .NET, mais Aspose fournit des bibliothèques pour divers langages, notamment Java et Python.

### Q2 : Existe-t-il un essai gratuit disponible pour Aspose.CAD pour .NET ?

 A2 : Oui, vous pouvez bénéficier d'un essai gratuit auprès de[ici](https://releases.aspose.com/).

### Q3 : Où puis-je trouver une documentation complète pour Aspose.CAD pour .NET ?

 A3 : Se référer à la documentation[ici](https://reference.aspose.com/cad/net/).

### Q4 : Comment puis-je obtenir une licence temporaire pour Aspose.CAD pour .NET ?

 A4 : Obtenir un permis temporaire[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Besoin d'aide ou souhaitez-vous vous engager auprès de la communauté ?

A5 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour du soutien et des discussions.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
