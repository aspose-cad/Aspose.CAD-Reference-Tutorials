---
date: 2026-03-29
description: Apprenez à configurer les options de rasterisation CAD et à exporter
  des DGN en PDF avec prise en charge 3D à l'aide d'Aspose.CAD pour .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Configurer les options de rasterisation CAD pour DGN V7 3D
url: /fr/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Configurer les options de rasterisation CAD pour DGN V7 3D

## Introduction

Dans ce tutoriel complet, vous apprendrez **comment configurer les options de rasterisation CAD** pour exporter un fichier DGN V7 3‑D au format PDF en utilisant Aspose.CAD pour .NET. Que vous construisiez un visualiseur CAD, un outil de reporting ou une chaîne de conversion automatisée, maîtriser ces paramètres vous donne un contrôle précis sur la taille de la page, le redimensionnement de la mise en page, les couleurs d’arrière‑plan et les vues spécifiques que vous souhaitez rendre. Parcourons le processus étape par étape.

## Réponses rapides
- **Que signifie « configure CAD rasterization options » ?**  
  Il s’agit de définir des propriétés telles que les dimensions de la page, le redimensionnement, la couleur d’arrière‑plan et la sélection de la mise en page avant de convertir un fichier CAD en format raster (par ex., PDF).
- **Comment exporter un DGN en PDF avec prise en charge 3 D ?**  
  Chargez le DGN avec `DgnImage`, définissez `PdfOptions` + `CadRasterizationOptions`, puis appelez `Save`.
- **Ai‑je besoin d’une licence pour une utilisation en production ?**  
  Oui – une licence commerciale est requise pour le déploiement ; un essai gratuit est disponible.
- **Quelles versions de .NET sont prises en charge ?**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Puis‑je choisir des vues spécifiques à exporter ?**  
  Absolument – définissez le tableau `Layouts` dans les options de rasterisation.

## Qu’est‑ce que « configure CAD rasterization options » ?

Configurer les options de rasterisation CAD signifie personnaliser la façon dont un dessin CAD est rasterisé (converti de vecteur en bitmap ou PDF). En ajustant ces paramètres, vous contrôlez le rendu visuel, les performances et la taille du fichier du document résultant.

## Pourquoi utiliser Aspose.CAD pour l’exportation 3 D DGN V7 ?

- **Intégration .NET complète** – aucune dépendance COM ou DLL native requise.  
- **Prise en charge de la géométrie 3 D** – conserve les informations de profondeur lors du rendu en PDF.  
- **Contrôle granulaire** – choisissez les mises en page exactes, le redimensionnement et les couleurs d’arrière‑plan.  
- **Multiplateforme** – fonctionne sous Windows, Linux et macOS avec .NET Core.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Aspose.CAD pour .NET** – téléchargez‑le depuis [here](https://releases.aspose.com/cad/net/).  
- **Visual Studio** ou tout IDE .NET compatible.  
- **Un fichier DGN d’exemple** – pour ce guide, nous utiliserons `Nikon_D90_Camera.dgn` (inclus dans le pack d’exemples Aspose).  

Maintenant que tout est prêt, plongeons dans le code.

## Importer les espaces de noms

Dans votre projet .NET, importez les espaces de noms requis :

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Étape 1 : Configurer le répertoire du document

Créez une variable qui pointe vers le dossier où votre DGN source et les fichiers de sortie seront stockés.

```csharp
string MyDir = "Your Document Directory";
```

## Étape 2 : Charger le fichier DGN

Chargez le fichier DGN en tant que `DgnImage`. Cet objet vous donne accès aux données CAD et au pipeline de rasterisation.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Étape 3 : Configurer les options d’exportation PDF (Configurer les options de rasterisation CAD)

Ici, nous **configurons les options de rasterisation CAD** qui déterminent comment le modèle 3‑D est rendu en PDF. Vous pouvez ajuster la taille de la page, activer le redimensionnement automatique des mises en page, définir une couleur d’arrière‑plan et choisir les mises en page (vues) exactes que vous souhaitez exporter.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Étape 4 : Enregistrer l’image raster

Enfin, exportez le DGN vers un fichier PDF en utilisant les options que vous venez de configurer.

```csharp
dgnImage.Save(outFile, options);
```

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **Sortie PDF vide** | Vérifiez que le tableau `Layouts` contient les identifiants de vue corrects présents dans le fichier DGN. |
| **Couleurs incorrectes** | Assurez‑vous que `BackgroundColor` est défini sur la valeur souhaitée ; utilisez `Color.White` pour un arrière‑plan clair. |
| **Goulot d’étranglement de performance sur de gros fichiers** | Activez `AutomaticLayoutsScaling` et envisagez de réduire `PageWidth/PageHeight` pour une résolution raster plus petite. |
| **Exception de licence** | Installez une licence Aspose.CAD valide avant de charger l’image afin d’éviter les filigranes d’essai. |

## Questions fréquentes

**Q : Puis‑je utiliser Aspose.CAD pour .NET avec d’autres formats de fichiers CAD ?**  
R : Oui, Aspose.CAD prend en charge DWG, DXF, DWF, DGN et de nombreux autres formats.

**Q : Comment gérer les exceptions lors de l’utilisation d’Aspose.CAD ?**  
R : Enveloppez votre code dans un bloc `try‑catch` et inspectez `Aspose.CAD.CADException` pour obtenir des informations détaillées sur l’erreur.

**Q : Aspose.CAD est‑il adapté aux projets commerciaux ?**  
R : Absolument. Vous pouvez acheter une licence [here](https://purchase.aspose.com/buy).

**Q : Puis‑je essayer Aspose.CAD pour .NET avant d’acheter ?**  
R : Oui, un essai gratuit est disponible [here](https://releases.aspose.com/).

**Q : Où puis‑je trouver du support communautaire pour Aspose.CAD ?**  
R : Rejoignez le forum de discussion [here](https://forum.aspose.com/c/cad/19).

---

**Dernière mise à jour :** 2026-03-29  
**Testé avec :** Aspose.CAD 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}