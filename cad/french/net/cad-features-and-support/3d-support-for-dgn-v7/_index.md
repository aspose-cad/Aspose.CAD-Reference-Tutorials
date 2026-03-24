---
date: 2026-03-24
description: Apprenez à convertir les fichiers DGN en PDF (et PNG) avec prise en charge
  3D pour DGN V7 en utilisant Aspose.CAD pour .NET – guide étape par étape.
linktitle: 3D Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Convertir DGN en PDF (prise en charge 3D) avec Aspose.CAD pour .NET
url: /fr/net/cad-features-and-support/3d-support-for-dgn-v7/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DGN en PDF (prise en charge 3D) avec Aspose.CAD pour .NET

## Introduction

Dans les flux de travail CAD modernes, pouvoir **convertir DGN en PDF** rapidement et conserver la géométrie 3‑D est essentiel. Que vous génériez de la documentation, partagiez des conceptions avec des parties prenantes non‑CAD ou archiviez des projets, Aspose.CAD pour .NET vous offre une méthode fiable pour transformer les fichiers DGN V7 en PDF de haute qualité (et même en PNG). Dans ce tutoriel, nous parcourrons les étapes exactes nécessaires pour activer la prise en charge 3D et produire un PDF à partir d’un fichier DGN.

## Quick Answers
- **Que couvre le tutoriel ?** Activation de la prise en charge 3D et conversion de DGN V7 en PDF avec Aspose.CAD pour .NET.  
- **Quel format principal est produit ?** PDF (avec exportation PNG en option).  
- **Ai‑je besoin d’une licence ?** Une version d’essai gratuite suffit pour les tests ; une licence commerciale est requise en production.  
- **Versions .NET prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Combien de temps prend l’implémentation ?** Environ 10‑15 minutes pour une conversion de base.

## Qu’est‑ce que « convert DGN to PDF » ?

Convertir DGN en PDF signifie rendre les données vectorielles stockées dans un fichier MicroStation DGN sous forme de document portable pouvant être visualisé sur n’importe quel appareil sans logiciel CAD spécialisé. Avec le moteur de rasterisation 3‑D d’Aspose.CAD, la conversion conserve la mise en page, les couleurs et les indications de profondeur, offrant une représentation visuelle fidèle.

## Pourquoi utiliser Aspose.CAD pour cette conversion ?

- **Rasterisation 3‑D complète** – conserve les informations de profondeur et de mise en page.  
- **Aucune dépendance externe** – bibliothèque pure .NET, aucune nécessité de MicroStation.  
- **Multiples formats de sortie** – PDF, PNG, JPEG, TIFF, etc. (le mot‑clé secondaire *convert dgn to png* est supporté immédiatement).  
- **Cross‑platform** – fonctionne sous Windows, Linux et macOS.

## Prérequis

Avant de commencer, assurez‑vous de disposer de :

- Aspose.CAD pour .NET installé. Vous pouvez le télécharger depuis la [page de téléchargement Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).  
- Un fichier DGN V7 valide que vous souhaitez traiter.  
- Un environnement de développement .NET (Visual Studio, VS Code ou la CLI). Les instructions d’installation sont disponibles dans la [documentation .NET](https://docs.microsoft.com/en-us/dotnet/core/install/).

## Import Namespaces

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Ces espaces de noms vous donnent accès aux classes principales d’Aspose.CAD et aux utilitaires .NET standards.

## Step 1: Set up the Environment

Définissez où se trouve votre fichier DGN source et où le PDF de sortie doit être enregistré.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

> **Astuce :** Utilisez `Path.Combine` pour une construction de chemin indépendante de la plateforme.

## Step 2: Load the DGN File

Créez une instance `DgnImage` en chargeant le fichier avec `Image.Load`. Cette étape prépare les données CAD pour la rasterisation.

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Code snippet continues...
}
```

## Step 3: Configure Export Options

Configurez `PdfOptions` avec `CadRasterizationOptions`. Vous contrôlez ici la taille de la page, l’arrière‑plan et les mises en page (vues) à exporter.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Export specific views
    }
};
```

Si vous devez **convertir DGN en PNG** à la place, remplacez simplement `PdfOptions` par `PpngOptions` tout en conservant les mêmes paramètres de rasterisation.

## Step 4: Save the Result

Enfin, écrivez la sortie rendue à l’emplacement souhaité.

```csharp
string outFile = "Your Output Directory"; // Specify the output directory
dgnImage.Save(outFile, options);
```

Après exécution, vous trouverez un fichier PDF (ou PNG si vous avez modifié les options) qui représente fidèlement le dessin DGN 3‑D original.

## Common Issues & Tips

- **Mises en page manquantes :** Assurez‑vous que les noms de mise en page dans `Layouts` correspondent à ceux du fichier DGN ; sinon ils seront ignorés.  
- **Fichiers volumineux :** Augmentez progressivement `PageWidth`/`PageHeight` pour éviter une consommation mémoire excessive.  
- **Précision des couleurs :** Si l’arrière‑plan apparaît sombre, vérifiez que `BackgroundColor` est réglé sur la valeur souhaitée (par ex., `Color.White`).

## Conclusion

Vous avez maintenant maîtrisé comment **convertir DGN en PDF** avec prise en charge complète 3‑D en utilisant Aspose.CAD pour .NET. Ce flux de travail peut être intégré à des pipelines automatisés, des utilitaires de bureau ou des services web afin de fournir des visualisations CAD à tout public.

## FAQ's

### Q1 : Puis‑je traiter plusieurs fichiers DGN simultanément avec cette approche ?

R1 : Oui, vous pouvez modifier le code pour gérer plusieurs fichiers dans une boucle ou dans le cadre d’un système de traitement par lots.

### Q2 : Quels autres formats d’exportation sont pris en charge par Aspose.CAD pour .NET ?

R2 : Aspose.CAD pour .NET prend en charge divers formats d’exportation, dont PDF, PNG, JPG et bien d’autres. Consultez la [documentation](https://reference.aspose.com/cad/net/) pour plus de détails.

### Q3 : Aspose.CAD pour .NET est‑il compatible avec les dernières versions de .NET Core ?

R3 : Oui, Aspose.CAD pour .NET est conçu pour être compatible avec les dernières versions de .NET Core. Assurez‑vous d’avoir la version appropriée installée dans votre environnement.

### Q4 : Puis‑je personnaliser davantage les paramètres d’exportation selon mes exigences spécifiques ?

R4 : Absolument ! Le code fourni constitue un point de départ. Vous pouvez explorer des options et configurations supplémentaires dans la [documentation Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q5 : Où puis‑je obtenir de l’aide ou partager mes expériences avec Aspose.CAD pour .NET ?

R5 : Rejoignez la communauté Aspose.CAD sur le [forum](https://forum.aspose.com/c/cad/19) pour interagir avec d’autres développeurs et demander de l’assistance.

---

**Dernière mise à jour :** 2026-03-24  
**Testé avec :** Aspose.CAD 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}