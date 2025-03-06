---
title: Exporter DGN au format PDF dans Aspose.CAD pour .NET
linktitle: Exporter DGN au format PDF
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Apprenez à exporter des fichiers DGN au format PDF sans effort avec Aspose.CAD pour .NET. Un guide étape par étape pour une manipulation transparente des fichiers CAO.
weight: 12
url: /fr/net/cad-export-formats/export-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter DGN au format PDF dans Aspose.CAD pour .NET

## Introduction

Dans le monde du développement .NET, Aspose.CAD est une bibliothèque puissante qui facilite la manipulation et la conversion des fichiers CAO. Une tâche courante que les développeurs rencontrent souvent consiste à exporter des fichiers DGN au format PDF. Dans ce didacticiel, nous allons parcourir le processus étape par étape, en utilisant Aspose.CAD pour .NET.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous d'avoir mis en place les éléments suivants :

- Une connaissance pratique de C# et du framework .NET.
-  Aspose.CAD pour la bibliothèque .NET installée. Vous pouvez le télécharger[ici](https://releases.aspose.com/cad/net/).
- Un exemple de fichier DGN, par exemple « Nikon_D90_Camera.dgn » pour ce didacticiel.

## Importer des espaces de noms

Dans votre projet C#, commencez par importer les espaces de noms nécessaires :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Étape 1 : Charger le fichier DGN

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Votre code ici...
}
```

## Étape 2 : configurer les options de rastérisation

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Étape 3 : Créer des options PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 4 : Enregistrer au format PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## Conclusion

Toutes nos félicitations! Vous avez exporté avec succès un fichier DGN au format PDF à l'aide d'Aspose.CAD pour .NET. Ce didacticiel a couvert les étapes essentielles, du chargement du fichier DGN à la configuration des options de rastérisation et à l'enregistrement de la sortie au format PDF.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour .NET sans connaissances préalables en CAO ?

A1 : Absolument ! Aspose.CAD simplifie les tâches de CAO complexes, les rendant accessibles aux développeurs d'horizons divers.

### Q2 : Où puis-je trouver plus d’exemples et de documentation pour Aspose.CAD ?

 A2 : Explorez le[Documentation](https://reference.aspose.com/cad/net/) pour des guides et des exemples complets.

### Q3 : Existe-t-il un essai gratuit disponible pour Aspose.CAD ?

A3 : Oui, vous pouvez bénéficier d'un essai gratuit[ici](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir des licences temporaires pour Aspose.CAD ?

 A4 : Obtenir des licences temporaires[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Besoin d'aide ou avez des questions ?

A5 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien de la communauté.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
