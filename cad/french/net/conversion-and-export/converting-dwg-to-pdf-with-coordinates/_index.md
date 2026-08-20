---
date: 2026-04-03
description: Apprenez à définir la fenêtre d’affichage et à convertir DWG en PDF en
  C# avec Aspose.CAD. Ce tutoriel de conversion DWG en PDF montre une exportation
  précise avec les coordonnées.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: Conversion de DWG en PDF avec coordonnées en C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Comment définir le viewport lors de la conversion de DWG en PDF avec coordonnées
  en C# – Tutoriel Aspose.CAD
url: /fr/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Conversion de DWG en PDF avec coordonnées en C# - Tutoriel Aspose.CAD

## Introduction

Bienvenue dans ce tutoriel complet sur **how to set viewport** lors de la conversion de fichiers DWG en PDF avec des coordonnées spécifiées en utilisant Aspose.CAD pour .NET. En contrôlant le viewport, vous obtenez des PDF pixel‑perfect qui correspondent exactement à la zone dont vous avez besoin — idéal pour les plans de construction, les aperçus de plans d'étage ou tout flux de travail BIM.

## Réponses rapides
- **What does “set viewport” mean?** Il définit la région visible et l'échelle du dessin CAD lors de la rasterisation.  
- **Which library handles the conversion?** Aspose.CAD for .NET.  
- **Do I need a license?** Un essai gratuit fonctionne pour l'évaluation ; une licence commerciale est requise pour la production.  
- **Supported platforms?** Windows, Linux, and macOS with .NET 5/6/7 or .NET Framework 4.6+.  
- **Typical implementation time?** Environ 10‑15 minutes pour une conversion de base.

## Prérequis

Avant de commencer, assurez-vous de disposer des prérequis suivants :

- **Aspose.CAD Library** – Téléchargez et installez la bibliothèque Aspose.CAD pour .NET. Vous pouvez trouver la bibliothèque [ici](https://releases.aspose.com/cad/net/).
- **Development Environment** – Environnement de développement – Visual Studio, Rider, ou tout IDE supportant le développement .NET.
- **DWG File** – Fichier DWG – Disposez d'un fichier DWG prêt pour la conversion. Vous pouvez utiliser le fichier d'exemple fourni ou votre propre fichier DWG.

## Comment définir le viewport pour une exportation PDF précise

Définir le viewport est l'étape principale qui vous permet de spécifier la zone exacte du dessin que vous souhaitez rendre. Dans le code ci‑dessous, nous créons un nouveau `CadVportTableObject`, le positionnons avec la coordonnée en haut‑à‑gauche, et calculons la largeur, la hauteur et le rapport d'aspect. Il s'agit de l'implémentation **how to set viewport** qui pilote le reste de la conversion.

## Importer les espaces de noms

Dans votre projet C#, importez les espaces de noms nécessaires :

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

Décomposons le code étape par étape pour une meilleure compréhension :

## Étape 1 : Définir le répertoire du document

```csharp
string MyDir = "Your Document Directory";
```

## Étape 2 : Définir le chemin du fichier DWG source

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Étape 3 : Charger le fichier DWG et configurer les options de rasterisation

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Étape 4 : Définir les coordonnées et le viewport  

Ici, nous **set the viewport** (how to set viewport) en spécifiant le coin supérieur gauche, la largeur et la hauteur de la zone que vous souhaitez exporter.

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

## Étape 5 : Appliquer les paramètres du viewport

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

## Étape 6 : Configurer les options PDF et exporter  

Nous rassemblons maintenant tous les éléments et **convert DWG to PDF** en utilisant les options de rasterisation que nous venons de préparer.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Étape 7 : Afficher le message de succès

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Cas d'utilisation courants

- **Construction documentation** – Documentation de construction – Générer des PDF imprimables de sections spécifiques de plans d'étage.  
- **BIM coordination** – Coordination BIM – Exporter uniquement la zone d'intérêt pour la détection de conflits.  
- **Client presentations** – Présentations client – Fournir un PDF propre d'une pièce ou d'une élévation sélectionnée sans exposer le dessin complet.

## Conclusion

Félicitations ! Vous avez réussi à **convertir DWG en PDF** avec des coordonnées précises et avez appris **how to set viewport** en utilisant Aspose.CAD pour .NET. Ce **dwg to pdf tutorial** montre comment **create pdf from dwg** et **export dwg as pdf c#** tout en conservant le contrôle total sur la zone de sortie.

## FAQ

### Q1 : Puis‑je utiliser Aspose.CAD avec d'autres formats de fichiers CAD ?

R1 : Oui, Aspose.CAD prend en charge divers formats CAD, notamment DWG, DXF, DWF, et plus encore.

### Q2 : Comment gérer les erreurs pendant le processus de conversion ?

R2 : Implémentez des mécanismes de gestion des erreurs à l'aide de blocs try‑catch pour capturer et gérer les exceptions.

### Q3 : Aspose.CAD convient‑il aux environnements Windows et Linux ?

R3 : Oui, Aspose.CAD est compatible avec les plateformes Windows et Linux.

### Q4 : Puis‑je personnaliser davantage la sortie PDF ?

R4 : Bien sûr ! Explorez les nombreuses options offertes par Aspose.CAD pour adapter la sortie PDF à vos exigences spécifiques.

### Q5 : Où puis‑je trouver un support supplémentaire ou des discussions communautaires ?

R5 : Consultez le [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) pour le support communautaire et les discussions.

## Questions fréquemment posées supplémentaires

**Q : Cette approche fonctionne‑t‑elle avec de gros fichiers DWG (des centaines de Mo) ?**  
R : Oui. La rasterisation est effectuée page par page, et vous pouvez ajuster `rasterizationOptions` (par ex., `Resolution`) pour équilibrer qualité et utilisation de la mémoire.

**Q : Puis‑je exporter plusieurs viewports vers des pages PDF séparées ?**  
R : Vous pouvez parcourir `cadImage.ViewPorts`, activer chacun, appeler `Save` pour chaque page, puis fusionner les PDF avec Aspose.PDF.

**Q : Est‑il possible d’ajouter un filigrane au PDF généré ?**  
R : Après avoir enregistré le PDF, vous pouvez le rouvrir avec Aspose.PDF et appliquer un filigrane texte ou image avant de le livrer à l'utilisateur.

---

**Last Updated:** 2026-04-03  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}